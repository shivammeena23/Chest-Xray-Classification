# 🩺 Chest X-ray Disease Classifier

**Self Project | May ’25 – June ’25**

A deep learning project focused on building an interpretable AI system to detect 14 thoracic diseases from chest X-ray images using multi-label classification. This project automates diagnostic support to enhance clinical workflows and reduce manual interpretation effort, particularly for critical conditions such as **Cardiomegaly** and **Edema**.

---

## 🧠 Objective

- Develop an AI model to detect **14 thoracic diseases** from chest X-ray images.
- Enable **automated diagnostic support** to improve clinical efficiency.
- Focus on **interpretable and accurate detection** of critical abnormalities.

---

## 🛠️ Approach

- ✅ Built on **DenseNet121** with **transfer learning** using 1,400+ X-ray images.  
- 🔁 Designed a robust data pipeline including:
  - Augmentation  
  - Normalization  
  - **Patient-level leakage prevention**
- 📊 Evaluated using **ROC-AUC** for multi-label performance.
- 👁️ Integrated **Grad-CAM** to visualize model focus and improve interpretability.

---

## 📈 Results

- 🎯 Achieved an **average AUC of 0.83** across all 14 disease classes.
- 📉 Improved baseline accuracy by **28%** through **class rebalancing**.
- ⚡ Reduced training time by **60%** using transfer learning.
- ✅ Delivered an **interpretable AI model** suitable for deployment in real-world healthcare workflows.

---

## 🗂️ Dataset

- Chest X-ray images (sourced via Roboflow)  
- Preprocessed into `train`, `valid`, and `test` folders.  
- Two primary classes: `NORMAL` and `PNEUMONIA` for demonstration purposes.

---

## 🚀 Model Architecture

- Backbone: `DenseNet121`
- Classification Head: Fully connected layer with `Sigmoid` activation for multi-label output
- Loss Function: `BCEWithLogitsLoss`
- Evaluation Metric: `ROC-AUC`

---

## 🧪 How to Run

```bash
# Clone the repository
git clone https://github.com/shivammeena23/Chest-Xray-Classification.git
cd Chest-Xray-Classification

# Install dependencies
pip install -r requirements.txt

# Train the model
python train.py

# Evaluate on test set
python evaluate.py
