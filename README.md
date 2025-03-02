# CMSN
Collatz-Matthews Sequence Networks: A Multidimensional Extension of the 3n + 1 Problem Daniel Scott Matthews March 2025

# Collatz-Matthews Sequence Networks (CMSN) Analysis

This repository contains the Python source code for generating and analyzing Collatz-Matthews Sequence Networks (CMSNs), a multidimensional extension of the Collatz conjecture introduced in the paper "Collatz-Matthews Sequence Networks: A Multidimensional Extension of the 3n + 1 Problem" by Daniel Scott Matthews (March 2025). CMSNs augment the traditional Collatz sequence with metrics \( b_x \) (total steps), \( b_y \) (odd-step logarithmic sums), \( b_z \) (odd-step counts), and \( G \) (odd-step growth), providing insights into convergence dynamics.

## Overview

The Collatz conjecture posits that for any positive integer \( n \), iterating \( n \to n/2 \) if even and \( n \to 3n + 1 \) if odd leads to 1. This code computes CMSNs for \( n = 1 \) to 30,000,000, revealing a key finding: \( b_z / b_x < 0.388 \) (max 0.374), with \( b_x - b_z > G \) universally across 30 million sequences. This supports the conjecture empirically and suggests a heuristic proof, detailed in the associated paper.

## Contents

- **`CMSN Analysis Script 4.0.py`**: The main Python script that generates CMSN sequences, analyzes metrics, and produces output files (CSV, PNG figures). It uses multi-threading for efficiency, processing 30M sequences in ~2-4 minutes with 16 processes.

## Prerequisites

- **Python**: Version 3.6+ (tested with 3.9).
- **Dependencies**:
  - `pandas`: For data handling and CSV output.
  - `numpy`: For numerical computations (e.g., \( \log_2 \)).
  - `matplotlib`: For plotting distributions and scatters.
  - `seaborn`: For enhanced visualization.
  - `scipy`: For statistical analysis (e.g., regression).
  - Install via: `pip install pandas numpy matplotlib seaborn scipy`

## Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/cmsn-analysis.git
   cd cmsn-analysis
   
