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

Another example could be a model designed to predict whether an email is spam. The feature


        
    
