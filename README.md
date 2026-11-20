<p align="center">
  <img src="assets/banner.svg" alt="Ryoya Kubo — AI red teaming and prompt-injection research" width="100%">
</p>

<p align="center">
  <a href="https://hoqo.ai"><img src="https://img.shields.io/badge/Hoqo-hoqo.ai-1C1B1A?style=flat-square" alt="Hoqo"></a>
  <a href="https://www.linkedin.com/in/ryoyakubo"><img src="https://img.shields.io/badge/LinkedIn-ryoyakubo-1C1B1A?style=flat-square" alt="LinkedIn"></a>
  <a href="mailto:hello@hoqo.ai"><img src="https://img.shields.io/badge/Email-hello%40hoqo.ai-1C1B1A?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://github.com/ryoyakubo-ai/jp-inject"><img src="https://img.shields.io/badge/OSS-jp--inject-E84C4C?style=flat-square&logo=github&logoColor=white" alt="jp-inject"></a>
</p>

I attack AI agents and chatbots the way a real adversary would: prompt injection, data exfiltration, and getting agents to misuse the tools they are connected to. I measure what works, and I write it up so it can be reproduced.

| | |
| --- | --- |
| **Now** | Founder of [Hoqo](https://hoqo.ai), a red teaming service for AI agents |
| **Research** | [jp-inject](https://github.com/ryoyakubo-ai/jp-inject): prompt injection written the Japanese way, measured |
| **Before** | AI Red Teaming & Evaluation Contractor, AI Safety Evaluator (freelance, 2025–2026) |
| **Languages** | Japanese · Korean · English |

---

## Research: jp-inject

**Does writing a prompt injection the Japanese way change whether it works?**

[jp-inject](https://github.com/ryoyakubo-ai/jp-inject) rewrites 20 standard injection attacks with techniques specific to Japanese: keigo (business honorifics), kana/romaji spellings, half-width katakana, old kanji forms, and look-alike characters. It measures the change in attack success with paired English controls and confidence intervals.

<p align="center">
  <img src="assets/finding.svg" alt="Full-width English: ProtectAI DeBERTa v2 flagged 70% of plain English attacks and 0% of full-width ones; Llama Prompt Guard 2 flagged 25% and 0%" width="100%">
</p>

| 545 | 2 × 2,725 | 2 | 0 / 20 |
| :---: | :---: | :---: | :---: |
| fixed test cases | generations on two open models | open detectors tested | full-width attacks flagged |

- **Finding:** on these models, no Japanese-specific rewrite made injection more effective on both, and most made it less effective. But English written in full-width letters got past both detectors in every case, and the models still followed it.
- Methodology written before the runs, a rule-based judge checked against hand labels, benign payloads only.
- **Next:** proposing a full-width rewrite buff (a module that transforms test prompts) and a Japanese version of the translation-based injection tests to [garak](https://github.com/NVIDIA/garak).

→ [Report](https://github.com/ryoyakubo-ai/jp-inject/blob/main/docs/report.md) · [日本語の要約](https://github.com/ryoyakubo-ai/jp-inject/blob/main/docs/report.ja.md)

## Work: Hoqo

[Hoqo](https://hoqo.ai) tests AI agents and support bots that are live in production and connected to business tools. I look for prompt injection that leads to data leaks or unauthorized actions, and I map findings to the OWASP Top 10 for LLM Applications and MITRE ATLAS.

- Research article: [Your pentest passed. Your AI agent might not.](https://hoqo.ai/blog)

## Background

- **AI Red Teaming & Evaluation Contractor** (freelance, 2025–2026): adversarial testing of AI models and evaluation of their responses to harmful requests
- **AI Safety Evaluator** (freelance, 2025)
- National Institute of Technology, Kurume College (Electrical & Electronic Engineering, 2025) · 42 Tokyo

## Tools

![Python](https://img.shields.io/badge/Python-1C1B1A?style=flat-square&logo=python&logoColor=white)
![garak](https://img.shields.io/badge/garak-1C1B1A?style=flat-square)
![PyRIT](https://img.shields.io/badge/PyRIT-1C1B1A?style=flat-square)
![Spikee](https://img.shields.io/badge/Spikee-1C1B1A?style=flat-square)
![Hugging Face](https://img.shields.io/badge/Hugging_Face_Transformers-1C1B1A?style=flat-square&logo=huggingface&logoColor=white)
![LM Studio](https://img.shields.io/badge/LM_Studio-1C1B1A?style=flat-square)
![Cloudflare Workers](https://img.shields.io/badge/Cloudflare_Workers-1C1B1A?style=flat-square&logo=cloudflareworkers&logoColor=white)
![Astro](https://img.shields.io/badge/Astro-1C1B1A?style=flat-square&logo=astro&logoColor=white)

---

<details>
<summary><b>日本語</b></summary>

<br>

AIエージェントやLLMアプリへのレッドチーミング（実際に攻撃して弱点を見つけるセキュリティテスト）と、プロンプトインジェクションの研究をしています。
AIエージェント向けのレッドチーミングサービス [Hoqo](https://hoqo.ai) を運営し、日本語特有のプロンプトインジェクションを測る OSS [jp-inject](https://github.com/ryoyakubo-ai/jp-inject) を公開しています。

</details>
