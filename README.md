# time-series
This is the code base for the website www.sridharn-ml.ca

About the Data : 
 The data used in this website is US CPI data averaged monthly across various urban centres. Source : https://fred.stlouisfed.org/series/CPIAUCSL


The idea of this website is to provide a playground for evaluating arima models , rationalize the breakdown of model selection process and provide an idea of performance across a sliding window

ARIMA Modeling: 
    Each knob represents a seasonal anbd /or non-seasonal parameter to the ARIMA model and can be adjusted ( only in Desktop/Laptop, not mobile).
    There is also a reset option for tuning to optimal parameters. Once the parameters are set , drag the joystick for "Fit Model" and observe the 
    ACF and PACF plots show up. At times, the plots may also display insights annotated. There is also a chart that shows residuals below the ACF 
    and PACF charts.
    
Model Selection: 
    One possible sequence of  model selection by applying Box-Jenkins method is displayed.The figures are cached in a cloud storage and served 
    for optimal model performance. However, the code also has the complete memoization logic implemented . (writing a fit model to storage, cache 
    default and serving a cached model)
    
Forecasting : 
    There is one figure displaying the regular forecast by the model and also displays the sliding window forecast by training upto a certain year 
    and forecasting the subsequent 12 months. Implements caching of forecast figures as the "Model Selection" tab.

Session Management: 
     There is some basic session management implemented by storing user session id against user inputs in a dictionary. These user inputs are leveraged 
     to serve the specific user's requests for ACF and PACF plots.
     

Whats Next : 
   1) Automate model selection insights/annotations and generalize code to make this work for any signal ( not just CPI data) 
   2) Create "Model" layer classes ("Model" as in MVC) . Objects instantiated per user session and encapsulate user knob inputs  and respective outputs 
      for the respective session. 
     


