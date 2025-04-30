# 🛰️ RL-Guided Planetary Navigation using Synthetic Terrain Generation

This repository contains the code and resources for a research project exploring reinforcement learning (RL)-based autonomous navigation across planetary surfaces. We enhance learning by augmenting terrain data using generative models such as WGANs, and Diffusion Models — all enforced with scientific constraints to improve generalization and realism.

![Sample Terrain Output](terrain_map.png)  
<p align="center"><i>Example of planetary terrain</i></p>

---

## Result

![RL Navigation Demo](results/agent_path3.gif)  
<p align="center"><i>RL agent navigating planetary terrain</i></p>

---

## Key Contributions

- **Reinforcement Learning Agent** using Deep Q-Network (QNet) trained on real and synthetic terrain.
- **Terrain Generation** using:
  - **WGAN** – Enhanced stability with gradient penalty.
  - **Diffusion Model** – Most realistic outputs, guided by an **Enforcer Network**.
- **Enforcer Network** – Applies soft scientific plausibility constraints during generator training.
- **Transfer Learning** – From synthetic terrains to real Moon and Mars orbiter datasets.

---

## Architectures

- **Q-Network**: 12D input → 256 ReLU neurons → 8 actions (directions)
- **GAN Generator**: 5-layer transposed CNN, BatchNorm, ReLU, Tanh
- **Diffusion Model**: U-Net with skip connections, attention, and Swish activations
- **All models trained with Adam optimizer**, learning rates:
  - QNet & Diffusion: 0.001
  - WGAN: 0.0001

---

##  Results Summary

Diffusion-generated terrains led to smoother convergence and more robust navigation policies, especially in complex or unseen terrains. GANs offered faster generation but sometimes lacked topographic diversity. RL agents trained with synthetic terrains significantly outperformed those trained on real data alone.

---

## Acknowledgements

Terrain generation code for GANs and diffusion models adapted from ![Aladdin Persson's ML Collection](https://github.com/aladdinpersson/Machine-Learning-Collection). We thank RVCE, the ETE Department, and Dr. Niranjana K M (Faculty Advisor, Dhruva – RVCE’s Astrophysics Club) and Dr. Karthik Shastry for their support. Special thanks to Dhruva and all co-authors who contributed to this research.

---

## Citation

If you use this code or work in your research, please consider citing our paper (to be updated post-publication).

---

## Contributors 

- ![Manohara](https://github.com/Manohara-Ai)
- ![vibha](https://github.com/paaduka32)
- ![Prarthana](https://github.com/kulkarniprar)
- Khushi
- Pratiksha 
- Krishna
