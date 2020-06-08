# stipplebomb
stipplebomb renders a grayscale image in a stippling technique via an
interesting method.

The method is as follows:

A rectangular field is mapped to the image so that coordinates in the
field correspond to coordinates in the image.

"Balls" are introduced into the field.  The radius of the balls is
proportional the intensity of the image at the corresponding coordianate.
The balls are given some initial velocity, and there is some friction to
slow them down.  The balls also have a repulsive magnetic field which 
varies in strength that is again proportional to the radius of the ball
(and to the image intensity at the ball's corresponding image coordinate).
The force of this repulsive magnetic field diminishes with the square of
the distance (so very rapidly falls off.)

As the simulation is run, the forces on each ball due to the surrounding
balls is calculated, and the corresponding acceleration is applied to the
balls.
