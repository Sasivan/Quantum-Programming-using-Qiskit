# 🧪 Initializing |0⟩ and |1⟩

This task sheet accompanies the notebook `Qiskit_qubit_measure.ipynb`.  
In this lab, we explored how to prepare and measure the **basis states** of a qubit:
- |0⟩ (default starting state)  
- |1⟩ (using an X gate to flip the qubit)

We used the **AerSimulator** in Qiskit to run the experiments.

---

## ✅ Tasks

### Task 1: Verify |0⟩ and |1⟩
1. Run the given program for |0⟩ and |1⟩.  
2. Record the counts for **512 shots**.  
3. Question: Are the results **deterministic** or **random**? Why?

---

### Task 2: Change the number of shots
1. Modify the code to run with **10 shots** and **1000 shots**.  
2. Observe the results. Do they change? Why or why not?

---

### Task 3: Superposition with Hadamard
1. Modify the circuit to apply a **Hadamard (H)** gate before measurement:
   ```python
   qc = QuantumCircuit(1, 1)
   qc.h(0)
   qc.measure_all()
   ```
2. Run with 512 shots.  
3. Question: What outcomes do you see? Are they deterministic or probabilistic?

---

### Task 4: Combine X and H gates
1. Create a circuit that applies **X** followed by **H**:
   ```python
   qc.x(0)
   qc.h(0)
   qc.measure_all()
   ```
2. Run with 512 shots.  
3. Predict the results **before running**: what distribution do you expect?  
   *(Hint: Think about how H acts on |1⟩).*  

---

### Task 5 (Challenge)
- Build a **2-qubit circuit** where:  
  - Qubit 0 is |0⟩  
  - Qubit 1 is |1⟩  
- Measure both.  
- Run with 512 shots.  
- Question: What outputs do you expect? Does the simulator confirm it?

---

## 📝 Notes
- Remember:  
  - Qubits start in |0⟩.  
  - `X` flips |0⟩ ↔ |1⟩.  
  - `H` creates superposition.  
  - Measurement collapses the qubit into `0` or `1`.  
