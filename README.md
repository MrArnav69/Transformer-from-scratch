# Transformer Model Implementation from Scratch

This repository contains a Jupyter notebook that provides a step-by-step guide to building a Transformer model from the ground up using PyTorch. The project focuses on a next-token prediction task, where the model learns to predict the subsequent digit in a cyclic sequence.

This implementation serves as an educational tool to understand the fundamental components of the Transformer architecture. By building each part from scratch, from positional encoding to the final encoder stack, one can gain a deeper insight into the inner workings of these powerful models.

## Model Architecture

The model implemented in this project is a standard Transformer encoder, as depicted in the diagram below.

<p align="center">
  <img src="https://d1.awsstatic.com/GENAI-1.151ded5440b4c997bac0642ec669a00acff2cca1.png" width="300">
</p>

The implemented Transformer model consists of the following key components:

- **Positional Encoding**: Sinusoidal positional encodings are used to inject information about the order of tokens in the input sequence.

- **Multi-Head Self-Attention**: The core of the Transformer, this mechanism allows the model to weigh the importance of different tokens in the sequence when encoding a particular token.

- **Position-wise Feed-Forward Networks**: A fully connected feed-forward network applied to each position separately and identically.

- **Transformer Block**: A single block that encapsulates a multi-head self-attention layer and a position-wise feed-forward network, with residual connections and layer normalization.

- **Transformer Encoder**: The full encoder, constructed by stacking multiple Transformer blocks.

## Dataset

The model is trained on a synthetically generated dataset. The task is to predict the next digit in a cyclic sequence (e.g., 0 -> 1, 1 -> 2, ..., 9 -> 0).

The vocabulary consists of digits from 0 to 9. The input data is one-hot encoded.

## Getting Started

### Prerequisites

Ensure you have Python 3 and Jupyter Notebook installed. The required Python libraries are listed in the `requirements.txt` file.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Transformer-from-scratch.git
   cd Transformer-from-scratch
   ```

2. It is recommended to create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

To run the project, start the Jupyter Notebook server:

```bash
jupyter notebook
```

Then, open the `main.ipynb` notebook and execute the cells sequentially.

## Contributing

Contributions are welcome. Please open an issue to discuss any changes or submit a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
