# DocuClear AI ⚖️⚡
### Autonomous Enterprise Contract Risk Auditor & Real-Time Redline Engine

> Built for **Hack With Hyderabad 3.0** (Devnovate / Hack With India) — Microsoft Hyderabad Campus Finale Track.

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/Backend-FastAPI-009688.svg)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/Frontend-React%20%2F%20Tailwind-61DAFB.svg)](https://reactjs.org/)
[![Azure](https://img.shields.io/badge/Cloud-Microsoft%20Azure-0078D4.svg)](https://azure.microsoft.com/)

---

## 👥 Team: Mission X
- **Bonthu Praveen** (Lead Developer & Runtime Architecture)
- **Hari Sri Lahari** (Product Strategy & Legal-Tech Design)

---

## 📌 Executive Summary
Enterprise legal and procurement teams spend an average of **4.5 hours manually reviewing single Master Services Agreements (MSAs)**. Over **68% of small-to-midsize businesses** unknowingly sign agreements with one-sided indemnity clauses, uncapped consequential liability, and core IP assignments, causing upwards of **$120,000 in average dispute losses**.

**DocuClear AI** automates contract auditing by combining multimodal layout parsing with deterministic structured LLM reasoning. It extracts clause hierarchies, calculates an objective risk index (0–100), executes real-time text redlining with visual diffs, and outputs print-ready enterprise compliance memoranda.

---

## 🌟 Key Capabilities
- **Deterministic Layout Extraction:** Uses Azure Document Intelligence to preserve multi-page hierarchies, section numbers, and nested tables.
- **Strict Pydantic Reasoning:** Powered by Azure OpenAI (GPT-4o) running at temperature `0.1` with strict JSON schema enforcement to eliminate hallucinations.
- **Dynamic Risk Scorecard:** Computes an aggregate risk index based on toxic clause weighting (Indemnification, Termination at Will, IP Transfer).
- **Interactive Inline Diffing:** Real-time `<ins>` and `<del>` redline visualizer with one-click enterprise liability remediation.
- **Executive Audit Export:** Native `@media print` engine generating clean, single-page legal compliance memoranda for board review.
- **Enterprise NDA Posture:** Designed for Zero Data Retention (ZDR) within private cloud tenant boundaries.
- **High-Reliability Fallback:** Offline cached runtime guaranteeing sub-second responsiveness regardless of venue Wi-Fi conditions.

---

## 🏗️ System Architecture

```text
┌───────────────────────────────────────────────┐
│           React / Tailwind Web Client         │
│  - Real-time Redline Diff Engine              │
│  - Live Contract Ingestion & State Machine    │
│  - Single-Click Formal Audit Memo Exporter    │
└───────────────────────▲───────────────────────┘
                        │ HTTP / JSON Payload
┌───────────────────────▼───────────────────────┐
│            FastAPI Application Core           │
│  - Pydantic v2 Schema Enforcer                │
│  - Deterministic Offline Fallback Service     │
└───────────▲───────────────────────▲───────────┘
            │                       │
┌───────────▼────────────┐   ┌──────▼────────────┐
│   Azure Document Intel │   │ Azure OpenAI      │
│   Hierarchical OCR     │   │ GPT-4o (Temp 0.1) │
└────────────────────────┘   └───────────────────┘
