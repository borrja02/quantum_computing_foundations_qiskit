# Quantum computing fundamentals with Qiskit.

This repository contains a structured collection of 5 interactive Jupyter Notebooks developed as an introduction to quantum information theory and foundational quantum algorithms. The project covers everything from essential principles like superposition and entanglement to algorithms demonstrating a proven quantum speedup over classical computation.

All implementations are built using **Qiskit 1.x** and simulated locally using the high-performance `Qiskit Aer` framework.

## Repository structure.

The project is organized into five sequential notebooks:

1. **`GHZ_experiment.ipynb` (Simulation of the GHZ experiment)**
   * Explores foundational quantum mechanics by breaking the EPR (Einstein-Podolsky-Rosen) paradox.
   * Implements a 3-qubit maximally entangled Greenberger-Horne-Zeilinger (GHZ) state.
   * Demonstrates the strict contradiction between local hidden variable theories and quantum mechanical predictions through selective measurement bases ($YYX$ vs. $XXX$).

2. **`Deutsch_Jozsa_algorithm.ipynb`**
   * Implements one of the earliest quantum algorithms showing a deterministic exponential speedup.
   * Solves the problem of determining whether a hidden Boolean function $f: \{0,1\}^n \rightarrow \{0,1\}$ is constant or balanced in a single query using phase kickback.

3. **`Bernstein_Vazirani_algorithm.ipynb`**
   * Processes an oracle containing a hidden bitstring $s \in \{0,1\}^n$ defining a Boolean function $f_s(x) = s \cdot x \pmod 2$.
   * Extracts the entire hidden string with $O(1)$ quantum queries, compared to the $O(n)$ queries required by classical trial-and-error approaches.

4. **`Simon_algorithm.ipynb`**
   * Explores the first quantum algorithm to provide an exponential speedup over classical algorithms for a structured black-box problem.
   * Solves Simon's period-finding problem by identifying a hidden period $s \in \{0,1\}^n$ for a function satisfying $f(x) = f(y) \iff x \oplus y \in \{0, s\}$.

5. **`Grover_algorithm.ipynb`**
   * Implements Grover's search algorithm providing a quadratic speedup ($O(\sqrt{N})$) for searching unsorted structures.
   * Includes custom oracle designs, stage-by-stage multi-qubit phase inversions, and amplitude amplification using the diffusion operator.
   * Features a practical demonstration applied to searching prime numbers within a 4-bit space.

## Prerequisites & installation.

To run these notebooks locally without breaking dependencies, we recommend setting up a clean virtual environment:

```bash
# 1. Clone the repository
git clone [https://github.com/YOUR_USERNAME/quantum-computing-fundamentals.git](https://github.com/YOUR_USERNAME/quantum-computing-fundamentals.git)
cd quantum-computing-fundamentals

# 2. Create and activate a virtual environment
python -m venv env
# On Windows:
env\Scripts\activate
# On Linux/macOS:
source env/bin/activate

# 3. Upgrade pip and install requirements
pip install --upgrade pip
pip install -r requirements.txt
