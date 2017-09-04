# sancus-examples
[![Build Status](https://travis-ci.org/sancus-pma/sancus-examples.svg?branch=master)](https://travis-ci.org/sancus-pma/sancus-examples)

Elementary example programs to test your Sancus distribution.

## Overview

| Security feature          | Example program                | Comments                                                        |
|-------------------------- |--------------------------------|-----------------------------------------------------------------|
| Software module isolation | [hello-world](hello-world)     | Minimal working example to enable/disable a Sancus module.      |
| Secure linking            | [sensor-reader](sensor-reader) | Caller/callee authentication between sensor and reader SMs.     |
| Remote attestation        | [sensor-reader](sensor-reader) | Compute MAC over fresh challenge (nonce).                       |
| Secure communication      | [sensor-reader](sensor-reader) | Authenticated encryption with associated data primitive.        |
| Secure memory-mapped I/O  | [sensor-reader](sensor-reader) | Assembly driver SM with exclusive ownership over sensor device. |
| Secure interrupt handling | todo                           | Minimalist program using `SM_ISR` for GPIO IRQ?                 |
| Confidential deployment   | todo                           | Issue #2                                                        |
| Dynamic loading           | todo                           | Issue #3                                                        |
| Reactive programming      | todo                           | Minimalist (non-contiki) program with `SM_INPUT/OUTPUT`?        |


## Running the examples

All example binaries can be ran in either the Sancus Verilog simulator, or on an external FPGA. To build and run the example in `sancus-sim`, proceed as follows:

```bash
$ make sim
```

Alternatively, to upload the example to an FPGA using `sancus-loader`:

```bash
$ make load
```
