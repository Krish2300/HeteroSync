# Framework for Resource-Adaptive Acceleration of Iterative Computations on Heterogeneous Low-Cost Devices


> **Official open-source repository for the paper presented at the 27th Annual AeSI CFD Symposium 2026 (11th–12th August 2026, IIT Madras, Chennai).**  
> Currently hosting the symposium paper—we are inviting **founding student contributors and builders** to implement the three software layers from scratch!

---

## Why This Project Exists
Engineering students and independent researchers rarely have access to institutional High-Performance Computing (HPC) clusters, causing simulations and iterative solvers to take hours or days on personal laptops.

Our baseline experiments in ANSYS Fluent demonstrate that **30–56% of solver runtime is wasted** on iterations after physical outputs (such as pressure drop, velocity, or drag) have already stabilised—simply waiting for arbitrary numerical residual thresholds.

This solver-agnostic framework solves that bottleneck without modifying underlying solvers (ANSYS Fluent, OpenFOAM, FEA, ML training loops, or any other iterative computation) by combining **intelligent early stopping** with **opportunistic offloading to devices students already own** (smartphones, old laptops, Raspberry Pis).

---

## System Architecture (Three Integrated Layers)
1. **Convergence Intelligence Engine (CIE):** Monitors solver log streams in real time using sliding-window variance plateau detection and time-series extrapolation to issue physics-aware stop signals.
2. **Heterogeneous Compute Fabric (HCF):** Discovers nearby satellite devices (smartphones, secondary laptops, SBCs) via mDNS or USB and offloads pre/post-processing tasks via a lightweight Python JSON-RPC agent.
3. **Adaptive Surrogate Engine (ASE):** Extracts compact case fingerprints (mesh statistics, boundary conditions, residual trajectories) into a local/federated library to warm-start future similar simulations.

* **Read the Full Paper:** https://github.com/Krish2300/HeteroSync/blob/main/Abstract.pdf

---

## Open Founding Issues (Claim a Task!)
Because this repository starts directly from the symposium architecture specification, **you have complete freedom to create folders, design the structure, and own an entire module.** Pick any of our 6 open tracks in the **Issues** tab:

| # | Track / Issue | Layer | What You Can Build |
| :--- | :--- | :--- | :--- |
| **1** | **Docker Multi-Node Simulation** | `HCF` / Infra | Add a `Dockerfile` & `docker-compose.yml` to simulate heterogeneous satellite nodes (e.g., throttled CPU/RAM limits) on a single laptop. |
| **2** | **Real-Time CLI Progress & Node Monitor** | `CIE` / UX | Build a terminal dashboard (`rich`/`tqdm`) displaying live residual plateaus, active satellite nodes, and runtime savings. |
| **3** | **Custom Iterative Workload Plugin** | `CIE` / Workloads | Plug in your own iterative solver or loop (OpenFOAM, Fluent logs, Jacobi/PageRank, or PyTorch/ML training curves). |
| **4** | **Custom Resource-Adaptive Splitting Policy** | `HCF` / Scheduler | Implement a task-offloading heuristic based on live node telemetry (network ping, RAM cap, or thermal/battery load). |
| **5** | **Hardware / OS Device Profile & Setup** | `HCF` / Agents | Contribute setup scripts and benchmarks for your own setup (Android/Termux, Raspberry Pi, Windows WSL2, macOS, or Linux). |
| **6** | **Communication / Transport Adapter** | `HCF` / Network | Implement the lightweight satellite agent over JSON-RPC, gRPC, ZeroMQ, WebSockets, or mDNS discovery. |

---

## How to Contribute
1. **Accept your collaborator invite** (or fork this repository).
2. **Create your own folders and files** cleanly (e.g., `cie/`, `hcf/`, `ase/`, `examples/`, `docker/`)—no prior boilerplate required.
3. **Push to a feature branch** (e.g., `feat/cie-plateau-detector` or `feat/hcf-jsonrpc-agent`) and open a **Pull Request**.
4. **Get Credited:** Founding contributors will be featured in the repository's Contributors Hall of Fame and invited to co-author follow-up benchmark studies.

*Head over to the **Issues** tab or comment on the pinned Welcome thread to claim any of the 6 tracks above!*

---

## Citation
@misc{panickker2026resource,
  title={Framework for Resource-Adaptive Acceleration of Iterative Computations on Heterogeneous Low-Cost Devices},
  author={Panickker, Krishnendhu Jayakumar},
  howpublished={Presented at the 27th Annual AeSI CFD Symposium, IIT Madras, Chennai},
  month={August},
  year={2026}
}

```
