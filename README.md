# 404Hunter.ai - Autonomous Subdomain Takeover Scanner (Development Mode)

## 📌 About the Project

**404Hunter.ai** is a fully autonomous subdomain takeover detection tool designed for real-world web application bug hunting. Its goal is to take a domain (or list of domains) as input and perform complete reconnaissance and analysis to identify possible subdomain takeovers — without any human interaction. The scanner aims for 99% detection accuracy and integrates AI and pattern recognition for intelligent decision-making.

> ⚠️ This README is currently in **development mode** to help guide the build process. A user-friendly version will be added once the tool is production-ready.

---

## 🚀 Project Goal

Build a zero-interaction, AI-powered tool that:

* Takes input as a domain or list of domains
* Performs full subdomain enumeration
* Resolves DNS and checks HTTP responses
* Matches known takeover fingerprints
* Uses fine-tuned free LLMs for intelligent classification
* Outputs accurate, repeatable, and bug bounty-ready results

---

## 🧩 Architecture Plan

### 🧱 Phase 1: Core Pipeline (Weeks 1–2)

* [ ] `subdomain_enum.py` — Subdomain enumeration (Subfinder + crt.sh)
* [ ] `resolver.py` — DNS resolution checker
* [ ] `http_check.py` — Fetch and parse HTTP responses
* [ ] `fingerprint.py` — Static fingerprint matching module
* [ ] `report.py` — JSON/Markdown report generator

### 🧠 Phase 2: AI & Pattern Matching (Weeks 3–4)

* [ ] `signatures.json` — Known cloud service error page signatures
* [ ] `ai_classifier.py` — Use local LLM to classify suspicious HTML
* [ ] Result ranking by confidence (AI + signature score)

### 🔁 Phase 3: Full Automation (Weeks 5+)

* [ ] Batch input + automated scanning loop
* [ ] Config file for thresholds (timeouts, retries, confidence cutoff)
* [ ] Auto-refresh/recheck mode
* [ ] Polished final report with evidence

---

## 🛠️ Technologies & Libraries

### ✅ Languages

* Python 3.10+

### ✅ Required Python Libraries

* `httpx` — Fast, modern HTTP requests
* `dnspython` — DNS resolution
* `beautifulsoup4` — HTML parsing
* `rich` — CLI formatting (for progress/output)
* `subprocess` — Run external tools like Subfinder
* `json`, `os`, `time`, `argparse` — Core Python modules

### ✅ External Tools

* [Subfinder](https://github.com/projectdiscovery/subfinder) — Fast passive subdomain enumeration
* `crt.sh` — Certificate Transparency Log API

### ✅ AI Stack (Phase 2)

* Fine-tuned LLM (e.g., LLaMA, TinyLLaMA, Phi-2, or GPT-J)
* `transformers` / `llama-cpp-python` — Local model inference
* Custom dataset of takeover error pages

---

## 📚 What You’ll Learn During This Project

* ✅ DNS resolution and domain mechanics
* ✅ Subdomain takeover exploitation techniques
* ✅ Python scripting for automation & web interaction
* ✅ AI/ML fine-tuning with domain-specific data
* ✅ Prompt engineering for classification use-cases
* ✅ Designing fully autonomous cybersecurity tools

---

## 🗂 Directory Structure (Planned)

```
ai_takeover_scanner/
├── main.py
├── core/
│   ├── subdomain_enum.py
│   ├── resolver.py
│   ├── http_check.py
│   ├── fingerprint.py
│   └── ai_classifier.py
├── data/
│   └── signatures.json
├── report/
│   └── report.json
├── requirements.txt
└── README.md
```

---

## ✅ Status: In Progress (Build Phase 1)

* [ ] Subdomain enumeration implemented
* [ ] DNS + HTTP check in progress
* [ ] AI logic planned

Stay tuned for weekly progress updates. Once we reach a working MVP, a new README will be created for external users.

---