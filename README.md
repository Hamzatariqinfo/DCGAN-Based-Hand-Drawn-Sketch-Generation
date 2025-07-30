#  DCGAN-Based Hand-Drawn Sketch Generation using QuickDraw Dataset

This repository holds the code and insights of **Deep Convolutional Generative Adversarial Networks (DCGANs)** to generate hand-drawn sketches from Google's **QuickDraw dataset**. The project consists of three tasks with emphasis on data exploration, basic sketch generation, and complex sketch generation.

---

##  Project Structure

- **Task 1**: Data investigation and preprocessing  
- **Task 2**: DCGAN implementation for simple sketches (Smiley Faces)  
- **Task 3**: Implementation of DCGAN for complex sketches (Cats)  

---

##  Objectives

- Understand category-wise complexity through analysis of the QuickDraw dataset.  
- Train DCGANs to produce simple and complex sketch patterns.  
- Compare performance on the basis of sketch complexity using both qualitative and quantitative assessments.  

---

## Technologies Used

- Python 3.8+  
- TensorFlow 2.x  
- Google Colab  
- NumPy, Matplotlib, Pandas  

---

##  Dataset

- **Source**: [Quick, Draw! Dataset by Google Creative Lab](https://quickdraw.withgoogle.com/data)  
- **Categories Used**:
  - Smiley Face (Simple)  
  - Cat (Complex)  

---

##  Implementation Details

###  Generator Architecture

- Input: 100-dim noise vector  
- Layers: 4 transposed convolutions  
- Activations: ReLU + Tanh  
- Batch Normalization: Yes  

###  Discriminator Architecture

- Input: 28×28 grayscale sketch  
- Layers: 4 convolutional layers  
- Activations: LeakyReLU  
- Batch Normalization: Yes  

###  Training Configuration

- Optimizer: Adam (`lr=2e-4`, β1=0.5, β2=0.999)  
- Epochs: 5  
- Batch Size: 128  
- Loss Function: Binary Cross-Entropy  
- Label Smoothing: Enabled  

---

##  Results

| Task   | Sketch Type | Stability            | Visual Quality | Loss Convergence |
|--------|-------------|----------------------|----------------|------------------|
| Task 2 | Smiley Face | ✅ Stable            | ✅ High        | ✅ Smooth        |
| Task 3 | Cat         | ⚠️ Slightly Unstable | ⚠️ Variable   | ⚠️ Noisy          |

---

##  Key Findings

- Simple patterns (smiley faces) are learned faster and better.  
- Complicated sketches (cats) need deeper or special architectures.  
- Morphological complexity has an effect on training stability and output quality.  

---


##  Reproducibility Guidelines

- Utilize the same random seed and preprocessing steps.  
- Use the same learning rate, batch size, and architecture.  
- Monitor generator/discriminator loss for diagnosis.  

---

##  Future Directions

- Apply **Progressive Growing GANs** to achieve improved complex sketch quality.  
- Add **Attention mechanisms** or **Multi-Scale GANs**.  
- Expand dataset or use **data augmentation** for increased diversity.  

---

## References

1. Radford et al. (2016) - DCGANs  
2. Goodfellow et al. (2014) - GANs  
3. Google Creative Lab - QuickDraw Dataset  
4. Arjovsky et al. (2017) - Wasserstein GAN  

---


