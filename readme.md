# Lamini Fine-Tuning Example Project

**Created by: Harsh Gidwani**

## Overview

This project demonstrates how to fine-tune a large language model (LLM) using the Lamini platform. The example shows how to customize Meta's Llama-3-8B-Instruct model using a curated dataset of questions and answers about Lamini's features and capabilities.

## What is Lamini?

Lamini is a program for the execution of LLMs called a large language model engine. It is not a robot, but rather a tool for building and executing LLMs. It provides a cloud-based platform for fine-tuning and deploying large language models with ease.

## Project Structure

```
2-finetuning/
├── finetune.py      # Main fine-tuning script
└── README.md        # This file
```

## Features

- **Custom Dataset**: 10 carefully crafted Q&A pairs about Lamini
- **Model Selection**: Uses Meta-Llama-3-8B-Instruct as base model
- **Hyperparameter Tuning**: Configurable learning rate and other parameters
- **Easy Integration**: Simple Python API for fine-tuning

## Prerequisites

- Python 3.7 or higher
- Lamini Python SDK
- Valid Lamini API key

## Installation

1. Install the Lamini SDK:
```bash
pip install lamini
```

2. Set up your Lamini API key in the script or as an environment variable

## Usage

1. Run the fine-tuning script:
```bash
python finetune.py
```

2. The script will:
   - Load the training data (10 Q&A pairs)
   - Initialize the Lamini model with Meta-Llama-3-8B-Instruct
   - Start the fine-tuning process with specified hyperparameters

## Training Data

The dataset includes questions about:
- Step-by-step tutorials and documentation
- Lamini type system and Python SDK
- API limits and free token allocation
- Job cancellation functionality
- Hyperparameter tuning capabilities
- Licensing (Apache 2.0) and commercial use
- Hardware requirements and accessibility
- Online/offline usage options
- Supported tasks (translation, Q&A, text generation)
- What Lamini is and how it works

## Hyperparameters

The following hyperparameters can be configured in the `finetune_args`:

- `learning_rate` (float): Learning rate for training (default: 1.0e-4)
- `early_stopping` (bool): Whether to use early stopping
- `max_steps` (int): Maximum number of training steps
- `optim` (str): Optimizer type (adam, sgd, etc.)

## Example Code Structure

```python
# Get training data
data = get_data()

# Initialize Lamini model
llm = Lamini(model_name="meta-llama/Meta-Llama-3-8B-Instruct")

# Start fine-tuning
llm.tune(data_or_dataset_id=data,
         finetune_args={'learning_rate': 1.0e-4})
```

## Key Benefits

- **Automated Hyperparameter Tuning**: Lamini uses intelligent algorithms including grid search, random search, Bayesian optimization, and genetic algorithms
- **Resource Efficiency**: Optimized computational resource utilization
- **Overfitting Prevention**: Built-in cross-validation techniques
- **Data Ownership**: You retain full ownership of your data and models

## Deployment Options

- **Cloud-based**: Use Lamini's hosted GPU-accelerated servers
- **On-premise**: Enterprise deployments on your own infrastructure
- **Hybrid**: Combination of cloud and local deployment

## License

This project follows Lamini's Apache 2.0 license for commercial use. You retain ownership of your data and models. Lamini doesn't use your data to tune models for anyone else.

## Support

For questions about deployment, enterprise solutions, or offline usage, reach out to the Lamini team directly.

---

**Project Author: Harsh