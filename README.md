### surf_code_sim
Program to simulate threshold of rotated surface code.
- The error model is one stochastic Pauli error after "encoding".
- The decoding algorithm is MWPM implemented in Pymatching package.

The program creates the lattice of qubits as a networkx graph and calculates its stabilizer generators. Errors are simulated by expressing in binary vector representation. Syndromes are calculated via the symplectic inner product. The bit flip and phase flip syndromes are decoded separately via Pymatching to get the correction. If the error followed by correction commutes with all stabilizer generators, then it is not a logical error. Otherwise, it is counted as a logical error. This is executed in a monte carlo simulation to get logical error rates.

Some results obtained using the program:

<img src="https://user-images.githubusercontent.com/61590679/203651667-2da595e5-a5e8-4d20-93c4-ae18041e4f04.PNG" alt="fig1" width="600"/>

<img src="https://user-images.githubusercontent.com/61590679/203651697-52684852-0e70-4c05-a6a9-03ac8ab7e42f.PNG" alt="fig2" width="600"/>

These are in close agreement with values reported in literature for this code, error model and decoder.
