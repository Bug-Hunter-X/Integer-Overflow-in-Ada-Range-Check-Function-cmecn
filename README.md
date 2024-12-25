# Ada Integer Overflow Bug

This repository demonstrates a subtle bug related to integer overflow in an Ada function designed to check if a number is within a specific range.  The original function `Check_Range` fails to correctly handle very large or very small integer inputs. This example highlights the importance of considering potential overflow when working with numerical data types in Ada.

## Bug Description

The `Check_Range` function uses simple `if-elsif-else` statements to determine if an integer falls within the range 10-20 (inclusive). However, it does not account for potential integer overflow.  If the input number is outside the range representable by the Integer type, the comparisons could yield unexpected results, leading to incorrect classification.

## Solution

The provided solution improves the function by adding explicit range checks. The updated code ensures that the function operates correctly regardless of the size of the input number within the constraints of Ada's integer type.

## How to Reproduce

1. Compile and run `Check_Range_bug.ada`. Observe the unexpected behavior for inputs that might cause overflow. 
2. Compile and run `Check_Range_solution.ada` to see how the issue is corrected.
