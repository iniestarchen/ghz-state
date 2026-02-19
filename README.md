# GHZ State

> **Category**: fundamentals &nbsp;|&nbsp; **Difficulty**: beginner &nbsp;|&nbsp; **Qubits**: 3 &nbsp;|&nbsp; **Gates**: 3 &nbsp;|&nbsp; **Depth**: 3

The GHZ state generalises the Bell state to three (or more) qubits. It exhibits genuine multipartite entanglement: no qubit is separable from the others. It violates the Mermin inequality, ruling out local hidden variable theories. Measuring any one qubit immediately collapses all others to a definite state.

## Expected Output

50% |000⟩, 50% |111⟩

## Circuit

The OpenQASM 2.0 circuit is in [`circuit.qasm`](./circuit.qasm).

```
OPENQASM 2.0;
include "qelib1.inc";
qreg q[3];
creg c[3];
h q[0];
cx q[0],q[1];
cx q[0],q[2];
measure q[0] -> c[0];
measure q[1] -> c[1];
measure q[2] -> c[2];
```

## Tags

`entanglement` `fundamentals` `ghz-state` `multipartite`

## References

- [Greenberger, Horne, Zeilinger (1989). Going Beyond Bell's Theorem](https://doi.org/10.1007/978-94-017-0849-4_10)

## License

MIT — part of the [OpenQC Algorithm Catalog](https://github.com/openqc-algorithms).
