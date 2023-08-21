# Explicit Equations for Fake Projective Plane (a = 7, p = 2, \emptyset, D_3 X_7)
This repository contains supplementary code for the paper *Explicit Equations for Fake Projective Plane (a = 7, p = 2, \emptyset, D_3 X_7)* by Borisov, Ji, and Li.

## Main Files

The main files are laid out in the current directory as follows. Unless specified otherwise, files with suffix **.txt** are Magma files.

### Magma Files
- [Section2.txt](Section2.txt) provides relevant verification codes that occur in Section 2 of the manuscript.

### Mathematica Files
- [Section3.nb](Section3.nb) calculates the equations of W and the birational model of Z.
- [Section4.nb](Section4.nb) computes the equations of the fake projective plane **(a = 7, p = 2, \emptyset, D_3 X_7)** in the number field and reduction modulo prime.

While all files can be executed independently on their own, the recommended order to run them are:
1. [Section2.txt](Section2.txt)
2. [Section3.nb](Section3.nb)
3. [Section4.nb](Section4.nb)

## Other Directories
The folders for this repository are as follows:
1. [Dependency](Dependency) : Contains pre-computed points and other dependencies for the main Mathematica files. 
    - The file **EqsFPP.txt** contains equations of the fake projective plane **(a = 7, p = 2, \emptyset, D_3 2_7)** produced in the [paper](https://arxiv.org/abs/1802.06333) *Explicit equations of a fake projective plane* by Borisov and Keum.

    - The file **4HD_one_section.txt** contains equations of one section of 4H + D from the FPP **(a=7, p=2, \emptyset, D_3 2_7)**. This is from the paper *On the Geometry of a Fake Projective Plane with 21 Automorphisms* and its accompanied [repository](https://github.com/mattie-ji/FPP-21-Geometry) by Borisov, Ji, Li, and Mondal.
    
    - The other files are all computed as part of this project.

2. [Equations](Equations): Contains relevant equations produced by the main Mathematica files:
    - **ginvariant_section_c3.txt** contains the 10 quadratics vanishing on the unique weight 0 section of 6H + D from the FPP **(a=7, p=2, \emptyset, D_3 2_7)**. These 10 quadratics are used in the definition of the coordinates U10, U11, ..., U19 in the calculation of W.
    - **minors_37.txt** contains three **7 x 7** minors of the Jacobian of the equations of **(a = 7, p = 2, \emptyset, D_3 X_7)** modulo 37.
    - **r-11_equations.txt** contains the 56 quadratics vanishing on **r_{-1,1}=0**.
    - **r00_equations.txt** contains the 56 quadratics vanishing on **r_{0,0}=0**.
    - **r11_equations.txt** contains the 56 quadratics vanishing on **r_{1,1}=0**.
    - **reduced_equations_37.txt** contains the equations of the FPP **(a = 7, p = 2, \emptyset, D_3 X_7)** reduced modulo 37. The coefficients here also include a cubic root of unity (See [Section4.nb](Section4.nb) for more details).
    - **Target_FPP_simple.txt** contains the 84 cubic equations defining the FPP **(a = 7, p = 2, \emptyset, D_3 X_7)** with coefficients in **Q(\sqrt{-7})**.
    - **ten_cubics.txt** contains the 10 cubic equations that defines the 10 sections of **X = (a = 7, p = 2, \emptyset, D_3 X_7)** in **2 K_X**.
    - **W_equations.txt** contains the 100 equations of the double cover W. The first 45 equations are the odd equations, and the second 55 equations are the even equations.
    - **Z_singular_equations.txt** contains the 66 cubic equations defining a birational model of Z.


3. [Verification](Verification): Contains code verifying the results produced by the main Mathematica files:
    - **FPP_Hilbert.txt** checks the Hilbert polynomial of the FPP **(a = 7, p = 2, \emptyset, D_3 X_7)**. 
    - **FPP_M2.txt** is a Macaulay2 file checking that the embedding of the FPP **X = (a = 7, p = 2, \emptyset, D_3 X_7)** is in **2 K_X**.
    - **FPP_smoothness_Hodge.txt** checks that the equations of the FPP **(a = 7, p = 2, \emptyset, D_3 X_7)** is smooth and computes its Hodge numbers modulo prime.
    - **r_11_check_Hilbert.txt** checks the Hilbert polynomial of **r_{1, 1}=0**.
    - **W_check_Hilbert.txt** checks the Hilbert polynomial of W.
    - **Z_singular_Hilbert.txt** shows the Hilbert polynomial of the birational model of Z.