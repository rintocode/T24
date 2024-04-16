# Working with Strings

## Definition

There are 3 ways of defining strings:

- Single quote: `name = 'Joe Doe'`
- Double quote: `company = "rintocode"`
- backslashes: `address = \23, avenue de l'armée\`

## String Operations

### String concatenation

To concatenate strings we use `colon (:)`

```basic
first_name = 'Joe' ; last_name = 'Doe'
full_name = fist_name : ' ': last_name
CRT full_name         ;* Joe Doe
```

### String Slicing

```basic
name = "John Smith"
CRT name[1,4]       ;* John
CRT name[5]         ;* Smith
CRT name[-5, 5]     ;* Smith
```

### Built-in functions to work with strings

Below are some samples of how to manipulate strings using some built-in functions

```basic
name = "John Smith"
CRT LEFT(4)             ;* John
CRT RIGHT(5)            ;* Smith
CRT UPCASE(name)        ;* JOHN SMITH
CRT DOWNCASE("Value")   ;* value
CRT LEN(name)           ;* 10
CRT STR('A', 3)         ;* AAA
```
