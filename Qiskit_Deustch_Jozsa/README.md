# 🧠 Qiskit_Deustch_Jozsa

## 📘 Overview
This repository demonstrates the **Deutsch–Jozsa algorithm** using **Qiskit 2.x**.  
The algorithm determines whether a given Boolean function \( f(x) \) is **constant** (same output for all inputs) or **balanced** (equal number of 0s and 1s as outputs) using **a single quantum query**, showcasing one of the earliest examples of **quantum speed-up** over classical algorithms.

The implementation is provided in the Jupyter notebook **`Qiskit_Deustch_Jozsa.ipynb`**, fully compatible with the latest Qiskit 2.x API.

---

## 🧩 Features
- Implementation of **constant** and **balanced** oracles.  
- Execution on **Qiskit AerSimulator**.  
- Circuit visualization and measurement histograms.  
- Step-by-step comments for easy learning.  
- Ready for classroom or self-paced lab exercises.

---

## ⚙️ Requirements
Make sure you have Python ≥ 3.9 and the following packages installed:

```bash
pip install qiskit qiskit-aer matplotlib
```

Verify installation:
```bash
python -m qiskit --version
```

---

## 🚀 How to Run
1. Clone or download this repository:
   ```bash
   git clone https://github.com/<your-username>/Qiskit_Deustch_Jozsa.git
   cd Qiskit_Deustch_Jozsa
   ```
2. Open the Jupyter notebook:
   ```bash
   jupyter notebook Qiskit_Deustch_Jozsa.ipynb
   ```
3. Run all cells sequentially to see:
   - Circuit diagrams  
   - Oracle behavior  
   - Measurement results  
   - Interpretation (constant or balanced)

---

## 📊 Expected Output
- For a **constant oracle**, the measurement result will be `000...0`.
- For a **balanced oracle**, you will observe a non-zero bitstring such as `101` or `010`.

---

## 🎯 Programming Tasks for Students

### 🧩 Task 1 — Modify the Oracle
Create your own **balanced oracle** function that flips the ancilla for half of all possible inputs (not just parity).  
Hint: You can use `cx` and `ccx` gates creatively.

### ⚙️ Task 2 — Change the Number of Input Qubits
Run the Deutsch–Jozsa algorithm with different numbers of input qubits (e.g., `n = 2, 4, 5`).  
Observe how the circuit depth and output pattern change.

### 📈 Task 3 — Add Noise Simulation
Simulate the same circuit using a **noisy backend**:
```python
from qiskit_aer.noise import NoiseModel
```
and observe how measurement outcomes are affected.

### 💡 Task 4 — Run on IBM Quantum Device
Modify the code to run on a real IBM Quantum backend using:
```python
from qiskit_ibm_runtime import QiskitRuntimeService
```
Compare real hardware results with simulator outcomes.

### 🧮 Task 5 — Circuit Analysis
Print the unitary of your oracle using:
```python
qc = QuantumCircuit(...)
oracle_func(qc, ...)
print(qc.to_gate().definition)
```
and explain how it implements the function \( f(x) \).

---

## 🧑‍🏫 Instructor Notes
This notebook is ideal for:
- Quantum Computing labs
- Courses introducing **quantum algorithms**
- Assignments demonstrating **quantum-classical speed-up**
- Qiskit 2.x training sessions

---

## 📂 Repository Structure
```
Qiskit_Deustch_Jozsa/
│
├── Qiskit_Deustch_Jozsa.ipynb     # Main implementation notebook
├── README.md                      # This documentation file
└── images/                        # (Optional) save circuit screenshots or histograms here
```

---

## 📚 References
- M. A. Nielsen & I. L. Chuang, *Quantum Computation and Quantum Information*  
- [Qiskit Textbook: Deutsch–Jozsa Algorithm](https://qiskit.org/textbook/ch-algorithms/deutsch-jozsa.html)  
- [Qiskit API Documentation](https://docs.quantum.ibm.com/api/qiskit)
