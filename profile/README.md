# Zen LM

Frontier language models from 600M to 480B parameters. Open-weight models optimized for edge devices through cloud-scale deployments, built on the Zen architecture with efficient inference via Rust, MLX, and GGUF.

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

Zen LM develops state-of-the-art language models spanning ten modalities from 600M (embedded) to 480B (frontier research). All models use the Zen architecture with RoPE embeddings, SwiGLU activation, grouped-query attention, and Flash Attention 2. Available through the Hanzo LLM Gateway, Hugging Face, vLLM, and local inference via MLX/GGUF.

## Quick Start

```python
# Using Hanzo LLM Gateway
from hanzo import Client

client = Client()
response = client.chat.completions.create(
    model="zenlm/zen4-pro",
    messages=[{"role": "user", "content": "Hello!"}]
)

# Using Transformers
from transformers import AutoModelForCausalLM, AutoTokenizer
model = AutoModelForCausalLM.from_pretrained("zenlm/zen4-pro")
```

## Model Family

### Language Models

| Model | Parameters | Context | Use Case |
|-------|------------|---------|----------|
| [zen-coder-480b](https://huggingface.co/zenlm/zen-coder-480b-instruct) | 480B (MoE) | 256K | Frontier code |
| [zen4-max](https://huggingface.co/zenlm/zen4-max) | 397B (MoE) | 128K | Frontier reasoning |
| [zen-max](https://huggingface.co/zenlm/zen-max) | 235B (MoE) | 128K | Production flagship |
| [zen4-thinking](https://huggingface.co/zenlm/zen4-thinking) | 80B (MoE) | 128K | Deep reasoning |
| [zen4-coder-pro](https://huggingface.co/zenlm/zen4-coder-pro) | 80B (MoE) | 128K | Professional code |
| [zen-voyager](https://huggingface.co/zenlm/zen-voyager) | 32B | 128K | Balanced |
| [zen4-mini](https://huggingface.co/zenlm/zen4-mini) | 8B | 128K | Fast inference |
| [zen-eco](https://huggingface.co/zenlm/zen-eco) | 4B | 32K | Edge devices |
| [zen-nano](https://huggingface.co/zenlm/zen-nano) | 0.6B | 8K | Embedded |

### Multimodal

| Model | Type | Description |
|-------|------|-------------|
| [zen-omni](https://huggingface.co/zenlm/zen-omni) | Audio+Vision | Hypermodal 30B MoE |
| [zen-vl](https://huggingface.co/zenlm/zen-vl-8b-instruct) | Vision | Vision-language models (4B/8B/30B) |
| [zen-video](https://huggingface.co/zenlm/zen-video) | Video | High-quality video synthesis |
| [zen-scribe](https://huggingface.co/zenlm/zen-scribe) | Speech | Speech recognition |
| [zen-translator](https://huggingface.co/zenlm/zen-translator) | Translation | Real-time multimodal translation |

## Core Projects

| Project | Description |
|---------|-------------|
| [zen](https://github.com/zenlm/zen) | Zen AI model family -- efficient models for edge and cloud |
| [engine](https://github.com/zenlm/engine) | High-performance inference engine -- Rust/MLX/GGUF |
| [gym](https://github.com/zenlm/gym) | Unified fine-tuning for 100+ LLMs and VLMs |
| [zen-omni](https://github.com/zenlm/zen-omni) | Zen-Omni 30B -- hypermodal AI with MLX/GGUF |
| [docs](https://github.com/zenlm/docs) | Documentation and model cards |

## Ecosystem

| Organization | Focus | Link |
|---|---|---|
| **Hanzo AI** | AI infrastructure, LLM gateway, MCP tools | [github.com/hanzoai](https://github.com/hanzoai) |
| **Lux Network** | Post-quantum blockchain, FHE, multi-consensus | [github.com/luxfi](https://github.com/luxfi) |
| **Zen LM** | Frontier language models, 600M-480B parameters | [github.com/zenlm](https://github.com/zenlm) |
| **Zoo Labs** | Open AI research, DeSci, 501(c)(3) foundation | [github.com/zoo-labs](https://github.com/zoo-labs) |
| **Lux FHE** | Fully homomorphic encryption research + SDK | [github.com/luxfhe](https://github.com/luxfhe) |
| **Lux C++** | High-performance C++ libraries | [github.com/luxcpp](https://github.com/luxcpp) |
| **Hanzo KMS** | Enterprise secret management | [github.com/hanzokms](https://github.com/hanzokms) |
| **Hanzo ID** | Identity, OAuth2/OIDC, WebAuthn | [github.com/hanzoid](https://github.com/hanzoid) |

### Links
- [Papers](https://github.com/luxfi/papers) -- 329+ research papers
- [Stats](https://zeekay.github.io/stats/) -- 38,906+ commits, 59M net LOC
- [Security](https://github.com/luxfi/node/blob/main/SECURITY.md) -- cryptographic audit trail
- [History](https://github.com/luxfi/node/blob/main/HISTORY.md) -- 2008-2026 timeline

## Resources

- [zenlm.org](https://zenlm.org) -- Website
- [huggingface.co/zenlm](https://huggingface.co/zenlm) -- Models on Hugging Face
- [github.com/zenlm/docs](https://github.com/zenlm/docs) -- Documentation

Apache 2.0 for code, model-specific licenses for weights.

*Co-developed by [Hanzo AI](https://hanzo.ai) and [Zoo Labs](https://zoo.ngo)*
