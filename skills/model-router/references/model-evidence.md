# Model-routing evidence register

Last reviewed: 2026-09-07

This register supports routing decisions; it is not a universal ranking. Scores from different evaluations are not directly interchangeable. Update entries with the retrieval date, evaluation conditions, and a link to the primary source.

## Evidence currently used

| Dimension | Source | What it supports | Limit |
| --- | --- | --- | --- |
| General reasoning, coding, agentic workflows, computer use | [OpenAI GPT-5.4 announcement](https://openai.com/index/introducing-gpt-5-4/) | The vendor reports GPT-5.4 combines reasoning, coding, and agentic workflows, including native computer-use capabilities in Codex/API; it reports MMMU-Pro 81.2% without tools versus GPT-5.2 79.5%. | Vendor-reported; not a neutral cross-model comparison. |
| Human preference and coding | [Arena coding leaderboard](https://arena.ai/leaderboard?category=coding) | Useful live, preference-based comparison for coding responses; retain rank and uncertainty interval at retrieval time. | Preference data is prompt/population dependent and does not measure long-horizon execution directly. |
| Agentic tool/browser/computer workflows | [BenchLM agentic leaderboard](https://benchlm.ai/agentic) | A task-specific signal for tool use and agentic workflows. | Methodology and model coverage can change; snapshot rather than ground truth. |
| Multimodal-agent benchmark catalog | [Awesome multimodal agent benchmarks](https://github.com/PhiloLabs/awesome-multimodal-agent-benchmarks) | Discovery index for multimodal-agent evaluations and their task definitions. | A catalog is not itself a score or validation result. |

## How to aggregate

1. Separate dimensions into reasoning, coding, agentic execution, multimodal understanding, latency, cost, and reliability.
2. Normalize only within the same benchmark family and evaluation conditions. Keep raw values and ranks alongside any normalized score.
3. Weight the dimension that matches the inferred task. Do not let a general leaderboard override a directly relevant task evaluation.
4. Require at least two independent sources before turning a claim into a routing rule. Label one-source or anecdotal claims as provisional.
5. Recheck volatile rankings before high-stakes routing. Retire stale entries rather than silently carrying them forward.

## Interpretation policy

Claims such as “Astra improves agentic and multimodal work more than Sol, while reasoning gains are small” may be a useful hypothesis, but are not established until exact model variants, effort settings, prompts, tools, and sample sizes are recorded. Public boards often expose model families rather than internal Codex aliases, so the router should use such claims as a prior and local task outcomes as the deciding evidence.
