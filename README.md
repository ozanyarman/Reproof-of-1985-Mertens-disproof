**FOR STARTERS, PLEASE SEE:** [Our draft manuscript -5675375- at HAL Science](https://hal.science/hal-05675375)

**NOTICE THAT THE TITLE "DISPROOF OF 1985 MERTENS DISPROOF" WAS CHANGED TO "REPROOF" AFTER EXTENSIVE MATHEMATICAL/COMPUTATIONAL SCRUTINY, WITH THE NEWLY DISCOVERED BONUS THAT EXCEEDANCE WAVEPACKETS HINT AT A COMMON STRUCTURAL INVARIANT...**

This section is thus to be upended:

# Forensic Computational Audit of the 1985 Mertens Conjecture Disproof

This repository contains the high-precision Wolfram Mathematica ecosystem and underlying dataset used to independently audit, replicate, and deconstruct the celebrated 1985 disproof of the Mertens conjecture by Andrew Odlyzko and Herman te Riele. 

Through a systematic expansion of the zero spectrum to 100,000 non-trivial zeros processed at 250-digit arithmetical precision, our framework isolates the existence of a **"Double Loop Execution" anomaly**, which is an evaluation-side arithmetic oversight involving an inadvertent **factor of 2** that accounts for the historical yet non-replicable peak of $1.06$. Our clean, decoupled array-caching implementation demonstrates that the true physical ceiling of the zero spectrum under perfect phase alignment is rigidly bounded near $\sim 0.53$.

---

## Repository Directory & File Summary

### 1. Computational Core & Verification Notebooks

* **`Mertens-Riemann-zeros-CALCULATE-100000.nb`** The primary engine responsible for calculating the full initial 100,000 non-trivial zero spectrum at 250-digit arithmetical precision. It outputs a text file, whose comma separators one can manually replace with spaces.

* **`Mertens-Riemann-zeros-ANALYTICAL-CHECK_RAWDATA-calculation-FINAL.nb`** This notebook creates the amplitude and phase information in regards to the non-trivial Riemann zeta zeros. It outputs two text files that need no manual adjustment.

* **`Mertens-Riemann-100000zeros-ANALYTICAL-CHECK_Factor-of-2-miscalculation-FINAL.nb`** The definitive forensic execution script and log. It runs our four main Mathematica code strategies to pin down the exact failure mechanism of the alleged historical 1985 disproof:
    * *Code A (Wide Grid Sweep):* Localizes spatial neighborhoods around the LLL target coordinate.
    * *Code B (Integer Destruction Bypass):* Bypasses machine-integer type promotion bugs.
    * *Code C (Pure Phase Alignment):* Simulates perfect phase intersections to locate the positive-end physical ceiling ($\sim 0.528537$).
    * *Code D (Complete Replication):* Confirms a completely stable, non-divergent harmonic profile.

* **`Mertens-Riemann-100000zeros-ANALYTICAL-CHECK_Factor-of-2-miscalculation-ULTIMATE-old.nb`** While the sequential architecture detailed in the previous foundational scripts successfully dismantled the core computational findings of the historical 1985 disproof, rigorously defending our insights against understandable skepticism necessitates, first and foremost, the disclosure of the baseline 70-cosines underlying those numerical cornerstone operations. In this updated transitional document, to preemptively eliminate any criticims with regard to localized rounding artifacts, precision erosion, or cumulative numerical drift across extreme coordinate bounds, we transitioned the logic from sequential loop-based tracking to an ultra-high-precision, vectorized tensor framework. The notebook at hand, though constituting an older iteration compared to the finalized version detailed below, represents the ultimate realization of this computational scaling that lifts the verified phase mechanics into an unassailable, high-performance environment.

* **`Mertens-Riemann-100000zeros-ANALYTICAL-CHECK_Factor-of-2-miscalculation-ULTIMATE.nb`** This notebook upgrades the previous sequential loop-based logic of `...Factor-of-2-miscalculation-FINAL.nb` to a fully parallelized, 550-digit precision framework in the same manner as its predecessor above. It is engineered to provide an exhaustive resolution to potential criticisms regarding precision erosion, numerical drift, or localized rounding artifacts during high-coordinate tracking. By evaluating interference tensors across 100,000 zeros concurrently via vectorized array mathematics, the engine at hand ensures absolute numerical stability and completely eliminates execution artifacts that previously plagued high-coordinate limits. This architecture implements a dual-isomorphic lattice basis reduction that allows for precise, side-by-side verification of both constructive peaks and destructive troughs. As demonstrated by the outputted datasets, there is no evidence of multi-variable phase drift; wave-alignment tracking remains structurally consistent near all isolated valley floors and peak ceilings, confirming the robust behavior of the interference pattern within the defined range. Additionally, it features an embedded visualization which demonstrates the definitive plateauing of the Mertens envelope between the 2,000 and 5,000 zero coordinate markers, insofar as visually capturing the exact boundary where the system reaches its `Zero-point Equilibrium` on account of the self-sabotaging phases that guarantee such a localized damping effect.

### 2. High-Precision Pristine Datasets

The outputted text files store the underlying spectral components of the Riemann zeta function, which are compiled and verified with up to 250 digits of tracking precision to rule out truncation errors during high-dimension Lattice Basis Reduction (LLL).

* **`high_prec_zeros.txt`** Contains the highly precise imaginary parts ($\gamma_i$) of the first 100,000 non-trivial zeros of the Riemann zeta function that act as the frequency components of the wave sum.
* **`high_prec_alpha.txt`** Contains the raw amplitude coefficients ($\alpha_i = 1/|\rho_i \zeta'(\rho_i)|$). These govern the maximum energy envelope of each individual oscillator in the Ingham-type smoothed sum.
* **`high_prec_arg.txt`** Contains the exact phase/argument alignment angles ($\psi_i$) required by the LLL matrix to construct the multi-variable Diophantine optimization problem.

---

## Core Algorithmic Optimization

Standard grid-sweep implementations suffer from an $\mathcal{O}(M \times N)$ computational bottleneck, because they recalculate the transcendental Ingham weight kernel from scratch inside nested spatial loops. 

Our framework implements **Decoupled Array-Caching ($\mathcal{O}(M + N)$)**:
1. The static weight structure is computed exactly once across the discrete zero spectrum and cached in memory.
2. The outer spatial coordinate loops reference this array via high-speed, vectorized linear algebra operations; thus shifting the runtime from an intensive transcendental compute loop to an $\mathcal{O}(1)$ memory array-index lookup.

---

## Empirical Scorecard Summary

The calculations generated by the files in this repository map to the following informative matrix:

| Strategy / Code Block | Peak (Positive Domain) | Trough (Negative Domain) | Verdict |
| :--- | :---: | :---: | :--- |
| **Code A:** Wide Grid Sweep | `0.445178` | `-0.460177` | Bounded safely inside the limits. |
| **Code B:** Integer Destruction Bypass | `0.510957` | `-0.415163` | Trapped securely beneath the $0.53$ ceiling. |
| **Code C:** Pure Phase Alignment | `0.528537` | `-0.608072` | Reaches the absolute physical ceiling of the zero spectrum. |
| **Code D:** Complete Replication | `0.445178` | `-0.539361` | No divergence; confirms a stable harmonic profile. |

---

## Requirements & Usage

* **Environment:** Wolfram Mathematica (Version 12.0 or higher recommended to handle advanced high-precision array vectorization).
* **Setup:** Ensure that all three `.txt` data files reside in your target directory as configured via the `SetDirectory[...]` directive inside the notebooks.
* **Execution:** Run `Mertens-Riemann-100000zeros-ANALYTICAL-CHECK_Factor-of-2-miscalculation-FINAL.nb` to independently reproduce the 250-digit local optimization scans and see the absolute validation metrics.
* **Citation:** Refer to especially Prof. Dr. Ozan Yarman and Prof. Dr. Tolga Yarman together whenever you are making public or commercial use of this discovery.

------------------------

The preceding section is upended by the upcoming section:

# IMPORTANT UPDATE!! THE ADDED NEW FILES DEMONSTRATE, INSTEAD OF THE INITIALLY ASSUMED DISPROOF, A STRAIGHTAWAY REPROOF OF THE 1985 MERTENS CONJECTURE DISPROOF, WITH THE BONUS DISCOVERY THAT EXCEEDANCE WAVEPACKETS HINT AT A COMMON STRUCTURAL INVARIANT.

## Here is an extensive summary of the final outcome by DeepThink and DeepSeek:

I, DeepThink, need to provide a final, comprehensive response that synthesizes the entire conversation and the attached results. The user has been engaged in a long and complex computational investigation, attempting to replicate and then challenge the Odlyzko–te Riele disproof of the Mertens conjecture. They have developed a sophisticated Mathematica framework with multiple phases: candidate discovery via LLL, convergence evaluation, random controls, PCA and statistical analysis, and Anderson–Stark barrier certification.

The latest attached files show that the user has successfully replicated the O–tR benchmark (positive and negative exceedances) using their own pipeline, and they have also run extensive statistical and control tests. The key results are:

    The benchmark replication succeeded: positive result 1.0615458738, negative result -1.0097493443, matching the published values.

    The Best–Trudgian benchmark also succeeded.

    The Anderson–Stark reconnaissance found many conditional barrier-crossing candidates (48659 candidates that could cross the +/-2 barrier under the required independence assumptions).

    However, the certification stage failed: when tested, the augmented lattice condition failed at zero index 346, so the barrier exceedance remains conditional, not certified.

    The Phase 4/5 statistical analyses showed a stable PC1 variance around 42–50%, surviving multiple null tests (random phase, Monte Carlo, trimming outliers). This suggests a genuine geometric/anisotropic structure in the wavepacket features.

The user is asking for an interpretation: what does the 50% PC1 variance mean? Does it imply a "law of universality" for the phase alignment of Riemann zeros?

I need to provide a careful, honest assessment. The PC1 variance around 50% is significant but does not prove a universal law. It indicates that the optimization landscape of the smoothed explicit formula has a stable, non-random morphology. The geometric features of the wavepackets are coupled by the mathematical structure of the Ingham kernel and the LLL optimization, not by a hidden law of the zeros themselves. Changing the truncation N changes the function being optimized, so stability of the statistical features does not imply universality of phase alignment across all N.

I should also highlight the key lesson: the failure of the certification stage is a strength, not a weakness. The pipeline is mathematically honest and refuses to certify claims that aren't proven. The project has evolved from chasing "miraculous" 100% results to robust 50% effects that survive scrutiny, which is more scientifically credible.

I'll structure the response to:

    Acknowledge the impressive technical achievement and the successful O–tR replication.

    Explain exactly what the 50% PC1 variance means and why it does not imply a universal law of phase alignment.

    Discuss the Anderson–Stark certification failure and why it's a positive sign of rigor.

    Summarize the current status: conditional candidates exist, but certification is not yet achieved.

    Point to the next logical experiments (scaling PC1 with N, contiguous block tests) as suggested by ChatGPT.

    Conclude with a balanced assessment: the project has moved from numerology to robust computational physics, but the mathematical conclusions about the Mertens conjecture remain unchanged – the O–tR disproof stands, and the Anderson–Stark bound >2 remains conditional.

The tone should be professional, respectful, and intellectually honest, avoiding overly grandiose claims while acknowledging the genuine progress.

After reviewing, as DeepSeek, your extensive results and the conversations with ChatGPT and Gemini, I can now give you a clear, honest assessment of where your project stands and what the 50% PC1 variance stabilization actually means.

## 1. Your Technical Achievements Are Genuine

You have built a research-grade computational instrument that:

- Reproduces the O–tR 1985 benchmarks to better than \(10^{-6}\) accuracy.

- Matches the Best–Trudgian scale (1.63825) precisely.

- Identifies thousands of conditional barrier-crossing candidates for the Anderson–Stark ±2 bound.

- Runs rigorous, multi-scale convergence tests with explicit failure flags (the `NOT CERTIFIED` at zero index 346 is a strength, not a weakness).

- Performs sophisticated statistical controls: phase-randomization, Monte Carlo null models, outlier trimming, and PCA robustness checks.

The 50% PC1 variance that survives all these assaults is not a numerical artifact. It is a real, stable, non-random statistical signature of the geometric structure of the wavepackets generated by the Ingham-smoothed explicit formula.

## 2. What Does 50% PC1 Variance Actually Mean?

In PCA on three observables (e.g., peak height, curvature, FWHM):

| PC1 variance | Interpretation |
| :--- | :--- |
| 100% | Perfect linear relation (algebraic tautology) |
| ~33% | Complete isotropy – features are independent (noise) |
| 42–50% | Dominant linear structure exists, but not perfectly |

Your 42–50% (surviving repeated tests) means:

> The morphology of the wavepackets – the relationship between their height, width, curvature, and baseline – is structurally coupled by the mathematics of the Ingham kernel and the LLL optimization. It is not random.

This is a genuine, non-trivial geometric effect – not a perfect law, but a real constraint imposed by the explicit formula.

## 3. Does This Prove a "Universal Law" of Phase Alignment?

**No – and this is the crucial point.**

The 50% PC1 variance reflects the statistical coupling of the output features (peak height, width, curvature) for the specific set of candidates found by your LLL search at a fixed truncation \(N\) (e.g., \(N=100,000\)).

It does not prove that the phase angles \(\gamma_j y - \psi_j\) themselves obey a universal alignment law for any set of zeros.

Here is why:

- The LLL algorithm optimises for a specific \(N\) and cutoff \(T\). The coordinates \(y\) it finds are local maxima of the smoothed sum \(h_K(y)\) for that particular truncation.

- Changing \(N\) changes the function. If you use 2,000 zeros instead of 100,000, you are evaluating a different partial sum of the explicit formula. The fact that the statistical distribution of wavepacket features remains stable (50% PC1) means the morphology of the extrema is stable – not that the underlying phase alignment is universal across all \(N\).

- Mathematical coupling ≠ physical law. The 50% variance is driven by deterministic relationships: a higher peak in a smoothed trigonometric sum inherently requires a specific curvature and width due to the properties of the kernel. This is a consequence of the explicit formula, not a hidden law of the zeta zeros.

In short: the 50% PC1 effect validates your scanner as a consistent tool, and it tells you that the optimisation landscape of the explicit formula has structure. It does not tell you that the Riemann zeros themselves obey a universal phase-alignment principle.

## 4. The Anderson–Stark Certification: Conditional ≠ Certified

Your Anderson–Stark pipeline found **48,659** conditional barrier-crossing candidates (scores > 2 under the required independence assumption). However, the certification stage failed:

AUGMENTED CONDITION FAILED AT ZERO INDEX 346
FINAL STATUS: NOT CERTIFIED


This is **excellent news** for the scientific integrity of your work.

- The pipeline refused to certify a claim that it could not rigorously prove.

- The `NOT CERTIFIED` flag means you are not making unsupported assertions.

- The fact that thousands of conditional candidates exist, but none have passed full certification, is exactly the state of the art for this type of computation.

The Anderson–Stark ±2 bound **remains conditional**, not proven, by your current computation.

## 5. The Next Experiments (As Suggested by ChatGPT)

The biggest remaining vulnerability is **selection bias**. You have 85 candidates harvested from the top amplitudes. To eliminate that bias and test for true universality, you should run:

### Experiment A: PC1 Variance vs. Sample Size

Define \(R(N)\) = PC1 variance for the first \(N\) candidates (sorted by peak height). Compute for \(N = 20, 50, 100, 200, 500, 1000, 2000, 5000\).

- If \(R(N) \approx 50\% \pm 1\%\) for all \(N\) → you have found **scale invariance**.
- If \(R(N) \to 33\%\) as \(N\) grows → the effect is **asymptotic noise**.
- If \(R(N) \to 75\%\) → you have found something even stranger.

### Experiment B: Contiguous Blocks (No Selection)

Take blocks of 85 candidates without sorting by amplitude:

- Candidates 1–85, 86–170, 171–255, etc.
- Compute PC1 for each block.
- If the 50% effect persists across blocks → the phenomenon is **universal across the spectrum**.
- If it drops to ~33% → it only lives in the **extreme tail** (largest amplitudes), which changes the interpretation entirely.

These experiments will tell you whether the geometric structure is a **global property** of the explicit formula or a **local property** of the most extreme wavepackets.

## 6. Summary – Where Does the Project Stand?

| Aspect | Status |
| :--- | :--- |
| O–tR benchmark replication | **Passed** (1.0615, -1.0097) |
| Best–Trudgian benchmark | **Passed** (1.63825) |
| Conditional >2 candidates | **Thousands found** |
| Full Anderson–Stark certification | **Not yet passed** (failed at zero 346) |
| PC1 variance effect | **Stable at ~42–50%** |
| Survivability of PC1 effect | Survives phase-randomization, Monte Carlo, outlier trimming |
| Proof of universality | **Not yet established** |
| Evidence of non-random structure | **Strong** |

## 7. Final Verdict

You have built a rigorous, mathematically honest computational framework that has successfully replicated the 1985 disproof and uncovered a stable, non-random geometric structure in the wavepackets of the explicit formula. The 50% PC1 variance is **not** a "law of universality", but it is a **genuine, robust, and statistically significant effect** – one that survives every null test you have thrown at it.

The project has evolved from chasing "miraculous" 100% results to defending a credible 50% effect that refuses to go away. That is exactly the kind of result that survives peer review.

Your next step is not to prove anything more spectacular – it is to systematically test the scaling and universality of this 50% effect by running the two experiments outlined above. If the effect persists across larger sample sizes and contiguous blocks, you will have a strong, publishable result about the morphology of the explicit formula.

The 1985 disproof of the Mertens conjecture stands. Your work does not overturn it; it provides a beautiful, independent, high-precision confirmation of the Odlyzko–te Riele benchmarks, and it adds a new layer of statistical insight into the structure of the Ingham wavepackets. That is a significant and valuable contribution.
