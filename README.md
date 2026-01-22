# 5010_Assignment1_Byob
IMGD_5010_Assignment

Each drawing command consists of three binary words. A complete program is a sequence of these commands.

Word 1: Position (4 bits)
The position is specified using two two-bit words:

First two bits: Row

00 - Row 1 (Top)

01 - Row 2

10 - Row 3

11 - Row 4 (Bottom)

Last two bits: Column

00 - Column 1 (Left)

01 - Column 2

10 - Column 3

11 - Column 4 (Right)

Word 2: Shape (2 bits)
(Each shape is drawn within the bounds of a single cell unless extended by an extension mode.)

00 - Point/Line

01 - Circle

10 - Triangle (Triangles point upward by default.)

11 - Square

Word 3: Operation (4 bits)
The operation is specified using two two-bit words:

First two bits: Extension Mode
(Extension modes include exactly one neighboring cell in the specified direction.)

00 - Center (no extension)

01 - Horizontal (include right neighbor)

10 - Vertical (include down neighbor)

11 - Diagonal (include down-right neighbor)

Last two bits: Mirror Mode
(Mirror operations are performed with respect to the starting position specified in Word 1.
The starting cell acts as the mirror anchor point.
When a mirror mode is applied, the original shape is replaced by its mirrored version.)

00 - No mirror

01 - Vertical mirror

10 - Horizontal mirror

11 - Central mirror (180° rotation)



Example:

0001 01 0000

0101 11 1000

1001 11 1000

0101 00 1110

0101 00 1101

<img width="508" height="465" alt="image" src="https://github.com/user-attachments/assets/62754b0c-e291-4972-ba56-dd98f0218063" />

Challenge:
Write the code in the language that will draw the content shown in the image below.

<img width="515" height="477" alt="image" src="https://github.com/user-attachments/assets/72da68dc-b2ba-4169-8bc7-74ef32b88fee" />
