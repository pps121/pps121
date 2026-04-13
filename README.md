<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:667eea,100:764ba2&height=200&section=header&text=Partha%20Pratim%20Saha&fontSize=40&fontColor=white&animation=fadeIn&fontAlignY=38&desc=Mechanistic%20Interpretability%20%7C%20AI-Safety%7C%20Large%20Language%20Models%7C%20Geometric%20Deep%20Learning%20%7C%20AI%20Alignment&descAlignY=55&descSize=16" width="100%"/>

[![Email](https://img.shields.io/badge/Email-technical.partha%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:technical.partha@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-pps121-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/pps121)
[![Website](https://img.shields.io/badge/Website-pps121.github.io-667eea?style=for-the-badge&logo=github-pages&logoColor=white)](https://pps121.github.io)
[![Research](https://img.shields.io/badge/Research-TBVF%20Paper-764ba2?style=for-the-badge&logo=arxiv&logoColor=white)](https://github.com/pps121/torsional-belief-vector-field)

</div>

---

## 🧭 Research Vision

> **Can the geometry of thought reveal how alignment works?**

I develop **differential-geometric frameworks** for understanding how large language models encode, transform, and ultimately suppress beliefs — with a focus on mechanistic interpretability and AI alignment. My flagship framework, the **Torsional Belief Vector Field (TBVF)**, models transformer hidden states as discrete curves on a Riemannian belief manifold equipped with a Cartan torsion connection. This reveals, for the first time, *where* and *how* DPO/RLHF alignment geometrically reshapes model internals — creating what I call **"brake layers"**: localized, geometrically distinct suppression mechanisms.

**I am actively seeking fully-funded PhD positions** at world-class research universities in mechanistic interpretability, geometric deep learning, and AI alignment.

---

## 🔬 Flagship Research: Torsional Belief Vector Fields

<table>
<tr>
<td width="60%">

**Torsional Belief Vector Field** treats each transformer layer's hidden state as a point on a high-dimensional Riemannian manifold with Fisher-Rao metric. The *torsion tensor* — antisymmetric component of cross-layer covariance — measures rotational mismatch between consecutive belief updates.
<!--
**Key discovery**: DPO alignment suppresses torsion norm by **44.4%** in Mistral-7B mid-early layers (Cohen's *d* = 0.611), with peak statistical significance at layer 27 (*d* = 0.741, *p* = 7.7×10⁻¹³ after Bonferroni correction). This is not noise — it is geometry.
-->
</td>
<td width="40%" align="center">

```
Layer 27 (Peak Brake Layer):
━━━━━━━━━━━━━━━━━━━━━━━━━━━
SFT torsion norm:  ████████████ 0.66
DPO torsion norm:  ██████       0.42
Cohen's d:         0.741 ***
p-value:           7.7 × 10⁻¹³
━━━━━━━━━━━━━━━━━━━━━━━━━━━━
"Brake layers are geometry."
```

</td>
</tr>
</table>
<!--
**📄 Paper:** [Where Alignment Bends: Geometric Torsion as a Mechanistic Probe of Preference Optimization](https://github.com/pps121/torsional-belief-vector-field)  
*Submitted to ICML 2026 Mechanistic Interpretability Workshop*

**🔗 Code + Data:** [github.com/pps121/torsional-belief-vector-field](https://github.com/pps121/torsional-belief-vector-field)
-->
---

## 📊 Research at a Glance

| Metric | Result |
|--------|--------|
| Models analyzed | OLMo-7B, Mistral-7B, Zephyr-7B (SFT+DPO pairs) |
| Torsion metrics developed | 17 (Frenet-Serret, spectral, holonomy, Ricci, Wasserstein…) |
| Peak alignment effect | 44.4% torsion suppression (Mistral mid-early layers) |
| Peak significance | *p* = 7.7×10⁻¹³, Cohen's *d* = 0.741 (layer 27) |
| DTW-Torsion bound | DC(*w*) ≥ 0.875 · |Σ‖S^IT‖_F − Σ‖S^PA‖_F| |
| Concepts tested (DTW) | 20 semantic concepts × 2 sentence framings |

---

## 🚀 Current Status

```
🟢 ACTIVE  — Submitting to ICML 2026 MechInterp Workshop
🟡 SEEKING — Fully-funded PhD (2026 intake), world-class research universities
🔵 BUILDING — Extending TBVF to vision transformers and multimodal models
```

**Research interests for PhD:**
- Mechanistic interpretability of alignment techniques (DPO, RLHF, CAI)
- Geometric / topological methods for neural network analysis  
- Formal foundations of AI safety and inner alignment
- Emergent computation and representation learning in LLMs

---

## 🗂️ Repositories

| Repository | Description | Status |
|-----------|-------------|--------|
| [🧮 torsional-belief-vector-field](https://github.com/pps121/torsional-belief-vector-field) | Geometric torsion framework for alignment — ICML 2026 | 🟢 Active |
| [🌐 pps121.github.io](https://github.com/pps121/pps121.github.io) | Academic portfolio website | 🟢 Live |

---

## 🛠️ Technical Stack

**Languages:** Python · LaTeX · Bash  
**ML/DL:** PyTorch · Hugging Face Transformers · PEFT  
**Math/Science:** NumPy · SciPy · scikit-learn · dtaidistance  
**Visualization:** Matplotlib · Plotly · Seaborn  
**Geometric ML:** Custom Riemannian geometry implementations (Fisher-Rao, Cartan connection, torsion tensor)

---

## 📬 Let's Collaborate

I am open to:
- Research collaborations on mechanistic interpretability or geometric ML
- PhD discussions with faculty working on AI alignment, interpretability, or geometric deep learning
- Feedback on TBVF framework and theoretical extensions

**📧 [technical.partha@gmail.com](mailto:technical.partha@gmail.com)**

---

<div align="center">

*"Geometry is not decoration. It is the language in which alignment speaks."*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:764ba2,100:667eea&height=100&section=footer" width="100%"/>

</div>
