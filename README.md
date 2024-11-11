**ASL_Fingerspelling**


**Custom Test Dataset:**
https://drive.google.com/drive/folders/1E7TX1gVHsRFBa65q_ODwo_zgHHfTHXAa?usp=sharing

**Description**
**Custom Model**
Custom Test Model folder includes 4 iPython Notebooks:

**Data extraction** - To extract Mediapipe landmarks and save in .txt file
**ASL_Training** - Training the FFNN on the data stored in .txt
**Livedemo** - Live webcam demo
**CustomEvaluation** - Reporting metrics for custom test dataset
There are 10 .txt files that store the data required to pass into FFNNs.

Train_X_aug, Train_Y_aug : Extracted data from Augmented YOLO dataset
Valid_X_yolo, Valid_X_yolo: Validation from Augmented YOLO dataset
Test_X_yolo, Test_Y_yolo: Test Dataset from Augmented YOLO dataset
Megalist, Maegalabel: Webcam Dataset landmarks file and corresponding labels
custom_test_data_mp, custom_test_labels = Mediapipe landmarks for custom test data and the corresponding labels
There are 3 .h5 files that store the model weights for the FFNN model.

bigdataASLNN26 : Weights for Model 3, trained on large but erroneous dataset
augdata_2layer : Weights for Model 2, trained on the augmented YOLO dataset
wcdata_2layers : Weights for Model 1, trained on the Webcam dataset
Note: The combined Model does not have a separate .h5 file. It post-processes the output of the three models and chooses the output accordingly.

