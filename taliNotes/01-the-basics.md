# Module #1: The Basics

## 2: Browser, editor, and terminal setup
### Shortcuts

#### Browser (Chrome):
- Open dev tools
    - Cmd + Option + J
- Inspect element
    - Cmd + Shift + C

#### Terminal:
- Clear screen
    - Cmd + K

---

## 3: Running and loading JS
- Code that you run in the inspector console applies to the page you're on.

### Inline Javascript
- Include inline Javascript just before the `</body>` tag.
    - You want the `<script>` tag to be able to access the content of the page.

### External Javascript
- `<script src="./main.js"></script>` to reference an external JS file.
- `type=` can be omitted unless you're using modules.
- `./` means 'this folder'.
- `../` means 'the folder above'.

### Javascript from Node
- Javascript that can run on a server
- To execute
    - Open Terminal > `node example.js`

---

## 4: Variables and statements

`'use strict'` prevents you from doing weird things that were previously allowed in older versions of JS. Enforced when you use JS modules.

e.g.: `name = 'Tali';`

### Variables
- Three different types: `var`, `let`, and `const`

#### General rules
- Good practice to start with `const`; if it needs to change, change it to `let`; if it's annoying that it's only block scoped, change it to `var`.
- Variable names should not start with a capital letter.
- Variable names should start with an A-Z letter, underscore (_) or dollar sign ($).
    - Underscore is synonymous with lodash.
    - Dollar sign is synonymous with jQuery.
- If your variable name consists of two or more words, use *camel case*, e.g.: thisIsACamelCaseString.

#### Updating values
- `var` and `let` can be updated
- `const` **cannot** be updated once it has been declared and initialised
    - Prevents accidentally overwriting a value
    - You must declare and initialise a `const` at the same time, i.e.: `const name` is illegal
    - `SyntaxError: Missing initializer in const declaration`

#### Scoping
"Where are my variables available at different parts of executing the code?"
- `var` is different to `let` and `const`
- Function scoped
    - `var`
- Block scoped (within `{}`)
    - `let` and `const`

### Statements
- Variable declaration statement
    - e.g.: `let cat = 'Lucky';`
- Function call statement
    - e.g.: `console.log('meow');`

---

## 5: Code quality tooling with Prettier and ESLint

### [ESLint](https://eslint.org/demo)
JS linter tool. Notifies you of potentially bad code. Different plugins available for different frameworks (e.g.: React, Vue, etc.).

### [Prettier](https://prettier.io/playground/)
Assists with consistency in formatting (and opinions), including:
- Indentation
- Whitespace
    - e.g.: const age=100;
- Quotes for strings
    - e.g.: '' vs. ""
- Semicolons

---

## 6: Types - Introduction

### SNOB'N'US
String
Number
Object
Boolean
Null
Undefined
Symbol

Everything in JS is an Object.

## 7: Strings
See `types.html`, `types.js`.

- Double quotes ("")
    - Allows a single quote within the string
    - e.g.: "She's so cool"
- Single quotes ('')
    - Allows a double quote within the string
- Backticks (``)
    - Permits single and double quotes
    - Maintains line breaks without using \ at the end of each line
- String concatenation
    - When a variable is inserted into the string
    - e.g.: 'Hello ' + name + ', nice to meet you'
- String interpolation
    - When a variable is inserted into the string within backticks only
    - The value within the interpolated string is evaluated, whether it's maths (1+2) or a variable
    - e.g.: \`Hello ${name}, nice to meet you. I am ${4+5} years old.`
- Escape character (\\)
    - Use a backslash to escape the following character
    - e.g.: 'She\'s so cool'

---

## 8: Numbers

### typeof
Tells you what the type of the variable/value is
- `typeof 11 = number`
- `typeof 'dsadas' = string`

### Math operators
- Plus is 'loaded' - it can be used for both addition and string concatenation, depending on inputs.
    - 1 + 1 = 2
    - 1 + "1" = "11"
- Subtraction, multiplication, and division, even when used with strings, will be converted into numbers.
    - "6" / "2" = 3
- Power (**)
    - 10 ** 2 = 100
- Modulo (%)
    - Tells you what the remainder will be after dividing
    - 10 % 3 = 1

### Helper methods
- Math.round()
- Math.floor(), Math.ceil()
- Math.random()

### Rounding and precision
- Computers can only store numbers as integers under the hood
- Never store money values as dollars and cents in a floating number, represent money as cents.
    - Bad: 10.34
    - Good: 1034

### Special values
- Infinity/-Infinity
    - Represents values that are greater than the computer can store
- NaN
    - Not a Number

---

## 9: Objects

Collections of data and functionality. Arrays and dates are both Objects. Order doesn't matter in Objects (if you need order to matter, use an array).

### Structure
- Creating an object
    - `const person = {};`
- Properties and values
    - ```
        const person = {
            name: 'Tali',
            age: '9',
        };```
- Accessing values
    - person.name

---

## 10: null and undefined

### undefined
A value that has been created but not yet defined.
A variable's value is set to 'undefined' until it's initialised.

### null
A value of 'nothing'. Set explicitly and intentionally.

---

## 11: Booleans and equality

### Booleans
True or false. Can be set or calculated.

### Equality
- =
    - Assignment operator
    - `let catName = 'Lucky';`
- ==
    - Checks for equality but is real loosey goosey about it
    - `"1" == 1` returns `true`
- ===
    - Use this where possible!
    - Checks for equality and ensures that values are of the same type, too
    - `"1" === 1` returns `false`
    - `50 === 50` returns `true`


---

## Glossary
| Abbreviation | Meaning | Notes |
|---|---|---|
| ASI | automatic semicolon insertion |   |
| REPL | read-eval-print loop |   |
|   |   |   |
