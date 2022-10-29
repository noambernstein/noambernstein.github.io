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
  
  
For simplicity, I assume that the system starts with only potential energy, determined by the 
initial flyer center of mass height, ignoring the fact that the body shape is not extended.
The initial potential energy (relative to the lowest height) is therefore
```math
V(t = 0) = m \, g \, \Delta h = 75~kg \, g \, (4.76~m - 1.65~m) = 2.286~kJ
```
where $g = 9.8~m/s^2$ is the acceleration of gravity, and the mass of the flyer is 75&nbsl;kg (165&nbsp;lbs).
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
F = \frac{2 K}{r} = \frac{2 2.286~kJ}{4.76~m} = 960.5~N
```
and the corresponding acceleration $a = F / m = 12.8~m/s^2 = 1.3~g$ (in addition to the $1~g$ exerted by gravity.
