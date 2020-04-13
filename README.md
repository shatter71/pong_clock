Pong clock code that has been updated to allow the screen to be turned off between certain hours each day and also to be turned off all weekend.  Options can be used separately or together.

Instructables post on Pong Clock project:

https://www.instructables.com/id/Pong-Word-Clock/

Original code:

https://www.dropbox.com/s/mh8qzsms8gl3f34/pongclock5.1.zip

These are the variables to set if you want the display to turn off daily between certain hours or off for the entire weekend.  They values are defaulted to be ON. Set to zero if you want them defaulted to OFF.
int dark_mode = 1;                      // Track if clock is off in the evening
int weekend_mode = 1;                   // Track if clock is off for the entire weekend

These entries define what hour you want the LED panel to turn on and turn off (24 hour time)
int clock_off = 22;                     // Hour to turn display off (24 hrs)
int clock_on = 7;                       // Hour to turn display on (24 hrs)

Default brightness was set to 1 from 7 as the panel I used is very bright
byte brightness = 1;                    // Screen brightness - default is 15 which is brightest.

Panel display parameters...you will find to places in the code where the y and x values define whether or not the panel needs to be flipped to display properly.  The panels I used needed the x value set but not the y. These lines were added to the code as the original code did not have them but were referenced on the original author's webpage.
//y = 15-y; //flip display upside-down
x = 47-x; //flip display front to back
