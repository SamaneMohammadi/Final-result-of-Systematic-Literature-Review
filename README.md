# Balancing privacy and performance in federated learning: A systematic literature review on methods and metrics

> **Authors** — Mohammadi, S.; Balador, A.; Sinaei, S.; Flammini, F.
> **Venue** — *Journal of Parallel and Distributed Computing* (2024)
> **DOI** — https://doi.org/10.1016/j.jpdc.2024.104918
> **Publisher link** — https://www.sciencedirect.com/science/article/pii/S0743731524000820

## TL;DR

A systematic literature review of privacy-preserving mechanisms in federated learning, analysing how each mechanism class affects FL performance metrics (accuracy, loss, convergence time, utility, communication, computation) and providing a selection guide tailored to application domains.

---

## A. Privacy-mechanism taxonomy

| Field | Value |
|---|---|
| Data-level | Yes — covers anonymisation, local DP on inputs, data perturbation |
| Content-level | Yes — covers gradient masking, parameter encryption, secure aggregation |
| Hybrid mechanism | Yes — explicitly reviews combinations (e.g. DP + HE, DP + SMC) |
| Main challenges | Privacy–utility trade-off; communication overhead; compute cost of cryptographic primitives at the edge |
| Main contribution | Taxonomy + impact analysis of privacy-preserving mechanisms on FL performance, plus a selection guide |
| Privacy evaluation metric | DP budget (ε, δ); attack success rate; mutual-information-based leakage |
| Other evaluation metrics | Accuracy; loss; convergence rounds; utility; communication cost; computation cost |
| Categories | Survey; Differential Privacy; Homomorphic Encryption; Secure Multi-Party Computation; Hybrid |

## B. Per-study analysis

### Proposed Model
Not applicable — this is a survey, not a system paper. The "artefact" is the taxonomy and the selection guide.

### Existing challenges addressed
- Prior surveys treat privacy mechanisms in isolation, without quantifying their effect on FL performance metrics.
- Evaluation across primary studies is fragmented and uses inconsistent metric sets, making direct comparison hard.
- Practitioners lack a structured way to choose a privacy-preserving mechanism given application constraints (e.g. low-latency edge vs. high-stakes healthcare).

### Main contributions
- A systematic review of recent privacy-preserving FL papers.
- Three-way taxonomy: data-level, content-level, and hybrid mechanisms.
- Mapping of each mechanism class to its impact on accuracy, convergence, communication, and computation.
- Application-domain-oriented selection guide for researchers and practitioners.

### Threat model
| Field | Value |
|---|---|
| Type of privacy attack | Membership inference; gradient leakage; model inversion; reconstruction; poisoning (as surveyed across primary studies) |
| Phase of attack | Training; aggregation; parameter exchange between clients and server |
| Impact of attack | Data leakage; label leakage; model extraction; integrity compromise (as surveyed) |

### Proposed method
Not applicable — review paper. The methodology is the SLR protocol (PRISMA): defined research questions, search strings, inclusion/exclusion criteria, quality assessment, and synthesis.

### Benefit of proposed method
Not applicable. Value of the work is the synthesis itself — a unified view that lets later authors compare mechanisms on the same axes.

### Experimental setup
| Field | Value |
|---|---|
| Evaluation metrics | Synthesised from primary studies: accuracy, loss, convergence rounds, communication overhead, ε, attack success rate |
| Application area | Healthcare; IoT / edge; smart cities; mobile; generic FL |
| Datasets | Various, as surveyed |
| ML / DL model | Various, as surveyed |
| Tools / frameworks | Various, as surveyed |

### Future work (per authors)
- Standardised benchmarks for privacy–performance trade-offs in FL.
- Reproducible evaluation protocols across primary studies.
- Adaptive privacy budgets that respond to client/data heterogeneity.
- Deeper study of hybrid mechanisms (DP + HE, DP + SMC) and their compounded overhead.

## C. Metadata

| Field | Value |
|---|---|
| Publication Title | Journal of Parallel and Distributed Computing |
| Publication Year | 2024 |
| Citation count (snapshot) | *fill in from Google Scholar at time of extraction* |
| J/C rank | Q1 (SJR, Computer Networks and Communications) — verify at time of extraction |
| PDF link | https://www.sciencedirect.com/science/article/pii/S0743731524000820 |

## My notes

This paper is the schema source for this whole repository. Every other paper in `papers/` is extracted using the categories defined here. When adding a primary study, refer back to Section 3 of this paper for the precise definitions of *data-level*, *content-level*, and *hybrid* mechanisms.
