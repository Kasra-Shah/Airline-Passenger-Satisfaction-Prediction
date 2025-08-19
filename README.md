Airline Passenger Satisfaction Prediction
A machine learning classification project to predict airline passenger satisfaction based on service review data. This project was completed as part of an Applied Statistical Analysis course.

![Classification Results](https://github.com/Kasra-Shah/Airline-Passenger-Satisfaction-Prediction/raw/main/classification-result.png)

📖 Project Overview
In the highly competitive airline industry, maintaining passenger satisfaction is crucial. This project aims to build predictive models that can classify a passenger as either satisfied or dissatisfied based on their flight experience. The goal was to compare parametric and non-parametric classification models to identify the most accurate and efficient one for this task.

The insights from such a model can help airlines identify key areas for service improvement and enhance overall customer satisfaction.

📊 Dataset
The dataset consists of customer satisfaction surveys from a US-based airline from 2014.

Source: [Kaggle - Airline Passenger Satisfaction](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)

Number of Instances: ~130,000 (after cleaning)

Number of Features: 25 (original), 23 after removing irrelevant IDs

Target Variable: satisfaction (satisfied / dissatisfied)

Key Features: Age, Flight Distance, Class, Type of Travel, along with numerous service rating features (e.g., Inflight wifi service, Seat comfort, Food and drink, On-board service) on a scale of 1-5.

🛠️ Models & Methodology
The data was split into Training (80%) and Testing (20%) sets. The training set was further divided for estimation and validation to fine-tune model parameters. Data normalization was applied for distance-based algorithms.

A variety of classification models from two main families were implemented and evaluated:

Non-Parametric Methods:

K-Nearest Neighbors (KNN): Tuned using the K parameter. The optimal value was found to be K=11.

Decision Tree: Tuned using the cp (complexity parameter) and minsplit parameters to find the optimal tree structure.

Parametric Methods:
3. Logistic Regression: Tuned using the classification cut-off point.
4. Linear Discriminant Analysis (LDA): Three models with different variable sets were tested.
5. Non-Linear Discriminant Analysis (QDA): Two models with linear and quadratic terms were tested.
6. Naive Bayes: A model with all features was implemented.

📈 Results & Conclusion
The models were evaluated based on their Misclassification Error on the test set.

Model	Misclassification Error
Decision Tree	0.06342
Linear Discriminant Analysis (LDA)	0.06708
K-Nearest Neighbors (KNN)	0.07091
Naive Bayes	0.15549
Logistic Regression	0.12706
Quadratic Discriminant Analysis (QDA)	0.13185
Conclusion: The Decision Tree model outperformed all other models, achieving the lowest misclassification error. However, the Linear Discriminant Analysis (LDA) model offered a very competitive error rate (0.06708) with the significant advantage of likely being much faster to train and predict. This presents a classic trade-off between pure accuracy and computational efficiency.

🚀 How to Run the Code
This project was implemented in R.

Clone the repository:

bash
git clone https://github.com/Kasra-Shah/Airline-Passenger-Satisfaction-Prediction.git
Open the R Project file in RStudio.

Install required packages: Ensure the following R packages are installed:

r
install.packages(c("tidyverse", "caret", "rpart", "MASS", "class", "e1071"))
Run the R script (classification.R) to reproduce the data cleaning, analysis, and modeling process.

📁 Repository Structure
text
Airline-Passenger-Satisfaction-Prediction/
├── data/
│   └── test.csv  # test dataset
│   └── train.csv # train dataset
├── scripts/
├────── classification.R # Main R script for analysis and modeling
└────── classification_markdown.Rmd # Rmarkdown for better understanding of analyses process
👨‍💻 Author
Kasra Shahriari
Industrial Engineering Student

📜 License
This project is for academic purposes.
