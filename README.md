# Deep Learning Project

Team: Ken, Dennis, Jeffery, Dexter

#### Background

The background of the task focuses on a spatial-temporal task, where the deep learning model is required to predict future trajectories of moving objects like cars on roads based on their previous positions and velocity. By improving the accuracy of the prediction, it could benefit the forecasting technology of fully autonomous driving vehicles, which would increase the safety of driving without supervision. Therefore, solving this problem can boost the progression of autonomous driving technology. Moreover, in the domain of traffic forecasting, predicting the trajectories of vehicles could give a better prediction and understanding of traffic conditions in major cities, thus benefiting efficiency of highway and public transportation planning.

#### Input, Output, Model Design

For this task, we are given a dataset that consists of individual scenes. Within each scene, the input matrix for the model can be described as $ m x n x p$, where m is the number of autonomous vehicles being tracked within the scene. $m = 60$ in all our cases, but there are cases where the number of tracked vehicles is smaller than 60. N equals the number of time steps recorded, where the recording interval is between 2 seconds. In all the cases, $n = 19$. p equals to the features the model is going to intake, which includes $p_in$ and $v_in$ $p_in$ contains a vector $[x_i, y_i]$ which records the vehicle’s positions for $x$ and $y$ coordinates. $v_in$ contains a vector $[v_x, v_y]$ which recorded the vehicle’s position for $x$ and $y$ velocity. We are given the first 19 times steps of vehicles’ information to predict the next 30 time steps of a corresponding target vehicle. The output matrix would have a similar form of $(m x n x p)$, where $n = 30$.

Other than prediction of the car coordinates, this deep learning model can solve any other tasks that record the position and velocity of objects along time, since this is what our deep learning model is designed for. For example, we can transform the electricity usage over a number of households, and predict the next 30 day dynamic electricity usage using our model. We can also predict fluctuations of the stock market or generate new sentences according to previous records.
