# M4R
Detecting and characterising higher-order interactions in time series:  an application to the United Nations Sustainable Development Goals.

### 0. Data imputation and preparation
We use World's Bank data set: https://databank.worldbank.org/source/sustainable-development-goals-(sdgs)#

- 0.Data_preparation: Cleaning up and transforming all country dataframes with SDG indicators into the same dimensions. Standardisation.
- 0.Imputations: Impute missing values using weighted kNN. Concatenate indicator data into final arrays for goals.
- 0.Plot_world: World maps with groupings of counties used in my thesis.
- 0.plots_of_data: Plots for showing the concatenation of indicator data for each SDG.


### 1. Computation of dHSIC on SDG data
- Functions for computing the statistic dHSIC and testing independence with a permutation test using a Monte Carlo approximation.
- We also scale pairwise dependencies found using the normalisation of HSIC.
- 1.dHSIC_continents_normalised: Computations for geographical groupings.
- 1.dHSIC_groupings_normalised: Computation for income-based groupings.


### 2. Visualisation of networks and hypergraphs. Computation of eigenvector centralities.
- 2.Network_plots: Plots of weighted networks and of their eigenvector centralities.
- 2.Complete_hypergraphs_plots: Plots of full hypergraphs (i.e. with all levels of dependencies)
- 2.Restricted_hx_plots_and_eig_centralities_CONTINENTS: Plots of hypergraphs for each level of dependence (i.e. 3-way hyperedges, 4-way hyperedges...). Computtion of eigenvector centralities for these sub-hypergraphs. For geographical groupings.
- 2.Restricted_hx_plots_and_eig_centralities_INCOME: Same for income-based groupings.

### 3. Proposed normalisation of dHSIC (dHcor)
- 3.Normalisation_of_dHSIC: Test our proposed measure dHcor on synthetic data and compare it to distance multicorrelation and generalized correlation.
- 3.dHcor_applied: Apply dHcor to SDG data.
