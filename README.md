# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("car.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
predictedCO2 = regr.predict(pd.DataFrame([[3300, 1300]], columns=['Weight', 'Volume']))
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)





```
## Output
</br>![WhatsApp Image 2024-12-31 at 12 59 04_dbeeb3e9](https://github.com/user-attachments/assets/655fbeda-1b71-41b8-adfd-c1b1de28b728)

</br>![WhatsApp Image 2024-12-31 at 12 59 04_59c040fa](https://github.com/user-attachments/assets/4bd3b964-3eec-4f42-9913-0735fac1c0a8)

</br>
</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
