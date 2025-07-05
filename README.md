# Mitigating LLM Social Bias by Assessing and Filtering Reasoning Steps with a Multi-Judge Pipeline

## Authors

- Fatemehzahra Ghafari Ghomi (<fatemezahra.ghafari@studio.unibo.it>)
- Shafagh Rastegari (<shafagh.rastegari@studio.unibo.it>)
- Habib Kazemi (<habib.kazemi2@studio.unibo.it>)

# Description

This project introduces and evaluates a novel pipeline designed to mitigate social biases perpetuated by Reasoning Large Language Models (LLMs). Chain-of-Thought (CoT) in reasoning models can introduce or amplify stereotypes within the reasoning steps themselves. Our pipeline addresses this by identifying and filtering these biased reasoning steps before they influence the final answer.

Our approach utilizes a multi-judge system, empolying LLMs to assess each step of a CoT sequence for social bias. Biased steps are then removed, creating a “debiased” CoT that is passed to a final model for answer generation.

We conducted extensive experiments on two datasets:

- **Bias Benchmark for Question Answering (BBQ)**

- **Multilingual Bias Benchmark for Question Answering (MBBQ)**

## Project Structure

The repository is organized into two main directories:

- `BBQ/`: Contains the code, dataset and results of running experiments on the English BBQ dataset.
- `MBBQ/`: Contains the code, dataset and results of our multilingual extension of the BBQ benchmark, covering English, Spanish, Dutch, and Turkish.

## Setup and Installation

### Prerequisites

- Python 3.12 or higher
- uv (Python package manager)

### Installation

1. **Install uv** (if not already installed)

   ```bash
   # macOS/Linux with curl
   curl -LsSf https://astral.sh/uv/install.sh | sh

   # Windows with PowerShell
   powershell -c "irm https://astral.sh/uv/install.ps1 | iex"

   ```

2. **Set up the project**

   ```bash
   # Clone the repository
   git clone <repository-url>
   cd path/to/project
   
   # Create virtual environment and install dependencies using uv
   uv sync

   # Activate a virtual environment using uv
   source .venv/bin/activate
   ```

## Running the projects

The main project notebooks are interactive [Marimo](https://marimo.io/) notebooks. They provide a reactive and reproducible environment for running the experiments.

To run notebooks of BBQ, First enter the BBQ directory:

```bash
cd BBQ
```

To run notebooks of MBBQ, First enter the MBBQ directory:

```bash
cd MBBQ
```

Then use the following command:

```bash
marimo edit <notebook-name>.py
```
