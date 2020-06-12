#numeric and String Comparisons

##numeric and String Comparisons

We are going to discuss numbereric and string comparisons. Using this comparisons, we can compare strings, words, and numberbers whether raw or as variables. Following table list comparison operators for both numberbers and strings.

| Description      | numbereric Comparison | String Comparison |
|------------------|--------------------|-------------------|
| less than        | -lt                | <                 |
| greater than     | -gt                | >                 |
| equal            | -eq                | =                 |
| not equal        | -ne                | !=                |
| less or equal    | -le                | N/A               |
| greater or equal | -ge                | N/A               |

### Numeric Comparison
`a=1`{{execute}}

`b=2`{{execute}}

`[ $a -lt $b ]`{{execute}}

`echo $`{{execute}}

0 signals true, while 1 signals false.

number1 -eq number2                  checks if 1st  number  is equal to 2nd numberber

number1 -ge number2                  checks if 1st  number  is greater than or equal to 2nd numberber

number1 -gt number2                  checks if 1st  number  is greater than 2nd numberber

number1 -le number2                  checks if 1st  number  is less than or equal to 2nd numberber

number1 -lt number2                  checks if 1st  number  is less than 2nd numberber

number1 -ne number2                  checks if 1st  number  is not equal to 2nd numberber

### String Comparison

var1 = var2     checks if var1 is the same as string var2

var1 != var2    checks if var1 is not the same as var2

var1 < var2     checks if var1 is less than var2

var1 > var2     checks if var1 is greater than var2

-n var1         checks if var1 has a length greater than zero

-z var1         checks if var1 has a length of zero