# QKD-BB84-Academic-Showcase: Quantum Cryptography and Vulnerability Analysis
## In-Depth R&D Project Summary: Verification of the Quantum Key Distribution Protocol (BB84)

---

### I. Introduction and Scientific Relevance

This project is a complete software simulator of the **BB84 protocol** (Bennett and Brassard 1984), implemented using the **IBM Qiskit** library. The work addresses the urgent need to develop quantum-resistant communication systems.

**Scientific Contribution:** The project focuses not only on simulating a successful key exchange but, crucially, on the **verification of the eavesdropper detection threshold (Eve)** through Quantum Bit Error Rate (QBER) analysis.

**Developer:** romaprogrammist
**Developer Status:** 9th Grade Student (Belarus)
**Project Commit Date:** November 2025

---

### II. Implementation Details and Methodology

The project uses Python, Qiskit, and NumPy to create, manipulate qubits, and perform efficient mathematical calculations.

#### 1. Quantum Encoding
* **Bases:** Two non-orthogonal bases are used (Standard/Z and Diagonal/X).
* **Operations:** For encoding bits 0 and 1, Alice applies Pauli-X (`qc.x(i)`) and Hadamard (`qc.h(i)`) gates, depending on the randomly chosen basis.

#### 2. Eavesdropping Attack Modeling
* **Method:** The **"Measure-Resend" attack** is implemented (function `eavesdrop_on_qubits`).
* **Mechanism:** Eve randomly selects a basis and measures the qubit, causing its wave function to collapse. Eve then prepares and sends a **new** qubit to Bob based on her measurement.

#### 3. Vulnerability Analysis (QBER)
* **QBER Calculation:** The `calculate_qber` function compares the final sieved keys of Alice and Bob.
* **Security Criterion:** The simulator uses a QBER threshold of **0.1** (10%). If QBER exceeds this value, the system issues a warning about a **compromised channel**.

---

### III. Conclusions and R&D Contribution

The project demonstrates the fundamental security principle of QKD: **any attempt by an eavesdropper to measure the quantum state inevitably introduces detectable disturbances.**

* **Practical Proof:** The simulator proves that Eve's interference **significantly increases the error rate** compared to the control scenario.
* **Academic Value:** A verified platform has been created for further research and testing the resilience against various types of quantum attacks.

### 🔒 Access to Full Implementation (R&D Implementation)

The full source code (file `BB84_Sim.py`), detailed QBER analysis results, and the official **Scientific Report (`Simfin.pdf`)** are held in a **Private Repository** to protect Intellectual Property.


* **For temporary access** to the full code and report (only for academic audit, application to innovation programs, or hiring procedures), please contact the Author. **Collaboration with local R&D teams in Belarus is especially welcome.**

---

### 📧 Contact Information

**Author and Professional Correspondence:** romaprogrammist
**Email:** rommaxcontact@gmail.com
