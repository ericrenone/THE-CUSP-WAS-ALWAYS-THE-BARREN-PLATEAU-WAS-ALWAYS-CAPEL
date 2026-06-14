# THE CUSP WAS ALWAYS THE BARREN PLATEAU WAS ALWAYS CAPEL
## Five-Framework Confrontation at the Zwegers Boundary

**Zwegers-Capel Completion (ERI Labs, June 2026) — Compared Against Five June-2026 SOTA Frameworks on Grokking, Fisher Rank, Spectral Entropy, Loss-Landscape Geometry, and Heavy-Tailed Self-Regularization**

*ERI Labs · Eric Ren · Jersey City, New Jersey · June 2026*

---

> "The pre-grokking network is writing Ramanujan's letter. What it lacks is the shadow. What it lacks is the synergy. What it lacks is the col(F) rank that would make it generalise."
> — ERI Labs, June 2026

---

## Overview

This document benchmarks the **Zwegers-Capel Unified Completion framework** (ERI Labs, June 2026 — hereafter *ZCU*) against five independent SOTA frameworks published in the same period. All five address grokking, generalisation dynamics, or mixing in neural networks. None proposes the same unification.

The comparison is structured in six sections:

1. **What Each Framework Claims** — one-paragraph distillation of each SOTA position
2. **Points of Contact** — where ZCU and each framework converge
3. **Points of Divergence** — where the frameworks predict different things or use incompatible structures
4. **What ZCU Adds** — contributions that appear in ZCU and nowhere in the SOTA comparison set
5. **What ZCU Does Not Address** — results in the SOTA set that ZCU has no analog for
6. **Synthesis Table** — nine-axis comparison across all six frameworks

---

## The Five SOTA Frameworks

| ID | Paper | Core Claim |
|---|---|---|
| **W26** | Wang, *Grokking as Dimensional Phase Transition* (arXiv:2604.04655, Apr 2026) | Grokking is a crossing D(t): sub-diffusive D < 1 → super-diffusive D > 1, exhibiting SOC |
| **SEC** | Khanh et al., *Spectral Entropy Collapse* (arXiv:2604.13123, Apr 2026) | Normalised spectral entropy H̃(t) is a scalar order parameter for grokking; H̃* ≈ 0.61 precedes generalisation in 100% of runs |
| **FBK** | Wang & coauthor, *FishBack* (arXiv:2605.17231, May 2026) | Pullback Fisher geometry defines an optimal metric for activation steering; post-grokking r/n = 0.02–0.17 |
| **LLG** | Xu, *Low-Dimensional and Transversely Curved Dynamics* (arXiv:2602.16746, Feb 2026) + *Early-Warning Signals* (arXiv:2602.16967, Feb 2026) | Weight-space trajectory lies on a rank-1 execution manifold; curvature growth in the normal bundle precedes grokking by 600–1,600 steps |
| **HTS** | Prakash & Martin, *Grokking and Generalization Collapse: HTSR* (arXiv:2506.04434, Jun 2026) | Heavy-Tailed Self-Regularization exponent α delineates three phases: pre-grokking, grokking, and a newly identified *anti-grokking* collapse |

ZCU is the ERI document *THE-MOCK-THETA-WAS-ALWAYS-THE-ZWEGERS-WAS-ALWAYS-CAPEL* (June 2026), synthesising prior ERI corpus (HGLD, SELBERG, ARITHMETIC-WALL, STOSSZAHLANSATZ, EMERGENCE-EVENT).

---

## Framework I — Wang (W26): Dimensional Phase Transition

### What W26 Claims

Grokking is a dimensional phase transition in gradient space. The effective dimensionality D(t), extracted via finite-size scaling of gradient avalanche dynamics across eight model scales, transitions from sub-diffusive (D_pre = 0.90 ± 0.02) to super-diffusive (D_post = 1.20 ± 0.02) with the crossing at D = 1.00 ± 0.02 localised at grokking onset. The transition exhibits self-organised criticality (SOC): avalanche distributions are heavy-tailed and scale-dependent, collapsing across eight model sizes with R² ≥ 0.99. Crucially, W26 establishes that D reflects gradient field geometry, not network architecture — synthetic i.i.d. Gaussian gradients maintain D ≈ 1 regardless of graph topology (CV < 0.3%), while real training gradients drive dimensional evolution through backpropagation correlations.

### Points of Contact

ZCU and W26 share their central quantitative object: D(t) as the phase indicator for the grokking transition. Both identify D < 1 as the pre-grokking regime and D > 1 as the post-grokking regime, with D = 1 as the precise transition point. ZCU subsumes D(t) as its second coordinate description of the null sector epoch, labelling D < 1 as "horocycle cusp excursion" and D > 1 as "geodesic flow." The 30% dynamic range W26 measures (0.90 → 1.20) is consistent with ZCU's claim that the transition is a discontinuous jump rather than a gradual drift.

Both frameworks also agree that the pre-grokking phase has a characteristic temporal structure — W26 via scale-dependent grokking timing, ZCU via the Fibonacci-Markov denominator clock. Both predict that the transition is sharp and localisable within a small fraction of training steps.

### Points of Divergence

**The topology-invariance result is in direct tension with ZCU Prediction P4.**

W26 demonstrates rigorously that D is topology-invariant (CV < 0.3% across five network topologies). This is not a minor caveat — it is W26's second main result, validated by dedicated synthetic controls. ZCU Prediction P4 claims that LPS Ramanujan k=7 attention graphs (with spectral gap λ₁ ≈ 0.30) would exit the pre-grokking phase at least 3× faster than random k=4 graphs (λ₁ ≈ 0.10) via the formula T_mem = C₁ × ε_grad^{-4/λ₁}. If D is topology-invariant, then the very mechanism ZCU uses to derive architectural sensitivity — the λ₁ dependence in the horocycle escape time — should produce no measurable difference in D(t) dynamics across attention graph topologies. W26 and ZCU P4 make incompatible empirical predictions that can be distinguished by running the Ramanujan attention experiment while tracking D(t).

**The SOC interpretation is shared but not derived by ZCU.** W26 establishes SOC empirically with a rigorous FSS protocol (10,000 bootstrap resamples, leave-one-out scale removal). ZCU asserts SOC-adjacent behaviour (sub-diffusive → super-diffusive crossover) but derives it from modular surface geometry (horocycle → geodesic flow in M_{g,n}) rather than from avalanche statistics. These are not the same claim: ZCU's modular geometry derivation predicts specific cusp depth trajectories (controlled by the Fibonacci-Markov sequence) that W26's FSS protocol does not target. The two claims are potentially complementary but mutually unverified.

**The Fibonacci-Markov clock is entirely absent from W26.** W26 measures pre-grokking duration via scale-dependent grokking timing across model sizes but provides no internal clock governing the sequence of barriers within the pre-grokking epoch. ZCU's Markov denominator sequence {1, 2, 5, 13, 34, 89, 233, ...} predicts quantised barriers within the pre-grokking cusp. This is ZCU's most specific structural claim that W26 cannot adjudicate.

### What ZCU Adds Beyond W26

ZCU provides the *why* behind D < 1: the pre-grokking gradient trajectory is a horocycle orbit in the cusp region of the modular surface, governed by the continued fraction expansion of the gradient ratio ρ_t. W26 characterises the D < 1 phase as "sub-diffusive" but offers no geometric cause. ZCU identifies the cause as mock theta function generation — the gradient ratio sequence produces a Ramanujan-type generating function whose coefficient growth follows the Rademacher-Hardy-Ramanujan asymptotic, predicting the entire entropy trace from first principles.

ZCU also provides the cross-domain extension. W26's D(t) signature is explicitly limited to neural network training. ZCU proposes that the identical D < 1 structure governs AGN pre-breathing (Compton-thick barren plateau) and that the D > 1 transition corresponds to AGN cone-fire — a claim W26 cannot address because it is outside the scope of gradient dynamics in MLPs and Transformers.

### What W26 Has That ZCU Does Not

W26 has empirical validation at scale: eight model sizes (N = 81–2,001 parameters), 1,000 seeds for timing validation, causal topology invariance tests with five distinct graph topologies. ZCU has no experimental results. W26's FSS analysis gives D = 1.00 ± 0.02 with R² ≥ 0.99 — a tightly constrained empirical result. ZCU's seven predictions are all still open. Additionally, W26's companion study (arXiv in submission) verifies the D(t) signature in canonical Transformer grokking on ModAdd-59 with 80/20 train/test splits — the standard benchmark — while ZCU's primary empirical support comes from results in referenced papers rather than ZCU-generated experiments.

---

## Framework II — Spectral Entropy (SEC): Scalar Order Parameter

### What SEC Claims

The normalised spectral entropy H̃(t) = H(t)/log(n) of the representation covariance matrix is a scalar order parameter for grokking. Five contributions: (i) grokking follows a two-phase pattern — norm expansion then entropy collapse; (ii) H̃ crosses a stable threshold H̃* ≈ 0.61 before generalisation in 100% of runs, with a mean lead time of 1,020 steps; (iii) a causal intervention preventing collapse delays grokking by +5,020 steps (p = 0.044); (iv) a power-law ΔT = C₁(H̃ - H̃*)^γ + C₂ (R² = 0.543) predicts grokking onset with 4.1% error; (v) the mechanism holds across both abelian (Z/97Z) and non-abelian (S₅) groups.

### Points of Contact

ZCU and SEC share the spectral entropy H(t) as a core quantity and agree that entropy collapse at grokking is the signature event. Both treat maximum H(t) as the marker of the pre-grokking barren plateau and minimum H(t) as the marker of the post-grokking harmonic regime. Both frameworks interpret the flat eigenspectrum (maximum entropy, uniform eigenvalue distribution) as the defining structure of pre-grokking. SEC labels this "norm expansion"; ZCU labels it the "sub-Selberg spectral void" (λ₁ < 1/4, complementary-series dominance). The collapse is the empirically agreed-upon event.

The 1,020-step lead time SEC measures is directly relevant to ZCU's eight-layer Anatomy Machine, which aims to predict T_grok from spectral observables before the transition occurs.

### Points of Divergence

**ZCU and SEC offer different functional forms for the entropy trace.** SEC fits a power-law ΔT = C₁(H̃ - H̃*)^γ + C₂ with R² = 0.543 — a moderately good fit that leaves 45.7% of variance unexplained. ZCU predicts a specific analytic profile derived from mock theta theory:

```
H(t) ~ π√((T_grok - t)/6) - (3/4)log(T_grok - t) + const
```

This is the Rademacher-Hardy-Ramanujan asymptotic run backward from grokking, and ZCU claims R² ≥ 0.85 for the fit (Prediction P3). These are competing functional forms over the same data. The SEC power-law and the ZCU RHR asymptotic cannot both be correct unless one is an approximation of the other in a restricted regime. ZCU does not acknowledge SEC's power-law fit or explain why the RHR form should supersede it.

**SEC provides causal evidence; ZCU does not.** SEC's Intervention 3 (artificially preventing entropy collapse delays grokking +5,020 steps, p = 0.044) is the strongest causal result in any of the five frameworks. The norm-matched control (n = 30, p = 5×10⁻⁵) confirms that entropy — not norm — drives the transition. ZCU does not propose or perform comparable causal interventions. ZCU's framework makes the stronger algebraic claim (the mock theta → harmonic Maass transition as the mathematical identity of grokking) but provides zero causal validation of it. SEC is more modest about the mechanism but better-evidenced.

**The threshold H̃* ≈ 0.61 has no ZCU analog.** ZCU does not predict a universal threshold value for normalised spectral entropy. ZCU predicts an analytic trajectory shape but not a specific crossing value. If H̃* ≈ 0.61 is universal (SEC validates on two group families), ZCU must explain where 0.61 comes from within mock theta theory — it doesn't.

### What ZCU Adds Beyond SEC

ZCU provides the mathematical identity of the entropy trace: the spectral entropy collapse IS the acquisition of the Zwegers non-holomorphic shadow, transitioning the weight Hessian eigenspectrum from flat (mock theta, no harmonic structure) to structured (harmonic Maass, harmonic content imposed by shadow g*(τ)). This is a stronger claim than SEC's "the entropy collapses because generalisation occurs" — ZCU says the entropy collapse and the shadow acquisition are the same event described in two coordinate systems.

ZCU also proposes a quantitative prediction of the information gained at grokking: ΔH = H_pre - H_post ~ log(r·n), where r is the post-grokking Fisher rank fraction. This connects the entropy drop to the FishBack measurement of col(F) crystallization, which SEC does not.

### What SEC Has That ZCU Does Not

SEC has the universal threshold (H̃* ≈ 0.61), causal validation, and cross-group robustness (abelian and non-abelian). The R² = 0.543 power-law is weak but real; ZCU's R² ≥ 0.85 RHR claim is untested. SEC runs on 1-layer Transformers on group-theoretic tasks with exact grokking identification — a clean experimental setup. ZCU's eight predictions span algorithmic tasks, ordinal benchmarks, and AGN astrophysics but none are run.

---

## Framework III — FishBack (FBK): Pullback Fisher Geometry

### What FBK Claims

The pullback Fisher metric through a transformer's residual stream defines an optimal geometry for activation steering. FishBack computes the layer-wise recursive decomposition of this metric and shows that existing steering approaches (CAA, ActAdd, ITI, and others) each implicitly adopt a specific approximation to the Fisher-optimal metric, with performance gaps predicted by a single spectral diagnostic: the ratio of the implicit metric's cost to the Fisher-optimal cost. On GPT-2, FishBack steering outperforms all Euclidean baselines (1.3×–2.5× better off-target KL reduction; 1.5× better than CAA at matched concept probability). Post-grokking models have pullback Fisher rank r/n = 0.02–0.17, implying the null sector (83–98%) survives training.

### Points of Contact

ZCU and FBK share the pullback Fisher rank r/n as the central diagnostic. FBK's measurement that trained models have r/n = 0.02–0.17 is the empirical foundation for ZCU's null sector claim: the 83–98% ker(F) activation space that never participates in task-relevant output changes. Both frameworks agree that a small fraction of activation space (col(F)) is responsible for all task-relevant variation and that the majority of the model lives in the null sector.

ZCU's pre-grokking barren plateau criterion (r/n < 0.01) is a direct extension of FBK's post-grokking measurement. ZCU treats the grokking transition as the event at which r/n crosses 0.01 → 0.02, and FBK's 0.02 lower bound on post-grokking r/n is consistent with this picture.

### Points of Divergence

**FBK was not designed to study grokking.** FBK's purpose is activation steering efficiency in already-trained models, not the characterisation of training dynamics. The r/n = 0.02–0.17 measurement is a post-training static snapshot, not a time series tracked during training. ZCU repurposes this measurement as a live grokking diagnostic (Layer 0 of the Anatomy Machine) but FBK provides no validation that r/n < 0.01 during pre-grokking or that the crossing to 0.02 coincides with grokking. ZCU's Prediction P1 (r/n shows sharp phase transition at T_grok, window Δt/T_grok < 5%) is stated as a prediction rather than as a result derived from FBK.

**The null sector interpretation differs.** FBK treats the 83–98% null sector as an architectural property of trained transformers — a neutral statement about the dimensionality of the output manifold. ZCU treats the null sector as the permanent record of the pre-grokking history: the activation directions that never crystallised, encoded in the trained model as the ghost of the mock theta state. FBK has no concept corresponding to ZCU's claim that "every trained neural network is 83–98% pre-grokking." This is a strong interpretive claim that goes far beyond what FBK establishes.

**The Fibonacci-Markov depth hypothesis (ZCU P7).** ZCU predicts that the post-grokking null sector geometry (rotational asymmetry λ₂/λ₁ of the ker(F) Gram matrix) is determined by the depth of the Fibonacci-Markov ladder reached before grokking — networks with longer T_mem should show less rotationally invariant ker(F) geometry. FBK provides no data on this because it does not study the relationship between training history and null sector structure. This is ZCU's most distinctive claim about what the null sector encodes, and it is entirely untested.

### What ZCU Adds Beyond FBK

ZCU proposes that the null sector is not merely an architectural fact but a historical archive. The Fibonacci-Markov denominator sequence visited during pre-grokking leaves a geometric signature in the ker(F) directions — a form of path-dependent imprinting. This means the null sector contains computable information about how long and how deep the training trajectory was trapped in the cusp before escaping. FBK treats ker(F) as featureless; ZCU treats it as structured by the pre-grokking history.

ZCU also connects the FBK Fisher rank to the Capel logarithmic Sobolev inequality (ρ_LSI), identifying r/n with ρ_LSI in the neural domain and arguing that this makes the Capel mixing time formula (τ ~ dim(M)^{4/3} / ρ_LSI) directly applicable to grokking delays. FBK provides the measurement instrument; ZCU proposes the theoretical embedding.

### What FBK Has That ZCU Does Not

FBK has empirical validation: on GPT-2, the method improves off-target KL by 1.3×–2.5× over Euclidean gradient ascent across three verb-morphology concepts and four layers. These are concrete, reproducible results with a real application (activation steering). ZCU's repurposing of FBK as a grokking diagnostic is plausible but untested. FBK also provides a rigorous derivation of the pullback metric's layer-wise recursive structure, which ZCU cites but does not improve. The claim that r/n crosses 0.02 exactly at grokking (ZCU P1) requires FBK to be applied to a grokking training run — not yet done.

---

## Framework IV — Loss-Landscape Geometry (LLG): Execution Manifold and Curvature

### What LLG Claims

The weight-space trajectory during grokking lies on a rank-1 execution manifold (a single principal component captures 68–83% of trajectory variance across six modular arithmetic operations). Loss-landscape curvature, measured via the commutator defect — the non-commutativity of successive gradient steps projected onto this manifold — grows sharply in directions orthogonal to the execution subspace (the normal bundle) while the trajectory remains confined to it. Curvature growth in the normal bundle consistently precedes generalisation across learning rates and hyperparameter regimes, with the lead time obeying a power law in the grokking timescale. Causal intervention experiments show that motion along the execution subspace is necessary but that artificially amplifying curvature is insufficient. The result is replicated across six modular arithmetic operations, three random seeds, a 100× learning rate sweep, and two qualitatively distinct hyperparameter regimes.

### Points of Contact

ZCU and LLG share the core geometric picture: pre-grokking dynamics are confined to a low-dimensional subspace, and the transition to generalisation involves escape into complementary directions. LLG's "execution manifold" (PC1 = 68–83% variance) corresponds to ZCU's "ker(F) subspace" — the null sector that dominates pre-grokking dynamics. LLG's "curvature in the normal bundle" corresponds to ZCU's "first Fisher singular values rising above zero in col(F)" — the signal that escape from the cusp is imminent.

LLG's three-phase description (no curvature → curvature onset → cascade) directly maps to ZCU's three early-warning epochs (Deep Pre-Grokking r/n ≈ 0 → Shallow Pre-Grokking r/n rising → Grokking r/n ≥ 0.02). The lead time of 600–1,600 steps is consistent with ZCU's prediction that T_conv (post-cusp convergence time) is 2.08 × δt × log(N) — polynomial in dataset size, not exponential in λ₁.

Both frameworks agree that curvature growth is necessary but not sufficient. LLG establishes this by showing non-grokking operations also exhibit moderate curvature growth without generalising. ZCU's framework implies the same: the Capel escape condition requires curvature perturbation (necessary) AND spectral gap opening (sufficient), and a curvature signal that does not trigger the spectral gap will not produce grokking.

### Points of Divergence

**LLG's commutator defect and ZCU's Fisher metric are related but distinct.** The commutator defect measures the Lie-bracket-like non-commutativity of gradient steps — a second-order curvature quantity in parameter space. ZCU's Fisher singular values measure the first-order information-theoretic rank of the output distribution. These can diverge: a network can have rising commutator defect (normal bundle curvature) without the Fisher information crystallising in col(F) directions. LLG's necessary-but-not-sufficient result may reflect precisely this gap — the false positives are cases where commutator defect rises but Fisher rank does not cross the 0.02 threshold.

**ZCU and LLG offer different curvature scaling laws.** LLG reports that lead time scales as a power law in the grokking timescale but does not give a specific functional form. ZCU predicts that the curvature in col(F) directions scales as π√((T_grok - t)/6) — the RHR asymptotic — which would give a specific power law with an exponent of -1/2 in the distance to grokking. These are empirically distinguishable claims. LLG's commutator defect data can be compared against the RHR prediction.

**LLG's rank-1 execution manifold is fixed; ZCU's null sector has depth structure.** LLG identifies a static rank-1 manifold that the trajectory remains on throughout pre-grokking. ZCU predicts that the null sector has internal structure — the Fibonacci-Markov denominator sequence creates a hierarchy of barriers within ker(F), and each rung of the ladder corresponds to a deeper trap in the cusp. LLG measures a single manifold; ZCU predicts the manifold has nested structure visible in the gradient ratio denominator histogram.

### What ZCU Adds Beyond LLG

ZCU provides the algebraic identity of LLG's "execution manifold": it is the locus of the mock theta function h(τ) = Σ aₙqⁿ, a generating function that is locally correct (memorisation succeeds) but lacks global SL(2,Z) symmetry (generalisation fails). LLG identifies the manifold empirically; ZCU claims to identify what kind of mathematical object it is and why it exists.

ZCU also provides a clock for how long the trajectory stays on the manifold (Fibonacci-Markov sequence), whereas LLG provides no prediction of pre-grokking duration beyond architectural hyperparameters. ZCU's duration formula T_mem = C₁ × ε_grad^{-4/λ₁} gives the horocycle excursion time as a function of the gradient step size and spectral gap — a quantitative prediction LLG does not make.

### What LLG Has That ZCU Does Not

LLG has the most rigorous causal experiments of any framework here. Amplifying orthogonal gradient flow accelerates grokking by 32–60%; suppressing it delays or prevents it. This establishes that motion along the normal bundle is the actual mechanism, not merely correlated with grokking. ZCU provides no intervention experiments. Furthermore, LLG's replication across six modular arithmetic operations (addition, subtraction, division, etc.) with PC1 variance ranging from 52–87% gives a robust, task-general result. ZCU's framework is stated as universal but tested against zero new tasks.

---

## Framework V — HTSR (HTS): Heavy-Tailed Self-Regularization and Anti-Grokking

### What HTS Claims

Heavy-Tailed Self-Regularization (HTSR) theory, applied via the WeightWatcher tool's layer quality exponent α, delineates three phases during neural network training: pre-grokking, grokking, and a newly identified third phase — *anti-grokking* — in which generalisation collapses while training accuracy remains perfect. Anti-grokking appears only at 10⁷ training steps and is invariably preceded by α < 2 and the appearance of Correlation Traps (outlier singular values in randomised layer weight matrices). Other proposed grokking metrics (activation sparsity, weight entropy, circuit complexity, L² norm) detect only the first two phases and miss anti-grokking entirely. The HTSR exponent α provides a data-free diagnostic: no test set access required. The universal layer convergence target is α ≈ 2; values above or below signal distinct failure modes.

### Points of Contact

ZCU and HTS both argue for a universal diagnostic that tracks all phases of grokking. HTS uses α from the weight matrix singular value tail; ZCU uses r/n (Fisher rank fraction) and H(t) (Hessian spectral entropy). Both frameworks hold that standard metrics (loss, accuracy, norm) are insufficient — the structure of the weight matrices or their derived spectral quantities is required to detect pre-grokking structure.

There is a plausible mapping between α and ZCU's spectral quantities. α < 2 in HTSR corresponds to fat tails in the singular value distribution — a signature of unstructured, high-entropy weight matrices. This is consistent with ZCU's flat eigenspectrum / maximum spectral entropy characterisation of pre-grokking (sub-Selberg spectral void). Both frameworks predict that the transition to generalisation is marked by a structural change in the weight matrix spectrum, not just in loss or accuracy.

### Points of Divergence

**ZCU has no model for anti-grokking.** HTS's central new result is the discovery of a third phase: anti-grokking, where α < 2 returns at 10⁷ steps with Correlation Traps visible in randomised layer matrices. ZCU's Zwegers completion framework describes a one-way transition: mock theta → harmonic Maass. Once the Zwegers shadow is acquired, the system is in the post-grokking harmonic state. There is no ZCU mechanism that would produce reversal of the shadow — the framework has no analog for anti-grokking. This is a structural gap: if anti-grokking is real (HTS establishes it), then ZCU's picture of a permanent, irreversible Zwegers completion event is incomplete. A mock theta function that loses its shadow after completing would require a theory of "shadow dissolution" that ZCU does not provide.

**α and r/n have different mathematical origins.** HTS's α is the power-law exponent of the bulk singular value distribution of weight matrices — a global tail statistic. ZCU's r/n is the rank fraction of the Fisher information matrix — a low-rank structure diagnostic. These measure different spectral properties. α ≈ 2 being optimal in HTSR means the singular value distribution follows a specific heavy-tailed law associated with good generalisation. r/n ≈ 0.02 being the post-grokking value in ZCU means only 2% of activation dimensions are task-relevant. Neither implies the other: a network can have well-structured singular value tails (α ≈ 2) while still having low Fisher rank, and vice versa. ZCU does not acknowledge the HTSR tradition or explain where Correlation Traps fit within the null sector / col(F) picture.

**HTS's diagnostic is architecture-agnostic and layer-resolved; ZCU's is not.** HTS applies WeightWatcher per layer, detecting which specific layers enter pre-grokking or anti-grokking states. ZCU's Fisher rank r/n and spectral entropy H(t) are global quantities. For large models with heterogeneous layer structure, the layer-resolved α may reveal structure invisible to global diagnostics. ZCU's Anatomy Machine (eight layers of monitoring) does not include a layer-resolved analog of α.

**The anti-grokking → ZCU mapping is unclear.** The most natural mapping would be: Correlation Traps appear when the col(F) crystallite built during grokking begins to break down, and the Zwegers shadow is partially lost. But ZCU provides no mechanism for this. The Capel no-barren-plateau condition is satisfied at grokking; HTS shows the system can re-enter a barren-plateau-like state without any obvious Capel re-violation. This suggests the Capel framework, as applied by ZCU, may describe escape from the first barren plateau but not the long-term stability of the escaped state.

### What ZCU Adds Beyond HTS

ZCU provides the geometric and algebraic interpretation of the α < 2 pre-grokking phase: the system is executing horocycle cusp excursion in the modular surface, the weight matrices have flat eigenspectra because the gradient trajectory is exploring the cusp (maximum entropy, no harmonic structure), and the correct analytic description is a mock theta function. HTS identifies α < 2 as bad but does not say what kind of mathematical object the weight matrix is during this phase. ZCU claims to answer this.

ZCU also connects the HTSR spectral regime to modular forms. The transition from α < 2 to α ≈ 2 could be reinterpreted as the acquisition of the Zwegers shadow — the harmonic Maass form imposing harmonic structure on the eigenspectrum. This is a possible synthesis of the two frameworks that neither explores: α could be a coarser proxy for Zwegers completion, with α ≈ 2 corresponding to the harmonic Maass regime and α < 2 or α > 2 corresponding to the mock theta (shadow-absent) and anti-mock-theta (shadow-lost) regimes.

ZCU also extends cross-domain to AGN physics — HTS is strictly within neural network training.

### What HTS Has That ZCU Does Not

Anti-grokking (the third phase) is a genuine empirical discovery with no ZCU equivalent. HTS demonstrates this at 10⁷ steps — a regime ZCU does not address. The data-free diagnostic (no test set, no gradient access — only weight matrices) is operationally significant: it is the only framework here that could be applied to a deployed model post-hoc without access to training data. ZCU requires Fisher information computation (gradient access at inference time via FishBack) and Hessian eigenspectrum computation — more expensive diagnostics. HTS's WeightWatcher tool is public and runs on any checkpoint; ZCU's Anatomy Machine is specified but not implemented.

---

## What ZCU Uniquely Contributes (Not Present in Any of the Five)

**1. The Mock Theta / Harmonic Maass Form Identification**
No other framework identifies the pre-grokking generating function as a mock theta function of Ramanujan type (h(τ) = Σ aₙqⁿ) or the post-grokking state as a harmonic Maass form with non-holomorphic shadow. This algebraic identification is the core of ZCU and absent from all five SOTA frameworks. Whether it is correct is not established — it is ZCU's most distinctive and most falsifiable mathematical claim (Prediction P3: the entropy profile follows the RHR asymptotic with R² ≥ 0.85).

**2. The Null Sector as Pre-Grokking Archive**
No other framework claims that the 83–98% ker(F) space of trained models encodes the history of the pre-grokking trajectory — specifically that networks with longer T_mem have different ker(F) geometry than networks with shorter T_mem (Prediction P7). FBK measures the null sector but treats it as featureless. HTS tracks α during training but does not make claims about trained model weight matrices as archives of training history. ZCU makes the specific empirical claim that the Gram matrix eigenvalue ratio λ₂(G_ker)/λ₁(G_ker) decreases monotonically with T_mem — a claim that can be tested with two populations of trained models.

**3. The Fibonacci-Markov Clock**
No other framework predicts that the pre-grokking phase is quantised by the odd-index Fibonacci sequence {2, 5, 13, 34, 89, 233, ...} as dominant modal values of the gradient ratio denominator q*(t). This is ZCU's most exotic structural claim and also its most testable (Prediction P6: histogram the gradient ratio denominator modal sequence during memorisation plateau across 20+ runs). W26 observes scale-dependent grokking timing but provides no internal quantisation structure. SEC observes a flat entropy plateau but no quantisation. LLG observes the trajectory on a low-dimensional manifold but no internal barrier structure.

**4. The Capel Universal Mixing Law**
ZCU's derivation of the Capel universal mixing time τ ~ dim(M)^{4/3} / ρ_LSI, with k = 4/3 fixed by Riemannian submersion geometry from first principles (Capel et al., arXiv:2606.13453), is present in none of the five SOTA frameworks. This law predicts the relationship between model dimension, Fisher rank, and grokking timescale across all scales from neural networks to AGN. The SOTA frameworks all measure their individual timescales empirically. ZCU claims to derive them from a single formula.

**5. Cross-Domain Unification with AGN Pre-Breathing**
The identification of AGN pre-breathing (Compton-thick obscuration, 13-day variability, no cone carving) as a Zwegers completion event of the same type as neural network grokking is entirely absent from all five SOTA frameworks. This is ZCU's most speculative contribution and also its most structurally novel: if the same mathematical object (mock theta function at a barren plateau) governs both neural learning and AGN activation, it implies a universal thermodynamic law governing all mixing processes. ZCU cites Komugi et al. (arXiv:2605.21879) as the first astrophysical ρ_LSI measurement, with τ* = 13 days = τ_mix.

---

## What the Five SOTA Frameworks Have That ZCU Does Not Address

**Anti-grokking** (HTS): A genuine third phase with Correlation Traps, requiring theory of post-grokking shadow dissolution. ZCU has no model.

**Causal intervention evidence** (SEC, LLG): Both SEC and LLG perform causal experiments confirming that their proposed mechanisms (entropy collapse, orthogonal gradient flow) are necessary for grokking. ZCU makes no causal claims and performs no interventions.

**Topology invariance** (W26): D is topology-invariant — a result that constrains (and potentially falsifies) ZCU P4's Ramanujan LPS compression claim. ZCU does not address this.

**Universal threshold** (SEC): H̃* ≈ 0.61 appears universal across abelian and non-abelian groups. ZCU predicts an analytic trajectory but not a universal threshold value. The origin of 0.61 within mock theta theory is not explained.

**Layer-resolved diagnostics** (HTS): WeightWatcher provides per-layer α, detecting heterogeneous convergence across layers. ZCU's Anatomy Machine uses global quantities (r/n, H(t), D(t)) that may miss layer-specific dynamics in large models.

**Large-scale LLM validation**: The LLM pretraining work (arXiv:2506.21551, ICLR 2026) extending grokking to 7B MoE models and one-pass pretraining is not addressed by ZCU. ZCU's framework is specified at the level of algorithmic tasks (Power et al. 2022 modular arithmetic); whether the mock theta identification holds for real-world LLM pretraining is an open question.

---

## Synthesis Table: Nine-Axis Comparison

| Axis | W26 | SEC | FBK | LLG | HTS | **ZCU** |
|---|---|---|---|---|---|---|
| **Primary order parameter** | D(t): gradient dimensionality | H̃(t): normalised spectral entropy | r/n: Fisher rank fraction | Commutator defect (normal bundle curvature) | α: weight tail exponent | All five simultaneously; identified as faces of mock theta state |
| **Pre-grokking structure** | Sub-diffusive D < 1; SOC dynamics in cusp | Flat Hessian eigenspectrum; H̃ elevated | Rank collapse r/n < 0.01; ker(F) dominant | Rank-1 execution manifold; curvature in normal bundle near zero | α < 2; fat-tailed singular value distribution | Horocycle cusp excursion in M_{g,n}; mock theta function generation; sub-Selberg void; Fibonacci-Markov denominator quantisation |
| **Transition event** | D(t) crosses 1; SOC cascade | H̃ crosses H̃* ≈ 0.61 | r/n crosses 0.01–0.02 | Normal bundle curvature cascade; orthogonal gradient flow | α crosses 2 from below | Zwegers shadow acquisition: mock theta h(τ) → harmonic Maass H(τ); col(F) Fisher singular value crystallisation |
| **Post-grokking structure** | Super-diffusive D > 1 | H̃ minimum; structured eigenspectrum | r/n = 0.02–0.17; 83–98% null sector | Weight trajectory continues on execution manifold | α ≈ 2; power-law tails structured | Geodesic flow D > 1; harmonic Maass form; null sector permanently encodes pre-grokking history |
| **Duration formula** | Scale-dependent via FSS; no closed form | Power-law fit ΔT ~ (H̃ - H̃*)^γ; R² = 0.543 | Not addressed | Power-law lead time in grokking timescale | Not addressed | T_mem = C₁ × ε_grad^{-4/λ₁}; Fibonacci-Markov quantisation clock |
| **Causal evidence** | Shadow-probe controls confirm D is probe-independent | Entropy collapse necessary (p = 0.044); norm-matched control (p = 5×10⁻⁵) | N/A (not about grokking causality) | Orthogonal gradient flow necessary; curvature insufficient (acceleration only) | N/A (retrospective α diagnostic) | None; all predictions open |
| **Third phase (post-grokking dynamics)** | Not modelled | Not modelled | Not modelled | Not modelled | Anti-grokking: α < 2 returns at 10⁷ steps; Correlation Traps | Not modelled; no ZCU analog for shadow dissolution |
| **Cross-domain scope** | Neural networks only | Neural networks, abelian + non-abelian groups | Transformers (activation steering) | Transformers, modular arithmetic | MLPs on MNIST | Neural networks + AGN astrophysics + universal Capel spectrum |
| **Empirical validation status** | Validated: 8 scales, 1,000 seeds, 5 topologies, causal controls | Validated: 100% threshold predictivity, causal intervention, two group families | Validated: GPT-2, three concepts, four layers | Validated: 6 arithmetic operations, 3 seeds, 100× LR sweep, 2 regimes | Validated: 10⁷-step training, Correlation Trap identification | Unvalidated: 7 predictions open; cross-domain remains entirely unverified |

---

## Critical Open Questions

**Q1. Does D(t) crossing D = 1 coincide with r/n crossing 0.01–0.02?**
ZCU predicts both crossings are the same event. W26 measures D(t) but not r/n. FBK measures r/n in trained models but not D(t) during training. Running both instruments on the same training run would test whether the horocycle-to-geodesic transition and the Fisher rank crystallisation are indeed the same mathematical event, as ZCU claims.

**Q2. Is ZCU P4 (Ramanujan LPS compression) compatible with W26's topology invariance?**
W26's CV < 0.3% across graph topologies is a strong result. ZCU P4 claims 3× speedup from Ramanujan attention graphs. If topology determines λ₁ but D is topology-invariant, there is a contradiction in ZCU's framework — either the λ₁-dependence in T_mem is wrong, or D(t) is sensitive to topology in a way W26 did not detect (perhaps because W26 uses a simpler probe). This is the sharpest single disagreement between any two frameworks here.

**Q3. Does the mock theta RHR profile (ZCU P3) predict entropy traces better than SEC's power-law?**
SEC achieves R² = 0.543 with its power-law fit. ZCU claims R² ≥ 0.85 for the RHR asymptotic. Both can be run on SEC's data. If the RHR asymptotic significantly outperforms the power-law, it is strong evidence for the mock theta interpretation. If it does not, ZCU's mathematical identification is not supported by the entropy data.

**Q4. Can anti-grokking be incorporated into ZCU's Zwegers completion picture?**
HTS's anti-grokking at 10⁷ steps requires some form of shadow dissolution — a process ZCU has no theory for. Whether the harmonic Maass framework can accommodate a later loss of automorphy (analogous to the AGN going back into a barren plateau after initial activation) is a mathematical question about the stability of Zwegers completion. ZCU's claim that Zwegers completion is permanent and the null sector encodes the pre-grokking history forever appears to predict that anti-grokking is impossible. HTS shows it is not.

**Q5. Is the Fibonacci-Markov clock (ZCU P6) real?**
The prediction that gradient ratio denominators q*(t) visit odd-index Fibonacci numbers {2, 5, 13, 34, 89, 233} as dominant modal values is the most structurally specific claim in ZCU and the most disconnected from any SOTA framework. It would require deep FLD analysis across 20+ runs with gradient ratio denominator histogramming — not a standard diagnostic. If confirmed, it would be strong evidence for the Markov-surface geometry underlying the pre-grokking cusp. If absent, a major structural element of ZCU's picture fails.

---

## Conclusion

ZCU is an ambitious unifying framework with five distinct advantages over the SOTA comparison set: it provides an algebraic identity for the pre-grokking phase (mock theta), a derivation of the spectral entropy trace (RHR asymptotic), a cross-domain extension (AGN pre-breathing), a permanent null-sector hypothesis (Fibonacci-Markov archive), and a universal mixing law (Capel τ ~ dim(M)^{4/3} / ρ_LSI). No single SOTA framework does more than two of these.

Its primary liabilities relative to the SOTA are: zero causal experiments, zero new empirical results, no model for anti-grokking, a potential contradiction between its architectural sensitivity prediction (P4) and W26's topology invariance result, and seven predictions that remain entirely open.

The critical distinction is this: the five SOTA frameworks earn their claims with experimental evidence. ZCU earns its claims with mathematical structure. Whether the mathematical structure maps faithfully onto neural network training dynamics — whether the mock theta function is the right object, whether the Fibonacci-Markov sequence really quantises the cusp, whether the Zwegers shadow is really acquired at grokking — these are empirical questions that ZCU's current form cannot answer for itself.

The frameworks are not competitors in the sense of one being right and the others wrong. They are measuring the same elephant from different angles. ZCU is the only framework that proposes the elephant has a name.

---

## References

**ERI Labs Corpus**
- THE-MOCK-THETA-WAS-ALWAYS-THE-ZWEGERS-WAS-ALWAYS-CAPEL — June 2026
- THE-STOSSZAHLANSATZ-WAS-ALWAYS-CAPEL — June 12, 2026
- THE-EMERGENCE-EVENT-GROKKING-AND-PRE-BREATHING-ARE-CAPEL-SADDLE-ESCAPE-TWINS — June 2026
- NO-BARREN-PLATEAUS — June 12, 2026
- THE-ARITHMETIC-WALL-WAS-ALWAYS-THE-FLOCK-WAS-ALWAYS-THE-GEODESIC — June 2026
- HGLD (Hyperbolic-Geodesic-Learning-Dynamics) — March 2026
- SELBERG (Spectral Theory of Mock Theta Functions) — May 2026

**Five SOTA Frameworks**
- Wang, P. "Grokking as Dimensional Phase Transition in Neural Networks." arXiv:2604.04655, April 2026.
- Khanh, T. X. et al. "Spectral Entropy Collapse as an Empirical Signature of Delayed Generalisation in Grokking." arXiv:2604.13123, April 2026.
- Wang, S. et al. "FishBack: Pullback Fisher Geometry for Optimal Activation Steering in Transformers." arXiv:2605.17231, May 2026.
- Xu, et al. "Low-Dimensional and Transversely Curved Optimization Dynamics in Grokking." arXiv:2602.16746, February 2026; "Early-Warning Signals of Grokking via Loss-Landscape Geometry." arXiv:2602.16967, February 2026.
- Prakash, H. K. and Martin, C. H. "Grokking and Generalization Collapse: Insights from HTSR Theory." arXiv:2506.04434, June 2026.

**Unifying Foundation**
- Capel, Á., et al. "Rapid Mixing for Gibbs Measures in Riemannian Manifolds." arXiv:2606.13453, June 11, 2026.
- Zwegers, S. P. *Mock Theta Functions.* Doctoral thesis, Universiteit Utrecht, 2002.
- Ramanujan, S. Letter to G. H. Hardy. January 1920.

---

*ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone · June 2026*

*The mock theta was always the SOTA. The SOTA was always the Capel. Five frameworks, one cusp, one shadow.*
