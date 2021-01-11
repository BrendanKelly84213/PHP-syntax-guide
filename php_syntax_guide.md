# PHP Comments

Comments are text that php will ignore.

```
//This text will be ignored 

/*This text will be ignored*/
```

# PHP Variables

A variable is a label on some data. A variable stores the data assigned to it, and is interchangeable with that data.

In php, variables are assigned and called using the `$` symbol.

Variables can be assigned to any kind of data in php. 

```
$a_string = "hello";
$an_int = 2;
$a_float = 1.1;

// And so on

$added = $an_int + $a_float; // The same as: 2 + 1.1

```

# PHP Echo / Print

`echo` and `print` are functions built into php which display text onto the page.

`echo` has no return value, and is slightly faster than `print`. `print` will always return 1. 

## echo
```
<?php
    $variable = "You can include variables in echo statements.";

    echo $variable;
    echo "This outputs a string.";
    echo "<p>You can also include HTML in an echo statement.</p>"
?>
```

## print
```
<?php
    print("Hello World!"); // Output a string 
    print "Hello World!"; // Same thing 
    $x = print "Hello World!"; // print has a return value
    print $x; // Print returns 1
?>
```




# PHP Data Types
PHP variables have different types.  
# PHP Strings
A string is a sequence of characters. 
## Example
```
<?php
	$x = "hello world!";
	$y = 'hello world!';
	echo $x; // hello world!
	echo $x == $y; // 1
?>
```
# PHP Numbers
Numbers can be integers or floats.

## Integers

An integer can be any number in the set `{-(2^32 - 1),...,-2,-1,0,1,2,...,(2^32 - 1)}`. 

Integers can be specified in  decimal, hexadecimal (base 16), octal (base 8) or binary (base 2).

```
<?php
$a = 1234; // decimal number
$a = 0123; // octal number (equivalent to 83 decimal)
$a = 0x1A; // hexadecimal number (equivalent to 26 decimal)
$a = 0b11111111; // binary number (equivalent to 255 decimal)
$a = 1_234_567; // decimal number (as of PHP 7.4.0)
?>
```

## Floats 

Floats are numbers with decimals. Floats can be specified as follows:

```
<?php
$a = 1.234; 
$b = 1.2e3; 
$c = 7E-10;
$d = 1_234.567; // as of PHP 7.4.0
?>
```

# PHP Constants

A constant is a value which cannot be changed once assigned.

Syntax:

```
<?php

// Valid constant names
define("FOO",     "something");
define("FOO2",    "something else");
define("FOO_BAR", "something more");

// Invalid constant names
define("2FOO",    "something");

// This is valid, but should be avoided:
// PHP may one day provide a magical constant
// that will break your script
define("__FOO__", "something"); 

const test = "something"; // Also works

echo test; // Outputs "something". Does not use $ 

?>
```

# PHP Operators

Operator are mainly divided by three groups that are totally seventeen types.

1.Arithmetic Operator

```
+ = Addition
- = Subtraction
* = Multiplication
/ = Division
% = Modulo
** = Exponentiation

2.Assignment Operator
     = "equal to

3.Array Operator
    + = Union
    == = Equality
    === = Identity
    != = Inequality
    <> = Inequality
    !== =    Non-identity

4.Bitwise Operator
& = and
^ = xor
| = not
<< = shift left
>> = shift right

5.Comparison Operator
==  = equal
=== = identical
!=  = not equal
!== = not identical
<>  = not equal
< = less than
<= less than or equal
> = greater than
>= = greater than or equal
<=> = spaceship operator

6.Execution Operator
`` = backticks 

7.Error Control Operator
    @ = at sign

8.Incrementing/Decrementing Operator
    ++$a = PreIncrement
    $a++ = PostIncrement
    --$a = PreDecrement
    $a-- = Postdecrement

9.Logical Operator
    && = And
    || = Or
    ! = Not
    and = And
    xor = Xor
    or = Or

10.string Operator
    . =  concatenation operator
    .= concatenating assignment operator

11.Type Operator
    instanceof = instanceof

12.Ternary or Conditional operator
   ?: = Ternary operator

13.Null Coalescing Operator
    ??" = null coalescing

14.Clone new Operator
    clone new = clone new

15.yield from Operator

    yield from = yield from

16.yield Operator
    yield = yield

17.print Operator
    print = print
```

# PHP If & Else & Elseif
An if statement executes a block of code given a condition is true. If statements take a boolean argument.

Syntax is as follows:

```
if (condition) {
	  code to be executed if condition is true;
}
```

else works in conjunction with if:

```
if(condition) {
	do something;
} else {
	do something else;
}
```

php also has elseif,

```
if(condition) {
	do something;
} elseif(condition) {
	do something else;
} else {
	executes when both conditions are false;
}
```

Example:
```
<?php
$x = 1;
if(x > 0) {
	echo "thats odd";
} elseif(x == 1) {
	echo "that makes more sense";
}

if(x > 0) {
	echo "thats odd";
} else {
	echo "This should also work";
}

?>
```

# PHP Functions

PHP has over 1000 built in functions. We've already gone over echo, print and so on.

Users can define their own functions as well:

```
function foo(args) {
	do something;
}
```

Example:

```
<?php
function writeMsg() {
	  echo "Hello world!";
}

writeMsg(); // call the function

// You can also return a value 
function returnMsg() {
	return "Hello World!";
}

echo returnMsg();

// Maybe a little more demonstrative: 
function add($a, $b) {
	return $a + $b;
}

echo add(1,1); // 2

?>
```

# PHP Arrays
An array is an ordered collection of values. In PHP, arrays associate values with keys. 

Syntax:
```
array(
    key  => value,
    key2 => value2,
    key3 => value3,
    ...
)
```

Example:

```
<?php
$array = array(
    "foo" => "bar",
    "bar" => "foo",
);

// Using the short array syntax
$array = [
    "foo" => "bar",
    "bar" => "foo",
];
?>
```

# PHP Loop

PHP has for, while, do while and foreach loops. In general, a loop executes a block of code repeatedly until a condition is met.

## for loops
Syntax:

```
for(init; condition; increment) {
	do something;
}
```

Example:

```
for($i=0; i<5; ++i) {
	echo "i: $i <br>";
}

```
Output:

```
i: 0
i: 1
i: 2
i: 3
i: 4

```

## while loops

Syntax:

```
while(condition) {
	do something;
}
```

Example:

```
<?php
$i = 0;
while($i<10) {
	$i++;
}

echo $i; // 10
?>
```
## do while

This loop executes the block of code before checking the condition.

Syntax:

```
do {
	something;
} while(condition);
```

Example:

```
<?php
do {
	echo "something"; // Executes
} while(false);
?>
```
## foreach

The foreach grabs values from an array

Example:
```
$array = array(1,2,3);
foreach($array as $value) {
	echo "value: $value <br>";
}
```

Output:

```
value: 1
value: 2
value: 3

```
