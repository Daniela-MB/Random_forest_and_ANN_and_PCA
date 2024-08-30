## Introduction

Since 2020, COVID-19 has claimed over 7 million lives worldwide, profoundly impacting global public health and the economy. While vaccines were rapidly developed to combat the virus, they have been associated with side effects ranging from mild to severe, including fever, cardiac issues, and, in rare cases. This project uses machine learning to predict the risk of death after vaccination, analyzing VAERS data to identify risk factors like pre-existing conditions.

## Objective
To apply machine learning models (Random Forest and Artificial Neural Networks) to identify factors, such as pre-existing conditions, that may contribute to the risk of death after vaccination.

## Dataset

The data is from the Vaccine Adverse Event Reporting System (VAERS). 

## Project execution

- Synthetic Minority Over-sampling Technique (SMOTE) was used to address class imbalance, and Principal Component Analysis (PCA) was applied to reduce dimensionality and avoid overfitting.
  
- Random Forest was chosen for its robustness in handling imbalanced data and its ability to provide feature importance.

- Artificial Neural Networks was selected for its strength in classification tasks.

- Both models were trained and compared using precision, recall, and F1 scores.
  
## Results

- *Random Forest (RF)*
  - When adjusted with hyperparameters and class balancing (RF-I), showed improvements in recall compared to other methods. However, precision remained low, indicating that while Random Forest could better identify actual death cases, it also produced more false positives.
 
- *Artificial Neural Networks (ANN)*
  - Demonstrated a 2.6-fold reduction in false positives compared to RF-I, resulting in significantly higher precision. Although this improvement in precision led to a decrease in recall, the overall F1 score indicated that the ANN was more effective for this specific task, providing a better balance between precision and recall.
 
## Conclusion

This study concluded that pre-existing conditions, such as illnesses reported on the day of vaccination, were significant factors contributing to the risk of death post-vaccination. ANN emerged as the more suitable model for predicting death risk in this dataset due to its higher precision and reduced false positives.



## References:

Bansal, H., Balamurugan Balusamy, T. Poongodi and Firoz Khan KP (2021). Machine Learning and Analytics in Healthcare Systems. CRC Press.

Bishop, C.M. (2006). Pattern Recognition and Machine Learning. Springer.

Garg, A. 2023. COVID-19 World Vaccine Adverse Reactions. [online] Available at: https://www.kaggle.com/datasets/ayushggarg/covid19-vaccine-adverse-reactions. [Accessed 15 Nov. 2023].

Khuroo, M.S., Khuroo, M., Khuroo, M.S., Sofi, A.A. and Khuroo, N.S. (2020). COVID-19 Vaccines: A Race Against Time in the Middle of Death and Devastation! Journal of Clinical and Experimental Hepatology. doi:https://doi.org/10.1016/j.jceh.2020.06.003.

Müller, A. C. and Guido, S. (2017). Introduction to machine learning with Python: a guide for data scientists. 1st ed. United States of America. O’reilly Media.

Scikit-learn.org. (2012). 3.2. Tuning the hyper-parameters of an estimator — scikit-learn 0.22 documentation. [online] Available at: https://scikit-learn.org/stable/modules/grid_search.html [Accessed 19 Nov. 2023].

World Health Organization (2023). WHO COVID-19 dashboard. [online] World Health Organization. Available at: https://covid19.who.int/.
