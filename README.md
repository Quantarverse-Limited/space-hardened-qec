# Space-Hardened Quantum Error Correction for Orbital Computing
This repository contains the implementation and simulation code for space-hardened Quantum Error Correction (QEC) protocols designed for the QUANTARNET orbital computing initiative. These protocols form the basis of WP2 (Work Package 2) for the STFC Cross Cluster Proof of Concept SparQ Quantum Computing project.

## Repository Contents

- **Quantum circuit implementation** of a [[4,2,2]] stabilizer code architecture with dual-round syndrome extraction
- **Realistic space radiation noise models** simulating Single Event Effects (SEEs) and other radiation-induced errors
- **Simulation results** with 1,500,000 shots demonstrating robust error detection capabilities
- **Analysis tools** for post-selection validation and error type differentiation
- **Visualization code** for error syndrome distribution
- **Tomography Analysis** to reconstruct the quantum state after applying the error correction scheme.
- **Quantum Error Correction Circuit for Rigetti Ankaa-3** designed for execution of  quantum error correction (QEC) circuit on the Rigetti Ankaa-3 quantum processor  
## Key Features

- 94.07% error-free operation demonstrated under simulated space radiation conditions
- Clear differentiation between different quantum error types (X: 2.43%, Z: 2.23%, Y: 1.27%)
- 86.10% post-selection validity, confirming measurement reliability in noise environments
- Symmetrical circuit design balancing detection capabilities across different error types

## Technical Details
The implementation uses a custom depolarizing noise model to simulate space radiation effects on quantum hardware. The circuit follows a two-round syndrome extraction protocol that enables reliable differentiation between various quantum error types:
- 00: No error (94.07%)
- 10: X error (2.43%)
- 01: Z error (2.23%)
- 11: Y error (1.27%)

## State Tomography

The StateTomography module from qiskit_experiments is used to analyze the quantum state.

The QEC circuit is executed on a simulated quantum backend.

## Requirements
 
To execute the Quantum error Correction for executing on the Rigetti Ankaa-3 Processor, you need:
Python 3.7+

AWS Braket SDK 
```bash
(pip install amazon-braket-sdk)
```
Boto3 
```bash
(pip install boto3)
```
NumPy 
```bash
(pip install numpy)
```
Matplotlib 
```bash
(pip install matplotlib)
```



## Usage

The main implementation is available in `SpaceHardenedQEC.ipynb`, which can be run with Qiskit to reproduce our simulation results.

The implementation of Tomography is available in `Tomography Analysis.ipynb`, in which the analysis results from the state tomography experiment showing reconstructed quantum state information.
The Execution of Quantum Error Correction circuit adapted for the Rigetti Ankaa-3 quantum processor using Amazon Braket SDK is available in `Rigetti QC circuit Simulation.ipynb`

## Citation

If you use this code or our QEC approach in your research, please cite our work:

```
Quantarverse Limited. (2025). Space-Hardened Quantum Error Correction for Orbital Computing.
STFC Cross Cluster Proof of Concept: SparQ Quantum Computing Call.
```

## Contact

For questions or collaboration opportunities, contact:
- Email: aa@quantarverse.com


## Acknowledgments
This work is supported by the Science and Technology Facilities Council (STFC) Cross Cluster Proof of Concept: SparQ Quantum Computing Call, with collaboration from Radiation Analysis Services Ltd and the Quantum Software Lab at the University of Edinburgh.
