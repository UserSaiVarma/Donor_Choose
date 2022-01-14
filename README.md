# Solving Donor Choose Problem
> Data source: [Kaggle](https://www.kaggle.com/manasvee1/donorschooseorg-application-screening)

## Short intro about data
DonorsChoose.org receives hundreds of thousands of project proposals each year for classroom projects in need of funding. Right now, a large number of volunteers is needed to manually screen each submission before it's approved to be posted on the DonorsChoose.org website.

The goal of the competition is to predict whether or not a DonorsChoose.org project proposal submitted by a teacher will be approved, using the text of project descriptions as well as additional metadata about the project, teacher, and school. DonorsChoose.org can then use this information to identify projects most likely to need further review before approval.
About the DonorsChoose Data Set

_The features provided in the data are:_
- **Feature**                         :	Description
- **project_id**           	        :    A unique identifier for the proposed project. Example: p036502
- **project_title**                   :	Title of the project
- **project_grade_category**          :	Grade level of students for which the project is targeted.
- **project_subject_categories** 	    :   One or more (comma-separated) subject categories for the project.
- **school_state**                    : 	State where school is located (Two-letter U.S. postal code).
- **project_subject_subcategories** 	:   One or more (comma-separated) subject subcategories for the project. 
- **project_resource_summary** 	    :   An explanation of the resources needed for the project. 
- **project_essay_1**                 : 	First application essay*
- **project_essay_2**                 :	Second application essay*
- **project_essay_3**                 : 	Third application essay*
- **project_essay_4**                 : 	Fourth application essay*
- **project_submitted_datetime**      : 	Datetime when project application was submitted. 
- **teacher_id**                      : 	A unique identifier for the teacher of the proposed project. 
- **teacher_prefix**                  : 	Teacher's title. 
- **teacher_number_of_previously_posted_projects**  :  Number of project applications previously submitted by the same teacher.  

- **description**                     : 	Desciption of the resource. 
- **quantity**                        : 	Quantity of the resource required.
- **price**                           : 	Price of the resource required.

Target Label:
- **project_is_approved**             : 	A binary flag indicating whether DonorsChoose approved the project. 

## Content
1. **Eploratory Data Analysis.ipynb**      :    This notebook contains all the exploratory data analysis done on the data and plotted the results for easy understanding.
2. **Data Preprocessing.ipynb**       : This notebook contains all the preprocessing operations performed on all the features of the data.
3. **Naive Bayes.ipynb**    : Perform vectorization using BOW and TFIDF separately and applied Naive bayes on top of it.
4. **Decision Tree and SVM.ipyn**  : Performed vectorization using TFIDF and TFIDFweightedW2V separately on the data and applied Decision tree along with SVM on top of it. 
5. **Gradient Boosted DT**  :  Performed vectorization using TFIDF and TFIDFweightedW2V separately on the data and applied Gradient boosted decision tree on top of it
6. **Results**   : Contains all the result plots for all models

## Results:
1. Applying Naive Bayes:
   -  Using BOW vectorization : 
      -  ![roc](/results/naive_bayes_bow_roc.png)
      -  ![confmat](/results/naive_bayes_bow_ConfMat.png)
   
   -  Using TFIDF vectorization :
      -  ![roc](/results/naive_bayes_tfidf_roc.png)
      -  ![confmat](/results/naive_bayes_tfidf_ConfMat.png)

2. Applying Decision Tree:
   -  Using TFIDF vectorization:
      -  ![roc](/results/dt_tfidf_roc.png)
      -  ![confmat](/results/dt_tfidf_ConfMat.png)
    
   -  Using TFIDF weighted W2Vec:
      -  ![roc](/results/dt_tfidfweighted_roc.png)
      -  ![confmat](/results/dt_tfidfweighted_ConfMat.png)

3. Applying SVM:
   -  Using TFIDF vectorization:
      -  ![roc](/results/SVM_tfidf_roc.png)
      -  ![confmat](/results/SVM_tfidf_ConfMat.png)

4. Applying Gradient Boosted Decision Tree:
   -  Using TFIDF vectorization:
      -  ![roc](/results/gbdt_tfidf_roc.png)
      -  ![confmat](/results/gbdt_tfidf_ConfMat.png)
    
   -  Using TFIDF weighted W2Vec:
      -  ![roc](/results/gbdt_tfidfweighted_roc.png)
      -  ![confmat](/results/gbdt_tfidfweighted_ConfMat.png) 

## Comparision:
| Vectorizer | Model | Hyper Parameter | AUC |
| :---: | :---: | :---: | :---: |
| BOW | Naive Bayes | 0.005 | 0.734 |
| TFIDF | Naive Bayes | 1e-05 | 0.875 |
| TFIDF | Decision Tree | 10-500 | 0.464 |
| TFIDF weighted W2V | Decision Tree | 5-500 | 0.479 |
| TFIDF | Linear SVM | 3.399 | 0.84 |
| TFIDF | GBDT | 100-0.4 | 0.844 |
| TFIDF weighted W2V | GBDT | 100-0.2 | 0.834 |