---
Title: "Excel"
draft: true
---

# Excel

- [Excel Easy](https://www.excel-easy.com/)

## You Suck At Excel

https://www.youtube.com/watch?v=0nbkaYsR94c

Notes from “You Suck at Excel” with Joel Spolsky

Joel Spolsky has a great YouTube video called “You Suck at Excel”, where he explains a bunch of great Excel tips and best practices to employees at his companies.

I’m pretty experienced with Excel, but I learned a ton from this. If you don’t have an hour to spare, here are my notes, with a few tips of my own interspersed:
“Riding the range”

    “Riding the range” means fill a column down based on the top cell to the bottom of adjacent columns. There are lots of ways to do this:
        Select the top cell and double-click the “fill handle” in the lower right-hand corner.
        Select the top cell and drag the handle in the lower right-hand corner down.
        Select the column you want to fill, including the top cell that the column should be based on, and press ctrl-d.

Formulas

    Excel users R1C1 reference style internally, which assigns numbers to both rows and columns, rather than A1 (“baby mode”), which uses letters for columns. Turning on R1C1 mode will help explain how Excel works with references to other cells in formulas (relative vs. absolute references).
    ctrl-` will toggle between seeing formulas and values
    When selecting a column, drag the fill handle from the bottom to the top to erase cells.
    Use $ to change relative cell references in formulas in A1 mode to absolute references that won’t change if you paste the formula. Think of the $ as an anchor.
        cmd-t on Mac or F4 on Windows when editing a formula will cycle the reference under your cursor between relative and absolute.

Resizing columns

    Double click on a column border in the heading (where it says A, B, etc. at the top of the spreadsheet) to autosize.
    You can select multiple columns and double click the border of one to autosize all.
    You can select multiple columns and drag the border to resize one of them. This will give all the selected columns the same size.
    Note: All this works with row heights too.

Entering data

    Select a range of cells and start typing. Then hit enter and it will jump to the next selected cell.
        Hit ctrl-enter and the range will be filled from the selected cell.
    Enter 1 in a cell and 2 in the cell directly below. Then select these cells and drag the fill handle down (lower right corner of the selection box). It will continue the series of numbers.
        Right-click drag the fill handle to get a list of options for how Excel should fill.
        You can do this with days of the week, dates, and lots of stuff. (Joel shows an example using the last day of the month, which Excel can figure out from 1/31/13 and 2/28/13.

Pasting

    You usually want to Paste Values rather than the default paste, which includes formats and formulas.
    Use the “Paste special” menu to do lots of fun stuff like:
        Adding a number in the clipboard to a bunch of cells
        Transposing tables (swap columns and rows).

Formatting

    Paint formats: you can format one cell, and then use the “paint formats” paintbrush to copy this format onto other cells.
    Put an apostrophe (’) in front of a number to format it as text. You can also do this with right click > Format cell… and change the cell type in the “Number” tab to “text”.
        Note: cmd-1 on the Mac will open this menu.

Selecting

    cmd-a on Mac and ctrl-a on Windows will select the current table.
        Note: Press it again to select the entire worksheet.
    Note: cmd-shift-down on Mac and ctrl-shift-down on Windows will select down a column to the last contiguous value.

Naming cells

    This allows you to assign a name to a cell, rather than referring to it as A1 or D24. Jump to 25:54 in the video to see this.
    You can name an entire column or row in the same way.
    To delete names, go to Insert > Name > Define…

Lookups

    Never use vlookup (it’s hard to parse the formulas; slow; confusing)
    Use index and match, which are faster and self-documenting compared to vlookup: =index(LookupValues, match(Value, LookupLabels))
    You have to sort the LookupLabels by name for match to work.

“Tables”

    Excel-only feature
    Jump to 37:45 to see this
    Allows you to add in new rows without messing up formulas (this often happens when you insert new rows in the middle of a non-table)
    Auto-names columns based on headers
    Auto-fills formulas down columns
    Makes lookups between tables easier
    Note: tables must be surrounded by whitespace, via @jswright61.

Excel features no one knows about

    There is a Goal Seek feature that will let you set one value in your spreadsheet based on another cell. Jump to 47:50 to see this in action.
    There is a Pivot Table feature that lets you aggregate and summarize data. Jump to 50:14 to see this in action.

Miscellaneous

    ctrl-; will insert today’s date in a cell
    cmd-shift-5 formats current cell as percentage
    cmd-shift-4 formats current cell as currency
    Make all column headers center-aligned. (Note: I disagree with this. Left-align the headers for text columns; right-align the headers for number columns.)
    Round currency using =round() to avoid sums being wrong (if you don’t do this, $0.024 + $0.024 = $0.048 will look like $0.02 + $0.02 = $0.05).
    There’s a convention to format calculated cells (cells with formulas) differently from normal cells so people don’t accidentally overwrite the formulas. There’s a built-in Cell Style for this.
