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
V = g \, (4.76~m - 1.65~m) \, 75~kg = 2.286~kJ.
```
At the bottom of the swing the potential energy is $V = 0$.
