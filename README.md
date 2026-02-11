# InjuriesClassifier
A model that classifies injuries based on images to three categories:

Overview:

This project focuses on building a deep learning model that can analyze images of injuries and classify their severity into three categories: minor, moderate, and severe. The idea is to teach the model to recognize visual patterns associated with injury seriousness and then apply that knowledge to new, unseen images.

Dataset:

The model is trained on a dataset of labeled injury images, where each image is assigned one of the three severity levels. The dataset is split into training and validation sets so that the model’s performance can be evaluated during training and overfitting can be avoided.

Training Process:

During training, the model learns from the training data while its performance is continuously evaluated on the validation set. Model checkpoints are saved throughout this process, allowing the best-performing version of the model to be retained based on validation results. This makes it possible to stop training early or return to the most reliable checkpoint if needed.

Prediction and Inference:

After training, the model is used to predict the severity of injuries in new images that were not part of the dataset. These predictions assign each image to one of the three severity classes based on what the model has learned.

Test-Time Augmentation:

To improve the stability and robustness of predictions, Test-Time Augmentation (TTA) is applied during inference. Multiple augmented versions of the same image are passed through the model, and their predictions are combined. This helps reduce sensitivity to variations in image orientation, scale, or lighting.

Summary:

Overall, this project implements a complete image classification pipeline, from training and validation to checkpointing and robust inference using TTA. The emphasis is on building a model that not only performs well on the dataset but also generalizes effectively to real-world injury images.
