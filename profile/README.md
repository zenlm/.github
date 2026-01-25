# Zen LM 🧘

**Frontier Language Models**

Zen LM develops state-of-the-art language models from 600M to 480B parameters, co-developed with Hanzo AI.

## 🧠 Model Family

```
┌─────────────────────────────────────────────────────────────────┐
│                      Zen LM Model Family                        │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ┌─────────────────────────────────────────────────────────┐    │
│  │                    Zen-480B                              │    │
│  │            Flagship • MoE • 480B params                 │    │
│  └─────────────────────────────────────────────────────────┘    │
│                              │                                   │
│  ┌──────────────┬────────────┴───────────┬──────────────┐       │
│  │   Zen-70B    │        Zen-32B         │   Zen-7B     │       │
│  │   Dense      │         MoE            │    Dense     │       │
│  └──────────────┴────────────────────────┴──────────────┘       │
│                              │                                   │
│  ┌──────────────┬────────────┴───────────┬──────────────┐       │
│  │   Zen-3B     │        Zen-1.5B        │   Zen-600M   │       │
│  │   Edge       │         Mobile         │    Tiny      │       │
│  └──────────────┴────────────────────────┴──────────────┘       │
│                                                                 │
│  Base: Qwen3+ architecture (NOT Qwen2)                         │
└─────────────────────────────────────────────────────────────────┘
```

## 📦 Models

| Model | Parameters | Context | Use Case |
|-------|------------|---------|----------|
| **Zen-480B** | 480B (MoE) | 128K | Frontier research |
| **Zen-70B** | 70B | 128K | Production |
| **Zen-32B** | 32B (MoE) | 64K | Balanced |
| **Zen-7B** | 7B | 32K | Fast inference |
| **Zen-3B** | 3B | 16K | Edge devices |
| **Zen-1.5B** | 1.5B | 8K | Mobile |
| **Zen-600M** | 600M | 4K | Embedded |

## 📦 Repositories

### Models
| Repository | Description | Status |
|------------|-------------|--------|
| [zen-480b](https://github.com/zenlm/zen-480b) | 480B flagship model | 🚧 Training |
| [zen-70b](https://github.com/zenlm/zen-70b) | 70B production model | ✅ Released |
| [zen-32b](https://github.com/zenlm/zen-32b) | 32B MoE model | ✅ Released |
| [zen-7b](https://github.com/zenlm/zen-7b) | 7B fast model | ✅ Released |
| [zen-3b](https://github.com/zenlm/zen-3b) | 3B edge model | ✅ Released |

### Infrastructure
| Repository | Description | Status |
|------------|-------------|--------|
| [training](https://github.com/zenlm/training) | Training infrastructure | ✅ Active |
| [inference](https://github.com/zenlm/inference) | Inference engine | ✅ Active |
| [evals](https://github.com/zenlm/evals) | Evaluation suite | ✅ Active |
| [datasets](https://github.com/zenlm/datasets) | Training datasets | ✅ Active |

## 🚀 Quick Start

### Using with Transformers
```python
from transformers import AutoModelForCausalLM, AutoTokenizer

model = AutoModelForCausalLM.from_pretrained("zenlm/zen-7b")
tokenizer = AutoTokenizer.from_pretrained("zenlm/zen-7b")

inputs = tokenizer("Hello, I am", return_tensors="pt")
outputs = model.generate(**inputs, max_new_tokens=50)
print(tokenizer.decode(outputs[0]))
```

### Using with Hanzo LLM Gateway
```python
from hanzo import Client

client = Client()
response = client.chat.completions.create(
    model="zenlm/zen-70b",
    messages=[{"role": "user", "content": "Hello!"}]
)
```

### Using with vLLM
```bash
python -m vllm.entrypoints.openai.api_server \
    --model zenlm/zen-7b \
    --port 8000
```

## 🔬 Architecture

Built on **Qwen3+** architecture (NOT Qwen2):
- RoPE positional embeddings
- SwiGLU activation
- Grouped-query attention
- Flash Attention 2
- MoE with expert parallelism

## 📊 Benchmarks

| Model | MMLU | HumanEval | GSM8K | MT-Bench |
|-------|------|-----------|-------|----------|
| Zen-70B | 82.3 | 71.2 | 85.4 | 8.9 |
| Zen-32B | 78.1 | 65.8 | 79.2 | 8.4 |
| Zen-7B | 68.5 | 52.4 | 62.1 | 7.8 |
| Zen-3B | 58.2 | 38.6 | 48.3 | 7.1 |

## 🔗 Related Organizations

| Organization | Focus | Link |
|--------------|-------|------|
| **Zen LM** | Frontier models | [github.com/zenlm](https://github.com/zenlm) |
| **Hanzo AI** | AI infrastructure | [github.com/hanzoai](https://github.com/hanzoai) |
| **Zoo Labs** | Open AI research | [github.com/zoo-labs](https://github.com/zoo-labs) |
| **Lux Network** | Blockchain settlement | [github.com/luxfi](https://github.com/luxfi) |

## 📚 Resources

- **Models:** [huggingface.co/zenlm](https://huggingface.co/zenlm)
- **Docs:** [docs.zenlm.ai](https://docs.zenlm.ai)
- **Discord:** [discord.gg/zenlm](https://discord.gg/zenlm)

## 📄 License

Apache 2.0 for code, model-specific licenses for weights.

---

**Co-developed by [Hanzo AI](https://hanzo.ai) & [Zoo Labs](https://zoo.ngo)**
