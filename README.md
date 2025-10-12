te # Qiskit 1-Qubit Verification (Qiskit 2.x)

This repository contains a simple Qiskit program to verify installation and demonstrate the basics of **quantum circuits** using the **AerSimulator**.

## 📂 File
- `Qiskit_1-qubit_Verify.ipynb` → Jupyter notebook with code.

## 📝 Program Explanation
- Creates a **1-qubit quantum circuit**.  
- Applies a **Hadamard gate (H)** to put the qubit into superposition.  
- Measures the qubit into a classical bit.  
- Runs the circuit on the **AerSimulator** for 1024 shots.  
- Prints the result counts (expected ~50% `0`, ~50% `1`).  

Example output:
```
Counts: {'0': 503, '1': 521}
```

---

## 🎯 Student Tasks
To strengthen understanding, try the following:

1. **Change number of shots**  
   - Run with `shots=10`, `1000`, and `10000`.  
   - Compare how close the results are to a 50–50 split.

2. **Two-qubit superposition**  
   - Apply `H` to both qubits.  
   - Expect outcomes: `00, 01, 10, 11` with ~25% each.

3. **Entangled state (Bell state)**  
   ```python
   qc.h(0)
   qc.cx(0, 1)
   qc.measure_all()
   ```
   - Expected: only `00` and `11`.

4. **Try an X gate**  
   - Replace `H` with `X`.  
   - Expected: always `1`.

5. **Three-qubit superposition** *(challenge)*  
   - Apply `H` to all 3 qubits.  
   - Expect 8 outcomes (`000` → `111`) with ~12.5% each.

---

## 🚀 Getting Started
1. Install Qiskit:
   ```bash
   pip install qiskit qiskit-aer
   ```
2. Open the notebook:
   ```bash
   jupyter notebook Qiskit_1-gubit_Verify.ipynb
   ```
3. Run the cells and explore the results!

---

👨‍🏫 This notebook can be used as a **classroom demo** to introduce:  
- Quantum circuits  
- Superposition  
- Measurement outcomes  
- Entanglement basics
