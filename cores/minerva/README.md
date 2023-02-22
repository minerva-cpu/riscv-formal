
riscv-formal proofs for minerva
===============================

Quickstart guide:

First install Yosys, SymbiYosys, and the solvers. See
[here](http://symbiyosys.readthedocs.io/en/latest/install.html)
for instructions. 

Then install [Amaranth HDL](https://amaranth-lang.org/docs/amaranth/latest/install.html)
and [Minerva](https://github.com/minerva-cpu/minerva).

Then generate the formal checks and run them:
```
python3 ../../checks/genchecks.py
make -C checks -j$(nproc)
```

The testbench wrapper relies on the Yosys `connect_rpc` frontend to instantiate Amaranth code.
