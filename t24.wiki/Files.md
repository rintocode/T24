# Working with Files

## Reading text file

Reading text files(txt, csv, etc) in info basic is done in 3 steps:

1. Open file using `OPENSEQ`
2. Read file (one line at time) using `READSEQ`
3. Close file using `CLOSESEQ`

Let's write a simple program to read a csv file

```jbc
PROGRAM MTD.ReadFile
   
    dir = '../bnk.interface/EBANK.IN'
    filename = 'transaction.csv'

    OPENSEQ dir, filename TO ptr THEN
        LOOP
            READSEQ line FROM ptr ELSE BREAK
            CRT line
        REPEAT
    END ELSE CRT 'Failed to open ': filename
    
    CLOSESEQ ptr

END
```

## Writing text files

Writing text files(txt, csv, etc) in info basic is done in 3 steps:

1. Open file using `OPENSEQ`
2. Write data to a file using `WRITESEQ`
3. Close file using `CLOSESEQ`

Let's write a simple logger in jBC

```jbc
SUBROUTINE MTD.Logger(in_data, out_err)
    
    err = ''
    log_file = OCONV(DATE(), 'DG') : '.log'
    log_line = OCONV(TIME(), 'MTS') : ' | ' : data

    OPENSEQ '../bnk.log', log_file TO file_ptr THEN NULL
    
    WRITESEQ log_line APPEND TO file_ptr ELSE err = 'Failed to write to ' : log_file

    CLOSESEQ file_ptr

    RETURN
END
```
