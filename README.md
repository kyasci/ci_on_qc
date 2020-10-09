
## Motivation for the project

With the much anticipated paradigm shift from 'classical' to 'quantum', it becomes a subject of great interest to make the most of it. Our motivation for this project lies in the fact that "Quantum Chemistry" promises the ability to accurately predict chemical and physical properties of molecules and materials. Predicting chemical properties using a first principles approach at the atomic scale is a theoretical and computational challenge [[1]](https://www.sciencedirect.com/bookseries/annual-reports-in-computational-chemistry). Even the most widely used classical simulation approaches like Hartree Fock (HF), Configuration Interaction Singles and Doubles (CISD), Coupled Cluster Singles and Doubles (CCSD),Full Configuration Interaction(FCI) fail to deliver chemical accuracy for larger systems and scale polynomially with larger systems. 

To give an idea , that why are we placing our bets on quantum computers to do chemical simulation, let's consider something that impacts the world in a great manner. Chemists hope that understanding FeMoco could accelerate efforts to improve upon the artificial catalyst currently used in industrial fertilizer production—a process that accounts for several percent (atleast 2-4%) of the world’s energy consumption. Unfortunately, classical methods such as DFT struggle to resolve the many closely-spaced energy levels of the complex FeMoco molecule[[2]](https://physics.aps.org/articles/v12/112).

With several applications in drug design, material science, water treatment - awaiting compuatational abilities- hopes ride on quantum computers’ potential to exactly simulate chemicals’ and materials’ quantum structures and behaviors.  Coming back to the example of FeMoco molecule, it's been estimated that simulation of FeMoco would need  200 perfectly-operating qubits and several weeks time[[3]](https://www.pnas.org/content/114/29/7555). However, qubits don’t operate perfectly, so thousands of additional qubits would likely be needed to stabilize the quantum states of the 200 “logical” qubits. With exciting possibilities and avenues to achieve greater computational powers and accuracies, scientists around the worls are striving to reach that goal. What do we have left to work upon if we need a large number of qubits to simulate molecules? IBM quantum roadmap promises 1000 qubits by 2023 so do we wait till then? No!

Even in this NISQ era, we have several variational algorithms that solve electronic structure problem on Noisy Intermediate Scale Quantum devices. Vaiational Quantum Eigensolver or VQE is one of the most feasible techniques yet. VQE can be used to generate ground state energies, excited state energies[[4]](https://arxiv.org/pdf/1805.08138.pdf) and several properties like charge density, dipole moment etc. of the molecules[[5]](https://arxiv.org/pdf/1509.04279.pdf). Studying reactions dynamics maybe a long shot for now, but we can start somewhere and accurately establishing molecular properties is a great advance. 

## What we tried to do

Keeping all this in mind, in this project, we have attempted to demonstrate such calculations for small molecules - believe me they are not at all small in terms of resources they need- using classical methods of Full Configuration Interaction(FCI) and Hartree fock(HF) method , as well as using variational algorithms . 

## Future possibilities and ideas for enhancing the project








# ci_on_qc

CI Implementation on QC as Simple as Possible.

## Abstract

Configuration interaction (CI)
is an exact post-Hartree-Fock method
of quantum chemistry within a given basis set.
Apart from the computational cost, it has many attractive features
from a conceptual view point, and you can find it suitable
for running on the quantum computer.

This project aims to implement CI by using
[Qiskit](https://github.com/Qiskit) to run on the quantum computer.
Our first priority is to make it simple so that you can
easily grasp the concept, and make it easy to test your idea
of static and dynamical simulations.
In contrast to the usual quantum computational chemistry,
we start from the non-zero CI matrix elements, which are somehow
evaluated on the classical computer.
All the complexity arising from quantum chemistry is handled by
the classical computer.
This matrix is expanded into the Pauli strings to generate
a qubit operator. We evaluate the ground state energy
by using the variational quantum eigensolver (VQE) algorithm.
