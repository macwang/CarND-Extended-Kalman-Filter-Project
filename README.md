# Extended Kalman Filter Project Starter Code
Self-Driving Car Engineer Nanodegree Program

## Compiling & running

I developed it in MacOS, checkout my code and cd to that directory.

1. mkdir build
2. cd build
3. cmake ..
4. make
5. ./ExtendedKF

## Accuracy

With the dataset 1, my final RMSE is X: 0.0973, Y: 0.0855, VX: 0.4513, VY: 0.4399.

![Simulator image](/sim_ss.png)

## Flow

With the course material and walkthrough video in you youtube. The implementation is straightforward. The modified files are tools.cpp, kalman_filter.cpp and FusionEKF.cpp.

We need to initialize the vectors in EKF object first. Then do prediction whenever we get a new data. Then update with the data.

I met two issues when I was developing this project. One was I didn't initialize H_laser_ in the begining, it still runs but the starting position is really far away from the car position. The other one was I didn't normalize the y[1] in the UpdateEKF() so the prediction would go far away when the car made it's first 360 turn. These two issues took me a while to find out. Over all it's a very educational project and I now I knew EKF better.