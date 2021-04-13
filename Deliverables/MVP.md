## MVP

This inital model yields the following function:

$$y_{pred} = f(x) = 76.58 - 22x_{danceability} -.003x_{popularity} - 1.6x_{numwks}$$

The four features used were selected for initial modeling as they had the most palpable correlative relationships with the target variable, peak rank on billboard charts. The four features include danceability, followers, popularity, and number of weeks on the charts at the point of that peak position. 


The following is a plot of this model:

![Log Peak Plot](logpeakplotmvp.png)

![Log Peak Plot](peakplotmvp.png)

The R2 value calculated was .412, with an adjusted R2 as .411. 
