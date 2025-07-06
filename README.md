# Electrical-Fault-detection-and-classification-with-Machine-learning

## Project Overview
Created a Simulink model for electrical line fault data generation. Utilized MATLAB for data processing, trained diverse ML models, utilized 5-fold cross-validation. Compared model accuracy/confusion matrices, then applied the most accurate model to predict faults on new simulated data.

### Key Highlights:
– Simulated a **Simulink circuit** for electrical line fault data generation. Utilized **MATLAB** for data processing, **training diverse ML models**, and applying **5-fold cross-validation** to avoid over fitting issues. **Compared models through accuracy scores and confusion matrices**, then applied the **most accurate model to predict faults on new simulated data**.

---

## Motivation

Electrical power systems are subjected to various faults that can cause significant damage, power outages, and economic losses. Timely and accurate fault detection and classification are paramount for maintaining grid stability and ensuring rapid restoration. This project explores the application of machine learning as an efficient way to catch such faultss, leveraging its capabilities for **pattern recognition in complex electrical data** to enable automated and precise fault identification. As an an electrical and electronics student, this project was also a crucial learning experience in applying machine learning methodologies to real-world problems.

---

## Features & Methodology

* **Simulink-based Data Generation:** Designed an Electrical Line simulation circuit using Simulink model (`Electrical_fault_detection_simulation.slx`). This generated realistic current and voltage data related to Fault scenarios.
* **Data Processing (MATLAB):** Raw data generated from Simulink was processed using MATLAB. This included steps such as - arranging the raw numeric arrays into matrices, compilation into readable dataset to be fed into ML model.
* **Machine Learning Model Training:**
    * Leveraged **MATLAB's Classification Learner App** for rapid prototyping and training of various machine learning classification models.
    * Explored and compared the performance of diverse algorithms, including [Artificial Neural Networks (FINE KNNs), Random Forests, Support Vector Machines (SVMs), Boosting Algorithms].
* Enabled **5-fold cross-validation** to prevent overfitting, providing an unbiased estimate of their performance on unseen data.
* **Performance Evaluation:** Comparison of trained models was conducted using key metrices such as **accuracy and test scores** and analysis of **confusion matrices** to assess precision, recall, and overall effectiveness for each fault class.
* **Real-time Prediction Simulation:** The most accurately trained model was successfully utilized to make predictions on newly generated, unseen simulated fault data, demonstrating its practical applicability in a diagnostic setting.

---

## Technologies Used

* **MATLAB R[2023b]**
* **Simulink**
* **Classification Learner Feature**

---

## Running this Project

To run this project, you will need MATLAB with Simulink.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/aarushi4225/Electrical-Fault-detection-and-classification-with-Machine-learning.git](https://github.com/aarushi4225/Electrical-Fault-detection-and-classification-with-Machine-learning.git)
    cd Electrical-Fault-detection-and-classification-with-Machine-learning
    ```
2.  **Open MATLAB:** Launch MATLAB application.
3.  **Navigate to the project directory:** In MATLAB's Current Folder browser, navigate to the directory where cloned repository was saved.
4.  **Simulate Fault Data:**
    * Open the Simulink model file: `Electrical_fault_detection_simulation.slx`.
    * Run the simulation to generate the raw current and voltage data. This data will be saved to the workspace.
4.  **Processing Data, Training Models & Predict:**
    * Open and run the MATLAB Live Script: `code_electrical_fault_detection.mlx`. Import the necessary files and then run the script:
        * First download the trained dataset **classData.csv** from `https://www.kaggle.com/datasets/esathyaprakash/electrical-fault-detection-and-classification/data`.
        * Import the csv file "classData.csv".
        * Import files named [model_A, model_B, model_C and model_D] from `Script_electrical_fault_detection.mat` to the workspace.
        * Now run the Live script. 

---

## References & Acknowledgements

This project draws insights from existing research on the topic electrical fault detection and machine learning. Specifically, the circuit designs and foundational ideas for simulating fault scenarios were adapted from the following works:

* [1] **Kaggle Data on Electrical Fault detection and classification `https://www.kaggle.com/datasets/esathyaprakash/electrical-fault-detection-and-classification/data`**
* [2] **Jamil, M., Sharma, S.K. & Singh, R. Fault detection and classification in electrical power transmission system using artificial neural network. SpringerPlus `https://rdcu.be/eu0yz`**

