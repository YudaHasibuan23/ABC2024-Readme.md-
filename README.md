# FacePsy Dataset: Depression Episode Detection  
This dataset contains facial behavior and head movement data used to predict depression episodes. It includes features such as Action Units (AUs), head movement metrics, and other facial structure indicators.  

---

## Dataset Structure  
The dataset consists of the following columns:  

| Column             | Description                                                   |
|--------------------|---------------------------------------------------------------|
| `AU24`             | Action Unit 24 activation (Lip Pressor)                        |
| `Eye_Open_Avg`     | Average eye openness                                           |
| `Facial_Structure` | Calculated facial structure value based on geometric features  |
| `AU23`             | Action Unit 23 activation (Lip Tightener)                      |
| `AU01`             | Action Unit 01 activation (Inner Brow Raiser)                  |
| `AU07`             | Action Unit 07 activation (Lid Tightener)                      |
| `AU02`             | Action Unit 02 activation (Outer Brow Raiser)                  |
| `AU_Smile`         | Activation value of smile-related Action Unit                  |
| `AU10`             | Action Unit 10 activation (Upper Lip Raiser)                   |
| `AU14`             | Action Unit 14 activation (Dimpler)                            |
| `Head_Movement`    | Head movement value (rotation and translation)                 |
| `AU_Sad`           | Activation value of sadness-related Action Unit                |
| `datetime`         | Date and time of data collection                               |
| `depression_episode`| Binary label: 0 (No episode), 1 (Depression episode)           |
| `pid`              | Participant ID (e.g., P08)                                     |  

---

## Sample Data  
Here is a sample of the dataset:  

| AU24      | Eye_Open_Avg | Facial_Structure | AU23     | AU01      | AU07      | AU02      | AU_Smile  | AU10      | AU14      | Head_Movement | AU_Sad    | datetime            | depression_episode | pid |
|-----------|--------------|-----------------|----------|-----------|-----------|-----------|-----------|-----------|-----------|----------------|-----------|---------------------|--------------------|-----|
| -11.351092 | 0.973326     | 0.567567         | -2.459438 | -11.097750 | 18.764470 | -13.701491 | 1.797318  | -7.621264  | -8.416746  | 0.093635      | 0.861408  | 2022-07-21 04:46   | 0                  | P08 |
| -12.812418 | 0.824679     | 0.584101         | -2.705608 | -8.061482  | 13.727324 | -12.742016 | 1.416385  | -0.372542  | -13.412502 | 0.094856      | 0.250375  | 2022-07-21 04:46   | 0                  | P08 |
| -9.396528  | 0.905175     | 0.609942         | 0.163664  | -5.724306  | 22.029821 | -9.810085  | 1.645429  | -4.372520  | -3.623914  | 0.095847      | 2.480238  | 2022-07-21 04:46   | 0                  | P08 |

# Universal Model Accuracy  

### Overall Evaluation of the KNN Model  

The overall evaluation of the model based on the following metrics:  

| Metric    | Value  |
|-----------|--------|
| Accuracy  | 0.6563 |
| Precision | 0.6303 |
| Recall    | 0.6999 |
| F1 Score  | 0.6183 |
| AUC       | 0.7240 |

### Overall Evaluation of the XGBoost Model  

The overall evaluation of the model based on the following metrics:  

| Metric    | Value  |
|-----------|--------|
| Accuracy  | 0.8167 |
| Precision | 0.8224 |
| Recall    | 0.8351 |
| F1 Score  | 0.7751 |
| AUC       | 0.9155 |

### Overall Evaluation of the Decision Tree Model  

The overall evaluation of the model based on the following metrics:  

| Metric    | Value  |
|-----------|--------|
| Accuracy  | 0.8475 |
| Precision | 0.8138 |
| Recall    | 0.8682 |
| F1 Score  | 0.8206 |
| AUC       | 0.9135 |

### Overall Evaluation of the Naïve Bayes Model  

The overall evaluation of the model based on the following metrics:  

| Metric    | Value  |
|-----------|--------|
| Accuracy  | 0.7291 |
| Precision | 0.6599 |
| Recall    | 0.9410 |
| F1 Score  | 0.7339 |
| AUC       | 0.8821 |



# Hybrid Model Accuracy  

# Classification Report - Stacking Model  

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.88      | 0.87   | 0.88     | 34,022  |
| 1     | 0.86      | 0.88   | 0.87     | 31,131  |
| **Accuracy**  |    0.87    |     0.87    | **0.87**     | 65,153  |
| **Macro Avg** | 0.87      | 0.87   | 0.87     | 65,153  |
| **Weighted Avg** | 0.87      | 0.87   | 0.87     | 65,153  |



## Usage  
Clone this repository:  
    ```bash
    git clone https://github.com/SkylarkOff/Semicolon-Model.git
    ```
