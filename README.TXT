Project: clock-display
Authors: David Barnes and Michael Kölling

This project is part of the material for the book

   Objects First with Java - A Practical Introduction using BlueJ
   Seventh edition
   David J. Barnes and Michael Kölling

It is discussed in chapter 3.

To use this project, create an instance of class ClockDisplay. Then inspect this 
instance and leave the object inspector window open. With the inspector window open, 
call the object's methods, such as timeTick and setTime. Watch the 
"displayString" in the inspector.

The displayString field simulates the actual clock display device. Were this 
program running in a real clock, it would change the real, physical display 
hardware instead of this string. The timeTick method would be triggered once 
every minute by some timer hardware.

Everything else could be pretty much the same.


Note: This project does not implement adequate handling of errors.

#21 The clock starts at 00:00 because that is the default behavior.
And we haven't modified it or incremented its value.

#23 You would need to call the timeTick 60 times. 
You could also setTime(1, 0)

#24 NumberDisplay digit;
    digit = new NumberDisplay(10);
    
#25 Rectangle window;
    window = new Rectangle(5, 10);
    
#26 It creates a new ClockDisplay object which starts at the time you specify
with the paramters hour and minute.

It does it by creating two NumberDisplay objects. and then calls setTime(hour, minute).

#27 They both create two NumberDispla objects and ensure that displayString
is updated before object is ready to use.

There is no direct updateDisplay() in the second constructor as setTime(hour, minute)
already calls updateDisplay within it.