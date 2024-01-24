# Bike Sales Project

Bike Sales Project is an Excel project that demonstrates demographics of customers who bought or did not buy bikes and showcases as a Dashboard, uses tools like Pivot Tables and Pivot Charts.

## Dataset

The dataset can be found from the attached 'Bike Sales Project' excel file. The file includes several sheets:
* 'Bike_buyers' sheet contains the original dataset.
* 'Clean dataset' sheet contains the dataset after cleaning has been performed.
* 'Pivot Table' sheet contains Pivot tables that quickly summarise key info that I want to show in the final Dashboard.
* 'Dashboard' sheet contains the final Dashboard overviewing the Bike Sales analysis and insights.

## Data cleaning
Steps taken:
* Created a seperate worksheet called 'Clean Data' and copied all data over just in case I mess up the original dataset
* Removed duplicates: Data Ribbon > Remove Duplicates
* Spell out the full form Female and Male instead of F/M in the original dataset so viewers can understand what F/M referred to.
* M appears to be in both columns Marital Status and Gender and not sure what it referring to - Selecting the whole column of Marital Status > Home ribbon > Find & Select > Find: M > Tick Match case > Search By Columns > Replace with: Married
* S also in short form - Selecting the whole column of Marital Status and click Find & Select > Home ribbon > Find & Select > Find: S > Tick Match case > Search By Columns > Replace with: Single
* Marital Status abbreviations: Replace M with Married, and replace S with Single - Selecting the whole column and click Find & Select > Home ribbon > Find & Select > Find: M/F > Tick Match case > Search By Columns > Replace with: Male/Female
* Income: change format to currency, remove last 2 decimals
* Click Filter Drop-down from each columns to see if there is any weird data that needs to work on
* Age not in age brackets, better to condense it and make it better to understand using IF statement with <31 classified as 'Adolescent', >= 31 classified as 'Middle Age', >55 classified as 'Old'

```bash
=IF(L2>55;"Old";IF(L2>=31;"Middle Age";IF(L2<31;"Adolescent";"Invalid")))
```

## Build Pivot Tables

Average Income of who bought and did not buy bikes:
* Drag Income to Values
* Gender to Row
* Purchased Bikes to Columns
* Insert Charts - Clustered Columns
* Add titles to axis x and axis y
  
Gender | Purchased Bikes? | Blank
--- | --- | ---
Blank | Yes | No
--- | --- | ---
Female | $ 53,440 | $ 55,774
Male | $ 56,208 | $ 60, 124

Average of Income	Column Labels	
Row Labels	No	Yes
Female	 $53.440 	 $55.774 
Male	 $56.208 	 $60.124 ![image](https://github.com/minnguyen2311/bike-sales-project/assets/110536543/532c2c72-4ef3-4763-a360-57744c283430)

<img width="234" alt="Screen Shot 2024-01-24 at 10 57 05 pm" src="https://github.com/minnguyen2311/bike-sales-project/assets/110536543/f5a69f0b-40d3-4f53-a193-acec14d4082b">

<img width="392" alt="image" src="https://github.com/minnguyen2311/bike-sales-project/assets/110536543/0159b0bd-a124-4472-9bd7-6f1dc794bc5e">

Distance of who bought and did not buy bikes:
* Drag Distance to Rows
* Drag Purchased Bikes to Values to count how many No/Yes
* Drag Purchased Bikes to Columns to separate Yes/No
* Insert Charts - Line Graph

(insert image)

Age Brackets of who bought and did not buy bikes:
* Drag Age Brackets to Rows
* Drag Purchased Bikes to Values to count how many No/Yes
* Drag Purchased Bikes to Columns to separate Yes/No
* Insert Charts - Line Graph

(insert image)

## Dashboard
* Added heading panel
* Copied and pasted the pivot charts over
* Rearranged pivot charts
* Added slicers for filters and better analysis

(insert image)
