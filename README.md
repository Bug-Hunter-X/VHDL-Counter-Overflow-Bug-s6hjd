# VHDL Counter Overflow Bug and Fix

This repository demonstrates a common error in VHDL code: an integer counter that doesn't handle overflow correctly. The original code (`buggy_counter.vhdl`) increments a counter without checking for the maximum value. When the counter reaches its limit, it wraps around to zero.  This might lead to unintended behavior in a larger design.  The fixed code (`fixed_counter.vhdl`) addresses this issue using a modulo operation.

## Bug Description
The original counter (`buggy_counter.vhdl`) lacks proper handling for when the `internal_count` reaches the maximum value of 15.  After 15, it wraps around to 0. This is not always desirable.

## Solution
The `fixed_counter.vhdl` example adds a modulo operation to prevent the counter from exceeding 15. This ensures correct behavior and prevents unexpected wrapping.