# Style Guide

This style guide inspired by [PEP8](https://www.python.org/dev/peps/pep-0008/) for python and adapted for MATLAB.

## Introduction

This document provides coding conventions for MATLAB code. This style guide can/will evolve over time and is a reflection of _my general_ conventions.

The conventions presented in this document _mostly_ agree with previously developed conventions.

## Layout

### Indentation

Use 4 spaces per indentation level.

Indentations continuing long lines of code should add an extra level.

```text
result = functionWithLongName(arg1, arg2, arg3, ...
    arg4, arg5);
```

The closing parenthesis or bracket should be in-line (1) or the first character on a new line (2):

```text
#1
result = functionWithLongName(arg1, arg2, arg3, ...
    arg4, arg5);

#2
result = functionWithLongName(...
    arg1, arg2, arg3, arg4, arg5 ...
    );
```

Use indentation to separate keyword/name-value arguments from one another.

```text
result = functionWithLongName(...
    key1, value1, ...
    key2, value2, ...
    );
```

This is especially useful when there a multiple keyword/name-value arguments.

Multiline constructs (e.g., brackets, parenthesis) may either line up under the first non-whitespace character of the last line:

```text
A = [...
    1, 2, 3, ...
    4, 5, 6, ...
    7, 8, 9
    ];
```

or it may be included in the last line of the construct (similar to function arguments)

```text
A = [...
    1, 2, 3, ...
    4, 5, 6, ...
    7, 8, 9 ];
```

The first method is preferred for easier readability between commands.

Indent all functions - it's just easier to read.

```text
# function
function n = addTwoNum(a, b)
    n = a + b;
end

# class
class Person
    properties
        name = 'John';
    end

    methods
        function greeting(obj)
            fprintf('Hello, my name is %s\n', obj.name);
        end
    end
end
```

### Tabs or Spaces

Spaces are preferred indentation.

Tabs should **only** be used with existing code using tab indentation.

### Maximum Line Length

Limit all lines to a maximum of 80. The MATLAB editor default is 75.

The line length (80) is standard for ASCII format.

To avoid exceeding the line length, use `...`

```text
result = functionWithVeryLongName(arg1, arg2, arg3, ...
    arg4, arg5);
```

### When should I line break?

Use line breaks before binary operators.

```text
income = [grossWages ...
    + taxableInterest ...
    + dividends ...
    ];
```

### Blank Lines

Use 2 blank lines around top-level definitions.

Use 1 blank line around local or nested definitions.

Use single blank lines sparingly inside functions or methods to indicate logical sections.

```text
function m = computeSlope(x1, y1, x2, y2)
    # slope of a line
    #   m = dy / dx
    #   m = rise / run
    dy = computeRise(y1, y2);
    dx = computeRun(x1, x2);
    m = dy / dx;
end


# local functions
function dy = computeRise(y1, y2)
    dy = y2 - y1;
end

function dx = computeRun(x1, x2)
    dx = x2 - x1;
end
```

### Strings

MATLAB "strings" are unique. Single-quoted text produce character arrays and double-quoted text produce _actual_ strings. These **are not** the same. There is no recommendation except to be consistent in your usage of single- and double-quoted text.

For print statements with quotations, consider using double-quote to surround the text and single-quotes around the quoted text.

```text
# preferred method
fprintf("This is the 'preferred' way of quoting")

# less preferred
fprintf('This is '''less preferred''')
```

### Whitespace

Use whitespace to increase readability.

Some rules for when to use whitespace:

- Immediately after a comma, semicolon, colon, or operator:

```text
x = 1; y = 1;
z = x + y;
```

If there a long or multiple operators in a single statement, use space sparingly and give whitespace to grouped terms.

```text
# preferred
a = 3;
b = 4;
c = a*a + b*b
a = (b / sin(b)) * sin(A)

# wrong
c = a * a + b * b
a = b / sin(b) * sin(A)
```

Do not use spaces to align assignments across lines.

```text
% DO NOT DO THIS
a          = 1;
b          = 3;
hypotenuse = a^2 + b^2
```

Do not have trailing whitespace, e.g., space after command and before a new line.

Use a space around function inputs.

## Comments

Make comments clear, concise, and full sentences. This includes proper capitalization and punctuation.

Block comments should consists of paragraphs with the above rule.

Use inline comments sparingly. If an inline comment is included, it should be separated with at least 2 spaces from the statement.

```text
% correct
x = x + 1;  # my comment
y = x * 3;      # my other comment

% wrong
z = x + y; # bad comment
```

### Documentation

Good documentation is crucial.

You should write documentation for all non-public or non-nested functions. For non-public or non-nested functions, classes, or modules, a single statement providing information of what it does is sufficient.

```text
% public function definition
function y = foo(x)
  % FUNCTION Perform random math on x
  %
  % Args:
  %   x (double): Input
  %
  % Returns:
  %   y (double): Output of math operation
end

% non-public function
function y = boo(x)
  % function takes input x and prints to screen
end
```

The help section should inside the function, class, or module definition block. The help section should follow the same indentation rules.

There should be one blank line between the help section and the code. The only exception is for small functions or scripts, e.g, less than 5 lines *or so*.

```text
function y = boo(x)
  % function takes input x and prints to screen
  fprintf('input was %s\n', x)
end
```

Favor simple help sections over complex or overly wording ones.

- Include a one line description
- (Optional) Long description, if necessary
- List of input arguments with datatype, description, and whether is optional
- List of output arguments with the same info as inputs
- (Optional) Examples

```text
function [a, b, c] = triangleAngles(x, y, z)
    % TRIANGLEANGLES Compute angle of a triangle
    %
    % Args:
    %   x (double): triangle side 1
    %   y (double): triangle side 2
    %   z (double): triangle side 3
    %
    % Returns:
    %   a (double): angle between side 1 and side 2
    %   b (double): angle between side 2 and side 3
    %   c (double): angle between side 1 and side 3
    %
    % Examples:
    %   [a, b, c] = triangleAngles(1, 1, sqrt(2))
    %   outputs a=90, b=45, c=45
    %
    %   [a, b, c] = triangleAngles(3, 4, 5)
    %   outputs a=90, b=60, c=30
end
```

## Naming Conventions

### Summary

| Type                                      | Naming convention     |
| ----------------------------------------- | --------------------- |
| [Function](#function-names)               | camelCase             |
| [Class](#class-names)                     | PascalCase            |
| [Class Property](#class-property-names)   | camelCase             |
| [Class Method](#class-method-names)       | camelCase             |
| [Package](#package-names)                 | lowercase             |
| [Variable](#variable-names)               | camelCase             |
| [Method Argument](#method-argument-names) | camelCase             |
| [Global](#global-variable-names)          | UPPERCASE, UPPER_CASE |
| [Constant](#constant-names)               | UPPERCASE, UPPER_CASE |
| [Exception](#exception-names)             | PascalCase            |
| [Unit Test](#unit-test-names)             | camelCase, PascalCase |

> There are some exceptions/substitutions that conform to other case(s), e.g., camelCase -> snake_case

### Function Names

Function names should follow the `camelCase` convention.

### Class Names

Class names should follow the `PascalCase` convention.

#### Class Property Names

Class property names should follow the `camelCase` convention.

They should follow the same convention as method arguments.

#### Class Method Names

Class method names should follow the `camelCase` convention.

They should follow the same convention as function names.

### Package Names

Package names should follow the `lowercase` convention.

Packages names should proceed with `+` and use short, abbreviated names, if possible.

### Variable Names

Variables names should follow the `camelCase` convention.

They should follow the same convention as function names.

### Method Argument Names

Method argument names should follow the `camelCase` convention.

They should follow the same convention as variable names.

### Global Variable Names

Global variable names should follow the `UPPERCASE`, `UPPER_CASE` convention.

Only use underscores when it improves readability.

### Constant Names

Constant names should follow the `UPPER_CASE` convention.

Underscores should be used to separate words, and generally follow global variable names.

### Exception Names

Exception names should follow the `PascalCase` convention.

They should follow the same convention as class names.

If the exception is an error, consider using `Error` at the end of the name.

### Unit Test Names

Unit test names should follow the `camelCase` or `PascalCase` convention.

All unit test file names should preceed with 'test'.

Script or function unit test names should follow the same convention as function names.

Class unit test names shold follow the same convention as class names.

Individual test names should, at a minimum, specify if the test result in the name.

## Programming Recommendations
