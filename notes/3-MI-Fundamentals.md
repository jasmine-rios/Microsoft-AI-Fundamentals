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

# INSERT TABLE

Next, we will split the data and use a portion of it to train the model.
In this case, the data was split randomly to ensure a  balanced representation of the dataset.

## INSERT TABLE of data selected for training.

While random spliting is common approach, there are other methpds that can be used based on the scenario:

*Stratified splitting*
    Ensures that specific proportions of key features (like popularity ranges) are maintained in both training and testing sets.

*Time-based splitting*
    Used when the data has a chronological order, such as time-series data, where older data is used for training and newer data for testing

*K-fold cross-validation*
    Splits the data into mulltiple folds, where each subset takes a turn as the test set while the others are used for training

To get a better understanding of how popularity scores (x)