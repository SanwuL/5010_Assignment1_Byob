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
00 - Point/Line
01 - Circle
10 - Triangle
11 - Square

Word 3: Operation (4 bits)
The operation is specified using two two-bit words:

First two bits: Extension Mode
00 - Center (no extension)
01 - Horizontal (include right neighbor)
10 - Vertical (include down neighbor)
11 - Diagonal (include down-right neighbor)

Last two bits: Mirror Mode
00 - No mirror
01 - Vertical mirror
10 - Horizontal mirror
11 - Central mirror (180° rotation)
