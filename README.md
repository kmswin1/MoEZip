
# MoEZip: Routing-Aware KV Cache Compression for Sparse Mixture-of-Experts LLMs

**NeurIPS 2026** | [Paper](https://openreview.net/pdf?id=R8hTibgKBX)

Official implementation of **MoEZip**, a routing-aware KV cache compression method for sparse Mixture-of-Experts (MoE) language models.

MoEZip addresses a key limitation of existing KV cache compression methods: evicting KV entries can alter expert routing decisions and degrade generation quality in MoE models.

To address this, MoEZip estimates routing sensitivity using Fisher information and combines it with attention-based importance scores to guide KV cache eviction.

### Key Results

At **10% KV cache retention**, MoEZip outperforms the state-of-the-art baseline by:

- **LongBench:** +24 points (2.3× higher score)
- **RULER:** +20 points (4.9× higher score)

## Installation

MoEZip builds on [NVIDIA KVPress](https://github.com/NVIDIA/kvpress).

Install KVPress:

```bash
pip install kvpress
```

Install any additional dependencies required by this repository.

## Quick Start

Run the provided example:

```bash
bash run_example.sh
```

## Citation

If you find MoEZip useful in your research, please cite our paper:

```bibtex
@inproceedings{kim2026moezip,
  title     = {MoEZip: Routing-Aware KV Cache Compression for Sparse Mixture-of-Experts LLMs},
  author    = {Kim, Minsang and Baek, Seungjun},
  booktitle = {Advances in Neural Information Processing Systems},
  year      = {2026},
  url       = {https://openreview.net/pdf?id=R8hTibgKBX}
}
```

## Acknowledgments

This implementation builds on [NVIDIA KVPress](https://github.com/NVIDIA/kvpress).
