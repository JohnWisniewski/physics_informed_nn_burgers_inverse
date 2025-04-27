# physics_informed_nn_burgers_inverse
PINN for Inverse Burgers' Equation Solves an inverse problem using a Physics-Informed Neural Network (PINN) to infer unknown parameters from sparse data while enforcing PDE constraints. Combines data fitting and physics residual loss for accurate estimation.


# Physics-Informed Neural Network (PINN) for Inverse Burgers' Equation

---

## Overview

This project uses a Physics-Informed Neural Network (PINN) to solve an **inverse problem** for the 1D Burgers' equation.  
The goal is to **infer the unknown viscosity parameter (\nu\)** based on limited observation data while enforcing the PDE through physics-based loss.

This work is an extension of starter code provided in [CISC489] at [University of Delaware] (Spring 2025), with major modifications including extended training, loss tracking, and visualization of results.

---

## Files

| File | Description |
|:-----|:------------|
| `physics_informed_nn_burgers_inverse.ipynb` | Full PINN model training, inverse parameter learning, and results. |


---

## Methods

- **Model**: Fully-connected neural network (MLP) with several hidden layers and activation functions (tanh).
- **Loss**: Combined **data loss** (supervised) + **physics residual loss** (unsupervised).
- **Optimization**: First trained with **Adam optimizer**, then polished using **L-BFGS** optimizer.
- **Physics Loss**: PDE residual computed via automatic differentiation using PyTorch.
- **Inverse Learning**: Viscosity coefficient \(\nu\) treated as a learnable parameter.

---

## Results

[Adam] Epoch 0, Loss: 2.1605e+00, inferred nu: 0.0999, true nu: 0.10
[Adam] Epoch 100, Loss: 2.2153e-01, inferred nu: 0.1101, true nu: 0.11
[Adam] Epoch 200, Loss: 9.5368e-02, inferred nu: 0.1155, true nu: 0.12
[Adam] Epoch 300, Loss: 7.7360e-02, inferred nu: 0.1185, true nu: 0.12
[Adam] Epoch 400, Loss: 6.3998e-02, inferred nu: 0.1338, true nu: 0.13
[Adam] Epoch 500, Loss: 5.4146e-02, inferred nu: 0.1492, true nu: 0.15
[Adam] Epoch 600, Loss: 4.6986e-02, inferred nu: 0.1603, true nu: 0.16
[Adam] Epoch 700, Loss: 4.2139e-02, inferred nu: 0.1658, true nu: 0.17
[Adam] Epoch 800, Loss: 3.9109e-02, inferred nu: 0.1671, true nu: 0.17
[Adam] Epoch 900, Loss: 3.7413e-02, inferred nu: 0.1667, true nu: 0.17
[Adam] Epoch 1000, Loss: 3.6532e-02, inferred nu: 0.1659, true nu: 0.17
[Adam] Epoch 1100, Loss: 3.6019e-02, inferred nu: 0.1654, true nu: 0.17
[Adam] Epoch 1200, Loss: 3.5655e-02, inferred nu: 0.1652, true nu: 0.17
[Adam] Epoch 1300, Loss: 3.5346e-02, inferred nu: 0.1651, true nu: 0.17
[Adam] Epoch 1400, Loss: 3.5054e-02, inferred nu: 0.1650, true nu: 0.17
[Adam] Epoch 1500, Loss: 3.4761e-02, inferred nu: 0.1650, true nu: 0.17
[Adam] Epoch 1600, Loss: 3.4448e-02, inferred nu: 0.1650, true nu: 0.16
[Adam] Epoch 1700, Loss: 3.4078e-02, inferred nu: 0.1649, true nu: 0.16
[Adam] Epoch 1800, Loss: 3.3656e-02, inferred nu: 0.1649, true nu: 0.16
[Adam] Epoch 1900, Loss: 3.3303e-02, inferred nu: 0.1648, true nu: 0.16
[Adam] Epoch 2000, Loss: 3.3031e-02, inferred nu: 0.1647, true nu: 0.16
[Adam] Epoch 2100, Loss: 3.2793e-02, inferred nu: 0.1646, true nu: 0.16
[Adam] Epoch 2200, Loss: 3.2572e-02, inferred nu: 0.1646, true nu: 0.16
[Adam] Epoch 2300, Loss: 3.2367e-02, inferred nu: 0.1647, true nu: 0.16
[Adam] Epoch 2400, Loss: 3.2176e-02, inferred nu: 0.1647, true nu: 0.16
[Adam] Epoch 2500, Loss: 3.1998e-02, inferred nu: 0.1647, true nu: 0.16
[Adam] Epoch 2600, Loss: 3.1830e-02, inferred nu: 0.1647, true nu: 0.16
[Adam] Epoch 2700, Loss: 3.1671e-02, inferred nu: 0.1648, true nu: 0.16
[Adam] Epoch 2800, Loss: 3.1713e-02, inferred nu: 0.1648, true nu: 0.16
[Adam] Epoch 2900, Loss: 3.1395e-02, inferred nu: 0.1648, true nu: 0.16
[Adam] Epoch 3000, Loss: 3.1289e-02, inferred nu: 0.1648, true nu: 0.16
[Adam] Epoch 3100, Loss: 3.1193e-02, inferred nu: 0.1648, true nu: 0.16
[Adam] Epoch 3200, Loss: 3.1116e-02, inferred nu: 0.1648, true nu: 0.16
[Adam] Epoch 3300, Loss: 3.1046e-02, inferred nu: 0.1648, true nu: 0.16
[Adam] Epoch 3400, Loss: 3.0998e-02, inferred nu: 0.1648, true nu: 0.16
[Adam] Epoch 3500, Loss: 3.0935e-02, inferred nu: 0.1649, true nu: 0.16
[Adam] Epoch 3600, Loss: 3.1081e-02, inferred nu: 0.1649, true nu: 0.16
[Adam] Epoch 3700, Loss: 3.0848e-02, inferred nu: 0.1650, true nu: 0.16
[Adam] Epoch 3800, Loss: 3.0811e-02, inferred nu: 0.1650, true nu: 0.16
[Adam] Epoch 3900, Loss: 3.0782e-02, inferred nu: 0.1650, true nu: 0.16
[Adam] Epoch 4000, Loss: 3.0748e-02, inferred nu: 0.1651, true nu: 0.17
[Adam] Epoch 4100, Loss: 3.0719e-02, inferred nu: 0.1651, true nu: 0.17
[Adam] Epoch 4200, Loss: 3.0698e-02, inferred nu: 0.1651, true nu: 0.17
[Adam] Epoch 4300, Loss: 3.0670e-02, inferred nu: 0.1651, true nu: 0.17
[Adam] Epoch 4400, Loss: 3.0646e-02, inferred nu: 0.1652, true nu: 0.17
[Adam] Epoch 4500, Loss: 3.0654e-02, inferred nu: 0.1652, true nu: 0.17
[Adam] Epoch 4600, Loss: 3.0605e-02, inferred nu: 0.1652, true nu: 0.17
[Adam] Epoch 4700, Loss: 3.0584e-02, inferred nu: 0.1653, true nu: 0.17
[Adam] Epoch 4800, Loss: 3.0636e-02, inferred nu: 0.1653, true nu: 0.17
[Adam] Epoch 4900, Loss: 3.0547e-02, inferred nu: 0.1653, true nu: 0.17
[L-BFGS] Final Loss: 3.0528e-02, inferred nu: 0.1672, true nu: 0.17

### Inferred Parameter

| Metric | Value |
|:-------|:------|
| True viscosity \(\nu\) | 0.17 |
| Inferred viscosity \(\nu\) | 0.167 |
| Final Loss | \( \3.05 × 10⁻²\) |

✅ The PINN successfully inferred \(\nu\) very close to the true value.

---

### Loss Convergence

Training loss steadily decreased during 5000 epochs of Adam optimization, and further reduced by L-BFGS optimization.  
The final loss stabilized around \3.05 × 10⁻²\), indicating good model convergence.

---

### Prediction vs True Solution

| Plot | Description |
|:-----|:------------|
| **True \( u(x,t) \)** | Shows sharp gradients and parabolic behavior expected from the analytical Burgers' solution. |
| **Predicted \( u(x,t) \)** | Captures general trends, including low-to-high transitions, but slightly underestimates sharp curvatures. |

### Reason for Mismatch
- **Model expressivity**: Neural network capacity (size, depth) may be limited.
- **Training time**: More epochs or points could reduce errors further.
- **Physics enforcement**: Small errors in PDE residuals propagate into solution.
- **Inverse instability**: Small errors in learned \(\nu\) cause solution deviations.

✅ Despite these limitations, the PINN was able to **capture the global behavior** accurately and **infer physical parameters** effectively.

---

## How to Run

1. Install required packages:

```bash
pip install torch numpy matplotlib
