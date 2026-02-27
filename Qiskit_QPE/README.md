# Quantum Phase Estimation (QPE) using Qiskit 2.x

This notebook demonstrates **Quantum Phase Estimation (QPE)** — a fundamental quantum algorithm that estimates the phase (eigenvalue) of a given unitary operator.  
QPE is widely used in **Shor’s Algorithm**, **Quantum Chemistry**, and **Hamiltonian simulations**.

---

## Explanation of the Code

### 1. Counting Qubits
These qubits store the estimated binary phase.  
Hadamard gates are applied to create superposition across all possible phase states.

### 2. Eigenstate Preparation
The target qubit is prepared in an eigenstate of the unitary operation (in this demo, simply |1⟩).

### 3. Controlled Unitary Operations
Controlled phase rotations are applied based on powers of two.  
This step encodes the unknown phase into the quantum register.

### 4. Inverse Quantum Fourier Transform (QFT)
The inverse QFT decodes the phase information stored in the counting qubits.

### 5. Measurement
The counting qubits are measured to reveal a binary representation of the estimated phase.

---

## Student Practice Tasks

1. **Change the Phase Value**
   Try different values of `theta` (e.g., 0.25, 0.375, 0.5) and see how the measured output changes.

2. **Increase the Number of Counting Qubits**
   Use 4 or 5 counting qubits for higher precision phase estimation.

3. **Compare with Theoretical Output**
   Calculate the expected binary representation of the phase and compare with simulation results.

4. **Inverse QFT Visualization**
   Add a `qc.draw('mpl')` command before measurement to visualize the inverse QFT structure.

5. **Noise Simulation**
   Introduce a `NoiseModel` using Qiskit Aer and observe how it affects accuracy.

---

## Requirements

Install dependencies:

```bash
pip install qiskit qiskit-aer matplotlib
