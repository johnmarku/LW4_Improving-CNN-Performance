# LW4_Improving-CNN-Performance

Google Colab (https://colab.research.google.com/drive/11TM5mp2acsh3iTxDYLvDhhXVIExGI4i3?usp=sharing)

# **GUIDE QUESTIONS (Student Explanation & Reflection)**

## **A. Model Evaluation Analysis**

**1. What were the weakest-performing classes based on the confusion matrix?**
**ANS:** Based on my SeaWeeds 20 Categories, the weakest-performing classes are:

* Chaetomorpha (40)
* CladophoraRupestris (40)
* CodiumFragile (44)

---

**2. How did Precision, Recall, and F1-score vary across classes?**
**ANS:** Precision, Recall, and F1-score are identical (1.00) for all classes, meaning there are no differences between them.

---

**3. What does a low recall indicate in your model?**
**ANS:** A low recall indicates that the model is missing some actual instances of a class. However, in this case, recall is 1.00 for all classes, so the model does not miss any instances.

---

**4. How does AUC score reflect model performance compared to accuracy?**
**ANS:** AUC (Area Under the ROC Curve) measures how well the model can distinguish between classes across all thresholds, while accuracy measures the percentage of correct predictions at a single threshold. Accuracy shows how often the model is correct, while AUC shows how well the model separates classes regardless of threshold.

---

## **B. Model Improvement**

**5. How did data augmentation affect validation accuracy?**
**ANS:** At the beginning, the validation accuracy was very low (around 0.1). After applying data augmentation, it rapidly increased within the first few epochs and reached close to 1.0 (100%). It then remained stable and closely followed the training accuracy. This shows that data augmentation improved validation accuracy and model generalization.

---

**6. Why is Batch Normalization important in CNNs?**
**ANS:** Batch Normalization is important because it stabilizes and speeds up training by normalizing the inputs of each layer. It reduces internal covariate shift, allowing the network to learn more efficiently.

---

**7. What role did Dropout play in improving your model?**
**ANS:** Dropout helps prevent overfitting by randomly disabling neurons during training. As a result, it reduces overfitting, improves generalization to validation/test data, and makes the model less sensitive to noise.

---

**8. How did Early Stopping prevent overfitting?**
**ANS:** Early Stopping prevents overfitting by monitoring validation performance during training. When the validation loss stops improving or starts to worsen, training is automatically stopped to avoid memorizing the training data.

---

## **C. Performance Comparison**

**9. What improvements were observed after modifying the model?**
**ANS:** After modifying the model, significant improvements were observed. Validation accuracy increased to nearly 100%, and loss values dropped close to zero. Training and validation curves became closely aligned, showing better generalization and reduced overfitting. Precision, recall, F1-score, and AUC also reached very high values.

---

**10. Which enhancement contributed the most to performance improvement? Why?**
**ANS:** Data augmentation contributed the most to performance improvement because it significantly increased validation accuracy from very low values to nearly 100%. It helped the model learn from more diverse and realistic training data, improving generalization.

---

**11. Did the gap between training and validation accuracy decrease? Explain.**
**ANS:** Yes, the gap between training and validation accuracy decreased. This means the model performed more similarly on both training and validation data. It shows that overfitting was reduced and the model generalized better to unseen data.

---

## **D. Explainability (Grad-CAM Integration)**

**12. How did Grad-CAM help in understanding model predictions?**
**ANS:** Grad-CAM helped by showing which parts of the image the model focused on when making a prediction. It generates a heatmap that highlights important regions, making it easier to understand the model’s decision and improve interpretability.

---

**13. Did the improved model focus on more relevant regions? Provide evidence.**
**ANS:** Yes. Based on my Grad-CAM result (OARWEED), the model focuses more on the important parts of the image. The highlighted regions show that it now pays attention to the object instead of irrelevant background areas.

*(Insert Grad-CAM images here)*

---

**14. Why is explainability important in real-world AI applications?**
**ANS:** Explainability is important because it helps us understand how the model makes decisions. It builds trust by showing why a prediction is made instead of just giving an output. It is also important for identifying errors and improving model performance, especially in critical areas like healthcare and finance.


