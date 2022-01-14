# Solving Donor Choose Problem
> Data source: [Kaggle](https://www.kaggle.com/manasvee1/donorschooseorg-application-screening)

## Short intro about data
DonorsChoose.org receives hundreds of thousands of project proposals each year for classroom projects in need of funding. Right now, a large number of volunteers is needed to manually screen each submission before it's approved to be posted on the DonorsChoose.org website.

The goal of the competition is to predict whether or not a DonorsChoose.org project proposal submitted by a teacher will be approved, using the text of project descriptions as well as additional metadata about the project, teacher, and school. DonorsChoose.org can then use this information to identify projects most likely to need further review before approval.
About the DonorsChoose Data Set

_The features provided in the data are:_
**Feature**                         :	Description
**project_id**           	        :    A unique identifier for the proposed project. Example: p036502
**project_title**                   :	Title of the project
**project_grade_category**          :	Grade level of students for which the project is targeted.
**project_subject_categories** 	    :   One or more (comma-separated) subject categories for the project.
**school_state**                    : 	State where school is located (Two-letter U.S. postal code).
**project_subject_subcategories** 	:   One or more (comma-separated) subject subcategories for the project. 
**project_resource_summary** 	    :   An explanation of the resources needed for the project. 
**project_essay_1**                 : 	First application essay*
**project_essay_2**                 :	Second application essay*
**project_essay_3**                 : 	Third application essay*
**project_essay_4**                 : 	Fourth application essay*
**project_submitted_datetime**      : 	Datetime when project application was submitted. 
**teacher_id**                      : 	A unique identifier for the teacher of the proposed project. 
**teacher_prefix**                  : 	Teacher's title. 
**teacher_number_of_previously_posted_projects**  :  Number of project applications previously submitted by the same teacher.  

**description**                     : 	Desciption of the resource. 
**quantity**                        : 	Quantity of the resource required.
**price**                           : 	Price of the resource required.

Target Label:
**project_is_approved**             : 	A binary flag indicating whether DonorsChoose approved the project. 