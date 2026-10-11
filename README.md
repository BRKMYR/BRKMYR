# Data & AI Platforms · Spatial Intelligence · Safe Autonomy

### Product strategist and builder in B2B deep tech: data & AI platforms for autonomous vehicles, intelligent machines and systems.

Close to a decade in product management. Here I turn where the market and the technology are moving into working prototypes, built like products: a problem worth solving, a system that runs, success criteria set before the result, and evals that say whether it works. Personal work, unrelated to my employment.

Most repositories are private; each project is presented as a case study in the **[AI Builder Portfolio](https://brkmyr.com/ai-builder-portfolio/)**.

---

## Selected Work

| Project | | What it does |
| :--- | :--- | :--- |
| **Kartograf** | [GitHub](https://github.com/BRKMYR/kartograf) | Ask a city map a question. A local language model writes spatial SQL over open map data, shows the answer on a map with the SQL behind it, and a 20-question eval says how often it is right. |
| **Waymax Safety Monitor** | [GitHub](https://github.com/BRKMYR/waymax-safety-monitor) | Which vehicle needs a human now, and why. A risk-ranked dashboard for remote operators of driverless fleets. |
| **INTENT Operator Console** | Case study | One human stays accountable for several machines, with authorization nothing can bypass and a log of every decision. |
| **Label Quality Engine** | Case study | Two sensors agree, or a human looks. Makes the line between machine labels and human review a priced decision. |
| **World Model Benchmark** | Case study | Six metrics against six failure modes, with baselines that validate the harness itself. |
| **AV Safety Benchmark** | [GitHub](https://github.com/BRKMYR/av-safety-benchmark) | A vendor-neutral safety scorecard for driving planners: 60 scenarios, one composite score. |
| **Assurance Gate** | [GitHub](https://github.com/BRKMYR/assurance-gate) | Eval scores in, release decision out. Thresholds are fixed before the run and every claim links to its evidence. |
| **SAR Intelligence & VLM** | Case study | Ask a radar image a question, and get a refusal where the physics cannot answer. |
| **iCub Object Recognition** | [GitHub](https://github.com/BRKMYR/icub-visual-recognition) | Master's thesis: a humanoid robot names objects it has never seen. |

---

## Tech Stack

| Layer | Technologies |
| :--- | :--- |
| **Evals & Release Gates** | pydantic, numpy, scipy, Inspect, Clopper Pearson bounds, UL 4600, SOTIF (ISO 21448) |
| **Autonomy & Simulation** | Waymax (JAX), Waymo Open Motion Dataset, PettingZoo, Gymnasium |
| **Perception & Data Engines** | PyTorch, CLIP, Grounding DINO, OWLv2, PandaSet, CVAT |
| **Agents & Geospatial** | Ollama (Qwen3, Llama 3.1), DuckDB spatial, Overture Maps, kepler.gl |
| **Earth Observation** | Rasterio, GeoPandas, Sentinel-1 |
| **Serving** | FastAPI, static HTML on Cloudflare, Hugging Face Spaces |

---

## What I Believe

AI is moving into the physical world, and the key enablers are platforms: the data machines learn from, the evals that check them, and the release that puts them to work.
