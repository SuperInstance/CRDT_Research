# CRDT Intra-Chip Communication Research

This repository contains comprehensive research on applying Conflict-free Replicated Data Types (CRDTs) to intra-chip communication for AI workloads.

## Overview

This doctoral-level research explores using CRDTs as an alternative to traditional MESI cache coherence protocols for multi-core AI accelerators. Key findings include:

- **98.4% latency reduction** compared to MESI directory protocols
- **52.2% traffic reduction** in cache coherence traffic
- **O(1) scaling** independent of core count

## Contents

### Documents
- `CRDT_Intra_Chip_Doctoral_Dissertation.docx` - Complete doctoral dissertation
- `CRDT_Research_Supplement.docx` - Mathematical foundations and supplementary data
- `CRDT_Intra_Chip_Research_Package.zip` - Complete research package with all files

### Simulation Code (`crdt_simulation/`)
- `thirty_round_simulation.py` - Main simulation framework
- `crdt_vs_mesi_simulator.py` - Core MESI vs CRDT comparison
- `rigorous_traffic_analysis.py` - Traffic validation analysis
- `mathematical_foundations.py` - Mathematical verification scripts

### Analysis Results
- `results/` - Raw simulation results (JSON)
- `reviews/` - Technical review documents
- `analysis_output/` - Generated analysis outputs

## Key Technologies

- **CRDT Types**: TA-CRDT (Tensor Accumulator), State Register CRDT, Set Membership CRDT
- **Baseline**: MESI directory-based cache coherence
- **Workloads**: ResNet-50, BERT, GPT-2/3, LLaMA, Mixtral, ViT, Whisper, SAM

## Mathematical Foundations

The research builds on semilattice theory with three key properties:
1. **Associativity**: (a ⊕ b) ⊕ c = a ⊕ (b ⊕ c)
2. **Commutativity**: a ⊕ b = b ⊕ a
3. **Idempotence**: a ⊕ a = a

These properties enable Strong Eventual Consistency (SEC) without coordination.

## How to Run Simulations

```bash
cd crdt_simulation
pip install -r requirements.txt
python thirty_round_simulation.py
```

## Citation

If you use this research, please cite:
```
[Author]. (2024). CRDT-Based Intra-Chip Communication for AI Workloads: 
A Comparative Analysis with MESI Cache Coherence. Doctoral Dissertation.
```

## License

MIT License - See LICENSE file for details.
