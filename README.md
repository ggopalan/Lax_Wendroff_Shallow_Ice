This notebook implements a Lax-Wendroff 2-D finite difference method that numerically solves the shallow ice approximation (SIA) partial differential equation (PDE), which is derived in:

Gopalan, G., Hrafnkelsson, B., Aðalgeirsdóttir, G., Jarosch, A. H., & Pálsson, F. (2018). A Bayesian hierarchical model for glacial dynamics based on the shallow ice approximation and its evaluation using analytical solutions. The Cryosphere, 12(7), 2229-2248.

The core logic of this approach is to integrate a Taylor approximation forward in time with two temporal derivatives of the thickness field, and to substitute spatial partial derivatives for the temporal derivatives, which are approximated with central differences.

The finite difference method is demonstrated on the periodic test case D of:

Bueler, E., Lingle, C. S., Kallen-Brown, J. A., Covey, D. N., & Bowman, L. N. (2005). Exact solutions and verification of numerical models for isothermal ice sheets. Journal of Glaciology, 51(173), 291-306,

with a mass balance forcing period of 20 years, substantially more frequent than the original 5000 year period. This is a setting where using the second time derivative of thickness provides an advantage over a method only using a first time derivative, due to a fast changing forcing.  
