# Transformer Implementation from Scratch

This repository contains an implementation of the Transformer model from scratch, inspired by the "Attention is All You Need" paper. The implementation is designed to be clear and understandable, with detailed comments and explanations, making it a great resource for learning and experimentation.

## Features

- **Self-Attention Layer**: Implements multi-head self-attention to compute attention scores between different positions in the input sequence.
- **Transformer Block**: Combines self-attention with feed-forward layers, incorporating residual connections and layer normalization.
- **Encoder-Decoder Architecture**: Implements the standard Transformer encoder-decoder architecture, with support for masked self-attention during training.
- **Positional Encoding**: Adds positional information to the embeddings to handle sequential data.
- **Flexible Configuration**: Allows for customization of embedding size, number of layers, number of heads, and other hyperparameters.

## Requirements

- **PyTorch**: This implementation uses PyTorch for tensor operations and model training.
  
To install PyTorch, follow the official installation guide: [PyTorch Installation](https://pytorch.org/get-started/locally/)

## Installation

Clone the repository to your local machine:

```bash
git clone https://github.com/yourusername/transformer-from-scratch.git
cd transformer-from-scratch
```

## Install the necessary dependencies

```bash
pip install torch
```
# Model Architecture

## Self-Attention Layer
The self-attention mechanism allows the model to weigh the importance of each word in the input sequence with respect to other words.  
Multi-head attention splits the attention mechanism into multiple parallel attention heads.

## Transformer Block
Each Transformer block consists of a self-attention layer followed by a feed-forward neural network, both with residual connections and layer normalization.

## Encoder and Decoder
- The **encoder** processes the input sequence and produces a sequence of encoded representations.
- The **decoder** generates the output sequence using the encoded representation from the encoder and the target sequence.

## Masking
Padding and causal masking are applied to ensure that the model does not attend to padded tokens or future tokens during training.

## Hyperparameters
- **src_vocab_size**: Size of the source vocabulary
- **trg_vocab_size**: Size of the target vocabulary
- **src_pad_idx**: Padding index for source sequences
- **trg_pad_idx**: Padding index for target sequences
- **embed_size**: The dimensionality of the word embeddings
- **num_layers**: Number of layers in both the encoder and decoder
- **heads**: Number of attention heads
- **dropout**: Dropout rate applied to layers
- **max_length**: Maximum length of inp

