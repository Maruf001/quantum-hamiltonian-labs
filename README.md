# quantum-hamiltonian-labs
GPU-accelerated quantum dynamics labs using NVIDIA CUDA-Q, covering Jaynes–Cummings, open systems, and time-dependent Hamiltonians – as completed during during the Quantum Device Design Workshop (Advanced Track), UCLA 2025


# CUDA-Q Quantum Dynamics Labs

This repository contains GPU-accelerated Jupyter notebooks that simulate time evolution of quantum systems using [NVIDIA CUDA-Q Dynamics](https://nvidia.github.io/cuda-quantum/latest/using/dynamics.html). The labs are designed for hands-on understanding of Hamiltonian dynamics, dissipation, and driven quantum systems in Cavity QED contexts.

## 🧪 Included Labs

### 📘 Lab 1: Jaynes–Cummings Hamiltonian & Open Quantum Systems

This notebook introduces the CUDA-Q Dynamics simulator and walks through:

- Building the **Jaynes–Cummings model** using built-in CUDA-Q operators.
- Solving the Schrödinger equation for coherent qubit-photon exchange.
- Adding **collapse operators** to model noise via Lindblad evolution:
  - Photon decay (loss)
  - Photon excitation
  - Qubit dephasing
- Generalization to the **Tavis–Cummings model** with many qubits coupled to a shared resonator.

📈 Outputs:
- Expectation value plots over time.
- Effects of noise, coupling, and dimensionality.
- Speed-up insights when simulating large systems on GPU.

---

### 📘 Lab 2: Time-Dependent Driven Hamiltonians

This lab explores:

- Constructing **time-dependent drive pulses**.
- Creating and combining custom `Schedule` objects.
- Defining **drive envelopes** for coherent control (e.g., Gaussian-modulated drives).
- Simulating **Landau-Zener transitions**.
- Exploring resonance, detuning, and population inversion.

📈 Outputs:
- Time-resolved population plots for driven systems.
- Effect of drive amplitude, duration, and detuning.
- Comparison between different pulse profiles and dynamics.

---

## 🔬 Why Use CUDA-Q for Dynamics?

While traditional quantum circuit simulators apply logic gates, **CUDA-Q Dynamics** simulates the full continuous-time evolution of open or closed quantum systems, capturing device-level physics including:

- Photon-qubit coupling
- Decoherence and dissipation
- Continuous drives and pulse shaping
- Strong scaling on GPUs (>1000x speedup in some systems)

---

## 🚀 Technologies Used

- [CUDA-Q Dynamics](https://nvidia.github.io/cuda-quantum/)
- `cupy` (GPU-backed linear algebra)
- `matplotlib`, `numpy`
- `cudaq.operators`, `cudaq.evolve()`
- Jupyter Notebooks

