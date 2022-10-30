# Mathematical analysis of the trapeze swing

## Introduction

In a the trapeze swing, the flyer moves their body to increase the
total energy in the swinging system, and therefore the height of
the swing.  The most obvious way is by raising or lowering the
flyer's center of mass (CoM), doing work against gravity, as in the
analysis at
[www.flying-trapeze.com](https://www.flying-trapeze.com/resources/physics-of-flying-trapeze/item/4311-investigation-6-an-advanced-swing).
In addition, as the muscles cause body parts to rotate around the
axes defined by the joints, they apply torques and change the angular
momentum of _parts_ of the flyer (although the total angular
momentum is conserved).  This is definitely the way flyers flip
over, for exampe in a face-off or a miss, but it is unclear if
the same effect can significantly affect the swing.  

Here I quantitatively analyze the effects of various motions on
swing height.

## The swing

### Geometry of the flyer

Some detailed measurements of  human body part masses and weights are listed in Tables&nbsp;I and II. Based 
on these measurements I calculated the height of the CoM of the flyer when fully extended, and when 
raising the legs by bending $180^\circ$ at the hips, as in the initial part of a force out.  A diagram of 
these two body positions and the resulting CoM positions is shown in Fig.&nbsp;1. The position of the extended
flyer's center of mass, measured from the fly bar (ends of arms) in terms of fraction of body height is
```math
h_\mathrm{extended} = 0.155 f_\mathrm{arms} + 0.205 f_\mathrm{head} + 0.44 f_\mathrm{torso} +
 0.7 f_\mathrm{ul} + 0.965 f_\mathrm{ll} = 0.495
```
where $f_\mathrm{part}$ is the mass fraction of each body part from Table&nbsp;I, "ul" stands for upper legs, and "ll" stands for lower legs.
For the force-out position the CoM position is
```math
h_\mathrm{extended} = 0.155 f_\mathrm{arms} + 0.205 f_\mathrm{head} + 0.44 f_\mathrm{torso} +
 0.44 f_\mathrm{ul} + 0.175 f_\mathrm{ll} = 0.364
```

Table&nbsp;I: body part volumes, based on https://msis.jsc.nasa.gov/sections/section03.htm Fig.&nbsp;3.3.6.3.2-1 panel 2 of 12. Note that for limbs, the values below include the sum of right and left.
| body part | fraction of total volume |
| ----------| --------------- |
| head + neck | 6.5 % |
| torso | 56 % |
| upper legs | 15.5 % |
| lower legs | 11.5 % |
| upper arms | 6 % |
| lower arms + hands | 4.5 % |

Table&nbsp;II: Body part lengths, based on https://msis.jsc.nasa.gov/sections/section03.htm Fig.&nbsp;3.3.1.3-1 with some 
additional personal observations.
From panel 2 of 12: overall height. Directly from height and panel 8 of 12 (or from its differences): hips-floor (upper + lower legs). 
From cited measurements and estimated offset between shoulder joint and cited figure shoulder height: 
shoulder joint-hips (torso), shoulder joint-top of head (head and neck). Estimated from personal observation: fraction of overall legs (hip-floor) accounted for by the upper and lower legs, arm length.
| body part | fraction of height |
| --------- | ------------------ |
| head and neck | 0.21 |
| torso | 0.26 |
| lower legs | 0.27 |
| upper legs | 0.26 |
| arms | 0.31 |

<figure>
  <img src="flyer.svg" width="800" alt="Figure 1: the flyer" />
  <figcaption>
  Figure 1: geometry of the flyer, fully extended and
  raising legs in the initial stage of the force out.  Blue
  arrows show extent of each body part as fraction of overall
  height, black arrows show position of CoM of each body part, and 
  red arrows show the position of the flyer's overall CoM.
  </figcaption>
</figure>

&nbsp;

Assuming that the flyer is 1.8&nbsp;m tall (5'11"), the distance from the hands to
the center of mass fully extended is $0.89\~\mathrm{m}$, and when raising legs it is $0.66\~m$.
Below I will approximate these as $0.9\~\mathrm{m}$ and $0.65\~\mathrm{m}$. In addition
to these dimensions I assume below that the mass of the flyer is $75\~\mathrm{kg} = 165\~\mathrm{lbs}$.

### The swing of a still, rigid flyer

The geometry of the rig and the flyer is shown in Fig.&nbsp;2, with (at best) approximate 
dimensions. The lowest possible center of mass position is with a fully extended flyer at the 
bottom of the swing (pulse), 4.54&nbsp;m below the fly-bar crane. The initial position of
the flyer is approximated as a "7", with horizontal arms.
 
<figure>
  <img src="rig.svg" width="800" alt="Figure 1: the rig" />
  <figcaption> 
    Figure 2: geometry of the rig and the flyer. The lines
    are 3.64&nbsp;m or 12' long, and the board is 2.8&nbsp;m or 9.2' below
    the fly-bar crane.
 </figcaption>
</figure>

&nbsp;

For simplicity, I assume that the system starts with only potential energy, determined by the 
initial flyer center of mass height, ignoring the fact that the body shape is not extended.
The initial height of the CoM above its lowest point is roughly estimated to be 
$(4.54 - 1.65)\~\mathrm{m} = 2.89\~\mathrm{m}$.
The initial potential energy (relative to the lowest height) is therefore
```math
V(t = 0) = m \, g \, \Delta h = 75~\mathrm{kg} \, g \, (4.54~\mathrm{m} - 1.65~\mathrm{m}) = 2.124~\mathrm{kJ}
```
where $g = 9.8\~\mathrm{m/s^2}$ is the acceleration of gravity, and the mass of the flyer is 75&nbsp;kg (165&nbsp;lbs).
At the bottom of the swing the potential energy is $V = 0$, so (assuming the flyer remains rigid)
at that point the kinetic energy is equal to the initial potential energy.
The rotational kinetic energy for a point mass rotating about an axis is
```math
K = \frac{1}{2} I \omega^2 = \frac{1}{2} \omega^2 m r^2
```
where $I = m r^2$ is the moment of inertia, $\omega = \dot{\theta}$ is the angular velocity,
and the centrifugal pseudo-force the flyer feels is
```math
F = m \omega^2 r.
```
Solving for $\omega$ in terms of $K$ gives
```math
\omega = \sqrt{\frac{2 K}{m r^2}}
```
and substituting into the expression for $F$ gives
```math
F = \frac{2 K}{m r^2} m r = \frac{2 K}{r} = \frac{2 \times 2.124~kJ}{4.54~m} = 935~N
```
and the corresponding acceleration 
```math
a = F / m = 12.5~m/s^2 = 1.3~g
```
in addition to the $1\~g$ exerted by gravity.

For completeness, the period of this swing, which is far from the commonly analyzed
infinitesimal amplitude limit, is given in [wikipedia](https://en.wikipedia.org/wiki/Pendulum_(mechanics)#Arbitrary-amplitude_period) as
```math
T = \frac{2 T_0}{\pi} K(k)
```
where $T_0 = 2 \pi \sqrt{\frac{r}{g}}$ is the small amplitude approximate period, 
$k = \sin \frac{\theta_0}{2}$ and $K$ is the complete elliptic integral of the first kind. 
For the dimensions in Fig.&nbsp;2 $r = 4.54\~\mathrm{m}$ and $\theta_0 = 70^\circ$.
Therefore, $T_0 = 4.3\~\mathrm{s}$, $k = 0.57$, $K(k) = 1.918$ [Wolfram Alpha](https://www.wolframalpha.com/input?i=complete+elliptic+integral+of+the+first+kind+for+0.57), so $T = 5.25\~\mathrm{s}$.

### The effect of raising and lowering the flyer's CoM

If the flyer raises or lowers their CoM they can change their potential or kinetic energy, but 
cannot affect their angular momentum.  I therefore compute the change in the swing if the
flyer raises their legs at the bottom of the swing, doing work against gravity and the 
centrifugal pseudo-force, while keeping angular momentum constant.

The increase in potential energy due to the $\Delta\~r = 0.25\~\mathrm{m}$ raising of the center of mass by lifting
the legs is
```math
{\Delta}V = m \, g \, {\Delta}r = 184~\mathrm{J}.
```
The angular momentum fully extended is
```math
L = I \omega = m r^2 \omega_i
```
and after raising the legs it is
```math
L = m (r-{\Delta}r)^2 \omega_f
```
Solving for the final angular velocity gives
```math
\omega_f = \omega_i \frac{r^2}{(r-{\Delta}r)^2}
```
The corresponding change in kinetic energy is
```math
\begin{eqnarray}
K_f - K_i & = & 
\frac{1}{2} \left( m (r - {\Delta}r)^2 \omega_f^2 - m r^2 \omega_i^2 \right) \\
& = & \frac{1}{2} m \omega_i^2 \left( (r - {\Delta}r)^2 \frac{r^4}{(r - {\Delta}r)^4} \omega_i^2 - r^2 \right) \\
& = & \frac{1}{2} m \omega_i^2 \left( \frac{r^4}{(r - {\Delta}r)^2} - r^2 \right) \\
& = & \frac{1}{2} m \omega_i^2 r^2 \left( \frac{r^2}{(r - {\Delta}r)^2} - 1 \right)
\end{eqnarray}
```
With $\Delta\~r = 0.25$&nbsp;m the fractional change of the kinetic energy of 12%, or 262&nbsp;J.
The increase of the total energy of the system is $184 + 262$&nbsp;J, to 2.63&nbsp;kJ. This
corresponds to a final height of 3.58&nbsp;m above the lowest point. 

When the flyer reaches peak, $3.58\~\mathrm{m} - 2.89\~\mathrm{m} = 0.7\~\mathrm{m}$ higher
than the beginning of the swing, their potential energy is maximized and kinetic energy is zero.
If they could extend their legs to increase $r$ back to its initial value without otherwise changing
their energy, they could go back to this new, larger height at the back of the the swing,
swing forward, and repeat the process. The gain in energy (and therefore height) from the next
swing will be even larger: the change in potential energy will be the same, but because the
initial height is larger, the value of $\omega$ at the bottom will be larger, so the kinetic
energy gain will be larger as well.

Note, however, that this simplistic analysis neglects two factors. The first is that changes in
body position at the back end of the swing are required for the flyer to avoid hitting the back
of their legs on the board. The other is that if the flyer is not exactly horizontal at peak,
extending the legs will lower the CoM somewhat, and lose some potential energy.  The change
in height of the CoM is exactly $\Delta r \cos \theta$. The peak angle can be determined
from $\cos \theta = (4.54 - 3.58) / 4.54 = 0.211$, so the loss of height will be 0.05&nbsp;m.
The flyer will therefore gain only 0.84&nbsp;m, rather than 0.89&nbsp;m.

Even this analysis neglects the fact that the lines are flexible, not rigid, so the flyer cannot
extend their legs exactly at peak without creating slack in the lines. As a result, the extension
has to happen more gradually, using gravity and the centrifugral pseudo-force to keep the lines
taut. A quantitative description of this effect is beyond the scope of this work.
