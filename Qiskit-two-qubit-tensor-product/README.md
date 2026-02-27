# 🧩 Two-Qubit Circuits and Tensor Products – Qiskit Lab Experiment

This repository contains the Jupyter Notebook and supporting materials for the Qiskit lab experiment on **Two-Qubit Circuits and Tensor Products**.

---

## 🎯 Objective
To construct and simulate two-qubit quantum circuits using Qiskit and understand how tensor products represent multi-qubit states.

---

## 🧰 Requirements
- Python 3.8 or above  
- Qiskit  
- Jupyter Notebook  

Install dependencies:
```bash
pip install qiskit matplotlib
```

---

## 🚀 How to Run
1. Clone the repository  
   ```bash
   git clone https://github.com/<your-username>/qiskit-two-qubit-tensor-product-lab.git
   cd qiskit-two-qubit-tensor-product-lab
   ```
2. Open Jupyter Notebook  
   ```bash
   jupyter notebook Exp06_Two_Qubit_Circuits_and_Tensor_Products.ipynb
   ```
3. Run all cells and observe output histograms.

---

## 🧪 Experiment Summary
- Create a 2-qubit circuit.
- Apply quantum gates (X, H) to explore tensor product states.
- Measure both qubits and visualize the probability distribution using a histogram.

---

## 📊 Expected Output
- **Circuit Diagram:** Shows applied quantum gates.  
- **Measurement Histogram:** Displays measurement outcomes (e.g., 00, 01, 10, 11).  
- **Observation:** Understand how individual qubit operations combine to form multi-qubit states.

---

## 💻 Practical Modification Tasks

Try modifying the code to explore different concepts:

1. **Change Gate Combination**  
   - Apply a **Hadamard gate on both qubits** and observe the output probabilities.  
   - What pattern do you notice in the histogram?

2. **Swap Qubit Roles**  
   - Apply an **X gate on the second qubit** instead of the first.  
   - Compare the output with the original circuit.

3. **Add a CNOT Gate**  
   - Add `qc.cx(0, 1)` after the Hadamard gate.  
   - What kind of state does this create? (Hint: entanglement)

4. **Increase Measurement Shots**  
   - Change the number of shots from 1024 to 4096 in the `execute()` function.  
   - Does the distribution become more stable?

5. **Add a New Visualization**  
   - Use `plot_bloch_multivector` to visualize the combined state of both qubits.  
   - Observe how the Bloch sphere changes before and after measurement.

---

## 📜 License
This project is released under the MIT License.
