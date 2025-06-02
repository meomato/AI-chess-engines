# AI-chess-engines

## Overview

This project presents a **comparative analysis of five modern AI-based chess engines** and implements the two most promising ones — **Leela Chess Zero** and **Stockfish NNUE** — for in-depth practical evaluation.

The engines analyzed are:

* **DeepChess**
* **AlphaZero**
* **Leela Chess Zero**
* **Stockfish NNUE**
* **Maia**

Among them, **Lc0** and **Stockfish NNUE** were selected for implementation based on criteria such as:

* Open-source availability
* Strength (Elo rating)
* Efficiency (CPU usage)
* Learning method
* Practical usability

## Selected Engines: Installation & Setup

### Leela Chess Zero (Lc0)

1. **Download the engine**:
 [LCZero Download Page](https://lczero.org/play/download/)

2. **Choose the version** for your OS:

   * Windows: `lc0.exe`
   * macOS/Linux: appropriate binary or compile from source

3. **Specify path in code**:

   ```python
   lc0_path = Path("your_path_to_lc0/lc0.exe")  # update to your actual location
   ```

### Stockfish NNUE

1. **Download the official Stockfish build**:
 [Stockfish Download Page](https://stockfishchess.org/download/)

2. **Pick the correct build**:

   * Example: `stockfish_17_x64_avx2.exe` (with NNUE support)

3. **Specify path in code**:

   ```python
   stockfish_path = Path("your_path_to_stockfish/stockfish_17_x64_avx2.exe")
   ```

## What This Project Includes

* **Theoretical comparison** of five engines (architecture, training method, resource demands, and evaluation)
* **Implementation** of Lc0 and Stockfish NNUE
* **120-game experimental evaluation** across four configurations
* **Statistical tests** (Kolmogorov–Smirnov, Levene’s test, Welch’s t-test) on:

  * Move time distributions
  * CPU usage variability
  * Evaluation quality

## Key Findings

| Engine             | Strength (Elo) | Eval Quality (+Elo/game) | Avg Move Time | CPU Load | Stability |
| ------------------ | -------------- | ------------------------ | ------------- | -------- | --------- |
| **Lc0**            | \~3580         | +3.2                     | 2.2s (varied) | High     |  Variable |
| **NNUE (default)** | \~3900         | +0.83                    | 2.3s (stable) | Low      |  Stable   |

* **Lc0** excels in evaluation strength but consumes more CPU and is less stable on CPU-only systems.
* **NNUE** is fast, stable, and efficient, making it suitable for practical use even on weak machines.

## Full Report

See the full implementation details, code explanations, and result visualizations in the notebook and the PDF report:

1. Notebook: [`lc0-and-stockfish.ipynb`](./lc0-and-stockfish.ipynb)
2. Analysis of Neural Models in Chess and Their Implementation pdf: [`course_work.pdf`](./course_work.pdf)
