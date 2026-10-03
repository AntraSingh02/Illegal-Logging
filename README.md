# Illegal-Logging
# WoodWitness

**Paperwork can lie. Chemistry can't.**

WoodWitness is a web-based prototype that checks whether a timber shipment's claimed harvest location matches the chemical fingerprint of the wood itself.

Built by **Team U Recognise** for **SANKALP by Satin Finserv: The Climate Edition** (Theme: Climate Tech).

> **Prototype note:** All model outputs in this version are **mock data** that demonstrate the workflow. The real machine learning model is planned for the next phase.

**Live Demo:**  https://app.netlify.com/projects/woodwitness/deploys/6ac1347db6ec63fdaf9f8238

## The problem

Illegal logging is the most profitable natural resource crime, estimated at $52 to $157 billion a year. It drives deforestation, releases stored carbon, erodes soil, and harms biodiversity. In India, states such as Madhya Pradesh, Chhattisgarh, Maharashtra and Odisha are major hotspots.

Timber passes through many hands before it reaches a buyer, and paper certificates can be forged or laundered along the way. Well-known cases include timber falsely declared as German when it was Russian, and timber relabeled to dodge trade sanctions. Paper records alone cannot prove where wood was actually harvested.

## Our solution

Trees absorb the chemistry of their surroundings, mainly from local rainfall and climate. The oxygen, hydrogen, carbon and sulphur in wood carry a fingerprint of where it grew. WoodWitness compares a wood sample's measured fingerprint with the fingerprint predicted for the claimed location, then returns a statistical verdict with an uncertainty score.

## How it works

1. **Suspicious shipment:** an inspector flags a shipment.
2. **Sampling:** a wood sample goes to a lab, which returns isotope values.
3. **Enter the claim:** the inspector opens a case, sets the claimed location, and enters the lab values.
4. **Verdict:** the tool returns *claim implausible*, *claim not rejected*, or *insufficient confidence*, with a p-value, a confidence level, and which isotope mismatched.
5. **Analysis:** a map shows where the wood could plausibly have come from.
6. **Report:** an audit log and an exportable report serve as supporting evidence.

## Features

- Case form with a clickable map for the claimed location
- Input for four isotopes (δ¹⁸O, δ²H, δ¹³C, δ³⁴S), any subset
- Verdict with p-value, confidence gauge, and per-isotope z-scores
- "Insufficient confidence" response when reference data is thin
- "Show possible origins" heatmap and an uncertainty layer
- Plain-language explanations of every number
- Accuracy-versus-distance chart (illustrative)
- Audit log of every check
- Export report (print to PDF)
- Built-in step-by-step **Tutorial** button
- Demo presets: a false claim and a consistent claim



