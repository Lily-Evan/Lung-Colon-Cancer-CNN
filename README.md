# Lung-Colon-Cancer-CNN
🧠 AI-Powered Cancer Detection from Medical Images (98.6% Accuracy)
Using Convolutional Neural Networks (CNNs) to Detect Lung and Colon Cancer from Histopathology Images

🔍 Project Overview
This project builds an AI model that can look at microscope images of human tissue and determine whether the tissue is healthy or cancerous. It focuses on lung and colon tissues—two of the most common types of cancer.

The model was trained on 25,000 real medical images, labeled by professionals, and achieved a remarkable 98.6% accuracy on unseen data.

👨‍⚕️ Why It Matters
Pathologists often examine tissue under a microscope to identify cancer. This process is:

Time-consuming

Prone to human error

Hard to scale

With this AI solution, we can support medical professionals by:

Speeding up diagnosis

Providing a second opinion

Reducing diagnostic errors

🔬 Step-by-Step Breakdown of What the Code Does
1. Load the Dataset
The dataset used is LC25000, which includes:

Colon Adenocarcinoma (cancer)

Colon Normal (healthy)

Lung Adenocarcinoma (cancer)

Lung Squamous Cell Carcinoma (cancer)

Lung Normal (healthy)

A total of 25,000 images are organized and labeled accordingly.

2. Organize the Data
File paths and labels are stored in a table (DataFrame).

Data is split into Training (80%), Validation (10%), and Test (10%) sets using stratified sampling (equal class distribution).

3. Prepare the Images
All images are resized to 224×224 pixels and normalized.

Data generators are created for each dataset split to efficiently load and preprocess images during training.

4. Build the AI Model
A deep CNN is built using TensorFlow/Keras.

It includes:

13 Convolutional layers

5 MaxPooling layers

3 Fully Connected layers

The model uses ReLU activations, Adamax optimizer, and categorical cross-entropy loss.

5. Train the Model
The model is trained for 20 epochs.

Training and validation accuracy/loss are plotted to monitor progress.

It reaches up to 99.08% validation accuracy and 99.87% training accuracy by the final epoch.

6. Evaluate the Model
Final accuracy scores:

🟢 Training Accuracy: 99.87%

🟢 Validation Accuracy: 99.00%

🟢 Test Accuracy: 98.60%

7. Generate Predictions
The model predicts on the test set and compares its output to actual labels.

8. Visualize Results
A confusion matrix is plotted showing how well the model performs per class.

A classification report provides:

Precision

Recall

F1-score

Accuracy per class

9. Save the Model
The trained model can be saved for future use or deployment in real-world diagnostic tools.

