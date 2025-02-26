# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
    ```
    /*
    Program to implement univariate Linear Regression to fit a straight line using least squares.
    Developed by: Jayani N
    RegisterNumber:  212224100025
    */
    ```
    import numpy as np
    import matplotlib.pyplot as plt
    x=np.array(eval(input()))
    y=np.array(eval(input()))
    #x=np.array([8,12,11,6,5,4,12,9,6,1])
    #y=np.array([3,10,3,6,8,12,1,4,9,14])
    x_mean=np.mean(x)
    y_mean=np.mean(y)
    
    num,den=0,0
    for i in range(len(x)):
      num+=((x[i]-x_mean)*(y[i]-y_mean))
      den+=((x[i]-x_mean)**2)
    m=num/den
    b=y_mean-m*x_mean
    print("Slope:",m)
    print("Intercept:",b)
    
    y_predit=m*x+b
    print(y_predit)
    
    plt.scatter(x,y,color='yellow')
    plt.plot(x,y_predit,color='red')
    plt.show()

## Output:
![image](https://github.com/user-attachments/assets/0ddc4161-016a-40cb-af63-238ae38efb62)

![image](https://github.com/user-attachments/assets/e9188394-c331-422b-8d7d-9f111cec61ea)

![image](https://github.com/user-attachments/assets/2095b02a-1949-4c30-9726-f4ca28107e14)

![image](https://github.com/user-attachments/assets/c28453a0-92e1-4de9-8a75-e43fa1cfd3a1)

![image](https://github.com/user-attachments/assets/610e22d9-5e68-41fd-9866-3c0c8db16bf9)









## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
