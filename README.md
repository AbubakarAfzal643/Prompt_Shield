# PromptShield

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1200&color=36BCF7&center=true&vCenter=true&width=650&lines=Detect+prompt+injection.;Flag+risky+requests.;Protect+LLM-powered+apps." alt="Animated text: Detect prompt injection. Flag risky requests. Protect LLM-powered apps.">
</p>

PromptShield is a proposed lightweight security gateway for applications that use large language models (LLMs). It aims to detect prompt-injection attempts in user prompts and supported external text before they reach a model, then apply configurable security policies.

## Planned features

- Rule-based checks for common prompt-injection patterns.
- A TF-IDF and logistic-regression classifier to assess input risk.
- Configurable actions to allow, flag, or block requests.
- Checks of generated responses for a demo canary phrase and selected leakage indicators.
- Decision logs that record the action taken and its reason.
- A small Python/FastAPI chatbot demo with an option to compare gateway-enabled and gateway-disabled runs.

## Planned evaluation

The prototype will be tested with benign prompts and direct, indirect, and lightly obfuscated attack examples. Evaluation will measure precision, recall, F1-score, false-positive rate, attack success rate, and additional processing latency.

## Scope and limitations

PromptShield is an academic risk-reduction prototype, not a guarantee against prompt injection or information leakage. Its rules and classifier may miss unfamiliar or obfuscated attacks, and may incorrectly flag benign text. The proposal covers supported PDF text extraction and supplied web text; it does not include training or modifying an underlying LLM.

## Project proposal

See the [PromptShield project proposal](docs/PromptShield_Proposal_G-10.pdf) for the full scope, methodology, and requirements.
