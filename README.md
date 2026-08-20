<!-- # LLM-Memory-Problem-Paper-List -->

<h1 align="center">
  <strong>LLM-Memory-Problem-Paper-List</strong>
</h1>

<div align="center">

[![Contribution Welcome](https://img.shields.io/badge/Contributions-welcome-Green?logo=mercadopago&logoColor=white)](https://github.com/ESkuratov/LLM-Memory-Problem-Paper-List/pulls)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg?)](LICENSE)
[![GitHub star chart](https://img.shields.io/github/stars/ESkuratov/LLM-Memory-Problem-Paper-List?style=social)](https://star-history.com/#ESkuratov/LLM-Memory-Problem-Paper-List)

</div>

## 📢 News

- [2026/08/20] 🎉 Repository created with 18 curated papers anchored on [Lost in the Middle](https://arxiv.org/abs/2307.03172).

## 👋 Introduction

Large language models (LLMs) are given ever-longer input contexts, yet they demonstrably fail to *use* that context robustly. Performance degrades when the relevant information sits in the middle of a long input — the **"Lost in the Middle"** phenomenon — and models remain fragile at retrieving facts, reasoning across positions, and reconciling external context with their parametric memory.

This list collects papers studying **memory and long-context problems** in LLMs, organized along three lenses:

- **What is the problem?** Mechanisms and explanations of position bias, the "lost in the middle" effect, and how LLMs allocate attention/information across a long context.
- **Why does it happen?** Theoretical and mechanistic accounts, including links to primacy/recency effects in human memory.
- **How to fix it?** Training methods, memory architectures, and retrieval/RAG strategies that mitigate context-loss and improve long-context utilization.

## 💡 Concepts

| Concept | Definition | Related |
|:--------|:-----------|:--------|
| **Lost in the Middle** | U-shaped performance: models use the start/end of a long context well but fail on information in the middle | [2307.03172](#-paper-list) |
| **Needle-in-a-Haystack (NIAH)** | Benchmark task testing single-fact retrieval from a long context | [2411.19360](#-paper-list) |
| **Parametric memory** | Knowledge stored in model weights during pretraining | [2409.08435](#-paper-list) |
| **Context memory** | Knowledge supplied in the input prompt / retrieved documents | [2409.08435](#-paper-list) |
| **Position bias** | Tendency to over-rely on the beginning/end of the input, ignoring the middle | [2603.10123](#-paper-list) |
| **Long-term agent memory** | Persistent memory across sessions for LLM agents | [2602.06052](#-paper-list) |

## 📚 Paper list

### Contents

- [Lost in the Middle: Mechanisms & Explanations](#lost-in-the-middle-mechanisms--explanations)
- [Mitigations & Reasoning](#mitigations--reasoning)
- [Parametric vs. Context Memory](#parametric-vs-context-memory)
- [Long-Context Benchmarks & Surveys](#long-context-benchmarks--surveys)

### Lost in the Middle: Mechanisms & Explanations

| Paper | Year | Focus |
|:------|:----:|:------|
| [Lost in the Middle: How Language Models Use Long Contexts](https://arxiv.org/abs/2307.03172) — N. Liu et al. | 2023 | The anchor paper: position-based degradation on long-context QA & key-value retrieval. |
| [Lost in the Middle, and In-Between: Enhancing LLMs' Ability to Reason Over Long Contexts in Multi-Hop QA](https://arxiv.org/abs/2412.10079) | 2024 | Extends the effect to multi-hop reasoning over long contexts. |
| [Lost in the Middle at Birth: An Exact Theory of Transformer Position Bias](https://arxiv.org/abs/2603.10123) | 2026 | Theory showing the phenomenon is structural, not a Softmax artifact. |
| [Lost in the Middle: An Emergent Property from Information Retrieval Demands in LLMs](https://arxiv.org/abs/2510.10276) | 2025 | Frames the effect as emergent from IR demands; links to primacy/recency in human memory. |
| [Lost-in-the-Middle in Long-Text Generation: Synthetic Dataset, Evaluation Framework, and Mitigation](https://arxiv.org/abs/2503.06868) | 2025 | Moves the problem to long-text *generation*, with dataset + mitigation. |
| [An Adjoint-Sensitivity Framework for Lost-in-the-Middle Phenomena in Causal Residual Transformers](https://arxiv.org/abs/2607.17696) | 2026 | Mechanistic, analytic account of positional influence. |
| [Kinetic theory for Transformers and the lost-in-the-middle phenomenon](https://arxiv.org/abs/2605.09213) | 2026 | Particle-system/kinetic model of causal self-attention explaining the effect. |

### Mitigations & Reasoning

| Paper | Year | Focus |
|:------|:----:|:------|
| [Never Lost in the Middle: Mastering Long-Context QA with Position-Agnostic Decompositional Training](https://arxiv.org/abs/2311.09198) | 2023 | Training-time fix for lost-in-the-middle in long-context QA. |
| [What Works for 'Lost-in-the-Middle' in LLMs? A Study on GM-Extract and Mitigations](https://arxiv.org/abs/2511.13900) | 2025 | Empirical comparison of mitigation strategies. |
| [Reasoning on Multiple Needles in a Haystack](https://arxiv.org/abs/2504.04150) | 2025 | Extends NIAH to multi-fact retrieval + reasoning. |
| [DENIAHL: In-Context Features Influence LLM Needle-In-A-Haystack Abilities](https://arxiv.org/abs/2411.19360) | 2024 | Analyzes which in-context features affect NIAH retrieval. |

### Parametric vs. Memory

| Paper | Year | Focus |
|:------|:----:|:------|
| [When Context Leads but Parametric Memory Follows in LLMs](https://arxiv.org/abs/2409.08435) | 2024 | How models split knowledge between context and parametric memory. |
| [Studying LLM Behaviors Under Context-Memory Conflicts With Real Documents](https://arxiv.org/abs/2404.16032) | 2024 | Behavior when context and parametric memory conflict (RAG knowledge updates). |
| [Gated Differentiable Working Memory for Long-Context Language Modeling](https://arxiv.org/abs/2601.12906) | 2026 | Working memory to fight attention dilution on long contexts. |
| [Needle in the Haystack for Memory Based LLMs](https://arxiv.org/abs/2407.01437) | 2024 | External dynamic memory to improve fact retrieval. |

### Long-Context Benchmarks & Surveys

| Paper | Year | Focus |
|:------|:----:|:-------|
| [Thus Spake Long-Context Large Language Model](https://arxiv.org/abs/2502.17129) | 2025 | Broad survey of long-context capabilities & lifelong learning. |
| [A Survey of Agent Memory in the Second Half: Towards Self-Evolving and Long-Horizon Agents](https://arxiv.org/abs/2602.06052) | 2026 | Survey of memory mechanisms for autonomous, long-horizon agents. |
| [Data Engineering for Scaling Language Models to 128K Context](https://arxiv.org/abs/2402.10171) | 2024 | How data engineering shapes information usage at arbitrary positions. |

## 🔗 Related Frameworks

| Framework | Papers |
|:----------|:-------|
| [Lost in the Middle (anchor)](https://arxiv.org/abs/2307.03172) | [2412.10079](#), [2603.10123](#), [2510.10276](#), [2503.06868](#), [2607.17696](#), [2605.09213](#), [2311.09198](#), [2511.13900](#) |
| [Needle-in-a-Haystack (NIAH)](https://arxiv.org/abs/2307.03172) | [2504.04150](#), [2411.19360](#), [2407.01437](#) |
| [Parametric vs. Context memory](https://arxiv.org/abs/2409.08435) | [2409.08435](#), [2404.16032](#), [2601.12906](#) |
| [Long-context surveys](https://arxiv.org/abs/2502.17129) | [2502.17129](#), [2602.06052](#), [2402.10171](#) |

## 📖 Citation

```bibtex
@misc{liu2023lostmiddle,
  title        = {Lost in the Middle: How Language Models Use Long Contexts},
  author       = {Nelson F. Liu and Kevin Lin and John Hewitt and Ashwin Paranjape and Michele Bevilacqua and Fabio Petroni and Percy Liang},
  year         = {2023},
  eprint       = {2307.03172},
  archivePrefix= {arXiv},
  primaryClass = {cs.CL}
}
```

## 📝 Contributing

1. Fork the repository.
2. Add the entry to the relevant section.
3. **Verify the arXiv link resolves** before opening a PR.
4. Open a pull request.

## ⭐️ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=ESkuratov/LLM-Memory-Problem-Paper-List&type=Date)](https://star-history.com/#ESkuratov/LLM-Memory-Problem-Paper-List)
