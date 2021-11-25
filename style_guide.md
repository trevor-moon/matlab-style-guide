# Style Guide

This style guide inspired by [PEP8](https://www.python.org/dev/peps/pep-0008/) for python and adapted for MATLAB.

## Introduction

This document provides coding conventions for MATLAB code. This style guide can/will evolve over time and is a reflection of *my general* conventions.

The conventions presented in this document *mostly* agree with previously developed conventions.

## Layout

### Indentation

Use 4 spaces per indentation level.

Indentations continuing long lines of code should add an extra level.

```text
result = functionWithLongName(arg1, arg2, arg3, ...
    arg4, arg5);
```

Optionally add 4 (extra) spaces to *better* distinguish long argument list items from others.

```text
result = functionWithLongName(...
        arg1, arg2, arg3, ...
        arg4, arg5 ...
        );
```

Use indentation to separate keyword/name-value arguments from one another.

```text
result = functionWithLongName(...
    key1, value1, ...
    key2, value2, ...
    );
```

Multiline constructs (e.g., brackets, parenthesis) may either line up under the first non-whitespace character of the last line:

```text
A = [...
    1, 2, 3, ...
    4, 5, 6, ...
    7, 8, 9
    ];
```

or it may be lined up under the first character of the line that starts the construct:

```text
A = [...
    1, 2, 3, ...
    4, 5, 6, ...
    7, 8, 9
];
```

> The first method is preferred for easier readability between commands.

Indent all functions (it's just easier to read).

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
    arg4, arg5 ...
    );
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

Use single blank lines *sparingly* inside functions or methods to indicate logical sections.

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

### Whitespace

### Trailing Commas

## Comments

### Block Comments

### Inline Comments

### Documentation Comments

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
