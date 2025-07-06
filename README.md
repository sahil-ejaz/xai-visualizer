
# ExplainableAI - Neural Network Visualization Tool
**Date:** 2025-07-06

A visualisation tool that aims to make neural networks more transparent and provides insights into activations, edge weights and decision paths when data flows through. 
Most ML models are considered black-box models, which is problematic for high-stakes decisions. An Understanding why a model made a certain prediction (e.g medical diagnosis), verifying and debugging ML models is needed. 
Problem: Hard to verify correctness of explanations and it was shown that most XAl methods are not reliable

Project Includes 
- Project Journal
- GitHub Repository (under development branch!)
- Demo (poster session)

### Advanced Features to be implemented

- Overlay ground truth on the input layer for comparison.
- Highlight the strongest path from input to output on hover.
- Enable viewing of individual samples inside the histograms.
- Support for various aggregation and visualization strategies for individual samples.


---

## Our First Steps

1. **Dataset Familiarization**:
- **Datasets**: 
- Explore datasets such as:
	- **GitHub**[XAI-Tris Dataset](https://github.com/braindatalab/xai-tris)
	- **Paper**: [arXiv:2306.12816](https://arxiv.org/abs/2306.12816)
	- **Download Link**: [Google Drive](https://drive.google.com/file/d/1eg27Rfx9nG4Wmxsi_fgLzUqtXtMCAuLN/view?usp=sharing)
 - Explore the dataset and train a classification model using PyTorch.
     - tetromino is a geometric shape composed of four squares/block (each being 8 x 8-pixels), connected orthogonally.
     - only 'T' or 'L' tetromino shapes in dataset
     - linear case uses additive generation model
     - multiplicative case uses multiplicative generation model

2. **Tool Architecture Planning**:
   - Determine frontend and backend architecture.
   - Decide on libraries to use.
   - Establish a data format for layer, node, and edge information.
   - Research for others tools in this field (only found: https://playground.tensorflow.org, which still does not do what we want)


## Overview Image

<img width="941" alt="Bildschirmfoto 2024-11-10 um 22 59 53" src="https://github.com/user-attachments/assets/187e3a61-b7d0-4ebe-b1b5-15e94ddf48cc">

*Example Info for Dataset xai-tris-ds/linear_1d1p_0.18_uncorrelated.pt:*
| Key/Dataset | Value/Shape |
|-------------|-------------|
| Keys in the .pt file | dict_keys(['key', 'x_train', 'y_train', 'x_val', 'y_val', 'x_test', 'y_test', 'masks_train', 'masks_val', 'masks_test']) |
| Shape of the Training Dataset | torch.Size([8000, 64]) |
| Shape of the Test Dataset | torch.Size([1000, 64]) |
| Number of Images in the Training Dataset | 8000 |
| Number of Images in the Test Dataset | 1000 |

# xai-visualizer
A lightweight tool to visualize neural network activations and internal connections for interpretability research.

