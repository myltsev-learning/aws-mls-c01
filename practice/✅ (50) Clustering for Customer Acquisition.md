A Marketing Manager at a pet insurance company plans to launch a targeted marketing campaign on social media to acquire new customers. Currently, the company has the following data in Amazon Aurora:  
✑ Profiles for all past and existing customers  
✑ Profiles for all past and existing insured pets  
✑ Policy-level information  
✑ Premiums received  
✑ Claims paid  
What steps should be taken to implement a machine learning model to identify potential new customers on social media?  

A. Use regression on customer profile data to understand key characteristics of consumer segments. Find similar profiles on social media

B. Use clustering on customer profile data to understand key characteristics of consumer segments. Find similar profiles on social media

C. Use a recommendation engine on customer profile data to understand key characteristics of consumer segments. Find similar profiles on social media.

D. Use a decision tree classifier engine on customer profile data to understand key characteristics of consumer segments. Find similar profiles on social media.

My answer: B

---

Absolutely! Option B is the most suitable approach. Here's why:

**B. Use clustering on customer profile data to understand key characteristics of consumer segments. Find similar profiles on social media**

- **Customer Segmentation:** Clustering excels at identifying groups within your data based on shared characteristics. This will reveal distinct segments of existing customers with similar profiles.
- **Targeted Ad Campaigns:** Once you understand these segments, you can leverage social media platforms' targeting features to find potential customers with profiles mirroring your high-value customer segments.

**Why other options are less ideal:**

- **A. Use regression on customer profile data...** Regression mainly predicts continuous target values (e.g., future premiums). While it might reveal relationships between features and customer likelihood, it's not directly suited for segmentation.
- **C. Use a recommendation engine...** Recommendation engines primarily suggest items (pets, policies) to existing customers. They're not designed to identify brand new customer profiles.
- **D. Use a decision tree classifier engine...** Decision trees classify data into predefined categories (e.g., likely to churn vs. unlikely to churn). This requires a labeled target variable, which you don't have for potential new customers.

#GeminiAdvanced 