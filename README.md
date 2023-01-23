# ExcelRefTypes

 The difference between absolute, relative and mixed references

    Relative references    A relative cell reference in a formula, such as A1, is based on the relative position of the cell that contains the formula and the cell the reference refers to. If the position of the cell that contains the formula changes, the reference is changed. If you copy or fill the formula across rows or down columns, the reference automatically adjusts. By default, new formulas use relative references. For example, if you copy or fill a relative reference in cell B2 to cell B3, it automatically adjusts from =A1 to =A2.

    Copied formula with relative reference   
    Copied formula with relative reference

    Absolute references    An absolute cell reference in a formula, such as $A$1, always refer to a cell in a specific location. If the position of the cell that contains the formula changes, the absolute reference remains the same. If you copy or fill the formula across rows or down columns, the absolute reference does not adjust. By default, new formulas use relative references, so you may need to switch them to absolute references. For example, if you copy or fill an absolute reference in cell B2 to cell B3, it stays the same in both cells: =$A$1.

    Copied formula with absolute reference   
    Copied formula with absolute reference

    Mixed references    A mixed reference has either an absolute column and relative row, or absolute row and relative column. An absolute column reference takes the form $A1, $B1, and so on. An absolute row reference takes the form A$1, B$1, and so on. If the position of the cell that contains the formula changes, the relative reference is changed, and the absolute reference does not change. If you copy or fill the formula across rows or down columns, the relative reference automatically adjusts, and the absolute reference does not adjust. For example, if you copy or fill a mixed reference from cell A2 to B3, it adjusts from =A$1 to =B$1.

    Copied formula with mixed reference   
    Copied formula with mixed reference
