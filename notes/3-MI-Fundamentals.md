# Fundamental Principles of Machine Learning

Foundational techniques:

- Regression analysis
- Classification
- Clustering

## What is Machine Learning?

Machine learning (ML) is a branch of AI (Artifical Intelligence).
Allows systems to perform tasks like **data analysis without needing explicity instructions**.
Instead, it processes large amounts of historical data, identifies patterns, and makes predictions based on those patterns.
For instance, you can use ML to classify images, numbers, or docum,ents and make predictions from them.

Let's say you work for a financial services organization looking differentiate between **fraudulent and genuine transactions**.
With ML, the **system would learn to identify patterns from known examples** and then apply that knowledge to **predict whether a new transaction is genuine**.

ML is **essential for modern businesses** because it helps **automate data collection, classification, and analysis**. This speed us decision making and drives growth.
It improces processes like customer experience and resource managemnt, enabling businesses to solve problems faster.

Although the terms *artifical intelligence* (AI) and *machine learning* (ML) are **used interchangeably**, they **aren't the same**. 
**AI is a broader** concept that includes anything from **voice assistants to self-driving cars**.
**ML, however, focuses on specific tasks**, such as predicting equipment maintenance schedules or classifying documents.

Take manufacturing, for example, ML can help with the following:

- Predictive maintenance
    Identify potential equipment failure **before they occur**, reducing down-time and repair costs

- Quality control
    Monitor production lines to **detect defects** and ensure **consistent product quality**

- Product design optimization
    **Redine designs**, such as improving the abrasiveness of sandpaper by **analyzing small changes in size and shape**

- Supply chain management
    Predict demand, identify bottlenecks, and streamline logistics to improve efficency

## The ML Model Workflow

An ML model is a software application that takes one or more input values and calculates an output value. The process of figuring out how to make that calculation is called *training*

Once the model is trained, you can use it to make *predictions*. This process is known as inferencing.

![Figure from Book about AI workflow](/assets/images/ai-worklow.png)

### Step 1: Train the model
The process of training an ML model begins with past data, which is referred to as the *training data* or *dataset*.
Each data point in the traning dataset is made up of two essential components
- Features
    The characteristics or attributes you observe in each data point
- Labels
    The outcome or result you want the model to predict

A dataset in table form is organized into **rows and columns**, as you would see in a spreadsheet or database.
Each **row represents an individual record or entry**, and each **column contains specific attributes or features of the data**.
This structure allows for easy comparison and analysis of data across multiple entries by s**yncing similar information in a consistant format**.

| Customer_ID | Purchase_Date | Product_Category | Rating | Feedback_Comments | Return_Request
|---|---|---|---|---|---|
| 001 | 2024-10-01 | Electronics | 5 | "Great product, fast delivery!" | No |
| 002 | 2024-10-05 | Apparel | 2 | "Size did not match the description." | Yes |
| 003 | 2024-10-07 | Home Goods | 4 | "Quality is good, but color is off." | No |
| 004 | 2024-10-10 | Electronics | 1 | "Item arrived damaged." | Yes |
| 005 | 2024-10-12 | Beauty | 3 | "Average product, packaging was poor." | No |

Data is often messy and incomplete. These imperfections can disort results, lead to inaccuracies, and complicate decision making.

For example, a common issue is **missing data**.
While removing incomplete informaiton is a straightforward approach, it can led to **unintended disortions**, particularly when the missing data is not randomly distributed.
Instead, consider alternative methods to handle missing data effectively:
- Mean/median imputation
    Replace missing values with the average (mean) or the middle value (median) of the dataset to maintain consistency
- Predictive imputation
    Leaverage statistical models to predict and fill in missing values based on **patterns in the avaliable data**, providing a more accurate estimate

Another common challenge in. data analysis is dealing with outliers.
*Outliers* are extreme **data points that differ significantly** from other observations.
They can distort results or obscure important patterns. **Properly managing outliers is essential for improving the accuracy and reliability of your findings**.
Consider the following approaches:
- Removal
    **Exclude outliers** from the dataset if they identified as errors or are **irrelevant to the analysis**
- Transformation
    **Use mathematical techniques** such as logarithmic or square root transformations, to **minimize the influence of outliers without removing them entirely**.
- Investigation
    Examine outliers closely to determine whether they provide valuable insights or are the result of data-entry mistakes

Data may also have **duplications**. For this you can consider these options:
- Deduplication algorithms
Use tools or scripts to identify and merge duplicate data
    
- Unique identifiers
Ensure that **each record** has a **unique key** to prevent duplication at the **entry point**

- Quality control
Regularly **audit data** to **detect and resolve duplicates**

Then there is a problem with **inconsistant data formats**.
You can use the following techniques to address this:

- Data normalization
**Convert data to a standard format** (e.g. ISO 8601 for dates)

- Validation rules
Implement **automated checks during data entry** to enforce consistent formatting

- Preprocessing pipelines
Develop extract, transform, and load **(ETL)** processes to clean and standardize data before analysis

Once you have improved the quality of the dataset--a process known as *data preparation*-- you can then look at training.
One way to think of this is in terms of basic algebra.
**The features are represented by x**, and there are often **several of them**, forming **a vector (an array of values)**. 
**The label is represented by y,** which is the prediction or **result the model tries to output**.

For example, let's say you're builidng a model that predicts the price of a house based on its characteristics. The **feature(x) might include the number of bedrooms**, square footage, or location. The **label (y) would be the house's sale price**. **The model is trained to learn how these features relate to the price** and then can **predict the price** of a new house based on similar characteristics.

Another example could be a **model** designed to predict whether an **email is spam**.
**The features (x) could be things like the presence of certain keywords**, the sender's address, and the time the email was sent.
**The label (y) would be a binary outcome: 1 if the email is spam, 0 is it's not.**
Over time, the model learns to recognize patterns in the features that indicate whether an email is spam or legitimate.

### Step 2: Apply the Algorithm

When you are working with an ML model, you need an **algorithm to figure out the relationship** between the features and the label.
The goal is to find a way to **take the features(x) and use them to predict the label (y)**.
The basic idea is to **fit a function to your data**.
In other words, the algorithm looks for a pattern that can calculate y based on x. For our example, this is what is looks like:

y = f(x)

**Once the algorithm has done it's job, it gives you a model.**
This model is essentially a function that performs the calculation.

### Step 3: Use Inferencing

Once the training phase is done, you can use the trained model **to make predictions, a process called *inferencing*.
The model now works like a **software program that contains the function learned during training**.
You provide it with a set of feature values, and it gives you a prediction for the label.

Since this output is a **prediction generated by the function rather than an actual observed value**, it's typically written as **ŷ**, pronounced "y-hat".
This is a useful way to show the **result is an estimate based on what the model has learned, not a guarenteed outcome**.

## Types of ML

There are several types of ML, each designed for differnt kinds of problems.
At the highest level, ML is divided into two main types: *supervised learning*, which has **labeled data**, and *unsupervised learning*, where the data does **not have labels**.
These two categories help determine how the model learns from the data and what kind of tasks it can perform. Under the umbrellas of supervised and unsupervised learning, **there are other types of ML**.

![ML Categories figure in the book](/assets/images/ML-Categories.png)

## Regression Analysis

*Regression analysis* is a statistical method used to **predict a numerical outcome**  based on **one or more known factors**, or variables.
It helps you **understand the relationship between these variables** and the **result you're trying to predict**.

For example, let's say you want to predict **how much a new product will sell** based on factors like **advertising speed**, the season, and market trends.
Regression analysis allows you to analyze these factos and estimate how they affect sales so that you can forecast future performance based on current data.

Here's how you would approach it:

Split the data
    Begin by **diving your data into three subsets, a training set, a validation set, and a testing set**. The **training set is used to develop** the model, the **validation set helps fine-tune** the model's parameters, and the **testing set is reserved for assessing the model's performance on new, unseen data**.

Train the model
    **Using the training data, apply an algorithm** to **identify relationships** between key variables, such as the advertising budget, seasonality, and market trends, **and their impact** on sales.
    The **model searches for patterns**, such as whether increased **ad spending leads to higher sales** or if **certain times of the year naturally see better sales performance**.

Fine-tune the model
    With the **validation set**, **optimize the model's parameters or hyperparameters to enhance its predictive accuracy**. This step helps ensure that the model generalizes well and **avoids overfitting** to the training data.

Test the model
    **Evaluate the performance of the fine-tuned model using the testing set**. In this stage, the model generates sales **predictions based on input** variables (e.g. advertising budget, season, market trends) and **compares these predictions to actual sales data to measure accuracy**.

Evaluate the model
    Access the accuracy of the model's predictions using relevant metrics, such as **mean absolute error (MAE), root mean square error (RMSE), or R²**. If the model's performance falls short of expectations, refine the process by revisiting earlier steps, such as trying a different algorithm, adjusting parameters, or including new features.

Iterate and improve
    Using the insights gained from the evaluation, **iterate on the model to improve it's performance**. This iterative process might include collecting additional data or exploring alternative modeling techniques to boost accuracy.

### Example: Ticket Sales

Let's take a look at a more detailed example to better understand how regression analysis works.
For this example, we won't cover every step outlined in the previous section.
When it comes to the exam, such in-depth detail about regression analysis isn't necessary.
Instead, we'll focus on the main phases.

In our example, we'll **predict a numeric label (y) based on a single feature (x)**. 
While most real-world applications involve multiple features, starting with just one keeps things simple and allows us to focus on the core idea.

Let's consider the example of predicting concert ticket prices based on the popularity of the performing artist. 
Here, the **popularity score** is derived from survey data collected bt fans, representing a **value on a scale from 1 to 100**.
This **score serves as our feature** while the **ticket price for the artist's concert is the label we aim to predict**.
To build this prediction model, we'll **use historical data that pairs popularity scores (x) with their corresponding tikcet prices (y) from past concerts**.

| Artist popularity (X) | Ticket Price (y)
|---|---|
| 35 | $45 |
| 40 | $60 |
| 45 | $55 |
| 50 | $75 |
| 55 | $65 |
| 60 | $85 |
| 65 | $100 |
| 70 | $105 |
| 75 | $115 |
| 80 | $135 |
| 85 | $140 |
| 90 | $170 |

Next, we will **split the data** and use a portion of it **to train the model**.
In this case, the data was **split randomly to ensure a  balanced representation of the dataset**.

| Artist popularity (X) | Ticket Price (y)
|---|---|
| 40 | $60 |
| 50 | $75 |
| 60 | $85 |
| 70 | $105 |
| 75 | $115 |
| 80 | $135 |

While random spliting is common approach, **there are other methods that can be used based on the scenario**:

*Stratified splitting*
    Ensures that **specific proportions of key features** (like popularity ranges) are **maintained in both training and testing sets**.

*Time-based splitting*
    Used when the data has a **chronological order**, such as time-series data, where **older data is used for training and newer data for testing**.

*K-fold cross-validation*
    **Splits the data into multiple folds**, where each subset **takes a turn as the test set** while the others are used for training

To get a better understanding of how popularity scores (x) and ticket prices (y) relate to each other, **we can plot these values on a graph**.
By plotting these points you can start to see the relationship between the two--typically, as the popularity increases, so does the ticket price.

![Scatter plot from book](/assets/images/ML-scatter-plot.png/)

With the training dataset, we're ready to apply an algorithm that can model the relationship between artist popularity and ticket price. 
We'll use the **linear regression formula**, which essentially finds the **best-fit line through the points** that minimizes the distance between the line and the actual data points.
This line represents a function where the slope tells you how much the ticket price will increase with each increase in the artist's popularity.

![Scatter plot with linear regression line figure from book](/assets/images/linear-regression-line.png)

Let's say an artist has a popularity score of 77.
By applying the equation derived from the linear regression line, we can estimate the corresponding ticket price.
In this case, the price would be something like $120 based on the trend we've established.

The next step is to **evaluate the accuracy of this regression model**.
Using the **training dataset**, we can **predict the ticket prices for each artist's popularity score**.

| Artist popularity (X) | Actual ticket price (y) | Predicted ticket price  (ŷ) |
|---|---|---|
| 35 | $45 | $50 |
| 45 | $55 | $60 |
| 55 | $65 | $70 |
| 65 | $100 | $85 |
| 80 | $135 | $120 |
| 90 | $170 | $140 |  

We can then plot these values on a chart.

![The orginal dataset with actual and predicted ticket prices for test data from the book](/assets/images/ML-predict-vs-actual.png)

The orginial data points capture the historical trend while the test datat highlights how closely the model's predictions align with actual ticket prices.
The chart makes it easy to visualize where the model performed well and where deviations occured, particularly by comparing the actual and predicted ticket prices across different levels of artist popularity.

In this case, the model performed fairly well.
For midrange popularity scores, the predicted values are close to the actual values, indicating minimal error.
However, at the lower (35) and higer (90) ends of the popularity scale, the model's predictions underestimate the actual ticket prices.
While the performance is promising, the noticable deviations at these extremes suggest the model could benefit from additional fine-tuning to improve accuracy, especially for edge cases.

### Evaluation Metrics for Regression Models

When it comes to measuring **how well your regression model performs,** there are a few handy metrics based on the differences between your predicted values and actual ones.

#### Mean absolute error

Imagine you're **predicting how many pizzas a group of friends will eat at your party**.
*Mean absolute error (MAE)* helps you figure out,  **on average, how far off your predictions were**--whether you guessed too high or too low.
For instance, if you **predicted 4 pizzas but your friends ate 7, you missed by 3**.
**MAE ignores whether the difference is positive or negative**, os it treats **both -3 and +3 as a difference of 3**.
If your absolute errors for a set of predictions were 1,2, 3, and 4 pizzas, the **MAE would simply be the average of those numbers: 2.5 pizzas**.

#### Mean Squared error

Sometimes, you want to **give more weight to bigger errors**.
After all, consistently being off by 1 pizza isn't as bad as being widly off by five.
That's where *mean squared error (MSE)* comes in.
Instead of just taking the differences as they are, you **square each error (making bigger mistakes stand out)**, and z88then averagez88 those squared values.
In our pizza example, if your errors were 1, 2, 3, and 4, squaring them gives you **1, 4, 9, and 16**.
The MSE would then be the **average of these squared errors: 7.5**.

#### Root mean squared error

While MSE is useful, **those squared numbers don't match up with the original quantities you were measuring**, so they can feel a little abstract.
If you want the **error back in terms of pizzas** (or whatever you're predicting), you can **take the square root of the MSE**.
That's called the *root mean squared error (RMSE)*.
In this case, the **square root of 7.6 is about 2.74, meaning your average error is around 2.74 pizzas**.

#### Coefficent of determination

What if you want to **understand how well your model explains the variation in your data**?
Enter R², also called the *coefficent of determination*.
This metric tells you how much of the **difference between actual and predicted values your model accounts for**.

For example, if you're trying to predict how many cupcakes a bakery sells each day, **R² tells you how much your model can explain**.  
If your **R² value is 0.85**, that means **your model explains 85% of the variation in cupcake sales**--the **rest might be due to some unexpected cupcake-related event, like a new bakery opening next door.**
R² ranges from 0 to 1, the closer it is to **1, the better your model fits the data.**

All of these metrics are certainly helpful. But in real-world scenarios, ML isn't a one-shot deal. Data scientists typically train models over and over, tweaking different aspects to improve performance. Here's what they adjust:

- Feature selection and preparation
    You can **choose which factors or features to include** in the model and **how to tweak them for better results**.
    For instance, maybe you realize that **cupcake sales don't depend just on wheather but also on nearby events**.

- Algorithm selection
    There is **more than one way to predict the number of cupcakes sold**.
    While **one algoritm might focus on simple linear relationships, another might use more complex patterns**.

- Algorithm parameters
    These are the **settings you adjust to fine-tune your algorithm**.
    Think of them like **dials on an oven.**
    If your cupcakes are coming out **undercooked, you tweak the temperature** (or in ML, the *hyperparameters*) to get better results.

After several rounds of this iterative process, you'll settle on the version of the model that performs best for your specific problem.

Let's sum up what we have learned about regression analysis

| Factors | Description |
|---|---|
| Purpose | To predict a numeric outcome label based on one or more predictor features by identifying patterns in historical data |
| Process | 1. Split data into training and testing sets. 2. Train the model to identify relationships. 3. Test the model to make predictions. 4. Evaluate model accuracy and refine if needed|
| Training the model | Uses an algorithm, such as linear regression, to analyze patterns in the training data, establishing a predictive relationship between the independent and dependent variables |
| Evaluation metrics | - MAE: Measures average prediction error without considering direction (over/under-estimate) - MSE: Empahsizes larger errors by squaring them - RMSE: Provide the error in original measurement units - R² (coefficient of determination): Indicates the model's explanatory power, with values closer to 1 suggesting a better fit |

## Classification

Classification in ML is a supervised learning task where the goal is to predict the category or class to which a given data point belongs.
It involves training a model on labeled data where the label is categorical, such as "yes" or "no".
The model learns the relationship between input features and output classes, enabling it to assign new, unseen data points to one of the predefined categories.

There are various types of classification techniques. In the next few sections, we'll take a look at binary and multiclass classification

### Binary Classification

*Binary classfication* is one of the **most common types of classification tasks**.
As its core, it's about **predicting one of two possible outcomes**. When you feed your model data, the goal is to get it to **categorize new information into one of two buckets, often labeled as 0 and 1.**
For example, if you're building a model to predict whether an email is spam or not, binary classification is your go-to technique.
**Each email gets analyzed, and the model spits out a prediction: "spam" or "not spam".**

What makes binary classification different from something like regression is that **you aren't predicting a continous values**, like a temperature or a sales figure.
Instead, **you're focused on making a choice between two discrete options**.
The **model looks at the features of the data** you provide, such as email content, and it uses that to **assign a probability**.
Based on this probability, it then makes a final classification.

Let's walk through a simple example to show how binary classification works.
Imagine we want to predict whether a person will default on a loan using one feature: their credit score (x).
Our goal is to classify them into one of the two categories: either they default (y = 1) or they don't (y = 0).
The model will learn from the data in the table below to make predictions

| Credit score (x) | Default (y) |
|---|---|
| 580 | 1 |
| 720 | 0 |
| 610 | 1 |
| 750 | 0 |
| 590 | 1 |
| 800 | 0 |

Based on the patterns in the training data, the model will eventually predict whether someone is likely to defauly or not.
As you can see, it's about using past information to make a binary choice.
In our example, people with a credit score of 610 or lower are predicted to default while anyone with a score of 720 or higher is predicted not to default.

To train our model, we'll use an algorithm that analyzes the training data and fits it to a function that calculates the probaility of a person defaulting on a loan.
For example, if the model predicts a probability of 0.8 for default, that means there's an 80% chance the person will default and a 20% chance they won't.

There are several algorithms that handle binary classification, but *logisitic regression* is a common choice. **Logistic regresssion gives us an S-Shaped curve, called a *sigmoid function*, that assigns values between 0 and 1 based on the input data** and shown in the figure below.
Even though its name includes *regression*, **the logistic regression algorithm is used for classification because it models the probability of different outcomes**. This is a common topic for the exam.

![Logistic Regression: Probability of Default by Credit Score figure from book](/assets/images/ML-classification.png)

In this case, the curve shows the probability that someone will defauly (y = 1) based on their credit score (x).
Mathematically, the model's function can be represented like this:

f(x) = P(y = 1 | x)

Note that for the exam, you will not have to memorize equations.
They are used in this book as a better way to help you understand the concepts.

For some people in the training data, we already know they defaulted (y = 1), so the probabilty for them is 1.0.
For others who didn't default, the probability is 0.0.
The sigmoid curve visually shows how the likelihood of default changes as credit scores increase.

In the figure, the dashed line at 0.5 serves as the treshold for our model's predictions. When the calculated probability is at or above 0.5, the model predicts that the person will default (y = 1).
If the probability falls below 0.5, the prediction is that they won't default (y = 0).
For instance, if someone has a credit score of 580, and the model assigns a 0.9 proability of default. that's well above the threshold, meaning the model would predict this person is likely to default.

Just like with regression models, when you train a binary classification model, it's essential to hold back a set of data to validate how well the model performs.
Let's say we kept the credit score data in the table aside to validate our model predictiong loan defaults, Note: The credit score values shown in the table below are normalized for demonstration purposes and do not reflect actual credit score ranges.

| Credit score (x) | Default? (y) |
|---|---|
| 62| 0 |
| 108 | 1 |
| 113 | 1 |
| 70 | 0 |
| 88 | 1 |
| 91 | 1 |

We can apply the logistic function we trained earlier to these values, which you can see in the figure below

![A sigmoid function used to evaluate a binary ](/assets/images/ML-credit-threshold.png)

Based on whether the calculated probability is above or below the threshold (usually 0.5), the model will predict either a defauly (1) or no default (0) for each credit score.
We can then compare the predicted defaults (ŷ) to the actual defaults (y), shown in the table below

| Credit score (x) | Default? (y) | predicted defaults (ŷ)
|---|---|---|
| 62| 0 | 0 |
| 108 | 1 | 1 |
| 113 | 1 | 1 |
| 70 | 0 | 0 |
| 88 | 1 | 0 |
| 91 | 1 | 1 |

This comparison helps us see where the model is getting it right and where it might need improvement.

### Evaluation Metrics for Binary Classification

The first step in calculating evaluation metrics for a binary classification model is usually to create a *confusion matrix* of the number of correct and incorrect predictions for each possible class label as you see in the table below:

| | Positive | Negative | 
|---|---|---|
| Positive | 30 | 45 |
| Negative | 20 | 19 |

The rows represent the actual values, labeled as "positive" or "negative", while the columns show the predicted values.
For example, **the model predicted the positive class correctly 30 times**, which is displayed as the true positive count.
However, it also made **45 incorrect predictions where it classified negatives as positives**.
Simarly, there are **20 instances of false negatives and 19 true negatives.**
This distrubution helps evaluate the accuracy and types of errors in the model's predictions.
One way to express the different possibilities for the confusion matrix is shown below

| | Predicted Positive | Predicted Negative | 
|---|---|---|
| Actual Positive | True positive | False negative |
| Actual Negative | False postive | True negative |

The rows and columns follow the same arrangement, but **each cell now includes a label: true positive, false positive, false negative, and true negative**.
These labels offer a clearer understanding of the relationship between predicted and actual outcomes:

- True Postitive (TP)
    The model predicted the positive class, and the actual class was also positive. This a correct prediction for the positive class.

- False Positive (FP)
    The model predicted the positive class, but the actual class was negative. This is an incorrect prediction, known as a *type I error*.

- False negative (FN)
    The model predicted the negative class, but the actual class was positive.
    This is another prediction, known as a type II error.

- True negative (TN)
    The model predicted the negative class, and the actual class was also negative.
    This is a correct prediction for the negative class.

Calling this a *confusion matrix* is certainly apt: it can be tough to understand this.
Yet this is on the exam... 🥲
So memorize the four outcomes.

Let's now take a look at other common evaluation metrics