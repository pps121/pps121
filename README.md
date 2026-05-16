<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=220&section=header&text=Partha%20Pratim%20Saha&fontSize=44&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Geometric%20Interpretability%20%C2%B7%20AI%20Safety%20%C2%B7%20Mechanistic%20Interpretability%20%C2%B7%20Alignment%20Geometry&descAlignY=58&descSize=15&descColor=c8b6ff" width="100%"/>

[![NeurIPS](https://img.shields.io/badge/NeurIPS%202025-Workshop%20Author-7c3aed?style=for-the-badge&logo=academia&logoColor=white)](https://arxiv.org/pdf/2509.00849)
[![SpringerNature](https://img.shields.io/badge/SpringerNature-ICOMP'24-0a7cc1?style=for-the-badge&logo=springer&logoColor=white)](https://link.springer.com/chapter/10.1007/978-3-031-72171-7_3)
[![Email](https://img.shields.io/badge/Email-technical.partha%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:technical.partha@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-partha121-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/partha121)
[![Portfolio](https://img.shields.io/badge/Portfolio-pps121.github.io-7c3aed?style=for-the-badge&logo=github-pages&logoColor=white)](https://pps121.github.io)
[![Scholar](https://img.shields.io/badge/Google%20Scholar-Publications-4285F4?style=for-the-badge&logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?user=M0nZ5pEAAAAJ&hl=en)
[![ORCID](https://img.shields.io/badge/ORCID-0000--0001--8140--7272-A6CE39?style=for-the-badge&logo=orcid&logoColor=white)](https://orcid.org/0000-0001-8140-7272)

</div>

---

<table>
<tr>
<td width="62%">

> **"AI systems must be aligned not only behaviourally but *geometrically* — with transparent, auditable internal representations that can be verified, not just tested."**

I build **differential-geometric and information-geometric frameworks** to answer one question: *What actually changes inside a model when we align it?*

I discovered that DPO/RLHF alignment creates geometrically localised **"brake layers"** — specific transformer depths where torsion is selectively suppressed. These are detectable via forward passes alone, reproducible across architectures, and directly patchable. Published at **NeurIPS 2025** and **SpringerNature**.

**Background:** Self-driven independent researcher. Lecturer in CS at Nalhati Government Polytechnic (West Bengal). All research built before/after office hours — no lab, no GPU cluster, no supervisor. 12 years of industry experience across Infosys, IIT Kanpur, J&J R&D, Wipro.

**Four active research threads:**
- 🔬 **GRAFT** — Geometric alignment audit toolkit (post-hoc, gradient-free)
- 🧬 **MENTIS** — Multi-scale latent torsion · NeurIPS 2026 submission
- 🌱 **AgriTalk** — Calibrated NLU for agricultural robotics
- 🌐 **nDNA / Semantic Helix** — Cultural epistemic inheritance in merged LLMs

</td>
<td width="38%" align="center">

```
┌──────────────────────────────────┐
│  GRAFT · Key Results             │
├──────────────────────────────────┤
│  T2 vs CKA discriminability:     │
│  ██████████████████  8×          │
│                                  │
│  Normative torsion amplification:│
│  ██████████████████████  20–46×  │
│                                  │
│  Safe-prompt paradox p-value:    │
│  p < 10⁻³³  (OLMo · n=20,439)   │
│                                  │
│  AUC T2  : 0.89 [0.85–0.93]     │
│  AUC CKA : 0.61                  │
│                                  │
│  DPO subspace: 2–3 dims          │
│  RLHF subspace: 4–5 dims         │
│                                  │
│  "Alignment writes geometry."    │
└──────────────────────────────────┘
```

</td>
</tr>
</table>

---

## 📄 Publications

| Year | Venue | Title | Links |
|------|-------|-------|-------|
| 2025 | **NeurIPS 2025 Workshop** | Prompting Away Stereotypes? Evaluating Bias in Text-to-Image Models for Occupations | [arXiv](https://arxiv.org/pdf/2509.00849) |
| 2025 | **Journal** | Enhancing Human Empathy in Conversations Using Transformer-Based Models | [DOI](https://doi.org/10.5281/zenodo.15126395) |
| 2024 | **SpringerNature ICOMP'24** | Collaborative Federated Learning Cloud Based System | [Paper](https://link.springer.com/chapter/10.1007/978-3-031-72171-7_3) |
| 2026 | **[Under Review — NeurIPS 2026]** | MENTIS: Multi-Scale Latent Torsion in Language Models | [Repo](https://github.com/pps121/torsional-belief-vector-field) |
| 2026 | **[Preprint]** | GRAFT: Geometric Representations of Alignment's Fingerprint in Transformer Belief Trajectories | [Repo](https://github.com/pps121/graft-belief-geometry) |

---

### 1 · GRAFT — Geometric Representations of Alignment's Fingerprint in Transformer Belief Trajectories
> **Mechanistic Interpretability** | [`graft-belief-geometry`](https://github.com/pps121/graft-belief-geometry)

GRAFT is a **post-hoc, gradient-free mechanistic audit toolkit** that characterises preference alignment via three torsion probes (𝒯, T1, T2) and an ERA depth profiler — requiring only forward passes through publicly available checkpoints.

| Result | Value |
|--------|-------|
| T2 concept discriminability | **CV = 0.64** vs CKA = 0.08 → **8× better** |
| T2 classification AUC | **0.89** [0.85, 0.93] vs CKA 0.61 |
| Normative torsion amplification | **20–46×** larger than factual concepts |
| Alignment depth address | **ℓ★ ∈ {14, 20, 29–30}** — architecture-specific, falsifiable patching targets |
| Safe-prompt paradox | Safe prompts drive **larger Δτ** than unsafe (p < 10⁻³³ OLMo; cross-dataset replicated) |
| Low-rank alignment signature | DPO operates in **2–3 dim subspace** vs RLHF's 4–5 |
| Benchmark | LITMUS · **20,439 prompts** · 7 value axioms · 3 null-baseline controls |
| Models | OLMo-2-7B · Llama-3-8B · Mistral-7B · Qwen-2.5-7B (IT→PA pairs) |

<details>
<summary><b>📌 Three pre-registered falsifiable hypotheses — all confirmed</b></summary>

**H1 (Concept selectivity):** Alignment torsion Δ_f is larger for normative concepts than factual ones; T2 spectral anisotropy is the dominant mechanistic signature (CV > 0.50; AUC > 0.85).
✅ *Confirmed — CV = 0.64, AUC = 0.89, normative 20–46× > factual; 3 null-baseline controls hold*

**H2 (Depth address):** Alignment concentrates at an architecture-specific depth ℓ★, determined by architecture family — providing a surgical patching target.
✅ *Confirmed — ℓ★ reproducible per architecture family, compatible with ROME/ACDC patching*

**H3 (Safe-prompt paradox):** Safe prompts produce *larger* alignment torsion Δτ than unsafe ones.
✅ *Confirmed — p < 10⁻³³ (OLMo), p < 10⁻⁴ (Llama); cross-dataset replication on SafetyBench + WildGuard (n=150 each)*

</details>

---

### 2 · MENTIS — What Belief Changes Under Alignment?
> **[Under Review — NeurIPS 2026]** | [`torsional-belief-vector-field`](https://github.com/pps121/torsional-belief-vector-field)
> **Team:** Partha Pratim Saha · Samarth Raina · Mayur Parvatikar · Amit Dhanda · Vinija Jain · Aman Chadha · Amitava Das

```
MENTIS · Headline Metrics
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  DPO torsion suppression (Mistral, Layer 27)
  ████████████████████████  44.4%   Cohen's d = 0.741 ***
  Bonferroni-corrected p-value        7.7 × 10⁻¹³

  H1 normative amplification          1500×  (vs factual concepts)
  Entropy–torsion bridge (Mistral)    ρ = −0.387   p = 5.43 × 10⁻³⁰
  17 geometric metrics · 4 model pairs · 20,439 prompts
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

### 3 · AgriTalk — Calibrated NLU for Agricultural Robotics
> [`AgriTalk`](https://github.com/pps121/AgriTalk) · Conformal prediction + HITL safety guarantees

**5-layer safety stack:** Input Sanitiser → Staleness Verifier → Conformal Predictor (RAPS) → Attribution Gate → Non-bypassable HITL for `ABORT` / `EMERGENCY_STOP`

---

### 4 · Semantic Helix / nDNA — Cross-Cultural AI
> Epistemic inheritance in merged LLMs via Fisher-Rao geometry · 8 cultural axes

---

## 🏆 Recognition & Fellowships

| Award | Year |
|---|---|
| 🛡️ **BlueDot Impact Scholar** — AGI Strategy + Technical AI Safety | 2025–2026 |
| 🔬 **LASR Labs** — Mechanistic interpretability research programme | 2025 |
| 📋 **NeurIPS 2025 Reviewer** — MTI-LLM Workshop | 2025 |
| 🖥️ **5× Google Colab Pro A100/H100** — Neuromatch AI Safety grant | 2025 |
| ☁️ **AWS AI & ML Scholar** | 2025 |
| 🎓 **Armenian LLM Summer School** — 90% scholarship | 2025 |
| 🌐 **Duke ML Summer School** | 2025 |
| 🌐 **Cohere Summer School** | 2025 |
| 🏙️ **University of Chicago DSI** — Eric & Wendy Schmidt Postdoctoral Fellowship | 2024 |
| 🎓 **MLx Generative AI Fellowship** — Oxford ML Summer School | 2024–2025 |
| 🧠 **diiP Summer School Paris** — Deep Learning & Interpretability | 2024 |
| 🤖 **Neuromatch Academy** — Deep Learning Summer School | 2023 |
| 🗽 **NYU AI Summer School** | 2022 |

---

## 🛠️ Technical Arsenal

<table>
<tr>
<td width="33%" valign="top">

**🔬 Geometric & Mathematical ML**
```
Fisher-Rao Metric
Cartan Torsion Tensor
Riemannian Manifolds
Frenet-Serret Framework
Persistent Homology
Spectral Methods (T2)
DTW Analysis
Information Geometry
Thermodynamic Length
```

</td>
<td width="33%" valign="top">

**🤖 LLMs & Alignment**
```
Mechanistic Interpretability
DPO / RLHF / SFT Probing
AI Safety & Alignment
Torsion-based Auditing
Belief State Geometry
Representation Engineering
Conformal Prediction (RAPS)
XAI / Explainable AI
```

</td>
<td width="33%" valign="top">

**⚙️ Stack**
```python
PyTorch · Transformers (HF)
OLMo · Llama · Mistral
LangChain · LlamaIndex
NumPy · SciPy · Plotly
Docker · Azure · AWS
LaTeX · scikit-learn
```

</td>
</tr>
</table>

---

## 🗂️ Key Repositories

| Repository | Description | Status |
|-----------|-------------|--------|
| [`graft-belief-geometry`](https://github.com/pps121/graft-belief-geometry) | GRAFT: post-hoc geometric audit of preference alignment | 🟢 Active |
| [`torsional-belief-vector-field`](https://github.com/pps121/torsional-belief-vector-field) | MENTIS — Riemannian torsion framework for alignment auditing | 🟢 Active |
| [`AgriTalk`](https://github.com/pps121/AgriTalk) | Calibrated NLU for agricultural robots — conformal prediction | 🟢 Active |
| [`nDNA`](https://github.com/pps121/nDNA) | Cultural epistemic inheritance in merged LLMs | 🟢 Active |
| [`pps121.github.io`](https://github.com/pps121/pps121.github.io) | Full academic portfolio | 🟢 Live |

---

## 💼 12 Years Across Industry & Academia

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🎓  Lecturer in CS &         Nalhati Govt. Polytechnic           2021–present
    Independent Researcher   BITS Pilani M.Tech · GPA 9.08 · Top 5%
                             NeurIPS 2025 author · 4 active research projects
                             All research self-funded, pre/post office hours

📚  Teaching Assistant       BITS Pilani (M.Tech Programme)      2021–2023
                             NLP · Deep Learning · Deep RL
                             Honorarium: USD $2,513.11

🏭  Lead Data Scientist      Wipro Limited, Bangalore            2021
                             Conversational AI · IBM Watson · 0.3M users

🔬  Senior Data Scientist    BirlaSoft / Johnson & Johnson R&D   2017–2019
                             Medical search engine · 0.1M+ users

🛡️  Project Engineer         IIT Kanpur                          2016–2017
                             Threat intelligence · cybersecurity research

🧬  Senior Systems Engg.     Infosys Technologies, Chennai       2011–2015
                             DNA alignment · Multiple Myeloma genomics
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 📊 GitHub Activity

<div align="center">

![Profile Views](https://komarev.com/ghpvc/?username=pps121&color=7c3aed&style=for-the-badge&label=Profile+Views)

| Metric | Value |
|:---|:---|
| 🔬 **Research Repos** | graft-belief-geometry · torsional-belief-vector-field · AgriTalk · nDNA |
| 📄 **Publications** | NeurIPS 2025 Workshop · SpringerNature ICOMP'24 · 3× under review / preprint |
| 🏆 **Fellowships** | BlueDot · LASR Labs · AWS Scholar · Duke ML · Oxford MLx · 14× competitive selections |
| 🌟 **Highlights** | NeurIPS 2025 Reviewer · 20,439-prompt benchmark · 4 model families probed |

[![GitHub followers](https://img.shields.io/github/followers/pps121?label=Followers&style=social)](https://github.com/pps121)
[![GitHub stars](https://img.shields.io/github/stars/pps121?label=Stars&style=social)](https://github.com/pps121)

</div>

---

I am actively seeking **fully-funded PhD positions starting 2026/2027** and open to:

- 🤝 Research collaborations in **mechanistic interpretability**, **geometric ML**, or **AI safety**
- 🎓 PhD discussions with faculty at world-class AI safety & interpretability groups
- 🔭 Partnerships validating geometric torsion findings against circuit-level causal analysis

**If you work at Anthropic · Redwood Research · ARC Evals · Oxford · Cambridge · MIT · CMU · or any world-class AI safety group — I would love to talk.**

<div align="center">

[![Email Me](https://img.shields.io/badge/📧%20Email%20Me-technical.partha%40gmail.com-7c3aed?style=for-the-badge)](mailto:technical.partha@gmail.com)
[![Full Portfolio](https://img.shields.io/badge/🌐%20Full%20Portfolio-pps121.github.io-0f0c29?style=for-the-badge)](https://pps121.github.io)

*"Geometry is not decoration. It is the language in which alignment speaks."*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=120&section=footer" width="100%"/>

</div>
