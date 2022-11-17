# Comparison between 6 different types of categorical data encoding


## Label Encoding
Label encoding maps each unique instance in a column to a unique number

![image](https://user-images.githubusercontent.com/109832303/202396397-eb331d97-13ac-4dc4-83a7-bb9bc679adbe.png)

#### When to use: 
- Used to encode the target variable
- Single column



## Ordinal Encoding
Same as labeled encoding but used on the input data and can cover multiple columns


#### When to use: 
- Used when there exists an order between the data
- When the amount of data is too large to be used with one hot encoding
- Used to encode the input variables
- multiple columns



## One-Hot Encoding
One-hot encoding adds a column for each unique feature and fills it with either 1 or 0 depending if it's relevent in that row.
![image](https://user-images.githubusercontent.com/109832303/202398911-e20745e5-7073-4e99-9993-814e63f744d3.png)

#### When to use: 
- Used when there is no order between the data
- When the amount unique features of is relatively small. (Remember 1 new column for each unique feature)
- if the presence of redundant information is acceptable
- Multiple columns


## Frequency Encoding
Encodes feature to the relative number of times it has shown up in the desired column. 
![image](https://user-images.githubusercontent.com/109832303/202403681-53e6bec7-9743-4e57-9591-8682a69e17f6.png)

#### When to use: 
- If the number of instances of each type is somehow relevant to the target variable


## Binary Encoding
A mix between Ordinal and One-Hot encoding. Uses Ordinal encoding first then converts the number into Binary and splits it into columns.
![image](https://user-images.githubusercontent.com/109832303/202405344-c70a07c8-1b3d-441f-b7d4-94b13ea40df2.png)

#### When to use: 
- A better solution to One-Hot Encoding if number of features is large. (Produces less new columns)


## Target Mean Encoding
Calculate the mean of all the target variables with the same category. Then replace all the relevant categories with that value.
![image](https://user-images.githubusercontent.com/109832303/202406720-05b08a5b-d48e-4259-8d17-35a220d55a96.png)![image](https://user-images.githubusercontent.com/109832303/202407157-30852bac-c06f-423e-950b-b9fd06e0cd06.png)



#### When to use: 
- A better solution to One-Hot Encoding if number of features is large. (Does not add redundant columns)
- The tradeoff is that is is known to cause overfitting.


