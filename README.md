# Day19-Lab-FE

![image](https://user-images.githubusercontent.com/87912604/202173096-41fa0fe2-7dde-43c4-b68a-ce75d67b9c26.png)

## Label Encoding

### refers to converting the labels into a numeric form so as to convert them into the machine-readable form. Machine learning algorithms can then decide in a better way how those labels must be operated. It is an important pre-processing step for the structured dataset in supervised learning.



## Example

### Assume we have a dataset called 'Height' it contains the values 'Tall , Medium , Short' .. After applying the Label Encoding, The values will be as follows '0 , 1 , 2 ' where is 0 refers to 'Tall' and 1 is 'Medium' and 2 is 'Short' .


## Don't use Label Encoding

### when the categorical features have more than two values. The nominal categorical features having more than two values may get treated as ordinal one by the machine learning model .


## Ordinal Encoding

### The name of the encoder gives it away, but ordinal encoders should be used when working with ordinal data. When working with any data related to ranking something with non-numerical categories, ordinal encoder is the way to go.


## Example

### In ordinal encoding, each unique category value is assigned an integer value.
### For example, “red” is 1, “green” is 2, and “blue” is 3.
### This is called an ordinal encoding or an integer encoding and is easily reversible. Often, integer values starting at zero are used.



## Don't use Ordinal Encoding

### Ordinal encoder should not be used if your data has no meaningful order. Going back to the car color example, there is no way to logically order these colors from smallest to largest or worst to best.


## Frequency Encoding

### Frequency Encoding It is a way to utilize the frequency of the categories as labels. In the cases where the frequency is related somewhat with the target variable, it helps the model to understand and assign the weight in direct and inverse proportion, depending on the nature of the data.


## Example

### It can help if frequency correlates with the target and also, it can help the model to understand that smaller categories are less trustworthy than bigger ones, especially when frequency encoding is used parallel with other types of encoding.

## Don't use Frequency Encoding

### We can lose valuable information if there are two different categories with the same amount of observations count—this is because we replace them with the same number

## Binary Encoding

### Binary encoding is a technique used to transform categorical data into numerical data by encoding categories as integers and then converting them into binary code

## Example

### Binary encoding works really well when there are a high number of categories. For example the cities in a country where a company supplies its products.


## Don't use Binary Encoding

###  The main drawback with this method is when the categorical variable with many values (e.g., city) which can tremendously increase the dimension of data. 


## One-Hot Encoding

### One-hot encoding in machine learning is the conversion of categorical information into a format that may be fed into machine learning algorithms to improve prediction accuracy.


## Example

###  Say we have the values red and blue. With one-hot, we would assign red with a numeric value of 0 and blue with a numeric value of 1.

### It’s crucial to be consistent when we use these values. This makes it possible to invert our encoding at a later point to get our original categorical back.

### Once we assign numeric values, we create a binary vector that represents our numerical values. In this case, our vector will have 2 as its length since we have 2 values. Thus, the red value can be represented with the binary vector [1,0], and the blue value will be represented as [0,1].


## Don't Use One-Hot Encoding

### Because this procedure generates several new variables, it is prone to causing a large problem (too many predictors) if the original column has a large number of unique values.

### Another disadvantage of one-hot encoding is that it produces multicollinearity among the various variables, lowering the model’s accuracy.


## Target Mean Encoding

### Target encoding is the process of replacing a categorical value with the mean of the target variable. Any non-categorical columns are automatically dropped by the target encoder model.


## Example

### Seattle can be replaced with average of salary (target variable) of all datapoints where city is Seattle.

## Don't Use Target Mean Encoding

### This encoding method is really easy and powerful. However, there are important issues that you need to keep in mind when using that.

### One really important effect is the Target Leakage. By using the probability of the target to encode the features we are feeding them with information of the very variable we are trying to model. This is like “cheating” since the model will learn from a variable that contains the target in itself.