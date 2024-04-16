# VERSION ROUTINES

## Validation Routines

Validation routines are used to validate user inputs at field level and default values.

### Steps
1. Write, compile and catalog a subroutine
2. Create an entry in EB.API
3. Attach routine to a version:
   1. 58.x VALIDATION.FLD -> Name of field to be validated
   2. 59.x VALIDATION.RTN -> Name of the routine
4. (Optional) Make field hot validation - only for browsers:
   1. 13.x FIELD.NO -> Name of the field
   2. 42.x.1 ATTRIBS : HOT-FIELD