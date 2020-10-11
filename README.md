# PID Control Self driving car
![Test Image 1](https://udacity-reviews-uploads.s3.us-west-2.amazonaws.com/_attachments/584463/1602395317/PID_Sucess.JPG)
Control is how to use steering , throttle and breaks to move the car. Through calculating proportional term , differential term and integral term we can determine the steering angle and throttle.
I implemented this project using C++.

---

## PID COMPONENTS

#### P component
P sets the steering angle in proportion to CTE ( cross track error ). To calculate P component, We multiply CTE with a proportional factor of tau.
#### D component
to prevent overshoot through the X-axis, we calculate the derivative of the error. this term is targeting to help the car to approach the line smoothly. the differential error is the difference between the current error and previous error.
#### I component
this component refers to Integral term. Integral term is to deal with systematic bias, and we calculate it using the summation the error.

---
# calculate hyperparameters
I choosed hyperparameters manually. by trying different values of hyperparameters until i found the best values to choose.
---

## Dependencies

* cmake >= 3.5
 * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1(mac, linux), 3.81(Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools]((https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
* [uWebSockets](https://github.com/uWebSockets/uWebSockets)
  * Run either `./install-mac.sh` or `./install-ubuntu.sh`.
  * If you install from source, checkout to commit `e94b6e1`, i.e.
    ```
    git clone https://github.com/uWebSockets/uWebSockets 
    cd uWebSockets
    git checkout e94b6e1
    ```
    Some function signatures have changed in v0.14.x. See [this PR](https://github.com/udacity/CarND-MPC-Project/pull/3) for more details.
* Simulator. You can download these from the [project intro page](https://github.com/udacity/self-driving-car-sim/releases) in the classroom.


---
## Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./pid`. 

Tips for setting up your environment can be found [here](https://classroom.udacity.com/nanodegrees/nd013/parts/40f38239-66b6-46ec-ae68-03afd8a601c8/modules/0949fca6-b379-42af-a919-ee50aa304e6a/lessons/f758c44c-5e40-4e01-93b5-1a82aa4e044f/concepts/23d376c7-0195-4276-bdf0-e02f1f3c665d)


