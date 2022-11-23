### surf_code_sim
Program to simulate threshold of rotated surface code.
- The error model is one stochastic Pauli error after "encoding".
- The decoding algorithm is MWPM implemented in Pymatching package.

The program creates the lattice of qubits as a networkx graph and calculates its stabilizer generators. Errors are simulated by expressing in binary vector representation. Syndromes are calculated via the symplectic inner product. The bit flip and phase flip syndromes are decoded separately via Pymatching to get the correction. If the error followed by correction commutes with all stabilizer generators, then it is not a logical error. Otherwise, it is counted as a logical error. This is executed in a monte carlo simulation to get logical error rates.
