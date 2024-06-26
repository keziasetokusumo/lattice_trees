## Lattice Models for Derivatives Valuation
Lattice methods are numerical techniques for valuing financial market derivatives, such as options. These methods are effective for assets whereby underlying price dynamics are uncertain and follow a discrete path over time. The key idea behind lattice methods is to model the possible future price movements of the underlying asset in a series of discrete steps, represented as a lattice or tree structure.

We can build these models in Python. This repository contains code for the binomial and trinomial models, which value European and American calls and puts. We further explore the difference in output as parameters are adjusted. The binomial and trinomial models are popular numerical methods in financial mathematics, particularly for pricing derivatives like options. They are based on discrete-time models representing an underlying asset's possible future price movements. Here's a summary of both models:

### Binomial Model
Concept:
- The binomial model assumes that the underlying asset's price can increase or decrease each time step until the option expires.
It constructs a binomial tree in which each node represents a possible asset price at a particular time.
- At each node, the price can move up by a factor 𝑢 or down by a factor 𝑑.

Model Construction:
- Start at the current price of the asset.
- For each time step, calculate the possible future prices based on the up and down factors 𝑢 and 𝑑.
- At each node, use risk-neutral probabilities to calculate the expected future values of the option's payoff.
- Work backward through the tree to compute the option's present value at each node.

### Trinomial Model
Concept:
- The trinomial model extends the binomial model by allowing for three possible asset price movements at each time step: up, down, or stay the same.
- Like the binomial model, it constructs a tree of possible asset prices over time.

Model Construction:
- Similar to the binomial model but with an additional state (staying the same) at each time step.
- The trinomial tree has more nodes than the binomial tree, providing potentially more accurate price estimations.

Link to complete [code](https://github.com/keziasetokusumo/lattice_trees/blob/main/Lattice%20Methods%20Black%20Scholes.ipynb).
