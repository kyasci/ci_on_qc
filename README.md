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
