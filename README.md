[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/qT3Kmf07)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24069106&assignment_repo_type=AssignmentRepo)

# Stable Diffusion Image Generator

A Python application that generates images from text prompts using the Stable Diffusion v1.5 model from Hugging Face.

## Overview

This project leverages the power of Stable Diffusion to create high-quality images based on natural language descriptions. Simply provide a text prompt, and the model will generate a corresponding image.

## Features

- 🎨 **Text-to-Image Generation**: Create images from textual descriptions
- 🚀 **GPU Acceleration**: Uses CUDA for fast GPU-accelerated inference
- 🖼️ **Interactive Display**: View generated images immediately
- 💾 **Auto-Save**: Generated images are automatically saved to disk

## Requirements

- Python >= 3.13
- NVIDIA GPU with CUDA support (for GPU acceleration)
- 4GB+ VRAM (recommended for Stable Diffusion v1.5)

## Dependencies

The project uses the following key libraries:

- **torch**: Deep learning framework
- **diffusers**: Hugging Face library for diffusion models
- **transformers**: Pre-trained model library
- **accelerate**: Distributed inference support
- **safetensors**: Safe model serialization
- **matplotlib**: Image visualization

## Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd image-generator-KANISHKA1503
   ```

2. **Create a virtual environment** (optional but recommended):
   ```bash
   python -m venv .venv
   .venv\Scripts\Activate.ps1  # On Windows PowerShell
   # or
   source .venv/bin/activate   # On Linux/macOS
   ```

3. **Install dependencies**:
   ```bash
   pip install -r "Stable Diffusor Image generator/requirements.txt"
   ```

   Or if using the project configuration:
   ```bash
   pip install -e "Stable Diffusor Image generator"
   ```

## Usage

1. **Navigate to the project directory**:
   ```bash
   cd "Stable Diffusor Image generator"
   ```

2. **Run the script**:
   ```bash
   python main.py
   ```

3. **Enter your prompt** when prompted:
   ```
   Enter the prompt to generate the image : a beautiful sunset over mountains
   ```

4. The application will:
   - Generate an image based on your prompt
   - Display the image in a window
   - Save it to `result/generated_image.png`

## Project Structure

```
image-generator-KANISHKA1503/
├── README.md                          # Project documentation
└── Stable Diffusor Image generator/
    ├── main.py                        # Main application script
    ├── pyproject.toml                 # Project configuration
    ├── requirements.txt               # Python dependencies
    ├── README.md                      # Project-specific notes
    └── result/                        # Output directory for generated images
```

## Model Details

- **Model**: Stable Diffusion v1.5 (`runwayml/stable-diffusion-v1-5`)
- **Precision**: float16 (for memory efficiency)
- **Hardware**: NVIDIA GPU with CUDA support

## Performance Tips

- **First Run**: The model will be downloaded on first use (~4GB). Ensure you have sufficient disk space.
- **VRAM Optimization**: Using float16 precision reduces memory usage significantly
- **GPU Required**: This setup is optimized for NVIDIA GPUs. CPU inference will be much slower

## Output

Generated images are saved to the `result/` directory with the filename `generated_image.png`.

## Troubleshooting

- **CUDA not found**: Ensure NVIDIA drivers and CUDA toolkit are properly installed
- **Out of Memory**: Reduce batch size or use a smaller model variant
- **Model not downloading**: Check internet connection and firewall settings
- **GPU not being used**: Verify CUDA is properly installed with `torch.cuda.is_available()`

## License

This project is part of SECE-24-28 coursework.

## Resources

- [Stable Diffusion Documentation](https://huggingface.co/docs/diffusers/index)
- [Hugging Face Model Card](https://huggingface.co/runwayml/stable-diffusion-v1-5)
- [PyTorch CUDA Setup](https://pytorch.org/get-started/locally/)
