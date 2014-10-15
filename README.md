ECE382_Lab_3
============

#The objective of this Lab was to draw a 8x8 block on an LCD screen, and then move the said block by using the directional keys on the nokia display

###Prelab

The different charts in the Prelab were filled out below by referencing the several datasheets and manuals on the course website.

![alt text](http://i61.tinypic.com/k4cn5f.png)

The waveform of the different signals can be seen in a rough sketch provided below.

###Lab

To do the logic analyzer portion of the lab, the following setup, provided from the lab instructions were used below.

![alt text](http://i59.tinypic.com/34858xd.png)

We ended up analyzing several different signals. The table below shows what specific lines of the Nokia code did with regards to registers and the overall purpose of the line.

![alt text](http://i59.tinypic.com/rlds7q.jpg)

Another table was made to help analyze what happened when SW3 was pressed. The SW3 waveform analysis can be seen below

![alt text](http://i59.tinypic.com/f4p7v7.png)

A picture of the entire waveform can be seen below

![alt text](http://i58.tinypic.com/rlazxs.png)

The picture below is of the waveform at line 66

![alt text](http://i59.tinypic.com/1hp4q8.png)

The picture below is of the waveform at line 276

![alt text](http://i62.tinypic.com/2rm6p0k.png)

The picture below is of the waveform at line 288

![alt text](http://i62.tinypic.com/vqnz1k.png)

The picture below is of the waveform at line 294

![alt text](http://i60.tinypic.com/24m9wg9.png)

The picture below is of the waveform when a reset occurs. The reset took about 19.4 ms

![alt text](http://i62.tinypic.com/2yv1hfa.png)

###Writing Modes

![alt text](http://i60.tinypic.com/35mr0pw.png)

###Required Functionality

![alt text](http://i58.tinypic.com/ige1xe.png)

The code above was where most of the changes were made to the original code in order to get required functionality. The code essentially took the original code that drew a broken line, filled the line in, and then ended up looping itself to draw the line 8 more times.

###A Functionality

![alt text](http://i61.tinypic.com/24vv4eo.png)

The above code is an example  of the 4 different checks that were in place to determine the direction of a button. Left would check for a left button press, and the check for a right buton press if a left press was not there. The right press in turn would check for a up press, the up press would then check for a down, and the down would check for left again. This cycle would keep running to determine the direction of a button that was pressed, and would then move the box in the said direction by deleting the box and drawing a new one. The constant LEFTB was defined along with the rest (UPB, DOWNB, RIGHTB) in the beginning of the program as .equ statements.

###Debugging

Most of my problems were with syntax. I did not always put the '#' sign in front of my subroutines/constants. I also tended to forget which case of the labels to put down, e.g. left instead of Left. Other than the syntax errors, the biggest challenge was learning how to increment and decrement the column and row registers.

###Documentation

For the Prelab, C2C Leaf, Thompson, and I worked together to try understanding the booklets and we would usually talk about our best guess for what some of the values meant. 

For the Lab, C2C Leaf helped explain to me that the Lab was more about understanding the code rather than trying to start rewriting the whole Nokia code. He also reminded me that for required functionality, you only need to make a small change to the already present code.

C2C Thompson and Terragnoli helped explain how the logic analyzer worked. C2C Thompson in further detail recommended that for checking button presses I should have a 4 way check that loops into itself. He also helped me out with the counters for the rows

