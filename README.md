# Image Captioning

## Project Overview
Automatically generating descriptive captions for images is a challenging task with applications in accessibility, image retrieval, and content generation.  
This project builds a deep learning model using the **Flickr8k** dataset to generate accurate captions by combining **Convolutional Neural Networks (CNNs)** for image feature extraction and **Recurrent Neural Networks (RNNs)** for language generation.

---

## Problem Statement
Generating meaningful image captions requires addressing several challenges:

- **Handling Diversity:** Capturing a wide range of image types, scenes, and objects  
- **Model Complexity:** Balancing performance and computational efficiency  
- **Limited Dataset Size:** Working with the relatively small Flickr8k dataset  
- **Evaluation Metrics:** Choosing appropriate metrics for caption quality  
- **Cross-Modal Learning:** Effectively aligning visual and textual data  

---

## Model Architecture
The model consists of two main components:

- **Encoder (ResNet-50):** Extracts high-level visual features from images  
- **Decoder (LSTM):** Generates sequential captions based on extracted features  

Both components are integrated into a single model for end-to-end training and caption generation.

---

## Dataset
**Flickr8k** dataset:  
- **8,000 images** with **40,000 human-written captions**  
- Split into:
  - Training: 6,000 images  
  - Validation: 1,000 images  
  - Test: 1,000 images  

---

## Training
The model was trained using a CNN-LSTM architecture with the following hyperparameters:

- **Embedding Dimension:** 300  
- **Hidden Dimension:** 500  
- **LSTM Layers:** 2  
- **Batch Size:** 128  
- **Learning Rate:** 1.25  
- **Optimizer:** SGD  

---

## Results
The model was evaluated using **BLEU scores**:

| Metric  | Score   |
|---------|---------|
| BLEU-1  | 0.6108  |
| BLEU-2  | 0.3907  |
| BLEU-3  | 0.2519  |
| BLEU-4  | 0.1636  |

The model performs well for unigram predictions (**BLEU-1**) but shows room for improvement in generating longer, coherent captions (**BLEU-4**).

---

## Conclusion
The current model generates relevant words but can be further improved by:
- Enhancing LSTM layers for better sequence modeling  
- Fine-tuning the ResNet encoder for domain-specific features  
- Exploring attention mechanisms for more context-aware captioning  

---

## References
- [Flickr8k Dataset](https://forms.illinois.edu/sec/1713398)  
- Vinyals et al., *"Show and Tell: A Neural Image Caption Generator"*, CVPR 2015  
