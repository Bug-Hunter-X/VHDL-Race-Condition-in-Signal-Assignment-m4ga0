# VHDL Race Condition Example

This repository demonstrates a potential race condition that can occur in VHDL when signals are assigned within a process.  The code shows an example of this problem, and an improved version that addresses the race condition.  See `bug.vhdl` for the buggy code and `bugSolution.vhdl` for the corrected version.

**The Issue:**
In the buggy code, there's a potential delay between assigning to `internal_data` and subsequently assigning `internal_data` to `data_out`. While unlikely to manifest in simple simulations, in actual hardware this can lead to incorrect values being output.