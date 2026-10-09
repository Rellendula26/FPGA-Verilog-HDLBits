# FPGA / Verilog HDLBits Exercises

A small repository for practicing combinational logic in SystemVerilog. The current checkout contains one 7458-style AND-OR gate exercise, not a complete collection of HDLBits solutions.

## Current exercise

`7458ChipRecreation.sv` defines `top_module` with two independent outputs:

```text
p1y = (p1a AND p1b AND p1c) OR (p1d AND p1e AND p1f)
p2y = (p2a AND p2b) OR (p2c AND p2d)
```

`7458Chip.png` is the accompanying reference image. The design is combinational: it has no clock or stored state.

## Compile

With Icarus Verilog installed, run from the repository root:

```bash
iverilog -g2012 -s top_module -o /tmp/7458.vvp 7458ChipRecreation.sv
```

This checks compilation only. To verify behavior, supply a testbench that drives the inputs and checks the equations above, or use the exercise's external test harness.

## Status

No testbench, FPGA constraints, synthesis project, or hardware programming files are included. Compilation and hardware behavior have not been verified as part of this documentation update.
