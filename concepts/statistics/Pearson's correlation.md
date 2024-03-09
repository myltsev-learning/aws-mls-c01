Pearson's [[concepts/statistics/Correlation|Correlation]] coefficient, also known as Pearson's product-moment correlation, <mark style="background: #FFF3A3A6;">is a statistical tool used to measure the strength and direction of a <strong>linear relationship</strong> between two continuous variables.</mark> It's basically a number between -1 and 1 that tells you how closely two sets of data are related.

Here's a breakdown of what Pearson's correlation does:

- **Measures Strength:** The value of the coefficient (usually denoted by r) indicates the strength of the association. A value closer to 1 (positive or negative) suggests a strong correlation, while a value closer to 0 suggests a weak or no correlation.
- **Indicates Direction:** The sign of the coefficient tells you the direction of the relationship. A positive sign indicates that as one variable increases, the other tends to increase as well (positive correlation). Conversely, a negative sign indicates that as one variable increases, the other tends to decrease (negative correlation).

Here are some key things to remember about Pearson's correlation:

- It assumes a **linear relationship** between the variables. If the relationship isn't linear, Pearson's correlation might not be the best tool.
- It works best for **continuous variables**. These are variables that can take on any value within a range, like height, weight, or temperature.
- Be cautious about interpreting correlation as causation. Just because two things are correlated doesn't necessarily mean one causes the other.

Overall, Pearson's correlation coefficient is a valuable tool for understanding how two continuous variables are related. It's widely used in various fields like statistics, machine learning, and research to analyze data and identify potential relationships.

### Formula

$r = Σ((xi - x̄)(yi - ȳ)) / √(Σ(xi - x̄)² * Σ(yi - ȳ)²)$

Where:

- **r:** Pearson's correlation coefficient
- **xi:** Individual values of variable x
- **x̄:** Mean of variable x
- **yi:** Individual values of variable y
- **ȳ:** Mean of variable y
- **Σ:** Symbol for summation

**How to interpret the formula:**

1. **Numerator:** Measures the covariance between the two variables. It looks at how much each data point deviates from the mean of each variable, and multiplies those deviations.
2. **Denominator:** Measures the variability of each variable separately and then combines the variability to ensure the final value is standardized (i.e., between -1 and 1).

### Example

**Scenario:** A researcher wants to see if there's a relationship between hours of study and exam scores.

**Data:**

|Hours of Study (x)|Exam Score (y)|
|---|---|
|2|65|
|5|75|
|3|70|
|6|90|
|4|82|

**Steps:**

1. **Calculate the means (x̄ and ȳ):**
    - x̄ = (2 + 5 + 3 + 6 + 4) / 5 = 4
    - ȳ = (65 + 75 + 70 + 90 + 82) / 5 = 76.4
2. **Calculate deviations from the mean for each variable:**
    

|Hours of Study (x)|Exam Score (y)|xi - x̄|yi - ȳ|
|---|---|---|---|
|2|65|-2|-11.4|
|5|75|1|-1.4|
|3|70|-1|-6.4|
|6|90|2|13.6|
|4|82|0|5.6|

3. **Calculate squared deviations and the products of deviations:**

|Hours of Study (x)|Exam Score (y)|xi - x̄|yi - ȳ|(xi - x̄)²|(yi - ȳ)²|(xi - x̄)*(yi - ȳ)|
|---|---|---|---|---|---|---|
|2|65|-2|-11.4|4|129.96|22.8|
|5|75|1|-1.4|1|1.96|-1.4|
|3|70|-1|-6.4|1|40.96|6.4|
|6|90|2|13.6|4|184.96|27.2|
|4|82|0|5.6|0|31.36|0|

4. **Sum the squared deviations and the product of deviations:**

$$
	Σ(xi - x̄)² = 10
$$
$$
	Σ(yi - ȳ)² = 389.2
$$
$$
    Σ((xi - x̄)(yi - ȳ)) = 55
$$

    
    
1. **Plug the sums into the formula:**

$$
	r = (55) / √(10 * 389.2) = 0.88	
$$

**Interpretation:** The Pearson correlation coefficient of 0.88 indicates a strong positive relationship between hours of study and exam scores. This means that students who study for more hours tend to score higher on exams.

#concept 