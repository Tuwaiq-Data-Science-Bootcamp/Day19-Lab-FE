# Comparison between 6 different types of categorical data encoding


## Label Encoding
Label encoding maps each unique instance in a column to a unique number

![image](https://user-images.githubusercontent.com/109832303/202396397-eb331d97-13ac-4dc4-83a7-bb9bc679adbe.png)

#### When to use: 
- When order of the data does not matter. (The machine model might misunderstand that 0<1<2<3)
- When the amount of data is too large to be used with one hot encoding
- Used to encode the target variable



## One-Hot encoding
One-hot encoding adds a column for each unique feature and fills it with either 1 or 0 depending if it's relevent in that row.
![image](https://user-images.githubusercontent.com/109832303/202398911-e20745e5-7073-4e99-9993-814e63f744d3.png)

#### When to use: 
- When the order matters
- When the amount unique features of is relatively small. (Remember 1 new column for each unique feature)
- if the presence of redundant information is acceptable


