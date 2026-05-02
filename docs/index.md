# Shunya KV
[![CI](https://github.com/somesh-m/shunya-kv/actions/workflows/ci.yaml/badge.svg?branch=master)](https://github.com/somesh-m/shunya-kv/actions/workflows/ci.yaml)
<p align="left">
  <!-- <a href="https://github.com/somesh-m/shunya-kv/actions/workflows/ci.yaml">
    <img src="https://github.com/somesh-m/shunya-kv/actions/workflows/ci.yaml/badge.svg?branch=master" />
  </a> -->
  <a href="https://github.com/somesh-m/shunya-kv">
    <img src="https://img.shields.io/badge/GitHub-Repository-black?logo=github" />
  </a>

  <img src="https://img.shields.io/badge/Language-C++17-blue" />
  <img src="https://img.shields.io/badge/Framework-Seastar-orange" />
  <img src="https://img.shields.io/badge/Status-Experimental-green" />
</p>
Shunya KV is a high-performance, shard-aware key–value store built on the Seastar framework.

The system is designed around a shared-nothing, per-core architecture to achieve predictable low latency and linear scalability on multi-core machines.

Repository:
https://github.com/somesh-m/shunya-kv

---

#### Architecture

Shunya KV follows these core principles:

- Per-core sharding (shared-nothing design)
- Single-threaded reactor per shard (Seastar model)
- Lock-free execution path
- Explicit backpressure via pipeline control
- Deterministic latency measurement (p50–p99.9)

Networking is supported in both standard TCP mode and DPDK mode for high-throughput environments.

---

#### Design Goals

- Sub-millisecond tail latency under load
- Million+ QPS throughput on commodity hardware
- Core-linear scalability
- Minimal synchronization overhead
- Deterministic performance under high concurrency

---

#### Documentations
* [Architecture](architecture/arch_dpdk.md)
* [How client connects in DPDK mode](dpdk_client_connection.md)
* [Performance](perf.md)
* [Installation](installation.md)
---
