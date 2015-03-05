Common Guidelines
=================

**We Support** (there could be exceptions)

* Internet Explorer 9+
* Firefox
* Google Chrome
* Safari

**Always Remember**
-------------------

* Don't try to prematurely optimize your code;
  keep it readable and understandable.

* All code in any code-base should look like a single person typed it,
  even when many people are contributing to it.

* Strictly enforce the agreed-upon style.

* Whatever you do, you should be able to explain the reason to other person.

* If it makes sense, if it feels right, do it. Code is just a means, not an end.

* If you have multiple code blocks doing some specific task, try to separate them with blank line and start each of them with a descriptive comment. It increases code readability. For example,

  ```php
  // Code block 1.
  // Initialize variables.
  $sum_even = 0;
  $sum_odd = 0;
  
  // Code block 2.
  // Calculate sum of even numbers.
  for ($i = 2; $i <= 50; $i += 2) {
    $sum_even += $i;
  }
  
  // Code block 3.
  // Calculate sum of odd numbers.
  for ($i = 1; $i <= 50; $i += 2) {
    $sum_odd += $i;
  }
  
  $result = $sum_even * $sum_odd;
  ```
  Code blocks 1, 2 and 3 separated by blank spaces and with descriptive comments.
  
  This is just an example, in real world scenarios code blocks can be longer and doing complex things.


**Common Practices**
--------------------

* Always use 2 spaces for indentation

* Strings longer than 80 characters should be written across
  multiple lines using string concatenation.

* Use braces with all multi-line blocks.

* Place 1 space before the leading brace.

* Set off operators with spaces.

* No trailing white spaces.

* Be descriptive with your naming for variables and functions.

* Comment as much as you can.

* Use `/* ... */` for multi-line comments and `//` for single line comments.

* Configure your editor according to these standards.

* If you have long arrays, try to use multiline arrays.
