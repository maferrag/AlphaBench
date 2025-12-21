# α³-Bench: An Open Benchmark Dataset for Conversational Reasoning in Autonomous UAV Systems

α³-Bench is an open, large-scale benchmark dataset for evaluating **LLM-based agents** in **autonomous UAV systems** through **multi-turn conversational reasoning** under realistic **6G network conditions**.  
It formulates UAV autonomy as a dialogue-driven decision-making problem, enabling systematic assessment of reasoning, safety, interaction quality, and network-aware control.

🌐 **Project Page**: https://github.com/maferrag/AlphaBench 
📄 **Research Paper**: α³-Bench: Who Wins the Conversational Reasoning Challenge for LLM Agents in 6G-Enabled Autonomous UAV Systems?

---

## Overview
Modern UAV systems increasingly rely on **Large Language Models (LLMs)** as high-level decision-makers. However, existing benchmarks lack the ability to evaluate **conversational, agentic reasoning** under realistic communication and networking constraints.

**α³-Bench** addresses this gap by providing a reproducible benchmark that captures:
- Dialogue-driven UAV mission execution  
- Dynamic 6G network conditions (latency, bandwidth, disruptions)  
- Safety-critical and resource-constrained decision-making  

The benchmark enables principled evaluation of **agentic autonomy**, where LLMs reason, plan, and act through structured conversations with the environment.

---

## Key Contributions
- **Conversational UAV Benchmark**: UAV autonomy modeled as multi-turn dialogue between agent and environment  
- **Large-Scale Dataset**: 100,000+ conversational mission episodes  
- **6G-Aware Evaluation**: Explicit modeling of latency, bandwidth, and communication failures  
- **Composite α³ Metric**: Integrates mission success, safety, dialogue quality, tool-use consistency, and communication efficiency  
- **Reproducible & Extensible**: Designed for benchmarking, training, and analysis of LLM agents  

---

## Dataset Overview
- **Domain**: Autonomous UAV systems, conversational AI, 6G networks  
- **Task Type**: Multi-turn conversational reasoning & decision-making  
- **Scale**: 100,000+ dialogue episodes  
- **Agents**: LLM-based decision agents  
- **Environment**: Dynamic missions with safety and network constraints  

Each episode consists of structured dialogue turns requiring the agent to interpret observations, reason over constraints, and select actions under uncertainty.

---

## Data Format
Episodes are provided in **JSONL** format:

```json
{
  "episode_id": "uav_042193",
  "network_profile": {
    "latency_ms": 18,
    "bandwidth_mbps": 120
  },
  "dialogue": [
    {"role": "environment", "content": "Mission initialized. Deliver package to Zone B."},
    {"role": "agent", "content": "Plan route avoiding restricted airspace."},
    {"role": "environment", "content": "Weather deteriorating. Wind speed increased."}
  ],
  "actions": [
    {"type": "navigate", "parameters": {"altitude": 120, "speed": 15}}
  ],
  "outcome": "success"
}
```

---

## Evaluation
α³-Bench evaluates LLM agents using the **α³ metric**, combining:
- Mission completion and efficiency  
- Safety and regulatory compliance  
- Conversational coherence  
- Tool-use and action consistency  
- Network robustness  
- Communication efficiency  

Full evaluation methodology is described in the accompanying paper.

---

## Repository Structure
```
alpha3-bench/
├── data/
│   ├── train/
│   ├── validation/
│   └── test/
├── docs/
│   ├── index.html      # Project website
│   └── paper.pdf
├── scripts/            # Evaluation utilities
├── README.md
├── CITATION.bib
└── LICENSE
```

> **Note**: Dataset files will be released upon publication / finalization.

---

## Citation
If you use **α³-Bench**, please cite:

```bibtex
@article{ferrag2026alpha3,
  title={α3-Bench: Who Wins the Conversational Reasoning Challenge for LLM Agents in 6G-Enabled Autonomous UAV Systems?},
  author={Ferrag, Mohamed Amine and Lakas, Abderrahmane and Debbah, Merouane},
  year={2026}
}
```

---

## Authors
- **Mohamed Amine Ferrag**  
- **Abderrahmane Lakas**  
- **Merouane Debbah**

---

## License
The dataset is released under the **Creative Commons Attribution 4.0 (CC BY 4.0)** license unless otherwise specified.

---

## Contact
For questions, issues, or collaboration:
- 📧 mohamed.ferrag@uaeu.ac.ae  
- 🌐 https://github.com/maferrag
