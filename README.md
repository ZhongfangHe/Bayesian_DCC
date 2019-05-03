# Bayesian Dynamic Correlation Models
A collection of codes that perform MCMC estimation of a number of dynamic correlation models, including three existing models: DCC (Engle 2002), VC (Tse and Tsui 2002), cDCC (Aielli 2013) and four versions of the proposed new model: GDC, top-integrated GDC (TIGDC), bottom-integrated GDC (BIGDC), both-levels-integrated GDC (IGDC). 

I am aware of the R package "bayesDccGarch" by Fiorucci et al. that performs Bayesian estimation of the DCC model. Nevertheless I find its implementation of the parameter restrictions unsatisfying. Specifically let a and b be the parameters governing the dynamics of the correlation matrix in the DCC model. We need not only 0<a<1 and 0<b<1 but also 0<a+b<1. From what I see, the package "bayesDccGarch" only enforces the former two constraints for individual parameters but not for the sum of the two parameters. In my implementation, I explicitly enforces 0<a+b<1.  
