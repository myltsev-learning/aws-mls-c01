Machine Learning Specialist is working with a media company to perform classification on popular articles from the company's website. The company is using random forests to classify how popular an article will be before it is published. A sample of the data being used is below.

| title         | Day_Of_Week |
| ------------- | ----------- |
| test article  | Tuesday     |
| test article2 | Monday      |
| test article3 | Sunday      |
| test article4 | Tuesday     |
Given the dataset, the Specialist wants to convert the Day_Of_Week column to binary values.  
What technique should be used to convert this column to binary values?  

A. Binarization
B. One-hot encoding
C. Tokenization
D. Normalization transformation

My answer: B

---
## Correct Answer

The correct answer is **B. One-hot encoding**.

## Explanation

In the given scenario, the `Day_Of_Week` column contains categorical data (days of the week). To convert categorical data into a format suitable for machine learning algorithms, one-hot encoding is typically used.

One-hot encoding creates a new binary column for each unique category in the original column. Each row is then assigned a value of 1 in the column corresponding to its category and 0 in all other columns. This process effectively transforms the categorical data into a numerical representation that can be used by machine learning models.

For example, after one-hot encoding, the `Day_Of_Week` column could be transformed into multiple binary columns like `Monday`, `Tuesday`, `Wednesday`, etc., where each row would have a 1 in the column corresponding to its day and 0 in the other columns.

The other options are not suitable for this task:

- **A. Binarization**: Binarization is typically used to convert continuous numerical data into binary values (0 or 1) based on a threshold. It is not applicable for encoding categorical data.
- **C. Tokenization**: Tokenization is a technique used in natural language processing to split text data into smaller units (tokens) like words or subwords. It is not relevant for encoding categorical data like days of the week.
- **D. Normalization transformation**: Normalization is used to rescale numerical data to a common range, such as [0, 1] or [-1, 1]. It is not applicable for encoding categorical data.

