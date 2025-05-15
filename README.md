# Synthetic Aperture Radar (SAR) Strip Map Imaging with Environmental Effects
Synthetic Aperture Radar (SAR) Strip Map Imaging in MATLAB under Environmental Effects



This MATLAB project simulates a Synthetic Aperture Radar (SAR) system mounted on an airborne platform. It generates strip map images of a point target and realistic terrain using a Digital Elevation Model (DEM). The simulation is extended to model environmental conditions such as rain, fog, and snowfall to observe their effects on SAR image quality.

## 🚀 Features

- 📡 SAR imaging from a side-looking airborne platform (squint angle: 0°)
- 🔁 Chirp waveform transmission with 100% duty cycle
- 🧱 Strip map image generation for:
  - Point target on flat ground
  - Realistic terrain using DEM
- 🌧️ Environmental condition simulation:
  - Rain
  - Fog
  - Snowfall

# 🛰️ Synthetic Aperture Radar (SAR) Simulation and Analysis Using MATLAB

This repository contains a complete simulation of a Synthetic Aperture Radar (SAR) system using MATLAB and its Radar Toolbox. The project simulates both point-target and terrain-based imaging using a Digital Elevation Model (DEM), and models environmental effects such as rain, fog, and snow. It includes parametric studies to analyze the influence of radar system parameters on imaging performance.

---

## 📋 Project Overview

Synthetic Aperture Radar (SAR) is a remote sensing technique that enables high-resolution imaging by synthesizing a large virtual aperture from a moving radar platform. This project demonstrates the simulation of SAR imaging in MATLAB under different configurations and environmental conditions.

---

## 👨‍💻 Team Members

| Name         | Contribution                                                                 |
|--------------|------------------------------------------------------------------------------|
| Param Gupta  | Point-target SAR system, parameter analysis, environmental condition models |
| Kumar Rishav | DEM integration, terrain-based imaging, data visualization, final presentation |
| Naman Garg   | MATLAB code documentation, results interpretation, report compilation       |

---

## 🧪 Simulation Phases

### 1. **Point Target Imaging**
- Simulates a SAR system imaging a single ground reflector.
- Range migration algorithm is used for image focusing.
- Parameter sweeps include:
  - Altitude
  - Platform velocity
  - Wavelength
  - Chirp rate
  - PRI (Pulse Repetition Interval)
  - Transmit power
  - Antenna gain

### 2. **Terrain-Based Strip Map Imaging**
- Utilizes a Digital Elevation Model (DEM) to simulate a realistic scene.
- Strip-map SAR image is generated using matched filtering and back-projection algorithms.
- Observed layover and foreshortening effects demonstrate realism.

### 3. **Environmental Effects Modeling**
Environmental conditions are simulated using ITU-R-based attenuation models:

| Condition   | Attenuation | Impact Summary                |
|-------------|-------------|-------------------------------|
| Light Rain  | ~0.1 dB/km  | Slight SNR degradation        |
| Heavy Rain  | >0.1 dB/km  | Moderate blurring             |
| Fog         | ~0.01 dB/km | Minimal impact                |
| Snowfall    | ~0.05 dB/km | Increased image noise         |

---

## 🧠 Key Insights

### Radar Parameter Trade-offs
- **Altitude**: Higher altitude improves coverage but reduces resolution.
- **Velocity**: Faster platforms improve azimuth resolution but risk Doppler aliasing.
- **Wavelength**: Shorter wavelengths enhance resolution but suffer more from attenuation.
- **Chirp Rate**: Controls range resolution and processing complexity.
- **Power & Gain**: Directly influence SNR and image quality.
- **PRI**: Needs optimization to balance resolution and avoid ambiguity.

### Environmental Robustness
- SAR remains resilient in fog and snow.
- Rain has the most pronounced negative impact on SNR and clarity.

---

## 📁 Repository Structure

sar-simulation/
│
├── data/ # Digital Elevation Models (DEM)
├── images/ # Output SAR images
├── scripts/
│ ├── point_target_sim.m # Point target simulation
│ ├── terrain_imaging_dem.m # Terrain imaging using DEM
│ ├── model_rain.m # Rain effect model
│ ├── model_fog.m # Fog effect model
│ ├── model_snow.m # Snowfall effect model
│ └── utils/ # Utility functions (compression, visualization, etc.)
├── results/ # Processed result images and data
├── README.md
└── LICENSE


---

## 💻 Requirements

- MATLAB R2021a or later
- Radar Toolbox
- Signal Processing Toolbox
- Mapping Toolbox (for DEM support)

---

## 📷 Sample Outputs

| Scenario        | Image Description                     |
|-----------------|----------------------------------------|
| Point Target     | High-resolution focused image         |
| DEM Terrain      | Strip-map image with layover effects  |
| Rainy Condition  | Blurred image with SNR degradation    |
| Foggy Condition  | Slight contrast loss                  |
| Snowy Condition  | Increased speckle and noise           |

---

## 📚 References

- MATLAB Radar Toolbox Documentation  
- ITU-R P.838 (rain), P.840 (fog), P.837 (snow) attenuation models  
- NASA SRTM DEM data  

---

## 🔭 Future Work

- Implement spotlight SAR imaging
- Introduce multipath and clutter effects
- Use real flight trajectory data
- Experiment with polarimetric SAR (PolSAR)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 📬 Contact

For any queries or collaboration opportunities, feel free to reach out via GitHub or email the contributors.

