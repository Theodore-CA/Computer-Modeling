# This repo contains the projects I worked on for my computer modeling class
Each project mainly uses libil 2.6.1: https://libigl.github.io/, a C++ library for geometry processing. Each project is written in Python.

## Project 1: Practice With libigl
The focus of this project was to get aquainted with libigl by calling some useful functions, and doing a simple subdivision scheme.
### Flat Shading and Per-vertex Shading:
<img width="514" height="456" alt="image" src="https://github.com/user-attachments/assets/37ec5f69-1842-4eaf-9511-8a1b789c5d94" />
<img width="522" height="450" alt="image" src="https://github.com/user-attachments/assets/81d2d05b-d091-44dc-9fd2-f2a8a7b25829" />

### Subdivision scheme:
<img width="692" height="1119" alt="image" src="https://github.com/user-attachments/assets/8a8e305a-0860-44d1-ba01-54f90f7fcdc5" />

## Project 2: Surface Reconstruction Using a Point Cloud
This project uses a provided point could to calculate the "inside" and "outside" of the surface, then constructs it.
### Obtaining the Luigi Point Cloud:
<img width="445" height="535" alt="image" src="https://github.com/user-attachments/assets/32225c0e-c59d-4176-8b4f-e264d49e8e54" />

### Calculate Inside (Green), Surface (Blue), and Outside (Red):
<img width="474" height="587" alt="image" src="https://github.com/user-attachments/assets/5a6af1c6-1160-4d3b-9568-cc0040e09620" />

### Use "Moving Least Squares" Algorithm to Obtain the Surface (Purple):
<img width="512" height="547" alt="image" src="https://github.com/user-attachments/assets/ba8ac41b-5169-461d-8589-ee6d3f243184" />

### Extract the Surface and Cull Artifacts:
<img width="502" height="561" alt="image" src="https://github.com/user-attachments/assets/be68bf41-88f9-4132-83c6-6d626f85918a" />
<img width="433" height="537" alt="image" src="https://github.com/user-attachments/assets/a7ba63b2-9ff8-4db9-854f-357ebf9dd270" />

## Project 3: Vertex Normals, Principal Curvature, and Object Smoothing:
In this project we explore different types of ways to obtain the normals of each vertex in a mesh, display the principal curvature, and smooth a surface.
### An example of one of the vertex normal algorithms (Quadratic Fitting Normals):
<img width="498" height="394" alt="image" src="https://github.com/user-attachments/assets/496aa79a-a548-44e9-a6f9-a8a0994e6c9d" />

### Principal Curvature (Min: Red, Max: Green)
<img width="638" height="602" alt="image" src="https://github.com/user-attachments/assets/e3257a86-998f-49bc-a2c6-8de7f683af88" />

### Explicit and Implicit Laplacian Smoothing:
Explicit: <img width="1588" height="350" alt="image" src="https://github.com/user-attachments/assets/c3dca2ba-1606-4245-b8e8-35b109416884" />
Implicit: <img width="1632" height="326" alt="image" src="https://github.com/user-attachments/assets/acef8a55-68c1-4732-ac1a-065024a9504e" />

## Project 4: Vector Feilds, Gradients, and Harmonic/LSCM Parameterization:
This project focused on a couple of things. First is creating a vector feild on a mesh based on some constraint. Then creating a scalar function to make a gradient on the surface.
Then Harmonic and LSCM parameterization to flatten a mesh to a 2d plane.
### Vector Feild and Reconstructed Scalar Feild:
<img width="520" height="457" alt="image" src="https://github.com/user-attachments/assets/45c9d661-694d-4900-b209-aadf2ad0e6e6" />
<img width="1240" height="582" alt="image" src="https://github.com/user-attachments/assets/e6ef72ab-ddf6-4822-bc9c-7a8040e4f907" />

### Harmonic and LSCM parameterization:
Harmonic: <img width="1409" height="352" alt="image" src="https://github.com/user-attachments/assets/b0848ad9-334f-4aca-a3be-11177c556888" />
LSCM: <img width="1271" height="330" alt="image" src="https://github.com/user-attachments/assets/700c49a4-6f02-44bd-a2a5-2f5696d95d23" />

## Project 5: Multiresolution Mesh Editing:
This project focused on manipulating certain parts of a mesh while leaving others untouched. Used a minimzation on the manipulated thin-plate energies to obtain best fitting locations 
for updated verticies by solving a bi-Laplacian system. Begins by storing the high frequency detail of the mesh, smooths it to allow for easier manipulation, then reapplies the detail after the manipulation.
This is the original hand:
<img width="580" height="555" alt="image" src="https://github.com/user-attachments/assets/0b965248-0932-4a62-a773-069fb2dec396" />
This is the smoothed version:
<img width="352" height="414" alt="image" src="https://github.com/user-attachments/assets/59ea611c-74e1-42b7-aa8c-a29e5ce68f94" />
This is the smoothed + deformed:
<img width="395" height="375" alt="image" src="https://github.com/user-attachments/assets/e2937efa-cc63-491a-8013-9a7a056e8b05" />
This is with the reapplied detail:
<img width="371" height="390" alt="image" src="https://github.com/user-attachments/assets/d67c91e4-23f9-4ebf-b75c-dd79f91d977d" />

