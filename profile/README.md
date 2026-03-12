# 🐧 PenguinxCutCell

## 📦 The Project

- **[CartesianGrids.jl](https://github.com/PenguinxCutCell/CartesianGrids.jl)** - Cartesian Grids definitions and utilities

- **[CartesianGeometry.jl](https://github.com/PenguinxCutCell/CartesianGeometry.jl)** - Cartesian geometry utilities and operations for computational geometry
  - **[VofiJul.jl](https://github.com/PenguinxCutCell/VofiJul.jl)** - Volume fraction calculation tools from C VOFI from a signed distance function
  - **[Vofinit.jl](https://github.com/PenguinxCutCell/Vofinit.jl)** - Volume fraction calculation tools from Julia VOFI from a signed distance function
  - **[VOFTools.jl](https://github.com/PenguinxCutCell/VOFTools.jl)** - Volume fraction calculation tools from Julia VOFTools from a vof field + plic interface
  - **[ImplicitIntegration.jl](https://github.com/maltezfaria/ImplicitIntegration.jl)** - External Library from (L. Maltez Faria) Quadrature on implicitly defined function

- **[CartesianOperators.jl](https://github.com/PenguinxCutCell/CartesianOperators.jl)** - Cartesian Operators (Diffusion, Advection, ...) 

- **[PenguinBCs.jl](https://github.com/PenguinxCutCell/PenguinBCs.jl)** - Standardized type for Outer Box Boundary condition and Interface condition

- **[PenguinSolverCore.jl](https://github.com/PenguinxCutCell/PenguinSolverCore.jl)** - Low-level machinery for time loop, linear system assembly

- **[Penguin.jl](https://github.com/PenguinxCutCell/Penguin.jl)** - The foundational library providing core functionality for cut-cell computations
  - **[PenguinDiffusion.jl](https://github.com/PenguinxCutCell/PenguinDiffusion.jl)** - One/Two-phase diffusion models and solvers
  - **[PenguinTransport.jl](https://github.com/PenguinxCutCell/PenguinTransport.jl)** - One/Two-phase transport models and solvers
  - **[PenguinTransportDiffusion.jl](https://github.com/PenguinxCutCell/PenguinTransportDiffusion.jl)** - One/Two-phase advection-diffusion models and solvers
  - **[PenguinStokes.jl](https://github.com/PenguinxCutCell/PenguinStokes.jl)** - One/Two-phase Stokes Flow models and solvers
  - **[PenguinNavierStokes.jl](https://github.com/PenguinxCutCell/PenguinNavierStokes.jl)** - One/Two-phase Navier-Stokes Flow models and solvers
  - **[PenguinStefan.jl](https://github.com/PenguinxCutCell/PenguinStefan.jl)** - One/Two-phase Stefan models and solvers
  - **[PenguinDarcy.jl](https://github.com/PenguinxCutCell/PenguinDarcy.jl)** - One/Two-phase Darcy models and solvers
  - **[PenguinStreamVorticity.jl](https://github.com/PenguinxCutCell/PenguinStreamVorticity.jl)** - One-phase Streamfunction-Vorticity models and solvers

- **[]()** Interface Tracking Algorithms
  - **[GlobalHeightFunctions.jl](https://github.com/PenguinxCutCell/GlobalHeightFunctions.jl)** - Global Height Functions tracking
  - **[LevelSetMethods.jl](https://github.com/maltezfaria/LevelSetMethods.jl)** - External Library for Level-Set Methods
  - **[isoap.jl](https://github.com/PenguinxCutCell/isoap.jl)** - Iso-surface extraction on arbitrary polyhedra and grids (J. Lopez, et al.)
  - **[gVOF.jl](https://github.com/PenguinxCutCell/gVOF.jl)** - Unsplit geometrical VOF method (J. Lopez, et al.)

- **[PenguinAnalysis.jl](https://github.com/PenguinxCutCell/PenguinAnalysis.jl)** - Weighted discrete error norms and convergence utilities 

- **[PenguinPlots.jl](https://github.com/PenguinxCutCell/PenguinPlots.jl)** - Visualization tools for solver's outputs

- **[STLInputs.jl](https://github.com/PenguinxCutCell/STLInputs.jl)** - To read and instantiate geometries defined by STL file

- **[sandbox](https://github.com/PenguinxCutCell/sandbox)** - Experimental space for new ideas and prototypes

## 🚧 Feature Matrix

Legend: ✅ done · 🟡 ongoing / partial · ⚪ planned · 🔬 experimental

| Package | Core scope | Status | Notes / next milestones |
|---|---|---:|---|
| `CartesianGrids.jl` | Cartesian meshes, indexing, grid utilities | ✅ | Stable base layer |
| `CartesianGeometry.jl` | Cut-cell geometry, moments, barycenters, apertures | ✅ | Reduce allocations, add curvature |
| `VofiJul.jl` | SDF → volume fraction via VOFI backend | ✅ | Useful pure Julia alternative |
| `Vofinit.jl` | Julia-based SDF → volume fraction init | ✅ | Production utility |
| `VOFTools.jl` | VOF/Plic reconstruction and tools | ✅ | Reconstruction workflows still expanding |
| `CartesianOperators.jl` | Discrete FV operators (diffusion, advection, gradient, divergence, etc.) | ✅ | More multiphysics/operator variants to add |
| `PenguinBCs.jl` | Outer-box BCs and interface conditions | ✅ | Continue enriching BC/IC catalogue |
| `PenguinSolverCore.jl` | Time loops, assembly helpers, solver machinery | 🟡 | Coupling, adaptive stepping, generic utilities in progress |
| `PenguinDiffusion.jl` | One/two-phase diffusion, fixed + moving interface | ✅ | Main mature scalar solver |
| `PenguinTransport.jl` | One/two-phase transport | 🟡 | Moving mono/diphase still under active development |
| `PenguinTransportDiffusion.jl` | One/two-phase advection-diffusion | 🟡 | Fixed-interface implementation advancing, moving planned |
| `PenguinStokes.jl` | One/two-phase Stokes flow | 🟡 | Fixed-interface strong, moving/FSI under development |
| `PenguinNavierStokes.jl` | One/two-phase Navier–Stokes | 🟡 | Transfer from Stokes ongoing |
| `PenguinStefan.jl` | One/two-phase Stefan problems | 🟡 | Height Function Level Set strong VOF / Front Tracking free-boundary workflows expanding |
| `PenguinDarcy.jl` | One/two-phase Darcy flow | 🟡 | Gravity, tensor permeability, wells, free boundary next |
| `PenguinStreamVorticity.jl` | Streamfunction–vorticity solver | 🟡 | 2D base in progress, 3D extension planned |
| `GlobalHeightFunctions.jl` | Global height-function interface tracking | ✅ | Curvature extension |
| `LevelSetMethods.jl` | Level-set transport / reinit (external) | ✅ | External dependency / interoperability target |
| `isoap.jl` | Iso-surface extraction on arbitrary polyhedra | ✅ | Interoperability / geometry support |
| `gVOF.jl` | Geometrical unsplit VOF | ✅ | Interoperability / future free-surface workflows |
| `PenguinAnalysis.jl` | Weighted norms, convergence, interface error metrics | ✅ | Modal analysis, etc ... |
| `PenguinPlots.jl` | Plotting and animations for solver outputs | 🟡 | Makie-based visualization under development |
| `STLInputs.jl` | STL import, geometry instantiation, SDF bridge | 🟡 |  early-stage package |
| `sandbox` | Experiments and prototypes | 🔬 | Rapid testing area |

## 📌 Physics Capability Matrix

Legend: ✅ available · 🟡 partial / ongoing · ⚪ planned

| Capability | Diffusion | Transport | Adv-Diff | Stokes | Navier-Stokes | Stefan | Darcy | Stream-Vorticity |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| One-phase, fixed embedded boundary | ✅ | ✅ | 🟡 | ✅ | 🟡 | n/a | ✅ | 🟡 |
| Two-phase, fixed interface | ✅ | 🟡 | 🟡 | ✅ | 🟡 | ✅ | 🟡 | n/a |
| Prescribed moving interface / boundary | ✅ | 🟡 | ⚪ | 🟡 | ⚪ | ✅ | ⚪ | ⚪ |
| Free boundary evolution | ⚪ | ⚪ | ⚪ | ⚪ | ⚪ | 🟡 | ⚪ | ⚪ |
| Steady solver | ✅ | ✅ | ✅ | ✅ | 🟡 | n/a | ✅ | 🟡 |
| Unsteady solver | ✅ | ✅ | 🟡 | ✅ | 🟡 | ✅ | 🟡 | 🟡 |
| Interface jump conditions | ✅ | 🟡 | ✅ | ✅ | 🟡 | ✅ | 🟡 | n/a |
| Embedded force / traction post-processing | n/a | n/a | n/a | ✅ | 🟡 | n/a | ⚪ | n/a |
| Convergence / analysis workflows | ✅ | 🟡 | 🟡 | ✅ | 🟡 | 🟡 | 🟡 | ⚪ |
| Examples & regression tests | ✅ | 🟡 | 🟡 | ✅ | 🟡 | 🟡 | 🟡 | 🟡 |

## 🛠️ Ongoing Development / TODO

### Core infrastructure
- [ ] Strengthen interoperability between geometry, operators, and solver layers
- [ ] Add more generic multiphysics coupling utilities in `PenguinSolverCore.jl`
- [ ] Add adaptive time-stepping helpers for moving/free-boundary problems
- [ ] Expand CI, regression tests, and convergence-report tooling across all repos
- [ ] Standardize docs structure across packages: models, API, examples, validation, feature matrix

### Geometry and interface representation
- [ ] Extend `CartesianGeometry.jl` toward curvature support
- [ ] Add robust utilities for interface sampling, normals, curvature, and interfacial quadrature
- [ ] Improve bridges between level-set, VOF, and global height-function descriptions
- [ ] Add STL → SDF / cut-cell workflow through `STLInputs.jl`

### Scalar transport family
- [ ] Finalize moving one-phase and two-phase support in `PenguinTransport.jl`
- [ ] Complete fixed one/two-phase support in `PenguinTransportDiffusion.jl`
- [ ] Add moving-interface advection-diffusion formulations
- [ ] Add more analytical and manufactured solutions for transport validation
- [ ] Investigate and fix degraded convergence in moving transport cases

### Fluid solvers
- [x] Extend `PenguinStokes.jl` to prescribed moving boundaries/interfaces
- [x] Add stronger FSI-oriented building blocks and rigid-body coupling
- [ ] Continue transfer from `PenguinStokes.jl` to `PenguinNavierStokes.jl`
- [ ] Add benchmark suites for one-phase/two-phase fixed and moving flows
- [x] Extend post-processing: drag, lift, integrated stresses, interfacial force balance

### Free-boundary and phase change
- [x] Continue `PenguinStefan.jl` development with global height-function updates
- [x] Add residual-based inner iterations and convergence diagnostics
- [x] Extend Gibbs–Thomson / curvature / kinetic corrections
- [ ] Develop one-phase and two-phase free-boundary Darcy workflows
- [ ] Build canonical validation cases for moving sharp-interface problems

### Analysis and visualization
- [x] Expand `PenguinAnalysis.jl` with interface-only norms and weighted `H1`-style seminorms
- [x] Add region-wise norms (`all`, `full`, `cut`, `interface`)
- [x] Build `PenguinPlots.jl` Makie recipes for fields, interfaces, residuals, and animations
- [ ] Add standardized convergence-report figures and summary tables

## 🧭 Near-Term Roadmap

### Priority 1
- [ ] Consolidate `PenguinTransport.jl`
- [ ] Consolidate `PenguinTransportDiffusion.jl`
- [ ] Extend `PenguinStokes.jl` to moving-boundary cases
- [ ] Continue `PenguinNavierStokes.jl` transfer from Stokes infrastructure

### Priority 2
- [ ] Strengthen `PenguinStefan.jl` free-boundary workflows
- [ ] Develop `PenguinDarcy.jl` toward free-boundary and two-domain problems
- [ ] Add adaptive time stepping in `PenguinSolverCore.jl`

### Priority 3
- [ ] Build `PenguinPlots.jl`
- [ ] Build `STLInputs.jl`
- [ ] Extend `PenguinStreamVorticity.jl` and explore 3D formulations


### Specialized Applications

- **[FrontCutTracking.jl](https://github.com/PenguinxCutCell/FrontCutTracking.jl)** - Front tracking and cut-cell interface methods
- **[BenchPhaseFlow.jl](https://github.com/PenguinxCutCell/BenchPhaseFlow.jl)** - Benchmarking suite for phase flow simulations
- **[ImplicitCutIntegration.jl](https://github.com/PenguinxCutCell/ImplicitCutIntegration.jl)** - Advanced implicit integration methods for cut cells
- **[VTKOutputs.jl](https://github.com/PenguinxCutCell/VTKOutputs.jl)** - VTK file format output capabilities for visualization in ParaView and other tools


## 💻 Technology Stack

Julia

## 📝 License

