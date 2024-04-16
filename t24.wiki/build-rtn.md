# Enquiry Routines

## Build Routines

Build routines are used to manipulate selection criteria in the enquiry.
Build routines accepts one dynamic array as parameter:

- <1>: Name of the enquiry
- <2>: Selection Field Names
- <3>: Operands
- <4>: Values

### Steps

1. Write, compile, catalog subroutine
2. Attach subroutine to the field `12.x BUILD.ROUTINE`

## Assignment

Create an enquiry to display a "List of current and savings accounts".
The accounts should be in these categories:

`1001 1002 1003 1004 1005 1006 6001 6002 6003 6004 6005 6006 6007`.

Following is the report format:

---

| Id    | Account Title   | Category        | Currency | Working Balance |
| ----- | --------------- | --------------- | -------- | --------------- |
| 10715 | MICHAEL DELL    | Current Account | EUR      | 37756.58        |
| 10723 | MICHAEL DELL    | Current Account | GBP      | 205415.77       |
| 10968 | WARREN BUFFET   | Current Account | EUR      | 4916300.66      |
| 10995 | COCA-COLA       | Current Account | USD      | -16573212.37    |
| 19666 | MICROSOFT       | Savings Acct 1  | USD      | 1249825         |
| 40274 | AARON NIYONZIMA | Current Account | USD      | 4662711         |
