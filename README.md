# GridSentry ⚡ Sentinel of the Smart Grid

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python Version](https://img.shields.io/badge/python-3.9%2B-blue.svg)](https://www.python.org/downloads/)
[![PyTorch Version](https://img.shields.io/badge/PyTorch-2.0%2B-EE4C2C.svg)](https://pytorch.org/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

**GridSentry is an end-to-end deep learning pipeline for probabilistic energy forecasting and grid optimization. It provides an interactive command center to simulate the impact of exogenous shocks (like mass EV adoption) and deploy intelligent, demand-side management strategies to ensure grid resilience.**



---

## 🤔 The Challenge: From Forecasting to Future-Proofing

A simple forecast tells you what *might* happen. A resilient system tells you what you can *do* about it. GridSentry bridges this gap. It's an integrated environment that moves beyond single-point predictions to provide a full-stack solution for stress-testing and intelligently managing our energy future.

This project tackles the entire ML lifecycle: from ingesting raw time-series data to deploying a sophisticated, interactive dashboard that allows stakeholders to explore scenarios and make data-driven decisions.

---

## ✨ Core Capabilities

* **🧠 Advanced Probabilistic Forecasting**: At its core is a hybrid **Temporal Convolutional Network (TCN) and Transformer** architecture. The TCN excels at capturing local, high-frequency patterns, while the Transformer models long-range dependencies and seasonality. The model performs **quantile regression**, providing a full range of potential outcomes to quantify uncertainty, not just a single prediction.

* **⚡ Dynamic Simulation Engine**: The "What-If" engine allows for the dynamic simulation of future grid stress. The flagship scenario models the impact of uncontrolled EV charging, allowing users to define the fleet size, charging power, and duration to analyze the resulting strain on the grid's peak load and infrastructure.

* **💡 Heuristic Optimization for Demand-Side Management**: GridSentry implements a **greedy optimization algorithm** to perform intelligent load shifting. This demand-side management strategy automatically moves flexible EV loads to off-peak hours, executing "peak shaving" to reduce infrastructure strain and "valley filling" to improve the overall load factor.

* **🎮 Rapid Prototyping & MLOps-Ready Interface**: The entire pipeline is wrapped in a sleek, interactive dashboard built with **`ipywidgets`**. This serves as a powerful tool for rapid experimentation and stakeholder engagement, allowing users to test hypotheses and visualize outcomes in real-time without touching the underlying code.

---

## 🛠️ The Technology Stack: A Modern AI & MLOps Toolkit

This project leverages a curated stack of modern libraries to build a robust, end-to-end AI system.

| Domain                               | Technologies & Libraries                                          | Application & Rationale                                                                                                                              |
| ------------------------------------ | ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Core ML & Deep Learning** | `PyTorch` (`torch.nn`, `DataLoader`), `Scikit-learn`              | **PyTorch** was used to architect and train the custom TCN-Transformer hybrid model. **Scikit-learn** provides robust modules for preprocessing and scaling. |
| **Data Science & Numerical Computing** | `Pandas`, `NumPy`, `SciPy`                                        | **Pandas** for its powerful time-series indexing and manipulation. **NumPy** for high-performance numerical computation and array manipulation.           |
| **ML Pipeline & Prototyping** | `Jupyter Notebook`, `ipywidgets`, `dataclasses`                   | **Jupyter** serves as the interactive development environment. **`ipywidgets`** provides the interactive dashboard for rapid, code-free experimentation. |
| **Optimization & Simulation** | `NumPy`                                                           | The core simulation engine and greedy optimization algorithm are built on NumPy's efficient vectorization for high-speed scenario analysis.         |
| **Data Visualization & Reporting** | `Matplotlib`                                                      | Used to generate the final, multi-panel "Smart Grid Optimization Dashboard" for a clear, visual summary of the results.                       |
| **Software Engineering & Utilities** | `tqdm`, `holidays`, `importlib`                                   | `tqdm` for progress bars during training, `holidays` for feature engineering, and `importlib` for robust environment checking.                |

---

## 🚀 Getting Started

Ready to become a grid sentinel? Get up and running in just a few steps.

### **1. Prerequisites**

* Python 3.9+
* An environment manager like `conda` or `venv` is highly recommended.

### **2. Installation**

Clone the repository and install the required packages into your environment.

```bash
# Clone this repository
git clone [https://github.com/your-username/GridSentry.git](https://github.com/your-username/GridSentry.git)
cd GridSentry

# Create and activate a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

# Install the dependencies
pip install -r requirements.txt
