# HMM for Sleep Apnea Detection

🔍 **Project Overview**  
This project explores the use of Hidden Markov Models (HMM) to detect sleep apnea by analyzing ECG signals from polysomnographic data. The study focuses on identifying apnea, hypopnea, and normal breathing events, as well as decoding sleep stages to advance automated diagnosis of sleep disorders.

🌟 **Key Features**  

**Dataset:**  
- **Source**: MIT-BIH Polysomnographic Database  
- **Content**: 80+ hours of polysomnographic recordings, including ECG signals.  
- **Annotations**: Sleep stages (e.g., REM, Stage 1) and breathing events (apneas, hypopneas, no apnea).

**Data Preprocessing:**  
- Bandpass filtering (0.5–50 Hz) applied to ECG signals.  
- Segmented into overlapping windows with standardized numerical feature extraction:
  - Mean, variance, skewness, kurtosis, Shannon entropy, zero crossings, and more.  
- Categorical data encoded numerically; features normalized with StandardScaler.

**HMM Architecture:**  
- Gaussian HMM with six hidden states representing sleep stages.  
- Transition and emission probabilities modeled from feature sequences.  
- Initialized with K-means clustering and trained over 2000 iterations.  

🛠️ **Methodology**  
1. **Data Analysis**:
   - Exploratory and multivariate analysis to uncover feature relationships.  
   - Correlation analysis revealed strong and weak feature dependencies.  

2. **Training & Evaluation**:
   - Synthetic data generation to address class imbalance.  
   - Evaluated on metrics including accuracy, precision, recall, F1-score, and confusion matrices.

📊 **Results**  
- **Respiration Event Classification**:  
  - Overall accuracy: 78.92%.  
  - Best performance for "No Apnea" class (precision: 86%, recall: 52%).  
  - Challenges in classifying rare events like hypopneas (precision: 1%, recall: 83%).

- **Sleep Stage Decoding**:  
  - Accuracy: 65.40%.  
  - Best for Awake and Stage 2; poor for REM and deeper stages.  

🧪 **Conclusions**  
The HMM demonstrates potential for automating sleep apnea detection but faces limitations in handling imbalanced datasets and complex sleep patterns. Improved feature engineering and hybrid modeling could enhance accuracy and reliability.

🚀 **Future Work**  
- Explore advanced feature extraction methods and deep learning integrations (e.g., LSTMs).  
- Incorporate multimodal data like EEG and respiratory signals.  
- Address class imbalance with techniques like GANs for synthetic data generation.  


