# Automated Testing

## Why?

Products and code bases tend to grow over time, which means more testing is needed. Manual tests are a bottleneck to shipping software quickly and getting valuable feedback from customers.

Automating tests build confidence for moving fast. It helps design and document the code, provides a safe-net for future refactoring and provides the base for CI and CD.

## How?

There are three main types of tests:

**1. Unit tests**

`"Is this function doing what I think it is doing?"`

Fast, reliable and easy to setup. Tests the smallest portion of code without dependencies (which are mocked).

**2. Integration tests**

`"Are these components working together as planned?"`

Tests a few components together, might involve setting up a database or testing a higher level component. Minimal or no mocks are used.

**3. End to end tests**

`"What will the user see?"`

Tests the entire system as a user would. Usually involves running a browser, clicking here asserting to simulate a real user behavior.

Tests are slow, flaky but can simulate real world problems.

We currently **focus on unit tests**, as they are more reliable and focus on testing that the logic is correct.

## What to test?

First, what shouldn't be tested? Getters, setters and anything trivial.

Test functions that can get multiple types of inputs, and their outputs are critical. Good candidates are code with lots of `if`s and `for`/`forEach`/`map`/`reduce`.
