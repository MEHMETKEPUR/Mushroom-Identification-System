🍄 Mushroom Classification Mobile App
A mobile application that uses a Convolutional Neural Network (CNN) model to classify mushroom species from images. Built using TensorFlow, Flask (for the API), and Flutter (for the front-end), this project aims to educate users about mushrooms and raise awareness about the risks of wild mushroom consumption.

📌 Project Overview
The goal of this project is to create an AI-powered mobile tool that classifies mushrooms from user-submitted images. The model can predict the top five possible species, provide detailed species information, and warn users against consumption without expert verification. While educational, it is not intended to be used for edibility confirmation.

🔍 Features

📷 Image Input: Users can take a photo or select one from their gallery.
🧠 AI-Powered Predictions: The CNN model returns top 5 predicted mushroom species with confidence scores.
📄 Mushroom Info Page: Tapping a prediction opens a page with:

Common name
Species description
Season & habitat
Edibility info
Example photos

🚨 Warning System: If confidence is below 50%, a warning is shown not to rely on prediction for consumption.
🛠 Reporting: Users can report incorrect predictions.
🕓 History: Stores user's past image predictions locally for traceability.

![image](https://github.com/user-attachments/assets/d7d3029f-720f-40cc-af9c-ddabffee5ce7)

                              (main page)

![image](https://github.com/user-attachments/assets/dd3e49d1-328c-43b1-b6ec-87a084a30a3a)

                          (prediction page)
                          
![image](https://github.com/user-attachments/assets/6d40ad40-c653-4ea4-ad66-b1c213fe2493)

                          (Description Page)

🧪 Technologies Used
Technology	Version	Purpose
Python	3.12.3	Backend and Model Training
TensorFlow	2.19.0	CNN Training and Prediction
NumPy	1.26.4	Image preprocessing
Keras	-	Model definition and training
Flask	3.0.2	REST API to serve model
Flutter	-	Cross-platform mobile interface

🗂 Dataset
Source: iNaturalist open-source dataset.
Curated by: Samsun Tarım ve İl Müdürlüğü (Turkey) – “Most Common Mushrooms in Turkey”.

Structure:

26 folders (one for each species).
100 images per class (total: 2600 images).
Image size: Resized to 375×500 in preprocessing.
Note: No text data included, but future versions may incorporate smell, texture, and habitat metadata.

🧠 Model Architecture
Model Type: ResNet50-based CNN.

Training Images: 2080 (80%)
Validation Images: 520 (20%)
Training Epochs: 20
Final Accuracy:
Training: 100%
Validation: 78.46%
Techniques Used:
Data augmentation
Normalization and resizing
Fine-tuning to reduce overfitting

🔁 Workflow

User uploads an image via mobile app
Flutter app sends image to Flask API
Flask preprocesses the image and forwards to TensorFlow model
Predictions are returned (top 5 with confidence)
Flutter app displays results and allows user interaction
