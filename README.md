# Variational Quantum Eigensolver (VQE) from Scratch

## Overview
This project implements a **Variational Quantum Eigensolver (VQE)** from scratch using Qiskit. The goal is to estimate the lowest eigenvalue of a given Hamiltonian matrix by leveraging quantum computing techniques.

## Features
- Decomposition of a unitary matrix into **Pauli operators**.
- Implementation of **quantum measurement strategies** using basis transformations.
- Estimation of eigenvalues via **quantum circuit simulation**.
- Parameterized circuit optimization to minimize the Hamiltonian energy.

## Prerequisites
Make sure you have the following dependencies installed:

```bash
pip install qiskit numpy matplotlib
```

## Usage
Clone the repository and run the Jupyter Notebook:

```bash
git clone https://github.com/yourusername/vqe-from-scratch.git
cd vqe-from-scratch
jupyter notebook vqe_from_scratch.ipynb
```

## Implementation Details
1. **Hamiltonian Decomposition**: The unitary matrix is expressed in terms of tensor products of Pauli operators (I, X, Y, Z).
2. **Quantum Circuit Design**: Qubits are manipulated using **CNOT, Hadamard, and Phase gates** to measure observables.
3. **Energy Estimation**: The expectation value of the Hamiltonian is computed to approximate the lowest eigenvalue.
4. **Optimization**: The parameters of the trial wavefunction are updated iteratively to minimize the energy.

## Quantum Circuit Example
```python
import qiskit as qk

qc = qk.QuantumCircuit(2, 1)
qc.h(0)
qc.cx(0,1)
qc.measure(1,0)
qc.draw(output="mpl")
```

## Results
The VQE algorithm successfully approximates the ground state energy of the given Hamiltonian by iteratively updating the parameters of the ansatz.

## References
- [Qiskit Documentation](https://qiskit.org/documentation/)
- [Variational Quantum Eigensolver Paper](https://arxiv.org/abs/1304.3061)

---
Feel free to contribute or open issues if you have suggestions!

