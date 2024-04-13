# Types of Machine learning


<table border="2">
    <tr>
        <td colspan="4" align="center" ><b>Types of Machine Learning</b></td>
    </tr>
    <tr>
        <td align="center" ><b>Supervised</b></td>
        <td align="center" ><b>Unsupervised</b></td>
        <td align="center" ><b>Semi-Supervised</b></td>
        <td align="center" ><b>Reinforcement</b></td>
    </tr>
    <tr>
        <td> - Regression</td>
        <td> - Clustering</td>
        <td rowspan="4"> </td>
    </tr>
    <tr>
        <td> - Classification</td>
        <td> - Dimensionality reduction</td>
    </tr>
    <tr>
        <td rowspan="2"></td>
        <td> - Anomaly detection</td>
    </tr>
    <tr>
        <!-- <td ></td> -->
        <td> -  Association Rule Learning</td>
    </tr>
</table>

<br>

## Supervised Machine Learning
Supervised learning is the types of machine learning in which machines are trained using well "labelled" training data, and on basis of that data, machines predict the output. The labelled data means some input data is already tagged with the correct output.

### - Regression :


![](https://miro.medium.com/v2/resize:fit:402/1*xYWJrCEcRw07dlUv9S0WMA.png)
- In regression, the goal is to predict a continuous value output based on input features.
- Examples include predicting house prices based on features like size and location, or predicting stock prices based on historical data.
- For example, given a radiological image, a model could predict how many more years the associated individual will be sick or healthy.

<br>

### - Classification :

![](https://miro.medium.com/v2/resize:fit:504/1*kaeos8R5BmsSOcCbUN0P6Q.png)
- Classification involves predicting a categorical label or class for a given input.
-   It's used for tasks like spam detection (classifying emails as spam or not), sentiment analysis (classifying text as positive or negative), and medical diagnosis (classifying diseases based on symptoms).
- For example is categorizing animal pictures into a cat group and a dog group. The machine is trained on data with many examples of inputs (like an image of an animal) along with corresponding outputs, often called labels (like “cat” or “dog”). Train the model with a million pictures of dogs and cats, and it should be able to classify a picture of a new dog that wasn’t in the training data.

## Unsupervised Machine Learning
Unsupervised  machine learning, uses machine learning (ML) algorithms to analyze and cluster unlabeled data sets. These algorithms discover hidden patterns or data groupings without the need for human intervention.

### - Clustering:
![Machine Learning with ML.NET – Complete Guide to Clustering](https://rubikscode.net/wp-content/uploads/2020/10/clusters.png)

Clustering is the task of dividing the unlabeled data or data points into different clusters such that similar data points fall in the same cluster than those which differ from the others. In simple words, the aim of the clustering process is to segregate groups with similar traits and assign them into clusters.
<br/>

### -Dimensionality Reduction:
![Dimensionality Reduction Technique](https://static.javatpoint.com/tutorial/machine-learning/images/dimensionality-reduction-technique.png)
Dimensionality reduction is a technique used to reduce the number of features in a dataset while retaining as much of the important information as possible. In other words, it is a process of transforming high-dimensional data into a lower-dimensional space that still preserves the essence of the original data.

### -Anomaly Detection:
![anomaly detection machine learning](https://editor.analyticsvidhya.com/uploads/66719Anamoly%20(1).png)

Anomaly detection, sometimes called outlier detection, is a process of finding patterns or instances in a dataset that deviate significantly from the expected or “normal behavior.”
 - An actual data point significantly outside a distribution’s mean or median is an **outlier**.
 - An anomaly is a **false data point** made by a different process than the rest of the data.
<br/>

 ### -Association Rule Learning:
 ![](https://miro.medium.com/v2/resize:fit:700/1*BEFF9cZF92Xn9Frds3XD4g.png)
 Association Rule Learning is used to discover interesting relationships or associations among variables in large datasets. It identifies frequent patterns, associations, or correlations among a set of items or variables. One of the most well-known algorithms for association rule learning is the Apriori algorithm. This technique finds rules like "If item A is bought, then item B is likely to be bought as well," which is commonly used in market basket analysis for product recommendation systems.
 
<br/>

## Semi-Supervised Machine Learning
![](https://miro.medium.com/v2/resize:fit:700/1*snZhMEQFhoJwbM5c0CPOAw.png)

Semi-supervised learning is a type of machine learning that falls in between supervised and unsupervised learning. It is a method that uses a small amount of labeled data and a large amount of unlabeled data to train a model. The goal of semi-supervised learning is to learn a function that can accurately predict the output variable based on the input variables, similar to supervised learning. However, unlike supervised learning, the algorithm is trained on a dataset that contains both labeled and unlabeled data.

<br/>

## Reinforcement Machine Learning
![Basic Diagram of Reinforcement Learning - KDNuggets](https://editor.analyticsvidhya.com/uploads/197201.jpg)
Reinforcement Learning is a type of machine learning where an agent learns to make decisions by interacting with an environment. The agent takes actions and receives feedback in the form of rewards or penalties from the environment. The goal of reinforcement learning is for the agent to learn the optimal strategy or policy that maximizes cumulative rewards over time. It's commonly used in scenarios where there is no explicit dataset available, and the agent needs to learn from its own experiences, such as in game playing, robotics, and autonomous vehicle control.

<br/>

![Reinforcement Learning Example - KDNuggets](https://editor.analyticsvidhya.com/uploads/496302.jpg)
Example - You can see a dog and a master. Let’s imagine you are training your dog to get the stick. Each time the dog gets a stick successfully, you offered him a feast (a bone let’s say). Eventually, the dog understands the pattern, that whenever the master throws a stick, it should get it as early as it can to gain a reward (a bone) from a master in a lesser time.

<table border="2">
    <tr>
        <td colspan="4" align="center">Algorithms</td>
    </tr>
    <tr>
        <td colspan="2" align="center">Supervised</td>
        <td rowspan="2" align="center">Unsupervised</td>
        <td rowspan="2" align="center">Reinforcement</td>
    </tr>
    <tr>
        <td>Regression</td>
        <td>Classification</td>
    </tr>
    <tr>
        <td>Linear Regression</td>
        <td>Naive Bayes</td>
        <td>K-Means Clustering</td>
        <td>Q-Learning</td>
    </tr>
    <tr>
        <td>Neural Network Regression</td>
        <td>Decision Trees</td>
        <td>Mean-shift Clustering</td>
        <td>R Learning</td>
    </tr>
    <tr>
        <td>Support Vector Regression</td>
        <td>Support Vector Machines</td>
        <td>DBSCAN Clustering</td>
        <td>TD Learning</td>
    </tr>
    <tr>
        <td>Decision Tree Regression</td>
        <td>Random Forest</td>
        <td>Agglomerative Hierarchical Clustering</td>
        <td></td>
    </tr>
    <tr>
        <td>Lasso Regression</td>
        <td>K-Nearest Neighbors</td>
        <td>Gaussian Mixture</td>
        <td></td>
    </tr>
    <tr>
        <td>Ridge Regression</td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>
