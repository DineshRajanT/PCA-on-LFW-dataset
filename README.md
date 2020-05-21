# PCA-on-LFW-dataset
Applying PCA on LFW dataset and classifying using SVM

#Implementation steps:

1) We need to first import the scikit-learn library for using the PCA function API that is provided into this library.
The scikit-learn library also provided an API to fetch LFW_peoples dataset. We also required matplotlib to plot faces.

2) Now we import the LFW_people dataset using sklearn’s fetch_lfw_people function API. LFW_prople is the preprocess excerpt of LFW. It contains 13233 images of 5749 classes of shape 125 * 94. This function provides an parameter min_faces_per_person. This parameter allows us to select the classes that have at least min_faces_per_person different pictures. This function also has a parameter resize which resize every image in the extracted face. We use min_faces_per_person = 70 and resize = 0.4
Now, we apply train_test_split to split the data into training and testing sets. We use 25% of the data for testing.

3) Now, we apply train_test_split to split the data into training and testing sets. We use 25% of the data for testing.

4) Now, we apply the PCA algorithm on the training dataset which computes EigenFaces. Here, we take n_components = 150 means we extract the top 150 Eigenfaces from the algorithm. We also print the time taken to apply this algorithm.

5)Now we have the EigenFace and each image is represented by a vector of size 1 * 150. The values in this vector represent the coefficient corresponding to that Eigenface. These coefficient are generated using transform function on the function.

6) Now we use Support Vector Machine (SVM) as our classification algorithm. We train the data using the PCA coefficient generated in previous steps.
