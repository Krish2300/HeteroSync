# Contributing to HeteroSync & Credit Policy

Welcome to **HeteroSync**! Our mission is to build an open, solver-agnostic framework that accelerates iterative computations on everyday devices without requiring an HPC cluster. 

Because this project spans distributed systems, numerical solvers, machine learning, and operations research/game theory, **we actively encourage multiple collaborators to experiment, propose competing routing/scheduling algorithms, and build modular implementations side-by-side.**


## 1. Open Multi-Contributor & Experimentation Policy
* **Parallel Implementations Welcome:** Multiple contributors are encouraged to try out their own architectural variations, routing heuristics, or transport adapters (e.g., plugging in different orchestrators like HiveMind or custom JSON-RPC/gRPC schedulers).
* **Modular Folder Structure:** Keep your experimental or specialized implementation cleanly separated in its own folder or plugin module (e.g., `hcf/adapters/hivemind/`, `hcf/routing/game_theoretic/`, `cie/parsers/`).
* **Branch & Pull Request Workflow:** Push your work to a dedicated feature branch (e.g., `poc/hivemind-hcf` or `feat/routing-algo`) and open a **Pull Request** against `main`.


## 2. Public Attribution & Impact Tracking
Every contribution—whether **code, system architecture, routing algorithm design, or hardware benchmarking**—will be publicly documented and permanently credited:

1. **Public Impact Log (`CONTRIBUTORS.md` & `README.md`):** Every merged contribution is logged publicly in the repository alongside a clear summary of **what was built** and **its measured impact** (e.g., latency reduction, runtime savings, or supported hardware).
2. **Final Release Acknowledgment:** When HeteroSync reaches a functional, complete release, the primary documentation and release notes will formally acknowledge every contributor and their specific module.
3. **Academic Co-Authorship Guarantee:** Whenever any academic paper, symposium extension, or technical report is written using code, algorithms, designs, or benchmarks from this repository, **all contributors whose work is utilized will be invited and added as co-authors.**


## 3. Licensing
HeteroSync uses a permissive open-source license (**MIT / Apache 2.0**) so external projects and student builders can integrate, fork, and build upon it freely without legal friction.
