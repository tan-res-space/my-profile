# Topic pillars

Chosen to continue P0 and to match work that is already public on the site and LinkedIn: SLM-on-one-GPU, medical coding copilots, medical ASR, on-prem data, speech endpoint detection (PhD), coaching.

## slm-agents (series spine)

NVIDIA Belcak et al. 2025/26: SLMs (<~10B, consumer-device feasible) should handle repetitive agent subtasks; heterogeneous systems invoke LLMs only for open-ended work. Conversion algorithm: log → curate/PHI-strip → cluster tasks → pick SLM → LoRA/QLoRA or distill → iterate.

Tanmoy angle: we already ran the specialist on one GPU; the point was inspectability, not fashion.

## healthcare-speech

DeliverHealth: Med-ASR, automatic notes, coding copilot, RAG correction. Public CV claim: fine-tuned STT at 12% medical WER. NVIDIA 2026 ambient healthcare / on-prem Parakeet–Nemotron ASR is the industry tailwind — comment on the *requirement* (audio never leaves), not on unreleased product.

PhD unique: wavelet/convolution endpoint detection (CNSNS 2019) and SEGRT features for SER. Use once as craft, not as nostalgia.

## evaluation

AUROC on "is this answer right?", calibration curves, deferral thresholds, WER, why verbal confidence from an API is not a score. Guardrails (topic control) vs meters (token probs). Publish one miss (P10) so the series does not read as vendor cosplay.

## craft

Hiring, coaching, how an applied DS in healthcare should think. One post only in this cycle so the feed stays expert, not HR.
