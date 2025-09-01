# ABSTRACT

## INTELLIGENT EDGE DEVICE FOR REAL TIME CARDIAC ARRHYTHMIA DETECTION
Cardiac arrhythmias, a leading manifestation of cardiovascular disease, often occur
intermittently and unpredictably, necessitating continuous and accurate monitoring
for early diagnosis and timely intervention. 
However, most existing solutions either rely on cloud-based AI processing—raising concerns about latency and privacy, or
are limited to detecting only a narrow class of arrhythmias.
To address this challenge, an intelligent edge device for real-time cardiac arrhythmia detection has been proposed.
This is a **low-power, portable system capable of on-device classification of cardiac arrhythmias using lightweight deep learning models**. 
The device integrates a high-fidelity ECG acquisition front-end (ADS1292R) with an energy-efficient microcontroller (nRF52840) to enable real-time inference without reliance on cloud 
connectivity, thereby ensuring data privacy and reducing latency. 
A compressed **ResNet based model**, trained using **knowledge distillation** and enhanced with adversarial robustness (PR-KDL), performs five-class arrhythmia detection compliant with **AAMI
standards** (N, S, V, F, Q). 
An integrated OLED display provides immediate user feedback, and BLE support enables optional transmission to external devices. 
This work demonstrates the feasibility of deploying clinically relevant arrhythmia detection on resource-constrained embedded platforms, offering a scalable and autonomous
solution for continuous cardiac monitoring in edge-healthcare applications.

---
*Project by: Ridhin Thomas Alex*

*Guided by: Prof. Kiran Boby*
