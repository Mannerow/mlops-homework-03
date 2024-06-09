## 🤔 What is it?

This project walks through the homework for Module 3 in DataTalk's MLOps Zoomcamp. The project can be started by running: 'docker compose up', which starts Mage on port 6789 and MLflow on port 5000. Mage is used to build a pipeline that ingests and transforms NYC taxi data, trains a linear regression model with sklearn, logs the model and the artifact (dict vectorizer), and then registers the model with MLFlow. 

## Homework-03

### Question 1. Run Mage

Start Mage: docker compose up'

Version Number: v0.9.70

Shut Down: docker compose down

### Question 2. Creating a project

Now let's create a new project. We can call it "homework_03", for example.

How many lines are in the created metadata.yaml file?

35
45
55
65

Answer: 55

### Question 3. Creating a project

Let's create an ingestion code block.

In this block, we will read the March 2023 Yellow taxi trips data.

How many records did we load?

3,003,766
3,203,766
3,403,766
3,603,766

Answer: 3,403,766

### Question 4. Data preparation

Added a Transformer block for Data Preperation. 

What's the size of the result?

2,903,766
3,103,766
3,316,216
3,503,766

Answer: 3,316,216

### Question 5. Train a model

We will now train a linear regression model using the same code as in homework 1

Fit a dict vectorizer
Train a linear regression with default parameres
Use pick up and drop off locations separately, don't create a combination feature
Let's now use it in the pipeline. We will need to create another transformation block, and return both the dict vectorizer and the model

What's the intercept of the model?

Hint: print the intercept_ field in the code block

21.77
24.77
27.77
31.77

Answer: 24.77

### Question 6. Register the model

Next, start the compose again and create a data exporter block.

In the block, we

Log the model (linear regression)
Save and log the artifact (dict vectorizer)
If you used the suggested docker-compose snippet, mlflow should be accessible at http://mlflow:5000.

Find the logged model, and find MLModel file. What's the size of the model? (model_size_bytes field):

14,534
9,534
4,534
1,534

Answer: 4,534
