# Success-Classification-of-Furniture-Products

**Project Objective**

The goal of this project was to classify whether a furniture product listed on an e-commerce platform is likely to be a high seller or low seller, based on features such as:

\* Product title

\* Price

\* Shipping tags (`Free shipping`, etc.)



This predictive system helps e-commerce sellers \*\*optimize product listings and pricing strategies\*\* to increase conversions.



---



**Tools and Libraries Used**



\* Python

\* Pandas, NumPy (data cleaning and manipulation)

\* Matplotlib, Seaborn (visualizations)

\* Scikit-learn (machine learning models \& metrics)

\* TfidfVectorizer (text feature extraction)



---



**Data Cleaning**



-Loaded 2,000 products scraped from AliExpress.

-Dropped duplicates (94 rows) and null values in `originalPrice` and `tagText`.

-Converted `price` from string to float for analysis.

-Final cleaned dataset: \*\*1,906 rows × 4 columns



---



**Target Creation**



A new column `HighSeller` was created:



\* `1` = High seller (≥ 10 units sold)

\* `0` = Low seller (< 10 units sold)



---



**Exploratory Data Analysis (EDA)**



-Most products had free shipping, which strongly correlated with higher sales.

-Price ranged widely, but high-sellers were often in the \*\*mid-price bands (\\$40–\\$120).

\-Common high-selling keywords in product titles included “modern”, “wood”, “drawer”, “compact”.



---



**Feature Engineering**

-AppliedTF-IDF on `productTitle` to convert text into numerical vectors.

-Encoded `tagText` using \*\*LabelEncoder\*\*.

-Final feature set included: price, encoded shipping tag, TF-IDF vectors.



---



**Classification Models**



Two models were trained:



1\. Logistic Regression

2\. Random Forest Classifier



Train-Test Split: 80:20 using `train\_test\_split`



---



**Model Evaluation**



| Metric    | Logistic Regression | Random Forest |

| --------- | ------------------- | ------------- |

| Accuracy  | 100%                | 100%          |

| Precision | 1.00                | 1.00          |

| Recall    | 1.00                | 1.00          |

| F1-Score  | 1.00                | 1.00          |



**Both models achieved perfect classification performance on the test data.**



---



**Business Insights**



-Free Shipping significantly boosts chances of high sales.

-Products within a certain price band (\\$40–\\$120) tend to perform better.

-Titles with key terms like “modern”, “compact”, “storage” increase product popularity.

-This model can help sellers flag potential bestsellers automatically before launch.



---

**Video Presentation Link:**
https://drive.google.com/drive/folders/1Mseb-ayMsD_jdUeRQHfaClCUatWv9L8_?usp=sharing



**Deliverables**



-Cleaned dataset

-Feature-engineered DataFrame

-Two trained classification models

-Visualizations (EDA, feature distributions)

-Final evaluation metrics

-Business recommendations



---



**Conclusion**



This project shows that with minimal features like title, price, and shipping tags, we can accurately classify product success in e-commerce.

It provides a strong foundation for further work in:



-Multi-class popularity prediction

-Integration with product recommendation engines

-Price optimization strategies


