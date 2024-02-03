# Semantic-Segmentation-for-Hyperspectral-Image
Performed Semantic Segmentation on Hyperspectral Images using a Deep Learning model. The Task involved loading Hyperspectral Data, creating RGB images, dividing the data into training and testing sets, applying data augmentation, training a segmentation model, and evaluating the results.

## Data Loading and Visualization
The Hyperspectral data was loaded from MATLAB files (Pavia.mat and Pavia gt.mat). The RGB image was created using bands 29, 19, and 9 corresponding to R, G, and B channels. The original image and ground truth were visualized as RGB and grayscale images, respectively.

Dataset link: https://www.ehu.eus/ccwintco/index.php/Hyperspectral_Remote_Sensing_Scenes#Pavia_Centre_and_University

## Data Preprocessing and Model Building
The hyperspectral data was reshaped into 3D patches, and data augmentation was applied to increase the number of training samples. The model architecture consisted of a convolutional layer, max-pooling layer, and a dense layer with softmax activation. The model was compiled using the Adam optimizer and sparse categorical crossentropy loss.

## Training and Evaluation
The data was split into training and testing sets, with 80% for training and 20% for testing. The model was trained for 2 epochs with a batch size of 32. The model’s performance was evaluated using metrics such as accuracy, precision, recall, and f-measure. Additionally, a confusion matrix was generated to visualize the classification results.

## Results
The semantic segmentation model achieved an overall accuracy of 95% on the hyperspectral image dataset. The model performed exceptionally well in classifying pixels belonging to class 1, with a precision of 96%, recall of 98%, and an F1-score of 97%. This indicates a robust ability to identify the dominant
class in the dataset. However, the model’s performance varies across other classes. For classes 3-10, the precision, recall, and F1-score are notably lower, indicating challenges in accurately classifying pixels belonging to these categories. In particular, the model struggled to recognize classes 3 to 10, where precision, recall, and F1-score are all close to zero. These findings suggest that the model excels in certain classes while facing difficulties in distinguishing pixels of less represented classes. Further analysis and potential model adjustments may be required to enhance performance across all classes. In conclusion, while the model demonstrates high accuracy overall, attention should be directed towards improving its ability to handle minority classes for a more balanced and comprehensive semantic segmentation. Further iterations and optimizations may be explored to address these challenges and enhance the model’s performance on the entire spectrum of classes present in the hyperspectral image dataset.
