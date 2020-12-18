# QAOA
The number paritioning problem can be reformulated as minimising the cost function $H = |(N_i\vec{s_i})^2|$ where ${N_i}$ are the numbers to be minimised and s_i (either +1 or -1) are the apparent weights for those numbers. The set {Ni} is then partitioned if the cost function is zero or minimum. The cost function can be simplified as:

$H = \Sigma(N_i^2 s_i^2) + N_iN_js_is_j$

Where the first term is a constant and the second term is a quantum ising model (but not only with nearest neighbour interaction) given s_i are Pauli matrices.

Using QAOA, we sample different starting states by applying unitary evolution under time $\beta$ $\gamma$ and then measure the expectation value of the ising hamiltonian in the resulting state. We then use classical optimization techniques to minimise this expectation value hence minimising our cost function indirectly.


