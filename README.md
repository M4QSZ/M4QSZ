<div align="center">

![Miguel Quevedo — Systems, Rust FFI & Multiplatform](./assets/profile-banner.svg)

<br />

[![Portfolio EN](https://img.shields.io/badge/Portfolio_EN-m4qsz.github.io%2Fen-e4a56c?style=for-the-badge&logo=astro&logoColor=white)](https://m4qsz.github.io/en/)
[![Portafolio ES](https://img.shields.io/badge/Portafolio_ES-m4qsz.github.io-c87b4b?style=for-the-badge&logo=astro&logoColor=white)](https://m4qsz.github.io/)
[![Resume / CV](https://img.shields.io/badge/Resume_%2F_CV-PDF_%26_ATS-83c6a0?style=for-the-badge&logo=readthedocs&logoColor=101314)](https://m4qsz.github.io/en/cv/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-miguel--quevedo--dev-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/miguel-quevedo-dev/)
[![Email](https://img.shields.io/badge/Email-miguel.270799%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:miguel.270799@gmail.com)

</div>

---

### "I design the product. I build the systems underneath."

I build **end-to-end multiplatform software, native Rust systems, and formally verified tooling** across desktop, mobile, web, game engines, and certified SAT proof logging — taking concepts from 0-to-1 UI fidelity (`on-model`) down to panic-safe Rust FFI boundaries, encrypted peer-to-peer sync, PostgreSQL/RLS schemas, and Lean 4 soundness proofs.

* **Target Roles:** `Rust Systems & AI Agent Infrastructure Engineer (MCP / GPUI)` · `Flutter / Rust FFI Multiplatform Engineer` · `Formal Verification / Systems Engineer` · `Full-Stack TypeScript Engineer`
* **Core Stack:** `Rust` (`GPUI CE 0.3.0` / `MCP stdio` / `Iroh QUIC` / `C-ABI FFI` / `tract-onnx`) · `Lean 4` / `VeriPB 3.0` · `Flutter` (`Skia` / `Impeller`) · `Dart` · `Kotlin` (`Android`) · `TypeScript` (`Next.js` / `Astro`) · `C#` (`Unity 6.3 LTS`) · `Luau` (`Roblox`) · `PostgreSQL` / `Supabase` / `Isar`
* **Availability & Location:** Aragua, Venezuela · **Remote · Hybrid · On-site · Open to relocate** · Direct: [`miguel.270799@gmail.com`](mailto:miguel.270799@gmail.com)
* **Education & Languages:** Systems Engineering (`UBA '27`, Programming Concentration) · Spanish & English (`Native / Bilingual`) · Portuguese & Italian (`Advanced`) · German & Japanese (`Basic`)

---

### Inspectable Open-Source Systems & Formal Research

Because my flagship commercial ecosystem (**Meson**) and multi-CLI desktop orchestrator (**Cockpit**) remain in private repositories, these standalone public repositories expose my Rust FFI, AEAD/CRDT sync, offline-first Dart, and Lean 4 + VeriPB 3.0 formal verification work in public:

| Repository | What It Implements & Proves | Verification |
| :--- | :--- | :---: |
| **[`certified-arith-preproc`](https://github.com/M4QSZ/certified-arith-preproc)** | Blind **VeriPB 3.0.2** pseudo-Boolean certification for scrambled CNF (arithmetic adders, disjunctive `PHP ∨ Tseitin` interpolants, degree-2 Veronese `RM(2, n)` & `F₂` homology for Goldreich PRGs) with **61 Lean 4.36.0 theorems (`0 sorryAx`)** and reproducible benchmarks vs. Kissat 4.0.4, CaDiCaL 1.9.5 & CryptoMiniSat 5. | **61 Lean 4 · 31/31 VeriPB** |
| **[`lan-delta-sync`](https://github.com/M4QSZ/lan-delta-sync)** | Offline-first LAN sync primitives in **Rust**: `HybridClock` (HLC with drift guards), `DeltaStore` (LWW CRDT + tombstones), `PeerSession` (`ChaCha20-Poly1305` AAD + 64-slot anti-replay window), bounded `RetryOutbox`, and **7 integration tests + mesh example**. | [![CI](https://github.com/M4QSZ/lan-delta-sync/actions/workflows/ci.yml/badge.svg)](https://github.com/M4QSZ/lan-delta-sync/actions/workflows/ci.yml) |
| **[`ffi-arena-bridge`](https://github.com/M4QSZ/ffi-arena-bridge)** | Zero-dep Rust **C-ABI & `dart:ffi` bridge**: `u64` generational handles (zero raw-pointer UAF), `catch_unwind` panic shield, zero-copy `FfiBytesView`, double-free-safe `FfiOwnedBuffer`, deterministic trigram search, and **live C99 `cdylib` smoke binary in CI**. | [![CI](https://github.com/M4QSZ/ffi-arena-bridge/actions/workflows/ci.yml/badge.svg)](https://github.com/M4QSZ/ffi-arena-bridge/actions/workflows/ci.yml) |
| **[`dart-offline-outbox`](https://github.com/M4QSZ/dart-offline-outbox)** | Transactional offline-first mutation outbox in **pure Dart**: per-entity write coalescing, jittered exponential `RetryPolicy`, partial batch ACKs (`DispatchOutcome`), dead-letter quarantine, `OutboxJournalStore`, and **strict `dart analyze --fatal-infos` + unit tests**. | [![CI](https://github.com/M4QSZ/dart-offline-outbox/actions/workflows/ci.yml/badge.svg)](https://github.com/M4QSZ/dart-offline-outbox/actions/workflows/ci.yml) |

---

### Live Web Deployments (Vercel)

| Deployment | Stack | Scope |
| :--- | :--- | :--- |
| **[Meson OS Platform](https://mesonapp.vercel.app)** | `Astro` · `Tailwind CSS` · `TypeScript` | 189-page, 19-language mobile-first commercial platform and modular ERP showcase. |
| **[SET — Ingeniería Eléctrica & Climatización](https://set-ingenieria.vercel.app)** | `Astro` · `Tailwind CSS` · `JavaScript` | Production service website backed by centralized business/project configuration. |
| **[MedPulse SOS — Emergency QR/NFC Platform](https://pulsera-medica.vercel.app)** | `Astro` · `TypeScript` · `Supabase` | Interactive prototype for QR/NFC emergency cards, wristband catalog, and order tracking. |

---

### Selected Architecture & Product Highlights

* **Meson *(private multiplatform ecosystem — `769/860` active-branch commits · `404/404` live Rust `cargo test` passing)*:** Lead architect & principal engineer across **7 specialized Flutter/Astro apps**, **10 decoupled Dart/Isar packages**, and **8 Rust workspace crates**:
  * **`meson_business` *(2,521 Dart files / 521 test files · 50,270 Rust LOC)*:** Multi-vertical POS/Retail, self-checkout with RS-232/USB weigh-scales, CRDT KDS, Flame 2.5D floor planner (+ Rust isometric 3D projection & magnetic snapping), double-entry accounting, SENIAT fiscal hash chain, 502-file Firestore → Supabase/PostgreSQL + 59 RLS cutover, B2B marketplace, `device_hub` (mDNS/BLE, offline Isar IoT, failover print queues, CFDs, WebRTC), and **Atelier** HR/payroll + PIN kiosk.
  * **49 Rust APIs & 8 Crates (`flutter_rust_bridge`):** Self-calibrating zero-LLM edge NLU (`meson_ai`, **300/300 tests**: online Platt scaling, 128d PC1-removed SIF, adaptive-RAM `tract-onnx`, Spanish phonetics, `catch_unwind` circuit breakers, Flutter `AutomationEngine` & documented pivot from in-process Candle `Qwen2.5` GGUF + Whisper for legacy POS hardware), deterministic retail/BOM/KDS engines (`meson_features`, **78/78 tests**: cycle-safe nested BOMs, FEFO, GS1 weight/price barcodes, BOGO/MultiBuy), sparse-chunked Office suite (`meson_tools`, **21/21 tests**: 1M-row `ChunkedColumn` + DAG + `.xlsx/.docx/.pptx` roundtrips), `qbsdiff` delta updater (`meson_shell`, **5/5 tests**), out-of-process Whisper STT worker, and `meson_gpui` (15 files).
  * **Satellite Apps & Telemetry Lab:** `meson_central`, `meson_delivery` (DTN mesh relay), `meson_customer`, `meson_pause` (15 tests), `meson_currency`, public **[`BUCO`](https://github.com/M4QSZ/BUCO)** (22 tests), and **Axion Mouse Lab** (`Tools/mouse_angle_calibrator`, 7,075 LOC Rust: exact `SO(2)`, 64-pt arc resampling, IRLS Huber, Jensen-immune polling radar, 39/41 tests). *(Collaborator `ljga_` contributed UI widgets & Flutter screens, ~10.6% of commits.)*
* **Cockpit v2.2 *(private Rust + GPUI CE 0.3.0 + concurrent MCP stdio orchestrator — `78k+` LOC Rust · `57` runtime modules · `228` passing unit tests — [Technical Report](https://m4qsz.github.io/en/lab/cockpit-paper/) · [PDF](https://m4qsz.github.io/papers/cockpit-orchestrator-paper.pdf) · [Case Study](https://m4qsz.github.io/en/projects/cockpit/))*:** Native desktop orchestrator unifying Claude Code, Codex CLI, Antigravity, and OpenCode with live 5h/7d quota telemetry, hot Auto-Failover, automatic RTK interception (`PreToolUse` + `PATH` shims, **−85.0%** live on `cargo test`), `94.13%` AST skeleton reduction, `88.34%–97.31%` KV-cache-safe compaction, `15s` `sync_all()` power-loss persistence + `/recover`, Iroh QUIC / Tailscale / 4G relay / Android Kotlin client, and `$0` pipelines (Win32 UIA, 7-provider S→D Cloud 3D + Blender `bpy`, Unity 10-rule, Roblox 14-rule, FFmpeg, Math/Music Lab).
* **Brasas & El Pueblo del Faro:** Cross-runtime action adventure (**Flutter Canvas** `21.1k` LOC + **Unity 6.3 LTS** engine-free C# core with **40 XML test logs, 0 failures up to 142 EditMode + 8 PlayMode**, `1,353`-vertex 13-control 2D mesh rig, and 30 fps MP4 temporal diff QA + **Roblox Luau** prototype) ([Paper 16](https://m4qsz.github.io/en/lab/meson-brasas-game-architecture/)).
* **Technical Reports & Lab — 18 Bilingual Papers with PDFs *([m4qsz.github.io/laboratorio](https://m4qsz.github.io/laboratorio/) · [EN Lab](https://m4qsz.github.io/en/lab/))*:**
  * **Cockpit Technical Reports (6):** [Cockpit v2.2 Architecture](https://m4qsz.github.io/en/lab/cockpit-paper/) · [Zero-Vision MCP Automation](https://m4qsz.github.io/en/lab/cockpit-zero-vision/) · [Local-First Multi-Device P2P](https://m4qsz.github.io/en/lab/cockpit-distributed/) · [Algebraic Context Compression](https://m4qsz.github.io/en/lab/cockpit-algebraic-compression/) · [Crash Resilience & Behavioral Fingerprinting](https://m4qsz.github.io/en/lab/cockpit-resilience-fingerprinting/) · [Automatic RTK, Delta Telemetry & `$0` Pipelines](https://m4qsz.github.io/en/lab/cockpit-rtk-telemetry-pipelines/)
  * **Meson, Game & Input Systems Reports (9):** [Multi-Currency Finance & Fiscal Hash](https://m4qsz.github.io/en/lab/meson-finance-erp/) · [Modular ERP, Rust Retail & Device Hub (v1.1)](https://m4qsz.github.io/en/lab/meson-management-erp/) · [Causal LAN Sync & Courier Mesh](https://m4qsz.github.io/en/lab/meson-offline-mesh/) · [FFI Arenas, Sparse Office & 3D Engines (v1.1)](https://m4qsz.github.io/en/lab/meson-rust-edge/) · [NoSQL → SQL PostgreSQL/RLS Migration](https://m4qsz.github.io/en/lab/meson-nosql-to-sql/) · [Green-Linter Illusion: 112-Table BaaS/RLS & Realtime WAL Audit](https://m4qsz.github.io/en/lab/meson-baas-rls-telemetry-audit/) · [Self-Calibrating Edge NLU & Flutter UI Automation](https://m4qsz.github.io/en/lab/meson-edge-nlu-automation/) · [Brasas Multi-Runtime Game Architecture & 2D Rig](https://m4qsz.github.io/en/lab/meson-brasas-game-architecture/) · [Biomechanical Raw Input Calibration, Huber IRLS & Jensen Immunity](https://m4qsz.github.io/en/lab/axion-biomechanical-input-telemetry/)
  * **Certified SAT & Formal Verification Notes (3 — Lean 4 + VeriPB 3.0.2):** [Certified Arithmetic Preprocessing](https://m4qsz.github.io/en/lab/certified-arith-preproc/) · [Blind Disjunctive Interpolants (`PHP ∨ Tseitin`)](https://m4qsz.github.io/en/lab/certified-disjunctive-interpolants/) · [Degree-2 Veronese `RM(2, n)` & `F₂` Homology for Goldreich PRGs](https://m4qsz.github.io/en/lab/certified-veronese-homological-prg/)
  * **Inspectable Demos:** Public modules across **Rust**, **Dart**, **C11 + NASM x64 Assembly**, **C++17**, **PHP 8.2**, and **Swift**.

<details>
<summary><b>Versión en Español (ES) — Resumen rápido y contacto</b></summary>

Desarrollo software multiplataforma, infraestructura de sistemas y verificación formal de extremo a extremo (PC, móvil y web): orquestación de agentes IA y servidores **MCP concurrentes en Rust (`GPUI CE 0.3.0`, `Iroh QUIC`, `Tailscale`, `Kotlin`)**, certificación SAT en **Lean 4.36.0 + VeriPB 3.0.2 (61 teoremas, `0 sorryAx`)**, interfaces **Flutter/Next.js/Astro**, lógica nativa segura en **Rust (`C-ABI` / `dart:ffi`, `404/404` tests en vivo)**, redes locales **P2P offline-first (`ChaCha20-Poly1305` + CRDT)**, bases locales (`Isar` / `SQLite`) + **PostgreSQL/Supabase (RLS)** y videojuegos multi-runtime (**Unity 6.3 LTS C#**, **Flutter Canvas**, **Roblox Luau**).

* **Roles objetivo:** Ingeniero de Sistemas Rust e Infraestructura IA (MCP / GPUI) · Ingeniero Flutter / Rust FFI · Verificación Formal y Sistemas · Full-Stack TypeScript
* **Portafolio interactivo:** [m4qsz.github.io](https://m4qsz.github.io/)
* **CV imprimible / ATS:** [m4qsz.github.io/cv](https://m4qsz.github.io/cv/)
* **Laboratorio Técnico (18 papers bilingües con PDF + 4 repos públicos):** [m4qsz.github.io/laboratorio](https://m4qsz.github.io/laboratorio/) · [Paper 1: Cockpit v2.2](https://m4qsz.github.io/laboratorio/cockpit-paper/) · [Paper 14: Veronese & Homología F₂](https://m4qsz.github.io/laboratorio/certified-veronese-homological-prg/) · [Paper 15: Edge NLU](https://m4qsz.github.io/laboratorio/meson-edge-nlu-automation/) · [Paper 16: Brasas](https://m4qsz.github.io/laboratorio/meson-brasas-game-architecture/) · [Paper 17: Raw Input & Huber](https://m4qsz.github.io/laboratorio/axion-biomechanical-input-telemetry/) · [Paper 18: Auditoría BaaS/RLS & WAL](https://m4qsz.github.io/laboratorio/meson-baas-rls-telemetry-audit/)
* **LinkedIn:** [linkedin.com/in/miguel-quevedo-dev](https://www.linkedin.com/in/miguel-quevedo-dev/)
* **Contacto directo:** `miguel.270799@gmail.com`

</details>
