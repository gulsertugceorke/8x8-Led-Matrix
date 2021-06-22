# 8x8-Led-Matrix
In this project, the text entered by the user is shifted using the dot matrix (max7219).
MaxMatrix library is used. First, I define the characters to be used one by one. 
After the character definitions were finished, I showed which pin was related to what.
VCC connected to 5 volts. GND connected to GND pin. DIN connected to 7th pin. 
CS connected to 5th pin and also CLK connected to 6th pin.   
The maxInUse command in the code shows the number of modules used.
I wrote 1 because one module is used in this project.
MaxMatrix m(DIN, CS, CLK, maxInUse) command creates matrix object.
char text[]= "TUGCE ORKE"; command contains text to scroll.
m.init command is used to initialize the matrix(Max7219).
m.setIntensity(15) command used for the intensity of the dot matrix(takes values between 0 to 15).
printStringWithShift(text, 150) command means first one is text and second one is scrolling speed.
Below the code, printing operations are done in this section and This process continues until the letters in the text is finished.
m.shiftLeft command used to move text left. 
printStringWithShift function separates the entered text into individual letters  then it sends these letters to the printstringwithshift function as well.
