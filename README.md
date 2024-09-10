# Adversarial Attacks on ResNet18 Trained on RIVAL10 Dataset

## Overview

This project demonstrates how to attack a ResNet18 model trained on the RIVAL10 dataset using various adversarial attack methods. The attacks implemented include:

- **PGD (Projected Gradient Descent)**
- **AutoAttack**
- **FGSM (Fast Gradient Sign Method)**
- **C&W (Carlini & Wagner Attack)**

The performance of the attacks is evaluated in terms of **ASR (Attack Success Rate)**, which measures the effectiveness of each attack in fooling the ResNet18 model. 

The RIVAL10 dataset used in this project is referenced from: [*A Comprehensive Study of Image Classification Model Sensitivity to Foregrounds, Backgrounds, and Visual Attributes*](https://arxiv.org/abs/2201.10766)
 
## Adversarial Attack Methods

1. **Projected Gradient Descent (PGD):** An iterative attack method that refines adversarial perturbations by taking multiple small steps towards increasing the loss function.
   
2. **AutoAttack:** A strong ensemble of diverse attacks that ensures the evaluation is more reliable.

3. **Fast Gradient Sign Method (FGSM):** A simple, fast attack that modifies the input by moving in the direction of the gradient of the loss with respect to the input.

4. **Carlini & Wagner (C&W):** A more complex optimization-based attack designed to generate adversarial examples with minimal perturbation while effectively deceiving the model.

## Results: ASR (Attack Success Rate) Comparison

The following table shows the ASR for each attack method when applied to the ResNet18 model trained on the RIVAL10 dataset.

| **Attack Method** | **ASR (%)** |
|-------------------|-------------|
| PGD               |    98.0     |
| AutoAttack        |    92.2     |
| FGSM              |    75.8     |
| C&W               |    74.0     |

> **Note**: The model's accuracy on clean images was 97.6%. The attacks were tested on 500 samples from the RIVAL10 dataset.

## Instructions to Run the Notebook

Install the required dependencies using the following command:

   ```bash
   pip install torch torchvision torchattacks autoattack 
