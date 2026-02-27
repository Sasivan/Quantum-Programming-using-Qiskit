# OpenQASM Demonstration using Qiskit 2.x

## Overview
OpenQASM (Open Quantum Assembly Language) is a human-readable language for describing quantum circuits. It allows interoperability between different quantum programming tools and is used internally by Qiskit when circuits are compiled for execution on real hardware or simulators.

In this notebook, we create a 2-qubit circuit, generate its OpenQASM representation, and simulate its output.

## Code Explanation

1. **Quantum Circuit Creation**
   - We define a circuit with 2 qubits.
   - Apply a **Hadamard (H)** gate to the first qubit.
   - Apply a **CNOT** gate with qubit 0 as control and qubit 1 as target.
   - Measure both qubits.

2. **OpenQASM Generation**
   - The `qc.qasm()` function exports the circuit to OpenQASM code.
   - The resulting QASM file shows gate-level operations in standard syntax.

3. **Simulation**
   - The circuit is transpiled and executed using `AerSimulator()`.
   - The measurement results are displayed as a count dictionary (e.g., `{ '00': 512, '11': 512 }`).

## Student Practice Tasks

1. Modify the circuit to have **3 qubits** and apply a different gate sequence.
2. Generate and display the **QASM code** for the new circuit.
3. Identify how **Hadamard** and **CNOT** operations are represented in QASM syntax.
4. Add a **barrier** and observe how it appears in the QASM code.
5. Run the modified circuit and compare simulation results.