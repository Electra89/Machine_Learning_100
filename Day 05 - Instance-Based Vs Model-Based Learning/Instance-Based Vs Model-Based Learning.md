
#   Instance-Based Vs Model-Based Learning



## Model-Based Learning

Model-based learning involves creating a mathematical model that can predict outcomes based on input data. The model is trained on a large dataset and then used to make predictions on new data. The model can be thought of as a set of rules that the machine uses to make predictions.

In model-based learning, the training data is used to create a model that can be generalized to new data. The model is typically created using statistical algorithms such as linear regression, logistic regression, decision trees, and neural networks. These algorithms use the training data to create a mathematical model that can be used to predict outcomes.

![](https://miro.medium.com/v2/resize:fit:700/1*yXSPjsFDaZyFkCtkxRXRrA.png)


### Advantages of Model-Based Learning

1.  **Faster predictions**: Model-based learning is typically faster than instance-based learning because the model is already created and can be used to make predictions quickly.
2.  **More accurate predictions**: Model-based learning can often make more accurate predictions than instance-based learning because the model is trained on a large dataset and can generalize to new data.
3.  **Better understanding of data**  Model-based learning allows you to gain a better understanding of the relationships between input and output variables. This can help identify which variables are most important in making predictions.

### Disadvantages of Model-Based Learning

1.  **Requires a large dataset**: model-based learning requires a large dataset to train the model. This can be a disadvantage if you have a small dataset.
2.  **Requires expert knowledge**: Model-based learning requires expert knowledge of statistical algorithms and mathematical modeling. This can be a disadvantage if you don’t have the expertise to create the model.
3.  **Requires expert knowledge**: Model-based learning requires expert knowledge of statistical algorithms and mathematical modeling. This can be a disadvantage if you don’t have the expertise to create the model.

##  Instance-Based Learning

Instance-based learning involves using the entire dataset to make predictions. The machine learns by storing all instances of data and then using these instances to make predictions on new data. The machine compares the new data to the instances it has seen before and uses the closest match to make a prediction.

In instance-based learning, no model is created. Instead, the machine stores all of the training data and uses this data to make predictions based on new data. Instance-based learning is often used in pattern recognition, clustering, and anomaly detection.

![](https://miro.medium.com/v2/resize:fit:700/1*qscVGbR4Lc0_0hu2TADVdg.png)

### Advantages of Instance-Based Learning

1.  **No need for model creation**: Instance-based learning doesn’t require creating a model, which can be an advantage if you don’t have the expertise to create the model.
2.  **Can handle small datasets**: Instance-based learning can handle small datasets because it doesn’t require a large dataset to create a model.
3.  **More flexibility**: Instance-based learning can be more flexible than model-based learning because the machine stores all instances of data and can use this data to make predictions.

### Disadvantages of Instance-Based Learning

1.  **Slower predictions**: Instance-based learning is typically slower than model-based learning because the machine has to compare the new data to all instances of data in order to make a prediction.
2.  **Less accurate predictions:**  Instance-based learning can often make less accurate predictions than model-based learning because it doesn’t have a mathematical model to generalize from.
3.  **Limited understanding of data:**  Instance-based learning doesn’t provide as much insight into the relationships between input and output variables as model-based learning does.



<table  border="2">
    <tr>
        <td colspan="2" align="center"><b>Comparison between Model-Based vs Instance-Based</b></td>
    </tr>
    <tr>
        <th>Usual/Conventional Machine Learning</th>
        <th>Instance Based Learning</th>
    </tr>
    <tr>
        <td>Prepare the data for model training</td>
        <td>Prepare the data for model training. No difference here</td>
    </tr>
    <tr>
        <td>Train model from training data to estimate model parameters i.e. discover patterns</td>
        <td>Do not train model. Pattern discovery postponed until scoring query received</td>
    </tr>
    <tr>
        <td>Store the model in suitable form</td>
        <td>There is no model to store</td>
    </tr>
    <tr>
        <td>Generalize the rules in form of model, even before scoring instance is seen</td>
        <td>No generalization before scoring. Only generalize for each scoring instance individually as and when seen</td>
    </tr>
    <tr>
        <td>Predict for unseen scoring instance using model</td>
        <td>Predict for unseen scoring instance using training data directly</td>
    </tr>
    <tr>
        <td>Can throw away input/training data after model training</td>
        <td>Input/training data must be kept since each query uses part or full set of training observations</td>
    </tr>
    <tr>
        <td>Requires a known model form</td>
        <td>May not have explicit model form</td>
    </tr>
    <tr>
        <td>Storing models generally requires less storage</td>
        <td>Storing training data generally requires more storage</td>
    </tr>
</table>
