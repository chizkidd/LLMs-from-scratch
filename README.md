# LLMs from Scratch 

My personal companion repository and implementation log as I work through Sebastian Raschka's book: **["Build a Large Language Model (from Scratch)"](https://sebastianraschka.com/llms-from-scratch/)**. 

The goal of this repo is to demystify generative AI by building, pre-training, and fine-tuning a GPT-style transformer model entirely from scratch using Python and PyTorch.

---

## Repository Roadmap & Progress

- [x] **Chapter 1: Understanding Large Language Models**
  - Conceptual overview of LLM architectures and applications.
- [x] **Chapter 2: Working with Text Data**
  - Implement text tokenization, Byte-Pair Encoding (BPE), and token/positional embeddings.
- [x] **Chapter 3: Coding Attention Mechanisms**
  - Build scaled dot-product attention, causal masks, and multi-head attention blocks.
- [x] **Chapter 4: Implementing a GPT Model from Scratch to Generate Text**
  - Assemble the complete decoder-only transformer architecture and generate text autoregressively.
- [ ] **Chapter 5: Pretraining on Unlabeled Data**
  - Set up loss functions, training loops, and save/load weights for model pre-training.
- [ ] **Chapter 6: Fine-tuning for Classification**
  - Adapt the pre-trained model for text classification tasks (e.g., spam detection).
- [ ] **Chapter 7: Fine-tuning to Follow Instructions**
  - Supervised fine-tuning (SFT) to build a responsive, instruction-following chat assistant.

---

## Tech Stack & Prerequisites

* **Language:** Python 3.9+
* **Deep Learning Framework:** PyTorch
* **Reference Source:** Official [rasbt/LLMs-from-scratch](https://github.com/rasbt/LLMs-from-scratch) repository

---

## Project Structure

```text
├── archive/                                           # Archived or superseded notebooks
├── ch02-text-data/                                    # Chapter 2: Tokenization & Embedding Pipelines
│   ├── 01-main.ipynb                                  # Core text preprocessing, vocabulary setup, & BPE embeddings
│   ├── 02-bonus_compare-bpe-tiktoken.ipynb            # Performance & footprint: BPE vs Tiktoken
│   ├── 03-bonus_embedding-vs-linear-layer.ipynb       # Proof: Embedding layers equal to one‑hot linear layers
│   ├── 04-bonus_bpe-from-scratch-simple.ipynb         # Minimalist educational BPE implementation
│   └── 05-bonus_bpe-from-scratch.ipynb                # Robust production‑style custom BPE
├── ch03-attention-mechanisms/                         # Chapter 3: Deep Dive into Attention Hooks
│   ├── imgs/                                          # Visual illustrations for attention concepts
│   │   ├── 1_forward-only.jpg
│   │   ├── 2_forward-and-backward.jpg
│   │   └── 3_forward-and-backward-compiled.jpg
│   ├── 01-main.ipynb                                  # Step‑by‑step causal multi‑head attention
│   ├── 02-bonus_efficient-multihead-attn-impl...ipynb # Benchmark: SDPA, FlashAttention, manual
│   ├── 03-bonus_understanding-buffers.ipynb           # PyTorch buffers for non‑trainable state
│   └── README.md
├── ch04-gpt-model/                                    # Chapter 4: Assembling the Full Decoder Architecture
│   ├── 01-main.ipynb                                  # GPT‑style transformer blocks & autoregressive generation
│   ├── 02-bonus_flops-analysis.ipynb                  # Compute efficiency: FLOPs scaling analysis
│   ├── 03-bonus_kv-cache.ipynb                        # Generation speedup via KV caching
│   ├── 04-bonus_gqa.ipynb                             # Grouped‑Query Attention (LLaMA/Mistral style)
│   ├── 05-bonus_mla.ipynb                             # Multi‑head Latent Attention (DeepSeek‑style compression)
│   ├── 06-bonus_swa.ipynb                             # Sliding Window Attention (Mistral / Long context)
│   ├── 07-bonus_moe.ipynb                             # Mixture of Experts (MoE) routing & scaling
│   ├── 08-bonus_deltanet.ipynb                        # Gated DeltaNet: Linear attention alternatives
│   ├── 09-bonus_dsa.ipynb                             # Differentiable Search (or DeepSeek‑style attention variants)
│   ├── 10-bonus_kv-sharing.ipynb                      # (Cross-layer) KV sharing across layers for memory efficiency
│   └── README.md
├── Building LLMs From Scratch.pdf
├── LICENSE
└── README.md
```

---

## Acknowledgments

All credits go to **Sebastian Raschka** for writing the foundational text and providing the official open-source code guidelines. Check out the book on [Manning Publications](https://www.manning.com/books/build-a-large-language-model-from-scratch).
