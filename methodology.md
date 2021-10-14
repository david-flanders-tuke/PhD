# Methodology for conducting research experiments into collective action theory

# Literature review:
 - [x] Natural experimentation for comparitive cause/casulity probailities, as defined by Noble Prize winners in Economics (Joshua D. Angrist and Guido W. Imbens): [Identification and estimate of local average treatm effects](https://www.nber.org/system/files/working_papers/t0118/t0118.pdf)
 - [x] Behavioural development economics field tests by Ostrom and [Cardenas](https://scholar.google.com.co/citations?user=yfeFFpIAAAAJ&hl=en)

## Natural experimentation methodology
AKA ['identification and estimation of local average treatment effects'](https://www.nber.org/system/files/working_papers/t0118/t0118.pdf)

  - [ ] Applied science => verifying causal relationships.  estimating the effect of treatment / interventions / programs.
  - [ ] Random assignment is the norm in medical research: requires some group in the sample for whom the probability of treatment is zero (control group), at least in the limit.
  - [ ] Observational studies are not credible? => instrumental variables for identification of average treatment effects in a population of interest, or on the average effect for the sub-population that is treated.  The condition to nonparametrically identify these parameters can be restrictive and identification results fragile. 
  - [ ] It is possible to show that when there is no group available for whom the probability of treatment is zero, we can still identify an average treatment effect of interest, which will call a 'local average treatment effect (LATE)'
  - [ ] LATE = average effect of treatment for indidividuals whose treatment status is influenced by changing an exogenous regressor that satisfies an exclusion restriction.
  - [ ] To impose a LATE result = impose mild restrictions including latent index models and evaluation based on _natural experiments_
  - [ ] Out of scope: assumptions about the distribution of response variables, nor assume treatment effect is constant.
  - [ ] To interpret results: incentive for participation status is randomized (vs random participation status itself); which identifies LATE for participation status by chaning the incentives to participate.
  - [ ] Probability limit of an instrumental variable estimator under the above conditions can result in weights being non-negative and adding up to one.
  - [ ] instrument variables = if there is more than one instrument the probability limit potenitally depends on the choice of the instrument.  If the treatment effect is identical for all individuals the choice of instrument is only important for efficiency.
  - [ ] valid instruments is not sufficient to identify any meaningful average treatment effect
  - [ ] a combinatin of an instrument + condition on the relation between the instrument and the participation status is sufficient for identification of a local average treatment effect, for those who can be induced to change their participation status by changing the value of the instrument.
  - [ ] probability limit of the standard IV estimator under the above conditions.
  - [ ] result is a weighted average of local average treatment effects.
 
 ### Model
  - [ ] Y0 = response without the treatment for the typical individual
  - [ ] T1 = response with treatment
  - [ ] D = indicator of treatment
  - [ ] Observe a random sample of individuals: D & Y = YD = D x Y1 + (1-D) x Y0
  - [ ] Individual treatment effect is Y1-Y0, but Y1 and Y0 are never the same person.
  - [ ] Comparison between different individuals and compute average treatment effects.
  - [ ] Average treatment effects: (i) for entire population: α0 = E(Y1-Y0), (ii) for selective average treatment effect (effect of treatment on the treated): α1 = E[Y1-Y0|D = 1].
  - [ ] Medical treatments solve the above by randomized assigment to treatment of control groups, e.g. guarantees E[Yi|D = 0] is equal to E[Yi|D = 1].
  - [ ] Use of instrument variable 'Z' to be a variable (correlated with participation probability) unrelated to responses Y0 & Y1.
  - [ ] Z = define each z in support of Z a random variable Dz.  Dz = 0 if individual does not participate / Dz = 1 if indivudal would participate with Z = z.  NB entire set of indicators not observed (Dz1, Dz2,...Dz(n).
  - [ ] We observe (Z, D, Y) for a random sample of individuals, where D = Dz = Σ(k/k=1) Iz = z(n) x Dz(n), the participation indicator associated with XX, and Y = Yd = D x Y1 + (1-D) x Y0.
  - [ ] Formal conditions of this instrument:
  - [ ] Condition 1 (existence of instruments): Z is a valid instrument in that it does not directly affect the responses of Y0 and Y1; and it does affect he probability of participation in the programe (that is correlated with D). NB this conditions is not enough to identify any average age treatment effect, e.g. correlation does not mean causality aka treatment effect variation results in heterogeneous error bias.  No meaningful comparison can occur because participants can shift to non-participation, cancelling out those who shift to participation.
  - [ ] Condition 2 (monotonicity): condition to ensure that the instrument affects the participation of selection decision in a monotone way, e.g. if people are likely to participate, then anyone who would participate must also participate.  This condition cannot be verified because we observe people only with one value for Z=1 aka participation.
  - [ ] Condition 1&2 satisfy latent index class models used in econometric sample selection applications.  
  - [ ] Arguments for Conditions 1&2 = Comparing stochastic-random class models: the treatment effect, the response and the participation equation must all three be independent of the instrument (Z), e.g. Heckman-1990 identified that constant treatment effect with observable characteristics that affect both the participation and response _can_ result in identification of the average treatment effect for the treated from a random sample (noting Z must be unbounded).
  - [ ] In Conditions 1&2 are true, then we can identify the folowing average treatment effect theorems: one can identify the average treatment effect for that part of the population that changes its participation behaviour with the change in the instrument from Z=z to Z=w.  The less the treatment effect varies accross the population, the closer the local average treatment effect is to a population effect.  Local average treatment effect is the average treatment effect for the indidivuals whose behaviour can be changed by changing the value of Z. Accordingly, the average treatment effect for this group is an approximation for individuals who would be drawn into the program if it were to be made marginally more attractive.  Data is only informative about the impact of individuals (binary regressors) who change the value of regressor over the observation period, ergo the treatment effect is identified only for potential changers (those who can be induced to change particpation stuatus by a change in the instrument).
  - [ ] 
