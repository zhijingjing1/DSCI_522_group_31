# Online Purchasing Intention Predictor

- author: Yazan Saleh
- contributors: Mai Le, Tran Doan Khanh Vu, Jingjing Zhi

A data analysis project for DSCI 522 (Data Science workflows) aiming to predict purchasing intentions of online shoppers.

## Introduction

In this project, the question we are interested in answering is: given visitor pageview and session information data for an e-commerce platform, is the visitor intending to make a purchase or not? This, in essence, is a binary classification problem where the target class, namely intent to purchase, can be `TRUE` or `FALSE`.

With the rising popularity of online shopping, particularly in the wake of the 2020 coronavirus pandemic, there exists a strong growth opportunity for businesses employing e-commerce solutions. While increasing overall traffic to online stores is a critical first step, higher traffic does not always convert into increased sales. Online visitors may exit the site without making a purchase for a variety of reasons including: loading times, website layout, pricing, amongst others.

Therefore, being able to predict purchasing intentions can be a valuable tool because it could potentially allow businesses to implement measures to better capture users with purchasing intention and thus try to convert them into actual revenue generators. Predicting purchasing intentions can also be useful for making more accurate forecasts about the business.

The data set used in this project is the "Online Shoppers Purchasing Intention" dataset provided by the [Gözalan Group](http://www.gozalangroup.com.tr/) and used by Sakar, OC et al. in their 2018 analysis publsihed in [Neural Computing and Applications](https://link.springer.com/article/10.1007/s00521-018-3523-0). The data set was sourced from UCI's Machine Learning Repository (Dua and Graff 2020) at this [link](https://archive.ics.uci.edu/ml/datasets/Online+Shoppers+Purchasing+Intention+Dataset). The specific file used for the analysis found [here](https://archive.ics.uci.edu/ml/machine-learning-databases/00468/online_shoppers_intention.csv). Each row in the data set contains pageview and session information belonging to a different visitor that browsed [Columbia](https://www.columbia.com.tr), an online e-commerce platform based in Turkey. Each row also contains the target class `REVENUE`, a boolean flag indicating whether that user session contributed to revenue or not. Pageview data includes the type of pages that the visitor browsed to and the duration spent on each page. Session information includes visitor-identifying data such as browser information, operating system information as well visitor location and type.

To answer the predictive question stated above, we plan to build a predictive classification model. The data will be split into a training set and a test set based on a 75% and 25% split, respectively. Exploratory Data Analysis (EDA) will be conducted to explore distribution of features and the target class. Feature distributions will be visualized as density plots color-coded by the target class. Target class distribution will be presented as a table showing counts for each class.

Considering this is a binary classification problem, Support Vector Machines (SVM) can be used as the classification algorithm. The hyperparameter k, which indicates the number of nearest neighbors that will be used in the prediction, will be optimized using a cross-validation workflow. The number of folds used will be 10 considering we have a moderately-sized data set of about 12,000 observations. The scoring measure, which will be used to chose optimal k, will be determined based on the results of the EDA and the presence, or lack thereof, of class imbalance.

Once our optimal model and hyperparameters are identified, the model will be re-fitted against the entire training data set. Its performance will then be evaluated on the test set. A few different scoring metrics, such as accuracy and f1 score, will looked at and presented in the final report. A confusion matrix will also be included to visualize the extent of misclassification errors, if any.

## Usage

To replicate this analysis, please follow these steps:

- Clone this GitHub repository
- Create a conda envrionment using the `env.yaml` at the root of this project (or install the dependencies listed within.)
- Run the following commands at the command line/terminal from the root directory of this project:

```bash
#TODO: directions to run download script and render EDA report.
```

## Dependencies

Please see the project dependencies included in the root env.yml file

## License

```
TODO: Include general statement from LICENSE file
```

## References

Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

Sakar, C.O., Polat, S.O., Katircioglu, M. et al. Real-time prediction of online shoppers’ purchasing intention using multilayer perceptron and LSTM recurrent neural networks. Neural Comput & Applic 31, 6893–6908 (2019). https://doi.org/10.1007/s00521-018-3523-0
