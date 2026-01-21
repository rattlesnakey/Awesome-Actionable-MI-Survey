<h1 align="center"> 🔎 Locate, Steer, and Improve: A Practical Survey of Actionable Mechanistic Interpretability in Large Language Models </h1>

<div align="center">

[![PDF](https://img.shields.io/badge/PDF-Download-red?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](https://github.com/rattlesnakey/Awesome-Actionable-MI-Survey/blob/master/Actionable-MI-Survey.pdf)
[![Status](https://img.shields.io/badge/STATUS-Active-brightgreen?style=for-the-badge)]()
<!-- [![Preprints](https://img.shields.io/badge/Preprints.org-202511.2077-blue?style=for-the-badge)](https://www.preprints.org/manuscript/202511.2077/v1) -->

</div>

> We will continue to update this repository.

If you enjoy or benefit from the project, a star ⭐ on GitHub would be greatly appreciated and will help you stay informed about future updates.


## 📖 Table of Contents
- [Overview](#-overview)
- [Latest News](#-latest-news)
- [Taxonomy & Legends](#-taxonomy--legends)
- [Paper List](#-paper-list)
  - [1. Improve Alignment](#1-improve-alignment)
    - [Safety and Reliability](#safety-and-reliability)
    - [Fairness and Bias](#fairness-and-bias)
    - [Persona and Role](#persona-and-role)
  - [2. Improve Capability](#2-improve-capability)
    - [Multilingualism](#multilingualism)
    - [Knowledge Management](#knowledge-management)
    - [Logic and Reasoning](#logic-and-reasoning)
  - [3. Improve Efficiency](#3-improve-efficiency)
    - [Efficient Training](#efficient-training)
    - [Efficient Inference](#efficient-inference)
- [Citation](#-citation)
- [Contact](#-contact)

## 📖 Overview
> **A systematic survey on how to locate interpretable objects, steer model behaviors, and improve LLMs (Alignment, Capability, Efficiency) via Mechanistic Interpretability.**

![Overview Figure](assets/overview_figure.png)

*Note: The figure illustrates our framework: **Locate** (Identifying internal objects), **Steer** (Manipulating behaviors), and **Improve** (Downstream applications).*

Mechanistic Interpretability (MI) has evolved from merely observing model internals to actively intervening in them. This repository maintains a curated list of papers reviewed in our survey, focusing on **Actionable MI**.

## 🔥 Latest News
<!-- - **[2025-XX-XX]** Our paper is available on arXiv! Check it out [here](https://arxiv.org/). -->
- **[2026-1-3]** This repository is created to track the latest progress in Actionable MI.

## 🏷 Taxonomy & Legends

To help navigate the paper list, we use the following abbreviations for Objects, Localizing Methods, and Steering Methods:

### Interpretable Objects

The core interpretable objects in our survey are shown below:

<div align="center">
  <img src="assets/notation.png" width="600">
</div>


### Localizing Methods (How to find it?)
- **Magnitude Analysis**: Weights or activation magnitude analysis, training-free but
data-dependent
- **Causal Attribution**: Patching and ablation
- **Gradient Detection**: Data-dependent and incurs extra compute
- **Probing**: Supervised property decoding
- **Vocab Projection**: Logit Lens, direct semantic mapping
- **Circuit Discovery**: Causal subnetwork identification

### Steering Methods (How to control it?)
- **Amplitude Manipulation**: Scaling and replace
- **Targeted Optimization**: Weight editing, targeted fine-tuning
- **Vector Arithmetic**: Steering via feature and task vectors

---

## 📑 Paper List
> For studies employing multiple objects or localizing/steering methods, we annotate the primary tag.

### 1. Improve Alignment

#### Safety and Reliability
| Paper | Object | Localizing Method | Steering Method | Venue | Year | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **Safety Layers in Aligned Large Language Models: The Key to LLM Security** | Residual Stream | Causal Attribution | Targeted Optimization | ICLR | 2025 | [Link](https://openreview.net/forum?id=kUH1yPMAn7) |
| **Refusal in Language Models Is Mediated by a Single Direction** | Residual Stream | Causal Attribution | Vector Arithmetic | NeurIPS | 2024 | [Link](https://openreview.net/forum?id=pH3XAQME6c) |
| **LLMs Encode Harmfulness and Refusal Separately** | Residual Stream | Causal Attribution | Vector Arithmetic | NeurIPS | 2025 | [Link](https://openreview.net/forum?id=zLkpt30ngy) |
| **Refusal Falls off a Cliff: How Safety Alignment Fails in Reasoning?** | Residual Stream | Probing | Vector Arithmetic | ArXiv | 2025 | [Link](https://arxiv.org/abs/2510.06036) |
| **A Mechanistic Understanding of Alignment Algorithms: A Case Study on DPO and Toxicity** | Residual Stream | Probing | Targeted Optimization | ICML | 2024 | [Link](https://proceedings.mlr.press/v235/lee24a.html) |
| **Understanding Jailbreak Success: A Study of Latent Space Dynamics in Large Language Models** | Residual Stream | Causal Attribution | Vector Arithmetic | ArXiv | 2024 | [Link](https://arxiv.org/abs/2406.09289) |
| **Surgical, Cheap, and Flexible: Mitigating False Refusal in Language Models via Single Vector Ablation** | Residual Stream | Causal Attribution | Vector Arithmetic | ICLR | 2025 | [Link](https://openreview.net/forum?id=SCBn8MCLwc) |
| **Refusal Direction is Universal Across Safety-Aligned Languages** | Residual Stream | Causal Attribution | Vector Arithmetic | NeurIPS | 2025 | [Link](https://openreview.net/forum?id=eWxKpdAdXH) |
| **Truthful or Fabricated? Using Causal Attribution to Mitigate Reward Hacking in Explanations** | Residual Stream | Causal Attribution | Vector Arithmetic | ICML | 2025 | [Link](https://arxiv.org/abs/2504.05294) |
| **Internal Causal Mechanisms Robustly Predict Language Model Out-of-Distribution Behaviors** | Residual Stream | Causal Attribution | Vector Arithmetic | ICML | 2025 | [Link](https://openreview.net/forum?id=wGFEzfhFae) |
| **The Hidden Dimensions of LLM Alignment: A Multi-Dimensional Analysis of Orthogonal Safety Directions** | Residual Stream | Causal Attribution | Vector Arithmetic | ICML | 2025 | [Link](https://openreview.net/forum?id=pH3XAQME6c) |
| **DoLa: Decoding by Contrasting Layers Improves Factuality in Large Language Models** | Residual Stream | Vocab Projection | Vector Arithmetic | ICLR | 2024 | [Link](https://openreview.net/forum?id=Th6NyL07na) |
| **In-Context Sharpness as Alerts: An Inner Representation Perspective for Hallucination Mitigation** | Residual Stream | Vocab Projection | Vector Arithmetic | ICML | 2024 | [Link](https://openreview.net/forum?id=s3e8poX3kb) |
| **TruthX: Alleviating Hallucinations by Editing Large Language Models in Truthful Space** | Residual Stream | Probing | Vector Arithmetic | ACL | 2024 | [Link](https://aclanthology.org/2024.acl-long.483/) |
| **LLMs Know More Than They Show: On the Intrinsic Representation of LLM Hallucinations** | Residual Stream | Probing | Vector Arithmetic | ICLR | 2025 | [Link](https://openreview.net/forum?id=KRnsX5Em3W) |
| **Improving Instruction-Following in Language Models through Activation Steering** | Residual Stream | - | Vector Arithmetic | ICLR | 2025 | [Link](https://openreview.net/forum?id=wozhdnRCtw) |
| **On the Role of MHA Heads in Large Language Model Safety** | MHA | Causal Attribution | Amplitude Manipulation | ICLR | 2025 | [Link](https://openreview.net/forum?id=h0Ak8A5yqw) |
| **Refine Large Language Model Fine-tuning via Instruction Vector** | MHA | Causal Attribution | Targeted Optimization | ArXiv | 2024 | [Link](https://arxiv.org/abs/2406.12227) |
| **Towards Understanding Safety Alignment: A Mechanistic Perspective from Safety Neurons** | Neuron | Causal Attribution | Amplitude Manipulation | ArXiv | 2025 | [Link](https://openreview.net/forum?id=1NkrxqY4jK) |
| **Whispering Experts: Neural Interventions for Toxicity Mitigation in Language Models** | Neuron | Magnitude Analysis | Amplitude Manipulation | ICML | 2024 | [Link](https://openreview.net/forum?id=2P6GVfSrfZ) |
| **H-Neurons: On the Existence, Impact, and Origin of Hallucination-Associated Neurons in LLMs** | Neuron | Magnitude Analysis | Amplitude Manipulation | ArXiv | 2025 | [Link](https://arxiv.org/abs/2512.01797) |
| **Understanding and Enhancing Safety Mechanisms of LLMs via Safety-Specific Neuron** | Neuron | Magnitude Analysis | Targeted Optimization | ICLR | 2025 | [Link](https://openreview.net/forum?id=yR47RmND1m) |
| **Precision Knowledge Editing: Enhancing Safety in Large Language Models** | Neuron | Magnitude Analysis | Targeted Optimization | ArXiv | 2025 | [Link](https://arxiv.org/abs/2410.03772) |
| **Scaling Monosemanticity: Extracting Interpretable Features from Claude 3 Sonnet** | SAE Feature | Magnitude Analysis | Amplitude Manipulation | Blog | 2024 | [Link](https://transformer-circuits.pub/2024/scaling-monosemanticity/index.html) |
| **Breaking Bad Tokens: Detoxification of LLMs Using Sparse Autoencoders** | SAE Feature | Magnitude Analysis | Amplitude Manipulation | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.641/) |
| **Understanding Refusal in Language Models with Sparse Autoencoders** | SAE Feature | Magnitude Analysis | Amplitude Manipulation | EMNLP | 2025 | [Link](https://aclanthology.org/2025.findings-emnlp.338/) |
| **Safe-SAIL: Towards a Fine-grained Safety Landscape of Large Language Models via Sparse Autoencoder Interpretation Framework** | SAE Feature | Magnitude Analysis | Amplitude Manipulation | ArXiv | 2025 | [Link](https://arxiv.org/abs/2509.18127) |
| **AxBench: Steering LLMs? Even Simple Baselines Outperform Sparse Autoencoders** | SAE Feature | Magnitude Analysis | Vector Arithmetic | ICML | 2025 | [Link](https://openreview.net/forum?id=K2CckZjNy0) |
| **Saif: A sparse autoencoder framework for interpreting and steering instruction following of language models** | SAE Feature | Magnitude Analysis | Vector Arithmetic | ArXiv | 2025 | [Link](https://arxiv.org/abs/2502.11356) |
| **Training Superior Sparse Autoencoders for Instruct Models** | SAE Feature | Magnitude Analysis | Vector Arithmetic | ArXiv | 2025 | [Link](https://arxiv.org/abs/2506.07691) |
| **Towards Secure Tuning: Mitigating Security Risks Arising from Benign Instruction Fine-Tuning** | Token Embedding | Gradient Detection | Vector Arithmetic | ArXiv | 2025 | [Link](https://arxiv.org/abs/2507.18043) |
| **Pierce the Mists, Greet the Sky: Decipher Knowledge Overshadowing via Knowledge Circuit Analysis** | MHA & FFN | Circuit Discovery | Targeted Optimization | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.781/) |

#### Fairness and Bias
| Paper | Object | Localizing Method | Steering Method | Venue | Year | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **Entangled in Representations: Mechanistic Investigation of Cultural Biases in Large Language Models** | Residual Stream | Causal Attribution | - | ArXiv | 2025 | [Link](https://arxiv.org/abs/2508.08879) |
| **MPF: Aligning and Debiasing Language Models Post Deployment via Multi Perspective Fusion** | Residual Stream | - | Amplitude Manipulation | ICML | 2025 | [Link](https://arxiv.org/abs/2507.02595) |
| **Mitigate Position Bias in LLMs via Scaling a Single Hidden States Channel** | Residual Stream | Magnitude Analysis | Amplitude Manipulation | ACL | 2025 | [Link](https://aclanthology.org/2025.findings-acl.316/) |
| **Analysing Moral Bias in Finetuned LLMs through Mechanistic Interpretability** | Residual Stream | Causal Attribution | Amplitude Manipulation | ArXiv | 2025 | [Link](https://arxiv.org/abs/2510.12229) |
| **Investigating Gender Bias in Language Models Using Causal Mediation Analysis** | MHA | Causal Attribution | Amplitude Manipulation | NeurIPS | 2020 | [Link](https://proceedings.neurips.cc/paper/2020/file/92650b2e92217715fe312e6fa7b90d82-Paper.pdf) |
| **Dissecting Bias in LLMs: A Mechanistic Interpretability Perspective** | MHA | Magnitude Analysis | Amplitude Manipulation | TMLR | 2025 | [Link](https://openreview.net/forum?id=EpQ2CBJTjD) |
| **Linear Representations of Political Perspective Emerge in Large Language Models** | MHA | Probing | Vector Arithmetic | ICLR | 2025 | [Link](https://openreview.net/forum?id=rwqShzb9li) |
| **Tracing Positional Bias in Financial Decision-Making: Mechanistic Insights from Qwen2.5** | MHA | Magnitude Analysis | - | ICAIF | 2025 | [Link](https://arxiv.org/abs/2508.18427) |
| **Eliminating Position Bias of Language Models: A Mechanistic Approach** | MHA | Magnitude Analysis | Amplitude Manipulation | ICLR | 2025 | [Link](https://openreview.net/forum?id=fvkElsJOsN) |
| **Identifying and Adapting Transformer-Components Responsible for Gender Bias in an English Language Model** | MHA | Causal Attribution | Targeted Optimization | ACLWS | 2023 | [Link](https://aclanthology.org/2023.blackboxnlp-1.29/) |
| **Locating and Mitigating Gender Bias in Large Language Models** | FFN | Causal Attribution | Targeted Optimization | ICIC | 2024 | [Link](https://arxiv.org/abs/2403.14409) |
| **Elucidating Mechanisms of Demographic Bias in LLMs for Healthcare** | FFN | Causal Attribution | Amplitude Manipulation | EMNLP | 2025 | [Link](https://aclanthology.org/2025.findings-emnlp.789) |
| **Anchored Answers: Unravelling Positional Bias in GPT-2's Multiple-Choice Questions** | FFN | Vocab Projection | Targeted Optimization | ACL | 2025 | [Link](https://aclanthology.org/2025.findings-acl.124/) |
| **Understanding and Mitigating Gender Bias in LLMs via Interpretable Neuron Editing** | Neuron | Circuit Discovery | Targeted Optimization | ArXiv | 2025 | [Link](https://arxiv.org/abs/2501.14457) |
| **The Devil is in the Neurons: Interpreting and Mitigating Social Biases in Pre-trained Language Models** | Neuron | Gradient Detection | Amplitude Manipulation | ICLR | 2024 | [Link](https://openreview.net/forum?id=SQGUDc9tC8) |

#### Persona and Role
| Paper | Object | Localizing Method | Steering Method | Venue | Year | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **Can Role Vectors Affect LLM Behaviour?** | Residual Stream | Causal Attribution | Vector Arithmetic | EMNLP | 2025 | [Link](https://aclanthology.org/2025.findings-emnlp.963/) |
| **Persona vectors: Monitoring and controlling character traits in language models** | Residual Stream | Causal Attribution | Vector Arithmetic | ArXiv | 2025 | [Link](https://arxiv.org/abs/2507.21509) |
| **From Monolingual to Bilingual: Investigating Language Conditioning in Large Language Models for Psycholinguistic Tasks** | Residual Stream | Probing | - | ArXiv | 2025 | [Link](https://arxiv.org/abs/2508.02502) |
| **Mechanistic Interpretability of Emotion Inference in Large Language Models** | Residual Stream | Probing | Vector Arithmetic | ACL | 2025 | [Link](https://aclanthology.org/2025.findings-acl.679/) |
| **Personality as a Probe for LLM Evaluation: Method Trade-offs and Downstream Effects** | Residual Stream | Causal Attribution | Vector Arithmetic | NeurIPS | 2025 | [Link](https://openreview.net/forum?id=TWbcIU0DBr) |
| **Steering Llama 2 via Contrastive Activation Addition** | Residual Stream | Causal Attribution | Vector Arithmetic | ACL | 2024 | [Link](https://aclanthology.org/2024.acl-long.828/) |
| **Probing then Editing Response Personality of Large Language Models** | Residual Stream | Probing | Targeted Optimization | COLM | 2025 | [Link](https://openreview.net/pdf?id=z9SbcYYP0M) |
| **Neural Transparency: Mechanistic Interpretability Interfaces for Anticipating Model Behaviors for Personalized AI** | Residual Stream | Causal Attribution | - | ArXiv | 2025 | [Link](https://arxiv.org/abs/2511.00230) |
| **Psychological Steering in LLMs: An Evaluation of Effectiveness and Trustworthiness** | Residual Stream | Causal Attribution | Vector Arithmetic | ArXiv | 2025 | [Link](https://arxiv.org/abs/2510.04484) |
| **Steering Latent Traits, Not Learned Facts: An Empirical Study of Activation Control Limits** | Residual Stream | Causal Attribution | Vector Arithmetic | ArXiv | 2025 | [Link](https://arxiv.org/abs/2511.18284) |
| **Personality Vector: Modulating Personality of Large Language Models by Model Merging** | Residual Stream | Causal Attribution | Vector Arithmetic | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.1253/) |
| **Billy: Steering large language models via merging persona vectors for creative generation** | Residual Stream | Causal Attribution | Vector Arithmetic | ArXiv | 2025 | [Link](https://arxiv.org/abs/2510.10157) |
| **Personas as a way to model truthfulness in language models** | Residual Stream | Probing | - | EMNLP | 2024 | [Link](https://aclanthology.org/2024.emnlp-main.364/) |
| **Who's asking? User personas and the mechanics of latent misalignment** | Residual Stream | Causal Attribution | Vector Arithmetic | NeurIPS | 2024 | [Link](https://proceedings.neurips.cc/paper_files/paper/2024/file/e40d5118ee8f837729fa877add71c38f-Paper-Conference.pdf) |
| **Understanding How Value Neurons Shape the Generation of Specified Values in LLMs** | Neuron | Causal Attribution | Amplitude Manipulation | EMNLP | 2025 | [Link](https://aclanthology.org/2025.findings-emnlp.501/) |
| **Neuron based Personality Trait Induction in Large Language Models** | Neuron | Causal Attribution | Amplitude Manipulation | ICLR | 2025 | [Link](https://openreview.net/forum?id=LYHEY783Np) |
| **From Yes-Men to Truth-Tellers: Addressing Sycophancy in Large Language Models with Pinpoint Tuning** | Neuron | Causal Attribution | Targeted Optimization | ICML | 2024 | [Link](https://openreview.net/forum?id=d2vONO90Rw) |



### 2. Improve Capability
#### Logic and Reasoning
| Paper | Object | Localizing Method | Steering Method | Venue | Year | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **Reasoning-Finetuning Repurposes Latent Representations in Base Models** | Residual Stream | Causal Attribution | Vector Arithmetic | ICML | 2025 | [Link](https://doi.org/10.48550/arXiv.2507.12638) |
| **Improving Reasoning Performance in Large Language Models via Representation Engineering** | Residual Stream | Causal Attribution | Vector Arithmetic | ICLR | 2025 | [Link](https://arxiv.org/abs/2504.19483) |
| **Bottom-up Policy Optimization: Your Language Model Policy Secretly Contains Internal Policies** | Residual Stream | Vocab Projection | Targeted Optimization | ArXiv | 2025 | [Link](https://arxiv.org/abs/2512.19673v1) |
| **Unlocking General Long Chain-of-Thought Reasoning Capabilities of Large Language Models via Representation Engineering** | Residual Stream | Causal Attribution | Vector Arithmetic | ACL | 2025 | [Link](https://aclanthology.org/2025.acl-long.339/) |
| **Probing for Arithmetic Errors in Language Models** | Residual Stream | Probing | - | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.411/) |
| **Eliciting Chain-of-Thought in Base LLMs via Gradient-Based Representation Optimization** | Residual Stream | Probing | Vector Arithmetic | AAAI | 2026 | [Link](https://arxiv.org/abs/2511.19131) |
| **Understanding Reasoning in Thinking Language Models via Steering Vectors** | Residual Stream | Causal Attribution | Vector Arithmetic | ICLR | 2025 | [Link](https://arxiv.org/abs/2506.18167) |
| **Hopping Too Late: Exploring the Limitations of Large Language Models on Multi-Hop Queries** | Residual Stream | Probing | - | EMNLP | 2024 | [Link](https://doi.org/10.18653/v1/2024.emnlp-main.781) |
| **Physics of Language Models: Part 2.1, Grade-School Math and the Hidden Reasoning Process** | Residual Stream | Probing | - | ICLR | 2025 | [Link](https://openreview.net/forum?id=Tn5B6Udq3E) |
| **The Reasoning-Memorization Interplay in Language Models Is Mediated by a Single Direction** | Residual Stream | Causal Attribution | Vector Arithmetic | ACL | 2025 | [Link](https://aclanthology.org/2025.findings-acl.1111/) |
| **Uncovering Latent Chain of Thought Vectors in Language Models** | Residual Stream | Causal Attribution | Vector Arithmetic | ICLR | 2025 | [Link](https://arxiv.org/abs/2409.14026) |
| **Fractional Reasoning via Latent Steering Vectors Improves Inference Time Compute** | Residual Stream | Causal Attribution | Vector Arithmetic | ArXiv | 2025 | [Link](https://arxiv.org/abs/2506.15882) |
| **Steering LLM Reasoning Through Bias-Only Adaptation** | Residual Stream | Causal Attribution | Vector Arithmetic | EMNLP | 2025 | [Link](https://arxiv.org/abs/2505.18706) |
| **Feature Extraction and Steering for Enhanced Chain-of-Thought Reasoning in Language Models** | Residual Stream | Causal Attribution | Vector Arithmetic | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.552/) |
| **How do Large Language Models Learn In-Context? Query and Key Matrices of In-Context Heads are Two Towers for Metric Learning** | MHA | Magnitude Analysis | Amplitude Manipulation | EMNLP | 2024 | [Link](https://doi.org/10.18653/v1/2024.emnlp-main.192) |
| **Interpreting Arithmetic Mechanism in Large Language Models through Comparative Neuron Analysis** | MHA | Causal Attribution | Amplitude Manipulation | EMNLP | 2024 | [Link](https://aclanthology.org/2024.emnlp-main.193/) |
| **Back MHA: Understanding and Enhancing Multi-Hop Reasoning in Large Language Models** | MHA | Causal Attribution | - | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.567/) |
| **Chain-of-Thought in Large Language Models: Decoding, Projection, and Activation** | MHA & FFN | Magnitude Analysis | - | ArXiv | 2024 | [Link](https://arxiv.org/abs/2412.03944) |
| **Interpreting and Improving Large Language Models in Arithmetic Calculation** | MHA & FFN | Causal Attribution | Targeted Optimization | ICML | 2024 | [Link](https://openreview.net/forum?id=CfOtiepP8s) |
| **A Mechanistic Interpretation of Arithmetic Reasoning in Language Models using Causal Mediation Analysis** | MHA & FFN | Causal Attribution | - | EMNLP | 2023 | [Link](https://doi.org/10.18653/v1/2023.emnlp-main.435) |
| **Uncovering the Interpretation of Large Language Models** | MHA & FFN | Causal Attribution | - | COMPSAC | 2024 | [Link](https://doi.org/10.1109/COMPSAC61105.2024.00143) |
| **Understanding Addition in Transformers** | MHA & FFN | Causal Attribution | Amplitude Manipulation | ICLR | 2024 | [Link](https://openreview.net/forum?id=rIx1YXVWZb) |
| **Inner Thinking Transformer: Leveraging Dynamic Depth Scaling to Foster Adaptive Internal Thinking** | MHA & FFN | Gradient Detection | Targeted Optimization | ACL | 2025 | [Link](https://aclanthology.org/2025.acl-long.1369/) |
| **How does GPT-2 compute greater-than?: Interpreting mathematical abilities in a pre-trained language model** | MHA & FFN | Circuit Discovery | - | NeurIPS | 2023 | [Link](http://papers.nips.cc/paper\_files/paper/2023/hash/efbba7719cc5172d175240f24be11280-Abstract-Conference.html) |
| **Arithmetic Without Algorithms: Language Models Solve Math with a Bag of Heuristics** | MHA & FFN | Circuit Discovery | - | ICLR | 2025 | [Link](https://openreview.net/forum?id=O9YTt26r2P) |
| **Sparse Autoencoders Learn Monosemantic Features in Vision-Language Models** | SAE Feature | Magnitude Analysis | Amplitude Manipulation | ArXiv | 2025 | [Link](https://doi.org/10.48550/arXiv.2504.02821) |
| **I Have Covered All the Bases Here: Interpreting Reasoning Features in Large Language Models via Sparse Autoencoders** | SAE Feature | Magnitude Analysis | Vector Arithmetic | ArXiv | 2025 | [Link](https://arxiv.org/abs/2503.18878) |
| **Internal states before wait modulate reasoning patterns** | SAE Feature | Magnitude Analysis | Vector Arithmetic | EMNLP | 2025 | [Link](https://aclanthology.org/2025.findings-emnlp.1012/) |
| **Can we interpret latent reasoning using current mechanistic interpretability tools?** | Token Embedding | Causal Attribution | Amplitude Manipulation | Blog | 2025 | [Link](https://www.alignmentforum.org/posts/YGAimivLxycZcqRFR/can-we-interpret-latent-reasoning-using-current-mechanistic) |
| **Analyzing chain-of-thought prompting in large language models via gradient-based feature attributions** | Token Embedding | Gradient Detection | - | ICML | 2023 | [Link](https://arxiv.org/abs/2307.13339) |
| **Probabilistic Soundness Guarantees in LLM Reasoning Chains** | Token Embedding | Magnitude Analysis | - | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.382/) |
| **Two Experts Are All You Need for Steering Thinking: Reinforcing Cognitive Effort in MoE Reasoning Models Without Additional Training** | FFN | Magnitude Analysis | Amplitude Manipulation | ArXiv | 2025 | [Link](https://doi.org/10.48550/arXiv.2505.14681) |

#### Multilingualism
| Paper | Object | Localizing Method | Steering Method | Venue | Year | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **Importance-based Neuron Allocation for Multilingual Neural Machine Translation** | Neuron | Magnitude Analysis | Amplitude Manipulation | ACL | 2021 | [Link](https://aclanthology.org/2021.acl-long.445/) |
| **On the Multilingual Ability of Decoder-based Pre-trained Language Models: Finding and Controlling Language-Specific Neurons** | Neuron | Magnitude Analysis | Amplitude Manipulation | NAACL | 2024 | [Link](https://aclanthology.org/2024.naacl-long.384/) |
| **Language-Specific Neurons: The Key to Multilingual Capabilities in Large Language Models** | Neuron | Magnitude Analysis | Amplitude Manipulation | ACL | 2024 | [Link](https://aclanthology.org/2024.acl-long.309/) |
| **How do Large Language Models Handle Multilingualism?** | Neuron | Magnitude Analysis | Amplitude Manipulation | NeurIPS | 2024 | [Link](https://proceedings.neurips.cc/paper_files/paper/2024/file/1bd359b32ab8b2a6bbafa1ed2856cf40-Paper-Conference.pdf) |
| **Language Arithmetics: Towards Systematic Language Neuron Identification and Manipulation** | Neuron | Magnitude Analysis | Amplitude Manipulation | ArXiv | 2025 | [Link](https://arxiv.org/abs/2507.22608) |
| **On Relation-Specific Neurons in Large Language Models** | Neuron | Magnitude Analysis | Amplitude Manipulation | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.52/) |
| **LinguaLens: Towards Interpreting Linguistic Mechanisms of Large Language Models via Sparse Auto-Encoder** | Neuron | Magnitude Analysis | Amplitude Manipulation | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.1433/) |
| **Sparse Autoencoders Can Capture Language-Specific Concepts Across Diverse Languages** | SAE Feature | Magnitude Analysis | Amplitude Manipulation | ArXiv | 2025 | [Link](https://arxiv.org/abs/2507.11230) |
| **Large Language Models Share Representations of Latent Grammatical Concepts Across Typologically Diverse Languages** | SAE Feature | Magnitude Analysis | Amplitude Manipulation | NAACL | 2025 | [Link](https://aclanthology.org/2025.naacl-long.312/) |
| **On the Language Neutrality of Pre-trained Multilingual Representations** | Residual Stream | Probing | - | EMNLP | 2020 | [Link](https://aclanthology.org/2020.findings-emnlp.150/) |
| **Can Cross-Lingual Transferability of Multilingual Transformers Be Activated Without End-Task Data?** | Residual Stream | - | Vector Arithmetic | ACL | 2023 | [Link](https://aclanthology.org/2023.findings-acl.796/) |
| **Identifying the Correlation Between Language Distance and Cross-Lingual Transfer in a Multilingual Representation Space** | Residual Stream | Magnitude Analysis | Vector Arithmetic | ACL | 2023 | [Link](https://aclanthology.org/2023.sigtyp-1.3/) |
| **Do Llamas Work in English? On the Latent Language of Multilingual Transformers** | Residual Stream | Vocab Projection | Vector Arithmetic | ACL | 2024 | [Link](https://aclanthology.org/2024.acl-long.820/) |
| **Exploring Alignment in Shared Cross-lingual Spaces** | Residual Stream | Magnitude Analysis | Vector Arithmetic | ACL | 2024 | [Link](https://aclanthology.org/2024.acl-long.344/) |
| **Why do LLaVA Vision-Language Models Reply to Images in English?** | Residual Stream | Probing | Vector Arithmetic | EMNLP | 2024 | [Link](https://aclanthology.org/2024.findings-emnlp.783/) |
| **ShifCon: Enhancing Non-Dominant Language Capabilities with a Shift-based Multilingual Contrastive Framework** | Residual Stream | Magnitude Analysis | Vector Arithmetic | ACL | 2025 | [Link](https://aclanthology.org/2025.acl-long.239/) |
| **Lost in Multilinguality: Dissecting Cross-lingual Factual Inconsistency in Transformer Language Models** | Residual Stream | Vocab Projection | Vector Arithmetic | ACL | 2025 | [Link](https://aclanthology.org/2025.acl-long.253/) |
| **The Semantic Hub Hypothesis: Language Models Share Semantic Representations Across Languages and Modalities** | Residual Stream | Vocab Projection | - | ICLR | 2025 | [Link](https://openreview.net/forum?id=FrFQpAgnGE) |
| **Language Mixing in Reasoning Language Models: Patterns, Impact, and Internal Causes** | Residual Stream | Vocab Projection | Vector Arithmetic | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.132/) |
| **Mechanistic Understanding and Mitigation of Language Confusion in English-Centric Large Language Models** | Residual Stream | Vocab Projection | Vector Arithmetic | EMNLP | 2025 | [Link](https://aclanthology.org/2025.findings-emnlp.37/) |
| **Tracing Multilingual Factual Knowledge Acquisition in Pretraining** | Residual Stream | Vocab Projection | Vector Arithmetic | EMNLP | 2025 | [Link](https://aclanthology.org/2025.findings-emnlp.113/) |

#### Knowledge Management
| Paper | Object | Localizing Method | Steering Method | Venue | Year | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **Locating and Editing Factual Associations in GPT** | FFN | Causal Attribution | Targeted Optimization | NeurIPS | 2022 | [Link](https://openreview.net/forum?id=-h6WAS6eE4) |
| **Mass-Editing Memory in a Transformer** | FFN | Causal Attribution | Targeted Optimization | ICLR | 2023 | [Link](https://openreview.net/forum?id=MkbcAHIYgyS) |
| **Joint Localization and Activation Editing for Low-Resource Fine-Tuning** | MHA | Magnitude Analysis | Targeted Optimization | ICML | 2025 | [Link](https://openreview.net/forum?id=Lllg9YjAFX) |
| **Taming Knowledge Conflicts in Language Models** | MHA | Magnitude Analysis | Amplitude Manipulation | ICML | 2025 | [Link](https://openreview.net/forum?id=0cEZyhHEks) |
| **Massive Values in Self-MHA Modules are the Key to Contextual Knowledge Understanding** | MHA | Magnitude Analysis | Amplitude Manipulation | ICML | 2025 | [Link](https://openreview.net/forum?id=1SMcxxQiSL) |
| **Cutting Off the Head Ends the Conflict: A Mechanism for Interpreting and Mitigating Knowledge Conflicts in Language Models** | MHA | Causal Attribution | Amplitude Manipulation | ACL | 2024 | [Link](https://doi.org/10.18653/v1/2024.findings-acl.70) |
| **Interpreting Key Mechanisms of Factual Recall in Transformer-Based Language Models** | MHA | Causal Attribution | Amplitude Manipulation | ArXiv | 2024 | [Link](https://arxiv.org/abs/2403.19521) |
| **Llama See, Llama Do: A Mechanistic Perspective on Contextual Entrainment and Distraction in LLMs** | MHA | Causal Attribution | Amplitude Manipulation | ACL | 2025 | [Link](https://aclanthology.org/2025.acl-long.791/) |
| **Probing and Boosting Large Language Models Capabilities via MHA Heads** | MHA | Probing | Targeted Optimization | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.1450/) |
| **TIES-Merging: Resolving Interference When Merging Models** | MHA & FFN | Magnitude Analysis | Vector Arithmetic | NeurIPS | 2023 | [Link](https://proceedings.neurips.cc/paper_files/paper/2023/hash/1644c9af28ab7916874f6fd6228a9bcf-Abstract-Conference.html) |
| **Neuron-Level Knowledge Attribution in Large Language Models** | MHA & FFN | Magnitude Analysis | Amplitude Manipulation | EMNLP | 2024 | [Link](https://aclanthology.org/2024.emnlp-main.191.pdf) |
| **Balancing Speciality and Versatility: a Coarse to Fine Framework for Supervised Fine-tuning Large Language Model** | MHA & FFN | Magnitude Analysis | Targeted Optimization | ACL | 2024 | [Link](https://doi.org/10.18653/v1/2024.findings-acl.445) |
| **Knowledge Localization: Mission Not Accomplished? Enter Query Localization!** | MHA & FFN | Magnitude Analysis | Amplitude Manipulation | ICLR | 2025 | [Link](https://openreview.net/forum?id=tfyHbvFZ0K) |
| **Enhancing Large Language Model Performance with Gradient-Based Parameter Selection** | MHA & FFN | Magnitude Analysis | Targeted Optimization | AAAI | 2025 | [Link](https://doi.org/10.1609/aaai.v39i23.34621) |
| **The Geometry of Forgetting: Analyzing Machine Unlearning through Local Learning Coefficients** | MHA & FFN | Magnitude Analysis | - | ICML | 2025 | [Link](https://openreview.net/forum?id=qKh7Aip3JC) |
| **Knowledge Circuits in Pretrained Transformers** | MHA & FFN | Circuit Discovery | - | NeurIPS | 2024 | [Link](https://proceedings.neurips.cc/paper_files/paper/2024/file/d6df31b1be98e04be48af8bedb95b499-Paper-Conference.pdf) |
| **Towards Secure Tuning: Mitigating Security Risks Arising from Benign Instruction Fine-Tuning** | MHA & FFN | Probing | Targeted Optimization | ArXiv | 2024 | [Link](https://doi.org/10.48550/arXiv.2410.04524) |
| **Unveiling Linguistic Regions in Large Language Models** | MHA & FFN | Gradient Detection | Targeted Optimization | ACL | 2024 | [Link](https://aclanthology.org/2024.acl-long.338/) |
| **Sens-Merging: Sensitivity-Guided Parameter Balancing for Merging Large Language Models** | MHA & FFN | Gradient Detection | Vector Arithmetic | ACL | 2025 | [Link](https://aclanthology.org/2025.findings-acl.984/) |
| **Activation-Guided Consensus Merging for Large Language Models** | MHA & FFN | Magnitude Analysis | Vector Arithmetic | NeurIPS | 2025 | [Link](https://openreview.net/pdf?id=ayzWTxb9ZD) |
| **Dissecting Recall of Factual Associations in Auto-Regressive Language Models** | MHA & FFN | Causal Attribution | - | EMNLP | 2023 | [Link](https://aclanthology.org/2023.emnlp-main.751.pdf) |
| **Multilingual Knowledge Editing with Language-Agnostic Factual Neurons** | Neuron | Magnitude Analysis | Targeted Optimization | COLING | 2025 | [Link](https://aclanthology.org/2025.coling-main.385/) |
| **Journey to the Center of the Knowledge Neurons: Discoveries of Language-Independent Knowledge Neurons and Degenerate Knowledge Neurons** | Neuron | Gradient Detection | Amplitude Manipulation | AAAI | 2024 | [Link](https://ojs.aaai.org/index.php/AAAI/article/view/29735) |
| **IRCAN: Mitigating Knowledge Conflicts in LLM Generation via Identifying and Reweighting Context-Aware Neurons** | Neuron | Gradient Detection | Amplitude Manipulation | NeurIPS | 2024 | [Link](http://papers.nips.cc/paper\_files/paper/2024/hash/08a9e28c96d016dd63903ab51cd085b0-Abstract-Conference.html) |
| **Identifying Query-Relevant Neurons in Large Language Models for Long-Form Texts** | Neuron | Gradient Detection | Amplitude Manipulation | AAAI | 2025 | [Link](https://doi.org/10.1609/aaai.v39i22.34529) |
| **Reviving Your MNEME: Predicting The Side Effects of LLM Unlearning and Fine-Tuning via Sparse Model Diffing** | Neuron | - | Amplitude Manipulation | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.1641/) |
| **SAEs Can Improve Unlearning: Dynamic Sparse Autoencoder Guardrails for Precision Unlearning in LLMs** | SAE Feature | Magnitude Analysis | Amplitude Manipulation | ICML | 2025 | [Link](https://openreview.net/pdf?id=8gFO7ebDLT) |
| **Breaking Bad Tokens: Detoxification of LLMs Using Sparse Autoencoders** | SAE Feature | Magnitude Analysis | Amplitude Manipulation | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.641/) |
| **Sparse Feature Circuits: Discovering and Editing Interpretable Causal Graphs in Language Models** | SAE Feature | Circuit Discovery | Amplitude Manipulation | ICLR | 2025 | [Link](https://arxiv.org/pdf/2403.19647) |
| **Impact of Co-occurrence on Factual Knowledge of Large Language Models** | Residual Stream | Probing | - | EMNLP | 2023 | [Link](https://aclanthology.org/2023.findings-emnlp.518.pdf) |
| **Backward Lens: Projecting Language Model Gradients into the Vocabulary Space** | Residual Stream | Vocab Projection | Targeted Optimization | EMNLP | 2024 | [Link](https://doi.org/10.18653/v1/2024.emnlp-main.142) |
| **ReFT: Representation Finetuning for Language Models** | Residual Stream | Causal Attribution | Targeted Optimization | NeurIPS | 2024 | [Link](https://proceedings.neurips.cc/paper_files/paper/2024/hash/75008a0fba53bf13b0bb3b7bff986e0e-Abstract-Conference.html) |
| **Analysing the Residual Stream of Language Models Under Knowledge Conflicts** | Residual Stream | Probing | - | ArXiv | 2024 | [Link](https://arxiv.org/abs/2410.16090) |
| **How Large Language Models Encode Context Knowledge? A Layer-Wise Probing Study** | Residual Stream | Probing | - | COLING | 2024 | [Link](https://aclanthology.org/2024.lrec-main.722.pdf) |
| **Exploring Concept Depth: How Large Language Models Acquire Knowledge and Concept at Different Layers?** | Residual Stream | Probing | - | COLING | 2025 | [Link](https://aclanthology.org/2025.coling-main.37.pdf) |
| **Transferring Linear Features Across Language Models With Model Stitching** | Residual Stream | Probing | Vector Arithmetic | NeurIPS | 2025 | [Link](https://openreview.net/forum?id=Qvvy0X63Fv) |


### 3. Improve Efficiency

#### Efficient Training
| Paper | Object | Localizing Method | Steering Method | Venue | Year | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **Task-Specific Skill Localization in Fine-tuned Language Models** | Neuron | Magnitude Analysis | Targeted Optimization | ICML | 2023 | [Link](https://arxiv.org/abs/2302.06600) |
| **LANDeRMT: Dectecting and Routing Language-Aware Neurons for Selectively Finetuning LLMs to Machine Translation** | Neuron | Gradient Detection | Targeted Optimization | ACL | 2024 | [Link](https://aclanthology.org/2024.acl-long.656/) |
| **Sparse is enough in fine-tuning pre-trained large language models** | Neuron | Gradient Detection | Targeted Optimization | ICML | 2024 | [Link](https://dl.acm.org/doi/10.5555/3692070.3693945) |
| **Fine-tuning Happens in Tiny Subspaces: Exploring Intrinsic Task-specific Subspaces of Pre-trained Language Models** | Neuron | Magnitude Analysis | Targeted Optimization | ACL | 2023 | [Link](https://aclanthology.org/2023.acl-long.95/) |
| **Let's Focus on Neuron: Neuron-Level Supervised Fine-tuning for Large Language Model** | Neuron | Magnitude Analysis | Targeted Optimization | COLING | 2025 | [Link](https://aclanthology.org/2025.coling-main.630/) |
| **Language-Specific Neurons Do Not Facilitate Cross-Lingual Transfer** | Neuron | Magnitude Analysis | Targeted Optimization | ACL | 2025 | [Link](https://aclanthology.org/2025.insights-1.6/) |
| **Sparse Subnetwork Enhancement for Underrepresented Languages in Large Language Models** | Neuron | Magnitude Analysis | Targeted Optimization | AACL | 2025 | [Link](https://arxiv.org/abs/2510.13580) |
| **How do Large Language Models Handle Multilingualism?** | Neuron | Causal Attribution | Targeted Optimization | NeurIPS | 2024 | [Link](https://proceedings.neurips.cc/paper_files/paper/2024/file/1bd359b32ab8b2a6bbafa1ed2856cf40-Paper-Conference.pdf) |
| **Optimizing Multimodal Language Models through MHA-based Interpretability** | MHA | Magnitude Analysis | Targeted Optimization | ICAI | 2025 | [Link](https://arxiv.org/abs/2511.23375) |
| **In-context Learning and Induction Heads** | MHA | Magnitude Analysis | - | ArXiv | 2022 | [Link](https://arxiv.org/abs/2209.11895) |
| **How Transformers Implement Induction Heads: Approximation and Optimization Analysis** | MHA | Magnitude Analysis | - | ArXiv | 2024 | [Link](https://openreview.net/forum?id=1lFZusYFHq) |
| **What needs to go right for an induction head? a mechanistic study of in-context learning circuits and their formation** | MHA | Magnitude Analysis | - | ICML | 2024 | [Link](https://dl.acm.org/doi/abs/10.5555/3692070.3693925) |
| **The developmental landscape of in-context learning** | MHA | Magnitude Analysis | - | TLMR | 2025 | [Link](https://arxiv.org/abs/2402.02364) |
| **In-Context Meta Learning Induces Multi-Phase Circuit Emergence** | MHA | Magnitude Analysis | - | ICLR | 2025 | [Link](https://openreview.net/forum?id=LNMfzv8TNb) |
| **Joint Localization and Activation Editing for Low-Resource Fine-Tuning** | MHA | Magnitude Analysis | Vector Arithmetic | ICML | 2025 | [Link](https://openreview.net/pdf?id=Lllg9YjAFX) |
| **The slingshot mechanism: An empirical study of adaptive optimizers and the Grokking Phenomenon** | MHA & FFN | Magnitude Analysis | - | NeurIPS | 2022 | [Link](https://openreview.net/pdf?id=lY1e0PNkSJ) |
| **Explaining grokking through circuit efficiency** | MHA & FFN | Magnitude Analysis | - | ArXiv | 2023 | [Link](https://arxiv.org/pdf/2309.02390) |
| **Towards Empirical Interpretation of Internal Circuits and Properties in Grokked Transformers on Modular Polynomials** | MHA & FFN | Magnitude Analysis | - | TMLR | 2024 | [Link](https://openreview.net/forum?id=MzSf70uXJO) |
| **Progress measures for grokking via mechanistic interpretability** | MHA & FFN | Magnitude Analysis | - | ICLR | 2023 | [Link](https://openreview.net/forum?id=9XFSbDPmdW) |
| **Predicting grokking long before it happens: A look into the loss landscape of models which grok** | MHA & FFN | Magnitude Analysis | - | ArXiv | 2023 | [Link](https://arxiv.org/abs/2306.13253) |
| **Exploring Grokking: Experimental and Mechanistic Investigations** | MHA & FFN | Magnitude Analysis | - | ArXiv | 2024 | [Link](https://arxiv.org/pdf/2412.10898) |
| **Omnigrok: Grokking Beyond Algorithmic Data** | MHA & FFN | Magnitude Analysis | - | ICLR | 2023 | [Link](https://openreview.net/forum?id=zDiHoIWa0q1) |
| **Where to find Grokking in LLM Pretraining? Monitor Memorization-to-Generalization without Test** | MHA & FFN | Magnitude Analysis | - | ArXiv | 2025 | [Link](https://openreview.net/forum?id=cG1EbmWiSs) |
| **Grokking of implicit reasoning in transformers: A mechanistic journey to the edge of generalization** | MHA & FFN | Magnitude Analysis | - | NeurIPS | 2024 | [Link](https://proceedings.neurips.cc/paper_files/paper/2024/file/ad217e0c7fecc71bdf48660ad6714b07-Paper-Conference.pdf) |
| **Unified View of Grokking, Double Descent and Emergent Abilities: A Comprehensive Study on Algorithm Task** | MHA & FFN | Magnitude Analysis | - | COLM | 2024 | [Link](https://arxiv.org/pdf/2402.15175) |
| **Fine-Tuning is Subgraph Search: A New Lens on Learning Dynamics** | MHA & FFN | Circuit Discovery | Targeted Optimization | ArXiv | 2025 | [Link](https://www.arxiv.org/pdf/2502.06106) |

#### Efficient Inference
| Paper | Object | Localizing Method | Steering Method | Venue | Year | Link |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: |
| **TokenSkip: Controllable Chain-of-Thought Compression in LLMs** | Token Embedding | Magitude Analysis | Amplitude Manipulation | EMNLP | 2025 | [Link](https://aclanthology.org/2025.emnlp-main.165/) |
| **Generic Token Compression in Multimodal Large Language Models from an Explainability Perspective** | Token Embedding | Gradient Detection | Amplitude Manipulation | ArXiv | 2025 | [Link](https://arxiv.org/abs/2506.01097) |
| **MHA Score is not All You Need for Token Importance Indicator in KV Cache Reduction: Value Also Matters** | Token Embedding | Magnitude Analysis | Amplitude Manipulation | EMNLP | 2024 | [Link](https://aclanthology.org/2024.emnlp-main.1178/) |
| **Fit and prune: Fast and training-free visual token pruning for multi-modal large language models** | Token Embedding | Magnitude Analysis | Amplitude Manipulation | AAAI | 2025 | [Link](https://ojs.aaai.org/index.php/AAAI/article/view/34366) |
| **Zipcache: Accurate and efficient kv cache quantization with salient token identification** | Token Embedding | Magnitude Analysis | Amplitude Manipulation | NeurIPS | 2024 | [Link](https://proceedings.neurips.cc/paper_files/paper/2024/hash/7e57131fdeb815764434b65162c88895-Abstract-Conference.html) |
| **Pyramidkv: Dynamic kv cache compression based on pyramidal information funneling** | Token Embedding | Magnitude Analysis | Amplitude Manipulation | COLM | 2025 | [Link](https://openreview.net/forum?id=ayi7qezU87) |
| **What Layers When: Learning to Skip Compute in LLMs with Residual Gates** | Residual Stream | Magnitude Analysis | Amplitude Manipulation | ArXiv | 2025 | [Link](https://arxiv.org/abs/2510.13876) |
| **Accelerating Large Language Model Inference with Self-Supervised Early Exits** | Residual Stream | Probing | Amplitude Manipulation | ArXiv | 2024 | [Link](https://arxiv.org/abs/2407.21082) |
| **LayerSkip: Enabling Early Exit Inference and Self-Speculative Decoding** | Residual Stream | Probing | Amplitude Manipulation | ACL | 2024 | [Link](https://aclanthology.org/2024.acl-long.681/) |
| **HadSkip: Homotopic and Adaptive Layer Skipping of Pre-trained Language Models for Efficient Inference** | Residual Stream | Magnitude Analysis | Amplitude Manipulation | EMNLP | 2023 | [Link](https://aclanthology.org/2023.findings-emnlp.283/) |
| **Learning to Skip the Middle Layers of Transformers** | Residual Stream | Magnitude Analysis | Amplitude Manipulation | ArXiv | 2025 | [Link](https://arxiv.org/abs/2506.21103) |
| **ShortGPT: Layers in Large Language Models are More Redundant Than You Expect** | Residual Stream | Magnitude Analysis | Amplitude Manipulation | ACL | 2025 | [Link](https://aclanthology.org/2025.findings-acl.1035/) |
| **Layer-wise quantization: A pragmatic and effective method for quantizing llms beyond integer bit-levels** | Residual Stream | Magnitude Analysis | - | ArXiv | 2024 | [Link](https://arxiv.org/abs/2406.17415) |
| **Towards Superior Quantization Accuracy: A Layer-sensitive Approach** | Residual Stream | Magnitude Analysis | - | ArXiv | 2025 | [Link](https://arxiv.org/abs/2503.06518) |
| **Exploring Layer-wise Information Effectiveness for Post-Training Quantization in Small Language Models** | Residual Stream | Magnitude Analysis | - | ArXiv | 2025 | [Link](https://arxiv.org/abs/2508.03332) |
| **Mix-QViT: Mixed-precision vision transformer quantization driven by layer importance and quantization sensitivity** | Residual Stream | Gradient Detection | - | ArXiv | 2025 | [Link](https://arxiv.org/abs/2501.06357) |
| **Lsaq: Layer-specific adaptive quantization for large language model deployment** | Residual Stream | Vocab Projection | - | ArXiv | 2024 | [Link](https://arxiv.org/abs/2412.18135) |
| **Towards Building Efficient Sentence BERT Models using Layer Pruning** | Residual Stream | Causal Attribution | Amplitude Manipulation | ACL | 2024 | [Link](https://aclanthology.org/2024.paclic-1.68/) |
| **KVSink: Understanding and Enhancing the Preservation of MHA Sinks in KV Cache Quantization for LLMs** | MHA & FFN | Circuit Discovery | - | COLM | 2025 | [Link](https://openreview.net/forum?id=gIqb6zWZoO) |
| **Massive activations in large language models** | MHA & FFN | Magnitude Analysis | - | NeurIPS | 2024 | [Link](https://openreview.net/forum?id=F7aAhfitX6) |
| **Systematic outliers in large language models** | MHA & FFN | Circuit Discovery | - | ICLR | 2025 | [Link](https://openreview.net/forum?id=rLX7Vyyzus) |
| **Quantizable Transformers: Removing Outliers by Helping MHA Heads Do Nothing** | MHA & FFN | Circuit Discovery | - | NeurIPS | 2023 | [Link](https://proceedings.neurips.cc/paper_files/paper/2023/hash/edbcb7583fd8921dad78adecfe06a99b-Abstract-Conference.html) |
| **RazorMHA: Efficient kv cache compression through retrieval heads** | MHA | Circuit Discovery | Amplitude Manipulation | ICLR | 2025 | [Link](https://iclr.cc/virtual/2025/poster/28028) |
| **DuoMHA: Efficient long-context llm inference with retrieval and streaming heads** | MHA | Circuit Discovery | Amplitude Manipulation | ICLR | 2025 | [Link](https://openreview.net/forum?id=cFu7ze7xUm) |
| **Unveiling visual perception in language models: An MHA head analysis approach** | MHA | Magnitude Analysis | - | CVPR | 2025 | [Link](https://openaccess.thecvf.com/content/CVPR2025/papers/Bi_Unveiling_Visual_Perception_in_Language_Models_An_MHA_Head_Analysis_CVPR_2025_paper.pdf) |
| **Rotatekv: Accurate and robust 2-bit kv cache quantization for llms via outlier-aware adaptive rotations** | MHA | Magnitude Analysis | Amplitude Manipulation | IJCAI | 2025 | [Link](https://www.ijcai.org/proceedings/2025/690) |
| **Efficient Streaming Language Models with MHA Sinks** | MHA | Magnitude Analysis | Amplitude Manipulation | ICLR | 2024 | [Link](https://openreview.net/forum?id=NG7sS51zVF) |
| **Unraveling babel: Exploring multilingual activation patterns within large language models** | Neuron | Magnitude Analysis | Amplitude Manipulation | ArXiv | 2024 | [Link](https://openreview.net/forum?id=nUtrPN0GHX) |
| **Neuron Specialization: Leveraging Intrinsic Task Modularity for Multilingual Machine Translation** | Neuron | Magnitude Analysis | - | EMNLP | 2024 | [Link](https://aclanthology.org/2024.emnlp-main.374/) |
| **The super weight in large language models** | FFN | Magnitude Analysis | Amplitude Manipulation | Arxiv | 2024 | [Link](https://arxiv.org/abs/2411.07191) |
| **Not all experts are equal: Efficient expert pruning and skipping for mixture-of-experts large language models** | FFN | Magnitude Analysis | Amplitude Manipulation | ACL | 2024 | [Link](https://aclanthology.org/2024.acl-long.334/) |
| **Unveiling super experts in mixture-of-experts large language models** | FFN | Magnitude Analysis | Amplitude Manipulation | ArXiv | 2025 | [Link](https://arxiv.org/abs/2507.23279) |



<!-- ## 🌟 Citation

If you find this survey or repository useful for your research, please cite:

```bibtex
@article{your_survey_key_2025,
  title={Locate, Steer, and Improve: A Survey of Actionable Mechanistic Interpretability in Large Language Models},
  author={Your Name and Co-authors},
  journal={arXiv preprint arXiv:25XX.XXXXX},
  year={2025}
}
``` -->

## 📧 Contact
Feel free to open an issue or contact us if you have any questions or want to include your work in this list!

Corresponding Author: Hengyuan Zhang (hengyuan.zhang88@gmail.com) and Zhihao Zhang (zhihaozhang017@gmail.com)
