# Intelligent Edge Device for Real-Time Cardiac Arrhythmia Detection

**Project Status:** In Progress (Final Year B.Tech Project | Expected Completion: March 2026)

## 1. Overview
[cite_start]This project involves the development of a low-power, portable intelligent edge device for the real-time, on-device detection and classification of cardiac arrhythmias using lightweight deep learning models[cite: 788, 792]. [cite_start]By performing all computation locally, this system aims to solve the critical issues of latency and data privacy inherent in cloud-based solutions, offering an autonomous and scalable tool for continuous cardiac monitoring[cite: 786, 789, 792].

## 2. Problem Statement & Research Gap
[cite_start]Cardiovascular diseases are a leading cause of death globally, and many related arrhythmias occur unpredictably, necessitating continuous monitoring for early diagnosis[cite: 618, 785]. [cite_start]While medical-grade ECG patches exist, they often rely on cloud processing ("capture now, analyze later"), which introduces latency and privacy concerns[cite: 620, 647]. [cite_start]Conversely, consumer smartwatches are economical but typically limited to detecting only a narrow class of arrhythmias, like Atrial Fibrillation[cite: 647].

[cite_start]This project addresses a clearly identified research gap: the need for a **low-cost, medical-grade, on-device system capable of real-time, multi-class arrhythmia classification**[cite: 647].

## 3. Proposed Solution & Objectives
[cite_start]The goal is to design a compact, wearable ECG monitor that performs all machine learning inference on the device itself[cite: 655].

The primary objectives are:
* [cite_start]To develop a cost-effective and power-efficient embedded system[cite: 657].
* [cite_start]To implement the real-time detection of 5 types of arrhythmias compliant with AAMI standards (N, S, V, F, Q)[cite: 655, 790].
* [cite_start]To ensure complete data privacy by processing all ECG data locally on the device[cite: 656].

![Proposed System Diagram](https://i.imgur.com/G5gT7S7.png)
*(Note: You should upload the block diagram image from your presentation to your GitHub repo and link it here. I have used a placeholder link.)*

## 4. Hardware & Software Architecture

The system is being built with modern, industry-relevant components selected for their efficiency and performance in resource-constrained environments.

### Planned Technology Stack
* [cite_start]**System on Chip (SoC):** Nordic nRF52840, featuring an ARM Cortex-M4F processor suitable for efficient ML inference and integrated Bluetooth Low Energy (BLE) connectivity[cite: 738, 789].
* [cite_start]**Analog Front-End (AFE):** Texas Instruments ADS1292R, a high-fidelity, 24-bit AFE for robust ECG signal acquisition[cite: 737, 789].
* [cite_start]**Display:** A 0.96-inch I2C OLED screen for providing immediate, on-device user feedback[cite: 740, 791].
* [cite_start]**Power Management:** A 3.7V LiPo battery managed by dedicated TI charger (BQ24050) and monitor (BQ27441) ICs for reliable, long-term operation[cite: 741].
* **ML Model:** A compressed, ResNet-based deep learning model optimized for the edge. [cite_start]Techniques such as **Knowledge Distillation** will be employed to reduce the model's footprint while maintaining high accuracy[cite: 639, 790].

## 5. Dataset & Preprocessing
* [cite_start]**Dataset:** The project will use the industry-standard **MIT-BIH Arrhythmia Database** from PhysioNet[cite: 676]. [cite_start]This is a certified database widely recommended for evaluating arrhythmia classification algorithms[cite: 1554].
* [cite_start]**Classification Standard:** Heartbeats will be classified according to the **AAMI 5-class standard (N, S, V, F, Q)**[cite: 707].
* [cite_start]**Preprocessing:** The dataset will be preprocessed to handle class imbalances via resampling and normalized before being used for model training[cite: 712, 713].

## 6. Project Roadmap
-   [ ] **Literature Survey & Problem Formulation** (Completed)
-   [ ] **ML Model Development & GUI Design** (In Progress)
-   [ ] **Hardware Implementation & GUI Integration** (Planned)
-   [ ] **System Integration, Testing, and Validation** (Planned)
-   [ ] **Final Project Report** (Planned)

## 7. Key References
This project is built upon a foundation of existing academic research. The following papers have been instrumental in defining the project's scope and technical approach.

1.  **Dell'Aquila, C. R., Cañadas, G. E., & Laciar, E. (2023). *Embedded System for the Simultaneous Study of SAHS and Cardiac Arrhythmia*. IEEE Embedded Systems Letters, 15(2), 53-56.**
    * [cite_start]*Relevance:* This paper provides a key hardware reference, validating the use of the nRF52840 SoC [cite: 384] [cite_start]and ADS1292R AFE [cite: 372] for ECG applications. [cite_start]However, its lack of real-time, on-device classification [cite: 631, 632] highlights the primary research gap this project aims to fill.

2.  **Wong, J., Nerbonne, J., & Zhang, Q. (2024). *Ultra-Efficient Edge Cardiac Disease Detection Towards Real-Time Precision Health*. IEEE Access, 12, 9940-9951.**
    * *Relevance:* This work forms the basis of our machine learning methodology. [cite_start]It demonstrates the effectiveness of using **Knowledge Distillation** to train a lightweight student model from a larger teacher model [cite: 2540][cite_start], achieving a 45x model size reduction with minimal accuracy loss [cite: 2543]—a technique critical for deployment on our resource-constrained hardware.

3.  **Silva, G. A. L., et al. (2025). *A SYSTEMATIC REVIEW OF ECG ARRHYTHMIA CLASSIFICATION: ADHERENCE TO STANDARDS, FAIR EVALUATION, AND EMBEDDED FEASIBILITY*. arXiv:2503.07276v1.**
    * *Relevance:* This review provides a broad understanding of the challenges in the field. [cite_start]It emphasizes the importance of adhering to AAMI standards, implementing the inter-patient paradigm for fair evaluation, and ensuring feasibility on embedded systems (the "E3C" criteria)[cite: 1531], which are core principles of this project.

---
*Authored by Ridhin Thomas Alex*
