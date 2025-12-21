# α³-Bench Dataset
**Conversational Reasoning Benchmark for LLM Agents in 6G-Enabled Autonomous UAV Systems**

α³-Bench is a large-scale benchmark dataset designed to evaluate **large language model (LLM) agents** acting as high-level controllers for **autonomous UAV systems** through **multi-turn conversational reasoning** under realistic **6G network conditions**.

The benchmark formulates UAV autonomy as a dialogue-driven decision-making problem involving mission planning, perception, safety, communication constraints, and tool interaction.

🌐 **Project Page**: https://USERNAME.github.io/REPO/  
📄 **Paper**: α³-Bench: Who Wins the Conversational Reasoning Challenge for LLM Agents in 6G-Enabled Autonomous UAV Systems?

---

## Dataset Overview
- **Domain**: Autonomous UAV systems, conversational AI, 6G networks  
- **Task Type**: Multi-turn conversational reasoning & decision-making  
- **Scale**: 100,000+ conversational episodes  
- **Agents**: LLM-based decision agents  
- **Environment**: Dynamic UAV missions with realistic 6G constraints  

Each episode consists of structured dialogue turns between an LLM agent and an environment interface, requiring the agent to reason, plan, and act under safety and network limitations.

---

## Benchmark Tasks
α³-Bench evaluates LLM agents across multiple dimensions:
- Mission completion and efficiency  
- Safety and regulatory compliance  
- Tool-use and action consistency  
- Conversational coherence  
- Network robustness (latency, bandwidth variation)  
- Communication cost awareness  

Performance is measured using the composite **α³ metric**, which integrates task outcome, safety, interaction quality, and network-aware reasoning.

---

## Dataset Structure
```
alpha3-bench/
├── data/
│   ├── train/
│   ├── validation/
│   └── test/
│       └── episodes.jsonl
├── docs/
│   ├── index.html      # Project website
│   └── paper.pdf
├── scripts/            # Evaluation / parsing scripts
├── README.md
├── CITATION.bib
└── LICENSE
```

> **Note**: Dataset files will be released upon publication / finalization.

---

## Data Format
Each episode is stored in **JSONL** format:

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
We provide scripts to evaluate LLM agents using the **α³ metric**, combining:
- Task success  
- Safety violations  
- Dialogue quality  
- Network adaptability  
- Communication efficiency  

Detailed evaluation methodology is described in the paper.

---

## Citation
If you use **α³-Bench** or the dataset, please cite:

```bibtex
@article{ferrag2025alpha3,
  title={α3-Bench: Who Wins the Conversational Reasoning Challenge for LLM Agents in 6G-Enabled Autonomous UAV Systems?},
  author={Ferrag, Mohamed Amine and Lakas, Abderrahmane and Debbah, Merouane},
  year={2025}
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
