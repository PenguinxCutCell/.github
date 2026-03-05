# .github

Here is a simple flow chart:

```mermaid
graph TD

%% Layer A — Mesh
A[CartesianGrids.jl<br/>Cartesian mesh definitions]

%% Layer B — Geometry
B[CartesianGeometry.jl<br/>Geometric moments & cut-cell geometry]
A --> B

%% Geometry backends (bidirectional for VOF*)
B <--> B1[VofiJul.jl]
B <--> B2[Vofinit.jl]
B <--> B3[VOFTools.jl]
B <-->  B4[ImplicitIntegration.jl]

%% Geometry -> Operators
C[CartesianOperators.jl<br/>Discrete FV operators<br/> advection, diffusion]
B --> C

%% BCs
D[PenguinBCs.jl<br/>Boundary & interface conditions]
D --> C

%% Solver core
E[PenguinSolverCore.jl<br/>Time loop & linear system assembly]
C --> E
D --> F

%% Physics solvers
F[Penguin.jl<br/>Core framework]
E --> F
F --> F1[PenguinDiffusion.jl]
F --> F2[PenguinTransport.jl]
F --> F3[PenguinTransportDiffusion.jl]
F --> F4[PenguinStokes.jl]
F --> F5[PenguinStefan.jl]

%% Interface tracking
G[Interface Tracking Algorithms]
F5 --> G
G --> G1[LevelSetMethods.jl]
G --> G2[gVOF.jl]
```
