# SUBVO Dataset: Submerged Monocular Visual Odometry

![Trajectory Demo](trajectory.gif)

**SUBVO** is an open, calibrated underwater dataset designed to benchmark monocular visual odometry (VO) systems in challenging submerged environments. Captured in a controlled pool using a monocular camera, it includes frame-by-frame ground truth, full camera calibration, and sample code for VO pipeline evaluation.

---

## 🧭 Dataset Overview

- **Environment**: Indoor pool, 1.6 m deep, stable lighting  
- **Platform**: Tracked crawler robot  
- **Camera**: IPC608UW‑10 POE IP Underwater Camera  
- **Frames**: 220 sequential images (1280 × 720, JPEG)  
- **Path Length**: 5.8 meters (X–Z plane)  
- **Calibration**: Intrinsic matrix & distortion coefficients via 9×6 checkerboard (2.2 cm squares)  
- **Ground Truth**: Floor-anchored chain with labelled colored tags  
- **Available Files**:
  - `/images/` – raw image sequence  
  - `calibration.yaml` – camera intrinsics  
  - `groundtruth.txt` – X, Z coordinates (meters) per frame  

---

## ⚙️ Use Cases

- Evaluate feature detector/descriptors under underwater conditions  
- Compare VO accuracy with different matching + pose estimation methods  
- Study the impact of preprocessing and parameter tuning (e.g. RANSAC threshold)

---

## 🧪 Reference Pipeline

 achieving **7 cm RMSE** using:
- **AKAZE** features  
- Genetic algorithm (GA) to optimize RANSAC threshold  
- Essential matrix estimation + pose refinement  
- Rotation clipping for motion smoothing

Example trajectory plots and performance metrics are available in the `/results/` folder.

---

## 📁 Repository Structure
- `/images/ → Underwater image frames`
- `/calibration.yaml → Camera intrinsic parameters`
- `/groundtruth.txt → Ground truth trajectory (X, Z)`
- `/results/ → Sample outputs: trajectory plots, logs, metrics`
- `README.md → You are here`

---

## 📜 Citation

If you use SUBVO in your research, please cite:

> Arman Neyestani, Francesco Picariello, Daniel Mihai Toma, Ahmad Falahzadeh, Pasquale Daponte, Joaquin Del Rio Fernandez, Luca De Vito  
> **"SUBVO Dataset: Analyzing Feature Extraction for Underwater Monocular Visual Odometry"**  
> *IEEE I2MTC 2025 Conference*  
> [Link to paper]

---

## 🔗 License

This dataset is released under the **CC BY 4.0 License**.  
Attribution required for redistribution and academic use.

---

## 🙏 Acknowledgements

Developed by the LESIM Lab (University of Sannio, Italy) and OBSEA Lab (UPC, Spain), with support from the EU HORIZON iMagine Project (GA 101058625) and AGAUR fellowship (BDNS 474817).


