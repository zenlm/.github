# Zen LM

Frontier language models from 600M to 480B parameters. Open-weight models optimized for edge devices through cloud-scale deployments, built on Qwen3+ architecture with efficient inference via Rust, MLX, and GGUF.

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

Zen LM develops state-of-the-art language models spanning seven sizes from 600M (embedded) to 480B (frontier research). All models use the Qwen3+ architecture with RoPE embeddings, SwiGLU activation, grouped-query attention, and Flash Attention 2. Available through the Hanzo LLM Gateway, Hugging Face, vLLM, and local inference via MLX/GGUF.

## Quick Start

```python
# Using Hanzo LLM Gateway
from hanzo import Client

client = Client()
response = client.chat.completions.create(
    model="zenlm/zen-7b",
    messages=[{"role": "user", "content": "Hello!"}]
)

# Using Transformers
from transformers import AutoModelForCausalLM, AutoTokenizer
model = AutoModelForCausalLM.from_pretrained("zenlm/zen-7b")
```

## Model Family

| Model | Parameters | Context | Use Case |
|-------|------------|---------|----------|
| Zen-480B | 480B (MoE) | 128K | Frontier research |
| Zen-70B | 70B | 128K | Production |
| Zen-32B | 32B (MoE) | 64K | Balanced |
| Zen-7B | 7B | 32K | Fast inference |
| Zen-3B | 3B | 16K | Edge devices |
| Zen-1.5B | 1.5B | 8K | Mobile |
| Zen-600M | 600M | 4K | Embedded |

## Core Projects

| Project | Description |
|---------|-------------|
| [zen](https://github.com/zenlm/zen) | Zen AI model family — efficient models for edge and cloud |
| [engine](https://github.com/zenlm/engine) | High-performance inference engine — Rust/MLX/GGUF |
| [gym](https://github.com/zenlm/gym) | Unified fine-tuning for 100+ LLMs and VLMs |
| [zen-omni](https://github.com/zenlm/zen-omni) | Zen-Omni 30B — hypermodal AI with MLX/GGUF |
| [docs](https://github.com/zenlm/docs) | Documentation and model cards |

## Benchmarks

| Model | MMLU | HumanEval | GSM8K | MT-Bench |
|-------|------|-----------|-------|----------|
| Zen-70B | 82.3 | 71.2 | 85.4 | 8.9 |
| Zen-32B | 78.1 | 65.8 | 79.2 | 8.4 |
| Zen-7B | 68.5 | 52.4 | 62.1 | 7.8 |
| Zen-3B | 58.2 | 38.6 | 48.3 | 7.1 |

## Related Organizations

| Organization | Focus |
|--------------|-------|
| [Hanzo AI](https://github.com/hanzoai) | AI infrastructure — LLM gateway, MCP, agents |
| [Lux Network](https://github.com/luxfi) | Post-quantum blockchain, FHE, cross-chain |
| [Zoo Labs](https://github.com/zoo-labs) | Open AI research network (501c3) |

## Resources

- [zenlm.org](https://zenlm.org) — Website
- [huggingface.co/zenlm](https://huggingface.co/zenlm) — Models on Hugging Face
- [docs.zenlm.ai](https://docs.zenlm.ai) — Documentation

Apache 2.0 for code, model-specific licenses for weights.

*Co-developed by [Hanzo AI](https://hanzo.ai) and [Zoo Labs](https://zoo.ngo)*
