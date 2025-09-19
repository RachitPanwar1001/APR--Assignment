# APR--Assignment
“data.csv” is used as dataset which contains the measurements from a digitized image of a fine needle aspirate (FNA) of a breast mass. 
80% data is used for training and 20% data for testing.
Independent variables/ Attributes/ Features:
1. Radius_mean
2. Texture_mean
3. Perimeter_mean
4. Area_mean
5. Smoothness_mean
6. Compactness_mean
7. Concavity_mean
8. Concavepoints_mean
9. Symmetry_mean
10.Fractal_dimension_mean
11. Radius_se
12.Texture_se
13.Perimeter_se
14.Area_se
15.Smoothness_se
16.Compactness_se
17.Concavity_se
18.Concavepoints_se
19.Symmetry_se
20.Fractal_dimension_se
21.Radius_worst
22.Texture_worst
23.Perimeter_worst
24.Area_worst
25.Smoothness_worst
29.Symmetry_worst
30.Fractal_dimension_worst

Dependent variable/ Target Attribute/ Class:
i. “Diagnosis”: (M = malignant, B = benign)

KNN based classification model from scratch is trained on the 
dataset and recommend the best value for K (number of neighbors) and
distance matrix that produces the highest accuracy for test data.
Hyperparameters for Experimentation
● Values of K: 3,4,9,20 and 47.
● Distance Matrix: Euclidean Distance, Manhattan Distance, Minkowski Distance,
Cosine Similarity, Hamming Distance .


Results
<img width="691" height="540" alt="image" src="https://github.com/user-attachments/assets/fcc459f4-cd6c-4da3-858e-e829b3a356ae" />

All results (metric, k) -> accuracy:
euclidean   k= 3  acc=0.965217
euclidean   k= 4  acc=0.965217
euclidean   k= 9  acc=0.982609
euclidean   k=20  acc=0.956522
euclidean   k=47  acc=0.965217
manhattan   k= 3  acc=0.982609
manhattan   k= 4  acc=0.973913
manhattan   k= 9  acc=0.965217
manhattan   k=20  acc=0.956522
manhattan   k=47  acc=0.965217
minkowski   k= 3  acc=0.956522
minkowski   k= 4  acc=0.965217
minkowski   k= 9  acc=0.965217
minkowski   k=20  acc=0.956522
minkowski   k=47  acc=0.947826
cosine      k= 3  acc=0.973913
cosine      k= 4  acc=0.973913
cosine      k= 9  acc=0.991304
cosine      k=20  acc=0.982609
cosine      k=47  acc=0.982609
hamming     k= 3  acc=0.921739
hamming     k= 4  acc=0.930435
hamming     k= 9  acc=0.913043
hamming     k=20  acc=0.904348
hamming     k=47  acc=0.895652


Final Best results: 
Best metric: cosine, Best K: 9, Test Accuracy: 0.991304

Confusion Matrix (rows: actual [0,1], cols: predicted [0,1]):
[[72  0]
 [ 1 42]]

Precision (for class=1/malignant): 1.000000
Recall    (for class=1/malignant): 0.976744
