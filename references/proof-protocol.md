# Long-Horizon Proof Protocol

Use this protocol to manage theorem-level work without losing assumptions, duplicating approaches, or accepting a theorem-strength gap as progress.

## 1. Target contract

Create a compact target contract with these fields:

| Field | Required content |
| --- | --- |
| Claim | Exact conclusion with all quantifiers |
| Objects | Spaces, random variables, distributions, algorithms, estimators, and parameters |
| Hypotheses | Every structural, regularity, tail, dependence, and existence condition |
| Probability mode | Deterministic, expectation, almost sure, in probability, in distribution, or high probability |
| Uniformity | Pointwise or uniform; identify the indexed class and parameter set |
| Regime | Finite sample, nonasymptotic, asymptotic, high dimensional, or distribution free |
| Constants | Universal or dependent; record allowed dependencies |
| Conventions | Null events, empty sets, ties, infinities, versions, and boundary values |
| Deliverable | Proof, disproof, repair, sharp rate, lower bound, or theorem-status determination |

Normalize ambiguous expressions before reasoning. For example, distinguish a statement for each fixed $h$ from a statement holding simultaneously for all $h \in \mathcal H$, and distinguish convergence for each fixed dimension from a joint limit in which dimension grows with sample size.

## 2. Live research state

Maintain five small ledgers during a substantial task.

### Assumption ledger

For each assumption, record its status:

- **Given**: present in the target statement.
- **Derived**: proved from given assumptions.
- **Imported**: supplied by a named result whose hypotheses have been checked.
- **Proposed**: useful but not authorized; any proof using it is conditional.
- **Forbidden**: explicitly excluded by the target.

### Obligation graph

Represent the proof as dependencies between concrete propositions. A node is closed only by a proof or a verified imported theorem. Flag nodes that are equivalent to the target, stronger than the target, or global compatibility claims hidden behind local constructions.

### Approach registry

Use one row per mathematical family, not per wording variant.

| Route | Mechanism or invariant | Current obligation | Concrete artifact | Failure mode | Status |
| --- | --- | --- | --- | --- | --- |
| A | Distinct proof mechanism | Lemma or construction needed next | Equation, lemma, example, or certificate | Exact reason it may fail | Exploring, promising, blocked, refuted, or merged |

### Dependency ledger

List every external result with its exact statement, source, and hypothesis mapping. Detect circular use, especially when an imported lemma is an equivalent formulation of the target.

### Counterexample and risk log

Record tested edge cases and unresolved risks. Include degeneracy, measurability, constants, dependence, optimizer existence, exceptional events, and limit interchanges.

## 3. Search rounds

### Seed a genuinely diverse portfolio

Start with routes that differ in mechanism: direct inequalities, structural decompositions, duality, coupling, martingales, change of measure, empirical processes, optimization geometry, information-theoretic reductions, minimax arguments, transform methods, and counterexample construction. Use [domain-routes.md](domain-routes.md) to specialize this list.

Do not tell every independent pass which route currently looks best. Early convergence often amplifies the same hidden gap. Let routes mature until they expose a lemma, construction, estimate, or counterexample that can be compared objectively.

### Allocate dynamically

If multiple agents are permitted, use the live registry rather than a fixed assignment. Give each agent a bounded mathematical objective and require a concrete return artifact. Useful roles include:

- route explorer for one mechanism;
- counterexample hunter for a proposed lemma;
- assumption auditor for a candidate chain;
- constant checker for a sharp inequality;
- literature verifier for one named theorem;
- synthesis checker for compatibility between two routes.

Redirect new work when many agents converge on the same family. Reopen a blocked route only when a new invariant, representation, construction, or source result changes its prospects.

### Require useful artifacts

Accept:

- a fully stated and proved lemma;
- a derivation with every inequality justified;
- an explicit construction with verified properties;
- a counterexample satisfying all target assumptions;
- a reduction that strictly lowers a well-founded complexity measure;
- a computation that isolates a conjecture or falsifies a finite subclaim.

Reject:

- an unproved global compatibility assertion;
- a route ending at an equivalent or stronger conjecture;
- a special case presented as the general theorem;
- numerical agreement presented as universal proof;
- a citation without an exact hypothesis match;
- a status report without a mathematical artifact.

## 4. Counterexample-first discipline

Before deep proof search, attack the statement at its weakest allowed points:

- smallest sample size, dimension, class size, or time horizon;
- deterministic, two-point, symmetric, or highly skewed distributions;
- zero variance, singular covariance, atoms, and heavy tails;
- boundary parameter values and empty or singleton classes;
- dependent variables that satisfy only the stated dependence conditions;
- data-dependent hypotheses or stopping times;
- nonexistence or nonuniqueness of estimators and optimizers;
- failure of measurability for suprema or selections.

When a claim survives, use the tests to identify why each hypothesis is needed. When it fails, minimize the counterexample and verify every target hypothesis explicitly.

## 5. Proof synthesis

Merge components only after checking:

1. The output of each lemma matches the next lemma's input exactly.
2. All constants have legal dependencies and remain valid in the target regime.
3. Exceptional events can be intersected or union-bounded at the stated confidence.
4. Versions of conditional expectations, regular conditional laws, or stochastic processes are compatible.
5. Filtrations and independence claims survive conditioning and data-dependent choices.
6. Limit operations occur in a justified order.
7. A local construction produces the required global object.

Rewrite the final proof as a clean chain from the target assumptions. Do not use the exploratory registry as a substitute for a proof.

## 6. Literature and computation

Use literature to verify theorem status, exact named results, constants, and hypotheses. Prefer primary sources. If the user forbids searching for the exact problem, respect that boundary and search only allowed background. Never suppress known status or claim novelty without evidence.

Use symbolic or numerical tools to test identities, optimize candidate constants, enumerate finite cases, or find counterexamples. Record precision, parameter ranges, and whether the result is diagnostic or certifying. Universal or infinite-domain claims still require analytic proof unless a formal exhaustive certificate covers the entire domain.

## 7. Exit conditions

Return a complete proof only after the obligation graph is closed and the adversarial audit passes. Return a disproof only after the counterexample is checked against every hypothesis. Otherwise return the strongest proved statement together with:

- the exact first open obligation;
- why existing routes do not close it;
- whether it is equivalent to the target or genuinely smaller;
- what new mechanism or information would reopen progress.

Never convert lack of progress into a fabricated lemma. Never treat a time budget as mathematical evidence.
