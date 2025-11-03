## 📘 Overview

This repository presents a **Neural ODE–PDE hybrid framework** for simulating and learning **traffic flow dynamics** from data. 
By combining the expressive power of **neural ordinary differential equations (Neural ODEs)** and the spatiotemporal structure of **partial differential equations (PDEs)**, this model captures both **local vehicle interactions** and **global flow evolution** in complex traffic systems.

---

## Key Features

* **Neural ODE component:** Learns continuous-time evolution of traffic density and velocity. 
* **PDE-based prior:** Embeds physical traffic laws (e.g., LWR model) into the learning process. 
* **Data-driven calibration:** Fits real or simulated traffic datasets using neural parameterization. 
* **Hybrid modeling:** Integrates numerical solvers with deep learning modules for efficient training. 
* **Extensible architecture:** Easy to adapt for other spatiotemporal systems (e.g., epidemic spreading, fluid dynamics).

---

## ⚙️ Methodology

The framework approximates the PDE system governing traffic flow:

$$
\frac{\partial \rho}{\partial t} + \frac{\partial f(\rho)}{\partial x} = 0
$$

where $\rho(x,t)$ is the traffic density and $f(\rho)$ the flow function.

A **Neural ODE** is employed to learn the evolution of parameters or residual dynamics:

$$
\frac{d z(t)}{dt} = f_\theta(z(t), t)
$$

These components are integrated via numerical solvers (e.g., Runge-Kutta or adjoint methods) to form an **end-to-end trainable neural PDE system**.

---

## 🧩 Repository Structure

```

NeuralTrafficFlow/
├── data/              \# Datasets (real or synthetic)
├── models/            \# Neural ODE and PDE modules
├── solvers/           \# Numerical solvers and integrators
├── experiments/       \# Training and evaluation scripts
├── results/           \# Output visualizations and checkpoints
├── requirements.txt   \# Dependencies
└── main.py            \# Entry point for training/testing

````

---

## Installation

```bash
git clone [https://github.com/neyaz-ahmed/NeuralTrafficFlow.git](https://github.com/neyaz-ahmed/NeuralTrafficFlow.git)
cd NeuralTrafficFlow
pip install -r requirements.txt
````

### Dependencies

  * Python ≥ 3.9
  * PyTorch ≥ 2.0
  * NumPy, SciPy, Matplotlib
  * Torchdiffeq (for Neural ODEs)

-----

## 🤝 Contributing

Contributions, issues, and feature requests are welcome\!
Feel free to open a pull request or start a discussion.

-----

## 📄 License

This project is licensed under the **MIT License** – see the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.

-----

## 🌐 Acknowledgments

  * [torchdiffeq](https://github.com/rtqichen/torchdiffeq) for Neural ODE implementation.
  * Researchers in traffic flow modeling and hybrid physics–ML systems.
  * Inspiration from PDE-based modeling of complex dynamical systems.

-----

> *"Bridging physics and learning for intelligent traffic modeling."*

## References

1. [UCI Machine Learning Repository – Traffic Flow Forecasting Dataset](https://archive.ics.uci.edu/dataset/608/traffic%2Bflow%2Bforecasting)  
2. [arXiv:2101.04359](https://arxiv.org/abs/2101.04359)  
3. [arXiv:2010.08895](https://arxiv.org/abs/2010.08895)  
4. [arXiv:1711.10561](https://arxiv.org/abs/1711.10561)  
5. [arXiv:1806.07366](https://arxiv.org/abs/1806.07366)


