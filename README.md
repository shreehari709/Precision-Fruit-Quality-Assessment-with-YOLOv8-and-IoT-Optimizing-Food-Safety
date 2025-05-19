# Precision-Fruit-Quality-Assessment-with-YOLOv8-and-IoT-Optimizing-Food-Safety
This Project proposes a system YOLOv8-based object detection to assess fruit quality. It enables real-time classification of fruits as fresh, mid, or degraded, supporting automated monitoring to reduce spoilage, improve food safety, and enhance supply chain efficiency.

![train_batch1](https://github.com/user-attachments/assets/b2a49992-4aa6-449e-b929-b3a4f1f6c608)
![train_batch0](https://github.com/user-attachments/assets/f10e7819-2f18-4d43-b9d8-e5c7ce2e0687)
![train_batch31610](https://github.com/user-attachments/assets/f0cf93d1-96af-4771-817d-ae7ae07fc5ec)
![train_batch2](https://github.com/user-attachments/assets/47f50afc-5aa0-430d-be0f-fcde62dcfcab)

#1 Data Collection:
A high-quality, diverse dataset of fruits and vegetables—including bananas, carrots, and apples—was curated to develop a robust model capable of accurately assessing fruit quality across various produce types. All images were captured under controlled conditions to ensure consistency.

#2 Annotation Using CVAT:
The dataset was annotated using the open-source Computer Vision Annotation Tool (CVAT). Each image was labeled into three categories: Fresh (no blemishes or decay), Mid (slight deterioration or discoloration), and Rotten (extensive decay or spoilage). This detailed annotation was critical for effective model training.

#3 YOLOv8 Model Development:
The YOLOv8nano model, known for its speed and efficiency in resource-constrained environments, was selected for real-time fruit quality detection. The model was trained on 1700 images, tested on 100 images, and trained over 300 epochs to achieve optimal performance suitable for deployment on edge and IoT devices.

#4 Detection Mechanism of YOLOv8nano:
YOLOv8nano uses a convolutional neural network (CNN) to detect objects quickly and accurately. It divides an image into a grid, predicting bounding boxes and confidence scores for each cell, alongside class probabilities for categories: Fresh, Mid, or Rotten. The model’s convolutional and pooling layers extract hierarchical features such as color, texture, and shape to identify fruit ripeness. Through backpropagation and gradient descent, YOLOv8nano learns to precisely localize and classify fruits in real-time for effective quality assessment.

#Result Analysis 

#Model Performance Overview
The YOLOv8 Nano model demonstrates robust performance in real-time fruit quality assessment through ethylene monitoring. The evaluation metrics, including precision, recall, and mean Average Precision (mAP), indicate high accuracy in classifying fruits into three categories: Fresh, Mid-quality, and Degraded.


![confusion_matrix](https://github.com/user-attachments/assets/7b910037-32e3-4e29-9605-35af7dc7d449)

#Confusion Matrix Analysis
The confusion matrix provides insights into the model's classification accuracy:

#Fresh Fruit Classification:

True Positives (TP): 469

False Negatives (FN): 23
The model exhibits strong performance in identifying fresh fruits, minimizing misclassifications that could lead to unnecessary food waste.

#Mid-Quality Fruit Classification:

True Positives (TP): 426

False Positives (FP): 114
While the model effectively classifies mid-quality fruits, some fresh fruits are incorrectly labeled as mid-quality, suggesting room for refinement.

Degraded Fruit Classification:
The model shows slightly lower precision for degraded fruits but improves significantly at higher confidence thresholds.

![PR_curve](https://github.com/user-attachments/assets/61b1d87f-cc86-44c0-a3e5-5e776b33fe69)
![PR_curve](https://github.com/user-attachments/assets/fb23a6bf-9898-4b93-b0f3-2d268e9ea1eb)

![R_curve](https://github.com/user-attachments/assets/80f61681-8a60-462d-8f5d-4b65921b704a)

#Precision-Confidence and Precision-Recall Curves
Precision-Confidence Analysis
Fresh Fruits: Maintains high precision (>0.8) even at lower confidence thresholds.

Mid-Quality Fruits: Precision improves from 0.75 to >0.9 as confidence increases.

Degraded Fruits: Precision starts at ~0.6 but rises to ~0.85 at higher confidence levels.

![labels_correlogram](https://github.com/user-attachments/assets/c81f8492-7753-4e6f-b871-b61931f73eb2)


#Precision-Recall Metrics
Class	Precision
Fresh	0.974
Mid	0.934
Degraded	0.961
All	0.956
The high precision values across all classes validate the model's effectiveness in distinguishing between fresh, mid-quality, and degraded fruits.

![results](https://github.com/user-attachments/assets/0360a38f-096b-431f-8c7c-15126be79bec)


Training Performance
Epochs: 300

Training Stability: Loss metrics (bounding box, classification, object detection) remained stable.

Consistent Metrics: Precision, recall, and mAP showed minimal fluctuations, indicating reliable performance in both training and validation phases.

Conclusion
The YOLOv8 Nano model proves to be a promising solution for automated fruit quality assessment, with high precision and stable training performance. Further optimizations could enhance mid-quality and degraded fruit classification accuracy.

