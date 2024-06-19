# Encoding Categorical Data
<br>
Encoding categorical data is a common preprocessing step in machine learning, particularly for algorithms that require numerical input.

- There are different types  encoding methods:

    - **Nominal Encoding( OHE ):**  Great for many categories, creates new binary features (1 for the category, 0 for others).
    - **Label Encoding:**  Simple, assigns a number to each category, but assumes order matters (which might not be true).
    - **Ordinal Encoding:**  Similar to label encoding, but only use it if categories have a natural order (like low, medium, high).
    
 > Ordinal Encoding and Label Encoding being two of the primary techniques.

---

### >  Nominal Encoding (One-Hot Encoding - OHE)

Nominal Encoding, often implemented as One-Hot Encoding (OHE), is used for categorical data where categories have no inherent order or ranking. Each category is converted into a new binary column .These newly created binary features are known as **Dummy variables.** The number of dummy variables depends on the levels present in the categorical variable. Here's an example:

**Example: Colors**

-   Categories: Red, Green, Blue

Using One-Hot Encoding:

-   Red -> [1, 0, 0]
-   Green -> [0, 1, 0]
-   Blue -> [0, 0, 1]

In this method, each category gets a separate binary column. It is useful when there is no ordinal relationship between categories and each category should be treated independently.

---
### > Ordinal Encoding

**Ordinal Encoding** is used for categorical data where the categories have an inherent order or ranking. This method assigns each category a unique integer value based on their order. For example, if you have a feature representing education levels:

-   High School
-   Bachelor's
-   Master's
-   PhD

Using Ordinal Encoding, these might be encoded as:

-   High School -> 1
-   Bachelor's -> 2
-   Master's -> 3
-   PhD -> 4

The encoding preserves the ordinal nature of the data, which can be important for certain models that leverage this order. However, it can introduce issues in models that assume equidistant intervals between the values.

---

### > Label Encoding

**Label Encoding** assigns a unique integer to each category, but it does not consider any order. It is typically used for Target Values, where the categories do not have any implicit order. For example, for a feature representing colors:

-   Red
-   Blue
-   Green

Using Label Encoding, these might be encoded as:

-   Red -> 0
-   Blue -> 1
-   Green -> 2

Label Encoding is straightforward and efficient but can be problematic if the encoded values are misinterpreted as having an ordinal relationship by certain machine learning algorithms.

> This transformer should be used to [encode target values](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.LabelEncoder.html), _i.e._  `y`, and not the input `X`.
---

### Choosing Between Ordinal and Label Encoding

-   **Ordinal Encoding** is appropriate when there is a clear, meaningful order to the categories.
-   **Label Encoding** is suitable when there is no meaningful order to the categories.