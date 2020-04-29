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

## Glossary
| Abbreviation | Meaning | Notes |
|---|---|---|
| ASI | automatic semicolon insertion |   |
| REPL | read-eval-print loop |   |
|   |   |   |
