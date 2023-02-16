# Credit_Risk_Analysis

## Overview of Project

### Purpose and Background
The purpose of this project is to employ different techniques to train and evaluate models with unbalanced classes. I am using imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling to predict credit risk and determine which sampling method should be used for analyzing this data. 

### Results
- The first sampling model used to analyze the data was the Random Oversampler Model. In using this model we can see that the precision for the predicion of high and low risk loan approvals are greatly unlines with one another. You can also see this reflected in the f-1 score. However, the sensitivity for the two are closely inline. With the precision being off so greatly and the recall being low for both risk types I don't believe we can trust a model like this one to analyze the data as it doesn't appear to have a highly likelyhood of returning an accurate predicion of the data. 

<img width="816" alt="Screen Shot 2023-02-16 at 5 35 24 PM" src="https://user-images.githubusercontent.com/80222506/219503561-5a5dbde1-c2aa-4637-8204-1120d600b0b1.png">

- Similar results were provided for the SMOTE Oversampling and undersampling models. Featured sequentailly below. 
<img width="643" alt="Screen Shot 2023-02-16 at 5 43 54 PM" src="https://user-images.githubusercontent.com/80222506/219503917-0267a7fd-607d-4f90-8ebe-fa8029963f13.png">
<img width="756" alt="Screen Shot 2023-02-16 at 5 44 43 PM" src="https://user-images.githubusercontent.com/80222506/219503948-828b5398-ce9d-40a4-8021-2d5e86b7b09f.png">

- The next model used was the Balanced Random Forest Classifier. The precision for prediction is variant; however, the recall for the two are both above 50, which means that there will be a low change of false negatives. The f-1 score is also quite variant and depicts that the true positive rate for the high_risk loan applicants is very low. Since these individuals will be what need to be considered most, inacurately depicting this information has the potential to be detrimental to the company. 

<img width="681" alt="Screen Shot 2023-02-16 at 5 49 41 PM" src="https://user-images.githubusercontent.com/80222506/219505836-120d237b-6587-456e-a466-7aa1a5677ef4.png">

- Finally the Easy Ensemble Classifier was used. The precision and f-1 measures are similar to the previous tests above, but one difference is the recall. 

<img width="727" alt="Screen Shot 2023-02-16 at 5 49 48 PM" src="https://user-images.githubusercontent.com/80222506/219505923-594be8dc-b200-4327-9ff8-67d6b960f41a.png">

### Summary
In summary, the first three models most likely will not be the best for determining credit risk and avoiding incorrect approvals because their precisions and f-1 are so vairant and won't be good at predicting this information. I also believe that because of this their accuracy will be low as well. 
