# QuantRisk — Quantum-Assisted Portfolio Optimization using QAOA

**QuantumXpo 2026** | Rajiv Gandhi University of Knowledge Technologies (RGUKT) – IIIT Nuzvid

## Problem
Classical portfolio optimization requires selecting an optimal subset of assets
that balances maximum returns with minimum risk. As the number of assets
increases, this becomes a combinatorial (NP-hard) problem that is
computationally expensive for classical algorithms at scale.

## Solution
We formulate the portfolio selection problem as a Quadratic Unconstrained
Binary Optimization (QUBO) problem and solve it using the Quantum Approximate
Optimization Algorithm (QAOA) implemented in Qiskit. The model selects a
fixed-size subset of assets that maximizes expected return while minimizing
risk (covariance), under a budget constraint.

## Methodology
1. Collect historical stock data (expected returns + covariance matrix).
2. Formulate the problem as a QUBO using Qiskit Optimization.
3. Map the QUBO to an Ising Hamiltonian.
4. Run QAOA (Qiskit Algorithms) with the COBYLA optimizer on a simulator.
5. Benchmark against a classical brute-force baseline.

## Tech Stack
Qiskit · Qiskit Optimization · Qiskit Algorithms · Qiskit Runtime · QAOA ·
COBYLA · NumPy · Matplotlib

## Setup
```bash
pip install qiskit qiskit-optimization qiskit-algorithms numpy matplotlib
python quantrisk.py
```

## Output
The script prints the quantum (QAOA) and classical (brute-force) asset
selections and their objective values, and saves a comparison bar chart
(`comparison_chart.png`).
