# Counterfactual Preference Learning (CPL)

**Companion resources for:** *Counterfactual Preference Learning for Hyper-Heuristics: Evolving Symbolic Search-Control Skills*


## Contents

| File | Description |
|---|---|
| `prompts/skill_induction_prompt.md` | LLM instructions for inducing state-dependent symbolic search-control skills from Counterfactual Preference Knowledge (CPK). |
| `prompts/rule_schema.json` | JSON Schema defining the structure and constraints of candidate symbolic skills. |
| `prompts/cpk_entries.json` | Illustrative CPK entries containing search-state features, operator rankings, counterfactual outcomes, and supporting statistics. |
| `prompts/initial_skill.json` | Initial symbolic skill with the fixed default ordering of five search operators. |

## Usage

The induction prompt accepts three inputs:

- `CURRENT_SKILL`: The current accepted symbolic skill, initialized using `initial_skill.json`.
- `CPK_ENTRIES`: Counterfactual preference evidence collected during the learning process.
- `RULE_SCHEMA`: The required output structure defined in `rule_schema.json`.

The LLM produces a candidate symbolic skill consisting of at most 12 state-dependent rules and one default rule. Candidate skills undergo deterministic structural verification and independent optimization-based validation before acceptance.
