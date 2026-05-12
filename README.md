<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=220&section=header&text=Partha%20Pratim%20Saha&fontSize=44&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=AI%20Safety%20%C2%B7%20Mechanistic%20Interpretability%20%C2%B7%20Geometric%20Deep%20Learning%20%C2%B7%20AI%20Alignment&descAlignY=58&descSize=15&descColor=c8b6ff" width="100%"/>

[![Email](https://img.shields.io/badge/Email-technical.partha%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:technical.partha@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-partha121-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/partha121)
[![Portfolio](https://img.shields.io/badge/Portfolio-pps121.github.io-7c3aed?style=for-the-badge&logo=github-pages&logoColor=white)](https://pps121.github.io)
[![Scholar](https://img.shields.io/badge/Google%20Scholar-Publications-4285F4?style=for-the-badge&logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?user=M0nZ5pEAAAAJ&hl=en)
[![ORCID](https://img.shields.io/badge/ORCID-0000--0001--8140--7272-A6CE39?style=for-the-badge&logo=orcid&logoColor=white)](https://orcid.org/0000-0001-8140-7272)

</div>

---

## 🧭 Research Vision

<table>
<tr>
<td width="62%">

> **"AI systems must be aligned not only behaviourally but *geometrically* — with transparent, auditable internal representations that can be verified, not just tested."**

I build **differential-geometric and information-geometric frameworks** to answer a question that keeps me up at night: *What actually changes inside a model when we align it?*

My research treats transformer hidden-state sequences as discrete curves on a **Riemannian belief manifold** equipped with the Fisher-Rao metric. The **torsion tensor** — antisymmetric component of cross-layer covariance — captures rotational mismatch invisible to attention patterns or activation norms. I call the resulting suppression pockets **"brake layers"**: geometrically localised, alignment-specific, and falsifiable with existing causal patching tools.

**Four active research threads:**
- 🔬 **GRAFT** — Geometric alignment Audit
- 🧬 **MENTIS** — Multi-scale latent torsion across NeurIPS-scale benchmarks
- 🌱 **AgriTalk** — Calibrated NLU for agricultural robotics (PhD programme)
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
│  p < 10⁻³³  (OLMo · n=20,439)    │
│                                  │
│  AUC T2  : 0.89 [0.85–0.93]      │
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

## 🔬 Active Research Projects

### 1 · GRAFT — Geometric Representations of Alignment's Fingerprint in Transformer Belief Trajectories
> **ICML 2026 · Mechanistic Interpretability Workshop** | [`graft-belief-geometry`](https://github.com/pps121/graft-belief-geometry)

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
> **NeurIPS 2026 (in preparation)** | Measuring Multi-Scale Latent Torsion in Language Models

MENTIS delivers a **NeurIPS-scale empirical study** of belief geometry across the full LITMUS benchmark, introducing 8 new torsion metrics and rigorous thermodynamic analysis across DPO, RLHF, and SFT checkpoints.

```
MENTIS · Headline Metrics
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  DPO torsion suppression (Mistral, Layer 27)
  ████████████████████████  44.4%   Cohen's d = 0.741 ***
  Bonferroni-corrected p-value        7.7 × 10⁻¹³

  H1 normative amplification          1500×  (vs factual concepts)
  Thermodynamic gap (normative/factual)  10×
  Entropy–torsion bridge (Mistral)    ρ = −0.387   p = 5.43 × 10⁻³⁰

  DTW–Torsion lower bound
  DC(w) ≥ 0.875 · |Σ‖Sᴵᵀ‖_F − Σ‖Sᴾᴬ‖_F|

  17 geometric metrics · 3×2 SFT/DPO model pairs · 500 unsafe prompts
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

### 3 · AgriTalk — Calibrated NLU for Agricultural Robotics
> **PhD Research Programme** · GreenFieldData Competition | [`AgriTalk`](https://github.com/pps121/AgriTalk)

AgriTalk proposes **calibrated natural-language control interfaces for agricultural spray robots**. Three pillars missing from all existing approaches: **formal safety guarantees**, **mechanistic explainability via BVF attribution**, **streaming grounding under sensor dropout**.

| Contribution | Core Guarantee | Target Venue |
|---|---|---|
| **C1** Conformal NLU (RAPS) | P(y∈C(x)) ≥ 95% under seasonal shifts, HITL ≤ 25% | EMNLP/ACL 2027 |
| **C2** BVF Attribution | Kendall τ(IG, BVF) > 0.5 on safety-critical intents | ACL 2029 |
| **C3** Temporal Streaming Architecture | Grounding recall maintained at 10–50% sensor dropout | VLDB 2028 |
| **C4** Conformal Trust Evaluation | BVF explanations achieve superior trust calibration vs CoT | FAccT 2029 |

**5-layer safety stack:** Input Sanitiser → Staleness Verifier → Conformal Predictor (RAPS) → Attribution Sufficiency Gate → Non-bypassable HITL for `ABORT` / `EMERGENCY_STOP`

---

### 4 · Semantic Helix / nDNA — Cross-Cultural AI
> **Active** | Epistemic inheritance in merged LLMs via Fisher-Rao geometry

Unifies fine-tuning, alignment, distillation, and merging as measurable deformations of depth-wise semantic flow. Cultural nDNA measured via spectral curvature deviation Δκ_ℓ and thermodynamic length divergence ΔL_ℓ across **8 cultural axes**: African · Latin American · South Asian · East Asian · Arabic · Indigenous · European · Pacific Islander.

---

## 📄 Publications

| Year | Venue | Title | Role |
|------|-------|-------|------|
| 2026 | **ICML 2026 Workshop** | GRAFT: Geometric Representations of Alignment's Fingerprint in Transformer Belief Trajectories | First author |
| 2026 | **NeurIPS 2026** *(prep)* | MENTIS: What Belief Changes Under Alignment? Multi-Scale Latent Torsion in LLMs | First author |
| 2025 | **Preprint** | SPINAL: Scaling-law and Preference Integration in Neural Alignment Layers | Co-author |
| 2025 | **NeurIPS 2025 Workshop** | Prompting Away Stereotypes? Evaluating Bias in Text-to-Image Models for Occupations | Co-author · [arXiv](https://arxiv.org/pdf/2509.00849) |
| 2025 | **Journal** | Enhancing Human Empathy in Conversations Using Transformer-Based Models | Top contributor · [DOI](https://doi.org/10.5281/zenodo.15126395) |
| 2024 | **SpringerNature ICOMP'24** | Collaborative Federated Learning Cloud Based System | First author · [Paper](https://link.springer.com/chapter/10.1007/978-3-031-72171-7_3) |

---

## 📊 GitHub Activity

<div align="center">

| | |
|:---:|:---:|
| ![GitHub Stats](https://github-readme-stats.vercel.app/api?username=pps121&show_icons=true&hide_border=true&bg_color=0d1117&title_color=c084fc&icon_color=c084fc&text_color=e2e8f0&rank_icon=github&include_all_commits=true&cache_seconds=1800) | ![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=pps121&layout=compact&hide_border=true&bg_color=0d1117&title_color=c084fc&text_color=e2e8f0&langs_count=7&cache_seconds=1800) |

</div>

<div align="center">

![Contribution Graph](https://github-readme-activity-graph.vercel.app/graph?username=pps121&theme=tokyo-night&bg_color=0d1117&color=c084fc&line=7c3aed&point=a855f7&area=true&area_color=1e1b4b&hide_border=true)

</div>

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
Holonomy Defect
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
AgentAI / Multi-Agent Systems
```

</td>
<td width="33%" valign="top">

**⚙️ Stack**
```python
PyTorch · Transformers (HF)
OLMo · Llama · Mistral
Qwen · DeepSeek · Zephyr
LangChain · LlamaIndex
NumPy · SciPy · Plotly
Docker · Azure · AWS
LaTeX · MetaFlow
dtaidistance · scikit-learn
```

</td>
</tr>
</table>

---

## 🏆 Recognition & Fellowships

| Award | Details |
|---|---|
| 🛡️ **BlueDot Impact Scholar** | AGI Strategy + Technical AI Safety (2025–2026) — catastrophic risk, power-seeking, geometric alignment evaluation |
| 🔬 **LASR Labs** | Progressed through initial selection — mechanistic interpretability research programme |
| 📋 **NeurIPS 2025 Reviewer** | MTI-LLM Workshop |
| 🖥️ **5× Google Colab Pro A100/H100** | 300 GPU units each — Neuromatch Academy AI Safety grant |
| ☁️ **AWS AI & ML Scholar** | Udacity, 2025 |
| 🎓 **Armenian LLM Summer School 2025** | 90% full scholarship |
| 🏆 **SPAR Demo Day 2025** | AI Safety & Alignment demonstration — Neuromatch / AI Safety cohort |
| 🌐 **Duke ML Summer School 2025** | Competitive selection |
| 🌐 **Cohere Summer School 2025** | Competitive selection |
| 🏙️ **University of Chicago DSI 2024** | AI-Science Research Program · Eric & Wendy Schmidt Postdoctoral Fellowship |

---

## 🗂️ Key Repositories

| Repository | Description | Status |
|-----------|-------------|--------|
| [`graft-belief-geometry`](https://github.com/pps121/graft-belief-geometry) | GRAFT: post-hoc geometric audit of alignment — ICML 2026 MechInterp Workshop | 🟢 Active |
| [`AgriTalk`](https://github.com/pps121/AgriTalk) | Calibrated NLU for agricultural spray robots — conformal prediction + BVF attribution | 🟢 Active |
| [`torsional-belief-vector-field`](https://github.com/pps121/torsional-belief-vector-field) | TBVF / MENTIS — Riemannian torsion framework for alignment auditing | 🟢 Active |
| [`AutoResearchClaw`](https://github.com/pps121/AutoResearchClaw) | Autonomous AI research pipeline: idea → full conference-ready paper | 🟢 Contributed |
| [`pps121.github.io`](https://github.com/pps121/pps121.github.io) | Full academic portfolio — research, publications, CV | 🟢 Live |

---

## 💼 12 Years Across Industry & Academia

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🎓  Lecturer in CS          Nalhati Govt. Polytechnic College      2021 – present
                             BITS Pilani M.Tech · GPA 9.08/10 · Top 5%
                             50+ students supervised · 4 active research projects

🏭  Lead Data Scientist     Wipro Limited (Bangalore)              2021
                             Conversational AI · IBM Watson · 0.3M users

🔬  Senior Data Scientist   BirlaSoft / Johnson & Johnson R&D       2017 – 2019
                             Medical search engine · SciBERT/SpaCy · 0.1M+ users

🛡️  Project Engineer        IIT Kanpur                             2016 – 2017
                             Threat intelligence system · cybersecurity research

🧬  Senior Systems Engg.    Infosys Technologies (Chennai)         2011 – 2015
                             DNA alignment algorithms · Multiple Myeloma genomics
                             Top 10 cancer-driving genes · 3 research papers
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 📬 Let's Collaborate

I am actively seeking **fully-funded PhD positions starting 2026** and open to:

- 🤝 Research collaborations in **mechanistic interpretability**, **geometric ML**, or **AI safety**
- 🎓 PhD discussions with faculty at world-class AI safety & interpretability groups
- 🔭 Partnerships validating geometric torsion findings against circuit-level causal analysis
- 🌱 Applied work connecting geometric alignment theory to deployment-time safety monitoring

**If you work at Anthropic · Redwood Research · ARC Evals · Oxford FHI · Cambridge LTL · MIT · CMU · or any world-class AI safety group — I would love to talk.**

<div align="center">

[![Email Me](https://img.shields.io/badge/📧%20Email%20Me-technical.partha%40gmail.com-7c3aed?style=for-the-badge)](mailto:technical.partha@gmail.com)
[![Full Portfolio](https://img.shields.io/badge/🌐%20Full%20Portfolio-pps121.github.io-0f0c29?style=for-the-badge)](https://pps121.github.io)

*"Geometry is not decoration. It is the language in which alignment speaks."*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=120&section=footer" width="100%"/>

</div>
