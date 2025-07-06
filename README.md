# Alarming System for Energy Theft Detection Using Deep Learning 

> **A prototype system to detect and alert energy theft in smart grids, combining ANN-based anomaly detection with hardware alarms.**

## Overview 

This project demonstrates a deep learning–powered alarming system that detects electricity theft in smart grids by analyzing consumption patterns. It leverages an Artificial Neural Network (ANN) to classify anomalies and activates an alarm (LED) on detection. It’s implemented as a prototype on Raspberry Pi hardware, making it a practical starting point for real-world deployments.

**Prediction accuracy achieved:** \~76%




## Objectives 

* Detect energy theft accurately using ANN models trained on real smart meter data. 
* Minimize false positives to reduce unnecessary alarms. 
* Provide a working prototype integrating software and hardware (alarm/LED). 
* Contribute towards sustainability by mitigating theft losses. 

## Dataset 

* **Source:** Irish Social Science Data Archive (ISSDA) — Smart Meter Readings Dataset.
* Includes real household and business electricity consumption data.
* Anomalous (theft) data was generated synthetically using controlled randomization & statistical methods.

## Methodology 

1. **Data Preprocessing**

   * Decoded smart meter time-series data.
   * Aggregated daily consumption and generated anomaly classes (C1, C2, C3).

2. **Clustering**

   * Used K-Means to handle unlabeled data and identify pattern clusters.
   * Elbow method determined optimal number of clusters.

3. **Deep Learning**

   * ANN with 4 dense layers, trained to distinguish normal and anomalous data.
   * Evaluated using confusion matrix & precision-recall metrics.

4. **Hardware Integration**

   * Raspberry Pi configured to run the trained model.
   * GPIO controls an LED acting as the “alarm” when theft is detected.

## Hardware Setup 

* Raspberry Pi (with Raspbian OS)
* Breadboard, LEDs, resistors, jumper wires
* SSH + VNC for Pi control
* GPIO pins configured to trigger output based on model predictions

## Results 

* Model accuracy: **76%**
* Low false positive rate
* Responsive LED indicator prototype
* Demonstrated feasibility of real-time deployment in smart grid environments

## Scope for Future Work 

1. Incorporate larger, more diverse datasets  
2. Experiment with advanced models like LSTM/GRU for time-series forecasting 
3. Integrate IoT devices for real-world grid deployment 
4. Collaborate with utilities for pilot testing 



---

### Reproducibility:  

If you clone this project and try to run it, make sure you have:

* Python ≥ 3.7
* `scikit-learn`, `numpy`, `pandas` installed
* Raspberry Pi properly set up with SSH/VNC and GPIO permissions


