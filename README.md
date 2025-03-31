# Fine-Tuning LLaMA 3.2 with Unsloth

## Overview
This repository contains scripts and Jupyter notebooks for fine-tuning the LLaMA 3.2 model using Unsloth. The goal is to efficiently train and deploy a state-of-the-art language model for various NLP applications.

## Features
- Fine-tuning LLaMA 3.2 using Unsloth for optimized GPU performance.
- Uses Hugging Face datasets and `trl` for supervised fine-tuning.
- Supports Retrieval-Augmented Generation (RAG) integration.
- Compatible with NVIDIA GPUs (Unsloth does not support Intel GPUs yet).

## Prerequisites
Ensure you have the following installed before running the scripts:

- Python 3.8+
- PyTorch (with CUDA support for GPU acceleration)
- `unsloth`
- `datasets`
- `transformers`
- `trl`
- `torch`

## Installation
```bash
# Clone the repository
git clone https://github.com/cbandi18/llama3.2-fine-tuning.git
cd llama3.2-fine-tuning

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

# Install dependencies
pip install -r requirements.txt
```

## Running the Fine-Tuning Script

Execute the provided Jupyter Notebook or Python script:
```bash
jupyter notebook llama3_2_finetuning.ipynb
```
Or run the Python script (if applicable):
```bash
python fine_tune.py
```

## Troubleshooting
- If you encounter `NotImplementedError: Unsloth currently only supports GPUs!`, ensure you have an NVIDIA GPU installed and CUDA properly configured.
- Intel Iris Xe GPUs are not currently supported by Unsloth.
- Check `torch.cuda.is_available()` in Python to verify if your GPU is being recognized.

## Future Enhancements
- Add support for CPU-based fine-tuning.
- Explore alternative libraries for Intel GPU support.
- Implement LoRA/QLoRA for efficient parameter tuning.

## Contributing
Feel free to submit pull requests or open issues for bug fixes and feature suggestions.

## License
This project is licensed under the MIT License.