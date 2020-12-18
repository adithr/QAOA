# QAOA
The number paritioning problem can be reformulated as minimising the cost function <a href="https://www.codecogs.com/eqnedit.php?latex=H&space;=&space;|(N_i\vec{s_i})^2|" target="_blank"><img src="https://latex.codecogs.com/gif.latex?H&space;=&space;|(N_i\vec{s_i})^2|" title="H = |(N_i\vec{s_i})^2|" /></a> where ${N_i}$ are the numbers to be minimised and s_i (either +1 or -1) are the apparent weights for those numbers. The set {Ni} is then partitioned if the cost function is zero or minimum. The cost function can be simplified as:

<a href="https://www.codecogs.com/eqnedit.php?latex=H&space;=&space;\Sigma(N_i^2&space;s_i^2)&space;&plus;&space;N_iN_js_is_j" target="_blank"><img src="https://latex.codecogs.com/gif.latex?H&space;=&space;\Sigma(N_i^2&space;s_i^2)&space;&plus;&space;N_iN_js_is_j" title="H = \Sigma(N_i^2 s_i^2) + N_iN_js_is_j" /></a>

Where the first term is a constant and the second term is a quantum ising model (but not only with nearest neighbour interaction) given s_i are Pauli matrices.

Using QAOA, we sample different starting states by applying unitary evolution under time <a href="https://www.codecogs.com/eqnedit.php?latex=\beta,&space;\gamma" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\beta,&space;\gamma" title="\beta, \gamma" /></a> and then measure the expectation value of the ising hamiltonian in the resulting state. We then use classical optimization techniques to minimise this expectation value hence minimising our cost function indirectly.


