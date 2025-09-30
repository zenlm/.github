  # Zen LM 🌍

  **Next-Generation AI for Humanity** • Local • Private • Free • Sustainable

  ---

  A groundbreaking collaboration between **[Hanzo AI](https://hanzo.ai)** (Techstars-backed,
  award-winning GenAI lab) and **[Zoo Labs Foundation](https://zoo.ngo)** (501(c)(3) environmental
  non-profit), building AI that runs entirely on your device — no cloud, no subscriptions, no
  surveillance.

  > **"Democratize AI while protecting our planet"**

  ---

  ## 🤗 Complete Model Zoo

  ### 💬 Language Models

  | Model | Size | Description |
  |-------|------|-------------|
  | [**zen-nano**](https://huggingface.co/zenlm/zen-nano) | 0.6B | Ultra-lightweight edge model |
  | [**zen-eco-instruct**](https://huggingface.co/zenlm/zen-eco-instruct) | 4B | Efficient
  instruction-following |
  | [**zen-eco-thinking**](https://huggingface.co/zenlm/zen-eco-thinking) | 4B | Chain-of-thought
  reasoning |
  | [**zen-eco-coder**](https://huggingface.co/zenlm/zen-eco-coder) | 4B | Code generation and
  analysis |
  | [**zen-eco-agent**](https://huggingface.co/zenlm/zen-eco-agent) | 4B | Tool-calling and functions
  |
  | [**zen-agent**](https://huggingface.co/zenlm/zen-agent) | 4B | Agentic workflows with MCP |
  | [**zen-pro**](https://huggingface.co/zenlm/zen-pro) | 8B | Professional-grade LLM |
  | [**zen-omni**](https://huggingface.co/zenlm/zen-omni) | Multimodal | Vision-language understanding
   |

  ### 🎨 3D & World Generation

  | Model | Type | Description |
  |-------|------|-------------|
  | [**zen-3d**](https://huggingface.co/zenlm/zen-3d) | 3.3B | Controllable 3D asset generation |
  | [**zen-voyager**](https://huggingface.co/zenlm/zen-voyager) | Diffusion | Camera-controlled world
  exploration |
  | [**zen-world**](https://huggingface.co/zenlm/zen-world) | Diffusion | Large-scale world simulation
   |

  ### 🎬 Video Generation

  | Model | Type | Description |
  |-------|------|-------------|
  | [**zen-director**](https://huggingface.co/zenlm/zen-director) | 5B | Text/image-to-video
  generation |
  | [**zen-video**](https://huggingface.co/zenlm/zen-video) | Diffusion | High-quality video synthesis
   |
  | [**zen-video-i2v**](https://huggingface.co/zenlm/zen-video-i2v) | Diffusion | Image-to-video
  animation |

  ### 🎵 Audio Generation

  | Model | Type | Description |
  |-------|------|-------------|
  | [**zen-musician**](https://huggingface.co/zenlm/zen-musician) | 7B | Music generation (lyrics →
  songs) |
  | [**zen-foley**](https://huggingface.co/zenlm/zen-foley) | Diffusion | Video-to-audio Foley effects
   |

  ### 🎨 Creative & Design

  | Model | Type | Description |
  |-------|------|-------------|
  | [**zen-artist**](https://huggingface.co/zenlm/zen-artist) | Multimodal | Creative visual
  generation |
  | [**zen-designer-instruct**](https://huggingface.co/zenlm/zen-designer-instruct) | Multimodal |
  Design instruction following |
  | [**zen-designer-thinking**](https://huggingface.co/zenlm/zen-designer-thinking) | Multimodal |
  Design reasoning |

  ### 💻 Code & Development

  | Model | Type | Description |
  |-------|------|-------------|
  | [**zen-code**](https://huggingface.co/zenlm/zen-code) | 4B | General code generation |
  | [**zen-coder**](https://huggingface.co/zenlm/zen-coder) | 4B | Advanced coding assistant |
  | [**zen-code-docs**](https://huggingface.co/zenlm/zen-code-docs) | 4B | Documentation generation |
  | [**zen-code-action**](https://huggingface.co/zenlm/zen-code-action) | 4B | Code action suggestions
   |

  ### 📝 Content Creation

  | Model | Type | Description |
  |-------|------|-------------|
  | [**zen-blog**](https://huggingface.co/zenlm/zen-blog) | 4B | Blog and article writing |
  | [**zen-scribe**](https://huggingface.co/zenlm/zen-scribe) | 4B | Professional content writing |

  ### 🛡️ Safety & Moderation

  | Model | Type | Description |
  |-------|------|-------------|
  | [**zen-guard**](https://huggingface.co/zenlm/zen-guard) | Classification | Content safety
  detection |
  | [**zen-guard-gen**](https://huggingface.co/zenlm/zen-guard-gen) | 4B | Safe content generation |
  | [**zen-guard-stream**](https://huggingface.co/zenlm/zen-guard-stream) | Classification | Real-time
   safety monitoring |

  ### 🔢 Embeddings

  | Model | Type | Description |
  |-------|------|-------------|
  | [**zen-embedding**](https://huggingface.co/zenlm/zen-embedding) | Embedding | High-quality text
  embeddings |

  ---

  ## Why Zen LM?

  🚀 **Ultra-Efficient** - 4B parameters achieving 70B-class performance • Runs on phones, laptops,
  Raspberry Pi

  🔒 **Truly Private** - 100% local processing • No accounts, no telemetry, no tracking

  🌱 **Environmentally Responsible** - 95% less energy than cloud AI • Carbon-negative operations

  💚 **Free Forever** - Apache 2.0 licensed • No premium tiers or API fees

  ---

  ## 🚀 Quick Start

  ```python
  from transformers import AutoModelForCausalLM, AutoTokenizer

  model = AutoModelForCausalLM.from_pretrained("zenlm/zen-eco-instruct")
  tokenizer = AutoTokenizer.from_pretrained("zenlm/zen-eco-instruct")

  inputs = tokenizer("Explain quantum computing", return_tensors="pt")
  outputs = model.generate(**inputs, max_length=200)
  print(tokenizer.decode(outputs[0]))

  ---
  🏗️ Infrastructure

  https://github.com/zenlm/zen-gym - Unified training platform supporting LoRA, GRPO, DPO, and all
  modern methods

  https://github.com/zenlm/zen-engine - High-performance inference engine (44K tok/s) with
  OpenAI-compatible API

  ---
  📜 License

  Models: Apache 2.0 • Code: MIT License • Privacy: No data collection, ever

  ---
  🏛️ Organizations

  Hanzo AI Inc - Techstars Portfolio • Award-winning GenAI lab • https://hanzo.ai

  Zoo Labs Foundation - 501(c)(3) Non-Profit • Environmental preservation • https://zoolabs.io

  ---
  📮 Contact

  🌐 https://zenlm.org • 💬 https://discord.gg/zenlm • 🐦 https://twitter.com/zenlm_ai • 📧
  hello@zenlm.org
