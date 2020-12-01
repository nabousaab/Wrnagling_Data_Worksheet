# Wrnagling_Data_Worksheet
This works sheet should cover step-by-step all details covering 'assess' and 'clean' process for data Wrangling


## Intoduction
This worksheet should cover a good part of the 'assess' and clean process for teh wrnagling data
This is also part of udacity Worksheet projects in teh nano degree
For this part we will not cover the 'gather' process, however, we will focus on the 'assess' and 'clean' process and I believe it is more improtant to generate a clean dataframe for our future works 

## Important notes
- We will use both visual and programatic assessment for the data
- We will focus on Programmatic: Data Cleaning 
  - Define
  - Code 
  - Test
- This will help us plot and recognise quality issues and tidiness isses within the data 
- Then we will go ahead and mark all our quality and tidy observation in this worksheet



## DataFrame needed 
- pandas
- numpy


## DataFrame files 
This should include three files, that we will intent to clean and then combine or merge at a later stage in this worksheet
- patients 
- treatments 
- adverse_reactions 


# Gather and import data

````

import pandas as pd
import pandas as np
patients = pd.read_csv('patients.csv')
treatments = pd.read_csv('treatments.csv')
adverse_reactions = pd.read_csv('adverse_reactions.csv')


````
- We have imported pandas as we will need it later on for during the 'clean' process


# Assess

````

patients


````


````

treatments


````


````

adverse_reactions


````

### At this stage we can start with our visial observation and 'assessment' for the DataFrames to be able to understand and plot teh Quality and Tidy data issues.


````

patients.info()

````

````

treatments.info()

````

````

adverse_reactions.info()


````


````

patients.surname.value_counts()

````

- We will notice some repetition and duplication for some names such as Doe              6
  - Jakobsen         3
  - Taylor           3
  - Kadyrov          2



````

patients.address.value_counts()

````

- This should confirm that the same name under the same address is been duplicated; example 
  - 123 Main Street                  6
  - 648 Old Dear Lane                2



````

patients[patients.address.duplicated()]

````

````

patients.weight.sort_values()

````

- We have noticed that there is an issue with same weight registration
- Propably these were registered as KG instead of LB
- It is for patient 210

   - 210     48.8
   - 459    102.1
   - 335    102.7
   - 74     103.2

````

weight_lbs = patients[patients.surname == 'Zaitseva'].weight * 2.20462
height_in = patients[patients.surname == 'Zaitseva'].height
bmi_check = 703 * weight_lbs / (height_in * height_in)
bmi_check

````

````

patients[patients.surname == 'Zaitseva'].bmi

````


- Checking it using the above code to change kg to lb
- This gices us same petient reult 
    - 210    19.055827


````

sum(treatments.auralin.isnull())

````

````

sum(treatments.novodra.isnull())

````

````

all_columns = pd.Series(list(patients) + list(treatments) + list(adverse_reactions))
all_columns[all_columns.duplicated()]


````

- This is a better programmatic way to discover duplicated names and addresses, that need to be cleaned later on


````

patients[patients['address'].isnull()]

````

- Checking for missing address 


````

patients.describe()


````

````

treatments.describe()

````

````

patients.sample(5)

````



