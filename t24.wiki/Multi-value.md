# Multi-Value

Consider the following example:

* We have a customer called `John Doe`
* John has 3 phone numbers: 
  * `MTN Rwanda`: `0788000000` and `0788111111`
  * `Airtel Rwanda`:`0739000000`

This is how we can represent these details:

```basic
 customer = 'John Doe':@FM:'MTN Rwanda':@VM:'0788000000':@SM:'0788111111':@FM:'Airtel Rwanda':@VM:'0739000000'
 CRT "Name: "      : customer<1>         ;* John Doe
 CRT "Operator1: " : customer<2,1>       ;* MTN Rwanda
 CRT "Phone1: "    : customer<2,2,1>     ;* 0788000000
 CRT "Phone2: "    : customer<2,2,2>     ;* 0788111111
 CRT "Operator2: " : customer<3,1>       ;* Airtel Rwanda
 CRT "Phone3: "    : customer<3,2,1>     ;* 0739000000
```

* We have one field for "Mobile Network Operator" which can have multiple values separated by `@VM` (`Value Mark`)
* We have one field for "Phone number" denoted by `@SM` (`Sub-Value Mark`)
* Here name are `Single Field`. The delimiter is `@FM` or `@AM` (`Field Mark`)
