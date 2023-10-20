# EXPERIMENT-05 INTERFACING A 4X4 MATRIX KEYPAD AND DISPLAY THE OUTPUT ON LCD

## Aim: 
To Interface a 4X4 matrix keypad and show the output on 16X2 LCD display to ARM controller , and simulate it in Proteus
## Components required: 
STM32 CUBE IDE, Proteus 8 simulator .
## Theory:

![image](https://github.com/vasanthkumarch/EXPERIMENT--05-INTERFACING-A-4X4-MATRIX-KEYPAD-AND-DISPLAY-THE-OUTPUT-ON-LCD/assets/36288975/2a4a795e-1674-4329-ae07-3f5e8d5073e2)

4×4 Keypad Module Pin Diagram
 
4x4 Keypad module Pin Diagram
4×4 Keypad module Pin Diagram
Pin Number	Pin Name	Description
1	R1	Taken out from 1st  ROW
2	R2	Taken out from 2nd  ROW
3	R3	Taken out from 3rd  ROW
4	R4	Taken out from 4th  ROW
5	C1	Taken out from 1st  COLUMN
6	C2	Taken out from 2nd COLUMN
7	C3	Taken out from 3rd  COLUMN
8	C4	Taken out from 4th  COLUMN
4×4 Matrix Keypad Module Hardware Overview
These Keypad modules are made of thin, flexible membrane material. The 4 x4 keypad module consists of 16 keys, these Keys are organized in a matrix of rows and columns. All these switches are connected to each other with a conductive trace. Normally there is no connection between rows and columns. When we will press a key, then a row and a column make contact.

## Procedure : 
 ## LCD 16X2 
   16×2 LCD is named so because; it has 16 Columns and 2 Rows. There are a lot of combinations available like,
   8×1, 8×2, 10×2, 16×1, etc. But the most used one is the 16*2 LCD, hence we are using it here.

All the above mentioned LCD display will have 16 Pins and the programming approach is also the same and hence the choice is left to you. 
Below is the Pinout and Pin Description of 16x2 LCD Module:

![image](https://user-images.githubusercontent.com/36288975/233858086-7b1a88a2-f941-475c-86c2-b3bae68bdf7e.png)
![image](https://user-images.githubusercontent.com/36288975/233857710-541ac1c2-786c-4dfc-b7b5-e3a4868a9cb6.png)
![image](https://user-images.githubusercontent.com/36288975/233857733-05df5dbf-1a1e-479e-85bb-8014a39ad878.png)

4-bit and 8-bit Mode of LCD:

The LCD can work in two different modes, namely the 4-bit mode and the 8-bit mode. In 4 bit mode we send the data nibble by nibble, first upper nibble and then lower nibble. For those of you who don’t know what a nibble is: a nibble is a group of four bits, so the lower four bits (D0-D3) of a byte form the lower nibble while the upper four bits (D4-D7) of a byte form the higher nibble. This enables us to send 8 bit data.

Whereas in 8 bit mode we can send the 8-bit data directly in one stroke since we use all the 8 data lines.

 8-bit mode is faster and flawless than 4-bit mode. But the major drawback is that it needs 8 data lines connected to the microcontroller. This will make us run out of I/O pins on our MCU, so 4-bit mode is widely used. No control pins are used to set these modes. 
 LCD Commands:

There are some preset commands instructions in LCD, which we need to send to LCD through some microcontroller. Some important command instructions are given below:

Hex Code

Command to LCD Instruction Register

0F

LCD ON, cursor ON

01

Clear display screen

02

Return home

04

Decrement cursor (shift cursor to left)

06

Increment cursor (shift cursor to right)

05

Shift display right

07

Shift display left

0E

Display ON, cursor blinking

80

Force cursor to beginning of first line

C0

Force cursor to beginning of second line

38

2 lines and 5×7 matrix

83

Cursor line 1 position 3

3C

Activate second line

08

Display OFF, cursor OFF

C1

Jump to second line, position 1

OC

Display ON, cursor OFF

C1

Jump to second line, position 1

C2

Jump to second line, position 2
 
## Procedure:
Select a new STM32 Project.

Select GPIO Ports
```

  PC0 , PC1 , PC2 , PC3 , PA0 , PA1 , PA2 , PA3 , PB0 , PB1  -> Output

  PC4 , PC5 , PC7 , PC8  -> Input
```
Configure the Input Ports at Pull up Mode followed by generating the code.

Build Debug and Create 'hex.file'

Open a new Proteus Project.

Select STM32F401RB, LCD 16*2 and Keypad.

Connect PA0 to D7 , PA1 to D6 , PA2 to D5 , PA3 to D4 , PB0 to RS , PB1 to E , PC0 to r1 , PC1 to r2 , PC2 to r3 , PC3 to r4 , PC4 to c1 , PC5 to c2 , PC6 to c3 and PC7 to c4.

Check the execution of the output using Run Option.
## STM 32 CUBE PROGRAM :

## Output screen shots of proteus  :

![Screenshot 2023-10-20 143221](https://github.com/Vanitha-SM/EXPERIMENT--05-INTERFACING-A-4X4-MATRIX-KEYPAD-AND-DISPLAY-THE-OUTPUT-ON-LCD/assets/119557985/29190e88-f423-4ce8-be48-bfeefe67d7d1)

 ![image](https://github.com/Vanitha-SM/EXPERIMENT--05-INTERFACING-A-4X4-MATRIX-KEYPAD-AND-DISPLAY-THE-OUTPUT-ON-LCD/assets/119557985/13b359ac-8c55-456d-a0a3-4a637f8aa06f)

 ## CIRCUIT DIAGRAM (EXPORT THE GRAPHICS TO PDF AND ADD THE SCREEN SHOT HERE): 
 ![image](https://github.com/Vanitha-SM/EXPERIMENT--05-INTERFACING-A-4X4-MATRIX-KEYPAD-AND-DISPLAY-THE-OUTPUT-ON-LCD/assets/119557985/6c1e9360-c744-4c12-b2d7-ccd86b3d33bc)

 
## Result :
Interfacing a 4x4 keypad with ARM microcontroller are simulated in proteus and the results are verified.
