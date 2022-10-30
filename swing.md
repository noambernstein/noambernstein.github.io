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
momentum of {\em parts} of the flyer (although the total angular
momentum is conserved).  This is definitely the way flyers flip
over, for exampe in a face-off or a miss, but it is unclear if
the same effect can significantly affect the swing.  

Here I quantitatively analyze the effects of various motions on
swing height.

## Mechanisms

### Raising and lowering the flyer's CoM

The geometry of the rig and the flyer is shown in Fig.&nbsp;1m, with (at best) approximate 
dimensions. The lowest possible center of mass position is with a straight flyer at the 
bottom of the swing (pulse), 4.76&nbsp;m below the fly-bar crane. The initial position of
the flyer is approximated as a "7", with horizontal arms.
 
<figure>
  <img src="rig.svg" width="800" alt="Figure 1: the rig" />
  <figcaption> Figure 1: geometry of the rig and the flyer.</figcaption>
</figure>

&nbsp;

For simplicity, I assume that the system starts with only potential energy, determined by the 
initial flyer center of mass height, ignoring the fact that the body shape is not extended.
The initial potential energy (relative to the lowest height) is therefore
```math
V(t = 0) = m \, g \, \Delta h = 75~kg \, g \, (4.76~m - 1.65~m) = 2.286~kJ
```
where $g = 9.8~m/s^2$ is the acceleration of gravity, and the mass of the flyer is 75&nbsp;kg (165&nbsp;lbs).
At the bottom of the swing the potential energy is $V = 0$, so (assuming the flyer remains rigid)
at that point the kinetic energy is equal to the initial potential energy.
The rotational kinetic energy for a point mass rotating about an axis is
```math
K = \frac{1}{2} I \omega^2 = \frac{1}{2} \omega^2 m r^2
```
where $I = m r^2$ is the moment of intertia, $\omega = \dot{\theta}$ is the angular velocity,

and the centrifugal pseudo-force the flyer feels is
```math
F = m \omega^2 r.
```
Solving for $F$ in terms of $K$ gives
```math
\omega = \sqrt{\frac{2 K}{m r^2}}
```
and substituting into the expression for $F$ gives
```math
F = \frac{2 K}{m r^2} m r = \frac{2 K}{r} = \frac{2 2.286~kJ}{4.76~m} = 960.5~N
```
and the corresponding acceleration 
```math
a = F / m = 12.8~m/s^2 = 1.3~g
```
in addition to the $1~g$ exerted by gravity.

Some detailed measurements of the human body part mass and weight are in Tables I and II. Based on these 
measurements I calculated the height of the CoM of the flyer when fully extended, and when raising the
legs by bending 180$^\circ$ at the hips, as in the initial part of a force out.  A diagram of these
two positions and the resulting CoM positions is shown in Fig.&nbsp;2. The position of the extended
flyer's center of mass, measured from the fly bar (end of arms) in terms of fraction of body height is
```math
h_\mathrm{extended} = 0.155 f_\mathrm{arms} + 0.205 f_\mathrm{head} + 0.44 f_\mathrm{torso} +
 0.7 f_\mathrm{ul} + 0.965 f_\mathrm{ll} = 0.495
```
where $f_\mathrm{part}$ is the mass fraction from Table&nbsp;I, "ul" stands for upper legs, and "ll" stands for lower legs.
For the force-out position the CoM position is
```math
h_\mathrm{extended} = 0.155 f_\mathrm{arms} + 0.205 f_\mathrm{head} + 0.44 f_\mathrm{torso} +
 0.44 f_\mathrm{ul} + 0.175 f_\mathrm{ll} = 0.364
```

Table&nbsp;I: body part volumes (from https://msis.jsc.nasa.gov/sections/section03.htm Fig.&nbsp;3.3.6.3.2-1 2 of 12)
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
From 2 of 12: overall height. Directly from height and 8 of 12 (or from its differences): hips-floor (upper + lower legs). 
From cited measurements and estimated offset between shoulders as measured in cited figure and shoulder joint: 
shoulder joint-hips (torso), shoulder joint-top of head. Estimated from personal observation: fraction of overall legs (hip-floor)
contributed by upper and lower legs, arm length.
| body part | fraction of height |
| --------- | ------------------ |
| head and neck | 0.21 |
| torso | 0.26 |
| lower legs | 0.27 |
| upper legs | 0.26 |
| arms | 0.31 |

<figure>
  <img src="flyer.svg" width="800" alt="Figure 2: the flyer" />
  <figcaption>
  Figure 2: geometry of the flyer, fully extended and
  raising legs in the initial stage of the force out.  Blue
  arrows show extent of each body part, and black arrows show 
  position of center of mass of each body part.
  </figcaption>
</figure>
