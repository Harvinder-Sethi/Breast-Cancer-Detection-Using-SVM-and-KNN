# Breast-Cancer-Detection-Using-SVM-and-KNN

This project is all to explore cancer and healthcare data, making the predictions from the data, classifying whether the patient has cancer or not, if so what are the Traits observed (Features), So as the government and doctors can be more aware of the information and take measures ahead of time. I believe that the role majorly includes classification problem and classification is a supervised learning approach in which the computer program learns from the input data (Training) and then uses this learning to classify new observations(Testing). The data may simply be bi-class (like identifying whether the result is true or false etc..) or it may be multi-class.
There are 10 features (which the doctors considered to be kept in mind if they are checking for breast cancer) and 1 target column (class), which is the label that tells the patient is benign if 2(not prone to cancer) or malignant if 4 (prone to cancer).

The data column names are briefly described below:-
1. Sample code number id number
2. Clump Thickness 1 - 10
3. Uniformity of Cell Size 1 - 10
4. Uniformity of Cell Shape 1 - 10
5. Marginal Adhesion 1 - 10
6. Single Epithelial Cell Size 1 - 10
7. Bare Nuclei 1 - 10
8. Bland Chromatin 1 - 10
9. Normal Nucleoli 1 - 10
10. Mitoses 1 - 10
11. Class: (2 for benign, 4 for malignant)

As our problem is of classification of breast cancer, whether malignant or benign. I used two algorithms namely SVM (Support Vector Machine) which will help us find the linear separation between these two above groups. The second algorithm I used is KNN (K-Nearest Neighbour) this algorithm takes a bunch of labeled points and uses them to learn how to label other points. To label a new point, it looks at the labeled points closest to that new point (those are its nearest neighbors). Closeness is typically expressed in terms of a dissimilarity function. Once it checks with ‘k’ number of nearest neighbors, it assigns a label based on whichever label most of the neighbors have and then classifies them into malignant or benign. Choosing K value wisely is really important, I tuned the model at different k values and other parameters and whichever gives the highest accuracy and doesn’t contribute to Overfitting was selected in my case k=5 gives the highest accuracy. While Comparing both of them SVM proves to be more robust and accurate giving 98% accuracy while the KNN was giving 97%.
After testing both KNN and SVM Model and getting the accuracy as 97% and 98% respectively, I did their comparison firstly, by coding the classification report and an and I found out that Precision, recall and F1 uses positives and negatives to measure models accuracy when making predictions. It depends on the problem statement which one to consider best, as in this scenario I would focus on “Recall” as I don’t want my model to predict the “Cancer-Prone Patients as No-Cancer”, Rather I can take the risk of accepting low Precision i.e. predicting “Non-Cancer Prone patients as Cancer- Prone”. While the F1 score is the balance of these two as it can be useful if there are very high precision and low recall or vice-versa.

Dataset Link:- https://www.kaggle.com/roustekbio/breast-cancer-csv

NOTE:- You can download the .ipynb and the dataset and run it using jupyter Notebook.
