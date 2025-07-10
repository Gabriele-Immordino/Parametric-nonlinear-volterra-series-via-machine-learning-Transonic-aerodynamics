```markdown
# BSCW Dataset for Volterra Series Identification (Chapter 4)

This directory contains datasets used in **Chapter 4** of the doctoral thesis:

**"Data-Driven Modelling of Nonlinear Aerodynamics in High-Speed Aircraft Using Machine Learning"**  
*Gabriele Immordino, University of Southampton, August 2025*

---

## 📁 Dataset Files

### 1. `dataset_CL0_CM0_M_AoA.npy`
- **Shape:** `(70, 900, 4)`  
- **Description:** Steady-state aerodynamic data. Although stored with a time axis, the data are temporally constant per sample and are repeated across 900 timesteps for compatibility with unsteady datasets.

#### 🧾 Features

| Index | Feature | Description                  | Units       |
|-------|---------|------------------------------|-------------|
| 0     | Mach    | Freestream Mach number       | –           |
| 1     | AoA     | Angle of attack              | degrees     |
| 2     | CL₀     | Steady-state lift coefficient| –           |
| 3     | CM₀     | Steady-state pitching moment coefficient   | –           |

---

### 2. `dataset_CL_CM_1_deg.npy`
- **Shape:** `(70, 900, 2)`  
- **Description:** Unsteady aerodynamic response (CL and CM) to a **1° pitch step input**, simulated with CFD URANS over 900 timesteps.

#### 🧾 Features

| Index | Feature | Description                  | Units       |
|-------|---------|------------------------------|-------------|
| 0     | CL      | Unsteady lift coefficient    | –           |
| 1     | CM      | Unsteady pitching moment coefficient  | –           |

---

### 3. `dataset_CL_CM_2_deg.npy`
- **Shape:** `(70, 900, 2)`  
- **Description:** Unsteady aerodynamic response (CL and CM) to a **2° pitch step input**, simulated with CFD URANS over 900 timesteps.

#### 🧾 Features

| Index | Feature | Description                  | Units       |
|-------|---------|------------------------------|-------------|
| 0     | CL      | Unsteady lift coefficient    | –           |
| 1     | CM      | Unsteady pitching moment coefficient  | –           |


