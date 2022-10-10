# PCOS_Classification_Project
Based on levels of certain vitamins, hormone levels and physical activities, predict if a woman may have PCOS

## Objectives: 
1.   Analyse the PCOS dataset [https://www.kaggle.com/datasets/prasoonkottarathil/polycystic-ovary-syndrome-pcos] :heavy_check_mark:
2.   Perform Binary Classification task using following ML Algorithms: **Logistic Regression, SVM, Decision Trees, Random Forest, Naive Bayes and K-Nearest Neighbours** :heavy_check_mark:
3.   Build Neural Network Model to perform Classification task. :heavy_check_mark:
4.   Using the trained Neural Model deploy it using Web Interface. :hourglass_flowing_sand:



## 1. Analysis [PCOS_Dataset_Analysis.ipynb]
1.   **PCOS Women have a majority of Cycle (R/I) based around 4 days**, while non-PCOS Women have a majority of Cycle (R/I) based around 2 days
2.   Cycle Lengths among PCOS women have been recorded to be around **2-8 days**.
3.   The age of PCOS Women range from 20-45 yrs, with majority cases between 25-30 yrs.
4.   **Non-PCOS Women have follicle lengths centered around 5 units**, while **PCOS Women have their follicle lengths centered around 10 units** of measurement.

5.   PCOS Women have a **FSH/LH ratio between -5 to 35**, while non-PCOS women have between 0-59.
6.   PCOS Women have **Vit D3 (ng/mL) levels between -100 to 90** as compared to non-PCOS Women whose Vit D3 (ng/mL) levels are centered around 10 to 70.
7.   PCOS Women have a **PRG(ng/mL) level between 0 to 1**, while non-PCOS women have PRG levels between -0.5 to 1.5
8.   PCOS Women also experience **weight gain, hair-growth, skin-darkening, hair-loss, pimples and craving for fast-foods** after developing PCOS.

## 2. Classification using ML Algorithms [PCOS_Classification.ipynb]
1.   Out of the 6 algorithms used, Naive Bayes performed the best with the **highest accuracy (83.7%)** and **highest precision(94.6%)** in comparison to other models.
       Models | Accuracy | Precision | Recall 
      --- | --- | --- | ---
      *Logistic Regression* | `0.7703` | `0.5178` |  `0.8787`
      *Support Vector Machines* | `0.6666` | `0.3928` |  `0.6666`
      *Decision Trees* | `0.7777` | `0.6250` |  `0.7954`
      *Random Forest* | `0.8222` | `0.6071` |  `0.9444`
      *Naive Bayes* | `0.8370` | `0.9464` |  `0.7361`
      *K-Nearest Neighbours* | `0.6000` | `0.1964` |  `0.5500`
      
3.   After feature selection using Wrapper method (Backward Elimination), 18 best features were selected for training with Naive Bayes model which led to the following results:
      Metric | Score 
      --- | --- 
      *Accuracy* | `0.851852` 
      *Precision* | `0.892857`
      *Recall* | `0.78125`
      
 ## 3. Neural Network Performance [PCOS_CLassification_NeuralNetwork.ipynb]
 Constructed a Neural Network model with PyTorch to classify features into PCOS and Non-PCOS categories.
 The following is the architecture of the Neural Model:
 ![Neural Model Architecture drawio](https://user-images.githubusercontent.com/55905682/194923061-efcabe53-e709-4be5-8d77-a30e4d08f517.png)
 
 The Test Results obtained after the result are as follows:
 
   Class (Yes: 1  / No: 0) | Precision | Recall | F1-Score | Support
   --- | --- | --- | --- | ---
   0 | `0.94` | `0.96` |  `0.95` | 106
   1 | `0.92` | `0.88` |  `0.90` | 56
   Accuracy | - | - | 0.93 | 162
      
 
  ## 4. Web Integration
 (*work in progress*)
