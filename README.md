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

1. Average Income of who bought and did not buy bikes:
* Drag Income to Values field
* Drag Gender to Row field
* Drag Purchased Bikes to Columns field
* Insert Charts - Clustered Columns
* Add titles to axis x and axis y
* Add heading
  
![image](https://github.com/minnguyen2311/bike-sales-project/assets/110536543/6adde6de-c523-4fb2-bd0e-a5590b536ed9)

<img width="392" alt="image" src="https://github.com/minnguyen2311/bike-sales-project/assets/110536543/0159b0bd-a124-4472-9bd7-6f1dc794bc5e">

2. Distance of who bought and did not buy bikes:
* Drag Distance to Rows field
* Drag Purchased Bikes to Values to count how many No/Yes
* Drag Purchased Bikes to Columns to separate Yes/No
* Insert Charts - Line Graph
* Add titles to axis y
* Add heading

![image](https://github.com/minnguyen2311/bike-sales-project/assets/110536543/98c9a2e8-338c-4c47-8d08-14583fe50a4d)

<img width="391" alt="image" src="https://github.com/minnguyen2311/bike-sales-project/assets/110536543/8ec3048a-b36d-402b-a0fb-c911b042cfe8">

3. Age Brackets of who bought and did not buy bikes:
* Drag Age Brackets to Rows field
* Drag Purchased Bikes to Values to count how many No/Yes
* Drag Purchased Bikes to Columns to separate Yes/No
* Insert Charts - Line Graph
* Add titles to axis y
* Add heading

![image](https://github.com/minnguyen2311/bike-sales-project/assets/110536543/812b879c-723f-4661-893c-a04503626964)

<img width="394" alt="image" src="https://github.com/minnguyen2311/bike-sales-project/assets/110536543/96fc8689-9680-47df-9459-eea8e64cbfa6">

4. Ocupation groups of of who bought and did not buy bikes:
* Drag Occupation to Rows field
* Drag Ocupation to Values to count how many No/Yes per occupation groups
* Drag Purchased Bikes to Columns to separate Yes/No
* Insert Charts - Clustered Bar
* Add heading

![image](https://github.com/minnguyen2311/bike-sales-project/assets/110536543/42b521ed-a196-4a70-a5c5-4f386229ec17)

<img width="797" alt="image" src="https://github.com/minnguyen2311/bike-sales-project/assets/110536543/b8f2baff-6684-4e61-a3c6-eed1e9ce112d">
   
## Bike Sales Dashboard
* Added heading panel
* Copied and pasted the pivot charts over
* Rearranged pivot charts
* Added slicers for filters and better analysis
													
![image](https://github.com/minnguyen2311/bike-sales-project/assets/110536543/01378cdd-6f3b-4e5b-afa4-737fd6b065dd)

## Findings

