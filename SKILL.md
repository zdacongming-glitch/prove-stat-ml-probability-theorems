---
name: prove-stat-ml-probability-theorems
description: Develop, complete, stress-test, and present rigorous proofs for theorem-level problems in probability, mathematical statistics, statistical learning theory, and machine learning theory. Use when Codex is asked to prove or disprove a theorem or conjecture, repair a proof, close a missing lemma, derive a sharp bound, audit an argument, or run a long-horizon multi-route search involving concentration, martingales, stochastic processes, empirical processes, asymptotics, optimization, generalization, information theory, or minimax theory. Also use for important or open-looking claims requiring exact assumptions, theorem-status checks, counterexample search, and adversarial proof review.
---

# Prove Statistics, Machine Learning, and Probability Theorems

## Operating contract

Seek the mathematically correct resolution, not a forced affirmative proof. Preserve the user's exact theorem and never add regularity, independence, boundedness, realizability, compactness, or asymptotic assumptions silently. If the stated claim is false, give a rigorous counterexample. If it remains unresolved, report the strongest proved result and the exact smallest open obligation; never disguise a reduction or numerical check as a proof.

Treat a proof as complete only when every dependency is either proved in the response or invoked as a precisely stated, applicable result. Track finite-sample versus asymptotic claims, pointwise versus uniform claims, and deterministic versus probabilistic quantifiers explicitly.

## Load the supporting protocol

- Read [proof-protocol.md](references/proof-protocol.md) at the start of every substantial proof or proof-repair task.
- Read [domain-routes.md](references/domain-routes.md) when selecting proof families or reopening a stalled search.
- Read [adversarial-audit.md](references/adversarial-audit.md) before accepting a candidate proof, and use its relevant sections earlier when a route contains delicate probability, asymptotic, optimization, or data-dependence steps.

For a short textbook exercise, compress the protocol but retain statement normalization, dependency checking, edge-case testing, and final audit.

## Workflow

### 1. Freeze the target contract

Rewrite the target as an exact theorem before attempting a proof. Record:

- all quantifiers, parameter ranges, spaces, sigma-fields, and conventions;
- the sampling model, independence or adaptedness relations, and sources of randomness;
- measurability, integrability, differentiability, convexity, compactness, and existence assumptions;
- whether the conclusion is deterministic, in expectation, almost sure, in probability, in distribution, or high probability;
- whether constants are universal, dimension-dependent, distribution-dependent, or allowed to change by line;
- excluded degenerate cases and required boundary cases;
- the requested deliverable: proof, disproof, proof repair, sharp rate, or status determination.

Create an assumption ledger. Mark each assumption as given, derived, standard but cited, proposed, or forbidden. Do not proceed under a proposed assumption without making the resulting claim conditional.

### 2. Check truth mode and provenance

Decide whether the task is to prove a known theorem, resolve an open-looking claim, or determine whether the statement is true. For open-looking or attribution-sensitive claims, verify current status with authoritative primary sources when browsing is available and permitted. Obey any restriction against searching for the exact problem. Do not use a prompt's instruction to "assume a proof exists" as evidence that the theorem is true.

If external results are allowed, state each one at the strength actually needed and verify that its hypotheses match the ledger. Prefer primary papers, monographs, or official documentation over summaries. Keep source verification separate from the mathematical proof.

### 3. Build proof obligations

Decompose the conclusion into a directed obligation graph. Identify the bottleneck lemmas, global compatibility conditions, and places where a theorem-strength claim may have been renamed rather than solved. Track dependencies so no route can invoke the target theorem, an equivalent formulation, or a downstream lemma circularly.

### 4. Search a diverse route portfolio

Use materially different proof mechanisms, not paraphrases of one idea. Maintain an approach registry with route family, key invariant, current obligations, evidence, failure mode, and status. Seed routes from [domain-routes.md](references/domain-routes.md), keeping several incompatible routes alive until their actual strengths and gaps are known.

If subagents are available and permitted, delegate concrete, bounded routes dynamically. Preserve independence in early rounds by withholding the favored approach and expected answer. Do not use a fixed agent count. Assign new work according to the live registry, redirecting effort from crowded families toward underexplored ones. If subagents are unavailable, perform the same independent passes sequentially and keep the registry explicit.

Require every route to return mathematical artifacts: a lemma with hypotheses, a derivation, a construction, an inequality with constants, a proof-obligation reduction, or a counterexample. Reject vague progress reports and unproved claims that a compatibility, measurability, interchange, or convergence step is routine.

### 5. Challenge and prune

Search actively for counterexamples before investing heavily in a proof. Test minimal dimensions, minimal sample sizes, degenerate distributions, boundary parameters, singular covariance, heavy tails, deterministic variables, empty classes, nonunique optimizers, and data-dependent choices.

Mark a route blocked when its missing lemma is equivalent in strength to the original theorem or lacks a new mechanism. Reopen it only after identifying a new invariant, construction, estimate, or source result. Elegant reductions do not outrank routes that actually discharge obligations.

Use computation only for conjecture generation, finite-instance testing, symbolic algebra checks, or locating counterexamples. A numerical experiment is not proof of a universal claim unless it exhausts a genuinely finite domain and the exhaustive certificate is itself verified.

### 6. Synthesize only compatible components

Combine routes only after checking that their assumptions, null sets, filtrations, constants, parameter regimes, and limiting orders agree. Re-derive the seams between imported lemmas. Promote a candidate proof only when every node in the obligation graph is discharged.

### 7. Run adversarial audit

Apply [adversarial-audit.md](references/adversarial-audit.md) to the entire proof. Independently re-derive critical identities, inequality directions, constants, and quantifier order. Attempt to break the proof with edge cases and with the weakest distributions allowed by the statement. Audit citations for exact applicability and audit every probabilistic exceptional event globally, not line by line in isolation.

If a defect appears, return the affected route to the registry and repair or replace it. Repeat until the proof survives or the exact irreducible gap is identified.

### 8. Return a calibrated result

Lead with one status label:

- **Complete proof**: every obligation is closed and the audit passes.
- **Disproof**: a valid counterexample satisfies all stated hypotheses and violates the conclusion.
- **Conditional proof**: the result follows from an additional clearly labeled assumption or external conjecture.
- **Partial result**: a rigorously proved subset remains, with the exact unresolved obligation stated.

Then present the normalized theorem, assumptions, proof or counterexample, dependency notes, and a concise audit summary. Keep exploratory dead ends out of the main proof unless they explain an essential limitation. Follow the active repository and user conventions for Markdown and mathematical delimiters in any written artifact.

## Persistence rules

Do not stop merely because the first round fails. Continue while a materially new route, counterexample test, or repair is available and within the user's time and tool constraints. Do not promise or simulate a fixed wall-clock research duration. When practical limits are reached, preserve rigor by returning the exact proof state rather than inventing closure.
