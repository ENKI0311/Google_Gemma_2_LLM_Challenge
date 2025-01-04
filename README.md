# GEMMA 2 Challenge: Advanced Text Generation with Large Language Models

Welcome to the **GEMMA 2 Challenge Repository**, where we leverage the power of large language models to explore and generate creative, diverse text based on unique prompts. This project uses a variety of themes—including detective noir, fantasy, and historical texts—to test and expand the capabilities of generative AI, specifically tailored for Google’s GEMMA 2 benchmark.

## Overview

This repository hosts our experimentation with text generation using **Transformer-based language models**. It provides scripts, notebooks, and resources that explore the depth of these models in creative storytelling, complex prompt engineering, and response customization.

### Key Features

- **Prompt Engineering**: Diverse prompts tailored to evoke unique responses from the model, including detective noir, medieval fantasy, and inspirational themes.
- **Bible Text Integration**: Includes content from the *King James Version of the Bible*, allowing for historically rich and profound text generation capabilities.
- **Visuals and Notebook**: Each theme is complemented by visual aids and organized Jupyter notebooks, creating a cohesive and interactive environment for exploring the generated text.

## Installation

### Prerequisites
- Python 3.7+
- [Transformers library](https://huggingface.co/transformers)
- (Optional) GPU for faster processing

1. Clone the repository:
   ```bash
   git clone https://github.com/ENKIO0311/gemma2-challenge.git
   cd gemma2-challenge
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Download or link the desired model(s) from Hugging Face or your chosen source.

## Usage

### Running the Model

1. **Initialize the model and generator** in `text_generation.py`:
   ```python
   from transformers import pipeline

   # Load text-generation pipeline
   generator = pipeline('text-generation', model='your-model', tokenizer='your-tokenizer', device=0)
   ```

2. **Select a prompt** from the prompt library in `prompts.py`. Example:
   ```python
   # Example prompt from detective noir theme
   noir_prompt = "Narrate a suspenseful, noir-style story where a detective uncovers a hidden biblical mystery."
   ```

3. **Generate Text**:
   ```python
   output = generator(noir_prompt, max_length=1000, temperature=0.7, repetition_penalty=1.2, do_sample=True)
   print(output[0]['generated_text'])
   ```

### Customizing Prompts

To experiment with different styles, modify or add prompts in `prompts.py`. Sample prompts include:

- **Detective Noir**: Creates suspenseful narratives with dark, atmospheric tones.
- **Medieval Fantasy**: Generates settings with mythical creatures and quests.
- **Biblical Themes**: Uses phrases inspired by the *King James Bible* for historically resonant responses.

### Notebooks and Visuals

Each notebook is structured to align with specific prompt themes. Visual aids complement generated text, enhancing the interpretability and depth of the stories created by the model.

## Repository Structure

```plaintext
gemma2-challenge/
├── data/                   # Contains scraped Bible text and other source material
├── notebooks/              # Thematic Jupyter notebooks for prompt testing and visualization
├── scripts/                # Script files for text generation, model setup, and custom prompts
├── images/                 # Visuals associated with the notebook themes
├── README.md               # Project overview and instructions
└── requirements.txt        # Required packages for setting up the environment
```

## Contribution

We welcome contributions! Please feel free to:
1. Submit new prompts or modify existing ones for more unique outputs.
2. Create additional visual assets to complement generated themes.
3. Suggest improvements for the model setup and parameter adjustments.

## License

This project is licensed under the MIT License. See `LICENSE` for more details.

