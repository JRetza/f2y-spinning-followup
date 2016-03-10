
The authors apologize for the delay in resubmitting this paper as we have been
rather preoccupied with work connected to LIGO's first observing run and
GW150914. We are grateful to the referee for their review and include comments
below.


# Referee comments

1. 50,000 sources were simulated, but only 250 of these were chosen for
   parameter estimation. The original 50,000 sources were chosen with a random
   distribution of masses and spins with likely ranges for BNS systems. The
   masses, spins and extrinsic parameters (sky location, orientation,
   polarisation, distance, etc) make up a 15-dimensional parameter space, over
   which 250 sources corresponds to a very sparse sampling. Does this sparse
   sampling impact any of the conclusions in this paper?

The subsample for parameter estimation should give a fair representation of the
potential sources we could see with Advanced LIGO. We may not cover the entire
parameter space, but 250 should give an ample cross-section of parameter space
to work out typical behavior. We only expect to detect a small number of
signals with Advanced LIGO, hence we are not too concerned if we miss some
small atypical corners of parameter space; however, we do not think it is
likely that there will be variation in results beyond what we have studied
here. Overall, we think that our conclusions are robust.

In previous work we have checked that this subsample is consistent with the
distributions used to draw samples: we have added a sentence to point this out
in section 2. Since we do not see a variation in these intrinsic parameters
from considering this subset, we believe that we have enough sources to
draw our conclusions.


2. The 90% credible regions in Fig. 5 are confusing. The text explains that in
   some cases they do not include the correct parameters of the source, and
   this is because the prior assumed that any spin value was possible, and this
   was not consistent with the real source distribution. However, results are
   also shown for priors that assume spins no higher than 0.7, 0.4, or even
   zero. In these cases, surely the credible regions *would* include the
   correct parameters? If those regions are not shown in the plot, then the
   meaning of the "a_{1,2} = 0", etc., marks should be made clearer.

We would always expect some sources to lie outside the 90% credible region. If
our priors perfectly match the input distribution, we should have 10% outside.
Checking this is one of the standard tests for our code, and was done in a
review prior to completing this study.

In Fig. 5, it is not just the spin range that is important, but also the mass
range, although the two are deeply linked. The simulated population of sources
have mass ratios 0.75 < q < 1, while our analysis prior allows 0.12 < q < 1.
The tail to lower values of q will pull us away from the true masses in some
cases when considering the central 90% (although this is mainly significant
only when considering the full spin range).

Upon further consideration, the typical distribution for q (skewed to high
values), makes quoting the upper 90% credible interval more appropriate.  We
have updated the figure and text to reflect this (see details below).


# Changes

Since some time has elapsed since submission, and the first results of O1 have
now been released we have updated some of the language.


## Abstract

The second sentence of the abstract has been change to:
"We investigate how well we could hope to measure properties of these binaries
using the Advanced LIGO detectors, which began operation in September 2015."

## Introduction

Changed "As we prepare to enter the advanced-detector era" to "As we enter the
advanced-detector era".

Changed "follow-up tools that are to be used for the forthcoming LIGO--Virgo
data analysis" to "follow-up tools that are used for LIGO–Virgo data analysis"
with additional reference.


## Section 3

Fig. 5: The figure now shows the projection of a rectangular
chirp-mass–mass-ratio region defined by the central 90% credible region in
chirp-mass, and the upper 90% credible region in mass-ratio.  This better
summarized the skewed nature of the mass-ratio PDFs shown in Fig. 1, and makes
it clear that the posterior PDFs have support at the simulated values.

The caption has been updated to reflect this change:
"Approximate 90% credible regions for the component-mass esti- mates of 5
selected simulations from the spinning analysis; each region is the projection
of a rectangular region of chirp-mass–mass-ratio space, bounded by the central
90% credible interval in chirp-mass and upper 90% credible interval in
mass-ratio. Circles indicate the true masses of each simulation, and bars
indicate the lower bounds of the upper 90% credible intervals (i.e. the 10th
percentiles) on mass ratio for increasingly strict prior assumptions on the
maximum spin of NSs."

and a paragraph has been added to sec. 3.3 that justifies these choices:
"Figure 5 compares cartoon 90% credible regions in component-mass space of 5
chosen simulated signals (Hannam et al. 2013; Chatziioannou et al. 2015, cf.).
As a consequence of the difficulty of estimating the narrow and nonlinearly
cor- related credible regions in m1–m2 space, we illustrate the cred- ible
regions in m1–m2 space as the projection of a rectangular region in Mc–q space.
To define the rectangular region we use 90% credible intervals of the
one-dimensional posterior PDFs of Mc and q; for Mc we use the central 90%
credi- ble interval (5th to 95th percentile), and for q the upper 90% credible
interval (10th to 100th percentile). These differing credible intervals were
chosen to better summarize the one- dimensional posterior PDFs, which are
typically normal for Mc and skewed toward high values for q (see figure 1)."


## Conclusions

Changed "assuming an aLIGO sensitivity comparable to that expected during its
first observing run" to "assuming an aLIGO sensitivity comparable to that
expected throughout its first observing run".

A statement has been added to the very end of the paper acknowledging that the
era of gravitational wave astronomy has begun with GW150914:

"Following the submission of this article, aLIGO made its first detection
(Abbott et al. 2016b). This was of a binary BH system (Abbott et al. 2016c)
rather than a BNS, but much of our understanding of the abilities of the
parameter-estimation analysis, such as the effects of mass–spin degeneracy,
trans- lates between sources. The era of GW astronomy has begun, and parameter
estimation will play a central role in the science to come."
