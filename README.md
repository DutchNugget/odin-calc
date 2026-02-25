# odin-calc
odin javascript calc project



# Calculator Project (HTML + JavaScript)

## Project Overview

Build a browser-based calculator using HTML for structure and JavaScript for functionality. The calculator should support basic arithmetic operations and handle common edge cases.

---

# Development Checklist

## 1. Project Setup

* Create `index.html`
* Create `script.js`
* Link `script.js` inside `index.html`
* Confirm JavaScript is connected using `console.log()`

---

## 2. Build HTML Structure

Create the basic calculator layout:

* Calculator container
* Display area
* Digit buttons (0–9)
* Operator buttons (+, −, ×, ÷)
* Equals (=) button
* Clear (C) button

Optional:

* Decimal (.) button
* Backspace button

Do not add functionality yet. Focus only on structure.

---

## 3. Create Basic Math Functions (JavaScript)

Create and test the following functions in the console:

* `add(a, b)`
* `subtract(a, b)`
* `multiply(a, b)`
* `divide(a, b)`

  * Handle division by zero

Test each function before moving forward.

---

## 4. Create the `operate()` Function

* Accepts an operator and two numbers
* Calls the correct math function
* Returns the result

Example test:

```
operate("+", 3, 5)
```

---

## 5. Create State Variables

Create variables to manage calculator state:

* `firstNumber`
* `secondNumber`
* `operator`
* `shouldResetDisplay` (boolean)

---

## 6. Implement Digit Button Functionality

* Add event listeners to digit buttons
* Update the appropriate number variable when clicked
* Update the display
* If a result was just shown, start a new calculation

---

## 7. Implement Operator Button Functionality

* Store selected operator
* If both numbers exist:

  * Run calculation immediately (for chained operations like `12 + 7 - 1`)
* Prevent evaluation when operators are pressed consecutively
* Replace the operator if user presses another operator before entering second number

---

## 8. Implement Equals Button

Only evaluate when:

* `firstNumber` exists
* `operator` exists
* `secondNumber` exists

Steps:

* Call `operate()`
* Round long decimal results
* Display result
* Store result as new `firstNumber`
* Clear `secondNumber`
* Clear `operator`

---

## 9. Implement Clear Button

* Reset all state variables
* Reset display to 0
* Ensure calculator starts completely fresh

---

## 10. Handle Edge Cases

Ensure the calculator:

* Does not evaluate without two numbers and an operator
* Prevents division by zero
* Prevents multiple operators in a row
* Prevents multiple decimals in one number
* Rounds long decimal results
* Starts a new calculation when a digit is pressed after a result is shown
* Does not break if equals is pressed too early

---

# Optional Features

* Decimal input support

  * Disable decimal if already used in current number
* Backspace button

  * Remove last digit from current number
* Keyboard support

  * Numbers, operators, Enter (equals), Backspace

---

# Manual Test Cases

Verify the following work correctly:

* `12 + 7 =` → 19
* `12 + 7 - 1 =` → 18
* Pressing an operator twice does not trigger evaluation
* Pressing equals too early does not break the app
* Division by zero shows an error
* Clear resets everything
* Typing a number after a result starts a new calculation

---

