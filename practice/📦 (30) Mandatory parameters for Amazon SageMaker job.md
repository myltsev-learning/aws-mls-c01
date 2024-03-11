When submitting [[Amazon SageMaker|Amazon SageMaker]] training jobs using one of the built-in algorithms, which common parameters MUST be specified? (Choose three.)  

A. The training channel identifying the location of training data on an Amazon S3 bucket.
B. The validation channel identifying the location of validation data on an Amazon S3 bucket.
C. The IAM role that Amazon SageMaker can assume to perform tasks on behalf of the users.
D. Hyperparameters in a JSON array as documented for the algorithm used.
E. The Amazon EC2 instance class specifying whether training will be run using CPU or GPU.
F. The output path specifying where on an Amazon S3 bucket the trained model will persist.

My answer: A, B, C

---
## Incorrect Answer

Your answer (A, B, C) is incorrect. The correct answer is: **C, E, F**.

## Documentation proof

In this documentation we can see that C, E, F are required: [CreateTrainingJob - Amazon SageMaker](https://docs.aws.amazon.com/sagemaker/latest/APIReference/API_CreateTrainingJob.html)

**F**
> Specifies the path to the S3 location where you want to store model artifacts. SageMaker creates subfolders for the artifacts.

**E**
> The resources, including the ML compute instances and ML storage volumes, to use for model training.

**C**
> The Amazon Resource Name (ARN) of an IAM role that SageMaker can assume to perform tasks on your behalf.

## YouTube video lesson proof

<iframe title="Build train and deploy model in sagemaker |  sagemaker tutorial | sagemaker pipeline" src="https://www.youtube.com/embed/Bxo_DrPSJgI?feature=oembed" height="113" width="200" allowfullscreen="" allow="fullscreen" style="aspect-ratio: 1.76991 / 1; width: 100%; height: 100%;"></iframe>

## Prompt for Lesson

```
# Learn about Amazon SageMaker Training Job Parameters

To better understand the required parameters for submitting Amazon SageMaker training jobs, please cover the following topics:

1. Overview of Amazon SageMaker training job workflow
2. Mandatory parameters for SageMaker training jobs
   - Training data location (S3 bucket and prefix)
   - IAM role with necessary permissions
   - Output location for trained model (S3 bucket and prefix)
3. Optional parameters for SageMaker training jobs
   - Validation data location
   - Hyperparameters
   - Instance types and resource configurations
4. Best practices for specifying training job parameters
5. Examples of submitting training jobs with different built-in algorithms

Please provide a comprehensive lesson covering these topics, with code examples and explanations to reinforce the understanding of required and optional parameters for SageMaker training jobs.
```

This lesson will help you better grasp the mandatory and optional parameters when submitting Amazon SageMaker training jobs, ensuring you can correctly identify the required parameters in the future. 🚀