### Electrical Fault Detection and Classification

This project uses machine learning to perform electrical fault detection and classification. It leverages data generated from Simulink and is supported by a comprehensive analysis in MATLAB. The primary goal is to apply machine learning methodologies to a real-world problem in electrical power systems.

---

### Motivation & Context

Electrical power systems are prone to various faults that can cause significant damage and power outages. Timely and accurate fault detection is crucial for maintaining grid stability. This project explores the application of machine learning for **automated and precise fault identification** by recognizing patterns in complex electrical data.

Initial algorithm development and comparative analysis were performed using Python. This foundational work provided key insights into the mechanics of different models. The project then transitioned to the MATLAB ecosystem for its seamless integration with Simulink, which was used for robust data simulation, and its efficient environment for machine learning tasks.

---

### Methodology

The project follows a systematic approach, from data generation to model validation:

* **Simulink Data Generation:** An electrical line simulation circuit was designed in Simulink based on methodologies from existing research [1]. This model generates realistic current and voltage data for various fault scenarios.
* **Data Processing:** Raw data from Simulink is processed in MATLAB to create a structured dataset suitable for machine learning.
* **Machine Learning:** The project involves training and comparing various machine learning models for precise fault classification. We used **5-fold cross-validation** to ensure unbiased performance estimates.
* **Performance Evaluation:** Models were evaluated based on key metrics like accuracy and test scores, with confusion matrices used to assess precision and recall for each fault class.
* **Real-time Prediction Simulation:** The best-performing model was tested on new, unseen simulated data to demonstrate its practical application in a diagnostic setting.

---
```text
├── ANN_EE_fault_detection_classification.ipynb               # Python notebook for ANN model.
├── Electrical_fault_detection_simulation.slx                 # Simulink model for fault data generation.
├── README.md                                                 # Project documentation.
├── Random_forest_EE_Fault_classification.ipynb               # Python notebook for Random Forest model.
├── Script_electrical_fault_detection.mat                     # MATLAB file with pre-trained models.
├── classData.csv                                             # Dataset for ML model training.
├── code_electrical_fault_detection.mlx                       # MATLAB Live Script for main workflow.
└── ensemble_stack_EE_fault_detection_classification.ipynb    # Python notebook for ensemble model.
```
---

### Features & Key Components

* **Simulink Model:** `Electrical_fault_detection_simulation.slx` for generating fault data.
* **MATLAB Live Script:** `code_electrical_fault_detection.mlx` for data processing, model training, and prediction.
* **Trained Models:** Pre-trained models (`model_A, model_B, model_C, model_G`) for quick implementation.
* **Dataset:** External dataset from Kaggle [2] used for training the initial models.

---

### How to Run

1.  **Prerequisites:** You need **MATLAB** with **Simulink** installed.
2.  **Download Files:** Clone or download the repository files.
3.  **Get Dataset:** Download the `classData.csv` file from the Kaggle dataset [2] and place it in the project directory.
4.  **Simulate Fault Data:** Open `Electrical_fault_detection_simulation.slx` in Simulink and run the simulation. The generated data will be saved to the MATLAB workspace.
5.  **Process & Predict:** Open and run the `code_electrical_fault_detection.mlx` Live Script. The script will load the `classData.csv` file and pre-trained models, then process the simulated data to make predictions.

The output will display the detected fault based on the following key:
* `[0 0 0 0]` - No Fault
* `[1 0 0 1]` - LG fault (Phase A to Ground)
* `[0 0 1 1]` - LL fault (Phase A to Phase B)
* `[1 0 1 1]` - LLG Fault (Phases A,B to Ground)
* `[0 1 1 1]` - LLL Fault (All three phases)
* `[1 1 1 1]` - LLLG fault (Symmetrical three-phase fault)

---

### References & Acknowledgements

* **Project Mentor:** Dr. Sparsh Mittal, Department of Electronics and Communication Engineering, Indian Institute of Technology Roorkee.
* **Dataset:** [2] E Sathya Prakash. "Dataset on Electrical Fault detection and classification." Kaggle. `https://www.kaggle.com/datasets/esathyaprakash/electrical-fault-detection-and-classification/data`
* **Simulink Methodology:** [1] Jamil, M., Sharma, S.K. & Singh, R. "Fault detection and classification in electrical power transmission system using artificial neural network." SpringerPlus. `https://rdcu.be/eu0yz`
