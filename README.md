# Hybrid Quantum-Classical Routing Framework (HQCRF) for MANETs

<p align="center">




\

</p>

---

# Hybrid Quantum-Classical Routing Framework (HQCRF)

A research implementation of a **Hybrid Quantum-Classical Routing Framework (HQCRF)** for **Mobile Ad hoc Networks (MANETs)** that combines adaptive classical routing with quantum search optimization using **Grover's Algorithm** executed on **real IBM Quantum hardware**.

The framework addresses multi-objective routing by jointly optimizing:

* Link Stability
* Energy Awareness
* Trust
* Interference Awareness
* Path Reliability
* Backup Route Diversity

Unlike conventional routing algorithms that optimize a single objective, HQCRF integrates classical preprocessing and quantum optimization to efficiently identify reliable routing paths while respecting current NISQ hardware limitations.

---

# Research Highlights

* Hybrid Quantum-Classical routing architecture
* Real IBM Quantum hardware execution
* Hierarchical Grover Search
* Adaptive Beam Search candidate generation
* Dual-layer reliability model
* Multi-objective routing optimization
* Immediate backup routing mechanism
* Mobility-aware MANET simulation
* Jamming attack simulation
* Interference-aware routing
* Experimental validation on networks containing **100–500 nodes**

---

# Repository Structure

```text
HQCRF-Implementation
│
├── scenario-1-normal-network.ipynb
├── scenario-2-jamming-attack.ipynb
├── scenario-3-interference-aware-routing.ipynb
│
├── paper/
│   └── HQCRF_Research_Paper.pdf
│
├── requirements.txt
├── LICENSE
└── README.md
```

---

# Project Overview

Routing in Mobile Ad hoc Networks (MANETs) is inherently challenging because the network topology changes dynamically due to node mobility. Traditional routing protocols generally optimize a single metric, such as shortest path or minimum hop count, making them unsuitable for environments where routing decisions must simultaneously consider:

* Link Stability
* Node Energy
* Trust
* Wireless Interference
* Reliability
* Dynamic Mobility

HQCRF introduces a hybrid approach where classical algorithms reduce the routing search space before Grover's quantum search identifies optimal candidate paths. The implementation is designed specifically for practical Noisy Intermediate-Scale Quantum (NISQ) devices and validated on IBM Quantum backends.

---

# Framework Architecture

```
Network Topology
        │
        ▼
Adaptive Beam Search
        │
        ▼
Candidate Path Generation
        │
        ▼
Cost Evaluation
        │
        ▼
Dual-Layer Reliability Filtering
        │
        ▼
Hierarchical Grover Search
        │
        ▼
Classical Verification
        │
        ▼
Primary Route Selection
        │
        ▼
Backup Route Generation
        │
        ▼
Packet Transmission
        │
        ▼
Performance Evaluation
```

---

# Core Components

## Adaptive Beam Search

Reduces the exponential routing search space using directional beam search with adaptive relaxation.

---

## Dual-Layer Reliability Model

Evaluates:

* Link Stability
* Path Stability
* Reliability Product

Low-quality paths are discarded before quantum optimization.

---

## Hierarchical Grover Search

Implements Grover's Algorithm using:

* Oracle construction
* Noise-aware iteration selection
* Candidate chunking
* Parallel execution
* Classical verification

This enables efficient routing despite the limited qubit availability of current IBM Quantum hardware.

---

## Immediate Backup Routing

Generates backup routes without requiring another quantum execution, enabling rapid recovery from link failures caused by mobility.

---

# Simulation Scenarios

## Scenario 1 — Normal MANET

Notebook:

```text
scenario-1-normal-network.ipynb
```

Features:

* No attackers
* Link stability evaluation
* Baseline routing performance
* Energy-aware routing

---

## Scenario 2 — Jamming Attack

Notebook:

```text
scenario-2-jamming-attack.ipynb
```

Features:

* Random jammers
* Constant jammers
* Reactive jammers
* Trust-aware routing
* Attack impact analysis

---

## Scenario 3 — Interference-Aware Routing

Notebook:

```text
scenario-3-interference-aware-routing.ipynb
```

Features:

* Jammer detection
* Jammed node exclusion
* Backup routing
* Interference-aware optimization
* Recovery mechanism evaluation

---

# Technologies Used

* Python
* Qiskit
* IBM Quantum Runtime
* NetworkX
* NumPy
* Pandas
* Matplotlib
* Google Colab
* Jupyter Notebook

---

# Installation

Clone the repository.

```bash
git clone https://github.com/<YOUR_USERNAME>/HQCRF-Implementation.git
```

Move into the repository.

```bash
cd HQCRF-Implementation
```

Install dependencies.

```bash
pip install -r requirements.txt
```

---

# Running the Project

Run the notebooks in the following order.

1. Scenario 1
2. Scenario 2
3. Scenario 3

Each notebook is self-contained and reproduces the corresponding experimental scenario described in the paper.

---

# Performance Evaluation

The framework is evaluated using:

* Packet Delivery Ratio (PDR)
* Packet Loss Ratio (PLR)
* End-to-End Delay
* Throughput
* Energy Consumption
* Recovery Rate
* Route Stability
* Quantum-Classical Agreement

---

# Experimental Highlights

The proposed framework demonstrates:

* High packet delivery under dynamic mobility
* Reliable routing under jamming attacks
* Efficient interference-aware routing
* Fast backup route recovery
* High agreement between classical and quantum optimization
* Successful execution on real IBM Quantum hardware

---

# Research Contributions

* First practical Hybrid Quantum-Classical routing framework for MANETs validated on IBM Quantum hardware.
* Adaptive beam-search-based candidate reduction.
* Hierarchical Grover optimization for large candidate sets.
* Dual-layer reliability scoring mechanism.
* Diversity-aware backup routing.
* Comprehensive evaluation across multiple network conditions.

---

# Future Work

Potential extensions include:

* Larger MANET deployments
* Quantum Error Correction integration
* Quantum Machine Learning-assisted routing
* Dynamic quantum resource allocation
* Multi-backup routing strategies
* Distributed quantum networking

---

# Acknowledgements

This work utilizes:

* IBM Quantum
* Qiskit
* Google Colab
* NetworkX
* NumPy
* Pandas
* Matplotlib

Special thanks to the Quantum and Nano Devices Lab, PES University, for supporting this research.
