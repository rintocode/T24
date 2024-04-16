# T24 Business Training

## Funds Transfer

FT module is used to transfer funds between customer accounts or internal accounts in our books and transfers to / from other banks through local clearing or other channels such as SWIFT.
FT module support transactions in local and foreign currencies(with automatic currency conversion).
![image](./images/ft.jpg)

## Payment Types

1. Internal Transfers
2. External Transfers (INWARDS and OUTWARDS):
   - local clearing
   - International transfers via correspondents
3. Banks own payments

## Parameter Files

1. CONDITION.PRIORITY
2. FT.GEN.CONDITION
3. FT.GROUP.CONDITION
4. CUSTOMER.CHARGE
5. FT.TXN.TYPE.CONDITION
6. FT.CHARGE.TYPE
7. FT.COMMISSION.TYPE

## SWIFT & DELIVERY

- DE.FORMAT.SWIFT
- DE.MAPPING
- DE.MESSAGE
- DE.O.HEADER
- DE.I.HEADER

## STANDING.ORDER

1. Fixed Payments ( same date, same amount)
2. Direct Debit (eg Invoice payments)
3. Preset Payments ( amount and date are not known)
4. Sweep account balances and Manage funds based on balance levels
5. Supports bulk STOs
