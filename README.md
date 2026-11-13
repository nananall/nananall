<div align="center">

# Qiao Guo

**LLM inference engineer** — serving runtime, distributed execution, and the kernel-level details that decide TTFT and tail latency.

SGLang · vLLM · CUDA · Triton · Python · C++

</div>

---

I work on LLM serving infrastructure: the layer where a model's theoretical speed meets
real traffic, real hardware, and real latency targets. Most of what I build runs in a
production environment I can't publish, so what lives here is the reusable part — the
methodology and tooling that makes inference optimization repeatable instead of
heroic.

## What I work on

- **Serving runtime** — request scheduling, continuous batching, KV-cache management in
  SGLang / vLLM
- **Distributed execution** — prefill/decode disaggregation, KV transfer, cross-stage
  overlap, and the capacity math that decides whether any of it pays off
- **Performance engineering** — trace-driven bottleneck location, sampler and metadata
  hot paths, and the TTFT / TPOT / throughput tradeoffs nobody gets for free
- **Hardware porting** — bringing inference stacks onto non-NVIDIA accelerators, including
  the monitoring that tells you whether the port is actually fast

## Open-source work

| Project | What it does |
| :-- | :-- |
| **[continual-inference-optimizer](https://github.com/nananall/continual-inference-optimizer)** | A trace-driven Agent Skill that turns profiling evidence into validated SGLang / vLLM changes: measure → locate the bottleneck → hypothesize → implement → screen → validate → keep or revert. It refuses changes that break correctness, TTFT, TPOT, tail latency or memory constraints, and leaves every winner reproducible and revertible. |
| **[human-code](https://github.com/nananall/human-code)** | The other half of the problem: a code-agent skill that keeps machine-written changes small, readable and scope-controlled, so performance work stays reviewable by whoever inherits it. |

## How I work

1. **Measure before reasoning.** A bottleneck you inferred from reading code is a
   hypothesis, not a finding.
2. **One change per experiment.** Bundled wins are un-attributable wins.
3. **Keep a rollback path, always.** Every kept optimization ships with the evidence and
   the revert instruction next to it.

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![Triton](https://img.shields.io/badge/Triton-2C2C2C?style=flat-square&logo=openai&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![SGLang](https://img.shields.io/badge/SGLang-1F6FEB?style=flat-square&logoColor=white)
![vLLM](https://img.shields.io/badge/vLLM-1F6FEB?style=flat-square&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

## Get in touch

Working on serving performance, disaggregation, or accelerator bring-up? Open an issue on
either repo — I read everything that comes in there.

</div>
