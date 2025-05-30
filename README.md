# Torque Estimation of Upper Limb Shoulder Joint during Elevation at Different Speeds

## Description

This repository contains a Jupyter notebook that uses inverse dynamics to estimate shoulder joint torque during sagittal-plane elevation of the upper limb at two distinct speeds (slow and rapid). The notebook demonstrates a reproducible workflow for biomechanical analysis, relevant for rehabilitation protocols, assistive-device development, and educational purposes.

## Features

* Import 2D kinematic data (`Ombro.txt` and `Mão.txt`) exported from Tracker Online.
* Compute segment geometry: mean length, center of gravity, and moment of inertia based on anthropometric parameters.
* Calculate instantaneous angular position, velocity, and acceleration using numerical differentiation and Savitzky–Golay smoothing.
* Estimate gravitational and inertial torque components and visualize their contributions over time and angle.
* Generate clear plots and summary statistics for comparative analysis between slow and fast trials.

## Installation

### Prerequisites

* Python 3.7 or higher
* [Git](https://git-scm.com/)
* [Google Colab](https://colab.research.google.com/) (optional but recommended)

### Dependencies

```bash
pip install numpy pandas matplotlib seaborn scipy ipython
```

## Usage

1. **Clone the repository**

   ```bash
   ```

git clone [https://github.com/guilherme-de-medeiros/torque-estimation-upper-limb.git](https://github.com/guilherme-de-medeiros/torque-estimation-upper-limb.git)
cd torque-estimation-upper-limb

````

2. **Prepare data files**
- Place the exported data files (`Ombro.txt` and `Mão.txt`) in the `data/` folder or upload them to your Google Drive.

3. **Open and run the notebook**
- In Colab: [Open in Colab](https://colab.research.google.com/github/guilherme-de-medeiros/torque-estimation-upper-limb/blob/main/torque_estimation_upper_limb.ipynb)
- If using local Jupyter:
  ```bash
jupyter notebook torque_estimation_upper_limb.ipynb
  ```

4. **Mount Google Drive** (if using Colab and storing data in Drive):
```python
from google.colab import drive
drive.mount('/content/drive')
````

5. **Run all cells** to reproduce the analysis. Adjust file paths if necessary.

## Repository Structure

```
torque-estimation-upper-limb/
├── data/
│   ├── Ombro.txt          # Shoulder coordinate data (Tracker Online export)
│   └── Mão.txt            # Hand coordinate data (Tracker Online export)
├── torque_estimation_upper_limb.ipynb  # Main analysis notebook
└── README.md              # Project overview and instructions
```

## Results

* Plots of angular position, velocity, acceleration, and torque components for both speed trials.
* Summary of peak gravitational and inertial torques.
* Insights into the relative contributions of gravity and inertia during controlled versus rapid movements.

## Contributing

Contributions to improve functionality, add tests, or enhance documentation are welcome. Please:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m "Add YourFeature"`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author

**Guilherme de Medeiros** (11201920193)
Email: [gmedeiros990514@gmail.com](mailto:gmedeiros990514@gmail.com)

<hr>
*Biomecânica II – 2025Q1*
