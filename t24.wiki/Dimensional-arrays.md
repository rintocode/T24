# Dimensional Arrays

Dimensioned arrays are `Matrix` and `Vectors` in other programming languages.

Bellow is an example:

```basic
PROGRAM Arrays
    rows = 2
    cols = 3
    DIM arr(rows, cols)     ;* declaring matrix 2x3

*-- Matrix --
*  1 2 3
*  4 5 6
*------------
    arr(1, 1) = 1
    arr(1, 2) = 2
    arr(1, 3) = 3
    arr(2, 1) = 4
    arr(2, 2) = 5
    arr(2, 3) = 6

    CRT @(-1)       ;* Clear the screen

    FOR i = 1 TO rows
        FOR j = 1 TO cols
            CRT @(j, i) : arr(i, j)
        NEXT j
    NEXT i

* Convert dimensioned array to dynamic array
    MATBUILD arr2 FROM arr USING ","
    PRINT arr2      ;* 1, 2, 3, 4, 5, 6

END
```
