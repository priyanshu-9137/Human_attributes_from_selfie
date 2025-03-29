# Human Attributes from Selfie
### Overview
The Human Attributes from Selfie project predicts key human attributes, such as age, gender, height, and weight, from a selfie image. This project integrates deep learning models to extract these attributes in two stages:

Age and Gender Prediction: Using DeepFace, a pre-trained deep learning model, to predict the age and gender based on the facial features from the selfie.

Height and Weight Prediction: A custom-built Artificial Neural Network (ANN) model to predict height and weight using facial feature distances (forehead-chin and ear-to-ear distances) and the predicted age and gender.

The system is powered by the DeepFace library for age and gender estimation, and a custom-built dataset and ANN models for predicting height and weight.

### Features
Age Prediction: Predicts the age of a person based on their facial features from the selfie.

Gender Prediction: Predicts the gender of a person from the selfie.

Height Prediction: Predicts the height (in feet) based on age, gender, and specific facial feature distances (forehead-chin and ear-to-ear distances).

Weight Prediction: Predicts the weight (in kilograms) based on age, gender, facial feature distances, and height.

### Dataset
To predict height and weight, we created a custom dataset based on the Celeb-FBI dataset from Kaggle. The dataset includes the following columns:

gender: Gender of the individual (male/female).

forehead_chin: Pixel distance between the forehead and chin.

left_ear_right_ear: Pixel distance between the left and right ears.

height: Height of the individual (in feet).

weight: Weight of the individual (in kilograms).

We calculated the forehead_chin and left_ear_right_ear pixel distances using MediaPipe, a library for face detection and analysis. The idea behind using these pixel distances is based on the Golden Ratio, which remains consistent regardless of the distance between the person and the camera.

### Technologies Used
Python: The programming language used to develop the project.

DeepFace: A deep learning library for facial recognition and attribute prediction, used to predict age and gender.

TensorFlow / Keras: Deep learning frameworks used to build and train the Artificial Neural Network (ANN) models for height and weight prediction.

OpenCV: Used for image processing and detecting facial landmarks.

MediaPipe: Used to calculate facial feature distances (forehead-chin and ear-to-ear).
