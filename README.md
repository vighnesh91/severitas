# 🛡️ Severitas Framework

[![Python Version](https://shields.io)](https://python.org)
[![License](https://shields.io)](LICENSE)
[![Safety Profile](https://shields.io)](#-structural-safety-by-design)

> **Severitas** is an authorized social-engineering awareness and simulation framework. It is structurally constrained to run exclusively inside isolated laboratory environments against synthetic identities.

---

## 💎 Features

Severitas isolates assessment execution logically so that security evaluation doesn't compromise corporate infrastructure or real data.

* 🎛️ **Kali-Style Interactive UI:** Dynamic console launcher to browse, validate, and execute training exercises quickly.
* 🧪 **Zero-Network Laboratory:** Embedded synthetic Mail, Web, and DNS servers that run entirely on your loopback adapter.
* 🛑 **Structural Discarder:** Inbound form data is validated, measured for interaction telemetry, and instantly deleted from memory. No credential values are ever retained or written to disk.
* 📊 **Offline Analytics & Reporting:** Automated assembly of chronological threat funnel maps, timeline summaries, and control effectiveness insights into clean **HTML**, **Markdown**, **JSON**, and **CSV** formats.

---

## 🏗️ Repository Architecture

The codebase separates authorization policy layers from business execution loops:

```text
severitas/
├── src/
│   └── severitas/
│       ├── core/           # Container bootstrapping, configuration, and logging
│       ├── scope/          # Target match gates (Domain, Email, Network ranges)
│       ├── authorization/  # Pre-execution pipeline validation
│       ├── infrastructure/ # Mock DNS, Mail, Web, and Tracking handlers
│       ├── scenarios/      # Phishing, OSINT, QR, Pretexting scenario plugins
│       ├── telemetry/      # Synchronous ordered event bus and analytics engine
│       └── security/       # Structural redaction filters and leak sentinels
```

---

## 🔒 Structural Safety by Design

Unlike advisory tools, Severitas guarantees compliance metrics structurally:
1. **Target allow-listing (`severitas.scope`):** Campaigns fail closed unless targets map perfectly to designated synthetic test definitions (`*.local`, `*.test`, `*.invalid`).
2. **Zero credential retention (`severitas.security.guards`):** The submission path counts field names but drops variables entirely before records transition or telemetry is captured.
3. **Redaction Filter:** A global regex logging block captures accidental leaks (JWTs, API tokens, Private keys) and strips them out dynamically.

---

## ⚡ Quick Start

### Prerequisites
* Python **3.11** or higher
* **PyYAML** (shipped and pinned within default requirements)

### Installation
Clone this repository layout and compile your development link in an isolated container instance or local virtualenv:

```bash
# Initialize development profile 
python3 -m venv .venv
source .venv/bin/activate

# Install in editable mode
pip install -e .
```

### Direct CLI Controls

Severitas includes quick terminal utilities to provision lab templates immediately:

```bash
# Launch the interactive menu wizard
severitas --menu

# Start the internal mock services bundle
severitas lab start

# Scope out target definitions for synthetic verification checks
severitas scope create --name alpha --domain training.local --email user@training.local

# Run an end-to-end sandbox execution demo to generate mock results
severitas lab demo --targets 25
```

---

## 📊 Interaction Funnel Mockup

When compiling analytics output folders, the offline reporting system measures user awareness cohorts using inline charts similar to this format:

```text
Targets simulated        ████████████████████████████████████████ 25
Messages simulated       ████████████████████████████████████████ 25
Interactions             ██████████████████████████              18
Clicks / visits          ████████████████████                    15
Synthetic submissions    ██████████████                          9
User reports             ████████                                5
```

---

## 📜 Legal & Disclaimer

This framework is built strictly for **authorized educational simulations, infrastructure tracking benchmarks, and training validation exercises**. Testing against public hosts or real user populations without explicit Rules of Engagement (ROE) and documented approval is highly prohibited. The code is shipped under the terms of the MIT License.
