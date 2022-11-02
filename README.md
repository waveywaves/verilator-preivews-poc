# Previews for Verilator

This repo will contain everything necessary to create previews for embedded systems. [Verilator](https://www.veripool.org/verilator/) is the Verilog/SystemVerilog simulator. So, we would be trying to understand how we can approximate a preview environment for simulating embedded systems which use Verilog.

Verilator lives in the https://github.com/verilator/verilator repo. The [Verilator Dockerfile](https://github.com/verilator/verilator/blob/master/ci/docker/run/Dockerfile) also lives here.


The paragraph below from [https://github.com/verilator/verilator#what-verilator-does](what-verilator-does) is very relevant and useful for us to understand.

> Verilator may not be the best choice if you are expecting a full featured replacement for a closed-source Verilog simulator, need SDF annotation, mixed-signal simulation, or are doing a quick class project (we recommend [Icarus Verilog](http://iverilog.icarus.com/) for classwork.) However, if you are looking for a path to migrate SystemVerilog to C++/SystemC, or want high speed simulation of synthesizable designs containing limited verification constructs, Verilator is the tool for you. 

# Goals

- [x] Install verilator (thankfully `dnf` had verilator)

```bash
dnf install verilator -y (this installs 4.0 version (atleast when I tried))
```

- [ ] Run all [Verilator examples](https://verilator.org/guide/latest/examples.html).
Clone the verilator repo and then run all the examples
```
git clone https://github.com/verilator/verilator

```

- [ ] Make a base image for Verilator which can take the examples as input and run them.
- [ ] Figure out OSS tools which can use/use Verilator. Use one of them with the solution above to finalize the PoC.
