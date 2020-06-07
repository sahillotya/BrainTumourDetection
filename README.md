Methodology:
BRAIN TUMOR DETECTION USING CNN MODEL
 
About DataSet:
The dataset contains 2 folders: yes and no which contains 253 Brain MRI Images. The folder yes contains 155 Brain MRI Images that are tumorous and the folder no contains 98 Brain MRI Images that are non-tumorous. You can find it here.
Dependencies:
We will be using following libraries of python 3.
1.	Keras
2.	Sklearn
3.	Cv2
4.	Imutils
5.	Numpy
6.	Matplotlib.pyplot
 Dataset Preparation:
1.	Download the dataset from the link here.
2.	 Upload it on google drive inside the collab folder 
3.	 Then mount the drive on the google collab
4.	The github repository is given  for data preparation and Training the model: 
Data Augmentation:
As limited data was available, we have used data augmentation i.e. that enables practitioners to significantly increase the diversity of data available for training models, without actually collecting new data.
Data augmentation techniques such as cropping, padding, and horizontal flipping are used and implemented through augment_data function.
Before data Augmentation:
	It consists of 253 brain MRI image, 155 were brain tumour positive and 98 were negative.
After data augmentation:
	It consists of 2065 brain MRI image, 1085 were brain tumour positive and 980 were negative.
We have augmented in such a way to balance the dataset.
Data Preprocessing:
We have cropped the image in such a way that only brain boundary part should come using Finding extreme points in contours with OpenCV this method.
 
Then we have load the data and split it into.
1.	70% of the data for training.
2.	15% of the data for validation.
3.	15% of the data for testing.
Layers of the Model:
We have buid the model with layers of
1)	Zeropadding
2)	Conv ->BN ->RELU->activation 2
3)	Maxpooling 


After training the models in the chunk of epochs 10+3+3+3+5 we have generated the accuracy of 89.9 for test dataset.
 
The best model gives the accuracy and f1 score as: 90% and 0.90 for test case .
 
