A company is running a machine learning prediction service that generates 100 TB of predictions every day. A Machine Learning Specialist must generate a visualization of the daily precision-recall curve from the predictions, and forward a read-only version to the Business team.  
Which solution requires the LEAST coding effort?  

A. Run a daily Amazon EMR workflow to generate precision-recall data, and save the results in Amazon S3. Give the Business team read-only access to S3.

B. Generate daily precision-recall data in Amazon QuickSight, and publish the results in a dashboard shared with the Business team.

C. Run a daily Amazon EMR workflow to generate precision-recall data, and save the results in Amazon S3. Visualize the arrays in Amazon QuickSight, and publish them in a dashboard shared with the Business team.

D. Generate daily precision-recall data in Amazon ES, and publish the results in a dashboard shared with the Business team.

My answer:  C

---

While option C could work, there's an even better choice for minimizing coding effort:

**B. Generate daily precision-recall data in Amazon QuickSight, and publish the results in a dashboard shared with the Business team.**

Here's why it's the most streamlined solution:

- **Built-in Functionality:** QuickSight likely has native support for calculating precision-recall metrics and generating the corresponding curve visualization. This eliminates the need for custom code in an EMR workflow.
- **Direct Visualization:** QuickSight is designed for business intelligence dashboards. You can generate the visualization and share it with the Business team within the same platform, avoiding the intermediate step of saving to S3.
- **Minimal Coding:** While some configuration in QuickSight might be necessary, it should involve significantly less coding compared to developing an EMR workflow with data manipulation steps.

**Considerations:**

- **Data Source:** Ensure that the prediction data can be easily accessed by QuickSight (e.g., stored in S3, a database compatible with QuickSight, or accessible via an API).
- **Calculation Support:** If QuickSight doesn't offer built-in precision-recall calculations, option C would then become the most viable approach.

> Claude3 agree with Gemini.

#GeminiAdvanced 