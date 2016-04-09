# BigNumber

BigNumber is a C++ class that allows for the creation and arithmetic of arbitrary-length
integers.

The maximum possible length of a BigNumber is `string::max_size`.

## Installation
To add BigNumber to your C++ project, download
[bignumber.cpp](https://github.com/Limeoats/BigNumber/blob/master/src/bignumber.cpp)
and [bignumber.h](https://github.com/Limeoats/BigNumber/blob/master/src/bignumber.h)
from this Github repository and include them in your project.

Then, simply include the header file in whichever file you need a BigNumber.

`#include "bignumber.h"`

## Usage
###`BigNumber(string)`


You can also use the `=` operator to set a BigNumber equal to an existing BigNumber.

Examples:

    BigNumber b("5");       //BigNumber b is created with value 5.
    BigNumber c("-20");     //BigNumber c is created with value -20.
    BigNumber d("0");       //BigNumber d is created with value 0.
    BigNumber e = b;        //BigNumber e is created with value 5.


##Methods
###`add(BigNumber other)`
Adds another big number to the current instance

`BigNumber("4").add(BigNumber("20")) => BigNumber("24")`

###`subtract(BigNumber other)`
Subtracts another big number from the current instance

`BigNumber("30").subtract(BigNumber("45")) => BigNumber("-15")`

###`multiply(BigNumber other)`
Multiplies the big number by another big number

`BigNumber("12").multiply(BigNumber("4")) => BigNumber("48")`

###`pow(int exponent)`
Raises the big number to the power of the exponent

`BigNumber("2").pow(3) => BigNumber("8")`

###`getString()`
Returns the BigNumber as an std::string

`BigNumber("3824").getString() => "3824"`

###`setString(std::string newStr)`
Sets the BigNumber's internal number string to a new string

`BigNumber("2847").setString("38") => BigNumber("38")`

###`negate()`
Changes the sign of the BigNumber

    BigNumber("3").negate() => BigNumber("-3")
    BigNumber("-27").negate() => BigNumber("27")

###`equals(BigNumber other)`
Checks if the other big number is equal to this one

`BigNumber("24").equals(BigNumber("28")) => false`

###`digits()`
Returns the number of digits in the BigNumber

`BigNumber("28374").digits() => 5`

###`isNegative()`
Determines whether a big number is negative

`BigNumber("-278").isNegative() => true`


##Operator overloads
The following operators have been overloaded to work with big numbers:

###`<<`
Output stream operator

`std::cout << BigNumber("26") << std::endl => 26`

###`+`
Addition operator

`BigNumber("2") + BigNumber("4") => BigNumber("6")`

###`-`
Subtraction operator

`BigNumber("0") - BigNumber("2000") => BigNumber("-2000")`

###`*`
Multiplication operator

`BigNumber("-20") * BigNumber("-5") => BigNumber("100")`

###`==`
Equal to operator

`BigNumber("24") == BigNumber("24") => true`

###`>`
Greater than operator

`BigNumber("2") > BigNumber("6") => false`

###`<`
Less than operator

`BigNumber("2") < BigNumber("6") => true`

###`>=`
Greater than or equal to operator

`BigNumber("34") >= BigNumber("22") => true`

###`<=`
Less than or equal to operator

`BigNumber("383") <= BigNumber("383") => true`

###`=`
Assignment operator

`BigNumber c("3") = BigNumber("8") => BigNumber("8")`

###`+=`
Adds and assigns to the BigNumber

`BigNumber c("4") += BigNumber("3") => BigNumber("7")`

###`-=`
Subtracts and assigns to the BigNumber

`BigNumber c("28") -= BigNumber("3") => BigNumber("25")`

###`*=`
Multiplies and assigns to the BigNumber

`BigNumber c("3") *= BigNumber("4") => BigNumber("12")`

###`[]`
Indexing operator

`BigNumber d("26")[1] => 6`

##License
This project is under the [MIT License](https://opensource.org/licenses/MIT). Check the
top of the source files for more information.

##Credit
The BigNumber class was created by [Mark Guerra](http://www.twitter.com/Limeoats). Visit
[Limeoats.com](http://www.limeoats.com) for more information.












