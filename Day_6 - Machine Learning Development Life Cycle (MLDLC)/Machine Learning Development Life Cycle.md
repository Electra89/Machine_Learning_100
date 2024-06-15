# Machine Learning Development Life Cycle (MLDLC)

<br>

## MLDLC
It is set of guidelines that you need to follow which while you creating machine learning based software product it could be recommender system, loan prediction model for bank.

![](https://miro.medium.com/v2/resize:fit:700/1*wekWcWfEgO4RK-lOyw7jdA.png)

### 1. Framing the Problem
In this stage, you decide what the problem is and how to solve it. Who is your customer? How much will it cost? How many people will be on the team? What will the end product look like? Which machine learning model will you be using? Where to deploy it? What framework will be used? From where will the date come? What will be the source of data?

![](https://miro.medium.com/v2/resize:fit:700/1*xwSkKW2Ouixl79m5r_Y6_g.jpeg)

After this all things are properly figured out properly, then only we can proceed to further step

<br>

### 2. Gathering Data
Data is essential. While working on a machine learning project, you need the data to build the model. without data it is not possible
![](https://miro.medium.com/v2/resize:fit:700/1*lZtzW2MUoq6IqrUYBdKfCQ.jpeg)

- **APIs** : - Hit the API using Python code and fetch data in JSON format.

- **Web Scrapping** :- Sometimes data is not publicly available, i.e., it is on some website, so we need to extract it from there. For eg- Trivago uses this method to collect hotel prices data from every website

- **Data Warehouse** :- Data is also stored in databases. But this data cannot be directly used as it is running data. So data from a database is stored in a data warehouse and then used.

- **Clusters**: - Also, data is sometimes stored in tools like Spark in the form of clusters, which are basically big data, so data is fetched through these clusters.

<br>

### 3. Data Pre-processing
when you are taking data from external sources that are bound to be unclean or dirty. You cannot use that data directly.
You cannot pass on this data directly to a machine learning model because the result is not good. Data can have structural issues. it can have missing data, can Contain some outliers & noises

![Free vector data processing concept illustration](https://img.freepik.com/free-vector/data-processing-concept-illustration_114360-4760.jpg?t=st=1718119371~exp=1718119971~hmac=2b64de39c69f7f0b2f5ea758f9c673ff3f0e3af29d0162829ab4638a0cace2e4)

So here, you need data preprocessing. it involves removing duplicates, removing missing values, removing outliers, and scaling the values (standardization)
The core idea behind data preprocessing is to bring data in such a format that it will be easily consumed by your machine learning model.

### 4. Exploratory Data Analysis
In this stage, you analyze data, which means you try to study the relationship between input and output variables.

At this stage, you need to perform. In many experiments with data, you have to extract hidden relationships from the data. This stage gives data insights by visualizing data, univariate analysis, bi-variate analysis, multi-variate analysis, outlier detection, handle imbalanced dataset

![Business analytics concept glow isometric 4 colorful graphic presentations with profit growth diagrams currency symbols vector illustration](https://img.freepik.com/free-vector/business-analytics-concept-glow-isometric-4-colorful-graphic-presentations-with-profit-growth-diagrams-currency-symbols-vector-illustration_1284-30863.jpg)

### 5. Feature Engineering and Selection
features are the input columns. Features are Important because output is depends upon the Input (features)

![Programmer Coder concentrated at working project Developing programming and coding technologies](https://img.freepik.com/premium-vector/programmer-coder-concentrated-working-project-developing-programming-coding-technologies_569013-338.jpg)

**feature selection-**

Sometimes you have more features, like 100 or 200, but you cannot proceed with all features because of two reasons.

1.  These features are not helpful. for building model not necessary every input affects the output you need to remove those features that are not impacting your off when you select features
2.  With more columns, it will take more time to train the model, so by removing irrelevant columns, you can save time.

Both feature engineering & selection are crucial

### 6. Model Training, Evaluation& Selection
Once you're sure about your data, you are ready to train the model. you try different diff. machine learning algorithm you train that algorithm by your data every algorithm

![Kids programming and creating robot at class, tiny people. Engineering for kids, learn science activities, early development classes concept. Pinkish coral bluevector isolated illustration](https://img.freepik.com/free-vector/kids-programming-creating-robot-class-tiny-people-engineering-kids-learn-science-activities-early-development-classes-concept-pinkish-coral-bluevector-isolated-illustration_335657-1490.jpg)

### 7. Model Testing
Once our machine learning model has been trained on a given dataset, we test the model. In this step, we check the accuracy of our model by providing a test dataset.

Testing the model determines the percentage accuracy of the model as per the requirements of the project or problem.

### 8. Model Deployment
In this step, we deploy the model in a real-world system.If the above-prepared model is producing an accurate result as per our requirement with acceptable speed, then we deploy the model in the real system. But before deploying the project, we will check whether it is improving its performance using the available data or not.

![Cloud services isometric composition with conceptual images of network elements storage capsules and small human characters vector illustration](https://img.freepik.com/free-vector/cloud-services-isometric-composition-with-conceptual-images-network-elements-storage-capsules-small-human-characters-vector-illustration_1284-30496.jpg)


For deployment we can use Heroku, Amazon Web Services, Azure ,Google Cloud Platform, etc. 