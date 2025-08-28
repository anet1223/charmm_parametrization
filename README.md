# CHARMM force field parametrization of small molecules via ffTK.
## Molecules:
* Baicalein
* Chrysin
* Luteolin
## Parametrization procedure:
The initial three-dimensional structures of baicalein, chrysin, and luteolin were obtained from the PubChem database. Automated parameter generation was performed using CGenFF v4.013. For quantum-based parameterization, the VMD plugin ffTK v2.116 and Gaussian 1620 were
employed.
First, the stream file (.str) produced by CGenFF was divided into existing and analogy parameter files, with only the analogy parameters subjected to further optimization. Geometry optimization was performed at the MP2/6-31++G** level of theory. Partial atomic charges were refined in ffTK based on the water interaction profiles calculated at the HF/6-31G* level. The QM Hessian
matrix, computed at the MP2/6-31G* level, was used to optimize the bond and angle parameters with slight adjustments to the default ffTK settings (Geom. Weight set to 2.0; Angles – Eq. Deviation reduced to 5.0). Each dihedral angle was scanned in both directions from the equilibrium value in 5-degree steps at the MP2/6-31G* level. The periodicity and phase shift were assigned according to the analogy
parameters from CGenFF and remained fixed during optimization. The maximum force constant (Kmax) was set to 4.5, and the energy cutoff was maintained at 10 kcal/mol. The initial dihedral optimization was performed using an annealing protocol, followed by a downhill protocol with a tolerance of 0.0001. The potential energy surfaces (PES) from both QM and
molecular mechanics (MM) calculations were visually inspected using VMD plotting tools to assess the fit and root mean square error (RMSE), and further refinement was performed as needed. The parameterization process was iterative and continued until convergence was achieved, typically within four iterations.
