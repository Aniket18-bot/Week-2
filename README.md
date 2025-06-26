
# 📌 E-Waste Image Classification — Week 2

This week focuses on building, training, and evaluating a deep learning model to classify e-waste images into categories such as Battery, Keyboard, Microwave, Mobile, Mouse, PCB, Player, Printer, Television, and Washing Machine.

## 🚀 Week 2 Key Tasks

✅ Checked class balance through visualizations of training, validation, and test data distributions using bar plots.  
✅ Applied data augmentation techniques to improve generalization:
- Random horizontal flip
- Random rotation
- Random zoom

✅ Selected **EfficientNetV2B0** as the base model for transfer learning, leveraging pre-trained weights from ImageNet.  
✅ Fine-tuned the model:
- First 100 layers frozen
- Remaining layers trainable  

✅ Added final classification layers:
- `GlobalAveragePooling2D`
- `Dropout`
- `Dense (softmax)`  

✅ Compiled the model using:
- Optimizer: Adam
- Loss: SparseCategoricalCrossentropy
- Metric: Accuracy  

✅ Trained the model using:
- EarlyStopping (patience = 3)
- 5 epochs max
- Batch size = 100  

✅ Evaluated performance:
- Accuracy and loss on the test set
- Confusion matrix
- Classification report (precision, recall, F1-score)
- Accuracy and loss trends visualized over epochs  

## 📊 Model Summary

- **Base model:** EfficientNetV2B0 (transfer learning)
- **Input shape:** (128, 128, 3)
- **Final accuracy:** ~96% on test set  
- **Evaluation tools:** Confusion matrix, classification report  

## 📈 Visualization Outputs

- Class distribution bar charts for each dataset split
- Confusion matrix heatmap
- Training vs Validation Accuracy/Loss curves  

## ⚙️ Resources

- **Dataset:** Custom e-waste images, organized by class folders  
- **Libraries:** TensorFlow, NumPy, Matplotlib, Seaborn  
