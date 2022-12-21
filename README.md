Using Tensor contraction to store geological model objects
=KRUTYE=
Daniil Sherki, Egor Cherepanov, Egor Malkershin

A three-dimensional geological model of a hydrocarbon reservoir is a three-dimensional representation of a reservoir in the form of a multidimensional object, which maximally reflects the geological structure of the object under study and is used to study the field production processes. As a result, a geological model is a copy of a real oil/gas field, but in the form of a set of cells of different size (often 5𝑚 × 5𝑚 × 1𝑚), the grid of cells stores various properties: saturation, permeability along the directions, porosity, etc.

Everything comes down to storing a large number of three-dimensional tensors and manipulating them. Due to small cell size in comparison with the size of the field itself, the number of cells can be large (11 trillion cells for the Gawar field, assuming that the cell size is 8𝑚 × 8𝑚 × 1𝑚).

Our first task is to represent the tensors of field properties: NTG, permeability, porosity, saturation of fluid in the form of compressed tensors, which can be restored with a certain error. The second task is to evaluate the quantity of this error and the applicability of this method to geological modeling.

We assume to use the following methods to compress tensors:
* Canonycal Polyadic Decomposition
* Tensor-Train Decomposition
* Tucker decomposition

Sources:
1. Oseledets, Ivan. (2011). Tensor-Train Decomposition. SIAM J. Scientific Computing. 33. 2295-2317. 10.1137/090752286.
2. Tucker LR. Some mathematical notes on three-mode factor analysis. Psychometrika. 1966 Sep;31(3):279-311. doi: 10.1007/BF02289464. PMID: 5221127.

The _=*KRUTYE*=_ team team would like to thank the movie "Fight Club" with Ryan Gosling for the motivation that contributed to this project.
