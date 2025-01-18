# VHDL Counter Bug
This repository demonstrates a subtle off-by-one error in a VHDL counter and its solution.

The `buggy_counter.vhdl` file contains a counter that fails to reset at the maximum count due to an incorrect comparison.  The `fixed_counter.vhdl` file provides the corrected code.

## Bug Description
The counter uses a simple `if` statement to check for the maximum count. However, the condition `if internal_count = 15 then` is the source of the error. In certain scenarios, the counter fails to reset as expected when reaching the maximum value.  This occurs because of the way the comparison happens within the process's execution. 

## Solution
The solution involves a simple fix within the `if` condition of the `process` in `fixed_counter.vhdl`.  The problem is corrected by using the correct comparison and ensuring the counter properly resets when it reaches its maximum value.