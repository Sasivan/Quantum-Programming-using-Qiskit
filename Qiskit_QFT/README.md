# Quantum Fourier Transform (QFT) using Qiskit 2.x

This repository demonstrates how to implement the **Quantum Fourier Transform (QFT)** using **Qiskit 2.x**.  
The QFT is the quantum version of the discrete Fourier transform, used in several key algorithms like **Shor’s Algorithm** and **Phase Estimation**.

---

## Explanation of the Code

### 1. QFT Rotations
The `qft_rotations()` function recursively applies **Hadamard** and **controlled phase** gates to perform the Fourier rotation pattern on qubits.

### 2. Swap Registers
After the rotations, the order of qubits must be **reversed**.  
The `swap_registers()` function swaps the qubits so the output matches the classical Fourier transform order.

### 3. Circuit Creation
The function `qft_circuit()` builds the complete circuit by combining rotations and swaps.

### 4. Simulation
`run_qft()` executes the circuit on **Qiskit AerSimulator** and visualizes the output using a Bloch sphere representation.

---

## Student Practice Tasks

1. **Vary the number of qubits**  
   Try running the QFT for 2, 3, and 4 qubits and observe how the circuit changes.

2. **Inverse QFT**  
   Modify the code to implement the inverse QFT (apply inverse rotations and swap again).

3. **Integration with Phase Estimation**  
   Combine QFT with a simple phase estimation circuit.

4. **Measure Output States**  
   Add measurements and simulate the probability distribution of different states.

5. **Circuit Visualization**  
   Use `qc.draw('mpl')` to plot the circuit diagram.

---

## Requirements

Install the dependencies before running the notebook:

```bash
pip install qiskit qiskit-aer matplotlib
