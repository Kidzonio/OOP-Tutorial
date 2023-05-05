# OOP-Tutorial
**Util Lib of OOP**

# Object Definition.

* Material or abstract thing that can be perceived by the senses and described through its characteristics, behaviors and current **states**.

# What is Object?

## Example using a pen:

Attributes:
color, load, capped, weight

Methods:
draw, cover, uncover

State.

**EVERY OBJECT HAS ATTRIBUTE, METHODS AND STATE.**

Instantiate = Generate **object** from a **class**;
Class = "classification", planning of an object;

Class:
* Defines common **attributes** and methods that will be shared by an **object**.

Object:
* It is an **instance** of a **class**.

### Example:

```lua
local instance -- will be our object

class 'Pen' {
    constructor = function (self)
        self.Opened = false; -- Pen State
        self.Charge = 100; -- Pen charge amount
        self.Weight = 10; -- Pen Weight ( In Grams )
        self.Color = 'Blue'; -- Pen Color
    end,

    openPen = function (self)
        if not (self.Opened) then
            self.Opened = true;
            print 'Pen Opened Successfully!';
            return true;
        end
        print 'Unable to open an already opened pen';
    end,

    closePen = function (self)
        if (self.Opened) then
            self.Opened = false;
            print 'Pen Closed Successfully!';
            return true;
        end
        print 'Unable to close an already closed pen';
    end,

    drawPen = function (self)
        if (self.Opened) then
            if (self.Charge ~= 0) then
                print 'You drew with your pen!';
                return true;
            end
            print 'Unable to draw with an empty pen';
        end
    end;

};

instance = new 'Pen' (); -- Instantiation of the 'Pen' class
```
