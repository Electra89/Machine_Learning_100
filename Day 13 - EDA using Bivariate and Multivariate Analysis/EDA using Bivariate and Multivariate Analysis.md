
#   EDA using Bivariate and Multivariate Analysis
<br>


### Bivariate and Multivariate Plots for Categorical and Numerical Data

#### Bivariate Plots

1.  **Scatter Plot (Numerical - Numerical)**
    
    -   **Description**: Displays the relationship between two numerical variables by plotting data points on a two-dimensional graph.
    -   **Methods for Creation**:
        -   `plt.scatter()`
        -   `sns.scatterplot()`
        -   `pd.DataFrame.plot.scatter()`
2.  **Line Plot (Numerical - Numerical)**
    
    -   **Description**: Shows trends over time or continuous data by connecting data points with a line.
    -   **Methods for Creation**:
        -   `plt.plot()`
        -   `sns.lineplot()`
        -   `pd.Series.plot.line()`
3.  **Box Plot (Categorical - Numerical)**
    
    -   **Description**: Summarizes the distribution of a numerical variable for each category, highlighting the median, quartiles, and potential outliers.
    -   **Methods for Creation**:
        -   `sns.boxplot()`
        -   `plt.boxplot()`
        -   `pd.DataFrame.boxplot()`
4.  **Violin Plot (Categorical - Numerical)**
    
    -   **Description**: Combines box plot and density plot to show the distribution of a numerical variable across different categories.
    -   **Methods for Creation**:
        -   `sns.violinplot()`
        -   `plotly.express.violin()`
5.  **Bar Plot (Categorical - Numerical)**
    
    -   **Description**: Displays the average (or other aggregate) of a numerical variable for each category.
    -   **Methods for Creation**:
        -   `sns.barplot()`
        -   `plt.bar()`
        -   `pd.DataFrame.plot.bar()`
6.  **Count Plot (Categorical - Categorical)**
    
    -   **Description**: Shows the frequency of occurrences of combinations of two categorical variables.
    -   **Methods for Creation**:
        -   `sns.countplot()` with `hue` parameter
7.  **Heatmap (Categorical - Categorical)**
    
    -   **Description**: Uses color to represent the frequency or magnitude of combinations of two categorical variables.
    -   **Methods for Creation**:
        -   `sns.heatmap()` with a contingency table

#### Multivariate Plots

1.  **Pair Plot (Numerical - Numerical)**
    
    -   **Description**: Creates a matrix of scatter plots for all pairs of numerical variables, along with histograms or density plots on the diagonal.
    -   **Methods for Creation**:
        -   `sns.pairplot()`
2.  **Facet Grid (Categorical - Numerical/Numerical)**
    
    -   **Description**: Creates subplots based on values of one or more categorical variables, displaying relationships between numerical variables.
    -   **Methods for Creation**:
        -   `sns.FacetGrid()`
3.  **Heatmap (Categorical - Numerical/Numerical)**
    
    -   **Description**: Uses color to represent values in a matrix format, often used for correlation matrices or pivot tables.
    -   **Methods for Creation**:
        -   `sns.heatmap()`
        -   `plt.imshow()`
4.  **Bubble Plot (Numerical - Numerical - Numerical)**
    
    -   **Description**: Similar to a scatter plot but with an additional variable represented by the size of the bubbles.
    -   **Methods for Creation**:
        -   `plt.scatter()` with `s` parameter
5.  **3D Scatter Plot (Numerical - Numerical - Numerical)**
    
    -   **Description**: Extends a scatter plot into three dimensions to visualize the relationship between three numerical variables.
    -   **Methods for Creation**:
        -   `mpl_toolkits.mplot3d.Axes3D.scatter()`
        -   `plotly.express.scatter_3d()`
6.  **Parallel Coordinates Plot (Categorical - Numerical)**
    
    -   **Description**: Represents multi-dimensional numerical data across multiple categories using parallel axes.
    -   **Methods for Creation**:
        -   `pd.plotting.parallel_coordinates()`
        -   `plotly.express.parallel_coordinates()`