# Excel Reference Types

 The difference between absolute, relative and mixed references

### Relative references    
A relative cell reference in a formula, such as A1, is based on the relative position of the cell that contains the formula and the cell the reference refers to. If the position of the cell that contains the formula changes, the reference is changed. If you copy or fill the formula across rows or down columns, the reference automatically adjusts. By default, new formulas use relative references. For example, if you copy or fill a relative reference in cell B2 to cell B3, it automatically adjusts from =A1 to =A2.

### Absolute references    
An absolute cell reference in a formula, such as $A$1, always refer to a cell in a specific location. If the position of the cell that contains the formula changes, the absolute reference remains the same. If you copy or fill the formula across rows or down columns, the absolute reference does not adjust. By default, new formulas use relative references, so you may need to switch them to absolute references. For example, if you copy or fill an absolute reference in cell B2 to cell B3, it stays the same in both cells: =$A$1.

### Mixed references    
A mixed reference has either an absolute column and relative row, or absolute row and relative column. An absolute column reference takes the form $A1, $B1, and so on. An absolute row reference takes the form A$1, B$1, and so on. If the position of the cell that contains the formula changes, the relative reference is changed, and the absolute reference does not change. If you copy or fill the formula across rows or down columns, the relative reference automatically adjusts, and the absolute reference does not adjust. For example, if you copy or fill a mixed reference from cell A2 to B3, it adjusts from =A$1 to =B$1.

Making a reference to a cell or a range of cells on another worksheet in the same workbook

In the following example, the AVERAGE function calculates the average value for the range `B1:B10` on the worksheet named Marketing in the same workbook.
Sheet eg `=AVERAGE(Marketing!B1:B10)`

1. Refers to the worksheet named Marketing

2. Refers to the range of cells from B1 to B10

3. The exclamation point (!) Separates the worksheet reference from the cell range reference

### The 3-D reference style

Conveniently referencing multiple worksheets    If you want to analyze data in the same cell or range of cells on multiple worksheets within a workbook, use a 3-D reference. A 3-D reference includes the cell or range reference, preceded by a range of worksheet names. Excel uses any worksheets stored between the starting and ending names of the reference. For example, =SUM(Sheet2:Sheet13!B5) adds all the values contained in cell B5 on all the worksheets between and including Sheet 2 and Sheet 13.

You can use 3-D references to refer to cells on other sheets, to define names, and to create formulas by using the following functions: SUM, AVERAGE, AVERAGEA, COUNT, COUNTA, MAX, MAXA, MIN, MINA, PRODUCT, STDEV.P, STDEV.S, STDEVA, STDEVPA, VAR.P, VAR.S, VARA, and VARPA.

3-D references cannot be used in array formulas.

3-D references cannot be used with the intersection operator (a single space) or in formulas that use implicit intersection.

What occurs when you move, copy, insert, or delete worksheets    The following examples explain what happens when you move, copy, insert, or delete worksheets that are included in a 3-D reference. The examples use the formula =SUM(Sheet2:Sheet6!A2:A5) to add cells A2 through A5 on worksheets 2 through 6.

Insert or copy    If you insert or copy sheets between Sheet2 and Sheet6 (the endpoints in this example), Excel includes all values in cells A2 through A5 from the added sheets in the calculations.

Delete     If you delete sheets between Sheet2 and Sheet6, Excel removes their values from the calculation.

Move    If you move sheets from between Sheet2 and Sheet6 to a location outside the referenced sheet range, Excel removes their values from the calculation.

Move an endpoint    If you move Sheet2 or Sheet6 to another location in the same workbook, Excel adjusts the calculation to accommodate the new range of sheets between them.

Delete an endpoint    If you delete Sheet2 or Sheet6, Excel adjusts the calculation to accommodate the range of sheets between them.
    
### The R1C1 reference style

You can also use a reference style where both the rows and the columns on the worksheet are numbered. The R1C1 reference style is useful for computing row and column positions in macros. In the R1C1 style, Excel indicates the location of a cell with an "R" followed by a row number and a "C" followed by a column number.

| Reference | Meaning |
| --- | --- |
| R[-2]C | A relative reference to the cell two rows up and in the same column |
| R[2]C[2] | A relative reference to the cell two rows down and two columns to the right |
| R2C2 | An absolute reference to the cell in the second row and in the second column |
| R[-1] | A relative reference to the entire row above the active cell |
| R | An absolute reference to the current row |

When you record a macro, Excel records some commands by using the R1C1 reference style. For example, if you record a command, such as clicking the AutoSum button to insert a formula that adds a range of cells, Excel records the formula by using R1C1 style, not A1 style, references.

You can turn the R1C1 reference style on or off by setting or clearing the R1C1 reference style check box under the Working with formulas section in the Formulas category of the Options dialog box. To display this dialog box, click the File tab.
