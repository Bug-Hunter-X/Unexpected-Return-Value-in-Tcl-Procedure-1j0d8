# Unexpected Return Value in Tcl Procedure

This repository demonstrates a common yet subtle error in Tcl:  unpredictable return values from procedures that don't explicitly handle all return cases. 

The `bug.tcl` file contains the erroneous code, which fails to explicitly return a value in all branches of the `badproc` procedure.  The `bugSolution.tcl` file provides a corrected version.

## How to Reproduce

1. Save the code in `bug.tcl`.
2. Run the Tcl script using `tclsh bug.tcl`. Observe that the result may vary or might even seem to be randomly selected from either the puts result or the implicit empty string, causing unexpected behavior.

## Solution

The `bugSolution.tcl` file provides the corrected code with an explicit `return` statement providing a consistent result.