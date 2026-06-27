\# Test-Time Entropy Minimization (TENT) Across Multiple Benchmarks

Graduate research project completed for \*\*CSE 710\*\* at the \*\*University at Buffalo\*\*.

\## Overview

Deep neural networks often experience significant performance degradation when evaluated on data that differs from their training distribution. This project investigates \*\*Test-Time Entropy Minimization (TENT)\*\*, a lightweight test-time adaptation (TTA) technique that improves model robustness by updating only Batch Normalization parameters during inference.

The project evaluates TENT under both \*\*single-corruption\*\* and \*\*sequential-corruption\*\* settings across several widely used robustness benchmarks.

\---


\## Features

\- Implementation of Test-Time Entropy Minimization (TENT)

\- Evaluation on multiple benchmark datasets

\- Comparison of baseline vs. adapted model performance

\- Sequential domain adaptation experiments

\- Entropy analysis during adaptation

\- Step-ablation study examining adaptation speed

\---


\## Datasets

\- CIFAR-10-C

\- CIFAR-100-C

\- ImageNet-C

\---


\## Models

\- ResNet-18 (fine-tuned for CIFAR-10 and CIFAR-100)

\- ResNet-50 (ImageNet)

Only Batch Normalization affine parameters are updated during test-time adaptation, following the original TENT methodology.

\---


\## Repository Structure

```
.

├── notebooks/

│   └── tent\_experiments.ipynb

├── models/

│   ├── resnet18\_cifar100.pth

├── docs/

│   ├── report.pdf

│   └── presentation\_1.pdf

│   └── presentation\_2.pdf

├── README.md

```

\---


\## Results

Key findings include:

\- TENT consistently improved robustness under distribution shift.

\- The largest improvements occurred on CIFAR-10-C.

\- CIFAR-100-C achieved moderate but reliable gains.

\- ImageNet-C showed measurable improvements with greater variability across corruption types.

\- Most adaptation benefits occurred within the first 5–20 optimization steps.

\- Sequential domain adaptation exposed performance drops when corruption types changed, highlighting limitations of continuous BatchNorm-only adaptation.

\---


\## Technologies

\- Python

\- PyTorch

\- torchvision

\- NumPy

\- Matplotlib

\- Jupyter Notebook

\---

\## Running the Project

1\. Clone this repository

```bash

git clone https://github.com/yourusername/test-time-entropy-minimization.git

```

2\. Install dependencies

```

3\. Download the required benchmark datasets (CIFAR-10-C, CIFAR-100-C, and ImageNet-C) and update the dataset paths if necessary.

4\. Open

```

notebooks/tent\_experiments.ipynb

```

and execute the notebook cells.

\---


\## Documentation

Additional details can be found in:

\- `docs/report.pdf` — Final project report

\- `docs/presentation.pdf` — Project presentation

\---


\## References

\- Wang et al. (2021). \*Tent: Fully Test-Time Adaptation by Entropy Minimization\*

\- Hendrycks \& Dietterich (2019). \*Benchmarking Neural Network Robustness to Common Corruptions and Perturbations\*

\- Sun et al. (2020). \*Test-Time Training with Self-Supervision\*

\- Niu et al. (2022). \*Efficient Test-Time Model Adaptation without Forgetting\*

\---


\## Author

Daniel Gulvin



M.S. Computer Science  

University at Buffalo

