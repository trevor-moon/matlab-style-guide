# Style Guide

This style guide inspired by [PEP8](https://www.python.org/dev/peps/pep-0008/) for python and adapted for MATLAB.

## Introduction

This document provides coding conventions for MATLAB code. This style guide can/will evolve over time and is a reflection of *my general* conventions.

The conventions presented in this document *mostly* agree with previously developed conventions.

## Layout

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
