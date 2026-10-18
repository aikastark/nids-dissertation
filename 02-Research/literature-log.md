# Literature log

Full reference list maintained in Zotero, exported as `My Library.bib`
(see `02-Research\My Library`). Papers sorted into 4 collections.

## Dataset paper
- **Sharafaldin, Lashkari & Ghorbani** — Toward Generating a New Intrusion Detection Dataset and Intrusion Traffic Characterization (ICISSP 2018). THE original CICIDS2017 dataset paper — must be cited whenever the dataset is used.

## Constrained-attacks (core group)
- **Catillo et al.** — Towards realistic problem-space adversarial attacks against ML in NIDS (ANCHOR). Perturbs DoS traffic via a traffic control utility, not by editing features directly. Shows transferability across 4 ML models.
- **Verkerken et al.** — "What is the Problem Space?" Defining Host-space Adversarial Perturbations against NIDS (ANCHOR). Defines host-space perturbations — what an attacker controlling only their own host can actually do. Systematic review of 316 papers finds most prior work manipulates already-collected datapoints.
- **elShehaby & Matrawy** — Evasion Adversarial Attacks Remain Impractical Against ML-based NIDS. Explains the "Inverse Feature-Mapping Problem" — why feature-space changes are hard to translate into real packets.
- **Yao et al.** — Modeling Realistic Adversarial Traffic Against DL-Based IDS in Industrial IoT. Packet-level attack respecting domain constraints, methodologically close to my constraint table.
- **Espindola et al.** — Understanding the Adversary: A Survey of Adversarial ML in NIDS. Adopts a "cautious realism boundary" — explicitly distinguishes feature-space success from problem-space feasibility. Directly supports my thesis framing.
- **McCarthy et al.** — Functionality-Preserving Adversarial ML for Robust Classification in Cybersecurity and Intrusion Detection: A Survey. Surveys attacks that must preserve the attack's functionality under perturbation — exactly the constraint my project applies.
- **Apruzzese et al.** — Modeling Realistic Adversarial Attacks against NIDS. Formalises the feature-space vs problem-space distinction and the dimensions of a realistic threat model (attacker knowledge, capability, goal, strategy).
- **Venturi, Stabili & Marchetti** — Problem Space Structural Adversarial Attacks for NIDS Based on GNN. Formalises problem-space constraints for structural/graph-based NIDS attacks (only feasible graph operations, e.g. edge addition).

## Feature-space attacks (contrast group)
- **Alatawi** — Adversarial Evasion in ML-Based NIDS: Systematic Review (186 studies, 2018-2026). Introduces a "perturbation-realism taxonomy"; argues most reported evasion success is feature-space sensitivity, not real risk. Directly supports my thesis.
- **Ennaji et al.** — Adversarial Challenges in NIDS: Research Insights and Future Prospects. General survey of NIDS vulnerability to evasion attacks.
- **Raj et al.** — Categorical Robustness Assessment for ML-based NIDS. RF has 99.98% clean accuracy but drops 73 points under FGSM/PGD attack on ACI-IoT-2023. Useful for baseline model choice.
- **Sivkov et al.** — Adversarial Robustness of ML-Based IDS. CatBoost accuracy drops from 94.86% (clean) to 3.53% under CW attack on CSE-CIC-IDS2018. Strong example of unconstrained attack severity.
- **Ke He, Kim & Asghar** — Adversarial Machine Learning for NIDS: A Comprehensive Survey (IEEE COMST 2023). Widely-cited foundational survey covering attack and defence taxonomy for ML-based NIDS.
- **Goodfellow, Shlens & Szegedy** — Explaining and Harnessing Adversarial Examples. Foundational paper introducing FGSM — the basis for many feature-space attacks used in the NIDS literature. Background/methodology reference, not NIDS-specific.
- **Kurakin, Goodfellow & Bengio** — Adversarial Machine Learning at Scale. Extends FGSM with an iterative method (BIM); another foundational technique reference.

## Defences
- **Bunzel & Siwakoti** — Detecting Adversarial Evasion Attacks Against Autoencoder-Based NIDS. Detection-based defence (not adversarial training), near-perfect results on IoT traffic.
- **Roken et al.** — Hybrid Adversarial Retraining Approach. Retraining on CICIDS2017+CSE-CIC-IDS2018 combined, +7% accuracy improvement.
- **Yin et al.** — DSAAT: Dual-Space Adaptive Adversarial Training. Adversarial training across both feature- and problem-space with explicit domain constraints, 91% adversarial accuracy on CICIDS2017.
- **Vitorino et al.** — An Adversarial Robustness Benchmark for Enterprise NIDS. Benchmarks RF/XGB/LGBM/EBM with regular vs adversarial training on CICIDS2017/NewCICIDS/HIKARI — concrete numbers for comparison in my evaluation stage.
- **Tafreshian & Zhang** — A Defensive Framework Against Adversarial Attacks on ML-Based NIDS. Combines adversarial training, dataset balancing, feature engineering, and ensembling; +35% detection accuracy, -12.5% false positives on NSL-KDD/UNSW-NB15.

## Baselines
- **Rahman & Zaidi** — Network Traffic Classification using ML: Review of DT, RF, SVM on CIC-IDS2017. Basis for choosing RF as a baseline model.

Target: 15+ papers (currently 22, see Zotero library and references above).