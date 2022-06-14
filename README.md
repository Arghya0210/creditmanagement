# creditmanagement
Who will use / how this prediction will add value

Ans. Bank , NBFC and any other financial institution will predict if the customer will default the credit payment or not in the next month based upon the data given.

2> define +ve case /-ve case(classification)(explanation must be domain specific)
Ans. Classification output column is represented as :	default.payment.next.month

If the customer is likely to default in the next month then it will be classified as 1(+ve case) and if the customer is not then it will be classified as 0(-ve case)


3> what metric is appropriate(accuracy,recall,precision,etc)

Ans.Higher recall, higher AUC score

If a customer is classified as -ve (0) but in actual scenario they are prone to default +ve case(1) , then it is very dangerous for the institution who are giving the credits to them.
And that's why we need to decrese the false negative case , so that this situation will be less likey to occur and we can classify who will be likely defaulters.
We need to decrese the False negative and if we do so then Recall will be higher.	

4> Is data file in CSV format ? what is separator? (can "read_csv" be used to open file?)
Ans. Yes,data file is in CSV format.

Separator: , 

5> header  present ? are column names are code frainedly? 

Ans. Yes,columns are code fraiendly except the last one and header is also present.

Following answers must be given after opening the file in PANDAS

6> How many rows and columns present in the file ?
Ans. Rows: 3000, columns:25
 
7> check which column has null(na)(percentage)[IMPORTANT]

Ans. No column has null(percentage - 0%)
ID                            0
LIMIT_BAL                     0
SEX                           0
EDUCATION                     0
MARRIAGE                      0
AGE                           0
PAY_0                         0
PAY_2                         0
PAY_3                         0
PAY_4                         0
PAY_5                         0
PAY_6                         0
BILL_AMT1                     0
BILL_AMT2                     0
BILL_AMT3                     0
BILL_AMT4                     0
BILL_AMT5                     0
BILL_AMT6                     0
PAY_AMT1                      0
PAY_AMT2                      0
PAY_AMT3                      0
PAY_AMT4                      0
PAY_AMT5                      0
PAY_AMT6                      0
default.payment.next.month    0
dtype: int64

8> Find your X and y(target)

Ans.   X :'ID', 'LIMIT_BAL', 'SEX', 'EDUCATION', 'MARRIAGE', 'AGE', 'PAY_0',
       'PAY_2', 'PAY_3', 'PAY_4', 'PAY_5', 'PAY_6', 'BILL_AMT1', 'BILL_AMT2',
       'BILL_AMT3', 'BILL_AMT4', 'BILL_AMT5', 'BILL_AMT6', 'PAY_AMT1',
       'PAY_AMT2', 'PAY_AMT3', 'PAY_AMT4', 'PAY_AMT5', 'PAY_AMT6'
	   
	   
	   Y: 'default.payment.next.month'


9> how many numeric and categorical(string)
    -in all numeric which are discrete / continuous
	
	Ans. All numeric, 15 continuous columns, 10 discrete columns.
	
10> for all categorical , find there labels

Ans. There is no as such categorical data but there are some columns which may require encoding for better data cleaning and model algorithm learning purpose.

11> in classification : distribution of y ( how many 1 and 0)

Ans. 0 (non-defaulters): 23363(77.88%)

1(defaulters): 6636 (22.12%)


12> are all continuous columns have same scale ?
Ans .No all the continuous data are not in same scale.

