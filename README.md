# Extended_Kalman_Filter-EKF-
Extended Kalman Filter

The Linear Kalman filter is a powerful tool, but many systems encountered in practice are nonlinear.
One approach to state estimation for nonlinear systems is to linearize the equations about the current
estimate and then apply Kalman's equations using the resulting approximation. This formulation is called
the extended Kalman filtering.

In summary we can implement EKF using the following equations:

Prediction equations:

![Prediction equations](https://github.com/EnriqManComp/Extended_Kalman_Filter-EKF-/blob/master/Theory%20images/EKF_form1.png)

Where X plus at t-1 corresponds to the mean of the corrected state t-1 and U at t corresponds to the noisy controls applied in the state t. Sigma plus at t-1 corresponds to the noise in the corrected state t-1, Sigma at A corresponds to the noise of the actual state and G at t corresponds to the Jacobian matrix for the prediction. 

Correction equations:

![Correction equations](https://github.com/EnriqManComp/Extended_Kalman_Filter-EKF-/blob/master/Theory%20images/EKF_form2.png)

Where K at t is a weight factor to consider the observation value, H at t is the Jacobian matrix for the correction. Sigma minus at t is the noise in the prediction of the state t and Sigma at M is the noise of the observation values. Z at t is the observation of the state t and h in X minus at t is the observations of the state t in the prediction. I is an identity matrix.
 
 Definition of Jacobians:
 
 Basically each Jacobian is a partial derivatives of the variables of the transition state matrix X, notice that Gt include the controls.
 
 ![Gt Jacobian](https://github.com/EnriqManComp/Extended_Kalman_Filter-EKF-/blob/master/Theory%20images/Gt.png)
 
 ![Ht Jacobian](https://github.com/EnriqManComp/Extended_Kalman_Filter-EKF-/blob/master/Theory%20images/Ht.png)
 
 # Description of the code:
 In this particular case, we setup controls with constant linear and angular velocities. Then, we add random noise using normal distribution to the controls and the observations provided by the sensor.
 
 | Columna 1 | Columna 2 | Columna 3 |
|-----------|-----------|-----------|
| Celda 1   | Celda 2   | Celda 3   |
| Celda 4   | Celda 5   | Celda 6   |
| Celda 7   | Celda 8   | Celda 9   |

 
 
