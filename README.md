# Lead Score Case Study

## Project Summary - 13-09-2022

### Executive Summary

**Target:**  
To find the potential lead for the company out of all leads.

**Steps:**
1. **Cleaning Data:**  
   - Partial cleaning of the data, replacing null values and irrelevant options.
   - Filtered data to include only leads from India, USA, and UAE.

2. **Dummy Variables:**  
   - Created dummy variables for categorical features.
   - Standardized data using StandardScaler.

3. **EDA (Exploratory Data Analysis):**  
   - Quick EDA performed to check data condition.
   - Outliers in numerical variables were identified and removed.

4. **Train-Test Split:**  
   - Data split into 70% train and 30% test sets with random_state = 100.

5. **Model Building:**  
   - Used Recursive Feature Elimination (RFE) to select top 15 relevant variables.
   - Removed remaining variables based on VIF and p-value criteria.

6. **Model Evaluation:**  
   - Confusion matrix created.
   - Optimum cut-off value determined using ROC curve.
   - Accuracy, sensitivity, and specificity evaluated (approx. 90% each).

7. **Prediction:**  
   - Predicted on the test dataset using an optimum cut-off of 0.42.
   
### Conclusions
- Manual segregation of leads required for nurturing potential customers.
- Model meets CEO's expectations with a target lead conversion rate of approx. 90%.
- Features contributing to lead conversion probability identified.

### Summary
#### Train Set:
- Accuracy: 0.8945
- Specificity: 0.8846
- Sensitivity/Recall: 0.9083
- Precision: 0.8491

#### Test Set:
- Accuracy: 0.8914
- Specificity: 0.8724
- Sensitivity/Recall: 0.9181
- Precision: 0.8358

The model predicts conversion rate well, providing confidence to the CEO in making informed decisions.

### Data Dictionary

| Variable                                | Description                                                                                   |
|-----------------------------------------|-----------------------------------------------------------------------------------------------|
| Prospect ID                             | A unique ID with which the customer is identified.                                           |
| Lead Number                             | A lead number assigned to each lead procured.                                                 |
| Lead Origin                             | The origin identifier with which the customer was identified to be a lead. Includes API, Landing Page Submission, etc. |
| Lead Source                             | The source of the lead. Includes Google, Organic Search, Olark Chat, etc.                     |
| Do Not Email                            | An indicator variable selected by the customer indicating whether they want to be emailed about the course or not. |
| Do Not Call                             | An indicator variable selected by the customer indicating whether they want to be called about the course or not. |
| Converted                               | The target variable. Indicates whether a lead has been successfully converted or not.         |
| TotalVisits                             | The total number of visits made by the customer on the website.                                |
| Total Time Spent on Website             | The total time spent by the customer on the website.                                          |
| Page Views Per Visit                    | Average number of pages on the website viewed during the visits.                               |
| Last Activity                           | Last activity performed by the customer. Includes Email Opened, Olark Chat Conversation, etc.  |
| Country                                 | The country of the customer.                                                                   |
| Specialization                          | The industry domain in which the customer worked before. Includes 'Select Specialization' for customers who had not selected an option while filling the form. |
| How did you hear about X Education     | The source from which the customer heard about X Education.                                    |
| What is your current occupation        | Indicates whether the customer is a student, unemployed, or employed.                          |
| What matters most to you in choosing this course | Indicates the main motivation behind choosing the course.                              |
| Search                                  | Indicates whether the customer had seen an ad in any of the listed items.                     |
| Magazine                                | Indicates whether the customer had seen an ad in any of the listed items.                     |
| Newspaper Article                       | Indicates whether the customer had seen an ad in any of the listed items.                     |
| X Education Forums                      | Indicates whether the customer had seen an ad in any of the listed items.                     |
| Newspaper                               | Indicates whether the customer had seen an ad in any of the listed items.                     |
| Digital Advertisement                   | Indicates whether the customer had seen an ad in any of the listed items.                     |
| Through Recommendations                 | Indicates whether the customer came in through recommendations.                               |
| Receive More Updates About Our Courses  | Indicates whether the customer chose to receive more updates about the courses.               |
| Tags                                    | Tags assigned to customers indicating the current status of the lead.                          |
| Lead Quality                            | Indicates the quality of lead based on data and intuition of the employee assigned to the lead.|
| Update me on Supply Chain Content       | Indicates whether the customer wants updates on Supply Chain Content.                          |
| Get updates on DM Content               | Indicates whether the customer wants updates on DM Content.                                     |
| Lead Profile                            | A lead level assigned to each customer based on their profile.                                  |
| City                                    | The city of the customer.                                                                      |
| Asymmetrique Activity Index             | An index and score assigned to each customer based on their activity and profile.               |
| Asymmetrique Profile Index              | An index and score assigned to each customer based on their activity and profile.               |
| Asymmetrique Activity Score             | An index and score assigned to each customer based on their activity and profile.               |
| Asymmetrique Profile Score              | An index and score assigned to each customer based on their activity and profile.               |
| I agree to pay the amount through cheque| Indicates whether the customer has agreed to pay the amount through cheque.                    |
| A free copy of Mastering The Interview  | Indicates whether the customer wants a free copy of 'Mastering the Interview' or not.           |
| Last Notable Activity                   | The last notable activity performed by the student.                                            |

### Libraries Used
- numpy
- pandas
- matplotlib.pyplot
- seaborn
- sklearn
- statsmodels.api
- warnings

