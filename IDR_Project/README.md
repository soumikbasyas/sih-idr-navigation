# 🛰️️ AI-ML Intelligent Dead Reckoning (IDR) System
**Smart India Hackathon | Problem Statement ID: 20768 | Organization: ISRO**

[![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20iOS-blue)](#)
[![AI/ML](https://img.shields.io/badge/AI%2FML-TensorFlow%20%7C%20PyTorch-orange)](#)
[![Dataset](https://img.shields.io/badge/Dataset-IO--VNBD-lightgrey)](#)
[![Status](https://img.shields.io/badge/Status-SIH_Screening_Phase-success)](#)

## 📌 Executive Summary
Modern vehicle logistics, ride-hailing services, and emergency responders rely heavily on GNSS-based navigation. However, in environments with structural blockages (long underground tunnels, deep urban canyons, dense foliage), GNSS signals drop entirely, causing critical navigation failures and safety hazards. 

This project delivers a **lightweight, edge-deployable software engine and mobile application** that transforms a standard smartphone into an Intelligent Dead Reckoning (IDR) system. By applying advanced AI/ML models to noisy, consumer-grade smartphone IMU sensors (accelerometer and gyroscope), our solution provides highly accurate, seamless navigation during GNSS blackouts without requiring external hardware or OBD-II speedometer feeds.

---

## 🚀 Core Innovation & Technical Modules

Our architecture is divided into a **Cloud-Based Training Pipeline** and an **Edge-Deployable Inference Engine**, ensuring complex training occurs off-device while real-time, low-latency prediction happens on the smartphone.

*   **In-Vehicle Alignment & Calibration Engine:** An algorithmic module that automatically determines the smartphone's pitch, roll, and yaw relative to the vehicle's driving direction, making the solution robust regardless of whether the phone is dashboard-mounted or placed loosely in a holder.
*   **AI Speed & Vibration Filter:** A deep-learning/statistical signal-processing model running locally on the edge. It filters out high-frequency road noise, engine idling, and pothole shocks to directly estimate vehicle forward velocity from IMU signals.
*   **Advanced Map-Matching & Kinematic Constraints:** A sophisticated framework (utilizing Unscented Kalman Filters + Hidden Markov Map Matching) that binds the calculated position to known road networks and geometric paths during signal dropouts.
*   **GNSS+INS Fusion Engine:** An innovative AI-based Sensor Fusion Algorithm that seamlessly combines GNSS and IMU measurements. It features an instant **Seamless GNSS Deficit Handler** to transition between GNSS-aided INS and Dead Reckoning within milliseconds.

---

## 🎯 Target Performance Benchmarks (SIH Requirements)

Our AI models and edge engine are strictly optimized to meet the Indian Space Research Organisation's (ISRO) performance criteria:

| Metric | Target Benchmark |
| :--- | :--- |
| **Positional Drift** | `< 10%` of the total distance traveled during a GNSS blackout. |
| **Short-Distance Accuracy** | `< 5 meters` of drift over a 50m GNSS-denied environment (in <1 min). |
| **Long-Distance Accuracy** | `< 100 meters` of drift over a 1km GNSS-denied environment at 60kmph. |
| **Processing Speed** | Position update rate of `10Hz` on the mobile application interface. |

---

## 📊 Dataset & Model Training
The core AI/ML models are trained, tested, and validated using the **IO-VNBD (Inertial and Odometry benchmark dataset for ground vehicle positioning)**. 
*   **Training (Cloud/Desktop):** Leveraging high-compute environments to process IO-VNBD and extract kinematic patterns.
*   **Inference (Smartphone):** The trained models are compressed and exported to the smartphone edge environment for live inference using the phone's built-in IMU.

---

## ⚙️ Getting Started & Installation

### Prerequisites
*   Python 3.9+ (For model training)
*   Android Studio / Flutter SDK (For mobile application deployment)

### 1. Model Training Environment
```bash
# Clone the repository
git clone [https://github.com/soumikbasyas/sih-idr-navigation.git](https://github.com/soumikbasyas/sih-idr-navigation.git)
cd YourRepoName

# Install Python dependencies
pip install -r requirements.txt

# Run the training pipeline on the IO-VNBD dataset
python train.py
