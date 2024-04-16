# Temenos Open Financial Service (OFS)

## Objectives

1. Have a good understanding of OFS and how it is used
2. Describe OFS Syntax (request and response)
3. Create and Post OFS message (requests)

## What is OFS

- OFS is the standard gateway to T24
- It works on request-response basis

## Message Format

- Native OFS format
- XML format

## Message Syntax

### Transaction Request

- Operation
- Options
- User information
- Transaction Id
- Request Data (depending on function)

### Enquiry Request

- `ENQUIRY.SELECT,,`
- User information
- Enquiry name
- Request Data(selection criteria)

## Samples

### Transactions

Request (1):

```ofs
ACCOUNT,MTD.NEW.AC/I/PROCESS,AARON02/123456,41041,CUSTOMER:=111217,CATEGORY:=1001,CURRENCY:=EUR,ACCOUNT.TITLE.1:=AARON EUR CA
```

Response (1):

```ofs
41041//1,CUSTOMER:1:1=111217,CATEGORY:1:1=1001,ACCOUNT.TITLE.1:1:1=AARON EUR CA,SHORT.TITLE:1:1=AARON NIYONZIMA,MNEMONIC:1:1=EFGO8888IW,POSITION.TYPE:1:1=TR,CURRENCY:1:1=EUR,CURRENCY.MARKET:1:1=1,ACCOUNT.OFFICER:1:1=2,CONDITION.GROUP:1:1=1,PASSBOOK:1:1=NO,OPEN.CATEGORY:1:1=1001,CHARGE.CCY:1:1=EUR,INTEREST.CCY:1:1=EUR,ALT.ACCT.TYPE:1:1=LEGACY,ALLOW.NETTING:1:1=NO,SINGLE.LIMIT:1:1=Y,RECORD.STATUS:1:1=INAU,CURR.NO:1:1=1,INPUTTER:1:1=81_AARON2___OFS_BALOFS,DATE.TIME:1:1=2102191547,CO.CODE:1:1=GB0010001,DEPT.CODE:1:1=1
```

Request (2)

```ofs
ACCOUNT,MTD.NEW.AC/S/PROCESS,AARON02/123456,41042
```

Response(2)

```ofs
41042//-1/NO,@ID:1:1=RECORD MISSING
```

### Enquiry

Request(3)

```ofs
ENQUIRY.SELECT,,AARON02/123456,MTD.AC.BALANCE,@ID:EQ=40274
```

Response(3)

```ofs
MTD.AC.BALANCE//1,,CURRENCY::CURRENCY/WORKING.BALANCE::WORKING.BALANCE,"USD" " 4570030.55"
```

Request(4)

```ofs
ENQUIRY.SELECT,,AARON02/123456,MTD.AC.BALANCE,@ID:EQ=41042
```

Response(4)

```ofs
MTD.AC.BALANCE//1,,CURRENCY::CURRENCY/WORKING.BALANCE::WORKING.BALANCE,"No records were found that matched the selection criteria","","SSELECT FBNK.ACCOUNT
```
