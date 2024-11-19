# Project Writeup
* Goals -
* Data -
* Analysis-
  
## EDA
* Descriptive statistics like mean, median, range, correlations
* Data visualizations for univariate and multivariate exploration
* Text explaining insights gained from exploration

### Inspecting and Transforming the Dataset

Several of the raw data tables had records with some missing data. Visualization indicated that most of the missing data was missing at random (MAR). Because this data was MAR and formed only a small percentage of the overall data, deletion seemed appropriate. Instead of fully deleting the missing rows, I separated the rows with missing data into their own table. This way, an analytics team can inspect the missing data themselves if they want, and we can keep track of how much data is missing as the cleaned database was updated.

Some of the missing data was structurally missing, corresponding to students who had never started any courses before cancelling their subscription. I handled these rows by introducing a new category for those students, so an analytics team can easily study subscribers who cancel before making any use of the product.

In addition to missing data, the student's contact information was stored in a dictionary, which needed to be converted to flat columns with the correct data types.

Lastly, I added new columns to assist an analytics team in filtering the subscriber population. For example, I used the subscriber birth date to create age and decade categories, so an analytics team can more easily see if those demographic attributes impact subscribers.
