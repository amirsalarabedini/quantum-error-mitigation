# Quantum Error Mitigation Toolkit

A comprehensive toolkit for exploring noise models and error mitigation techniques in quantum computing using Qiskit.

## Overview

This project provides implementations and demonstrations of various quantum error mitigation techniques to improve the fidelity of noisy quantum circuits. The toolkit addresses the critical challenge of noise in near-term quantum computers by implementing state-of-the-art error mitigation strategies.

## Features

- **Custom Noise Models**: Implementation of depolarizing and thermal relaxation noise models
- **Error Mitigation Techniques**:
  - Zero Noise Extrapolation (ZNE)
  - Dynamical Decoupling (DD)
  - Pauli Twirling
  - Probabilistic Error Cancellation (PEC)
  - Measurement Error Mitigation (TREX and M3)
  - Quantum Error Correction (Shor Code)
- **Error Amplification**: Techniques to study error propagation and sensitivity
- **Visualization Tools**: Compare the effectiveness of different mitigation strategies

## Notebooks

- `Noise_Model_QiskitErrorMitigation.ipynb`: Main notebook exploring various error mitigation techniques
- `Noise_Model_ShorCode.ipynb`: Implementation of Shor's 9-qubit quantum error correction code

## Getting Started

### Prerequisites

- Python 3.7+
- Qiskit 0.39+
- NumPy
- Matplotlib

### Installation

```bash
# Clone the repository
git clone https://github.com/amirsalarabedini/quantum-error-mitigation.git
cd quantum-error-mitigation

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install required packages
pip install -r requirements.txt
```

## Usage

The notebooks can be run in any Jupyter environment. Start with `Noise_Model_QiskitErrorMitigation.ipynb` for a comprehensive overview of error mitigation techniques.

```bash
jupyter notebook Noise_Model_QiskitErrorMitigation.ipynb
```

## Implemented Error Mitigation Techniques

### Zero Noise Extrapolation (ZNE)
Runs circuits with scaled noise levels and extrapolates back to the zero-noise limit.

### Dynamical Decoupling (DD)
Implements XY4 sequence to suppress decoherence during idle periods of quantum circuits.

### Pauli Twirling
Converts coherent errors into stochastic noise to improve the performance of other mitigation techniques.

### Probabilistic Error Amplification (PEA)
Intentionally increases error rates to study error characteristics and test mitigation techniques.

### Probabilistic Error Cancellation (PEC)
Represents ideal gates as linear combinations of noisy operations through quasi-probability sampling.

### Measurement Error Mitigation
- **TREX**: Twirled Readout Error eXtinction for diagonalizing readout error matrices
- **M3**: Matrix-free Measurement Mitigation for efficiently calibrating and correcting measurement errors

### Quantum Error Correction (Shor Code)
Implements Shor's 9-qubit code for protection against arbitrary single-qubit errors.

## Results and Analysis

Each notebook includes detailed visualizations and comparisons between:
- Unmitigated noisy circuits
- Mitigated circuits using different techniques
- Ideal (noise-free) circuit behavior

These comparisons are presented through:
- Probability distribution histograms
- Error rate measurements
- KL divergence calculations

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- IBM Quantum for the Qiskit framework
- The quantum computing community for developing these error mitigation techniques 