# Multi-Language GPT-2 Implementation and Analysis

## Overview

This project implements and analyzes GPT-2, a large language model, across multiple programming languages: Python, C++, JavaScript, and a Python-C++ hybrid. It aims to compare the performance, memory usage, and architecture of GPT-2 implementations in different languages, providing insights into the trade-offs and characteristics of each approach.

## Project Structure

- `implementations/`: Contains the GPT-2 implementations in different languages
  - `gpt2.py`: Python implementation
  - `gpt2.cpp`: C++ implementation
  - `gpt2.js`: JavaScript implementation
  - `gpt2_hybrid.py` and `gpt2_hybrid_cpp.cpp`: Hybrid Python-C++ implementation
- `analysis/`: Contains scripts for analyzing each implementation
  - `gpt2_python_analysis.py`: Analysis script for the Python implementation
  - `gpt2_cpp_analysis.py`: Analysis script for the C++ implementation
  - `gpt2_js_analysis.py`: Analysis script for the JavaScript implementation
  - `gpt2_hybrid_analysis.py`: Analysis script for the hybrid implementation
  - `gpt2_comparative_analysis.py`: Script for comparing results across all implementations
- `utils/`: Utility scripts
  - `onnx_export.py`: Script for exporting the PyTorch model to ONNX format
- `models/`: Directory to store the ONNX model
- `results/`: Directory to store analysis results
- `setup.py`: Setup file for building the C++ extension used in the hybrid implementation

## Requirements

See `requirements.txt` for a full list of Python dependencies. Additionally, you'll need:

- C++ compiler with C++17 support
- Node.js and npm
- Eigen library (for C++ implementation)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/gpt2-multi-language.git
cd gpt2-multi-language
```

2. Install Python dependencies:
```bash
pip install -r requirements.txt
```

3. Install Node.js dependencies:
```bash
npm install @tensorflow/tfjs-node
```

4. Build the C++ extension for the hybrid implementation:
```bash
python setup.py build_ext --inplace
```

5. Export the PyTorch model to ONNX format:
```bash
python utils/onnx_export.py


## Usage

1. Run individual implementations:
```bash
python implementations/gpt2.py <input_size>
./implementations/gpt2_cpp <input_size>
node implementations/gpt2.js <input_size>
python implementations/gpt2_hybrid.py <input_size>
```

Replace <input_size> with an integer value representing the desired input sequence length. 

For example:
```bash
python implementations/gpt2.py 100
./implementations/gpt2_cpp 500
node implementations/gpt2.js 1000
python implementations/gpt2_hybrid.py 250
```

Typical values range from 10 to 1000, but you can experiment with different sizes to see how 
the models perform with varying input lengths.

2. Run analysis scripts:
```bash
python analysis/gpt2_python_analysis.py
python analysis/gpt2_cpp_analysis.py
python analysis/gpt2_js_analysis.py
python analysis/gpt2_hybrid_analysis.py
```

These scripts will automatically test a range of input sizes and generate analysis results.

3. Run comparative analysis:
```bash
python analysis/gpt2_comparative_analysis.py
```

This script compares the results from all implementations.

## Analysis Outputs

Each analysis script generates:
- A PDF file in the `results/` directory with visualizations of performance benchmarks, memory usage analysis, and model architecture.
- A CSV file in the `results/` directory with raw data for use in the comparative analysis.

The comparative analysis script produces an additional PDF with cross-implementation comparisons.

## ONNX Model

The `utils/onnx_export.py` script exports the PyTorch model to ONNX format, which is stored in the `models/` directory. This ONNX model is used by the C++ and JavaScript implementations for inference.

## Contributing

Contributions to improve the implementations, extend the analysis, or add new language implementations are welcome. Please submit a pull request or open an issue to discuss proposed changes.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- OpenAI for the original GPT-2 model
- The open-source community for libraries and tools used in this project

## Contact
avijit.dhaliwal@gmail.com