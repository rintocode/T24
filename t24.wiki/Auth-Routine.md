# VERSION ROUTINES

## Authorization Routines

Authorization routines are invoked at the authorization stage. They can be used to trigger custom actions (such as generating transaction advice,etc) when a record is authorized.

### Steps
1. Write, compile and catalog a subroutine
2. Create an entry in EB.API
3. Attach routine to a version:
   64.x AUTH.ROUTINE -> Name of the routine
