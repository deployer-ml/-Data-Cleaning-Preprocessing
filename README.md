# -Data-Cleaning-Preprocessing



### 🔹 Step 1: Import Required Libraries

All necessary Python libraries (like `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`, etc.) are imported at the beginning to support data manipulation, visualization, and transformation.

### 🔹 Step 2: Load the Dataset

The dataset is loaded using `Titanic-Dataset.csv` or similar methods, and basic info (`head()`, `info()`, `shape`, `describe()`) is reviewed.

### 🔹 Step 3: Identify Missing Values

Missing values are identified using:

```python
df.isnull().sum()
df.isna().mean()
```

### 🔹 Step 4: Exploratory Data Analysis (EDA)

* Visualize distributions (`sns.histplot`, `sns.boxplot`)
* Correlation matrix (`df.corr()`)
* Target variable analysis

### 🔹 Step 5: Missing Value Treatment

Depending on the data type and business logic:

* Numerical: Impute with mean/median or use KNNImputer


### 🔹 Step 6: Outlier Detection & Handling

* Use IQR or Z-score method
* Visual methods: `boxplot`, `scatterplot`
* Optionally cap or remove outliers

### 🔹 Step 7: Encoding Categorical Variables

* Label Encoding for ordinal variables
* One-Hot Encoding for nominal variables using:

```python
pd.get_dummies(df, drop_first=True)
```

### 🔹 Step 8: Feature Scaling / Normalization

Normalize or standardize numerical features:

```python
from sklearn.preprocessing import MinMaxScaler, StandardScaler
```

