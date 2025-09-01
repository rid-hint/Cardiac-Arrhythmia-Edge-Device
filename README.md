# Intelligent Edge Device for Real-Time Cardiac Arrhythmia Detection

**Project Status:** In Progress (Final Year B.Tech Project | Expected Completion: March 2026)

## 1. Overview
This project involves the development of a low-power, portable intelligent edge device for the real-time, on-device detection and classification of cardiac arrhythmias using lightweight deep learning models[cite: 2034, 2095]. [cite_start]By performing all computation locally, this system aims to solve the critical issues of latency and data privacy inherent in cloud-based solutions, offering an autonomous and scalable tool for continuous cardiac monitoring[cite: 2060, 2096, 2115].

## 2. Problem Statement & Research Gap
[cite_start]Cardiovascular diseases are a leading cause of death globally, and many related arrhythmias occur unpredictably, necessitating continuous monitoring for early diagnosis[cite: 2021, 2058]. [cite_start]While medical-grade ECG patches exist, they often rely on cloud processing ("capture now, analyze later"), which introduces latency and privacy concerns[cite: 2060, 2087]. [cite_start]Conversely, consumer smartwatches are economical but typically limited to detecting only a narrow class of arrhythmias, like Atrial Fibrillation[cite: 2087].

[cite_start]This project addresses a clearly identified research gap: the need for a **low-cost, medical-grade, on-device system capable of real-time, multi-class arrhythmia classification**[cite: 2087].

## 3. Proposed Solution & Objectives
[cite_start]The goal is to design a compact, wearable ECG monitor that performs all machine learning inference on the device itself[cite: 2095].

The primary objectives are:
* [cite_start]To develop a cost-effective and power-efficient embedded system[cite: 2097].
* [cite_start]To implement the real-time detection of 5 types of arrhythmias compliant with AAMI standards (N, S, V, F, Q)[cite: 2095, 2147].
* [cite_start]To ensure complete data privacy by processing all ECG data locally on the device[cite: 2096].

![Proposed System Diagram](PASTE_YOUR_IMAGE_LINK_HERE)
*(Note: Replace "PASTE_YOUR_IMAGE_LINK_HERE" with the link you copied in the steps above.)*

## 4. Hardware & Software Architecture
The system is being built with modern, industry-relevant components selected for their efficiency and performance in resource-constrained environments.

### Planned Technology Stack
* [cite_start]**System on Chip (SoC):** Nordic nRF52840, featuring an ARM Cortex-M4F processor suitable for efficient ML inference and integrated Bluetooth Low Energy (BLE) connectivity[cite: 2178].
* [cite_start]**Analog Front-End (AFE):** Texas Instruments ADS122R, a high-fidelity, 24-bit AFE for robust ECG signal acquisition[cite: 2175, 2177].
* [cite_start]**Display:** A 0.96-inch I2C OLED screen for providing immediate, on-device user feedback[cite: 2180].
* [cite_start]**Power Management:** A 3.7V LiPo battery managed by dedicated TI charger (BQ24050) and monitor (BQ27441) ICs for reliable, long-term operation[cite: 2181].
* **ML Model:** A compressed, ResNet-based deep learning model optimized for the edge. [cite_start]Techniques such as **Knowledge Distillation** will be employed to reduce the model's footprint while maintaining high accuracy[cite: 2079].

## 5. Dataset & Preprocessing
* [cite_start]**Dataset:** The project will use the industry-standard **MIT-BIH Arrhythmia Database** from PhysioNet[cite: 2116]. [cite_start]This is a certified database widely recommended for evaluating arrhythmia classification algorithms[cite: 443, 445].
* [cite_start]**Classification Standard:** Heartbeats will be classified according to the **AAMI 5-class standard (N, S, V, F, Q)**[cite: 2147].
* [cite_start]**Preprocessing:** The dataset will be preprocessed to handle class imbalances via resampling and normalized before being used for model training[cite: 2152, 2153].

## 6. Project Roadmap
-   [x] **Literature Survey & Problem Formulation**
-   [ ] **ML Model Development & GUI Design**
-   [ ] **Hardware Implementation & GUI Integration**
-   [ ] **System Integration, Testing, and Validation**
-   [ ] **Final Project Report**

## 7. Key References
This project is built upon a foundation of existing academic research. The following papers have been instrumental in defining the project's scope and technical approach.

1.  **Dell'Aquila, C. R., Cañadas, G. E., & Laciar, E. (2023). *Embedded System for the Simultaneous Study of SAHS and Cardiac Arrhythmia*. [cite_start]IEEE Embedded Systems Letters, 15(2), 53-56.** [cite: 2208]
    * [cite_start]*Relevance:* This paper provides a key hardware reference, validating the use of the nRF52840 SoC and ADS1292R AFE for ECG applications[cite: 2282, 2303, 2315]. [cite_start]However, its lack of real-time, on-device classification highlights the primary research gap this project aims to fill[cite: 2071, 2072].

2.  **Wong, J., Nerbonne, J., & Zhang, Q. (2024). *Ultra-Efficient Edge Cardiac Disease Detection Towards Real-Time Precision Health*. [cite_start]IEEE Access, 12, 9940-9951.** [cite: 2206]
    * *Relevance:* This work forms the basis of our machine learning methodology. [cite_start]It demonstrates the effectiveness of using **Knowledge Distillation** to train a lightweight student model from a larger teacher model, achieving a 45x model size reduction with minimal accuracy loss—a technique critical for deployment on our resource-constrained hardware[cite: 2079, 2538, 2673].

3.  **Silva, G. A. L., et al. (2025). [cite_start]*A SYSTEMATIC REVIEW OF ECG ARRHYTHMIA CLASSIFICATION: ADHERENCE TO STANDARDS, FAIR EVALUATION, AND EMBEDDED FEASIBILITY*. arXiv:2503.07276v1.** [cite: 292]
    * *Relevance:* This review provides a broad understanding of the challenges in the field. [cite_start]It emphasizes the importance of adhering to AAMI standards, implementing the inter-patient paradigm for fair evaluation, and ensuring feasibility on embedded systems (the "E3C" criteria), which are core principles of this project[cite: 304, 355].

---
*Authored by Ridhin Thomas Alex*
