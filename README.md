# DogOS-Quest Dataset

## Overview
This dataset captures EEG recordings and behavioral data from Snow's gunpowder detection training sessions. The recordings provide insights into neural and behavioral responses as Snow differentiates between target and non-target odors.

---

## Dataset Structure

### **EEG Data**
- **File Prefix:** `Explore_84CF_ExG_ExG_stream`
- **Description:** Contains EEG recordings during the detection sessions.
- **Details:**
  - 8 channels: `Fz`, `Cz`, `T3`, `T4`, `P3`, `P4`, `FP1`, `FP2`
  - Sampling rate: 1000 Hz
  - Timestamps for synchronization

---

### **Sniffing Behavior Data**
- **Description:** IR sensor data capturing Snow's sniffing activity.
- **Details:**
  - 8 columns representing scent ports.
  - **Values:**
    - `1`: Port being sniffed.
    - `0`: No sniffing activity.

---

### **Marker Data**
- **File Prefix:** `Explore_84CF_Marker_Markers_stream`
- **Description:** Contains event markers for the detection sessions.
- **Details:**
  - `sw1`: Positive marker. Timestamp aligns with the onset of a sniffing event.
  - `sw2`: False positive marker (not relevant to the task).

---

### **Calibration Data**
- **File Prefix:** `calibration`
- **Description:** Baseline EEG recordings taken during rest state before detection sessions.
- **Purpose:** The calibration data is used to perform Artifact Subspace Reconstruction (ASR), a preprocessing technique to remove artifacts and noise from EEG signals, ensuring cleaner and more reliable data for analysis.

---

### **ORN Data**
- **Description:** Captures inbuilt IMU data from the EEG amplifier.

---

## **Time Synchronization**
- **Methodology:** Lab Streaming Layer (LSL)
- **Purpose:** Ensures all data streams (EEG, IR sensors, markers) are synchronized to the same clock.
- **Outcome:** Maintains precise temporal alignment across all recordings.

---

## Your Mission, If You Choose to Accept...
The goal is to explore and analyze the dataset to develop a machine-learning model capable of distinguishing between **target sniffs** (positive marker: `sw1`) and **non-target sniffs**. 

### Steps to Accomplish:
1. **Exploratory Data Analysis (EDA):**
   - Understand the relationships between EEG patterns, sniffing behavior, and marker events.
   - Visualize EEG activity across different sessions.
   - Correlate IR sniffing behavior with EEG responses.

2. **Preprocessing And Feature Engineering:**
   - Preprocess and extract meaningful features from EEG and sniffing activity. ( maybe try multi-modal data fusion)

3. **Model Training:**
   - Develop and train a classifier to identify target sniffs using:
     - EEG channels.
     - Sniffing activity.
   - Evaluate model performance using metrics like accuracy, precision, recall, and F1 score.

4. **Submission and Evaluation:**
   - Save your trained model and related code to a **Google Drive folder**.
   - Email the folder link along with documentation (model architecture, preprocessing steps, evaluation metrics, etc.) to **engineering@dognosis.tech** for testing. (would be nice if its a colab/ipynb)

---

### **Hidden Test Dataset**
- We will evaluate your model's performance using a **hidden dataset**. 
- This ensures robust evaluation and prevents overfitting to the provided dataset.
- Submit your model in a form that can process the hidden dataset in the same way it handles the provided dataset.

---

## Contact
For any questions or support, reach out to **engineering@dognosis.tech**.
