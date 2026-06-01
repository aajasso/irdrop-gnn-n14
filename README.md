# GNN-Based IR Drop Prediction on CircuitNet-N14

**Paper**: GNN-Based IR Drop Prediction on CircuitNet-N14: 
A Graph Attention Network Approach with Cross-Design Generalization  
**Author**: Adriana Arizaga Jasso | Mission College | Santa Clara, CA  
**arXiv**: [link after submission]

GNN-based IR drop prediction on CircuitNet-N14 (14nm).  Dual-head Graph Attention Network with zero-shot cross-design  transfer from RISC-V CPU to GPU accelerator. 
---

## Overview

IRDropGNN is a dual-head Graph Attention Network for predicting 
IR drop on CircuitNet-N14 at the 14nm technology node. 

Key results:
- MAE 11.97 mV on Vortex-small (in-distribution)
- MAE 9.75 mV on NVDLA-small (zero-shot, no retraining)
- First GNN-based IR drop evaluation on CircuitNet-N14

![Architecture](figures/figure3_architecture.png)

---

## How to run

1. Open `gnn-irdrop-n14-final.ipynb` on Kaggle
2. Enable GPU T4 (Settings → Accelerator)
3. Run all cells in order
4. Data downloads automatically in Cell 2 (~3GB total)
5. Training takes ~10 minutes on T4 GPU

---

## Requirements
torch >= 2.1.0
torch_geometric
networkx
numpy
matplotlib

Install on Kaggle: handled automatically in Cell 1.  
Install locally: `pip install -r requirements.txt`

---

## Dataset

CircuitNet-N14 — available free on HuggingFace:  
https://huggingface.co/datasets/CircuitNet/CircuitNet

No registration required. Cell 2 downloads automatically.

---

## Results

| Metric | Vortex (in-dist.) | NVDLA (zero-shot) |
|--------|-------------------|-------------------|
| RMSE (mV) | 47.18 | 27.96 |
| MAE (mV) | 11.97 | 9.75 |
| NRMSE | 0.0343 | 0.0269 |
| Hotspot Acc | 0.321 | 0.202 |

---

## Citation

If you use this work please cite:
[add arXiv citation after submission]

