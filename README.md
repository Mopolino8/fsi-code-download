# fsi-code-download
The method has been presented systematically in the attached thesis: one-field fictitious domain method_PhD thesis_2018.PDF

The 2-step splitting scheme decouples the convection and diffusion steps of the Navier-Stokes equations, and a preconditioned MinRes algorithm is used to solve the Stokes problem, however this linear solver cannot converge for channel flows, such as Test8 and Test11 in the attached thesis. When further splitting the Stokes equation as diffusion and pressure steps, the diffusion problem can be efficiently solved using Conjugate Gradient method while the pressure step can be efficiently solved using preconditioned MinRes algorithm. This is why the 3-step splitting scheme is introduced, and this scheme can solve all the numerical test in the thesis.

For both schemes, the input files are the same. User should provide a mesh of the fluid and a mesh of the solid defined in the folder ‘input’, and some other basic files like time step, material properties, etc, all of which are defined in the folder ‘input’ as well. At the same time, user should define the boundary and initial conditions in the folder ‘bc’.

Mesh can be generated by any software package, as long as saved as the same format using in this piece of code. In order to start, several examples of input files and boundary conditions are provide together with the code. These examples have been successfully compiled and tested on Windows and Linux systems. 

Now download it from the “Clone and download” button (green) on the right-hand side, and have a try!