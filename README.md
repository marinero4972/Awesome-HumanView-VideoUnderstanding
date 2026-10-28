[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
[![PR's Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](https://github.com/lxtGH/Awesome-HumanView-VideoUnderstanding/pulls)
<br />
<p align="center">
  <h1 align="center">Watch, Remember, Reason: Human-View Video Understanding with MLLMs</h1>
  <p align="center">
    <br />
    <a href="https://marinero4972.github.io/"><strong>Jiahao Meng</strong></a>
    ·
    <a href="https://openreview.net/profile?id=~Tan_Yue2"><strong>Yue Tan</strong></a>
    ·
    <a href="https://insomniaaac.github.io/"><strong>Qi Xu</strong></a>
    ·
    <strong>Kuan Gao</strong>
    ·
    <strong>Weisong Liu</strong>
    ·
    <a href="https://yanwei-li.com/"><strong>Yanwei Li</strong></a>
    ·
    <strong>Jason Li</strong>
    <br />
    <a href="https://ldkong.com/"><strong>Lingdong Kong</strong></a>
    ·
    <a href="https://haochen-wang409.github.io/"><strong>Haochen Wang</strong></a>
    ·
    <strong>Qianyu Zhou</strong>
    ·
    <a href="https://zhangzjn.github.io/"><strong>Jiangning Zhang</strong></a>
    ·
    <a href="https://sites.google.com/view/guangliangcheng"><strong>Guangliang Cheng</strong></a>
    <br />
    <a href="https://www.ai.pku.edu.cn/en/info/1459/2082.htm"><strong>Yunhai Tong</strong></a>
    ·
    <a href="http://luqi.info/"><strong>Lu Qi</strong></a>
    ·
    <a href="https://faculty.ucmerced.edu/mhyang/"><strong>Ming-Hsuan Yang</strong></a>
  </p>

  <p align="center">
    <a href='https://arxiv.org/pdf/2606.07433'>
      <img src='https://img.shields.io/badge/Paper-PDF-green?style=flat&logo=arXiv&logoColor=green' alt='Paper PDF'>
    </a>
  </p>
<br />

## Overview

This repository accompanies our survey, which takes a **human-view** perspective on LLM/MLLM-based video understanding by decomposing it into three core cognitive abilities and reviewing how recent methods realize each:

- **Watch** — perceptual grounding of multimodal video streams: fine-grained spatio-temporal grounding, comprehensive captioning, audio-visual (omni-modal) perception, and efficient long-video processing.
- **Remember** — maintaining context over long or streaming inputs: offline memory (agentic vs. non-agent) and streaming memory.
- **Reason** — deriving grounded answers from perceived and retained evidence: text-only reasoning and the emerging *thinking-with-videos* paradigm, each split into agentic and non-agent approaches.

Beyond methods, the survey covers domain-specific subfields (egocentric, sports, instructional, medical, narrative videos), training datasets and evaluation benchmarks across major task types and capability dimensions, and open problems on the path to scalable, memory-aware, evidence-grounded video intelligence.

## Table of Contents

- [1. Watch — How to Watch?](#1-watch--how-to-watch)
  - [1.1 Fine-grained Watching](#11-fine-grained-watching)
  - [1.2 Comprehensive Watching](#12-comprehensive-watching)
  - [1.3 Audio-Visual Watching](#13-audio-visual-watching)
  - [1.4 Efficient Watching](#14-efficient-watching)
- [2. Remember — How to Remember?](#2-remember--how-to-remember)
  - [2.1 Offline Memory — Agentic](#21-offline-memory--agentic)
  - [2.2 Offline Memory — Non-Agent](#22-offline-memory--non-agent)
  - [2.3 Streaming Memory](#23-streaming-memory)
- [3. Reason — How to Reason?](#3-reason--how-to-reason)
  - [3.1 Text-only Reasoning — Agentic](#31-text-only-reasoning--agentic)
  - [3.2 Text-only Reasoning — Non-Agent](#32-text-only-reasoning--non-agent)
  - [3.3 Thinking with Videos — Agentic](#33-thinking-with-videos--agentic)
  - [3.4 Thinking with Videos — Non-Agent](#34-thinking-with-videos--non-agent)
- [4. Subfields](#4-subfields)
  - [4.1 Egocentric Videos](#41-egocentric-videos)
  - [4.2 Sports Videos](#42-sports-videos)
  - [4.3 Instructional Videos](#43-instructional-videos)
  - [4.4 Medical Videos](#44-medical-videos)
  - [4.5 Movie and Narrative Videos](#45-movie-and-narrative-videos)
- [5. Datasets and Benchmarks](#5-datasets-and-benchmarks)
  - [5.1 Training Datasets](#51-training-datasets)
  - [5.2 Evaluation Benchmarks](#52-evaluation-benchmarks)
- [6. Future Directions](#6-future-directions)
- [Citation](#citation)
- [Contributing](#contributing)

---

## 1. Watch — How to Watch?

Watching corresponds to the perceptual stage where models transform raw multimodal inputs into structured representations. We organize methods along four complementary dimensions.

### 1.1 Fine-grained Watching

Precise spatio-temporal grounding: time representation, long-video efficiency, structured decoding, fine-grained perception architectures, and verifiable post-training. Includes both flagship methods (Table 2) and the broader family cited in §3.1.1 (temporal grounding, spatio-temporal grounding, video referring).

**Temporal grounding & VTG-style methods**

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2023 | ICCV | SOONet | [Scanning Only Once: An End-to-end Framework for Fast Temporal Grounding in Long Videos](https://arxiv.org/abs/2303.08345) | [Code](https://github.com/afcedf/SOONet) |
| 2023 | NeurIPS | SeViLA | [Self-Chained Image-Language Model for Video Localization and Question Answering](https://arxiv.org/abs/2305.06988) | [Code](https://github.com/Yui010206/SeViLA) |
| 2024 | CVPR | TimeChat | [TimeChat: A Time-sensitive Multimodal Large Language Model for Long Video Understanding](https://arxiv.org/abs/2312.02051) | [Code](https://github.com/RenShuhuai-Andy/TimeChat) |
| 2024 | CVPR | VTimeLLM | [VTimeLLM: Empower LLM to Grasp Video Moments](https://arxiv.org/abs/2311.18445) | [Code](https://github.com/huangb23/VTimeLLM) |
| 2024 | ECCV | LITA | [LITA: Language Instructed Temporal-Localization Assistant](https://arxiv.org/abs/2403.19046) | [Code](https://github.com/NVlabs/LITA) |
| 2024 | ICML | Momentor | [Momentor: Advancing Video Large Language Model with Fine-Grained Temporal Reasoning](https://arxiv.org/abs/2402.11435) | [Code](https://github.com/DCDmllm/Momentor) |
| 2026 | ICPR | LLaVA-MR | [LLaVA-MR: Large Language-and-Vision Assistant for Video Moment Retrieval](https://arxiv.org/abs/2411.14505) | - |
| 2025 | EMNLP Findings | Grounded-VideoLLM | [Grounded-VideoLLM: Sharpening Fine-grained Temporal Grounding in Video Large Language Models](https://arxiv.org/abs/2410.03290) | [Code](https://github.com/WHB139426/Grounded-Video-LLM) |
| 2025 | ICLR | TimeSuite | [TimeSuite: Improving MLLMs for Long Video Understanding via Grounded Tuning](https://arxiv.org/abs/2410.19702) | [Code](https://github.com/OpenGVLab/TimeSuite) |
| 2025 | ICLR | TRACE | [TRACE: Temporal Grounding Video LLM via Causal Event Modeling](https://arxiv.org/abs/2410.05643) | [Code](https://github.com/gyxxyg/TRACE) |
| 2025 | ICCV | DisTime | [DisTime: Distribution-based Time Representation for Video Large Language Models](https://arxiv.org/abs/2505.24329) | - |
| 2025 | AAAI | VTG-LLM | [VTG-LLM: Integrating Timestamp Knowledge into Video LLMs for Enhanced Video Temporal Grounding](https://arxiv.org/abs/2405.13382) | [Code](https://github.com/gyxxyg/VTG-LLM) |
| 2025 | arXiv | TAR-TVG | [TAR-TVG: Enhancing VLMs with Timestamp Anchor-Constrained Reasoning for Robust Temporal Video Grounding](https://arxiv.org/abs/2508.07683) | - |
| 2025 | arXiv | VideoPerceiver | [VideoPerceiver: Enhancing Fine-grained Temporal Perception in Video Multimodal Large Language Models](https://arxiv.org/abs/2511.18823) | - |
| 2025 | EMNLP | TVG-R1 | [Datasets and Recipes for Video Temporal Grounding via Reinforcement Learning](https://arxiv.org/abs/2507.18100) | - |
| 2026 | ACL | MUSEG | [MUSEG: Reinforcing Video Temporal Understanding via Timestamp-Aware Multi-Segment Grounding](https://arxiv.org/abs/2505.20715) | [Code](https://github.com/THUNLP-MT/MUSEG) |
| 2025 | NeurIPS | UniTime | [Universal Video Temporal Grounding with Generative Multi-modal Large Language Models](https://arxiv.org/abs/2506.18883) | [Project](https://lzq5.github.io/UniTime/) |
| 2025 | arXiv | Video-OPD | [Video-OPD: Efficient Post-training of Multimodal Large Language Models for Temporal Video Grounding via On-policy Distillation](https://arxiv.org/abs/2602.02994) | - |
| 2026 | CVPR | TimeLens | [TimeLens: Rethinking Video Temporal Grounding with Multimodal LLMs](https://arxiv.org/abs/2512.14698) | [Code](https://github.com/TencentARC/TimeLens) |
| 2026 | ICML | OMTG | [Towards One-to-Many Temporal Grounding](https://arxiv.org/abs/2606.06294) | [Code](https://insomniaaac.github.io/OMTG/) |
| 2026 | ECCV | SemVID | [Keeping the Evidence Chain: Semantic Evidence Allocation for Training-Free Token Pruning in Video Temporal Grounding](https://arxiv.org/abs/2603.05663) | - |
| 2026 | arXiv | SlotVTG | [SlotVTG: Object-Centric Adapter for Generalizable Video Temporal Grounding](https://arxiv.org/abs/2603.25733) | - |
| 2026 | arXiv | UniversalVTG | [UniversalVTG: A Universal and Lightweight Foundation Model for Video Temporal Grounding](https://arxiv.org/abs/2604.08522) | - |
| 2026 | CVPR | OmniVTG | [OmniVTG: A Large-Scale Dataset and Training Paradigm for Open-World Video Temporal Grounding](https://arxiv.org/abs/2604.25276) | [Code](https://github.com/oceanflowlab/OmniVTG) |
| 2026 | NeurIPS | EvoGround | [EvoGround: Self-Evolving Video Agents for Video Temporal Grounding](https://arxiv.org/abs/2605.13803) | [Code](https://github.com/minjoong507/EvoGround) |
| 2026 | arXiv | TimeLens2 | [TimeLens2: Generalist Video Temporal Grounding with Multimodal LLMs](https://arxiv.org/abs/2607.17423) | [Code](https://github.com/MCG-NJU/TimeLens2) |
| 2026 | arXiv | TimePLE | [TimePLE: Rethinking Temporal Representation for Video Temporal Grounding](https://arxiv.org/abs/2607.23951) | - |
| 2026 | arXiv | ID-VTG | [ID-VTG: Image-Disambiguated Video Temporal Grounding](https://arxiv.org/abs/2608.20127) | [Code](https://github.com/oceanflowlab/ID-VTG) |
| 2026 | arXiv | — | [Grounding with Confidence: Controllable Generative Video Temporal Grounding](https://arxiv.org/abs/2609.39883) | - |
| 2026 | arXiv | VideoEvolve | [VideoEvolve: Evolving Agent Harnesses for Video Temporal Grounding](https://arxiv.org/abs/2610.01766) | - |
| 2026 | arXiv | GMR | [Retrieving Any Relevant Moments: Benchmark and Models for Generalized Moment Retrieval](https://arxiv.org/abs/2605.02623) | - |

**Spatio-temporal grounding & video referring**

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2026 | CVPR | VITAL | [Thinking With Videos: Multimodal Tool-Augmented Reinforcement Learning for Long Video Reasoning](https://arxiv.org/abs/2508.04416) | - |
| 2025 | arXiv | Rex-Omni | [Detect Anything via Next Point Prediction](https://arxiv.org/abs/2510.12798) | [Code](https://github.com/IDEA-Research/Rex-Omni) |
| 2026 | ICML | Open-o3 Video | [Open-o3 Video: Grounded Video Reasoning with Explicit Spatio-Temporal Evidence](https://arxiv.org/abs/2510.20579) | [Code](https://github.com/marinero4972/Open-o3-Video) |
| 2025 | arXiv | STVG-o1 | [Thinking with Bounding Boxes: Enhancing Spatio-Temporal Video Grounding via Reinforcement Fine-tuning](https://arxiv.org/abs/2511.21375) | - |
| 2026 | TPAMI | Sa2VA | [Sa2VA: Marrying SAM2 with LLaVA for Dense Grounded Understanding of Images and Videos](https://arxiv.org/abs/2501.04001) | [Code](https://github.com/bytedance/Sa2VA) |
| 2025 | NeurIPS | SAMA | [SAMA: Towards Multi-Turn Referential Grounded Video Chat with Large Language Models](https://arxiv.org/abs/2505.18812) | - |
| 2026 | arXiv | Event-STVG | [Event-STVG: Spatio-Temporal Video Grounding for Long-Form Event Reasoning](https://arxiv.org/abs/2610.22444) | [Code](https://github.com/THU-KEG/EventSTVG) |
| 2026 | CVPR | SPARROW | [SPARROW: Learning Spatial Precision and Temporal Referential Consistency in Pixel-Grounded Video MLLMs](https://arxiv.org/abs/2603.12382) | [Code](https://github.com/RISys-Lab/SPARROW) |
| 2026 | ECCV | ScanFocus | [ScanFocus: A Coarse-to-Fine Framework for Spatio-Temporal Video Grounding](https://arxiv.org/abs/2607.13421) | - |
| 2026 | arXiv | ParallelTubeDecoding | [Locate Anything in Videos: Rethinking Efficient Generative Spatio-Temporal Video Grounding](https://arxiv.org/abs/2608.28192) | [Code](https://github.com/mbzuai-oryx/ParallelTubeDecoding) |
| 2026 | arXiv | TCoVP | [Think Visually Across Space and Time: Grounded Reasoning for Video Segmentation](https://arxiv.org/abs/2610.25090) | [Project](https://victor-wjw.github.io/TCoVP/) |
| 2026 | arXiv | AgentRVOS | [AgentRVOS: Reasoning over Object Tracks for Zero-Shot Referring Video Object Segmentation](https://arxiv.org/abs/2603.23489) | - |
| 2026 | CVPR | VIRST | [VIRST: Video-Instructed Reasoning Assistant for SpatioTemporal Segmentation](https://arxiv.org/abs/2603.27060) | - |
| 2026 | arXiv | ORVOS | [Online Reasoning Video Object Segmentation](https://arxiv.org/abs/2604.11411) | - |
| 2026 | arXiv | STAC | [STAC: Selective Spatiotemporal Aggregation and Compression for Video Reasoning Segmentation](https://arxiv.org/abs/2607.02922) | - |
| 2026 | arXiv | PhysMLLMs | [PhysMLLMs: Spatial Priors for Unified Referring Segmentation and Grounded Reasoning of Images and Videos](https://arxiv.org/abs/2608.24574) | - |
| 2026 | arXiv | OPERA | [OPERA: A Unified Omnimodal Progressive Spatio-Temporal Reasoning Agent for Referring Video Segmentation](https://arxiv.org/abs/2609.33338) | - |
| 2026 | arXiv | — | [Event-Driven Refresh and Recurrence Memory to Reduce Stale Grounding in Referring Video Object Segmentation](https://arxiv.org/abs/2609.38758) | - |

### 1.2 Comprehensive Watching

Whole-video, dense, and region-level captioning over visual-token sequences. Includes flagship methods (Table 2) and the broader family cited in §3.1.2.

**Whole-video captioning**

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2024 | ACL | Video-ChatGPT | [Video-ChatGPT: Towards Detailed Video Understanding via Large Vision and Language Models](https://arxiv.org/abs/2306.05424) | [Code](https://github.com/mbzuai-oryx/Video-ChatGPT) |
| 2024 | EMNLP | Video-LLaVA | [Video-LLaVA: Learning United Visual Representation by Alignment Before Projection](https://arxiv.org/abs/2311.10122) | [Code](https://github.com/PKU-YuanGroup/Video-LLaVA) |
| 2024 | arXiv | PLLaVA | [PLLaVA: Parameter-free LLaVA Extension from Images to Videos for Video Dense Captioning](https://arxiv.org/abs/2404.16994) | [Code](https://github.com/magic-research/PLLaVA) |
| 2024 | arXiv | Tarsier | [Tarsier: Recipes for Training and Evaluating Large Video Description Models](https://arxiv.org/abs/2407.00634) | [Code](https://github.com/bytedance/tarsier) |
| 2024 | arXiv | LLaVA-Video | [Video Instruction Tuning with Synthetic Data](https://arxiv.org/abs/2410.02713) | [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) |
| 2024 | arXiv | Video ReCap | [Video ReCap: Recursive Captioning of Hour-Long Videos](https://arxiv.org/abs/2402.13250) | [Code](https://github.com/md-mohaiminul/VideoRecap) |
| 2025 | arXiv | LongCaptioning | [LongCaptioning: Unlocking the Power of Long Caption Generation in Large Multimodal Models](https://arxiv.org/abs/2502.15393) | - |
| 2025 | ICML | SGC | [Fine-Grained Captioning of Long Videos through Scene Graph Consolidation](https://arxiv.org/abs/2502.16427) | - |
| 2025 | ICLR | AuroraCap | [AuroraCap: Efficient, Performant Video Detailed Captioning and a New Benchmark](https://arxiv.org/abs/2410.03051) | [Code](https://github.com/rese1f/aurora) |
| 2025 | arXiv | Tarsier2 | [Tarsier2: Advancing Large Vision-Language Models from Detailed Video Description to Comprehensive Video Understanding](https://arxiv.org/abs/2501.07888) | [Code](https://github.com/bytedance/tarsier) |
| 2025 | arXiv | video-SALMONN 2 | [video-SALMONN 2: Captioning-Enhanced Audio-Visual Large Language Models](https://arxiv.org/abs/2506.15220) | [Code](https://github.com/bytedance/video-SALMONN-2) |
| 2025 | arXiv | VideoCap-R1 | [VideoCap-R1: Enhancing MLLMs for Video Captioning via Structured Thinking](https://arxiv.org/abs/2506.01725) | - |
| 2025 | arXiv | OwlCap | [OwlCap: Harmonizing Motion-Detail for Video Captioning via HMD-270K and Caption Set Equivalence Reward](https://arxiv.org/abs/2508.18634) | - |
| 2025 | ACM MM | HMI / M-ACM | [Towards Fine-Grained Human Motion Video Captioning](https://arxiv.org/abs/2510.24767) | - |
| 2025 | arXiv | AnyCap | [AnyCap Project: A Unified Framework, Dataset, and Benchmark for Controllable Omni-modal Captioning](https://arxiv.org/abs/2507.12841) | [Code](https://github.com/anycap-project/anycap) |
| 2025 | arXiv | IF-VidCap | [IF-VidCap: Can Video Caption Models Follow Instructions?](https://arxiv.org/abs/2510.18726) | [Code](https://github.com/NJU-LINK/IF-VidCap) |
| 2025 | ACM MM | IntentVCNet | [IntentVCNet: Bridging Spatio-Temporal Gaps for Intention-Oriented Controllable Video Captioning](https://arxiv.org/abs/2507.18531) | - |
| 2026 | arXiv | PIGEONS | [PIGEONS: Incremental Long-Video Captioning with Persistent Identity Gallery and Evolving Overarching Narrative Summary](https://arxiv.org/abs/2610.16066) | - |

**Dense video captioning**

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2018 | CVPR | Masked Transformer | [End-to-End Dense Video Captioning with Masked Transformer](https://arxiv.org/abs/1804.00819) | - |
| 2021 | ICCV | PDVC | [End-to-End Dense Video Captioning with Parallel Decoding](https://arxiv.org/abs/2108.07781) | [Code](https://github.com/ttengwang/PDVC) |
| 2023 | CVPR | Vid2Seq | [Vid2Seq: Large-Scale Pretraining of a Visual Language Model for Dense Video Captioning](https://arxiv.org/abs/2302.14115) | [Code](https://github.com/google-research/scenic/tree/main/scenic/projects/vid2seq) |
| 2024 | CVPR | Streaming DVC | [Streaming Dense Video Captioning](https://arxiv.org/abs/2404.01297) | [Code](https://github.com/google-research/scenic) |
| 2024 | CVPR | CM² | [Do You Remember? Dense Video Captioning with Cross-Modal Memory Retrieval](https://arxiv.org/abs/2404.07610) | [Code](https://github.com/ailab-kyunghee/CM2_DVC) |
| 2024 | CVPR | DIBS | [DIBS: Enhancing Dense Video Captioning with Unlabeled Videos via Pseudo Boundary Enrichment and Online Refinement](https://arxiv.org/abs/2404.02755) | [Code](https://github.com/haowuxc/DIBS) |
| 2025 | EMNLP Findings | MMDuet | [VideoLLM Knows When to Speak: Enhancing Time-Sensitive Video Comprehension with Video-Text Duet Interaction Format](https://arxiv.org/abs/2411.17991) | [Code](https://github.com/yellow-binary-tree/MMDuet) |
| 2025 | AAAI | HiCM² | [HiCM²: Hierarchical Compact Memory Modeling for Dense Video Captioning](https://arxiv.org/abs/2412.14585) | - |
| 2026 | ECCV | PadCaptioner | [Parallelized Autoregressive Decoding for Omni-Modal Dense Video Captioning](https://arxiv.org/abs/2607.02963) | [Code](https://github.com/showlab/PadCaptioner) |

**Region-level captioning & video referring**

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2024 | arXiv | Dense VOC | [Dense Video Object Captioning from Disjoint Supervision](https://arxiv.org/abs/2306.11729) | [Code](https://github.com/google-research/scenic/tree/main/scenic/projects/densevoc) |
| 2024 | NeurIPS | Artemis | [Artemis: Towards Referential Understanding in Complex Videos](https://arxiv.org/abs/2406.00258) | [Code](https://github.com/qiujihao19/Artemis) |
| 2024 | ECCV | Elysium | [Elysium: Exploring Object-Level Perception in Videos via MLLM](https://arxiv.org/abs/2403.16558) | [Code](https://github.com/Hon-Wong/Elysium) |
| 2025 | CVPR | VideoRefer | [VideoRefer: Advancing Spatial-Temporal Object Understanding with Video LLM](https://arxiv.org/abs/2501.00599) | [Code](https://github.com/DAMO-NLP-SG/VideoRefer) |
| 2025 | CVPR | Omni-RGPT | [Omni-RGPT: Unifying Image and Video Region-level Understanding via Token Marks](https://arxiv.org/abs/2501.08326) | [Project](https://miranheo.github.io/omni-rgpt/) |
| 2025 | ICCV | DAM | [Describe Anything: Detailed Localized Image and Video Captioning](https://arxiv.org/abs/2504.16072) | [Code](https://github.com/NVlabs/describe-anything) |
| 2026 | AAAI | CAT-V | [Caption Anything in Video: Fine-grained Object-centric Captioning via Spatiotemporal Multimodal Prompting](https://arxiv.org/abs/2504.05541) | [Code](https://github.com/yunlong10/CAT-V) |
| 2025 | NeurIPS | PAM | [Perceive Anything: Recognize, Explain, Caption, and Segment Anything in Images and Videos](https://arxiv.org/abs/2506.05302) | [Code](https://github.com/Perceive-Anything/PAM) |
| 2025 | arXiv | PixelRefer | [PixelRefer: A Unified Framework for Spatio-Temporal Object Referring with Arbitrary Granularity](https://arxiv.org/abs/2510.23603) | [Code](https://github.com/alibaba-damo-academy/PixelRefer) |
| 2025 | NeurIPS | Strefer | [Strefer: Empowering Video LLMs with Space-Time Referring and Reasoning via Synthetic Instruction Data](https://arxiv.org/abs/2509.03501) | - |
| 2025 | CVPR | VideoGLaMM | [VideoGLaMM: A Large Multimodal Model for Pixel-Level Visual Grounding in Videos](https://arxiv.org/abs/2411.04923) | [Code](https://github.com/mbzuai-oryx/VideoGLaMM) |
| 2025 | arXiv | VoCap | [VoCap: Video Object Captioning and Segmentation from Any Prompt](https://arxiv.org/abs/2508.21809) | - |
| 2026 | CVPR | CaptionFormer | [CaptionFormer: Unified Segmentation, Tracking, and Captioning for Spatio-Temporal Objects](https://arxiv.org/abs/2510.14904) | [Code](https://github.com/gabfstr/CaptionFormer) |
| 2026 | ECCV | MotionAtlas | [MotionAtlas: Detailed Region Captioning for Motion-Centric Videos](https://arxiv.org/abs/2606.29531) | [Project](https://kagura-0001.github.io/projects/MotionAtlas/) |
| 2026 | arXiv | RefCaptioner | [RefCaptioner: Multi-Reference Image-Grounded Video Captioning](https://arxiv.org/abs/2607.28509) | [Code](https://github.com/pkucs-Ltf/RefCaptioner) |

### 1.3 Audio-Visual Watching

Omni-modal perception unifying speech, environmental audio, and music with visual streams under a shared LLM backbone.

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2026 | ICLR | OmniCaptioner | [OmniCaptioner: One Captioner to Rule Them All](https://arxiv.org/abs/2504.07089) | [Code](https://github.com/Alpha-Innovator/OmniCaptioner) |
| 2026 | ICLR | OmniVinci | [OmniVinci: Enhancing Architecture and Data for Omni-Modal Understanding LLM](https://arxiv.org/abs/2510.15870) | [Code](https://github.com/NVlabs/OmniVinci) |
| 2025 | arXiv | Qwen2.5-Omni | [Qwen2.5-Omni Technical Report](https://arxiv.org/abs/2503.20215) | [Code](https://github.com/QwenLM/Qwen2.5-Omni) |
| 2025 | arXiv | Qwen3-Omni | [Qwen3-Omni Technical Report](https://arxiv.org/abs/2509.17765) | - |
| 2025 | arXiv | Ming-Omni | [Ming-Omni: A Unified Multimodal Model for Perception and Generation](https://arxiv.org/abs/2506.09344) | [Code](https://github.com/inclusionAI/Ming) |
| 2024 | arXiv | Baichuan-Omni | [Baichuan-Omni Technical Report](https://arxiv.org/abs/2410.08565) | [Code](https://github.com/westlake-baichuan-mllm/bc-omni) |
| 2025 | ICLR | LLaMA-Omni | [LLaMA-Omni: Seamless Speech Interaction with Large Language Models](https://arxiv.org/abs/2409.06666) | [Code](https://github.com/ictnlp/LLaMA-Omni) |
| 2025 | ACL | LLaMA-Omni2 | [LLaMA-Omni2: LLM-based Real-time Spoken Chatbot with Autoregressive Streaming Speech Synthesis](https://arxiv.org/abs/2505.02625) | - |
| 2025 | arXiv | Stream-Omni | [Stream-Omni: Simultaneous Multimodal Interactions with Large Language-Vision-Speech Model](https://arxiv.org/abs/2506.13642) | [Code](https://github.com/ictnlp/Stream-Omni) |
| 2025 | arXiv | Megrez-Omni | [Megrez-Omni Technical Report](https://arxiv.org/abs/2502.15803) | - |
| 2025 | arXiv | InteractiveOmni | [InteractiveOmni: A Unified Omni-Modal Model for Audio-Visual Multi-Turn Dialogue](https://arxiv.org/abs/2510.13747) | - |
| 2026 | ACL Findings | Omni-R1 | [Omni-R1: Towards the Unified Generative Paradigm for Multimodal Reasoning](https://arxiv.org/abs/2601.09536) | - |
| 2026 | arXiv | Script-a-Video | [Script-a-Video: Deep Structured Audio-visual Captions via Factorized Streams and Relational Grounding](https://arxiv.org/abs/2604.11244) | - |
| 2026 | arXiv | AVCap | [AVCap: Reinforcing Audio-Video Joint Caption with Detail-Aware Reward](https://arxiv.org/abs/2608.06930) | - |
| 2026 | arXiv | OmniReasoning | [OmniReasoning: Pushing the Limits of Audio-Visual Joint Reasoning](https://arxiv.org/abs/2609.39490) | [Code](https://github.com/PKU-VaLuE-Lab/OmniReasoning) |
| 2026 | arXiv | — | [Exploring Audio Hallucination in Egocentric Video Understanding](https://arxiv.org/abs/2604.23860) | - |
| 2026 | arXiv | Audio-Visual Flamingo | [Audio-Visual Flamingo: Open Audio-Visual Intelligence for Long and Complex Videos](https://arxiv.org/abs/2607.16107) | [Project](https://avflamingo.pages.dev/) |
| 2026 | arXiv | OmniVChat | [OmniVChat: Synthesizing, Benchmarking, and Training for Native Audio-Visual Dialogue](https://arxiv.org/abs/2609.21465) | [Code](https://github.com/HarlandZZC/OmniVChat) |

### 1.4 Efficient Watching

Reducing redundancy in long videos: frame-level selection, token-level compression / merging, and model-level efficient processing.

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2024 | NeurIPS | VideoLLM-MoD | [VideoLLM-MoD: Efficient Video-Language Streaming with Mixture-of-Depths Vision Computation](https://arxiv.org/abs/2408.16730) | - |
| 2025 | CVPR | AKS | [Adaptive Keyframe Sampling for Long Video Understanding](https://arxiv.org/abs/2502.21271) | [Code](https://github.com/ncTimTang/AKS) |
| 2025 | ICCV | Q-Frame | [Q-Frame: Query-aware Frame Selection and Multi-Resolution Adaptation for Video-LLMs](https://arxiv.org/abs/2506.22139) | [Code](https://github.com/xiaomi-research/q-frame) |
| 2025 | NeurIPS | Logic-in-Frames | [Logic-in-Frames: Dynamic Keyframe Search via Visual Semantic-Logical Verification for Long Video Understanding](https://arxiv.org/abs/2503.13139) | - |
| 2025 | arXiv | DIG | [Divide, then Ground: Adapting Frame Selection to Query Types for Long-Form Video Understanding](https://arxiv.org/abs/2512.04000) | - |
| 2026 | CVPR Findings | ReFoCUS | [ReFoCUS: Reinforcement-guided Frame Optimization for Contextual Understanding](https://arxiv.org/abs/2506.01274) | - |
| 2025 | arXiv | FrameOracle | [FrameOracle: Learning What to See and How Much to See in Videos](https://arxiv.org/abs/2510.03584) | - |
| 2025 | arXiv | F2C | [From Frames to Clips: Efficient Key Clip Selection for Long-Form Video Understanding](https://arxiv.org/abs/2510.02262) | - |
| 2025 | arXiv | K-Frames | [K-frames: Scene-Driven Any-k Keyframe Selection for long video understanding](https://arxiv.org/abs/2510.13891) | - |
| 2025 | ICCV | FrameFusion | [FrameFusion: Combining Similarity and Importance for Video Token Reduction on Large Vision Language Models](https://arxiv.org/abs/2501.01986) | [Code](https://github.com/thu-nics/FrameFusion) |
| 2025 | CVPR | DyCoke | [DyCoke: Dynamic Compression of Tokens for Fast Video Large Language Models](https://arxiv.org/abs/2411.15024) | [Code](https://github.com/KD-TAO/DyCoke) |
| 2025 | NeurIPS | HoliTom | [HoliTom: Holistic Token Merging for Fast Video Large Language Models](https://arxiv.org/abs/2505.21334) | - |
| 2025 | EMNLP | VidCom² | [Video Compression Commander: Plug-and-Play Inference Acceleration for Video Large Language Models](https://arxiv.org/abs/2505.14454) | [Code](https://github.com/xuyang-liu16/VidCom2) |
| 2025 | EMNLP | LangDC | [Seeing More, Saying More: Lightweight Language Experts are Dynamic Video Token Compressors](https://arxiv.org/abs/2509.00969) | - |
| 2025 | NeurIPS | DyToK | [Less Is More, but Where? Dynamic Token Compression via LLM-Guided Keyframe Prior](https://arxiv.org/abs/2512.06866) | [Code](https://github.com/yu-lin-li/DyToK) |
| 2025 | ACL Findings | AdaReTaKe | [AdaReTaKe: Adaptive Redundancy Reduction to Perceive Longer for Video-language Understanding](https://arxiv.org/abs/2503.12559) | - |
| 2025 | arXiv | Video-XL-2 | [Video-XL-2: Towards Very Long-Video Understanding Through Task-Aware KV Sparsification](https://arxiv.org/abs/2506.19225) | [Project](https://unabletousegit.github.io/video-xl2.github.io/) |
| 2026 | ICLR | VideoNSA | [VideoNSA: Native Sparse Attention Scales Video Understanding](https://arxiv.org/abs/2510.02295) | [Code](https://github.com/Espere-1119-Song/VideoNSA) |
| 2026 | NeurIPS | FrameScout | [FrameScout: Scouting Query-Relevant Frames for Long Video Understanding](https://arxiv.org/abs/2610.23975) | [Code](https://github.com/Hubert-1102/FrameScout) |
| 2026 | arXiv | FramePack-U | [Elephant in the Fridge: Constant-Memory Frame Packing for Long Video Understanding](https://arxiv.org/abs/2610.16118) | [Project](https://zeld0n.github.io/framepack-U/) |
| 2026 | arXiv | VisualRouter | [VisualRouter: Query-Grounded Visual Sampling for Long Video Understanding](https://arxiv.org/abs/2607.28463) | - |
| 2026 | CVPR | AOT | [Token Reduction via Local and Global Contexts Optimization for Efficient Video Large Language Models](https://arxiv.org/abs/2603.01400) | [Code](https://github.com/TyroneLi/AOT) |
| 2026 | CVPR | AutoGaze | [Attend Before Attention: Efficient and Scalable Video Understanding via Autoregressive Gazing](https://arxiv.org/abs/2603.12254) | [Code](https://github.com/NVlabs/AutoGaze) |
| 2026 | arXiv | HiMu | [HiMu: Hierarchical Multimodal Frame Selection for Long Video Question Answering](https://arxiv.org/abs/2603.18558) | [Code](https://github.com/DanBenAmi/HiMu) |
| 2026 | arXiv | CodecSight | [CodecSight: Leveraging Video Codec Signals for Efficient Streaming VLM Inference](https://arxiv.org/abs/2604.06036) | - |
| 2026 | arXiv | LiteFrame | [LiteFrame: Efficient Vision Encoders Unlock Frame Scaling in Video LLMs](https://arxiv.org/abs/2605.17260) | [Code](https://github.com/jjihwan/LiteFrame) |
| 2026 | CVPR | EarlyTom | [EarlyTom: Early Token Compression Completes Fast Video Understanding](https://arxiv.org/abs/2605.30010) | [Code](https://github.com/viridisGreen/EarlyTom) |
| 2026 | ECCV | — | [Linear Scaling Video VLMs for Long Video Understanding](https://arxiv.org/abs/2605.31598) | - |
| 2026 | arXiv | AdaCodec | [AdaCodec: A Predictive Visual Code for Video MLLMs](https://arxiv.org/abs/2606.02569) | [Project](https://haowenhou.github.io/AdaCodec-Page/) |
| 2026 | arXiv | OmniFocus | [OmniFocus: Query-Guided Modality-Balanced Token Compression for Omni-Modal Large Language Models](https://arxiv.org/abs/2607.03050) | - |
| 2026 | arXiv | EcoFrame | [When and Where to Look: Adaptive Visual Evidence Scheduling for Efficient Long Video Understanding](https://arxiv.org/abs/2608.03918) | - |
| 2026 | arXiv | AVIOT | [Aggregating Visual Information with Optimal Transport for VideoLM Token Compression](https://arxiv.org/abs/2608.20473) | - |
| 2026 | arXiv | — | [Select, Compress, Reinvest: A Controlled Study of Visual-Token Allocation in Long-Video MLLMs](https://arxiv.org/abs/2609.03820) | [Code](https://github.com/codeprakhar25/omp-keyframe-sampling) |
| 2026 | arXiv | — | [Rethinking Visual Token Compression for Video Large Language Models: A Simple Yet Strong Baseline](https://arxiv.org/abs/2609.35394) | - |
| 2026 | arXiv | RESUME | [RESUME: Recurrent State Updates from Motion and Residual Signals for Efficient Video Language Modeling](https://arxiv.org/abs/2609.39563) | - |
| 2026 | arXiv | CoVisco | [CoVisco: Codec-Native Vision Encoder with Native Token Compression for Unified Image-Video Understanding](https://arxiv.org/abs/2609.39924) | - |
| 2026 | NeurIPS | LoHi | [Rethinking Long-Video Efficiency: A Joint Allocation Perspective on Frames, Pixels, and Front-End Latency](https://arxiv.org/abs/2610.04318) | [Code](https://github.com/Ironieser/LongVideo-Eval) |
| 2026 | arXiv | OmniScope | [OmniScope: Modality-Decoupled Token Compression for Omnimodal Large Language Models](https://arxiv.org/abs/2607.23193) | [Code](https://github.com/MAC-AutoML/OmniScope) |
| 2026 | arXiv | Omni-Prune | [Omni-Prune: Query-Aware Unified Token Pruning for Efficient Omnimodal Large Language Models](https://arxiv.org/abs/2607.23445) | - |
| 2026 | arXiv | EgoGazeLite | [EgoGazeLite: On-Device Egocentric Gaze Prediction for Token-Efficient Multimodal LLM Video Input](https://arxiv.org/abs/2608.15614) | - |
| 2026 | arXiv | OmniRoute | [OmniRoute: Mapping Temporal Semantic Evidence to Audio-Visual Token Budgets for Efficient Omnimodal Large Language Models](https://arxiv.org/abs/2609.37052) | - |
| 2026 | arXiv | Video Encoders | [Video Encoders Built on Image Representations](https://arxiv.org/abs/2610.06616) | - |

---

## 2. Remember — How to Remember?

Memory connects perception with higher-level understanding by retaining salient information over time. We split methods by storage paradigm.

### 2.1 Offline Memory — Agentic

LLMs/VLMs autonomously invoke memory tools through multi-round reasoning to construct and retrieve memory.

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2024 | NeurIPS | AVUA | [Adaptive Video Understanding Agent: Enhancing Efficiency with Dynamic Frame Sampling and Feedback-driven Reasoning](https://arxiv.org/abs/2410.20252) | - |
| 2024 | ECCV | VideoAgent | [VideoAgent: A Memory-augmented Multimodal Agent for Video Understanding](https://arxiv.org/abs/2403.11481) | [Code](https://github.com/YueFan1014/VideoAgent) |
| 2025 | ICCV | LVAgent | [LVAgent: Long Video Understanding by Multi-Round Dynamical Collaboration of MLLM Agents](https://arxiv.org/abs/2503.10200) | [Code](https://github.com/64327069/LVAgent) |
| 2025 | NeurIPS | AdaVideoRAG | [AdaVideoRAG: Omni-Contextual Adaptive Retrieval-Augmented Efficient Long Video Understanding](https://arxiv.org/abs/2506.13589) | [Code](https://github.com/xzc-zju/AdaVideoRAG) |
| 2025 | NeurIPS | VideoLucy | [VideoLucy: Deep Memory Backtracking for Long Video Understanding](https://arxiv.org/abs/2510.12422) | [Code](https://github.com/Zplusdragon/VideoLucy) |
| 2026 | TMM | GCAgent | [GCAgent: Long-Video Understanding via Schematic and Narrative Episodic Memory](https://arxiv.org/abs/2511.12027) | - |
| 2026 | ACL | EGAgent | [Agentic Very Long Video Understanding](https://arxiv.org/abs/2601.18157) | - |
| 2026 | ICLR | MemGen | [MemGen: Weaving Generative Latent Memory for Self-Evolving Agents](https://arxiv.org/abs/2509.24704) | [Code](https://github.com/KANABOON1/MemGen) |
| 2026 | ICLR | M3-Agent | [Seeing, Listening, Remembering, and Reasoning: A Multimodal Agent with Long-Term Memory](https://arxiv.org/abs/2508.09736) | [Code](https://github.com/ByteDance-Seed/m3-agent) |
| 2026 | arXiv | Homer | [Homer: Understanding Long-form Videos with Hierarchical Memory and Agentic Reasoning](https://arxiv.org/abs/2607.02588) | - |
| 2026 | arXiv | MemLife | [MemLife: Curating and Reasoning over Long-Term Egocentric Video Memories](https://arxiv.org/abs/2609.40195) | - |
| 2026 | arXiv | MAGIC-Video | [Bridging Modalities, Spanning Time: Structured Memory for Ultra-Long Agentic Video Reasoning](https://arxiv.org/abs/2605.08271) | - |
| 2026 | arXiv | MemDreamer | [MemDreamer: Decoupling Perception and Reasoning for Long Video Understanding via Hierarchical Graph Memory and Agentic Retrieval Mechanism](https://arxiv.org/abs/2606.07512) | [Project](https://aim-uofa.github.io/MemDreamer/) |
| 2026 | ECCV | MERIT | [Keep It Simple: Multi-Key Episodic Memory Retrieval for Ultra-Long Video Understanding](https://arxiv.org/abs/2608.07663) | [Code](https://github.com/choi-yeeun/MERIT) |
| 2026 | arXiv | Sprout | [Sprout: Building Dynamic Memory While Reasoning for Agentic Video Understanding](https://arxiv.org/abs/2609.35497) | - |
| 2026 | arXiv | VideoLoop | [VideoLoop: Looped Working Memory Against Semantic Thrashing in Long-Form Video Agents](https://arxiv.org/abs/2609.38119) | [Code](https://github.com/philipxjm/videoloop) |
| 2026 | arXiv | ReflectWorld-MM | [ReflectWorld-MM: An Entity-Oriented Multimodal Memory System for Open-Ended Video Streams](https://arxiv.org/abs/2607.09759) | [Code](https://github.com/addxai/ReflectWorld) |

### 2.2 Offline Memory — Non-Agent

Deterministic pipelines where memory construction and retrieval are sequential, fixed stages.

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2024 | CVPR | MovieChat | [MovieChat: From Dense Token to Sparse Memory for Long Video Understanding](https://arxiv.org/abs/2307.16449) | [Code](https://github.com/rese1f/MovieChat) |
| 2024 | CVPR | MA-LMM | [MA-LMM: Memory-Augmented Large Multimodal Model for Long-Term Video Understanding](https://arxiv.org/abs/2404.05726) | [Code](https://github.com/boheumd/MA-LMM) |
| 2024 | arXiv | VidCompress | [VidCompress: Memory-Enhanced Temporal Compression for Video Understanding in Large Language Models](https://arxiv.org/abs/2410.11417) | - |
| 2025 | CVPR | ReWind | [ReWind: Understanding Long Videos with Instructed Learnable Memory](https://arxiv.org/abs/2411.15556) | - |
| 2025 | ICME | HEM-LLM | [Enhancing Long Video Understanding via Hierarchical Event-Based Memory](https://arxiv.org/abs/2409.06299) | - |
| 2025 | ICML | ∞-Video | [∞-Video: A Training-Free Approach to Long Video Understanding via Continuous-Time Memory Consolidation](https://arxiv.org/abs/2501.19098) | [Code](https://github.com/deep-spin/Infinite-Video) |
| 2025 | ICML | LongVU | [LongVU: Spatiotemporal Adaptive Compression for Long Video-Language Understanding](https://arxiv.org/abs/2410.17434) | [Code](https://github.com/Vision-CAIR/LongVU) |
| 2025 | ICCV | VideoLLaMB | [VideoLLaMB: Long Streaming Video Understanding with Recurrent Memory Bridges](https://arxiv.org/abs/2409.01071) | [Code](https://github.com/bigai-nlco/VideoLLaMB) |
| 2025 | ICCV | HERMES | [HERMES: Temporal-Coherent Long-Form Understanding with Episodes and Semantics](https://arxiv.org/abs/2408.17443) | [Code](https://github.com/joslefaure/HERMES) |
| 2025 | CVPR | HierarQ | [HierarQ: Task-Aware Hierarchical Q-Former for Enhanced Video Understanding](https://arxiv.org/abs/2503.08585) | [Project](https://sacrcv.github.io/HierarQ-website/) |
| 2025 | arXiv | MemVid | [Memory-enhanced Retrieval Augmentation for Long Video Understanding](https://arxiv.org/abs/2503.09149) | - |
| 2026 | ICLR | MARC | [MARC: Memory-Augmented RL Token Compression for Efficient Video Understanding](https://arxiv.org/abs/2510.07915) | - |
| 2026 | EACL Findings | See More, Store Less | [See More, Store Less: Memory-Efficient Resolution for Video Moment Retrieval](https://arxiv.org/abs/2601.09350) | - |
| 2026 | WACV | Compact Video Reps | [Learning Compact Video Representations for Efficient Long-Form Video Understanding in Large Multimodal Models](https://arxiv.org/abs/2602.17869) | - |
| 2026 | CVPR | QViC-MF | [Question-guided Visual Compression with Memory Feedback for Long-Term Video Understanding](https://arxiv.org/abs/2603.15167) | - |
| 2026 | CVPR | FlexMem | [Scaling the Long Video Understanding of Multimodal Large Language Models via Visual Memory Mechanism](https://arxiv.org/abs/2603.29252) | [Code](https://github.com/city1517/FlexMem) |
| 2026 | ECCV | ReMem | [Reasoning with Memory: A Temporal Granularity-Adaptive Framework for Training-Free Long Video Understanding](https://arxiv.org/abs/2607.24794) | - |
| 2026 | ECCV | Tempo | [Small Vision-Language Models are Smart Compressors for Long Video Understanding](https://arxiv.org/abs/2604.08120) | [Code](https://github.com/FeiElysia/Tempo) |
| 2026 | arXiv | PyraVid | [PyraVid: Hierarchical Multimodal Memory for Long-Horizon Video Reasoning](https://arxiv.org/abs/2605.17065) | - |
| 2026 | arXiv | Q-GeoMem | [Q-GeoMem: Question-Guided Geometric Memory for Video Spatial Reasoning](https://arxiv.org/abs/2605.27318) | [Code](https://github.com/Q-GeoMem/Q-GeoMem) |
| 2026 | arXiv | LongSpace | [LongSpace: Exploring Long-Horizon Spatial Memory from Perception to Recall in Video](https://arxiv.org/abs/2606.05677) | - |

### 2.3 Streaming Memory

Processing unbounded streams within fixed memory budgets via causal compression, KV pruning, sink reuse, or hierarchical caches.

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2024 | NeurIPS | VideoStreaming | [Streaming Long Video Understanding with Large Language Models](https://arxiv.org/abs/2405.16009) | - |
| 2024 | arXiv | Flash-VStream | [Flash-VStream: Memory-Based Real-Time Understanding for Long Video Streams](https://arxiv.org/abs/2406.08085) | [Code](https://github.com/IVGSZ/Flash-VStream) |
| 2025 | ICLR | StreamChat | [Streaming Video Understanding and Multi-round Interaction with Memory-enhanced Knowledge](https://arxiv.org/abs/2501.13468) | [Code](https://github.com/hmxiong/StreamChat) |
| 2025 | arXiv | LiveVLM | [LiveVLM: Efficient Online Video Understanding via Streaming-Oriented KV Cache and Retrieval](https://arxiv.org/abs/2505.15269) | - |
| 2025 | arXiv | QuickVideo | [QuickVideo: Real-Time Long Video Understanding with System Algorithm Co-Design](https://arxiv.org/abs/2505.16175) | - |
| 2025 | NeurIPS | StreamBridge | [StreamBridge: Turning Your Offline Video Large Language Model into a Proactive Streaming Assistant](https://arxiv.org/abs/2505.05467) | - |
| 2025 | NeurIPS | ReKV | [Recurrent Attention-based Token Selection for Efficient Streaming Video-LLMs](https://arxiv.org/abs/2510.17364) | [Code](https://github.com/Becomebright/ReKV) |
| 2025 | ICCV | ProVideLLM | [Memory-efficient Streaming VideoLLMs for Real-time Procedural Video Understanding](https://arxiv.org/abs/2504.13915) | [Project](https://dibschat.github.io/ProVideLLM/) |
| 2025 | NeurIPS | InfiniPot-V | [InfiniPot-V: Memory-Constrained KV Cache Compression for Streaming Video Understanding](https://arxiv.org/abs/2506.15745) | [Code](https://github.com/aiha-lab/InfiniPot-V) |
| 2025 | arXiv | StreamMem | [StreamMem: Query-Agnostic KV Cache Memory for Streaming Video Understanding](https://arxiv.org/abs/2508.15717) | [Project](https://yanlai00.github.io/streammem/) |
| 2025 | NeurIPS | StreamForest | [StreamForest: Efficient Online Video Understanding with Persistent Event Memory](https://arxiv.org/abs/2509.24871) | - |
| 2026 | arXiv | video-SALMONN S | [video-SALMONN S: Streaming Audio-Visual LLMs Beyond Length Limits via Memory](https://arxiv.org/abs/2510.11129) | - |
| 2026 | ICLR | StreamingVLM | [StreamingVLM: Real-Time Understanding for Infinite Video Streams](https://arxiv.org/abs/2510.09608) | [Code](https://github.com/mit-han-lab/streaming-vlm) |
| 2025 | CVPR | VideoChat-Online | [Online Video Understanding: OVBench and VideoChat-Online](https://arxiv.org/abs/2501.00584v2) | [Project](https://videochat-online.github.io/) |
| 2026 | arXiv | CurveStream | [CurveStream: Boosting Streaming Video Understanding in MLLMs via Curvature-Aware Hierarchical Visual Memory Management](https://arxiv.org/abs/2603.19571) | [Code](https://github.com/streamingvideos/CurveStream) |
| 2026 | arXiv | SyncPro | [SyncPro: Synchronous Reasoning and Responding for Proactive Streaming Video Understanding](https://arxiv.org/abs/2610.32132) | - |
| 2026 | ACL Findings | StreamMeCo | [StreamMeCo: Long-Term Agent Memory Compression for Efficient Streaming Video Understanding](https://arxiv.org/abs/2604.09000) | [Code](https://github.com/Celina-love-sweet/StreamMeCo) |
| 2026 | CVPR | StreamReady | [StreamReady: Learning What to Answer and When in Long Streaming Videos](https://arxiv.org/abs/2603.08620) | [Code](https://github.com/sacrcv/StreamReady) |
| 2026 | ECCV | Think While Watching | [Think While Watching: Online Streaming Segment-Level Memory for Multi-Turn Video Reasoning in Multimodal Large Language Models](https://arxiv.org/abs/2603.11896) | [Code](https://github.com/wl666hhh/Think_While_Watching) |
| 2026 | ECCV | VST | [Video Streaming Thinking: VideoLLMs Can Watch and Think Simultaneously](https://arxiv.org/abs/2603.12262) | [Code](https://github.com/1ranGuan/VST) |
| 2026 | arXiv | ThinkStream | [Thinking in Streaming Video](https://arxiv.org/abs/2603.12938) | - |
| 2026 | arXiv | WAT | [WAT: Online Video Understanding Needs Watching Before Thinking](https://arxiv.org/abs/2603.13412) | - |
| 2026 | arXiv | PEARL | [PEARL: Personalized Streaming Video Understanding Model](https://arxiv.org/abs/2603.20422) | - |
| 2026 | arXiv | STRIDE | [STRIDE: When to Speak Meets Sequence Denoising for Streaming Video Understanding](https://arxiv.org/abs/2603.27593) | [Code](https://github.com/interlive-team/STRIDE) |
| 2026 | arXiv | SimpleStream | [A Simple Baseline for Streaming Video Understanding](https://arxiv.org/abs/2604.02317) | [Code](https://github.com/EvolvingLMMs-Lab/SimpleStream) |
| 2026 | arXiv | AURA | [AURA: Always-On Understanding and Real-Time Assistance via Video Streams](https://arxiv.org/abs/2604.04184) | [Code](https://github.com/aurateam2026/AURA) |
| 2026 | arXiv | DSCache | [Decouple and Cache: KV Cache Construction for Streaming Video Understanding](https://arxiv.org/abs/2605.01858) | - |
| 2026 | arXiv | — | [Semantic-Aware Adaptive Visual Memory for Streaming Video Understanding](https://arxiv.org/abs/2605.07897) | - |
| 2026 | CVPR | MuKV | [MuKV: Multi-Grained KV Cache Compression for Long Streaming Video Question-Answering](https://arxiv.org/abs/2605.22269) | - |
| 2026 | arXiv | StreamOV | [StreamOV: Streaming Omni-Video Understanding via Evidence-Guided Memory and Response Triggering](https://arxiv.org/abs/2605.25621) | - |
| 2026 | arXiv | LiveStarPro | [LiveStarPro: Proactive Streaming Video Understanding with Hierarchical Memory for Long-Horizon Streams](https://arxiv.org/abs/2606.17798) | - |
| 2026 | ICML | ProtoKV | [ProtoKV: Streaming Video Understanding under Delayed Query with Summary-State Memory](https://arxiv.org/abs/2606.26762) | - |
| 2026 | arXiv | Stream3D-VLM | [Stream3D-VLM: Online 3D Spatial Understanding with Incremental Geometry Priors](https://arxiv.org/abs/2606.06891) | [Code](https://github.com/hanxunyu/Stream3D-VLM) |
| 2026 | ECCV | — | [Forget, Anticipate and Adapt: Test Time Training for Long Videos](https://arxiv.org/abs/2606.26515) | - |
| 2026 | arXiv | Light-Omni | [Light-Omni: Reflex over Reasoning in Agentic Video Understanding with Long-Term Memory](https://arxiv.org/abs/2607.05511) | [Code](https://github.com/Clare-Nie/Light-Omni) |
| 2026 | arXiv | FOLIO | [FOLIO: Focused Semantic Memory for Streaming Video Understanding](https://arxiv.org/abs/2607.13298) | - |
| 2026 | arXiv | StreamTTT | [StreamTTT: Reconciling Real-Time Perception and Long-Term Memory in Streaming VLMs](https://arxiv.org/abs/2608.13416) | - |
| 2026 | arXiv | StreamOPD | [StreamOPD: A Post-Training Recipe with Spatio-Temporal Cue Gating for Streaming Video Understanding](https://arxiv.org/abs/2608.16320) | [Code](https://github.com/UniX-AI-Lab/StreamOPD) |
| 2026 | arXiv | StreamScout | [StreamScout: Learning When to Look Deeper for Streaming Video Understanding](https://arxiv.org/abs/2609.00291) | - |
| 2026 | arXiv | ShallowStream | [ShallowStream: Index Shallow then Answer Deep for Streaming Video Understanding](https://arxiv.org/abs/2609.02780) | [Code](https://github.com/CURRENTF/ShallowStream) |
| 2026 | arXiv | LatentStream | [Beyond Retrieval: Progressive Latent Memory Evolution for Streaming Video Understanding](https://arxiv.org/abs/2609.04131) | [Code](https://github.com/quhongyu/LatentStream) |
| 2026 | arXiv | OST | [Omni-Streaming Thinking](https://arxiv.org/abs/2609.15128) | [Project](https://enjundu.com/blog/ost/) |
| 2026 | arXiv | FlashBack | [FlashBack: Knowing When to Remember in Streaming Vision-Language Models](https://arxiv.org/abs/2610.01192) | - |
| 2026 | arXiv | OneStreamer | [OneStreamer: Unifying Perception, Memory, and Proactive Response in Streaming Video Interaction](https://arxiv.org/abs/2610.01762) | [Code](https://github.com/MCG-NJU/OneStreamer) |
| 2026 | arXiv | Foresight | [Foresight: planning future perception in streaming VLMs without retraining](https://arxiv.org/abs/2610.03123) | [Code](https://github.com/thenaivekid/foresight) |
| 2026 | arXiv | SPARE | [SPARE: Shared Perception and Adaptive Retrieval of Evidence for Streaming Video Understanding](https://arxiv.org/abs/2610.14671) | - |
| 2026 | arXiv | DeltaStreamer | [DeltaStreamer: Towards Human-Like Agentic Streaming Video Understanding](https://arxiv.org/abs/2610.19849) | [Code](https://github.com/BBBBchan/DeltaStreamer) |
| 2026 | arXiv | Streaming Harness | [Harnessing Streaming Video in the Wild](https://arxiv.org/abs/2606.08615) | - |
| 2026 | ECCV | GuideMe | [GuideMe: Multi-Domain Task Guidance and Intervention in Streaming Video](https://arxiv.org/abs/2607.02991) | - |
| 2026 | arXiv | Live Assistant | [Live Assistant: Learning Whether, When, and Whom to Assist in Real-World Live Social Streams](https://arxiv.org/abs/2609.27303) | - |
| 2026 | arXiv | VideoJev | [VideoJev: System One Model for Video Understanding and Interaction](https://arxiv.org/abs/2610.18615) | [Code](https://github.com/MCG-NJU/VideoJev) |
---

## 3. Reason — How to Reason?

Reasoning operates on perceived and retained evidence. We separate models by *what* they reason over (text-only vs. interleaved with visual evidence) and *how* the reasoning is controlled (agentic tool loops vs. non-agent post-training).

### 3.1 Text-only Reasoning — Agentic

Agent loops with tools / memory / planning that orchestrate perception, retrieval, verification, and reflection.

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2024 | ECCV | VideoAgent | [VideoAgent: A Memory-augmented Multimodal Agent for Video Understanding](https://arxiv.org/abs/2403.11481) | [Code](https://github.com/YueFan1014/VideoAgent) |
| 2024 | ICML | DoraemonGPT | [DoraemonGPT: Toward Understanding Dynamic Scenes with Large Language Models](https://arxiv.org/abs/2401.08392) | [Code](https://github.com/z-x-yang/DoraemonGPT) |
| 2024 | ICML | VoT | [Video-of-Thought: Step-by-Step Video Reasoning from Perception to Cognition](https://arxiv.org/abs/2501.03230) | [Code](https://github.com/scofield7419/Video-of-Thought) |
| 2026 | KDD | VideoRAG | [VideoRAG: Retrieval-Augmented Generation with Extreme Long-Context Videos](https://arxiv.org/abs/2502.01549) | [Code](https://github.com/HKUDS/VideoRAG) |
| 2025 | arXiv | VideoMind | [VideoMind: A Chain-of-LoRA Agent for Long Video Reasoning](https://arxiv.org/abs/2503.13444) | - |
| 2025 | ICCV | VCA | [VCA: Video Curious Agent for Long Video Understanding](https://arxiv.org/abs/2412.10471) | - |
| 2025 | ICCV | Flow4Agent | [Flow4Agent: Long-form Video Understanding via Motion Prior from Optical Flow](https://arxiv.org/abs/2510.05836) | - |
| 2025 | NeurIPS | DVD | [Deep Video Discovery: Agentic Search with Tool Use for Long-form Video Understanding](https://arxiv.org/abs/2505.18079) | [Code](https://github.com/microsoft/DeepVideoDiscovery) |
| 2025 | NeurIPS | VideoAgent2 | [VideoAgent2: Enhancing the LLM-Based Agent System for Long-Form Video Understanding by Uncertainty-Aware CoT](https://arxiv.org/abs/2504.04471) | - |
| 2025 | arXiv | CoT-Vid | [CoT-Vid: Dynamic Chain-of-Thought Routing with Self Verification for Training-Free Video Reasoning](https://arxiv.org/abs/2505.11830) | - |
| 2026 | VISAPP | ViQAgent | [ViQAgent: Zero-Shot Video Question Answering via Agent with Open-Vocabulary Grounding Validation](https://arxiv.org/abs/2505.15928) | - |
| 2025 | arXiv | Video-in-the-loop | [Video-in-the-loop: Span-grounded Long Video QA with Interleaved Reasoning](https://arxiv.org/abs/2510.04022) | - |
| 2025 | NeurIPS | Vgent | [Vgent: Graph-based Retrieval-Reasoning-Augmented Generation For Long Video Understanding](https://arxiv.org/abs/2510.14032) | [Project](https://xiaoqian-shen.github.io/Vgent/) |
| 2025 | arXiv | StreamAgent | [StreamAgent: Towards Anticipatory Agents for Streaming Video Understanding](https://arxiv.org/abs/2508.01875) | - |
| 2026 | arXiv | VideoDetective | [VideoDetective: Clue Hunting via both Extrinsic Query and Intrinsic Relevance for Long Video Understanding](https://arxiv.org/abs/2603.22285) | [Code](https://github.com/yangruoliu/VideoDetective) |
| 2026 | CVPR | EVA | [EVA: Efficient Reinforcement Learning for End-to-End Video Agent](https://arxiv.org/abs/2603.22918) | [Code](https://github.com/wangruohui/EfficientVideoAgent) |
| 2026 | arXiv | ToolMerge | [Decomposing Queries into Tool Calls for Long-Video Keyframe Retrieval](https://arxiv.org/abs/2605.23826) | [Code](https://github.com/michalsr/ToolMerge) |
| 2026 | arXiv | Robust-TO | [Confidence-Aware Tool Orchestration for Robust Video Understanding](https://arxiv.org/abs/2606.26904) | [Code](https://github.com/ROVA-V2/Robust-TO) |
| 2026 | arXiv | TRACE | [TRACE: Evidence Grounding-Guided Multi-Video Event Understanding and Claim Generation](https://arxiv.org/abs/2605.16740) | - |
| 2026 | arXiv | DynFrame | [DynFrame: Adaptive Reasoning-Driven Multimodal Framework with Dynamic Frame Augmentation for Complex Video Understanding](https://arxiv.org/abs/2605.26680) | - |
| 2026 | arXiv | AgentCVR | [AgentCVR: Active Multi-Agent Cross-Video Reasoning via Script-Simulated Reinforcement Learning](https://arxiv.org/abs/2605.29643) | - |
| 2026 | ECCV | VideoSearch-R1 | [VideoSearch-R1: Iterative Video Retrieval and Reasoning via Soft Query Refinement](https://arxiv.org/abs/2607.00446) | [Code](https://github.com/mlvlab/VideoSearch-R1) |
| 2026 | arXiv | OmniReasoner | [OmniReasoner: Thinking with Long Audio-Video via Native Tool Use](https://arxiv.org/abs/2607.19339) | - |

### 3.2 Text-only Reasoning — Non-Agent

CoT-style supervised fine-tuning and RL/DPO post-training without tool-driven control loops.

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2025 | arXiv | Chain-of-Frames | [Chain-of-Frames: Advancing Video Understanding in Multimodal LLMs via Frame-Aware Reasoning](https://arxiv.org/abs/2506.00318) | - |
| 2025 | NeurIPS | Video-R1 | [Video-R1: Reinforcing Video Reasoning in MLLMs](https://arxiv.org/abs/2503.21776) | [Code](https://github.com/tulerfeng/Video-R1) |
| 2026 | ECCV | TW-GRPO | [Reinforcing Video Reasoning with Focused Thinking](https://arxiv.org/abs/2505.24718) | [Code](https://github.com/longmalongma/TW-GRPO) |
| 2025 | ICML | VistaDPO | [VistaDPO: Video Hierarchical Spatial-Temporal Direct Preference Optimization for Large Video Models](https://arxiv.org/abs/2504.13122) | [Code](https://github.com/HaroldChen19/VistaDPO) |
| 2025 | arXiv | VerIPO | [VerIPO: Cultivating Long Reasoning in Video-LLMs via Verifier-Guided Iterative Policy Optimization](https://arxiv.org/abs/2505.19000) | [Code](https://github.com/HITsz-TMG/VerIPO) |
| 2025 | arXiv | VidBridge-R1 | [VidBridge-R1: Bridging QA and Captioning for RL-based Video Understanding Models with Intermediate Proxy Tasks](https://arxiv.org/abs/2506.09079) | - |
| 2025 | arXiv | video-SALMONN-o1 | [video-SALMONN-o1: Reasoning-enhanced Audio-visual Large Language Model](https://arxiv.org/abs/2502.11775) | - |
| 2025 | NeurIPS | VideoRFT | [VideoRFT: Incentivizing Video Reasoning Capability in MLLMs via Reinforced Fine-Tuning](https://arxiv.org/abs/2505.12434) | [Code](https://github.com/QiWang98/VideoRFT) |
| 2025 | NeurIPS | Time-R1 | [Time-R1: Post-Training Large Vision Language Model for Temporal Video Grounding](https://arxiv.org/abs/2503.13377) | [Code](https://github.com/xiaomi-research/time-r1) |
| 2025 | NeurIPS | DeepVideo-R1 | [DeepVideo-R1: Video Reinforcement Fine-Tuning via Difficulty-aware Regressive GRPO](https://arxiv.org/abs/2506.07464) | [Code](https://github.com/mlvlab/DeepVideoR1) |
| 2025 | ACM MM | Video-CoT | [Video-CoT: A Comprehensive Dataset for Spatiotemporal Understanding of Videos Based on Chain-of-Thought](https://arxiv.org/abs/2506.08817) | [Project](https://video-cot.github.io/) |
| 2025 | arXiv | SpaceR | [SpaceR: Reinforcing MLLMs in Video Spatial Reasoning](https://arxiv.org/abs/2504.01805) | [Code](https://github.com/OuyangKun10/SpaceR) |
| 2025 | arXiv | vsGRPO | [Improved Visual-Spatial Reasoning via R1-Zero-like Training](https://arxiv.org/abs/2504.00883) | - |
| 2025 | arXiv | VIDEO-STR | [Video-STR: Reinforcing MLLMs in Video Spatio-Temporal Reasoning with Relation Graph](https://arxiv.org/abs/2510.10976) | - |
| 2025 | arXiv | SpatialLadder | [SpatialLadder: Progressive Training for Spatial Reasoning in Vision-Language Models](https://arxiv.org/abs/2510.08531) | - |
| 2025 | arXiv | Cambrian-S | [Cambrian-S: Towards Spatial Supersensing in Video](https://arxiv.org/abs/2511.04670) | - |
| 2025 | arXiv | Video-R2 | [Video-R2: Reinforcing Consistent and Grounded Reasoning in Multimodal Language Models](https://arxiv.org/abs/2511.23478) | - |
| 2026 | arXiv | VidGround | [Watch Before You Answer: Learning from Visually Grounded Post-Training](https://arxiv.org/abs/2604.05117) | [Code](https://github.com/reacher-z/vidground) |
| 2026 | arXiv | ClueNet | [Clue Matters: Leveraging Latent Visual Clues to Empower Video Reasoning](https://arxiv.org/abs/2603.15008) | - |
| 2026 | arXiv | EasyVideoR1 | [EasyVideoR1: Easier RL for Video Understanding](https://arxiv.org/abs/2604.16893) | [Code](https://github.com/cyuQ1n/EasyVideoR1) |
| 2026 | arXiv | Video-ToC | [Video-ToC: Video Tree-of-Cue Reasoning](https://arxiv.org/abs/2604.20473) | [Code](https://github.com/qizhongtan/Video-ToC) |
| 2026 | arXiv | STORMS | [STORM: Internalized Modeling for Spatial-Temporal Reasoning in Video-Language Models](https://arxiv.org/abs/2605.26014) | - |
| 2026 | arXiv | Video-MOPD | [Video-MOPD: Multi-Teacher On-Policy Distillation for Video Understanding](https://arxiv.org/abs/2609.09300) | - |
| 2026 | arXiv | ASSEMBLE | [ASSEMBLE: Atomic Skills for Evidence-Grounded Video Reasoning](https://arxiv.org/abs/2609.32466) | - |
| 2026 | arXiv | SAVER | [Less from More: Reinforcing Sparse Video Reasoning from Dense References](https://arxiv.org/abs/2610.10893) | [Code](https://github.com/lmsdss/SAVER) |
| 2026 | arXiv | Motion-o | [Motion-o: Trajectory-Grounded Video Reasoning](https://arxiv.org/abs/2603.18856) | [Code](https://github.com/ostadabbas/Motion-o) |
| 2026 | arXiv | When Rewards Disagree | [When Rewards Disagree: Reward Weighting for Token-Efficient Video Reasoning](https://arxiv.org/abs/2604.04415) | - |
| 2026 | EMNLP | Future-L1 | [Imagine Before You Predict: Interleaved Latent Visual Reasoning for Video Event Prediction](https://arxiv.org/abs/2606.05769) | [Code](https://github.com/OpenGVLab/Future-L1) |
| 2026 | arXiv | Video-FLAIR | [Video-FLAIR: Not Whether to Reason, But How](https://arxiv.org/abs/2608.26495) | - |
| 2026 | NeurIPS | BPO | [Behavior Pack Optimization for Video MLLM Post-Training](https://arxiv.org/abs/2610.03141) | - |

### 3.3 Thinking with Videos — Agentic

Models that interleave reasoning with explicit visual grounding and re-inspection (o3-style "thinking with images" extended to video).

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2025 | NeurIPS | VideoChat-R1.5 | [VideoChat-R1.5: Visual Test-Time Scaling to Reinforce Multimodal Reasoning by Iterative Perception](https://arxiv.org/abs/2509.21100) | [Code](https://github.com/OpenGVLab/VideoChat-R1) |
| 2025 | NeurIPS | Pixel Reasoner | [Pixel Reasoner: Incentivizing Pixel-Space Reasoning with Curiosity-Driven Reinforcement Learning](https://arxiv.org/abs/2505.15966) | [Code](https://github.com/TIGER-AI-Lab/Pixel-Reasoner) |
| 2026 | ICLR | VideoZoomer | [VideoZoomer: Reinforcement-Learned Temporal Focusing for Long Video Reasoning](https://arxiv.org/abs/2512.22315) | [Code](https://github.com/zsgvivo/VideoZoomer) |
| 2026 | CVPR | VITAL | [Thinking With Videos: Multimodal Tool-Augmented Reinforcement Learning for Long Video Reasoning](https://arxiv.org/abs/2508.04416) | - |
| 2025 | arXiv | FrameMind | [FrameMind: Frame-Interleaved Video Reasoning via Reinforcement Learning](https://arxiv.org/abs/2509.24008) | [Project](https://framemind.github.io/) |
| 2025 | NeurIPS | ViLaSR | [Reinforcing Spatial Reasoning in Vision-Language Models with Interwoven Thinking and Visual Drawing](https://arxiv.org/abs/2506.09965) | - |
| 2025 | arXiv | CyberV | [CyberV: Cybernetics for Test-time Scaling in Video Understanding](https://arxiv.org/abs/2506.07971) | [Code](https://github.com/marinero4972/CyberV) |
| 2026 | CVPR Findings | AVP | [Active Video Perception: Iterative Evidence Seeking for Agentic Long Video Understanding](https://arxiv.org/abs/2512.05774) | - |
| 2025 | arXiv | LOVE-R1 | [LOVE-R1: Advancing Long Video Understanding with an Adaptive Zoom-in Mechanism via Multi-Step Reasoning](https://arxiv.org/abs/2509.24786) | - |
| 2025 | arXiv | LongVT | [LongVT: Incentivizing "Thinking with Long Videos" via Native Tool Calling](https://arxiv.org/abs/2511.20785) | [Code](https://github.com/EvolvingLMMs-Lab/LongVT) |
| 2026 | CVPR | Conan | [Conan: Progressive Learning to Reason Like a Detective over Multi-Scale Visual Evidence](https://arxiv.org/abs/2510.20470) | [Code](https://github.com/ariesssxu/Conan-Active-Reasoning) |
| 2026 | ICML | VideoTemp-o3 | [VideoTemp-o3: Harmonizing Temporal Grounding and Video Understanding in Agentic Thinking-with-Videos](https://arxiv.org/abs/2602.07801) | - |
| 2026 | ICML | Video-o3 | [Video-o3: Native Interleaved Clue Seeking for Long Video Multi-Hop Reasoning](https://arxiv.org/abs/2601.23224) | [Code](https://github.com/MCG-NJU/Video-o3) |
| 2026 | CVPR | VideoSeek | [VideoSeek: Long-Horizon Video Agent with Tool-Guided Seeking](https://arxiv.org/abs/2603.20185) | [Code](https://github.com/jylins/videoseek) |
| 2026 | arXiv | Open-o3-Video-v2 | [Open-o3-Video-v2: Seek, Ground, and Reason with Verifiable Spatio-Temporal Evidence](https://arxiv.org/abs/2610.17656) | [Project](https://msalab-pku.github.io/projects/Open-o3-Video-v2) |
| 2026 | arXiv | VideoSlate | [VideoSlate: Stateful Commit Control for Temporally Grounded Agentic Video Reasoning](https://arxiv.org/abs/2610.16357) | - |
| 2026 | arXiv | VideoSeeker | [VideoSeeker: Incentivizing Instance-level Video Understanding via Native Agentic Tool Invocation](https://arxiv.org/abs/2605.16079) | [Code](https://github.com/gaotiexinqu/VideoSeeker) |
| 2026 | ICML | OmniAgent | [Native Active Perception as Reasoning for Omni-Modal Understanding](https://arxiv.org/abs/2606.19341) | [Code](https://github.com/harryhsing/OmniAgent) |
| 2026 | arXiv | VideoRover | [Thinking Beyond Videos: Unifying Video Reasoning and Deep Research for Open-World Video Agents](https://arxiv.org/abs/2608.23329) | - |
| 2026 | arXiv | VLX-VR | [VLX-VR: An Agentic-Aware Video Reasoning Model](https://arxiv.org/abs/2609.09985) | - |
| 2026 | arXiv | VideoResearchAgent | [VideoResearchAgent: Grounded Task Synthesis and Sim-to-Real RL for Open-Web Video Research](https://arxiv.org/abs/2610.04911) | - |
| 2026 | arXiv | InternVideo3 | [InternVideo3: Agentify Foundation Models with Multimodal Contextual Reasoning](https://arxiv.org/abs/2606.12195) | - |

### 3.4 Thinking with Videos — Non-Agent

Models that natively emit grounded reasoning traces (timestamps, boxes, captions) without external tool calls.

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2026 | ICML | Open-o3-Video | [Open-o3 Video: Grounded Video Reasoning with Explicit Spatio-Temporal Evidence](https://arxiv.org/abs/2510.20579) | [Code](https://github.com/marinero4972/Open-o3-Video) |
| 2025 | arXiv | Video-Thinker | [Video-Thinker: Sparking "Thinking with Videos" via Reinforcement Learning](https://arxiv.org/abs/2510.23473) | [Code](https://github.com/shijian2001/Video-Thinker) |
| 2026 | ICLR | ReWatch-R1 | [ReWatch-R1: Boosting Complex Video Reasoning in Large Vision-Language Models through Agentic Data Synthesis](https://arxiv.org/abs/2509.23652) | [Code](https://github.com/alibaba/ReWatch-R1) |
| 2026 | CVPR | VideoReasoner | [Incentivizing Versatile Video Reasoning in MLLMs via Data-Efficient Reinforcement Learning](https://openaccess.thecvf.com/content/CVPR2026/papers/Wang_Incentivizing_Versatile_Video_Reasoning_in_MLLMs_via_Data-Efficient_Reinforcement_Learning_CVPR_2026_paper.pdf) | [Code](https://github.com/Wang-Xiaodong1899/VideoReasoner) |
| 2026 | arXiv | VideoLVR | [VideoLVR: Latent Visual Reasoning over Grounded Video Evidence](https://arxiv.org/abs/2610.37613) | - |
| 2026 | ECCV | VisionCoach | [VisionCoach: Reinforcing Grounded Video Reasoning via Visual-Perception Prompting](https://arxiv.org/abs/2603.14659) | [Code](https://github.com/daeunni/VisionCoach) |
| 2026 | arXiv | — | [Beyond Visual CoT: Internalized Visual Thinking for Proactive Video Reasoning](https://arxiv.org/abs/2608.15869) | [Project](https://zgzxy001.github.io/blog/internalized-visual-thinking.html) |
| 2026 | arXiv | 4DThinker | [4DThinker: Thinking with 4D Imagery for Dynamic Spatial Understanding](https://arxiv.org/abs/2605.05997) | [Code](https://github.com/zhangquanchen/4DThinker) |

---

## 4. Subfields

Domain-specific scenarios that stress different combinations of perception, memory, and reasoning.

### 4.1 Egocentric Videos

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2025 | ICCV | EgoMask | [Fine-grained Spatiotemporal Grounding on Egocentric Videos](https://arxiv.org/abs/2508.00518) | [Code](https://github.com/LaVi-Lab/EgoMask) |
| 2025 | ACM MM | DMC³ | [DMC³: Dual-Modal Counterfactual Contrastive Construction for Egocentric Video Question Answering](https://arxiv.org/abs/2510.20285) | - |
| 2026 | WACV | ST-Think | [ST-Think: How Multimodal Large Language Models Reason About 4D Worlds from Ego-Centric Videos](https://arxiv.org/abs/2503.12542) | - |
| 2025 | arXiv | VLN-R1 | [VLN-R1: Vision-Language Navigation via Reinforcement Fine-Tuning](https://arxiv.org/abs/2506.17221) | [Code](https://github.com/Qi-Zhangyang/GPT4Scene-and-VLN-R1) |
| 2025 | arXiv | Ego-R1 | [Ego-R1: Chain-of-Tool-Thought for Ultra-Long Egocentric Video Reasoning](https://arxiv.org/abs/2506.13654) | [Code](https://github.com/egolife-ai/Ego-R1) |
| 2025 | NeurIPS | VideoLLM-EyeWO | [Eyes Wide Open: Ego Proactive Video-LLM for Streaming Video](https://arxiv.org/abs/2510.14560) | - |
| 2025 | arXiv | EgoSocial | [EgoSocial: Benchmarking Proactive Intervention Ability of Omnimodal LLMs via Egocentric Social Interaction Perception](https://arxiv.org/abs/2510.13105) | - |
| 2025 | KDD | DVBench | [Are Vision LLMs Road-Ready? A Comprehensive Benchmark for Safety-Critical Driving Video Understanding](https://arxiv.org/abs/2504.14526) | [Code](https://github.com/tong-zeng/DVBench) |
| 2026 | arXiv | EgoEverything | [EgoEverything: A Benchmark for Human Behavior Inspired Long Context Egocentric Video Understanding in AR Environment](https://arxiv.org/abs/2604.08342) | - |
| 2026 | COLM | EgoMemReason | [EgoMemReason: A Memory-Driven Reasoning Benchmark for Long-Horizon Egocentric Video Understanding](https://arxiv.org/abs/2605.09874) | [Project](https://egomemreason.github.io/) |
| 2026 | arXiv | EgoProbe | [EgoProbe: Benchmarking Long-Range and Exact Memory in Streaming Egocentric Videos](https://arxiv.org/abs/2610.17128) | - |
| 2026 | arXiv | EgoReasoner | [EgoReasoner: Learning Egocentric 4D Reasoning via Task-Adaptive Structured Thinking](https://arxiv.org/abs/2603.06561) | - |
| 2026 | arXiv | MA-EgoQA | [MA-EgoQA: Question Answering over Egocentric Videos from Multiple Embodied Agents](https://arxiv.org/abs/2603.09827) | [Code](https://github.com/KangsanKim07/MA-EgoQA) |
| 2026 | arXiv | EgoIntent | [EgoIntent: A Pre-Outcome Micro-Step Benchmark for Understanding What, Why, and Next](https://arxiv.org/abs/2603.12147) | - |
| 2026 | arXiv | EgoExoMem | [EgoExoMem: Cross-View Memory Reasoning over Synchronized Egocentric and Exocentric Videos](https://arxiv.org/abs/2605.18734) | - |
| 2026 | arXiv | EgoCoT-Bench | [EgoCoT-Bench: Benchmarking Grounded and Verifiable Operation-Centric Chain of Thought Reasoning for MLLMs](https://arxiv.org/abs/2605.19559) | - |
| 2026 | arXiv | SuperMemory-VQA | [SuperMemory-VQA: An Egocentric Visual Question-Answering Benchmark for Long-Horizon Memory](https://arxiv.org/abs/2606.00825) | [Code](https://github.com/AIoT-MLSys-Lab/supermemory-vqa) |
| 2026 | ECCV | EgoSAT | [EgoSAT: A Comprehensive Benchmark of Egocentric Streaming Interaction Understanding](https://arxiv.org/abs/2606.24422) | - |
| 2026 | arXiv | EgoSG | [Graph it first! Enabling Reasoning on Long-form Egocentric Videos through Scene Graphs](https://arxiv.org/abs/2606.25842) | - |
| 2026 | ECCV | Vinci2 / EgoMemo | [Vinci2: Providing Proactive Assistance in Continuous Egocentric Videos](https://arxiv.org/abs/2607.11523) | [Code](https://github.com/SitongGong/EgoMemo) |
| 2026 | arXiv | SCOUT | [SCOUT: Self-Checking and Recovery-Aware Tool-Thought Agents for Ultra-Long Egocentric Video Reasoning](https://arxiv.org/abs/2608.07959) | - |
| 2026 | arXiv | EgoCITE | [EgoCITE: Context-Augmented Indexing and Time-Aware Retrieval for Long-Horizon Egocentric Memory](https://arxiv.org/abs/2608.12627) | - |
| 2026 | arXiv | EgoMonth | [EgoMonth: A Month-Level Egocentric Video Benchmark for Long-Term Spatiotemporal Memory](https://arxiv.org/abs/2608.13113) | - |
| 2026 | arXiv | APM-Bench | [APM-Bench: Benchmarking Cross-session Persistent Memory for Egocentric Streaming Video Assistants](https://arxiv.org/abs/2609.37559) | [Code](https://github.com/Jianguo-Huang11/APM-Bench) |
| 2026 | arXiv | EgoTools | [EgoTools: Towards Tool-Centric Reasoning in Real-World Egocentric Videos](https://arxiv.org/abs/2609.39378) | [Code](https://github.com/Ropedia/EgoTools) |
| 2026 | arXiv | From Frames to Temporal Graphs | [From Frames to Temporal Graphs: In-Context Egocentric Action Recognition with Vision-Language Models](https://arxiv.org/abs/2606.15417) | - |
| 2026 | arXiv | UNIEGO | [UNIEGO: Proxies as Mediators for Unified Egocentric Video Representation Learning](https://arxiv.org/abs/2606.20559) | - |
| 2026 | arXiv | R3D | [R3D: Quantitative 3D Spatial Reasoning for Egocentric Wearables](https://arxiv.org/abs/2607.02921) | - |
| 2026 | arXiv | EgoSafe | [EgoSafe: A First-Person Mobile-Captured Benchmark for Visual Safety Understanding](https://arxiv.org/abs/2607.26518) | - |

### 4.2 Sports Videos

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2025 | ICLR | SPORTU | [SPORTU: A Comprehensive Sports Understanding Benchmark for Multimodal Large Language Models](https://arxiv.org/abs/2410.08474) | [Code](https://github.com/chili-lab/SPORTU) |
| 2025 | CVPR | UniSoccer | [Towards Universal Soccer Video Understanding](https://arxiv.org/abs/2412.01820) | [Code](https://github.com/jyrao/UniSoccer) |
| 2025 | CVPR-W | — | [Domain Adaptation of VLM for Soccer Video Understanding](https://arxiv.org/abs/2505.13860) | - |
| 2025 | arXiv | DeepSport | [DeepSport: A Multimodal Large Language Model for Comprehensive Sports Video Reasoning via Agentic Reinforcement Learning](https://arxiv.org/abs/2511.12908) | - |
| 2025 | ACM MM | FineQuest | [FineQuest: Adaptive Knowledge-Assisted Sports Video Understanding via Agent-of-Thoughts Reasoning](https://arxiv.org/abs/2509.11796) | - |
| 2026 | ICASSP | TennisTV | [TennisTV: Do Multimodal Large Language Models Understand Tennis Rallies?](https://arxiv.org/abs/2509.15602) | - |
| 2026 | ECCV | — | [Learning Consistent Temporal Grounding between Related Tasks in Sports Coaching](https://arxiv.org/abs/2603.18453) | - |
| 2026 | arXiv | SportMV-Bench | [Beyond the Single Camera: Agentic Multi-View Reasoning in Sports Video Understanding](https://arxiv.org/abs/2607.11844) | - |
| 2026 | arXiv | CourtSI | [Stepping VLMs onto the Court: Benchmarking Spatial Intelligence in Sports](https://arxiv.org/abs/2603.09896) | [Code](https://github.com/Visionary-Laboratory/CourtSI) |
| 2026 | arXiv | EgoEsportsQA | [EgoEsportsQA: An Egocentric Video Benchmark for Perception and Reasoning in Esports](https://arxiv.org/abs/2604.12320) | - |
| 2026 | arXiv | CoTR / SportsTime | [Towards Temporal Compositional Reasoning in Long-Form Sports Videos](https://arxiv.org/abs/2604.22226) | - |
| 2026 | arXiv | TreeSoc | [TreeSoc: Tree-Structured Dynamic Reasoning and Tool Synergy for Soccer Video Understanding](https://arxiv.org/abs/2607.10990) | - |
| 2026 | arXiv | TennisVAR | [TennisVAR: A Stroke-Evidence-Grounded Multimodal Large Language Model for Tactical Reasoning in Tennis Videos](https://arxiv.org/abs/2608.12920) | - |
| 2026 | arXiv | BFMD | [BFMD: A Full-Match Badminton Dense Dataset for Dense Shot Captioning](https://arxiv.org/abs/2603.25533) | - |
| 2026 | KDD | SVHighlights | [SVHighlights: Towards Extremely Long Sport Video Highlight Detection](https://arxiv.org/abs/2606.06926) | - |

### 4.3 Instructional Videos

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2026 | ACL | Video-MMMU | [Video-MMMU: Evaluating Knowledge Acquisition from Multi-Discipline Professional Videos](https://arxiv.org/abs/2501.13826) | [Code](https://github.com/EvolvingLMMs-Lab/VideoMMMU) |
| 2025 | ICCVW | Video-MMLU | [Video-MMLU: A Massive Multi-Discipline Lecture Understanding Benchmark](https://arxiv.org/abs/2504.14693) | [Code](https://github.com/Espere-1119-Song/Video-MMLU) |
| 2025 | arXiv | InstructionBench | [InstructionBench: An Instructional Video Understanding Benchmark](https://arxiv.org/abs/2504.05040) | - |
| 2025 | ICASSP | DocVideoQA | [DocVideoQA: Towards Comprehensive Understanding of Document-Centric Videos through Question Answering](https://arxiv.org/abs/2503.15887) | - |
| 2025 | UIST | NoteIt | [NoteIt: A System Converting Instructional Videos to Interactable Notes Through Multimodal Video Understanding](https://arxiv.org/abs/2508.14395) | [Project](https://zhaorunning.github.io/NoteIt/) |
| 2025 | ICASSP | InsTALL | [InsTALL: Context-aware Instructional Task Assistance with Multi-modal Large Language Models](https://arxiv.org/abs/2501.12231) | - |
| 2026 | arXiv | DenseStep2M | [DenseStep2M: A Scalable, Training-Free Pipeline for Dense Instructional Video Annotation](https://arxiv.org/abs/2604.26565) | - |

### 4.4 Medical Videos

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2024 | arXiv | LLaVA-Surg | [LLaVA-Surg: Towards Multimodal Surgical Assistant via Structured Surgical Video Learning](https://arxiv.org/abs/2408.07981) | - |
| 2024 | arXiv | Surgical-LLaVA | [Surgical-LLaVA: Toward Surgical Scenario Understanding via Large Language and Vision Models](https://arxiv.org/abs/2410.09750) | - |
| 2025 | Med IA | EndoChat | [EndoChat: Grounded Multimodal Large Language Model for Endoscopic Surgery](https://arxiv.org/abs/2501.11347) | [Code](https://github.com/gkw0010/EndoChat) |
| 2025 | arXiv | SurgVLM | [SurgVLM: A Large Vision-Language Model and Systematic Evaluation Benchmark for Surgical Intelligence](https://arxiv.org/abs/2506.02555) | [Project](https://jinlab-imvr.github.io/SurgVLM/) |
| 2025 | arXiv | SurgVidLM | [SurgVidLM: Towards Multi-grained Surgical Video Understanding with Large Language Model](https://arxiv.org/abs/2506.17873) | - |
| 2026 | IJCARS | SurgViVQA | [SurgViVQA: Temporally-Grounded Video Question Answering for Surgical Scene Understanding](https://arxiv.org/abs/2511.03325) | [Code](https://github.com/J-I-N-G-L-I/SurgViVQA_on_STSG_VQA) |
| 2024 | Nature Med | EchoCLIP | [Vision–Language Foundation Model for Echocardiogram Interpretation](https://www.nature.com/articles/s41591-024-02959-y) | - |
| 2024 | MICCAI | MMSummary | [MMSummary: Multimodal Summary Generation for Fetal Ultrasound Video](https://arxiv.org/abs/2408.03761) | - |
| 2026 | NBME | Sonomate | [A Visually Grounded Language Model for Fetal Ultrasound Understanding](https://www.nature.com/articles/s41551-025-01578-3) | - |
| 2026 | arXiv | MedStreamBench | [MedStreamBench: A Time-Aware Benchmark for Streaming and Proactive Medical Video Understanding](https://arxiv.org/abs/2607.01751) | [Dataset](https://huggingface.co/datasets/Venn2024/MedStreamBench) |
| 2026 | arXiv | SUREON | [SUREON: A Benchmark and Vision-Language-Model for Surgical Reasoning](https://arxiv.org/abs/2603.06570) | - |
| 2026 | arXiv | SurgTEMP | [SurgTEMP: Temporal-Aware Surgical Video Question Answering with Text-guided Visual Memory for Laparoscopic Cholecystectomy](https://arxiv.org/abs/2603.29962) | - |
| 2026 | arXiv | SurgAtlas | [SurgAtlas: A Large-Scale Surgical Video-Language Dataset with 2,391 Hours of Open and Minimally Invasive Surgery](https://arxiv.org/abs/2606.25905) | - |
| 2026 | arXiv | SurgRec | [Scaling Video Pretraining for Surgical Foundation Models](https://arxiv.org/abs/2603.29966) | - |
| 2026 | arXiv | SurgicalMamba | [SurgicalMamba: Dual-Path SSD with State Regramming for Online Surgical Phase Recognition](https://arxiv.org/abs/2605.14889) | [Code](https://github.com/sukjuoh/Surgical-Mamba) |

### 4.5 Movie and Narrative Videos

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2016 | CVPR | MovieQA | [MovieQA: Understanding Stories in Movies through Question-Answering](https://arxiv.org/abs/1512.02902) | [Code](https://github.com/makarandtapaswi/MovieQA_CVPR2016) |
| 2023 | arXiv | MoVQA | [MoVQA: A Benchmark of Versatile Question-Answering for Long-Form Movie Understanding](https://arxiv.org/abs/2312.04817) | - |
| 2024 | CVPR | MovieChat | [MovieChat: From Dense Token to Sparse Memory for Long Video Understanding](https://arxiv.org/abs/2307.16449) | [Code](https://github.com/rese1f/MovieChat) |
| 2026 | IJCV | SFD / SF20K | [Long Story Short: Story-level Video Understanding from 20K Short Films](https://arxiv.org/abs/2406.10221) | [Dataset](https://huggingface.co/datasets/rghermi/sf20k) |
| 2025 | IJCAI | SCVBench | [SCVBench: A Benchmark with Multi-turn Dialogues for Story-Centric Video Understanding](https://www.ijcai.org/proceedings/2025/0255.pdf) | [Code](https://github.com/yuanrr/SCVBench) |
| 2025 | ICCV | VRBench | [VRBench: A Benchmark for Multi-Step Reasoning in Long Narrative Videos](https://arxiv.org/abs/2506.10857) | [Code](https://github.com/OpenGVLab/VRBench) |
| 2025 | CVPR | SeriesBench | [SeriesBench: A Benchmark for Narrative-Driven Drama Series Understanding](https://arxiv.org/abs/2504.21435) | [Code](https://github.com/zackhxn/SeriesBench-CVPR2025) |
| 2025 | arXiv | Cinéaste | [Cinéaste: A Fine-grained Contextual Movie Question Answering Benchmark](https://arxiv.org/abs/2509.14227) | - |
| 2025 | EMNLP | MovieCORE | [MovieCORE: COgnitive REasoning in Movies](https://arxiv.org/abs/2508.19026) | [Code](https://github.com/joslefaure/moviecore) |
| 2025 | arXiv | ARC-Chapter | [ARC-Chapter: Structuring Hour-Long Videos into Navigable Chapters and Hierarchical Summaries](https://arxiv.org/abs/2511.14349) | - |
| 2026 | arXiv | StoryVideoQA | [StoryVideoQA: Scaling Deep Video Understanding with a Large-Scale, Multi-Genre and Auto-Generated Dataset](https://arxiv.org/abs/2606.06338) | - |
| 2026 | arXiv | NARU | [NARU: A Benchmark for NARrative Evolution and Cultural Nuance Understanding in Japanese Extreme Long Video](https://arxiv.org/abs/2608.13210) | [Code](https://github.com/infinimind-inc/naru_benchmark) |
| 2026 | arXiv | Beyond Visual Boundaries | [Beyond Visual Boundaries: Rethinking Scene Segmentation for Movie RAG](https://arxiv.org/abs/2608.28699) | - |

---

## 5. Datasets and Benchmarks

### 5.1 Training Datasets

#### 5.1.1 Video QA

Covers both training corpora and widely used QA benchmarks (many pre-MLLM datasets are still used for evaluation).

| Year | Acronym | Paper | Code / Project |
| :---: | :---: | :--- | :---: |
| 2017 | MSVD-QA | [Video Question Answering via Gradually Refined Attention over Appearance and Motion](https://dl.acm.org/doi/10.1145/3123266.3123427) | - |
| 2017 | TGIF-QA | [TGIF-QA: Toward Spatio-Temporal Reasoning in Visual Question Answering](https://arxiv.org/abs/1704.04497) | [Code](https://github.com/YunseokJANG/tgif-qa) |
| 2018 | TVQA | [TVQA: Localized, Compositional Video Question Answering](https://arxiv.org/abs/1809.01696) | [Code](https://github.com/jayleicn/TVQA) |
| 2019 | ActivityNet-QA | [ActivityNet-QA: A Dataset for Understanding Complex Web Videos via Question Answering](https://arxiv.org/abs/1906.02467) | [Code](https://github.com/MILVLG/activitynet-qa) |
| 2020 | CLEVRER | [CLEVRER: Collision Events for Video Representation and Reasoning](https://arxiv.org/abs/1910.01442) | [Project](http://clevrer.csail.mit.edu/) |
| 2021 | NExT-QA | [NExT-QA: Next Phase of Question-Answering to Explaining Temporal Actions](https://arxiv.org/abs/2105.08276) | [Code](https://github.com/doc-doc/NExT-QA) |
| 2021 | HowToVQA69M | [Just Ask: Learning to Answer Questions from Millions of Narrated Videos](https://arxiv.org/abs/2012.00451) | [Code](https://github.com/antoyang/just-ask) |
| 2024 | VideoInstruct100K | [Video-ChatGPT: Towards Detailed Video Understanding via Large Vision and Language Models](https://arxiv.org/abs/2306.05424) | [Code](https://github.com/mbzuai-oryx/Video-ChatGPT) |
| 2024 | VideoChat2-IT | [MVBench: A Comprehensive Multi-modal Video Understanding Benchmark](https://arxiv.org/abs/2311.17005) | [Code](https://github.com/OpenGVLab/Ask-Anything) |
| 2024 | LLaVA-Video-178K | [Video Instruction Tuning with Synthetic Data](https://arxiv.org/abs/2410.02713) | [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) |
| 2024 | VideoCoT | [VideoCoT: A Video Chain-of-Thought Dataset with Active Annotation Tool](https://arxiv.org/abs/2407.05355) | - |
| 2025 | VideoEspresso | [VideoEspresso: A Large-Scale Chain-of-Thought Dataset for Fine-Grained Video Reasoning via Core Frame Selection](https://arxiv.org/abs/2411.14794) | [Code](https://github.com/hshjerry/VideoEspresso) |
| 2025 | Video-R1 | [Video-R1: Reinforcing Video Reasoning in MLLMs](https://arxiv.org/abs/2503.21776) | [Code](https://github.com/tulerfeng/Video-R1) |
| 2025 | VideoRFT | [VideoRFT: Incentivizing Video Reasoning Capability in MLLMs via Reinforced Fine-Tuning](https://arxiv.org/abs/2505.12434) | [Code](https://github.com/QiWang98/VideoRFT) |
| 2025 | LongVideo-Reason | [Scaling RL to Long Videos](https://arxiv.org/abs/2507.07966) | [Code](https://github.com/NVlabs/Long-RL) |
| 2025 | STGR | [Open-o3 Video: Grounded Video Reasoning with Explicit Spatio-Temporal Evidence](https://arxiv.org/abs/2510.20579) | [Code](https://github.com/marinero4972/Open-o3-Video) |
| 2025 | ReWatch-CoT | [ReWatch-R1: Boosting Complex Video Reasoning in Large Vision-Language Models through Agentic Data Synthesis](https://arxiv.org/abs/2509.23652) | [Code](https://github.com/alibaba/ReWatch-R1) |
| 2025 | VideoZoomer | [VideoZoomer: Reinforcement-Learned Temporal Focusing for Long Video Reasoning](https://arxiv.org/abs/2512.22315) | [Code](https://github.com/zsgvivo/VideoZoomer) |
| 2025 | VideoSIAH | [LongVT: Incentivizing "Thinking with Long Videos" via Native Tool Calling](https://arxiv.org/abs/2511.20785) | [Code](https://github.com/EvolvingLMMs-Lab/LongVT) |
| 2025 | Conan | [Conan: Progressive Learning to Reason Like a Detective over Multi-Scale Visual Evidence](https://arxiv.org/abs/2510.20470) | [Code](https://github.com/ariesssxu/Conan-Active-Reasoning) |
| 2026 | Seeker-173K | [Video-o3: Native Interleaved Clue Seeking for Long Video Multi-Hop Reasoning](https://arxiv.org/abs/2601.23224) | [Code](https://github.com/MCG-NJU/Video-o3) |
| 2026 | LongVideo-R1 | [LongVideo-R1: Smart Navigation for Low-cost Long Video Understanding](https://arxiv.org/abs/2602.20913) | [Code](https://github.com/qiujihao19/LongVideo-R1) |
| 2026 | VideoKR | [VideoKR: Towards Knowledge- and Reasoning-Intensive Video Understanding](https://arxiv.org/abs/2606.05259) | [Code](https://github.com/Fu-Fu-Fu-Fu/VideoKR) |
| 2026 | OmniVideo-100K | [OmniVideo-100K: A Dataset for Audio-Visual Reasoning through Structured Scripts and Evidence Chains](https://arxiv.org/abs/2606.14702) | [Code](https://github.com/MiG-NJU/OmniVideo-100K) |

#### 5.1.2 Video Captioning

Includes classical clip / dense / narration-level corpora, MLLM-era recaptioned corpora, and grounded / omni-modal captioning data.

| Year | Acronym | Paper | Code / Project |
| :---: | :---: | :--- | :---: |
| 2016 | MSR-VTT | [MSR-VTT: A Large Video Description Dataset for Bridging Video and Language](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/06/cvpr16.msr-vtt.tmei_-1.pdf) | - |
| 2017 | ActivityNet Captions | [Dense-Captioning Events in Videos](https://arxiv.org/abs/1705.00754) | [Project](https://cs.stanford.edu/people/ranjaykrishna/densevid/) |
| 2018 | YouCook2 | [Towards Automatic Learning of Procedures from Web Instructional Videos](https://arxiv.org/abs/1703.09788) | [Project](http://youcook2.eecs.umich.edu/) |
| 2019 | VATEX | [VATEX: A Large-Scale, High-Quality Multilingual Dataset for Video-and-Language Research](https://arxiv.org/abs/1904.03493) | [Project](https://eric-xw.github.io/vatex-website/) |
| 2020 | TVC | [TVR: A Large-Scale Dataset for Video-Subtitle Moment Retrieval](https://arxiv.org/abs/2001.09099) | [Code](https://github.com/jayleicn/TVRetrieval) |
| 2020 | ViTT | [Multimodal Pretraining for Dense Video Captioning](https://arxiv.org/abs/2011.11760) | [Code](https://github.com/google-research-datasets/Video-Timeline-Tags-ViTT) |
| 2022 | Ego4D | [Ego4D: Around the World in 3,000 Hours of Egocentric Video](https://arxiv.org/abs/2110.07058) | [Project](https://ego4d-data.org/) |
| 2024 | Panda-70M | [Panda-70M: Captioning 70M Videos with Multiple Cross-Modality Teachers](https://arxiv.org/abs/2402.19479) | [Code](https://github.com/snap-research/Panda-70M) |
| 2024 | ShareGPT4Video | [ShareGPT4Video: Improving Video Understanding and Generation with Better Captions](https://arxiv.org/abs/2406.04325) | [Code](https://github.com/ShareGPT4Omni/ShareGPT4Video) |
| 2024 | Video ReCap | [Video ReCap: Recursive Captioning of Hour-Long Videos](https://arxiv.org/abs/2402.13250) | [Code](https://github.com/md-mohaiminul/VideoRecap) |
| 2024 | Vript | [Vript: A Video Is Worth Thousands of Words](https://arxiv.org/abs/2406.06040) | [Code](https://github.com/mutonix/Vript) |
| 2024 | MiraData | [MiraData: A Large-Scale Video Dataset with Long Durations and Structured Captions](https://arxiv.org/abs/2407.06358) | [Code](https://github.com/mira-space/MiraData) |
| 2024 | FineVideo | [FineVideo Dataset](https://huggingface.co/datasets/HuggingFaceFV/finevideo) | [Dataset](https://huggingface.co/datasets/HuggingFaceFV/finevideo) |
| 2025 | Tarsier2-Recap-585K | [Tarsier2: Advancing Large Vision-Language Models from Detailed Video Description to Comprehensive Video Understanding](https://arxiv.org/abs/2501.07888) | [Code](https://github.com/bytedance/tarsier) |
| 2025 | UltraVideo | [UltraVideo: High-Quality UHD Video Dataset with Comprehensive Captions](https://arxiv.org/abs/2506.13691) | [Project](https://xzc-zju.github.io/projects/UltraVideo/) |
| 2025 | HMD-270K | [OwlCap: Harmonizing Motion-Detail for Video Captioning via HMD-270K and Caption Set Equivalence Reward](https://arxiv.org/abs/2508.18634) | - |
| 2025 | ViCaS | [ViCaS: A Dataset for Combining Holistic and Pixel-level Video Understanding using Captions with Grounded Segmentation](https://arxiv.org/abs/2412.09754) | [Code](https://github.com/Ali2500/ViCaS) |
| 2025 | iGround / HowToGround1M | [Large-scale Pre-training for Grounded Video Caption Generation](https://arxiv.org/abs/2503.10781) | - |
| 2025 | PerceptionLM (PLM-Video) | [PerceptionLM: Open-Access Data and Models for Detailed Visual Understanding](https://arxiv.org/abs/2504.13180) | [Code](https://github.com/facebookresearch/perception_models) |
| 2025 | UGC-VideoCaptioner | [UGC-VideoCaptioner: An Omni UGC Video Detail Caption Model and New Benchmarks](https://arxiv.org/abs/2507.11336) | - |
| 2026 | TimeChatCap-42K | [TimeChat-Captioner: Scripting Multi-scene Videos with Time-aware and Structural Audio-Visual Captions](https://arxiv.org/abs/2602.08711) | - |
| 2026 | LAION-BVD | [LAION-BVD: A 10-Million-Hour Open Video Dataset for Multimodal Pre-training](https://arxiv.org/abs/2608.24845) | [Project](https://projects.laion.ai/bvd/) |
| 2026 | MVC | [Advancing Video-Text Pretraining with Multi-View Captions](https://arxiv.org/abs/2609.35090) | - |

#### 5.1.3 Video Temporal Grounding

Includes large-scale narrated-video pretraining corpora, MLLM-era instruction tuning corpora, and reasoning-/RL-oriented re-annotated data.

| Year | Acronym | Paper | Code / Project |
| :---: | :---: | :--- | :---: |
| 2021 | YT-Temporal-180M | [MERLOT: Multimodal Neural Script Knowledge Models](https://arxiv.org/abs/2106.02636) | [Project](https://rowanzellers.com/merlot/) |
| 2023 | TimeIT | [TimeChat: A Time-sensitive Multimodal Large Language Model for Long Video Understanding](https://arxiv.org/abs/2312.02051) | [Code](https://github.com/RenShuhuai-Andy/TimeChat) |
| 2024 | ActivityNet-RTL | [LITA: Language Instructed Temporal-Localization Assistant](https://arxiv.org/abs/2403.19046) | [Code](https://github.com/NVlabs/LITA) |
| 2024 | VTimeLLM Data | [VTimeLLM: Empower LLM to Grasp Video Moments](https://arxiv.org/abs/2311.18445) | [Code](https://github.com/huangb23/VTimeLLM) |
| 2024 | VTG-IT-120K | [VTG-LLM: Integrating Timestamp Knowledge into Video LLMs for Enhanced Video Temporal Grounding](https://arxiv.org/abs/2405.13382) | [Code](https://github.com/gyxxyg/VTG-LLM) |
| 2024 | E.T. Instruct 164K | [E.T. Bench: Towards Open-Ended Event-Level Video-Language Understanding](https://arxiv.org/abs/2409.18111) | [Code](https://github.com/PolyU-ChenLab/ETBench) |
| 2024 | Moment-10M | [Momentor: Advancing Video Large Language Model with Fine-Grained Temporal Reasoning](https://arxiv.org/abs/2402.11435) | [Code](https://github.com/DCDmllm/Momentor) |
| 2024 | Vid-Morp | [Vid-Morp: Video Moment Retrieval Pretraining from Unlabeled Videos in the Wild](https://arxiv.org/abs/2412.00811) | [Code](https://github.com/baopj/Vid-Morp) |
| 2025 | TimePro | [TimeSuite: Improving MLLMs for Long Video Understanding via Grounded Tuning](https://arxiv.org/abs/2410.19702) | [Code](https://github.com/OpenGVLab/TimeSuite) |
| 2025 | VideoITG | [VideoITG: Multimodal Video Understanding with Instructed Temporal Grounding](https://arxiv.org/abs/2507.13353) | [Code](https://github.com/NVlabs/VideoITG) |
| 2025 | TimeLens-100K | [TimeLens: Rethinking Video Temporal Grounding with Multimodal LLMs](https://arxiv.org/abs/2512.14698) | [Code](https://github.com/TencentARC/TimeLens) |
| 2025 | TimeRFT | [Time-R1: Post-Training Large Vision Language Model for Temporal Video Grounding](https://arxiv.org/abs/2503.13377) | [Code](https://github.com/xiaomi-research/time-r1) |
| 2025 | TVG-R1 | [Datasets and Recipes for Video Temporal Grounding via Reinforcement Learning](https://arxiv.org/abs/2507.18100) | - |
| 2025 | VTTS-80K | [VideoChat-R1.5: Visual Test-Time Scaling to Reinforce Multimodal Reasoning by Iterative Perception](https://arxiv.org/abs/2509.21100) | [Code](https://github.com/OpenGVLab/VideoChat-R1) |
| 2025 | MTVR | [Thinking With Videos: Multimodal Tool-Augmented Reinforcement Learning for Long Video Reasoning](https://arxiv.org/abs/2508.04416) | - |

#### 5.1.4 Long Video Memory

| Year | Acronym | Paper | Code / Project |
| :---: | :---: | :--- | :---: |
| 2025 | VideoMarathon | [Unleashing Hour-Scale Video Training for Long Video-Language Understanding](https://arxiv.org/abs/2506.05332) | [Code](https://github.com/jylins/hourllava) |
| 2026 | M3-Bench | [Seeing, Listening, Remembering, and Reasoning: A Multimodal Agent with Long-Term Memory](https://arxiv.org/abs/2508.09736) | [Code](https://github.com/ByteDance-Seed/m3-agent) |

### 5.2 Evaluation Benchmarks

Categorized into six capability dimensions.

#### 5.2.1 General Video Understanding

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2024 | CVPR | Video-MME | [Video-MME: The First-Ever Comprehensive Evaluation Benchmark of Multi-modal LLMs in Video Analysis](https://arxiv.org/abs/2405.21075) | [Code](https://github.com/MME-Benchmarks/Video-MME) |
| 2024 | NeurIPS | MMBench-Video | [MMBench-Video: A Long-Form Multi-Shot Benchmark for Holistic Video Understanding](https://arxiv.org/abs/2406.14515) | [Code](https://github.com/open-compass/VLMEvalKit) |
| 2025 | arXiv | Video-MME v2 | [Video-MME v2: Evaluating Multimodal LLMs with Cohesive Question Groups on Fresh Videos](https://arxiv.org/abs/2510.21075) | [Code](https://github.com/MME-Benchmarks/Video-MME) |
| 2025 | ICLR | MMWorld | [MMWorld: Towards Multi-Discipline Multi-Faceted World Model Evaluation in Videos](https://arxiv.org/abs/2406.08407) | [Code](https://github.com/eric-ai-lab/MMWorld) |
| 2026 | ECCV | Video-Oasis | [Video-Oasis: Rethinking Evaluation of Video Understanding](https://arxiv.org/abs/2603.29616) | [Code](https://github.com/sejong-rcv/Video-Oasis) |
| 2026 | arXiv | CL-VISTA | [CL-VISTA: Benchmarking Continual Learning in Video Large Language Models](https://arxiv.org/abs/2604.00677) | - |
| 2026 | arXiv | CLIP-CC-Bench | [CLIP-CC-Bench: Evaluating Paragraph-Level Video Descriptions in Video-Language Models](https://arxiv.org/abs/2608.04302) | [Code](https://github.com/Multimodal-Intelligence-Lab/CLIP-CC-Bench) |
| 2026 | arXiv | Video-IFBench | [Video-IFBench: Evaluating Instruction Following of Multimodal LLMs in Video Understanding Scenarios](https://arxiv.org/abs/2608.25529) | [Code](https://github.com/Alexios-hub/Video-IFBench) |
| 2026 | arXiv | Video-Index | [Video-Index: A Curated Meta-Benchmark for Video Understanding](https://arxiv.org/abs/2610.00960) | - |
| 2026 | arXiv | Video-MME-v2 | [Video-MME-v2: Towards the Next Stage in Benchmarks for Comprehensive Video Understanding](https://arxiv.org/abs/2604.05015) | [Code](https://github.com/MME-Benchmarks/Video-MME-v2) |
| 2026 | EMNLP Findings | MVEB | [MVEB: Massive Video Embedding Benchmark](https://arxiv.org/abs/2606.14958) | [Code](https://github.com/embeddings-benchmark/mteb) |
| 2026 | arXiv | CodeCap-Bench | [CodeCap-Bench: Can Code Serve as a Good Video Caption?](https://arxiv.org/abs/2610.37341) | [Project](https://codecap-bench.github.io/) |

#### 5.2.2 Temporal & Spatial Understanding

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2024 | CVPR | MVBench | [MVBench: A Comprehensive Multi-modal Video Understanding Benchmark](https://arxiv.org/abs/2311.17005) | [Code](https://github.com/OpenGVLab/Ask-Anything) |
| 2024 | ACL | TempCompass | [TempCompass: Do Video LLMs Really Understand Videos?](https://arxiv.org/abs/2403.00476) | [Code](https://github.com/llyx97/TempCompass) |
| 2025 | ACL | TOMATO | [TOMATO: Assessing Visual Temporal Reasoning Capabilities in Multimodal Foundation Models](https://arxiv.org/abs/2410.23266) | [Code](https://github.com/yale-nlp/TOMATO) |
| 2024 | NeurIPS | E.T. Bench | [E.T. Bench: Towards Open-Ended Event-Level Video-Language Understanding](https://arxiv.org/abs/2409.18111) | [Code](https://github.com/PolyU-ChenLab/ETBench) |
| 2025 | ACL | TUNA | [TUNA: Comprehensive Fine-Grained Temporal Understanding Evaluation on Dense Dynamic Videos](https://arxiv.org/abs/2505.20124) | [Project](https://friedrichor.github.io/projects/TUNA) |
| 2026 | CVPR | TimeLens | [TimeLens: Rethinking Video Temporal Grounding with Multimodal LLMs](https://arxiv.org/abs/2512.14698) | [Code](https://github.com/TencentARC/TimeLens) |
| 2025 | EMNLP | TVGBench | [Datasets and Recipes for Video Temporal Grounding via Reinforcement Learning](https://arxiv.org/abs/2507.18100) | - |
| 2025 | arXiv | TimeScope | [TimeScope: Towards Task-Oriented Temporal Grounding in Long Videos](https://arxiv.org/abs/2509.26360) | - |
| 2025 | arXiv | SVAG-Bench | [SVAG-Bench: A Large-Scale Benchmark for Multi-Instance Spatio-temporal Video Action Grounding](https://arxiv.org/abs/2510.13016) | - |
| 2025 | CVPR | MotionBench | [MotionBench: Benchmarking and Improving Fine-grained Video Motion Understanding for Vision Language Models](https://arxiv.org/abs/2501.02955) | [Code](https://github.com/THUDM/MotionBench) |
| 2025 | arXiv | DSI-Bench | [DSI-Bench: A Benchmark for Dynamic Spatial Intelligence](https://arxiv.org/abs/2510.18873) | - |
| 2025 | ICCV | STI-Bench | [STI-Bench: Are MLLMs Ready for Precise Spatial-Temporal World Understanding?](https://arxiv.org/abs/2503.23765) | [Project](https://mira-sjtu.github.io/STI-Bench.io/) |
| 2025 | arXiv | SI-Bench | [How Far Are VLMs from Visual Spatial Intelligence? A Benchmark-Driven Perspective](https://arxiv.org/abs/2510.04030) | - |
| 2026 | arXiv | ExtremeWhenBench | [Natural-Language Temporal Grounding in Hour-Long Videos is a Search Problem: A Benchmark and Empirical Decomposition](https://arxiv.org/abs/2606.12300) | [Code](https://github.com/naver-ai/ExtremeWhenBench) |
| 2026 | arXiv | Moment-Video | [Moment-Video: Diagnosing Temporal Fidelity of Video MLLMs on Momentary Visual Events](https://arxiv.org/abs/2606.02522) | - |
| 2026 | arXiv | CoMET-Bench | [Conditional Multi-Event Temporal Grounding in Long-Form Video](https://arxiv.org/abs/2606.15320) | - |
| 2026 | arXiv | AnyGroundBench | [AnyGroundBench: A Multi-Domain Adaptation Benchmark for Video Grounding in VLMs](https://arxiv.org/abs/2607.02269) | [Code](https://github.com/rinost081/AnyGroundBench) |
| 2026 | arXiv | CameraMotionDataset | [Geometry-Guided Camera Motion Understanding in VideoLLMs](https://arxiv.org/abs/2603.13119) | - |
| 2026 | arXiv | VISTA | [VISTA: Video Interaction Spatio-Temporal Analysis Benchmark](https://arxiv.org/abs/2605.01391) | - |
| 2026 | arXiv | GST-Bench | [GST-Bench: Can VLMs Develop Global Spatial Awareness from Video?](https://arxiv.org/abs/2608.05747) | [Project](https://qwerirwq.github.io/GST-Bench/) |
| 2026 | EMNLP Findings | TempCloze | [TempCloze: Can Video-LLMs Identify the Missing Middle?](https://arxiv.org/abs/2609.01515) | [Code](https://github.com/CedricPei/Temporal-Cloze) |
| 2026 | arXiv | MotionBlind | [MotionBlind: Probing the Illusion of Motion Understanding in Video-LLMs](https://arxiv.org/abs/2609.09528) | - |
| 2026 | NeurIPS | MVVBench | [MVVBench: Benchmarking 4D Reasoning in Vision-Language Models](https://arxiv.org/abs/2609.30952) | - |
| 2026 | arXiv | — | [Reasoning over Video: Evaluating How MLLMs Extract, Integrate, and Reconstruct Spatiotemporal Evidence](https://arxiv.org/abs/2603.13091) | - |

#### 5.2.3 Complex Reasoning

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2025 | arXiv | VCR-Bench | [VCR-Bench: A Comprehensive Evaluation Framework for Video Chain-of-Thought Reasoning](https://arxiv.org/abs/2504.07956) | [Code](https://github.com/zhishuifeiqian/VCR-Bench) |
| 2026 | CVPR | V-STaR | [V-STaR: Benchmarking Video-LLMs on Video Spatio-Temporal Reasoning](https://arxiv.org/abs/2503.11495) | [Code](https://github.com/V-STaR-Bench/V-STaR) |
| 2025 | ICCV | MINERVA | [MINERVA: Evaluating Complex Video Reasoning](https://arxiv.org/abs/2505.00681) | [Code](https://github.com/google-deepmind/neptune) |
| 2025 | ICCV | Video-TT | [Towards Video Thinking Test: A Holistic Benchmark for Advanced Video Reasoning and Understanding](https://arxiv.org/abs/2507.15028) | [Project](https://zhangyuanhan-ai.github.io/video-tt) |
| 2025 | arXiv | MMR-V | [MMR-V: What's Left Unsaid? A Benchmark for Multimodal Deep Reasoning in Videos](https://arxiv.org/abs/2506.04141) | [Project](https://mmr-v.github.io/) |
| 2025 | arXiv | SEED-Bench-R1 | [Exploring the Effect of Reinforcement Learning on Video Understanding: Insights from SEED-Bench-R1](https://arxiv.org/abs/2503.24376) | [Code](https://github.com/TencentARC/SEED-Bench-R1) |
| 2026 | ICLR | VideoReasonBench | [VideoReasonBench: Can MLLMs Perform Vision-Centric Complex Video Reasoning?](https://arxiv.org/abs/2505.23359) | [Code](https://github.com/llyx97/video_reason_bench) |
| 2025 | arXiv | Know-Show | [Know-Show: Benchmarking Video-Language Models on Spatio-temporal Grounded Reasoning](https://arxiv.org/abs/2510.10202) | - |
| 2026 | arXiv | VideoZeroBench | [VideoZeroBench: Probing the Limits of Video MLLMs with Spatio-Temporal Evidence Verification](https://arxiv.org/abs/2604.01569) | [Code](https://github.com/marinero4972/VideoZeroBench) |
| 2026 | ACL | GameplayQA | [GameplayQA: A Benchmarking Framework for Decision-Dense POV-Synced Multi-Video Understanding of 3D Virtual Agents](https://arxiv.org/abs/2603.24329) | [Project](https://hats-ict.github.io/gameplayqa/) |
| 2026 | CVPR | CaST-Bench | [CaST-Bench: Benchmarking Causal Chain-Grounded Spatio-Temporal Reasoning for Video Question Answering](https://arxiv.org/abs/2605.23216) | [Project](https://woven-by-toyota.github.io/CaST-Bench) |
| 2026 | arXiv | EG-VQA | [EG-VQA: Benchmarking Verifiable Video Question Answering with Grounded Temporal Evidence](https://arxiv.org/abs/2606.24797) | - |
| 2026 | arXiv | VideoGAIA | [VideoGAIA: A Benchmark for General AI Assistants on Agentic Video Understanding](https://arxiv.org/abs/2608.14718) | - |
| 2026 | arXiv | AgentVidBench | [AgentVidBench: A Multi-Hop Video Question Answering Benchmark for Evaluating MLLM Agents](https://arxiv.org/abs/2609.21386) | [Code](https://github.com/krafton-ai/agentvidbench) |
| 2026 | arXiv | LongVidSearch | [LongVidSearch: An Agentic Benchmark for Multi-hop Evidence Retrieval Planning in Long Videos](https://arxiv.org/abs/2603.14468) | - |
| 2026 | arXiv | SVI-Bench | [SVI-Bench: A Dynamic Microworld for Strategic Video Intelligence](https://arxiv.org/abs/2605.31529) | [Code](https://github.com/Texaser/SVI-Bench) |
| 2026 | arXiv | ST-Evidence | [Evidence-Backed Video Question Answering](https://arxiv.org/abs/2607.11862) | - |
| 2026 | arXiv | BVB | [BVB: Benchmarking Agentic Video Understanding via Programmatic Reconstruction in Blender](https://arxiv.org/abs/2609.15478) | [Code](https://github.com/yunlong10/BVB) |
| 2026 | arXiv | Video-Arena | [Video-Arena: A Scalable Agentic Video Benchmark for Spatiotemporal Capability](https://arxiv.org/abs/2610.14158) | [Code](https://github.com/THUSI-Lab/VideoArena) |
| 2026 | arXiv | OmniDR-Bench | [Beyond Watching and Searching: Benchmarking Agents for Video-centered Deep Research Reports](https://arxiv.org/abs/2610.31158) | [Code](https://github.com/marinero4972/OmniDR-Bench) |
| 2026 | arXiv | ViMU | [ViMU: Benchmarking Video Metaphorical Understanding](https://arxiv.org/abs/2605.14607) | [Code](https://github.com/LiQiiiii/Video-Metaphorical-Understanding) |

#### 5.2.4 Long-Context & Streaming Understanding

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2025 | CVPR | MLVU | [MLVU: Benchmarking Multi-task Long Video Understanding](https://arxiv.org/abs/2406.04264) | [Code](https://github.com/JUNJIE99/MLVU) |
| 2025 | ICCV | LongVideoBench | [LongVideoBench: A Benchmark for Long-context Interleaved Video-Language Understanding](https://arxiv.org/abs/2407.15754) | [Code](https://github.com/longvideobench/LongVideoBench) |
| 2025 | ICCV | LVBench | [LVBench: An Extreme Long Video Understanding Benchmark](https://arxiv.org/abs/2406.08035) | [Code](https://github.com/THUDM/LVBench) |
| 2025 | AAAI | ALLVB | [ALLVB: All-in-One Long Video Understanding Benchmark](https://arxiv.org/abs/2503.07298) | [Code](https://github.com/sssecret2333/ALLVB) |
| 2025 | ICLR | CG-Bench | [CG-Bench: Clue-grounded Question Answering Benchmark for Long Video Understanding](https://arxiv.org/abs/2412.12075) | [Code](https://github.com/CG-Bench/CG-Bench) |
| 2026 | ACL Findings | MT-Video-Bench | [MT-Video-Bench: A Holistic Video Understanding Benchmark for Evaluating Multimodal LLMs in Multi-Turn Dialogues](https://arxiv.org/abs/2510.17722) | [Code](https://github.com/Open-Source-LLM/MT-Video-Bench) |
| 2024 | NeurIPS D&B | StreamingBench | [StreamingBench: Assessing the Gap for MLLMs to Achieve Streaming Video Understanding](https://arxiv.org/abs/2411.03628) | [Code](https://github.com/THUDM/StreamingBench) |
| 2025 | CVPR | OVO-Bench | [OVO-Bench: How Far is Your Video-LLMs from Real-World Online Video Understanding?](https://arxiv.org/abs/2501.05510) | [Code](https://github.com/JoeLeelyf/OVO-Bench) |
| 2025 | ICLR | SVBench | [SVBench: A Benchmark with Temporal Multi-turn Dialogues for Streaming Video Understanding](https://arxiv.org/abs/2502.10810) | [Code](https://github.com/yzy-bupt/SVBench) |
| 2025 | CVPR | OmniMMI | [OmniMMI: A Comprehensive Multi-modal Interaction Benchmark in Streaming Video Contexts](https://arxiv.org/abs/2503.22952) | [Project](https://omnimmi.github.io/) |
| 2025 | ICCV | VStream-QA | [Flash-VStream: Memory-Based Real-Time Understanding for Long Video Streams](https://arxiv.org/abs/2406.08085) | [Code](https://github.com/IVGSZ/Flash-VStream) |
| 2025 | NeurIPS | RTV-Bench | [RTV-Bench: Benchmarking MLLM Continuous Perception, Understanding and Reasoning through Real-Time Video](https://arxiv.org/abs/2505.02064) | [Code](https://github.com/LJungang/RTV-Bench) |
| 2025 | CVPR | VideoChat-Online | [Online Video Understanding: OVBench and VideoChat-Online](https://arxiv.org/abs/2501.00584v2) | [Project](https://videochat-online.github.io/) |
| 2026 | arXiv | VideoOdyssey | [VideoOdyssey: A Benchmark for Ultra-Long-Context and Omni-Modal Video Understanding](https://arxiv.org/abs/2605.22907) | - |
| 2026 | arXiv | StreamArena | [StreamArena: Toward Continuous, Interactive, and Long-Horizon Agentic Streaming Video Understanding](https://arxiv.org/abs/2608.05703) | - |
| 2026 | arXiv | SPOT-Bench | [Don't Pause! Every prediction matters in a streaming video](https://arxiv.org/abs/2604.24317) | - |
| 2026 | arXiv | IPIBench | [IPIBench: Evaluating Interactive Proactive Intelligence of MLLMs under Continuous Streams](https://arxiv.org/abs/2605.27074) | - |
| 2026 | arXiv | EGOSTREAM | [EGOSTREAM: A Diagnostic Benchmark for Streaming Episodic Memory in Egocentric Vision](https://arxiv.org/abs/2605.31557) | - |
| 2026 | arXiv | X-Stream | [X-Stream: Exploring MLLMs as Multiplexers for Multi-Stream Understanding](https://arxiv.org/abs/2606.02482) | [Code](https://github.com/PeiwenSun2000/X-Stream) |
| 2026 | EMNLP | OVO-S-Bench | [OVO-S-Bench: A Hierarchical Benchmark for Streaming Spatial Intelligence in Multimodal LLMs](https://arxiv.org/abs/2606.03890) | [Code](https://github.com/InternLM/OVO-S-Bench) |
| 2026 | EMNLP Findings | StreamMemBench | [StreamMemBench: Streaming Evaluation of Agent Memory for Future-Oriented Assistance](https://arxiv.org/abs/2606.14571) | - |
| 2026 | arXiv | TRACE | [TRACE: Temporal Audit and Condition-aware Evaluation of Streaming Video Understanding](https://arxiv.org/abs/2609.30670) | [Code](https://github.com/om-ai-lab/trace-bench) |
| 2026 | arXiv | MM-Lifelong | [Towards Multimodal Lifelong Understanding: A Dataset and Agentic Baseline](https://arxiv.org/abs/2603.05484) | [Code](https://github.com/cg1177/Recursive-Multimodal-Agent) |

#### 5.2.5 Domain-Specific Knowledge

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2025 | CVPR | MMVU | [MMVU: Measuring Expert-Level Multi-Discipline Video Understanding](https://arxiv.org/abs/2501.12380) | [Code](https://github.com/yale-nlp/MMVU) |
| 2026 | ACL | Video-MMMU | [Video-MMMU: Evaluating Knowledge Acquisition from Multi-Discipline Professional Videos](https://arxiv.org/abs/2501.13826) | [Code](https://github.com/EvolvingLMMs-Lab/VideoMMMU) |
| 2026 | ICLR | ExpVid | [ExpVid: A Benchmark for Experiment Video Understanding & Reasoning](https://arxiv.org/abs/2510.11606) | - |
| 2025 | ICCVW | Video-MMLU | [Video-MMLU: A Massive Multi-Discipline Lecture Understanding Benchmark](https://arxiv.org/abs/2504.14693) | [Code](https://github.com/Espere-1119-Song/Video-MMLU) |
| 2025 | arXiv | BEAR | [BEAR: Benchmarking and Enhancing Multimodal Language Models for Atomic Embodied Capabilities](https://arxiv.org/abs/2510.08759) | [Code](https://github.com/aiwen-li/BEAR) |
| 2026 | arXiv | DVBench | [DVBench: Benchmarking MLLMs for Understanding Dynamic Charts and Narratives in Data Videos](https://arxiv.org/abs/2608.29711) | - |
| 2026 | arXiv | DataVista | [DataVista: Diagnosing Multimodal LLMs on Data Video Understanding](https://arxiv.org/abs/2610.11993) | [Code](https://github.com/HKUSTDial/DataVista) |

#### 5.2.6 Omnimodal Collaboration

| Year | Venue | Acronym | Paper | Code / Project |
| :---: | :---: | :---: | :--- | :---: |
| 2026 | ICLR | WorldSense | [WorldSense: Evaluating Real-world Omnimodal Understanding for Multimodal LLMs](https://arxiv.org/abs/2502.04326) | [Code](https://github.com/jaaackhongggg/WorldSense) |
| 2026 | ICLR | OmniVideoBench | [OmniVideoBench: Towards Audio-Visual Understanding Evaluation for Omni MLLMs](https://arxiv.org/abs/2510.10689) | - |
| 2025 | CVPR | LongVALE | [LongVALE: Vision-Audio-Language-Event Benchmark Towards Time-Aware Omni-Modal Perception of Long Videos](https://arxiv.org/abs/2411.19772) | [Code](https://github.com/ttgeng233/LongVALE) |
| 2026 | ACL Findings | LongInsightBench | [LongInsightBench: A Comprehensive Benchmark for Evaluating Omni-Modal Models on Human-Centric Long-Video Understanding](https://arxiv.org/abs/2510.17305) | - |
| 2026 | arXiv | LVOmniBench | [LVOmniBench: Pioneering Long Audio-Video Understanding Evaluation for Omnimodal LLMs](https://arxiv.org/abs/2603.19217) | - |
| 2026 | arXiv | MMOU | [MMOU: A Massive Multi-Task Omni Understanding and Reasoning Benchmark for Long and Complex Real-World Videos](https://arxiv.org/abs/2603.14145) | - |
| 2026 | ICLR | OmniCaptioner | [OmniCaptioner: One Captioner to Rule Them All](https://arxiv.org/abs/2504.07089) | [Code](https://github.com/Alpha-Innovator/OmniCaptioner) |
| 2026 | arXiv | OMD-Bench | [Omni-Modal Dissonance Benchmark: Systematically Breaking Modality Consensus to Probe Robustness and Calibrated Abstention](https://arxiv.org/abs/2603.27187) | - |
| 2026 | AAAI | LiViBench | [LiViBench: An Omnimodal Benchmark for Interactive Livestream Video Understanding](https://arxiv.org/abs/2601.15016) | - |
| 2026 | ECCV | Video-HolmesV2 | [Video-HolmesV2: Can MLLMs Reason with Spatio-Temporal Audio-Visual Evidence in Long Videos?](https://arxiv.org/abs/2609.17248) | - |
| 2026 | arXiv | OmniCompass | [OmniCompass: A Holistic Benchmark for Omni-Modal Video Grounding and Understanding](https://arxiv.org/abs/2610.18829) | - |
| 2026 | arXiv | OmniPro | [OmniPro: A Comprehensive Benchmark for Omni-Proactive Streaming Video Understanding](https://arxiv.org/abs/2605.18577) | [Code](https://github.com/RuixiangZhao/OmniPro) |
| 2026 | arXiv | OmniInteract | [OmniInteract: Benchmarking Real-World Streaming Interaction for Real-Time Omnimodal Assistants](https://arxiv.org/abs/2605.26485) | [Code](https://github.com/Lucky-Lance/OmniInteract) |
| 2026 | arXiv | OmniCap-IF | [OmniCap-IF: Benchmarking and Improving Instruction Following Abilities for Omni-Video Captioning](https://arxiv.org/abs/2606.08572) | [Code](https://github.com/NJU-LINK/omnicap-if) |
| 2026 | arXiv | OmniAssistBench | [OmniAssistBench: Assistant-style Interaction Benchmark for Omni-LLMs](https://arxiv.org/abs/2608.21360) | [Code](https://github.com/XianyunSun/OmniAssistBench) |
| 2026 | arXiv | AVID | [AVID: A Benchmark for Omni-Modal Audio-Visual Inconsistency Understanding via Agent-Driven Construction](https://arxiv.org/abs/2604.13593) | - |
| 2026 | arXiv | TraceAV-Bench | [TraceAV-Bench: Benchmarking Multi-Hop Trajectory Reasoning over Long Audio-Visual Videos](https://arxiv.org/abs/2605.07593) | - |
| 2026 | NeurIPS | OmniCapBench | [OmniCapBench: A Deep-Structured Evaluation Framework for Fine-Grained Audio-Visual Captioning](https://arxiv.org/abs/2610.12458) | [Code](https://github.com/Tencent-Hunyuan/OmniCapBench) |
| 2026 | ICML | AVI-Bench | [AVI-Bench: Toward Human-like Audio-Visual Intelligence of Omni-MLLMs](https://arxiv.org/abs/2606.07643) | - |

---

## 6. Future Directions

Open problems highlighted by the survey:

- **Spatial reasoning in video understanding** — bridging object-level and scene-level spatial understanding for embodied / 3D-aware applications.
- **Multi-video and multi-segment temporal grounding** — set-based retrieval + refinement under verifiable rewards.
- **Hour-scale video understanding with structured memory** — multi-level memory with evidence pointers and learned write/forget policies.
- **Efficient and verifiable video reasoning** — budgeted evidence search jointly optimizing answer correctness, evidence alignment, and compactness.
- **Streaming egocentric video understanding** — stateful, goal-driven streaming memory with proactive timing for embodied agents.

---

## Citation

If you find this survey useful, please consider citing:

```bibtex
@article{meng2026watch,
  title   = {Watch, Remember, Reason: Human-View Video Understanding with MLLMs},
  author  = {Meng, Jiahao and Tan, Yue and Xu, Qi and Gao, Kuan and Liu, Weisong and Li, Yanwei and Li, Jason and Kong, Lingdong and Wang, Haochen and Zhou, Qianyu and Zhang, Jiangning and Cheng, Guangliang and Tong, Yunhai and Qi, Lu and Yang, Minghsuan},
  journal = {arXiv preprint arXiv:2606.07433},
  year    = {2026}
}
```

## Contributing

Contributions are welcome — please open a PR to add a missing paper, dataset, or benchmark. When adding an entry, place it in the most specific subsection that fits the taxonomy and follow the existing column order. Papers are listed roughly in chronological order within each table.
