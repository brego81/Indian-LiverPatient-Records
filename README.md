# Indian-Liver-Patient-Records
A binary classification probelm
### credits https://www.kaggle.com/uciml/indian-liver-patient-records

### Content
This data set contains 416 liver patient records and 167 non liver patient records collected from North East of Andhra Pradesh, India. The "Dataset" column is a class label used to divide groups into liver patient (liver disease) or not (no disease). This data set contains 441 male patient records and 142 female patient records.

Any patient whose age exceeded 89 is listed as being of age "90".

### Columns:

- Age of the patient
- Gender of the patient
- Total Bilirubin
- Direct Bilirubin
- Alkaline Phosphotase
- Alamine Aminotransferase
- Aspartate Aminotransferase
- Total Protiens
- Albumin
- Albumin and Globulin Ratio
- Dataset: field used to split the data into two sets (patient with liver disease, or no disease) [TARGET]

### Target definition
To properly set the target variable we sugget to:

  1 = no disease --> 0
  
  2 = disease    --> 1
```
import pandas as pd
data = pd.read_csv('https://raw.githubusercontent.com/brego81/Indian-LiverPatient-Records/main/indian_liver_patient.csv')
data.Dataset = data.Dataset.map({1:0, 2:1})
data.head(20)
```
