<p align="center">
  <a href="README.md"><b>English</b></a>
  &nbsp;·&nbsp;
  <a href="README.fr.md">Français</a>
  &nbsp;·&nbsp;
  <a href="README.es.md">Español</a>
</p>

# PyTorch Tensor Fundamentals

> Hands-on introduction to PyTorch tensors, automatic differentiation, and GPU computing — foundations of modern deep learning.

**University:** Université d'Avignon — Master 1 Approaches Neuronales  
**Environment:** Python 3.10 · PyTorch · CUDA · Jupyter Notebook

---

## Overview

This project covers the complete set of tensor operations required before building any neural network in PyTorch. From basic construction to GPU transfers and autograd, every exercise is designed to build an intuitive understanding of how PyTorch works under the hood.

---

## Topics Covered

| Exercise | Concept | Key Operations |
|----------|---------|---------------|
| 1 | Tensor creation | `torch.tensor`, `ones`, `zeros`, `rand` |
| 2 | Shape manipulation | `reshape`, `t()`, `transpose` |
| 3 | Indexing & masking | Slicing, boolean masks |
| 4 | Arithmetic & broadcasting | `+`, `*`, `/`, broadcasting rules |
| 5 | Concatenation & stacking | `torch.cat`, `torch.stack`, `torch.chunk` |
| 6 | Data types & devices | `.float()`, `.double()`, `.to('cuda')` |
| 7 | Autograd | `requires_grad`, `.backward()`, `.grad` |
| 8 | Advanced operations | `norm`, `flatten`, `permute` |

---

## Key Concepts

### Broadcasting
Two tensors of shapes `(3,1)` and `(1,4)` are automatically expanded to `(3,4)` for element-wise operations — no data is copied, PyTorch handles the virtual expansion.

### Autograd
PyTorch's automatic differentiation engine tracks every operation on a tensor when `requires_grad=True`. Calling `.backward()` on a scalar propagates gradients back through the computation graph.

```python
x = torch.rand(2, 2, requires_grad=True)
y = (x**2 + 2*x + 1).sum()
y.backward()
print(x.grad)  # dy/dx = 2x + 2
```

### `t()` vs `transpose()`

| Function | Dimensions | Use case |
|----------|-----------|---------|
| `t()` | 2D only | Quick matrix transposition |
| `transpose(d0, d1)` | ≥ 2D | Permute any two axes |

### `cat` vs `stack`

- **`torch.cat`** — joins along an *existing* axis (keeps dimensionality)
- **`torch.stack`** — creates a *new* axis (increases rank by 1)

### GPU Transfer
```python
x = x.to('cuda')   # moves tensor to GPU
x = x.to('cpu')    # moves tensor back to CPU
torch.cuda.is_available()  # True
```

---

## Project Structure

```
TP1/
└── tp1.ipynb    # 8 exercises with solutions and explanations
```

---

## Setup

```bash
python -m venv env
source env/bin/activate
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
pip install jupyter
jupyter notebook tp1.ipynb
```

---

## Results / Observations

| Operation | Observation |
|-----------|-------------|
| CUDA availability | ✅ GPU detected (`cuda:0`) |
| `requires_grad` + `backward()` | Gradients computed analytically match manual formula |
| Norm (manual vs `torch.norm`) | Identical results — validates implementation |
| `permute` vs `transpose` | Identical output on 3D swap of dims 0 and 1 |

---

## Learning Outcomes

After completing these exercises you can:
- Create, reshape and index tensors of any shape
- Understand how broadcasting eliminates explicit loops
- Use autograd to compute gradients without manual calculus
- Transfer data between CPU and GPU efficiently
- Know when to use `cat` vs `stack`, `t()` vs `transpose()`

---

*Master 1 — Approches Neuronales — Université d'Avignon*
