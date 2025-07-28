# SYSTEMTRON-Titanic-Survival-Prediction-with-Generative-AI-

Titanic Survivor Prediction using Generative AI  
(Project under SystemTron Internship)

This project demonstrates how we can combine traditional Machine Learning with Generative AI to predict whether a passenger survived the Titanic disaster and generate human-like prediction statements.

Dataset Used:
We used the "train.csv" file from the Titanic dataset. The dataset contains demographic and passenger information such as name, age, gender, ticket class, and whether the passenger survived or not.

Note:
The other files in the dataset - "test.csv" and "gender_submission.csv" - were not used in this project. The test.csv file does not contain survival labels (so it’s not suitable for training), and gender_submission.csv is just a sample submission format for competitions.

Project Workflow:

1. Data Preprocessing:
   - Loaded the dataset using pandas.
   - Dropped irrelevant columns like 'Cabin', 'Ticket', and 'Name' to reduce noise.
   - Handled missing values: filled missing 'Age' values with the median and dropped rows with missing 'Embarked'.
   - Converted categorical variables like 'Sex' and 'Embarked' to numeric using Label Encoding.

2. Feature Selection:
   - Selected useful features for prediction such as:
     - Pclass
     - Sex
     - Age
     - SibSp (Number of siblings/spouses aboard)
     - Parch (Number of parents/children aboard)
     - Fare
     - Embarked
   - These features are used as input for the ML model.

3. Model Training:
   - Used Logistic Regression for binary classification (Survived or Not).
   - Split the data into training and testing sets using train_test_split.
   - Trained the model and evaluated it using accuracy score and classification report.

4. Generative AI Integration:
   - Used Hugging Face's Transformers library.
   - Loaded the 'distilgpt2' model using a text generation pipeline.
   - Created human-readable prediction statements based on model output.
   - For example:
     Input prompt: "Based on the data, this passenger is likely to"
     Output: "Based on the data, this passenger is likely to survive and reach the destination safely."

5. Final Output:
   - The logistic regression model gives a binary prediction (0 or 1).
   - The Generative AI model transforms this into a human-friendly, understandable sentence.
   - This adds explainability to the prediction, making it easier for end-users to understand.

Technologies Used:
- Python
- pandas, numpy
- scikit-learn (Logistic Regression)
- transformers (Hugging Face)
- Jupyter Notebook

Conclusion:
This project is an example of how Generative AI can enhance traditional ML models by providing natural language explanations. It shows how we can build not just accurate, but also user-friendly AI systems. The main ML model does the prediction, while the GPT-2-based model provides a narrative-style response based on the output.

This project was done as part of the SystemTron Internship for Generative AI.
