+  Wine quality can be influenced by a multitude of factors, from the chemical composition and fermentation process to the growing conditions and the winemaking techniques.

+  The project aims to develop a classification system for the "Wine Quality" dataset to predict wine quality using the PCA algorithm and the Bayes Classifier under the assumption of normal(gaussian) distribution. My goal was therefore to observe how many pca components should be applied, but also what was the ideal Train-Test split ratio, in order to obtain the highest accuracy of the classifier.
  
+  The dataset used in this project is "Wine Quality Dataset", which can be downloaded from: https://www.kaggle.com/datasets/yasserh/wine-quality-dataset/data. The classes are unbalanced, containing more normal wines than excellent or poor. The set contains the following properties: fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free and total sulphur dioxide, density, pH, sulphate and alcohol. The output variable is wine quality, rated on a scale from 0 to 10.
  
+  "Principal Component Analysis" is one of the most widely used algorithms for feature extraction, transforming a set of generally correlated variables into a set of uncorrelated values called principal components, thus reducing the dimensionality of the data. This not only simplifies the model, reducing the number of variables to be considered, but also helps to eliminate noise and identify hidden structures in the data.

  The 2D and 3D representations of the dataset using PCA: 
 
   ![image](https://github.com/RalucaVidrasc/WineClassifier/assets/105721568/03e4e927-4162-463c-946b-4a3de6bd89ad)

   ![image](https://github.com/RalucaVidrasc/WineClassifier/assets/105721568/49efdb96-1ef9-4a82-92f6-d70418f33e69)

 
+  After applying the PCA, the next step is to use a classifier to model the relationship between the principal components and the quality of the wine. The Bayes classifier is a popular choice because of its foundation in probability theory and the assumption of conditional independence. Under the assumption of normal distribution, it assumes that the data for each class (wine quality, in this case) are normally distributed and uses this assumption to calculate probabilities. 

+  The Bayes classifier will estimate the parameters of the normal distribution for each class and principal component and use these parameters to calculate conditional probabilities. When presented with a new wine sample, the classifier will use these probabilities to determine the most likely wine quality class for that sample.
     
  The formula used for the discriminant:
![image](https://github.com/RalucaVidrasc/WineClassifier/assets/105721568/9753aca9-6008-4b04-968f-c0b7074501c2)

where,

    - g𝑘(x) --> the Bayes Classifier score for de data x belonging to the class k
    
    - X --> the data being classified
    
    - μ𝑘 --> the mean of the features for class k
    
    - Σ𝑘 --> the covariance matrix for class k
    
    - P(w𝑘) --> the prior probability of class k 
    
+  The accuracy of the classifier for each of the presented cases was displayed in order to observe the most suitable number of PCA components and the best train-test ratio. The overall accuracy values are generally low, which may be due to the unstructured distribution of the data in the dataset, as there are not enough training examples for each considered class. Then, the accuracy was calculated per class.

+  The correlation matrix shows how strongly pairs of variables are correlated. Values close to 1 or -1 indicate a strong positive or negative correlation and values close to 0 indicate no correlation.
    
+  Individual and Cumulative Explained Variances indicate the percentage of variation in the data that each principal component / all components combined explain in a PCA model.
   
+  The confusion matrix shows, for a specified number of PCA components and Train-Test split ratio how correctly the classification model predicts the true classes. It helps identifying the types of errors the model makes.
