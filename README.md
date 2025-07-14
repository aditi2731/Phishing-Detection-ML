## Phishing continues to prove one of the most successful and effective ways for cybercriminals to defraud us and steal our personal and financial information.
## Our growing reliance on the internet to conduct much of our day-to-day business has provided fraudsters with the perfect environment to launch targeted phishing attacks. The phishing attacks taking place today are sophisticated and increasingly more difficult to spot. A study conducted by Intel found that 97% of security experts fail at identifying phishing emails from genuine emails.

## I built an MLsystem that can analyze a website and determine whether it’s legitimate or a phishing scam .

# The Machine Learning Process
### Step 1: Exploring the Data
I started with a dataset profiling thousands of websites. Using automated tools, I uncovered patterns humans might miss. This process is also called Exploratory Data Analysis.

### Step 2: Cleaning the Dataset
* A majority of the fields are numeric, which is perfect for this use case. However there are two that are not, “url” and “status”.
* URL is not needed for modeling purposes so we can drop that field.
* The status field is text, but it only contains one of two values “legitimate” or “phishing”. To solve this issue we will encode these values numerically.
* legitimate will equal 0.
* phishing will equal 1.

### Step 3: Training Multiple AI Models
Instead of betting on one algorithm, I trained three models to compete:

* Logistic Regression — Methodical and rule‑based.
* Random Forest — Experienced, ensemble‑based detective.
* SVM — Pattern‑recognition specialist that draws clear boundaries
Each model was trained on 80% of the data and tested on the remaining 20% to ensure they generalized well to unseen samples.

### Step 4: Refining Model
Random Forest emerged as the winner — but I wanted exceptional. So I used GridSearchCV to tune hyperparameters (like number of trees, max depth, max features, etc.). Over 1,000 configurations were tested.

### Step 5: Saving the best Model
Since the resulting model is highly accurate with fewer false positive and false negatives, we will go ahead and save the model’s output.

