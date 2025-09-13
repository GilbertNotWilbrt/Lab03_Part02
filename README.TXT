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

#28 print: 
    p1.print("report.pdf", true);
    p1.print("notes.txt", false);
    
    getStatus:
    p1.getStatus(5);
    p1.getStatus(0);
    
#29 Square, Triangle and Circle.

#30 changeSize(int, int)
    moveHorizontal(int)
    moveVertical(int)
    makeVisible()
    
#31 The picture class does not contain any internal method calls.

#32 The remainder is 2

#33 The result takes the sign of the dividend.

#34 0,1,2,3,4

#35 n can be any int
    m can be any nonzero integer
    
#36 private void updateDisplay()
{
    int rawHour = hours.getValue();
    int displayHour = rawHour % 12;
    if (displayHour == 0) {
        displayHour = 12;
    }
    String ampm = (rawHour < 12) ? "am" : "pm";
    displayString = displayHour + ":" + minutes.getDisplayValue() + ampm;
}

#37 Keep hours as 0–23 and converting to 12-hour with AM/PM in updateDisplay()
is easier and better because the clock remains simple, and the display is the 
only thing changing.