#  Batch Machine Learning (Offline) Vs Machine Learning

<br>

# Batch (Offline) Machine Learning
Batch learning is a conventional way of training an ML model. In which you use all the data to train the model. you utilize all of your data.

**There is no incremental training**. incremental training is a learning technique where a model is updated and improved over a time by training it on a new data while retaining from previous learned patterns

When you are working on a real-world problem. The data will be huge. generally it is. when you are going to train such a huge amount of data on a server.**It would be costly and time consuming.**

In batch learning, you take up your entire data. You train your machine learning model on an offline system. Once the model is trained, you deploy it on the server.

![](https://miro.medium.com/v2/resize:fit:700/1*-HJtPmbHiEAPK_35YZ3MTQ.png)

## **Problems with batch learning:-**

Your model is static, which means it doesn’t update or learn from new data. the problem with this approach is your business scenario is evolving     

The biggest problem with batch learning is that you need to retrain your model frequently; generally, people do this periodically. What they do is take the updated data, merge it with the old data, and retrain the model with the whole new data. Once the model is trained, you test it again and put it on the server.

Basically this process which happens in cycle Repeats again and again in the given period. This period could be 24 hr period, weekly or monthly or 6 monthly

![](https://miro.medium.com/v2/resize:fit:700/1*2AA1g-gKB8BC-nFMSBfeMg.png)


## **Disadvantages of batch learning:-**

1.  **Handling large amounts of data**: Batch learning requires loading the entire dataset into memory for training. This becomes a challenge when dealing with large datasets that exceed the available memory capacity. In such cases, it may not be feasible to load the entire dataset at once, leading to potential memory errors and system crashes. Additionally, the processing time for training increases as the dataset size grows, making it impractical for real-time or time-sensitive applications
2.  **Hardware limitations**: Batch learning can be computationally expensive, especially when dealing with complex models or large datasets. Training a model on a single machine may take a significant amount of time and may require high-performance hardware, such as GPUs or specialized processing units. However, not all users or organizations have access to such resources, limiting the practicality and scalability of batch learning in resource-constrained environments.
3.  **Availability constraints**: In some scenarios, obtaining the entire dataset required for batch learning may not be feasible or practical. For instance, data may be continuously generated or collected in streams, making it impossible to accumulate the complete dataset in advance. Furthermore, there may be situations where the data is distributed across multiple sources, making it difficult to centralize and train on all the data simultaneously. In such cases, alternative learning approaches, like online learning or mini-batch learning, are preferred.

# Online Machine  Learning
Online learning is quite unlike batch learning, which is done incrementally.
In  **online learning**  is that. You feed data to your model in small batches, sequentially. These batches are called mini batches.

After, each batch of training, your model gets better. since these batches are small chunks of data. so you can perform this training on server (in production)

That’s why it is called online learning means your model is getting trained when your model is on server

![](https://miro.medium.com/v2/resize:fit:700/1*078YorTPCYcFEtTrb-Wy8Q.png)

## **When to use:-**

1) **where there is a Concept drift**:-

Sometimes what happens is that you create a machine learning model for a problem. The nature of the problem keeps changing over time. There, you may use online learning.

for example, the stock market, e-commerce website

2) **Cost effective**:-

wherever you want to save money. If you are, working on large-scale batch learning will make you spend more money. It would be great if you use online learning It will be cost effective

3) **faster solution**-

This thing is fast, no doubt, because you are doing training in mini batches. Training is fast. Overall, you have to make your system fast; this is the solution.


<br>
<table border="2">
    <tr>
        <td colspan="3" align="center"><b>Batch Learning VS Online Learning</b></td>
    </tr>
    <tr>
        <th>Features</th>
        <th>Offline Learning</th>
        <th>Online Learning</th>
    </tr>
    <tr>
        <td>Complexity</td>
        <td>Less complex as model is constant</td>
        <td>Dynamic complexity as the model keeps evolving over time</td>
    </tr>
    <tr>
        <td>Computational Power</td>
        <td>Fewer computations, single time batch-based training</td>
        <td>Continuous data ingestions result in consequent model refinement computations</td>
    </tr>
    <tr>
        <td>Use in Production</td>
        <td>Easier to implement</td>
        <td>Difficult to implement and manage</td>
    </tr>
    <tr>
        <td>Applications</td>
        <td>Image Classification or anything related to Machine Learning - where data patterns remains constant without sudden concept drifts</td>
        <td>Used in finance, economics, health where new data patterns are constantly emerging</td>
    </tr>
    <tr>
        <td>Tools</td>
        <td>Industry proven tools. E.g. Sci-kit, TensorFlow, Pytorch, Keras, Spark Mlib</td>
        <td>Active research/New project tools: E.g. MOA, SAMOA, scikit-multiflow, streamDM</td>
    </tr>
</table>



