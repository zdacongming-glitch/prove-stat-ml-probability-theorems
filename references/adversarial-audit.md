# Adversarial Proof Audit

Use the relevant sections throughout proof development and all sections before labeling a substantial result complete.

## Statement fidelity

- [ ] The conclusion matches the target exactly; no weaker norm, rate, probability mode, or parameter range was substituted.
- [ ] Every quantifier appears in the correct order.
- [ ] Pointwise and uniform statements are not conflated.
- [ ] Finite-sample and asymptotic conclusions are clearly separated.
- [ ] No hidden boundedness, moment, independence, realizability, compactness, or existence assumption was introduced.
- [ ] Degenerate and boundary cases are either covered or explicitly excluded by the original statement.

## Logic and dependencies

- [ ] Every lemma used is proved or precisely imported.
- [ ] Imported results are stated at the needed strength and every hypothesis is mapped to the assumption ledger.
- [ ] No step invokes the target, an equivalent statement, or a downstream consequence circularly.
- [ ] A reduction strictly advances the proof and does not merely rename the hard part.
- [ ] Local constructions satisfy the required global compatibility conditions.
- [ ] Case splits are exhaustive and induction decreases a well-founded quantity.

## Probability and measure theory

- [ ] Every random object and supremum that must be measurable is measurable or handled with an accepted outer-probability convention.
- [ ] Independence, conditional independence, exchangeability, and adaptedness survive all conditioning and data-dependent choices.
- [ ] Conditional expectations and regular conditional laws are used with compatible versions.
- [ ] Stopping times satisfy the hypotheses of optional-stopping or localization arguments.
- [ ] Expectations, derivatives, integrals, suprema, and limits are interchanged only under a valid theorem.
- [ ] Almost-sure exceptional sets are controlled jointly when a uniform statement is claimed.
- [ ] Tail integration, moment generating functions, and change-of-measure densities exist on the claimed domain.

## Statistics

- [ ] The sampling model and parameter space make the estimator or test well-defined.
- [ ] Identifiability is proved where the conclusion requires recovery of a parameter rather than an equivalence class.
- [ ] Selection, tuning, stopping, and reuse of data are accounted for.
- [ ] Risks, losses, and divergences use the same normalization throughout.
- [ ] Minimax upper and lower bounds concern the same class, metric, and probability or expectation mode.
- [ ] Asymptotic expansions control remainders in the required local or uniform regime.
- [ ] Singular information, boundary parameters, nuisance estimation, and nonunique estimators have been tested.

## Machine learning and optimization

- [ ] A generalization claim specifies whether it is for a fixed hypothesis, the algorithm output, or all hypotheses simultaneously.
- [ ] An uncountable union was not handled by a naive union bound.
- [ ] Complexity terms are computed for the actual class after localization or data dependence.
- [ ] Approximation, estimation, and optimization error are not conflated.
- [ ] The optimizer or iterate exists, and tie-breaking or algorithmic randomness is defined when relevant.
- [ ] Convexity, strong convexity, smoothness, Lipschitzness, and gradient assumptions hold on the domain where they are used.
- [ ] A nonconvex guarantee proves the stated target rather than only stationarity.
- [ ] Computational, oracle, and information-theoretic lower bounds are labeled correctly.

## Inequalities, constants, and algebra

- [ ] Inequality directions are correct, especially for Jensen, conditioning, infimum-supremum swaps, and variational bounds.
- [ ] Signs, transposes, norms, dimensions, and normalizations are consistent.
- [ ] Constants have only the dependencies allowed by the theorem.
- [ ] Confidence parameters remain in their valid range and all failure probabilities sum to the stated level.
- [ ] Logarithms, denominators, variances, and square roots are well-defined, including at boundary values.
- [ ] Critical calculations have been independently re-derived or checked symbolically.

## Limits and asymptotics

- [ ] The limiting regime specifies which quantities are fixed and which vary.
- [ ] Tightness or uniform integrability is supplied when finite-dimensional convergence or convergence in probability is insufficient.
- [ ] Pointwise bounds are not upgraded to uniform bounds without compactness, entropy, equicontinuity, or another valid mechanism.
- [ ] Remainder terms are uniform over the range claimed by the theorem.
- [ ] Orders such as $O_p$ and $o_p$ are manipulated under valid closure rules.
- [ ] Joint, iterated, and diagonal limits are not interchanged without justification.

## Edge-case attacks

Attempt at least the applicable attacks:

- sample size zero or one;
- dimension zero or one and dimension larger than sample size;
- deterministic variables and zero variance;
- two-point, atomic, highly skewed, or heavy-tailed laws;
- singular covariance or design;
- empty, singleton, or uncountable hypothesis classes;
- boundary confidence, regularization, or step-size parameters;
- nonunique optimizer, estimator, eigenvector, or conditional version;
- zero-probability conditioning events;
- dependence structures at the weakest allowed assumption.

## Computation and sources

- [ ] Numerical or symbolic checks are labeled diagnostic unless they constitute a verified exhaustive certificate.
- [ ] Floating-point evidence is not used as an exact sign or equality proof without error control.
- [ ] Citations resolve to authoritative sources and support the precise invoked statement.
- [ ] Current theorem status or novelty claims were verified when relevant and browsing was permitted.

## Closure test

Before declaring completion, answer all five questions affirmatively:

1. Does every target assumption appear in the proof or is its redundancy explained?
2. Does every proof step follow from earlier closed obligations?
3. Do the weakest allowed examples survive the argument?
4. Can the proof be reconstructed without relying on exploratory intuition or unstated folklore?
5. Would removing any unproved sentence leave a genuine gap that has already been closed elsewhere?

If any answer is negative, downgrade the result and state the first exact open obligation.
