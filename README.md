# Task 04: Image-to-Image Translation (Pix2Pix)

This project implements a **Conditional Generative Adversarial Network (cGAN)** for paired image-to-image translation. 

## 🖼️ Examples
* **Edges → Photo:** Turn line drawings into realistic objects.
* **Map → Satellite:** Convert Google Maps styling into satellite imagery.
* **Day → Night:** Change the lighting of architectural photos.

## 🧠 The Architecture
1. **Generator (U-Net):** An encoder-decoder with skip connections to prevent "bottlenecking" of spatial information.
2. **Discriminator (PatchGAN):** Instead of looking at the whole image, it classifies $70 \times 70$ patches as real or fake, which forces the model to focus on high-frequency crisp details.

## 📉 Loss Function
We optimize the model using a weighted objective:
$$L = \arg \min_G \max_D \mathcal{L}_{cGAN}(G, D) + \lambda \mathcal{L}_{L1}(G)$$
Where $L1$ loss encourages the output to be structurally similar to the ground truth.

---
# Author
- Name: Pruonh Kimliya
- Email: kimliyapruonh@gmail.com
