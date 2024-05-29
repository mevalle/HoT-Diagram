# HoT-Diagram

HoT Diagram is a short name for "Hasse of (Hypothesis) Test Diagram." The HoT diagram is a tool for comparing methods with statistical significance and easy visual interpretation. 

You should input (pandas) data frame where rows correspond to experiments, and columns correspond to methods. Optional parameters include the significance level of the hypothesis test (default: significance_level = 0.99), the assumption that the data follows a normal distribution (default: Gaussian = True), pre-processing the data (default: NormalizeData = False), and the information that the lower values are best (default: LowerAreBest = False).

The output is a boxplot and a Hasse diagram where the best models appear on top (if LowerAreBest = False). The Hasse diagram is a graph in which the nodes are the methods. An edge is built whenever the method on top overcomes the method above using  a pair-wise hypothesis test with the given significance level. Edges that can be deduced from transitivity are omitted from the diagram. Despite the best methods usually appearing at the top, the results should be carefully interpreted!

For further details on the Hasse diagram of a hypothesis test, see the paper: Weise, T., Chiong, R.: An alternative way of presenting statistical test results when evaluating the performance of stochastic approaches. Neurocomputing 147, 235–238 (2015). https://doi.org/10.1016/j.neucom.2014.06.071.
