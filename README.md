# **Non-linear MPC for maximum distance and obstacle avoidance**                                                                 
Implemented a NMPC system to overtake the leading vehicle considering the constraints such as lane keeping, input bounds, and collision avoidance optimizing for maximum distance travelled in the x-direction, achieving 1374.22 units. The control system successfully minimized deviations from the y=0 axis, with a low standard deviation of 18.25 units. 

# Car Dynamics

We consider the car dynamics with lumped rear and front tire forces. 

For simplification, we consider the positions and orientation in the world coordinates.  

\begin{aligned}
\dot{U}_x & =\frac{F_{x_f} \cos \delta-F_{y_f} \sin \delta+F_{x_r}-F_d}{m}+r U_y \\
\dot{U}_y & =\frac{F_{y_f} \cos \delta+F_{x_f} \sin \delta+F_{y_r}+F_b}{m}-r U_x \\
\dot{r} & =\frac{a\left(F_{y_f} \cos \delta+F_{x_f} \sin \delta\right)-b F_{y_r}}{I_{z z}} \\
\dot{x} & = \cos(\phi)U_x - \sin(\phi)U_y  \\
\dot{y} & = \sin(\phi)U_x + \sin(\phi)U_y   \\ 
\dot{\phi} & =r  
\end{aligned}

