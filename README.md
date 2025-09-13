# RW-Steering: Context Engineering for Trustworthiness

[![arXiv](https://img.shields.io/badge/arXiv-2509.04500-b31b1b.svg)](https://arxiv.org/abs/2509.04500)

**Rescorla–Wagner Steering Under Mixed and Inappropriate Contexts**

A simple, generalizable approach to make LLMs internally identify and ignore inappropriate signals in mixed contexts.

## 🌟 Overview

RW-Steering introduces a novel method to address the vulnerability of Large Language Models (LLMs) when exposed to mixed contexts containing both appropriate and inappropriate content. By adapting the Rescorla–Wagner (RW) model from classical conditioning theory, we provide a framework to understand and mitigate how competing signals steer LLM behavior.

### Key Highlights

- **🔬 Behavioral Insight**: Small contamination can over-steer LLMs; RW conditioning explains the dynamics
- **🧪 Testbed**: Poisoned Context Testbed with realistic mixed contexts to stress-test behavior curves  
- **⚡ Method & Results**: RW-Steering reverses behavior curves and outperforms filtering/alignment baselines (~+39.8% avg. gain)

## 🚀 Quick Start

### Installation

```bash
git clone https://github.com/Oppugno-Rushi/RW-Steering.git
cd RW-Steering
pip install -r requirements.txt
```

## 📊 Results

### Key Findings

1. **Mixed-Context Vulnerability**: Even minimal inappropriate content can disproportionately degrade LLM responses
2. **Robust & Safe LLMs**: RW-Steering generalizes across diverse contamination types and improves response quality by ~39.8%
3. **Behavior Curve Reversal**: Our method successfully reverses undesired behavior curves under mixed contexts
4. **Generalization**: Works across contamination types, positions, and ratios

## 🏗️ Methodology

### Poisoned Context Testbed

We introduce a controlled benchmark pairing real queries with web/RAG-like mixed contexts that blend evidence with inappropriate content (fake news, hate speech, non-factual claims, privacy leaks). By varying contamination type, position, and ratio, we trace behavior curves and demonstrate that even minor contamination can steer answers.

### RW-Steering Approach

Our two-stage fine-tuning method:

1. **Stage 1**: Restructure prompts to encourage joint optimization of inappropriate context detection and human-preferred answer generation
2. **Stage 2**: Supplement training with examples containing inappropriate context segments to address cases where internal judgment may fail

### Rescorla–Wagner Model Adaptation

We adapt the classical conditioning RW model to explain how competing signals in context influence LLM behavior, providing theoretical grounding for our approach.

## 📈 Case Studies

Explore how different approaches handle mixed contexts with inappropriate content:

- **Case 1**: Qwen2 with disproportionate inappropriate context
- **Case 2**: Qwen2 with disproportionate inappropriate context  
- **Case 3**: Phi-2 with proportionate inappropriate context
- **Case 4**: Llama-3.2 with proportionate inappropriate context
- **Case 5**: Gemma-2 with proportionate inappropriate context

## 📚 Citation

If you find RW-Steering useful in your research, please cite our work:

```bibtex
@article{wang2025context,
  title={Context Engineering for Trustworthiness: Rescorla Wagner Steering Under Mixed and Inappropriate Contexts},
  author={Wang, Rushi and Liu, Jiateng and Qian, Cheng and Shen, Yifan and Pan, Yanzhou and Xu, Zhaozhuo and Abbasi, Ahmed and Ji, Heng and Zhang, Denghui},
  journal={arXiv preprint arXiv:2509.04500},
  year={2025}
}
```

## 🔗 Links

- [📝 arXiv Paper](https://arxiv.org/abs/2509.04500)
- [📄 PDF](https://arxiv.org/pdf/2509.04500)
- [💻 Code Repository](https://github.com/Oppugno-Rushi/RW-Steering)
- [🌐 Project Page](https://oppugno-rushi.github.io/rw-steering-page/)

---

**⭐ If you found this project helpful, please give it a star!**