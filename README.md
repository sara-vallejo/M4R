# M4R

Notebooks for preparaing data and imputing missing values are Data_preparation.ipynb and Imputations.ipynb.

In dHSIC_continents.ipynb we have the first version with code for computing dHSIC statistic and performing an independence test using this staistic. To do this we used a permutation test and chose as threshold the ($\alpha$-1)B th greatest statistic found (for B permutations). It also contains the algorithm we developed for finding high-order dependencies among SDGs goals/targets in an ascending order (starting with 2-way, then 3-way and so on). We then experiment on the goal level for different continents and make some visualitations of the Hypergraphs.

In dHSIC_groupings.ipynb similar computations are done but experimenting on different groupings of countries (e.g. Low income).

In dHSIC_continents_MC.ipynb, we make a change in the permutation test. We consider a Monte Carlo approximation as described in https://arxiv.org/abs/1603.00285. This would be more appropiate than what was explained before, since we are not computing all $n!^d$ permutations, but instead a lower number $B$.

In dHSIC_continents_normalised we introduce a normalisation for normal HSIC statistic, which corresponds to the distance correlation. Moreover, a slight modification in our previous code has made so that the Kernel matrices are precomputed and the algorithm is more efficient. Visualitations for both the 2-way graph and the hypergraphs are available.

In dHSIC_continents_change_alpha we experiment the results obtained when $\alpha$ in the independence test is reduced from $0.05$ to $0.01$. No major difference is observed.
