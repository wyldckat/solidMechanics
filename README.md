Solid Mechanics - Finite Volume Solvers
=======================================

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
------------------------

Disabled capabilities for compilation:
   - solidInterface because of faMesh
   - ggiInterpolation option in contact boundaries
   - fixedRotation boundary condition because of RodriguesRotation
   - finiteElement mesh motion in FSI solver

   
Further modifications
=====================

Original source came from here: http://www.cfd-online.com/Forums/openfoam-news-announcements-other/106881-solid-mechanics-solvers-added-openfoam-extend-4.html#post432903

Further modificiations made by Bruno Santos (wyldckat@github working at [blueCAPE Lda](http://www.bluecape.com.pt)):
   - Moved solvers to their own folder.
   - Simplified Allw* scripts, since this way we can use the multi-core building ability that OpenFOAM has got.
   - Using "realpath" as a compatibility measure with compiling on Windows (blueCFD).
   - Created branches for each one of the latest OpenFOAM git versions: OF23x OF22x OF21x OF20x
     - Note: Have not tested any of the tutorials with all of these OpenFOAM versions.


Building on OpenFOAM 2.3.x, 2.2.x, 2.1.x and 2.0.x
==================================================

Using Git
---------

  1. Go to your user folder:

     ```
     mkdir -p $FOAM_RUN
     cd $FOAM_RUN/..
     ```

  2. Clone the repository and go into the cloned repository:

     ```
     git clone https://github.com/wyldckat/solidMechanics.git
     cd solidMechanics
     ```

  3. Checkout the repository respective to the version of OpenFOAM you are using:

   * OpenFOAM 2.3.x:

     ```
     git checkout OF23x
     ```

   * OpenFOAM 2.2.x:

     ```
     git checkout OF22x
     ```

   * OpenFOAM 2.1.x:

     ```
     git checkout OF21x
     ```

   * OpenFOAM 2.0.x:

     ```
     git checkout OF20x
     ```
     
   4. Build all of the libraries and utilities by running:

     ```
     ./Allwmake
     ```

   5. The tutorials are available at the folder `tutorials`.


Using Zip
---------

  1. Go to your user folder:

     ```
     mkdir -p $FOAM_RUN
     cd $FOAM_RUN/..
     ```

  2. Get the Zip file for the repository respective to the version of OpenFOAM you are using:

   * OpenFOAM 2.3.x:

     ```
     wget https://github.com/wyldckat/solidMechanics/archive/OF23x.zip
     ```

   * OpenFOAM 2.2.x:

     ```
     wget https://github.com/wyldckat/solidMechanics/archive/OF22x.zip
     ```

   * OpenFOAM 2.1.x:

     ```
     wget https://github.com/wyldckat/solidMechanics/archive/OF21x.zip
     ```

   * OpenFOAM 2.0.x:

     ```
     wget https://github.com/wyldckat/solidMechanics/archive/OF20x.zip
     ```

  3. Unzip the respective file and go into the respective folder, for example:

    ```
    unzip OF23x.zip
    cd solidMechanics-OF23x
    ```
    
  4. Build all of the libraries and utilities by running:

    ```
    ./Allwmake
    ```

  5. The tutorials are available at the folder `tutorials`.




License
=======

The same as OpenFOAM(R), namely GNU GPL v3. For more information, see the file LICENSE.

