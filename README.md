# 🎨 Text-to-Image Generation

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

> Transform your text prompts into stunning images using Stable Diffusion models with autocast support

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Demo](#demo)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## 🌟 Overview

This project implements a text-to-image generation system using state-of-the-art Stable Diffusion models. Simply input a text description, and the model generates corresponding high-quality images. The implementation leverages autocast for efficient memory usage and faster inference.

## ✨ Features

- 🚀 **Fast Generation**: Optimized with autocast for quick image generation
- 🎯 **High Quality**: Produces detailed, high-resolution images
- 💡 **Easy to Use**: Simple interface for text-to-image conversion
- 🔧 **Customizable**: Adjust parameters like steps, guidance scale, and resolution
- 📊 **Stable Diffusion**: Built on proven diffusion model architecture
- 🖼️ **Multiple Formats**: Supports various output image formats

## 🎥 Demo

<!-- Add your demo images here -->
```
Input: "A serene landscape with mountains at sunset"
Output: [Generated Image]
```

*Note: Add screenshots or GIFs of your results here*

## 🛠️ Tech Stack

- **Python 3.8+**
- **PyTorch**: Deep learning framework
- **Diffusers**: Hugging Face diffusion models library
- **Transformers**: NLP model support
- **CUDA**: GPU acceleration (optional but recommended)
- **PIL/Pillow**: Image processing

## 📦 Installation

### Prerequisites

- Python 3.8 or higher
- CUDA-capable GPU (recommended for faster generation)
- 8GB+ RAM (16GB recommended)

### Setup

1. **Clone the repository**
```bash
git clone https://github.com/rohithreddy5250/Text-to-Image-Generation-.git
cd Text-to-Image-Generation-
```

2. **Create a virtual environment** (recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Download the model** (if not auto-downloaded)
```bash
# The model will be automatically downloaded on first run
# Ensure you have ~4GB free space for model weights
```

## 🚀 Usage

### Basic Usage

```python
from text_to_image import generate_image

# Generate an image from text
prompt = "A beautiful sunset over the ocean with palm trees"
image = generate_image(prompt)
image.save("output.png")
```

### Advanced Usage

```python
from text_to_image import generate_image

# Customize generation parameters
prompt = "A futuristic city with flying cars at night"
image = generate_image(
    prompt=prompt,
    num_inference_steps=50,      # More steps = better quality
    guidance_scale=7.5,           # How closely to follow prompt
    height=512,                   # Image height
    width=512,                    # Image width
    seed=42                       # For reproducible results
)
image.save("futuristic_city.png")
```

### Command Line Interface

```bash
python generate.py --prompt "Your text prompt here" --output output.png --steps 50
```

### Parameters Explained

| Parameter | Description | Default | Range |
|-----------|-------------|---------|-------|
| `prompt` | Text description of desired image | Required | Any text |
| `num_inference_steps` | Number of denoising steps | 50 | 20-100 |
| `guidance_scale` | How closely to follow prompt | 7.5 | 1-20 |
| `height` | Output image height | 512 | 256-1024 |
| `width` | Output image width | 512 | 256-1024 |
| `seed` | Random seed for reproducibility | Random | Any integer |

## 📁 Project Structure

```
Text-to-Image-Generation-/
│
├── models/                  # Pre-trained model files
├── outputs/                 # Generated images
├── src/
│   ├── text_to_image.py    # Main generation logic
│   ├── utils.py            # Helper functions
│   └── config.py           # Configuration settings
├── generate.py             # CLI interface
├── requirements.txt        # Python dependencies
├── README.md              # This file
└── LICENSE                # License information
```

## 🎯 Example Prompts

Try these prompts to get started:

1. **Nature**: "A peaceful forest with rays of sunlight filtering through trees"
2. **Architecture**: "Modern minimalist house with glass walls in the mountains"
3. **Fantasy**: "A magical library filled with floating books and glowing crystals"
4. **Sci-Fi**: "A spaceship landing on an alien planet with two moons"
5. **Abstract**: "Abstract geometric patterns in vibrant colors"

## ⚙️ Configuration

Edit `config.py` to customize default settings:

```python
DEFAULT_MODEL = "stabilityai/stable-diffusion-2-1"
DEFAULT_STEPS = 50
DEFAULT_GUIDANCE = 7.5
DEFAULT_SIZE = (512, 512)
```

## 🔧 Troubleshooting

### Common Issues

**Out of Memory Error**
- Reduce image size (height/width)
- Decrease num_inference_steps
- Use CPU instead of GPU (slower but uses less memory)

**Slow Generation**
- Ensure CUDA is properly installed
- Use GPU acceleration
- Reduce num_inference_steps

**Poor Quality Images**
- Increase num_inference_steps (50-100)
- Adjust guidance_scale (7-15)
- Make prompts more detailed and specific

## 🚀 Future Improvements

- [ ] Add web-based UI interface
- [ ] Support for image-to-image generation
- [ ] Batch processing multiple prompts
- [ ] Fine-tuning on custom datasets
- [ ] Integration with other diffusion models
- [ ] Real-time generation preview
- [ ] Style transfer capabilities

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Contact

**Rohith Reddy**

- GitHub: [@rohithreddy5250](https://github.com/rohithreddy5250)
- LinkedIn: [rohithreddyy](https://linkedin.com/in/rohithreddyy)
- Email: rohithreddybaddam8@gmail.com

## 🙏 Acknowledgments

- [Stability AI](https://stability.ai/) for Stable Diffusion
- [Hugging Face](https://huggingface.co/) for the Diffusers library
- [PyTorch](https://pytorch.org/) team for the framework

---

⭐ If you found this project helpful, please give it a star!

**Made with ❤️ by Rohith Reddy**
