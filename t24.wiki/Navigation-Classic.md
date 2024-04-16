# TEMENOS T24 FOUNDAMENTALS

## Navigation Through Classic Interface

## Agenda
1. Access to jshell
2. Login to T24
3. Layout of the interface
4. Commands and Keyboard Shortcut Keys
5. Working with Multi-Valued fields
6. Functions
7. Useful tips
   - List and copy records from linked table
   - Display help
   - Customizing your terminal

&nbsp;

### Access to jshell

`jsh t24 ~ -->`
&nbsp;  
&nbsp; 

### Login to T24

```
jsh t24 ~ -->ETS

Terminal type set to EBS-JBASE

jsh t24 ~ -->EX

GLOBUS Rev. R08.000     SIGN.ON         Copyright (c) Temenos Systems Ltd 2021


 ------------------------------------------------------------------------------
      $$$$$$$$$$ $  $ $ $$   $$$$$        $$$$$    $$$ $$$$$$$$$$$$$$$$$$$$
     $$$$$$$$$$$$$$$$$$ $$$  $$$   $     $$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$
      $$$$$$$$$$$$$$   $$    $$         $$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$
       $    $$$$$$$$   $$$$           $  $$  $$$$$$$$$$$$$$$$$$$$$$    $$
             $$$$$$$$$$$$$$$         $$ $$$$$$$$$$$$$$$$$$$$$$$$$$$   $
              $$$$$$$$$$$$ $           $$$$$$$$$$$$$$$$$$$$$$$$$$$$
              $$$$$$$$$$$            $$  $$$$  $$ $$$$$$$$$$$$$$$  $
               $$$$$$$$$             $$$$     $$$$$$$$$$$$$$$$$ $ $
                 $$$                $$$$$$$$$$$$$$$$$$$$$$$$$$$
                   $$$$             $$$$$$$$$$$$$    $$   $$$  $
                       $$$$$$        $$$$$$$$$$$$          $  $
                       $$$$$$$$$         $$$$$$            $ $$   $$$
                        $$$$$$$          $$$$$$ $              $$$$$
                         $$$$$            $$$$  $            $$$$$$$$
                         $$$                $$                $$  $$$     $
                        $$                                               $
 ------------------------------------------------------------------------------
 10 JAN 2021 09:36:54  USER                            [60,IN]
 ACTION
 PLEASE ENTER YOUR SIGN ON NAME
```
### Layout of the interface
1. Instruction bar
2. Action box
3. Details and functions
4. Record Id
3. Application description and function name

```
R8 MODEL BANK           USER PROFILE INPUT

     USER.ID........... AARON2
 ------------------------------------------------------------------------------
   1 USER.NAME......... AARON NIYONZIMA
   2 SIGN.ON.NAME...... AARON02
   3 CLASSIFICATION.... INTERNAL
   4 LANGUAGE.......... 1                   English
   5. 1 COMPANY.CODE... GB0010001           R8 MODEL BANK
   5. 2 COMPANY.CODE... SG0010001           R8 LEAD CO SINGAPORE
   5. 3 COMPANY.CODE... EU0010001           R8 LEAD CO GERMANY
   5. 4 COMPANY.CODE... GB0010002           MF LEAD COMPANY
   5. 5 COMPANY.CODE... GB0010003           MF BRANCH 1
   5. 6 COMPANY.CODE... GB0010004           MF BRANCH 2
   6 DEPARTMENT.CODE... 1                   Implementation
   7 PASSWORD.VALIDITY. 01 FEB 2021 M0601   01 FEB 2021 Every 6 months on day 1
   8 START.DATE.PROFILE 01 JAN 1985
   9 END.DATE.PROFILE.. 31 DEC 2049
  10. 1 START.TIME..... 00:01
  11. 1 END.TIME....... 23:59
 ------------------------------------------------------------------------------
 10 JAN 2021 11:54:12  USER (09 JAN) AARON1            [60,IN] PAGE 1   >>>6>>>
 ACTION
 AWAITING PAGE INSTRUCTIONS
```
&nbsp; 
&nbsp;
### Commands and Keyboard Shortcut Keys

| Actions            | Commands(keys)       | Mapped keys|
|--------------------|----------------------|------------|
| Move to the Next   | CRTL+F+ENTER         |  F3        |
| Go to the Previous | CRTL+B+ENTER         |  F2        |
| Commit / Validate  | CRTL+V+ENTER         |  F5        |
| Quit w/t saving    | CRTL+U+ENTER         |  ESC       |
| Move to the last   | CRTL+E+ENTER         |  F4        |
| ---                | --                   | --         |
|Move to the field   | Field# (eg. 3 or 4.1 or 5.2.1)|
|                    |

&nbsp; 
&nbsp; 
### Working with Multi-Valued fields

| Action                              |   Key    |
|-------------------------------------|----------|
| Extend multi valued field           |    `<`   | 
| Extend multi valued field above     |    `>`   |
| Extend sub valued field before      |    `(`   | 
| Extend sub valued field above       |    `)`   |
| Delete multi/sub value              |    `-`   |
|                                     |          |

&nbsp; 
&nbsp; 

### Functions

| Functions                  |   Keys   | 
|----------------------------|----------|
| View                       |    S     |
| Input (create or modify)   |    I     |
| Authorize                  |    A     |   
| Delete                     |    D     |
| Copy                       |    C     |     
| Reverse                    |    R     |
| Verify                     |    V     |
| List live records          |    L     |
| List exceptions            |    E     |
|                            |          |
&nbsp; 
&nbsp; 
### List records of linked table
```
R8 MODEL BANK           USER PROFILE INPUT

     USER.ID........... AARON1
 ------------------------------------------------------------------------------
 R8 MODEL BANK            LANGUAGE - Default List

    LAN  MNEMONIC  DESCRIPTION                          RECORD.STATUS    FUNCT.
 ------------------------------------------------------------------------------
 1    1  GB        English
 2    2  FR        French
 3    3  DE        German
 4    4  ES        Spanish








 ------------------------------------------------------------------------------
 10 JAN 2021 17:16:01  USER (09 JAN) AARON1            [60,IN] PAGE   1 >>>1>>>
 ACTION
 AWAITING PAGE INSTRUCTIONS
```
&nbsp; 
&nbsp; 
### Display help
```
 R8 MODEL BANK           USER PROFILE INPUT

            FIELD NO 3 = CLASSIFICATION
 ------------------------------------------------------------------------------
   Indicates whether the User is 'Internal', i.e. an
   employee of the bank using GLOBUS., or 'External',
   i.e. a customer.
   __________________________________________________

      (1) 1-3 uppercase alpha characters:
          I, IN or INT for an employee of the bank
          E, EX or EXT for a customer.
          (Mandatory input)







 ------------------------------------------------------------------------------
 10 JAN 2021 17:13:13  USER (09 JAN) AARON1            [60,IN] PAGE 1
 ACTION
 AWAITING PAGE INSTRUCTIONS
 ```
&nbsp; 
&nbsp; 
### Customizing your terminal