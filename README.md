Parametric Nonlinear Volterra Series via Machine Learning
====================================================================

This script supports Chapter 4 of the doctoral thesis:
"4 Parametric Nonlinear Volterra Series via Machine Learning for 3D Unsteady Transonic Loads." for 3D Test Case

Purpose:
--------
This code provides a framework for identifying Volterra series kernels from CFD-based unsteady aerodynamic responses and leveraging machine learning techniques for efficient kernel prediction. It supports both linear and quadratic kernel modeling and enables flutter prediction using data-driven surrogates.

Key Features:
-------------
- Kernel Extraction: Computes linear and nonlinear Volterra kernels for lift (CL) and pitching moment (CM) from small-amplitude forced CFD simulations.
- ML Prediction: Uses Fully Connected Neural Networks (FCNN) and Gaussian Process Regression (GPR) to estimate kernel coefficients from flight condition inputs (Mach, AoA, CL₀, CM₀).
- Flutter Analysis: Predicts unsteady structural response and flutter dynamic pressure using FCNN-predicted Volterra kernels.

Dependencies:
-------------
Install the required Python packages before running the scripts:

```bash
pip install numpy
pip install pandas
pip install matplotlib
pip install tensorflow
pip install keras-tuner
pip install GPy
pip install scipy
```
-------------
Ensure the following scripts are executed in the proper sequence:

1. **Volterra Kernel Identification (Baseline from CFD)**
   
   ```bash
   Volterra/Volterra_kernels.ipynb
   ```
   Extracts ground-truth linear and nonlinear kernels from CFD-based forced pitch simulations.

2. **ML-Based Kernel Prediction**
   
   - FCNN (linear kernels):
     ```bash
     ML_models/FCNN_Volterra_kernels_linear.ipynb
     ```

   - FCNN (nonlinear kernels):
     ```bash
     ML_models/FCNN_Volterra_kernels_NL.ipynb
     ```

   - GPR (both kernels):
     ```bash
     ML_models/GPR_Volterra_kernels.ipynb
     ```

3. **Kernel Comparison and Flutter Prediction**
   
   ```bash
   Volterra/Volterra_vs_fcnn_vs_gp.ipynb
   ```
   - Reconstructs CL and CM using Volterra kernels (true vs predicted).
   - Performs flutter analysis using FCNN kernels.
   - Saves predicted flutter dynamic pressures.

4. **Data Fusion with Co-Kriging**

   ```bash
   ML_models/co_kriging_Qflutter.ipynb
   ```
   Combines low- and high-fidelity predictions to enhance flutter boundary estimation using multi-fidelity surrogate modeling.

Author: Gabriele Immordino
