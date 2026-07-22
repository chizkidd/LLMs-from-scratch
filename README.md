# LLMs from Scratch 

My personal companion repository and implementation log as I work through Sebastian Raschka's book: **["Build a Large Language Model (from Scratch)"](https://sebastianraschka.com/llms-from-scratch/)**. 

The goal of this repo is to demystify generative AI by building, pre-training, and fine-tuning a GPT-style transformer model entirely from scratch using Python and PyTorch.

---

## Repository Roadmap & Progress

- [ ] **Chapter 1: Understanding Large Language Models**
  - Conceptual overview of LLM architectures and applications.
- [ ] **Chapter 2: Working with Text Data**
  - Implement text tokenization, Byte-Pair Encoding (BPE), and token/positional embeddings.
- [ ] **Chapter 3: Coding Attention Mechanisms**
  - Build scaled dot-product attention, causal masks, and multi-head attention blocks.
- [ ] **Chapter 4: Implementing a GPT Model from Scratch to Generate Text**
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

*(Modify this section as your file structure evolves chapter-by-chapter)*
```text
├── ch02-text-data/                 # Chapter 2: Tokenization & Embedding Pipelines
│   ├── 01-main.ipynb               # Core text preprocessing, vocabulary setup, & BPE embeddings
│   ├── 02-bonus_compare-bpe-...    # Performance & vocabulary footprint analysis: BPE vs Tiktoken
│   ├── 03-bonus_embedding-vs-...   # Mathematical proof: Equivalence of Embedding layers & One-Hot Linear weights
│   ├── 04-bonus_bpe-from-scr...    # Minimalist, educational walkthrough of Byte-Pair Encoding logic
│   └── 05-bonus_bpe-from-scr...    # Robust, production-style implementation of custom BPE from scratch
├── ch03-attention-mechanisms/      # Chapter 3: Deep Dive into Attention Hooks
│   ├── 01-main.ipynb               # Step-by-step implementation of Causal Multi-Head Attention
│   ├── 02-bonus_efficient-mu...    # Speed benchmarking: PyTorch SDPA, FlashAttention, & manual implementations
│   └── 03-bonus_understandin...    # Memory management: Registering non-trainable state arrays using PyTorch buffers
├── ch04-gpt-model/                 # Chapter 4: Assembling the Full Decoder Architecture
│   ├── 01-main.ipynb               # Configures GPT-style transformer blocks & autoregressive generation
│   ├── 02-bonus_flops-analyi...    # Compute efficiency: Floating Point Operations (FLOPs) scaling analysis
│   ├── 03-bonus_kv-cache.ipynb     # Generation speedup: Storing past Keys & Values to avoid redundant attention recalculations
│   ├── 04-bonus_gqa.ipynb          # Modern scaling: Grouped-Query Attention (LLaMA/Mistral style) for reduced memory footprint
│   └── 05-bonus_mla.ipynb          # DeepSeek innovation: Multi-head Latent Attention implementation for extreme cache compression
```

---

## Acknowledggments

All credits go to **Sebastian Raschka** for writing the foundational text and providing the official open-source code guidelines. Check out the book on [Manning Publications](https://www.manning.com/books/build-a-large-language-model-from-scratch).
