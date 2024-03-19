# cLFV_GlobalBounds
This repository contains the global bounds and inverse correlation matrices needed to build the proxy- $\chi^2$ that encodes the results of [arXiv:2403.09772] in the SMEFT scenario. The bounds and correlations are given at the 95% C.L. and should only be used to extract the corresponding 95% C.L. bounds for a specific UV-complete scenario. This is due to the fact that the extreme non-gaussianity of our test statistics makes it so that constraints change dramatically between different C.L.

Global bounds and correlations are available for the following scenarios:
- $\tau-\ell$ operators involving all light quarks and with only first generation quarks
- $\tau-\ell$ operators involving only first generation quarks
- $\mu-e$ operators involving all light quarks after the inclusion of nuclear uncertainties
- $\mu-e$ operators involving only first generation quarks after the inclusion of nuclear uncertainties

IMPORTANT NOTE: Due to the extreme correlations present in the $\mu-e$ sector, which cause a degradation of ~8 orders of magnitude between the global and one-at-a-time bounds, the resulting correlation matrix is numerically ill-behaved. This means that there will be sizeable errors upon inversion of the matrix due to finite numerical precision. We find that float64 is not enough in order to keep the numerics well-behaved, and 20-digit precision is enough for this purpose. Nevertheless, a user naively loading the .txt files in their favourite programming language (e.g. Mathematica, Python...) and trying to reproduce our global bounds will find discrepancies at the 30% level, which is a tolerable amount of mismatch.
