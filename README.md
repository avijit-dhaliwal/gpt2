# Multi-Language GPT-2 Implementation and Analysis

## Overview

This project implements and analyzes GPT-2, a large language model, across multiple programming languages: Python, C++, JavaScript, and a Python-C++ hybrid. It aims to compare the performance, memory usage, and architecture of GPT-2 implementations in different languages, providing insights into the trade-offs and characteristics of each approach.

## Project Structure

- `gpt2.py`: Python implementation of GPT-2
- `gpt2.cpp`: C++ implementation of GPT-2
- `gpt2.js`: JavaScript implementation of GPT-2
- `gpt2_hybrid.py` and `gpt2_hybrid_cpp.cpp`: Hybrid Python-C++ implementation of GPT-2
- `gpt2_python_analysis.py`: Analysis script for the Python implementation
- `gpt2_cpp_analysis.py`: Analysis script for the C++ implementation
- `gpt2_js_analysis.py`: Analysis script for the JavaScript implementation
- `gpt2_hybrid_analysis.py`: Analysis script for the hybrid implementation
- `gpt2_comparative_analysis.py`: Script for comparing results across all implementations
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
## Usage

1. Run individual implementations:
python gpt2.py <input_size>
./gpt2_cpp <input_size>
node gpt2.js <input_size>
python gpt2_hybrid.py <input_size>
Copy


Copy

## Usage

1. Run individual implementations:
```bash
python gpt2.py <input_size>
./gpt2_cpp <input_size>
node gpt2.js <input_size>
python gpt2_hybrid.py <input_size>
```

Replace <input_size> with an integer value representing the desired input sequence length. 
For example:

```bash
python gpt2.py 100
./gpt2_cpp 500
node gpt2.js 1000
python gpt2_hybrid.py 250
```

Typical values range from 10 to 1000, but you can experiment with different sizes to see how 
the models perform with varying input lengths.

2. Run analysis scripts:
```bash
python gpt2_python_analysis.py
python gpt2_cpp_analysis.py
python gpt2_js_analysis.py
python gpt2_hybrid_analysis.py
```

These scripts will automatically test a range of input sizes and generate analysis results.

3. Run comparative analysis:
```bash
python gpt2_comparative_analysis.py
```

This script compares the results from all implementations.

## Analysis Outputs

Each analysis script generates:
- A PDF file with visualizations of performance benchmarks, memory usage analysis, and model architecture.
- A CSV file with raw data for use in the comparative analysis.

The comparative analysis script produces an additional PDF with cross-implementation comparisons.

## Contributing

Contributions to improve the implementations, extend the analysis, or add new language implementations are welcome. Please submit a pull request or open an issue to discuss proposed changes.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- OpenAI for the original GPT-2 model
- The open-source community for libraries and tools used in this project

## Contact

avijit.dhaliwal@gmail.com