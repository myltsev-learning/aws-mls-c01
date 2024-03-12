Unbalanced data occurs when <mark style="background: #FFF3A3A6;">your dataset has a significant difference in the number of examples belonging to each class</mark>. For instance, in the case of spam detection, you might find that the majority of your emails are "not spam" with relatively few actually being "spam".

**Why Does it Matter?**

Standard classification algorithms tend to favor the majority class. This can be problematic because they might become really good at predicting the common class, but might struggle to accurately identify examples of the less frequent class (which might be what you're really interested in, like predicting spam or user churn).

#concept 