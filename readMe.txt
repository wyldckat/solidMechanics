Solid Mechanics
Finite Volume Solvers

The included solid mechanics solvers employ the finite volume method
(not finite elements) to numerically approximate the displacements
and stresses in solid bodies undergoing deformation.

The included solvers are suitable for small strain, small strain with
large rotations, large strain, cohesive zones, plasticity, thermal-
elasticity, visco-elasticity, gravity forces, fluid-structure
interactions, multi-material analyses and contact stress analysis.

A number of custom boundary conditions with full non-orthogonal correction
are including time-varying displacements and tractions, fixed rotations,
and fixed displacements with zero shear stress.

A number of people have contributed to the development of the solvers,
mainly within Alojz Ivankovic's research group. The main contributors are:
Aleksandar Karac, Zeljko Tukovic, Hrvoje Jasak, Philip Cardiff, Declan Carolan,
Michael Leonard and Valentine Kanyanta.

The solvers have been assembled and are maintained by Philip Cardiff,
University College Dublin.

Have fun.


Notes for OpenFOAM-2.2.0
disabled capabilities for compilation:
	 - solidInterface because of faMesh
	 - ggiInterpolation option in contact boundaries
	 - fixedRotation boundary condition because of RodriguesRotation
	 - finiteElement mesh motion in FSI solver
