# 14_DLP_Algorithmic_Trading
## Introduction
An application designed to combine machine learning and Python language to create an algorithmic trading bot using an SVC classifier and Linear Regression Model (Supervised Learning) for comparison.

Live application link: https://github.com/davidlp94/14_DLP_Algorithmic_Trading/blob/main/machine_learning_trading_bot.ipynb

---

## Technologies

The following technology/software was used for this application:


-Python 3.7.11 (Programming language)

    Imported Python Libraries/Packages:
    
    -import pandas as pd
    
    -import numpy as np
    
    -from pathlib import Path
    
    -import hvplot.pandas
    
    -import matplotlib.pyplot as plt
    
    -from sklearn import svm
    
    -from sklearn.preprocessing import StandardScaler
    
    -from pandas.tseries.offsets import DateOffset
    
    -from sklearn.metrics import classification_report
    
-JupyterLab

-Git version 2.34.11.windows.1

-Windows 10 Operating System

---

## Installation Guide

To install this application on your machine, download (or clone using http link) all files contained in this repository davidlp94/14_DLP_Algorithmic_Trading.

Next, open GitBash (terminal for MacOS), change your directory to the davidlp94/14_DLP_Algorithmic_Trading, open JupyterLab in a dev environment and open/run the machine_learning_trading_bot.ipynb file.

---

## Baseline Performance
(Please refer to Jupyter Notebook for full source-code)
## SVC Model vs. Linear Regression Comparison

Note: Rolling windows can be adjusted to your liking in cell-block #4.
Note: Training Dataset period can be adjusted in cell block #12.

Setting the fast_SMA to 4 (or 4-day SMA average) and the slow_SMA to 100, the below plot is generated. The trading bot that uses SVC classifier shows a greater return (1.5x) than the underlying asset (1.4x)

![image](https://user-images.githubusercontent.com/96163075/162093697-0ca71857-0273-4f0b-9435-492bb04b9974.png)

The above generated plot shows that the trading bot has more returns than the underlying baseline asset.

However, this same rolling window used on the linear regression model shows that the trading bot generated lower returns (1.1x) than the underlying baseline asset.

![image](https://user-images.githubusercontent.com/96163075/162093734-0ae645ce-f633-41ab-9550-94665413185c.png)

We can tune the linear regression model by adjusting the rolling wondows to 4-day SMA and 50-day SMA which benifits only the LR model.

Below shows the plot for SVC Classifier model which shows the same amount of return:

![image](https://user-images.githubusercontent.com/96163075/162093943-108e4994-1f85-44ad-8524-922162986e32.png)

Below shows the plot for Linear Regression model which shows a much greater return of 1.6x. However, the trading bot had major losses towards the end of the period which ultimately shows about a 1.2x return.

![image](https://user-images.githubusercontent.com/96163075/162093999-f5f02cbb-630a-43e9-8263-30cfa590b8f0.png)

Also, if you adjust the dataset period to different values such as 2, 3 6 and 10, both model/trading bots perform lower than the actual returns. Therefore, a dataset with 3 months of offset is the most efficient.

## Conclusion
In conclusion, if you want lower risk/reward ratio, use the SVC model with a dataset of 3 months offset and rolling windows of 4 and 100. See plot below:

![image](https://user-images.githubusercontent.com/96163075/162095239-9bea9b0c-9406-40ff-a8cd-6addd5aef1b9.png)

If you want more high risk/reward, use the Linear Regression model with a dataset of 3 months offset and rolling windows of 4 and 50. However, be prepared for high volatility in the portfolio as shown in the plot below:

![image](https://user-images.githubusercontent.com/96163075/162095387-7b8f2661-f630-41c9-afa1-7f77cf540e7f.png)


## Contributors

David Lee Ping

email: davidleeping@gmail.com

Phone: 570.269.5973

LinkedIn: https://www.linkedin.com/in/david-lee-ping/

---

## License

MIT License

Copyright (c) [2022] [David Lee Ping]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


