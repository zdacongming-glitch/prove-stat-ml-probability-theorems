# Domain Route Catalog

Use this catalog to seed genuinely different proof routes. Select only routes compatible with the target contract; do not apply a fashionable technique without checking its hypotheses.

## Probability theory

### Measure and representation

- Reduce to simple functions, finite sigma-fields, canonical spaces, or monotone classes.
- Use truncation, approximation, tightness, regularization, or disintegration.
- Compare laws through couplings, stochastic orders, transport, or common-randomness representations.
- Use characteristic functions, Laplace transforms, probability-generating functions, or moment problems when transforms determine the law.

### Martingales and dependence

- Construct a filtration and expose a Doob martingale or martingale difference sequence.
- Use stopping, localization, optional sampling, predictable variation, or exponential supermartingales.
- Apply blocking, mixing, dependency graphs, exchangeable pairs, or decoupling when independence is absent.
- Audit adaptedness, integrability, uniform integrability, stopping-time hypotheses, and version choices.

### Concentration and tails

- Try exponential moments, bounded differences, Bernstein-type variance control, self-normalization, entropy methods, or functional inequalities.
- Use symmetrization, contraction, chaining, or maximal inequalities for indexed processes.
- Explore truncation plus tail integration for heavy-tailed variables.
- For lower bounds or sharpness, use two-point laws, rare events, moderate deviations, or change of measure.

### Processes and limits

- Use finite-dimensional convergence plus tightness for process convergence.
- Try generators, semigroups, resolvents, spectral methods, coupling, regeneration, or Lyapunov drift for Markov processes.
- Use subadditivity, ergodic arguments, renewal structure, or invariance principles for long-time behavior.
- Check topology, separability, modification, and interchange of limits carefully.

## Mathematical statistics

### Likelihood and estimation

- Use sufficiency, completeness, ancillarity, conditioning, Rao-Blackwellization, or exponential-family structure.
- Analyze likelihood, score, observed or expected information, estimating equations, or convex loss geometry.
- For M-estimators, separate identification, stochastic equicontinuity, consistency, local expansion, and limiting distribution.
- For U-statistics or symmetric statistics, try Hoeffding decomposition and projection arguments.

### Decision theory and minimax analysis

- Use Bayes risk, least-favorable priors, complete-class reasoning, convex duality, or testing reductions.
- Seed lower bounds with two-point testing, Le Cam methods, Fano inequalities, Assouad constructions, packing, or constrained risk inequalities.
- Match upper and lower bounds in the same loss, parameter class, and probability or expectation mode.
- Verify that prior support, separation, divergence bounds, and metric entropy calculations match the target.

### Asymptotic and semiparametric routes

- Try local asymptotic normality, contiguity, delta methods, influence functions, tangent spaces, or Hájek projections.
- Separate fixed-dimensional asymptotics from growing-dimensional or nonstandard regimes.
- Check differentiability notions, nuisance rates, remainder control, and uniformity over local alternatives.
- Do not infer uniform convergence from pointwise asymptotics without an additional argument.

### Robust and high-dimensional routes

- Use truncation, median-of-means, influence-function control, small-ball methods, restricted eigenvalues, decomposability, or sparsity geometry.
- Track contamination model, tail class, dimension, sparsity, confidence level, and tuning-parameter dependence.
- Test singular designs, adversarial contamination, and nonidentifiability at the parameter-class boundary.

## Statistical learning theory and machine learning

### Generalization

- Try uniform convergence through VC dimension, growth functions, covering numbers, Rademacher or Gaussian complexity, symmetrization, and chaining.
- Try algorithm-dependent routes through stability, compression, margins, localization, information, or PAC-Bayes bounds.
- Use online-to-batch conversion when regret control is more natural than direct empirical-process analysis.
- State whether a bound holds for a fixed predictor, the algorithm output, or uniformly over a class.

### Optimization and algorithms

- Use convexity, strong convexity, smoothness, co-coercivity, monotonicity, duality, mirror descent geometry, or proximal structure.
- For nonconvex problems, identify the promised target: stationary point, local optimum, global optimum, escape from saddles, or function-value gap.
- Use potential functions, estimate sequences, contraction, spectral analysis, or Lyapunov functions for deterministic iterations.
- For stochastic algorithms, combine conditional descent with martingale concentration and explicit control of bias and variance.

### Representation and model structure

- Use kernel, spectral, low-rank, sparsity, invariance, margin, mean-field, or neural tangent representations only in their valid regime.
- Separate approximation, estimation, and optimization error.
- Track realizability, identifiability, overparameterization, implicit bias, initialization, and algorithmic randomness explicitly.

### Lower bounds and impossibility

- Reduce learning to testing, communication, information, query complexity, or adversarial online decisions.
- Construct packings that respect the model class and loss.
- Check whether the lower bound is computational, statistical, oracle-based, or information-theoretic; do not conflate them.

## Cross-domain transformations

Try these when direct routes stall:

- primal-dual reformulation or convex conjugacy;
- variational characterization of a probability metric, divergence, eigenvalue, or risk;
- randomization, conditioning, symmetrization, or exchangeability;
- localization by scale, peeling, truncation, or stopping;
- interpolation between endpoint inequalities;
- induction on dimension, sample size, support size, or structural complexity;
- tensorization, product decomposition, or leave-one-out identities;
- reduction from estimation to testing or from batch learning to online learning;
- invariance, sufficient statistics, canonical coordinates, or quotienting symmetries.

## Route selection questions

Before committing to a route, ask:

1. Which target assumption powers this mechanism?
2. What is the route's first nonstandard lemma?
3. Could that lemma be equivalent to the target?
4. What minimal example would falsify it?
5. Does the route preserve uniformity, constants, and data dependence?
6. What concrete artifact should the next search round return?

Favor routes with a falsifiable next lemma and a well-founded decrease in complexity. Keep at least one counterexample route alive until the theorem is secure.
