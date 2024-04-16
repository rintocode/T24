# Auto New Content Routines

Used to automatically populate content of a field when a record is opened.

## Requirements
The bank would like to have account MNEMONIC automatically generated and populated for all newly created accounts using the version `ACCOUNT,MTD.NEW.AC`. Your assignment is to adapt this version based on these business requirements. Mnemonics are to be generated in this format: `AAAANNNNAA`

## Solution

1. [ ] Create a subroutine
2. [ ] Create a record in PGM.FILE of type `S`, define product(e.g `EB`) and `APPL.FOR.SUB` (e.g AC) 
3. [ ] Define `AUTOM.FIELD.NO`
4. [ ] Add our routine in `AUT.NEW.CONTENT` prefixed by `@`