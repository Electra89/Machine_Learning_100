#  EDA using Univariate Analysis
<br>

##  Categorical Data: Unveiling the Power of Labels

-   **Definition**: Qualitative data with distinct categories or labels, lacking numerical value.
-   **Subtypes**:
    -   **Nominal**: No specific order or hierarchy.
    -   **Ordinal**: Predefined order among categories.
-   **Applications**: Customer segmentation, sentiment analysis, market research.
-   **Utility**: Classifies and groups data points to reveal patterns and trends.

## Numerical Data: Unleashing the Power of Numbers

-   **Definition**: Quantitative measurements or values.
-   **Subtypes**:
    -   **Discrete**: Whole numbers or counts.
    -   **Continuous**: Range of real numbers from measurements.
-   **Applications**: Statistical analysis, predictive modeling, machine learning.
-   **Utility**: Extracts meaningful information, uncovers relationships, makes predictions.

<br>



> ### Univariate Plots for Categorical Data

1.  **Bar Chart**
    -   **Description**: Depicts the distribution of a categorical variable. Nominal categories are commonly reordered by frequency, while ordinal categories are left unordered.
    -   **Methods for Creation**:
        -   `sns.countplot()`
        -   `sns.barplot()`
        -   `plt.bar()`
3.  **Pie Chart**
    
    -   **Description**: Shows the relative proportions of categories as slices of a pie, where each slice represents a category's contribution to the whole.
    -   **Methods for Creation**:
        -   `plt.pie()`
        -   `pd.Series.plot.pie()`
4.  **Count Plot**
    
    -   **Description**: Similar to a bar chart, but specifically used within data analysis libraries to display the count of occurrences for each category.
    -   **Methods for Creation**:
        -   `sns.countplot()`

> ### Univariate Plots for Numerical Data

1.  **Histogram**
    
    -   **Description**: Displays the distribution of numerical data by showing the frequency of data points within specified ranges (bins).
    -   **Methods for Creation**:
        -   `plt.hist()`
        -   `sns.histplot()`
        -   `pd.Series.plot.hist()`
2.  **Box Plot**
    
    -   **Description**: Summarizes numerical data using the median, quartiles, and potential outliers, providing insight into the data's spread and any anomalies.
    -   **Methods for Creation**:
        -   `sns.boxplot()`
        -   `plt.boxplot()`
        -   `pd.Series.plot.box()`
3.  **Density Plot**
    
    -   **Description**: Estimates the probability density function of numerical data, providing a smoothed version of the histogram to show the data's distribution.
    -   **Methods for Creation**:
        -   `sns.kdeplot()`
        -   `pd.Series.plot.kde()`

4.  **Violin Plot**

-   **Description**: Combines aspects of box plots and density plots to provide a detailed view of the distribution of numerical data. The width of the plot represents the density of the data at different values, offering insight into the data’s distribution, including multimodal distributions.
-   **Methods for Creation**:
    -   `sns.violinplot()`
    -   `plotly.express.violin()`
    -   `alt.Chart().mark_violin()` (using Altair library)
