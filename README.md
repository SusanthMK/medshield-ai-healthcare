# Intrusion-Aware Dynamic Encryption for Self-Healing Medical Communication

## Overview

This project presents an AI-driven framework for securing medical data transmission in healthcare systems. The system integrates machine learning-based intrusion detection with dynamic encryption techniques to ensure secure and reliable communication.

The primary objective is to detect cyber-attacks in real time and automatically adapt encryption mechanisms to protect sensitive medical data.

## Introduction

Healthcare systems transmit large volumes of sensitive patient data through networked devices and medical IoT systems. This data is highly vulnerable to cyber-attacks, unauthorized access, and privacy breaches.

Traditional security mechanisms rely on static encryption techniques, which are not capable of adapting to evolving threats. This project introduces an intelligent system that dynamically adjusts encryption strategies based on detected intrusions. 


## Problem Statement

* Medical data is highly sensitive and frequently targeted by cyber-attacks
* Existing systems rely on static encryption and lack adaptability
* Current systems detect threats but cannot automatically respond
* Lack of intelligent, self-healing security frameworks


## Objectives

* Detect cyber-attacks using machine learning models
* Secure medical data using AES encryption
* Implement ECDH-based secure key exchange
* Dynamically update encryption keys based on threat levels
* Develop a self-healing communication system


## System Architecture

The system operates through the following pipeline:

1. Medical data is collected from sensors
2. Intrusion detection is performed using AI models
3. If an anomaly is detected:

   * Transmission is blocked OR
   * Encryption keys are updated dynamically
4. Secure data transmission is maintained

(Refer to architecture diagram in project) 


## Concepts Used

### 🔹 CNN–BiLSTM Intrusion Detection Model

A hybrid deep learning model used to detect malicious network traffic:

* CNN extracts important features from network data
* BiLSTM captures sequential patterns in traffic behavior
* Enables accurate detection of complex cyber-attacks


### 🔹 Elliptic Curve Diffie–Hellman (ECDH)

A secure key exchange mechanism:

* Generates a shared secret between sender and receiver
* Ensures secure communication without transmitting keys directly


### 🔹 HMAC-Based Key Derivation Function (KDF)

* Converts shared secrets into strong encryption keys
* Enhances security by generating unpredictable keys


### 🔹 Advanced Encryption Standard (AES)

* A symmetric encryption algorithm
* Used to encrypt sensitive medical data during transmission
* Provides strong confidentiality and data protection


### 🔹 Dynamic Re-Keying (Self-Healing Mechanism)

* Automatically updates encryption keys when threats are detected
* Maintains secure communication even under attack conditions
* Enables adaptive and resilient security

## Dataset

The project uses intrusion detection datasets:

* UNSW-NB15
* CICIDS2017

These datasets include:

* Normal traffic
* Cyber-attacks such as:

  * DDoS
  * Brute force
  * Botnet
  * Port scanning

Each record contains features like packet size, flow duration, protocol type, and connection statistics. 


## Methodology and Implementation

### 1. Data Collection

Network traffic data is collected from standard intrusion detection datasets.

### 2. Data Preprocessing

* Handling missing values
* Encoding categorical data
* Feature scaling

### 3. Feature Extraction (CNN)

Extracts important traffic features.

### 4. Sequence Analysis (BiLSTM)

Analyzes temporal patterns in network behavior.

### 5. Threat Prediction

Classifies traffic into:

* LOW
* MEDIUM
* HIGH


### 6. Secure Encryption

* AES encryption is applied to medical data
* Keys are generated using ECDH

### 7. Self-Healing Response

* Detect intrusion → regenerate keys
* Maintain secure communication


### 8. Performance Evaluation

Metrics used:

* Accuracy
* Precision
* Recall
* F1-score
* ROC curve

## Results

The system demonstrates:

* High intrusion detection accuracy
* Effective classification of network traffic
* Secure encrypted communication
* Automatic response to cyber threats

(Refer to graphs and UI in repository) 

## Repository Structure

* `cnn_bilstm.py` – Intrusion detection model
* `aes.py` – Encryption
* `ecdh.py` – Key exchange
* `kdf.py` – Key derivation
* `train.py` – Model training
* `interface.py` – UI
* `README.md` – Documentation


## Technologies Used

* Python
* TensorFlow / PyTorch
* NumPy
* Pandas
* Matplotlib


## Dependencies

* Python 3.x
* numpy
* pandas
* scikit-learn
* matplotlib
* tensorflow / torch


## How to Run

```bash id="sec_final"
pip install -r requirements.txt
python train.py
```


## Project Scope

* AI-based secure communication system
* Simulation of real-world healthcare IoT security
* Academic and research-focused


## Conclusion

This project introduces a self-healing security system that combines AI-based intrusion detection with adaptive encryption techniques. The system ensures secure medical communication by dynamically responding to cyber threats.


## Future Work

* Real-time deployment in healthcare IoT
* Integration with live network traffic
* Advanced deep learning models
* Cloud-based secure healthcare systems
