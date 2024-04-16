# Structure of Subroutine

A subroutine starts with a key word `SUBROUTINE` followed by the name of the routine. Parameters (both inwards and outwards) are optional.

```jbc
SUBROUTINE MY.T24.ROUTINE(in_params, out_params)
*------------------------------------------------------------------
* The purpose of the routine
*------------------------------------------------------------------
* Developer: Joe Doe(joe.doe@rintocode)
* Date     : 28/10/2020
* Version  : 0.0.1
*------------------------------------------------------------------
    $INSERT I_COMMON
    $INSERT I_EQUATE
    
* add your code here

    RETURN
END
```

You need to put the keyword `RETURN` towards the end of your return.
