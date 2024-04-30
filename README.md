# IdentifyingLungCancer_ConvolutionalNeuralNet
By Alice Pascalev and Will Arliss - Utilizing convolutional neural networks to identify Lung Cancer from an image set. (Python)
GWU - Machine Learning I - Summer 2023

The dataset utilized in this project is [Lung and Colon Cancer Histopathological Image Dataset (LC25000)](https://www.kaggle.com/datasets/andrewmvd/lung-and-colon-cancer-histopathological-images), a dataset of 25,000 color images of lung and colon tissue compiled and prepared by Borkowski et al., which we accessed via Kaggle. The 25,000 images are in 5 classes, each containing 5,000 images. The classes are as follows:

Benign Colonic tissue
Colon adenocarcinoma (cancerous)
Benign Lung tissue
Lung adenocarcinoma (cancerous)
Lung Squamous cell carcinoma (cancerous)

The images were generated from an original set of 750 images of lung tissue and 500 images of colon tissue (250 images per class), and augmented to a set of 25,000 (5,000 per class) for public use. All of the data is de-identified, HIPAA compliant, and from verified sources.

For the purpose of this project, we are focusing on the three lung classes - benign lung tissue, lung adenocarcinoma, and lung squamous cell carcinoma.

The motivation behind choosing the dataset on lung cancer stems from a combination of our interests in convolutional neural networks (CNNs) and healthcare applications of data science. CNNs have demonstrated remarkable performance in image recognition tasks, making them well-suited for analyzing medical images. Additionally, lung cancer holds a significant place in healthcare due to its high mortality rate, which ranges from 3% to 65% over 5 years depending on the stage and type. As one of the leading causes of cancer-related deaths, it presents a pressing challenge for the medical community. By leveraging the power of CNNs, we aim to build a model which can distinguish cancerous tissue from healthy tissue, and distinguish between the two types of lung cancer. With aggressive cancers such as lung, colon, and pancreatic cancer, early detection and diagnosis is key to survival. With the advancements in medical imaging and machine learning, early detection with CNNs can save many lives.

Adenocarcinoma is the most common type of lung cancer, accounting for 40% of cases, with incidences rising over the past few decades. It has 10 subtypes. Squamous cell carcinoma accounts for 20% of lung cancers.

The lung tissue dataset consists of 15,000 768 x 768 pixel images distributed equally across three classes. This posed a challenge in Colab, where we were working with limited memory, which resulted in extremely long runtime (and often also causing Colab to crash). To mitigate this, we made the decision to both resize the images to 256x256 (224x224 for pretrained models), and undersample the dataset to 1,200 (1,000 for training, 100 for validation, 100 for testing) to train the model. Because the dataset was previously augmented from 250 images from each class to 5,000 of each class, there are still more images in our dataset than there were originally.
