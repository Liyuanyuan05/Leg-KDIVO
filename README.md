
# R-KDIV

R-KDIVO is a robust kinematic-dynamic-inertial-visual odometry framework for legged robot pose estimation. The proposed framework integrates visual, inertial, encoder, and controller-derived foot-force information to improve state estimation robustness under challenging locomotion conditions. The core estimation module is built upon a Robust Error-State Kalman Filter (R-ESKF), which fuses camera observations, IMU measurements, and joint encoder-based kinematic information in a unified filtering framework. To further enhance robustness against unmodeled contact effects, an STA-based disturbance observer is introduced. The observer uses the nominal foot-force inputs provided by the legged robot controller together with the robot dynamic model to estimate a lumped disturbance term. This estimated disturbance is then fed back into the ESKF propagation process to compensate for model errors, contact uncertainty, and external perturbations. Compared with purely kinematic-inertial or visual-inertial estimators, R-KDIVO explicitly incorporates dynamic information and disturbance compensation, making it more suitable for legged robots operating under complex contact interactions such as foot slippage, impact, and visual degradation. The datasets and source code will be released in the future.
## Platform: AlienGo

<p align="center">
  <img src="figures/dog.jpg" width="50%">
</p>

## Framework

<p align="center">
  <img src="figures/observer_eskf.jpg" width="60%">
  <br>
  <b>Fig. 1.</b> The proposed R-KDIV framework.
</p>

## Experimental Results

### Indoor sequence

<p align="center">
  <img src="figures/indoor_traj_2.jpg" width="60%">
  <br>
  <b>Fig. 2.</b> Indoor trajectory comparison.
</p>

### Outdoor sequence

<p align="center">
  <img src="figures/campus_trajectory_plot.jpg" width="60%">
  <br>
  <b>Fig. 3.</b> Outdoor Campus trajectory comparison.
</p>

### Challenge scene

<p align="center">
  <img src="figures/robust.png" width="80%">
  <br>
  <b>Fig. 4.</b> Challenge scenes trajectory comparison, including foot slippage and camera occlusion.
</p>
