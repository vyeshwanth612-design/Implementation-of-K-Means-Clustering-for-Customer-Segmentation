# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import NumPy and RandomForestRegressor from sklearn.
2. Create the input data (environmental sensor values) and output data (Temperature, PM2.5 and Energy).
3. Train the Random Forest Regressor using the fit() function.
4. 1. Predict temperature, PM2.5 and energy using the predict() function and display the results.

## Program:
```py

import numpy as np
from sklearn.ensemble import RandomForestRegressor

X = np.array([
    [25, 60, 10, 2],
    [27, 55, 15, 3],
    [30, 50, 20, 4],
    [32, 45, 25, 5],
    [29, 65, 18, 3],
    [26, 70, 12, 2],
    [31, 40, 30, 6],
    [33, 35, 35, 7],
    [28, 60, 16, 3],
    [24, 75, 8, 1]
])

Y = np.array([
    [25, 35, 120],
    [27, 40, 130],
    [30, 55, 150],
    [32, 65, 170],
    [29, 45, 140],
    [26, 30, 110],
    [31, 75, 180],
    [33, 85, 200],
    [28, 42, 135],
    [24, 25, 100]
])

model = RandomForestRegressor(n_estimators=100, random_state=42)
model.fit(X, Y)

prediction = model.predict([[30, 55, 20, 4]])

print("Predicted Temperature:", prediction[0][0])
print("Predicted PM2.5:", prediction[0][1])
print("Predicted Energy:", prediction[0][2])

```

## Output:
<img width="245" height="86" alt="image" src="https://github.com/user-attachments/assets/70aa025d-8006-4eda-8a0a-8db98f29948a" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
