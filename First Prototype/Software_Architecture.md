# Control Software Architecture 

* **Top Layer** (User Layer)

  * 

* **Middle Layer** (Algorithm)

  * **Rotational**

    * Attitude Calculation

      * IMU

        * Gyro $\implies $Angular Velocity in $\R^3$ $\implies$ $\theta = \int \vec{\omega}$  (zero drifting | Cumulated Error [Low Freq])
        * Accel $\implies$ Vector Direction Relative to Gravity $\implies$ $\theta$, Not accurate in general, require quad to be translational stationary, High Freq Error
        * Meg $\implies$ Compass 
        * DMP

        % Python Plot

      * Filter Algorithm 

        * Kalman - Probabilistic approach involve linear algebra  -----\
        * Complementary - (High pass + Low pass filter ?) ------------------> Gyro + Accel

        % Design a gimble testing apparatus (supervised learning)

      * Control Algorithm

        * PID
        * PID in series vs parallel
        * L infinity

        % Experimenting on it with above apparatus (Plotting state vs output)

  * **Translational**

* **Bottom Layer** (Embedded System)

  * IMU
  * Motors
  * Sonar
  * CV module