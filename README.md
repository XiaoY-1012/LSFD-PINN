# LSFD-PINN
Supplementary code for the publication: "Xiao Y, Yang L M, Shu C, et al. Least-square finite difference-based physics-informed neural network for steady incompressible flows[J]. Computers & Mathematics with Applications, 2024, 175: 33-48. https://doi.org/10.1016/j.camwa.2024.08.035".
# Abstract
In this work, a least-square finite difference-based physics-informed neural network (LSFD-PINN) is proposed to simulate steady incompressible flows. The original PINN employs the automatic differentiation (AD) method to compute differential operators. However, the AD method, which is essentially based on the chain rule, requires a series of matrix operations to obtain derivatives during the training process. This may reduce computational efficiency, especially for large-scale networks. Additionally, the AD method still needs to compute lower-order derivative terms even if the partial differential equation (PDE) involves only higher-order derivatives, leading to unnecessary calculations. Although conventional finite difference (FD) methods can effectively mitigate these limitations, they only consider information in a single direction. Moreover, they require introducing extra virtual collocation points for each collocation point to assist in computing differential operators when using randomly distributed collocation points. This increases the computational effort and storage requirements, especially in scenarios involving high-order discretization schemes or a large number of collocation points. To address these issues, we introduced the least squares finite difference (LSFD) method to calculate the differential operators required in PINN. Compared to the AD method, the LSFD method relies only on the network's output for calculating derivatives, thus avoiding a series of matrix operations. In comparison to the FD method, the LSFD not only considers multi-directional information but also can be applied to random point distributions without the need for introducing virtual points. To demonstrate its effectiveness, LSFD-PINN is tested on representative problems such as lid-driven cavity flow, flow around a backward-facing step, and flow around a circular cylinder in a pipe. Numerical results indicate that LSFD-PINN achieves satisfactory accuracy without any labeled data, significantly outperforming AD-PINN and FD-PINN, especially in high Reynolds number flows. Additionally, the computational efficiency of LSFD-PINN is superior to that of AD-PINN.
# Citation
@article{XIAO202433,
title = {Least-square finite difference-based physics-informed neural network for steady incompressible flows},
journal = {Computers & Mathematics with Applications},
volume = {175},
pages = {33-48},
year = {2024},
issn = {0898-1221},
doi = {https://doi.org/10.1016/j.camwa.2024.08.035},
url = {https://www.sciencedirect.com/science/article/pii/S0898122124004024},
author = {Y. Xiao and L.M. Yang and C. Shu and H. Dong and Y.J. Du and Y.X. Song},
keywords = {Physics-informed neural network, Steady incompressible flows, Least-square finite difference, Automatic differentiation method}
}
