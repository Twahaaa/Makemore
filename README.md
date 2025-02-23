# Makemore MLP Model

This repository contains an implementation of a simple Multi-Layer Perceptron (MLP) model inspired by Andrej Karpathy's "makemore" series. The model is designed to generate text by predicting the next character/word in a sequence based on previous inputs.

## Model Overview

The `MLP` class is built using PyTorch and consists of:
- **Token Embedding Layer (`nn.Embedding`)**: Converts token indices into dense vector representations.
- **Multi-Layer Perceptron (`nn.Sequential`)**:
  - Fully connected layers (`nn.Linear`)
  - `Tanh` activation function
  - Final output layer predicting the next token

## How It Works

1. The input sequence of tokens is embedded into dense vectors.
2. The model shifts input tokens and replaces the first token with a special `<BLANK>` token.
3. The embeddings of previous words are concatenated and passed through an MLP.
4. The model outputs **logits** (predictions) for the next token.
5. During training, the model computes cross-entropy loss if target labels are provided.

## References
- [Andrej Karpathy's makemore series](https://www.youtube.com/@AndrejKarpathy)

## License
This project is open-source and available under the MIT License.

