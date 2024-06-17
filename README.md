# Brief of the Approach and method
  1. Handling of missing values using the model of IterativeImputer that accepts the missing values, and encoding using one hot encoder
  <br>
  2. Selection of ML models - RandomForestClassifier and GradientBoostingClassifier as they can haldle various data types and it can handle missing values directly.
  <br>
  3. Using LinearRegression rather than Bayesianridge as it converged better to fit the data
  <br>
  4. We create two separate pipelines because we have two target variables (xyz_vaccine and seasonal_vaccine) to predict.
   <br>
  Each pipeline includes:
  <br>
       1. A preprocessor that handles both numerical imputation and categorical encoding.
     <br>
       2. A model that will make predictions based on the processed data.
<br>
 5. we recieved two ROC AUC scores- one for each vaccine and a final as avg of these two.
    <br>
 6. we use ROC AUC because it helps to predict the probabilities on many present columsns and to know how well the model performs in two separate groups.

