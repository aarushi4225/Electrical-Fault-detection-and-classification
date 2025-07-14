# Electrical Fault Detection and Classification

## Project Overview
Leveraged machine learning for electrical fault detection and classification, powered by Simulink-generated data and comprehensive MATLAB analysis.

---

## Motivation

Electrical power systems are subjected to various faults that can cause significant damage, power outages, and economic losses. Timely and accurate fault detection and classification are important for maintaining grid stability. 

This project explores the application of machine learning as an efficient way to catch such faults, by leveraging machine learning's capabilities for **pattern recognition in complex electrical data** to enable automated and precise fault identification. As an an electrical and electronics student, this project was also a crucial learning experience in applying machine learning methodologies to real-world problems.

---
## Development Context

The initial development and testing of machine learning algorithms for this project were carried out using Python libraries. This foundational work provided a deep understanding of algorithm mechanics through custom implementations, alongside enabling a rigorous comparative analysis of diverse approaches. **The Python-based implementations of the conventionally trained models are available within this repository for further review.** Subsequently, the project transitioned to the MATLAB ecosystem. This shift was motivated by MATLAB's seamless integration with Simulink for robust data simulation, as well as its efficient environment for pre-built machine learning models and streamlined training processes.

---

## Features & Methodology

* **Simulink-based Data Generation:** Designed an Electrical Line simulation circuit using Simulink model (`Electrical_fault_detection_simulation.slx`). This generated realistic current and voltage data related to Fault scenarios.
![Screenshot 2025-07-06 122319](https://github.com/user-attachments/assets/e95520ae-0ab4-47d8-a133-daf209b9b92f)

* **Data Processing (MATLAB):** Raw data generated from Simulink was processed using MATLAB. This included steps such as - arranging the raw numeric arrays into matrices, compilation into readable dataset to be fed into ML model.
* **Machine Learning Model Training:**
    * The project involved training and comparative analysis of various models to achieve precise electrical fault identification.

* Leveraged 5-fold cross-validation to prevent overfitting, providing an unbiased estimate of their performance on unseen data.
* **Performance Evaluation:** Comparison of trained models was conducted using key metrices such as accuracy and test scores and analysis of confusion matrices to assess precision, recall, and overall effectiveness for each fault class.
* **Real-time Prediction Simulation:** The most accurately trained model was successfully utilized to make predictions on newly generated, unseen simulated fault data, demonstrating its practical applicability in a diagnostic setting.

---

## Technologies Used

* **MATLAB R[2023b]**
* **Simulink**

---

## Run this Project

To run this project, you will need MATLAB with Simulink.

### Installation

1. Download the files attached in the repository.
2.  Open MATLAB.
3.  In MATLAB's Current Folder browser, navigate to the directory where files were saved.
4.  **Simulate Fault Data:**
    * Open the Simulink model file: `Electrical_fault_detection_simulation.slx`.
    * Run the simulation to generate the raw current and voltage data. This data will be saved to the workspace.
4.  **Processing Data, Training Models & Predict:**
    * Open and run the MATLAB Live Script: `code_electrical_fault_detection.mlx`. Import below mentioned files and then run the script:
        * First download the trained dataset **classData.csv** from `https://www.kaggle.com/datasets/esathyaprakash/electrical-fault-detection-and-classification/data`.
        * Import the csv file "classData.csv".
        * Import files named [model_A, model_B, model_C and model_G] from `Script_electrical_fault_detection.mat` to the workspace.
        * Now run the Live script. 

---
## Interpretation of the Output Data:
* KEY:
   - A : Phase A
   - B : Phase B
   - C : Phase C
   - G : Ground (GND)
     
* Inferences from Output [G C A B]
   - [0 0 0 0] - No Fault
   - [1 0 0 1] - LG fault (Between Phase A and Gnd)
   - [0 0 1 1] - LL fault (Between Phase A and Phase B)
   - [1 0 1 1] - LLG Fault (Between Phases A,B and ground)
   - [0 1 1 1] - LLL Fault(Between all three phases)
   - [1 1 1 1] - LLLG fault( Three phase symmetrical fault)
---

## References & Acknowledgements

This project and the initial learning phase were conducted under the valuable guidance of **Dr. Sparsh Mittal**, from the **Department of Electronics and Communication Engineering, Indian Institute of Technology Roorkee.**

The project draws insights from existing research on the topic **Electrical fault detection and machine learning**. Specifically, the circuit designs and foundational ideas for simulating fault scenarios were adapted from the following works:

* [1] **Jamil, M., Sharma, S.K. & Singh, R. Fault detection and classification in electrical power transmission system using artificial neural network. SpringerPlus `https://rdcu.be/eu0yz`**
* [2] **Dataset on Electrical Fault detection and classification - E Sathya Prakash`https://www.kaggle.com/datasets/esathyaprakash/electrical-fault-detection-and-classification/data`**
