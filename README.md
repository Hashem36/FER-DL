# FER-DL
Facial Emotions Recognition using Deep-Learning Developed a real-time facial emotion recognition model (Xception, TensorFlow).


### **📂 Data Collection & Preparation**
- **Dataset Sources**:  
  1️⃣ **FER2013** – Large-scale dataset with labeled facial expressions.  
  2️⃣ **CK+ (Extended Cohn-Kanade Dataset)** – High-quality images with emotional annotations.  
  3️⃣ **AugmentedFER** – Augmented dataset based on FER2013 to improve generalization.  

- **Data Transformation**:  
  ✅ Convert images to CSV format, extracting pixel values pixel by pixel.  
  ✅ Normalize pixel values for efficient training.  
  ✅ Structure data into training, validation, and test sets.  

---

### **🏗 Model Architecture**
- **Base Model**: Xception-based convolutional neural network (CNN).  
- **Processing Flows**:  
  ✅ **Entry Flow** – Extracts basic image features using convolutional layers.  
  ✅ **Middle Flow** – Deep feature extraction with separable convolutions.  
  ✅ **Exit Flow** – Final classification using global average pooling & dense layers.  
- **Optimization Features**: Batch normalization, residual connections, dropout layers.  

---

### **🔧 Training Configuration**
- **Data Augmentation**: Rotation, width shift, height shift, zoom, and horizontal flip.  
- **Optimizer**: Adam with adaptive learning rates.  
- **Loss Function**: Categorical cross-entropy for multi-class classification.  
- **Checkpoints**: Automatic saving of best-performing models.  

---

### **🚀 Model Training**
- **Multi-Stage Training Strategy**:  
  ✅ Initial phase with **learning rate = 0.001** (100 epochs).  
  ✅ Fine-tuning with **learning rate = 0.0001** (30 epochs).  
  ✅ Final optimization with **learning rate = 0.00001** (20 epochs).  
- **Batch Size**: 64 images per training iteration.  

---

### **📊 Performance Evaluation**
- **Prediction Analysis**: Model processes test images and generates emotion labels.  
- **Evaluation Metrics**:  
  ✅ **Confusion Matrix** – Visualizes correct vs. incorrect predictions.  
  ✅ **Classification Report** – Provides precision, recall, and F1-score per emotion class.  
- **Visualization Tools**:  
  ✅ Heatmap for confusion matrix (Seaborn).  
  ✅ Accuracy & loss plots over epochs (Matplotlib).  

---

### **💾 Model Deployment & Saving**
- **Model Export**: Saves trained model as `.h5` file for future use.  
- **Inference Capability**: Can make real-time predictions on unseen facial images.  
- **Potential Applications**: Emotion recognition in AI assistants, security systems, healthcare, and customer sentiment analysis.  

