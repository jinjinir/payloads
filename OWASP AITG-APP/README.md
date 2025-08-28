# OWASP AITG

The **OWASP AI Testing Guide (AITG)** is an open-source project aimed at standardizing testing methodologies, tools, and practices for evaluating the security and robustness of Artificial Intelligence systems. This repository provides practical resources, templates, and documentation to help red teamers, security researchers, and developers test and assess LLMs and AI-powered applications.

* https://github.com/OWASP/www-project-ai-testing-guide/

## 🎯 What Are the Payloads?

Each AITG-APP-XX.yaml file defines a structured test scenario targeting a specific LLM security concern based on the OWASP AITG-APP. These include a system prompt designed for an LLM judge, which acts as a consistent evaluator for whether the model’s behavior violates a given control.

These YAML files can be integrated into red teaming pipelines, model eval frameworks, or used manually by analysts for step-by-step testing.

## 📊 Results

To demonstrate the LLM attack surface, the payloads in this repository were run against four major models: GPT-5, Gemini 2.5 Flash, Claude Sonnet 4, and Llama 4 Maverick. The results show the percentage of successful attacks (fail rate) for each test scenario. For detailed results and methodology, see the [RESULTS folder](./RESULTS/). Raw results are provided in both `jsonl` and `csv`.

## 📚 Getting Started

1. Clone the repo:
   ```bash
   git clone https://github.com/your-org/owasp-aitg.git
   cd owasp-aitg
   ```

2. Explore the YAML files (`AITG-APP-*.yaml`) for specific test cases and guidelines.

## 📢 Contributing

Community contributions are welcome! Open issues, submit pull requests, or suggest improvements.

- Edit the relevant file in the OWASP AITG-APP directory.
- Clearly document your changes.
- Update topics, judge, or prompts if your changes affect them.
- If possible, run your test case(s) against your target models first.
- Follow the existing formatting style.
- For questions or suggestions, open an issue or start a discussion!

## 🗂️ Taxonomy

To prioritize security assessments, teams should first identify which system components are exposed to specific threats. Early testing focuses on validating configurations and scanning for vulnerabilities, while later stages involve simulating adversarial attacks on targeted components. To guide these efforts, AI-specific threat taxonomies, like OWASP’s LLM Top 10, are used. As GenAI threat testing evolves, taxonomies are becoming more specialized, especially for threats like prompt injection like [Pangea's](https://pangea.cloud/taxonomy/). More granular classifications help define where and how these attacks occur, enabling more precise testing.
