# Human vs AI Text Classification

This project tackles the problem of distinguishing **human-written** text from **AI-generated** text. It was developed during a hackathon and explores multiple machine learning approaches to achieve high classification accuracy.

---

## Dataset

- The dataset contains **105,000 text samples**.  
- Two columns:
  1. `text` – the content of the text sample.
  2. `label` – binary label (0 for human-written, 1 for AI-generated).  
- After cleaning, the dataset had **100,386 samples** with balanced labels:
  - 50,986 human-written
  - 49,400 AI-generated

The data was split stratified into **70% training, 15% validation, 15% test** sets.

---

## Methodology

### **1. Feature-based Models**
- **TF-IDF + Logistic Regression**
  - Validation Accuracy: **0.8991**
  - Achieved reasonable performance but had limitations in capturing context.
- **TF-IDF + Linear SVM**
  - Validation Accuracy: **0.9158**
  - Outperformed Logistic Regression by ~1.67%.
  - Selected as the best feature-based model.

### **2. Transformer-based Model**
- **DistilBERT Fine-Tuning**
  - Used the `distilbert-base-uncased` transformer model.
  - Fine-tuned for one epoch on the training set.
  - Achieved **93% accuracy** on validation.
  - High precision (**0.906**) and recall (**0.955**) indicate strong ability to distinguish between human and AI text.

---

## Training Pipeline

1. **Data Cleaning:** Removed duplicates and nulls.  
2. **Train/Validation/Test Split:** Stratified 70/15/15.  
3. **Feature Extraction:** TF-IDF vectorization for baseline models.  
4. **Model Training:**  
   - Logistic Regression  
   - Linear SVM  
   - Fine-tuned DistilBERT  
5. **Evaluation:** Metrics include Accuracy, F1-Score, Precision, and Recall.

---

## Results

| Model                  | Validation Accuracy |
|------------------------|------------------|
| Logistic Regression     | 0.8991           |
| Linear SVM             | 0.9158           |
| DistilBERT (fine-tuned)| 0.9291           |

**Conclusion:** The fine-tuned **DistilBERT model achieved the best performance**, with 93% accuracy, effectively detecting whether a text is human-written or AI-generated.

---

## Usage

The model can be used to classify text samples for **research, content moderation, or educational purposes**. Transformers provide contextual understanding that outperforms traditional TF-IDF-based methods.

---

## Notes

- Some warnings like `UNEXPECTED` and `MISSING` during DistilBERT loading are normal when fine-tuning on a new task.  
- TF-IDF + Linear SVM remains a strong baseline model if lightweight, fast inference is needed.  

---

##Lisence
# Human vs AI Text Classification

This project tackles the problem of distinguishing **human-written** text from **AI-generated** text. It was developed during a hackathon and explores multiple machine learning approaches to achieve high classification accuracy.

---

## Dataset

- The dataset contains **105,000 text samples**.  
- Two columns:
  1. `text` – the content of the text sample.
  2. `label` – binary label (0 for human-written, 1 for AI-generated).  
- After cleaning, the dataset had **100,386 samples** with balanced labels:
  - 50,986 human-written
  - 49,400 AI-generated

The data was split stratified into **70% training, 15% validation, 15% test** sets.

---

## Methodology

### **1. Feature-based Models**
- **TF-IDF + Logistic Regression**
  - Validation Accuracy: **0.8991**
  - Achieved reasonable performance but had limitations in capturing context.
- **TF-IDF + Linear SVM**
  - Validation Accuracy: **0.9158**
  - Outperformed Logistic Regression by ~1.67%.
  - Selected as the best feature-based model.

### **2. Transformer-based Model**
- **DistilBERT Fine-Tuning**
  - Used the `distilbert-base-uncased` transformer model.
  - Fine-tuned for one epoch on the training set.
  - Achieved **93% accuracy** on validation.
  - High precision (**0.906**) and recall (**0.955**) indicate strong ability to distinguish between human and AI text.

---

## Training Pipeline

1. **Data Cleaning:** Removed duplicates and nulls.  
2. **Train/Validation/Test Split:** Stratified 70/15/15.  
3. **Feature Extraction:** TF-IDF vectorization for baseline models.  
4. **Model Training:**  
   - Logistic Regression  
   - Linear SVM  
   - Fine-tuned DistilBERT  
5. **Evaluation:** Metrics include Accuracy, F1-Score, Precision, and Recall.

---

## Results

| Model                  | Validation Accuracy |
|------------------------|------------------|
| Logistic Regression     | 0.8991           |
| Linear SVM             | 0.9158           |
| DistilBERT (fine-tuned)| 0.9291           |

**Conclusion:** The fine-tuned **DistilBERT model achieved the best performance**, with 93% accuracy, effectively detecting whether a text is human-written or AI-generated.

---

## Usage

The model can be used to classify text samples for **research, content moderation, or educational purposes**. Transformers provide contextual understanding that outperforms traditional TF-IDF-based methods.

---

## Notes

- Some warnings like `UNEXPECTED` and `MISSING` during DistilBERT loading are normal when fine-tuning on a new task.  
- TF-IDF + Linear SVM remains a strong baseline model if lightweight, fast inference is needed.  

---

## License

Under the lisence of the author V Sree Kirthana,all right's reserved
