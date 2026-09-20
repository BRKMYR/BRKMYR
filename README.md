# Product · Spatial Intelligence · Safe Autonomy · AI Assurance

### Product strategist and builder in B2B deep tech: AI & data platforms for autonomous vehicles, spatial data and analytics, and assurance.

Close to a decade in product management. On this GitHub I explore the latest market and technology trends and turn them into AI project prototypes: everything here is personal work, built fully outside of and unrelated to my employment. I build at the intersection of spatial intelligence, autonomous systems and AI safety, with a focus on **Operational Design Domain (ODD) management**: deciding where an automated driving function is cleared to operate and where it must hand back, by road, region and condition, so that agents perceive, reason, and act only where they are cleared to.

Data engines, evals, and RL environments: the data loop behind AD/ADAS, dual use Earth Observation, and industrial automation. Most projects live in private repositories; each one is presented as a case study with a video, leaderboard or live dashboard in my [AI Builder Portfolio](https://brkmyr.com/ai-builder-portfolio/). Public repos are linked where available.

My background in Physical AI goes back to 2016, when I worked with the **iCub humanoid robot** at TU Munich on visual recognition, semantic reasoning, and visual servoing, combining CNNs with structured knowledge so a robot could place objects it had never been trained on and learn new ones from a person. That early work on grounding perception in reasoning shapes how I approach autonomous product development today. See [`icub-visual-recognition`](https://github.com/BRKMYR/icub-visual-recognition), [`icub-semantic-reasoning`](https://github.com/BRKMYR/icub-semantic-reasoning), [`icub-visual-servoing`](https://github.com/BRKMYR/icub-visual-servoing).

---

## Focus Areas

### Safe Autonomy: Assurance, Evals and ODD
ODD management as a clearance question: where an automated driving function may operate, where it must hand back, and how that boundary is maintained in the map rather than discovered in test. Alongside it, safety evaluation for autonomous driving with adversarial scenarios and safety critical metrics on a vendor neutral scorecard, applying **UL 4600** and **SOTIF** (ISO 21448). Real time safety monitoring for robotaxi fleets with teleoperation trigger detection, built in the shape of Waymax and the Waymo Open Motion Dataset and running on synthetic scenes today. Above the benchmarks sits the decision layer, where thresholds exist before the data and every claim carries its evidence. Live: [Assurance Gate](https://huggingface.co/spaces/N20X/assurance-gate).

### Data Engines: Auto-Labeling Economics and Sensor-Fusion Quality
Models are cheap to call and expensive to trust. The decision that sets the cost and quality of a perception program is where you draw the line between what a machine labels alone and what a human confirms. The Label Quality Engine makes that line explicit for 3D: a camera-to-LiDAR fusion labeler and a LiDAR-geometry labeler look at the same frame, agreement is auto-accepted, disagreement is routed, and the engine reports escaped error, per-sensor error attribution and total expected cost as one frontier, so the threshold becomes a decision with a price tag instead of a default. The shipped tier runs on synthetic frames, with the PandaSet loader and the open vocabulary detectors wired in behind a flag and not yet run end to end. Live 3D viewer, threshold sweep and the decision memo a PM would actually write.

### Spatial Intelligence: SAR and Earth Observation
SAR and EO AI pipelines from satellite tasking to intelligence product: a designed Sentinel-1 workflow for change and ship detection and damage assessment, and a vision language analyst console that refuses questions the imaging physics cannot answer. Private repos, case studies in the portfolio.

### World Models and Synthetic Data
World foundation model evaluation for the sim to real gap: six metrics, six failure modes, closed form baselines so the harness itself can be validated. Private repo, case study in the portfolio. Next up: domain randomized synthetic data for long tail edge cases with NVIDIA Omniverse Replicator.

### Agentic AI and Human Machine Teaming
A PettingZoo multi agent environment for manned unmanned teaming in air defence, with enforced safety gates, rules of engagement, human authorization on the path to any consequential action, and AI decision logs that record every call and who approved it. Meaningful human control written as code rather than as policy. Scripted autonomy flies the aircraft today and the reinforcement learning run is shelved. Private repo, case study in the portfolio. Deep RL foundations completed (Stanford XCS224R).

---

## 2026 AI Projects

Ordered by current priority. Private repos are presented as case studies in the [AI Builder Portfolio](https://brkmyr.com/ai-builder-portfolio/); public repos are linked. The last two rows are planned, not started.

| Project | Status | Repo | Focus |
| :--- | :--- | :--- | :--- |
| Assurance Gate | Live | [Space](https://huggingface.co/spaces/N20X/assurance-gate) and [GitHub](https://github.com/BRKMYR/assurance-gate) | Evaluation results in, release decision out. Gates are hashed and published before the run, every rate is reported as a Clopper Pearson bound, and every claim links to the run behind it. Live dashboard, NO GO on the holdout suite, two tracks: driving scenario runs and LLM safety evals. |
| Waymax Safety Monitor | Shipped | Private | Robotaxi teleoperators cannot watch twenty screens. Risk ranked dashboard that surfaces the specific reason a car needs attention and lets the operator rewind: five synthetic scenes, nine trigger kinds, 84 tests, built in the shape of the Waymo Open Motion Dataset. |
| INTENT Operator Console | Prototype | Private | One human stays accountable for several machines under time pressure. Air defence console for manned unmanned teaming over a PettingZoo multi agent testbed: tasking, human authorization that nothing can bypass, and AI decision logs that record every call and who approved it. Three scenarios, a five ship element, 261 tests, scripted autonomy. |
| AV Safety Benchmark | Shipped | Private | Every AV company claims its planner is safer; none of the claims are comparable. Vendor neutral safety scorecard: 60 scenarios, four families, one composite score, 180 runs against three reference planners. |
| Label Quality Engine | v0.1 | Private | Models are cheap to call and expensive to trust. Two labelers look at the same road through different sensors; where they agree the label is kept, where they disagree a human looks, and the engine prices what escapes. The shipped tier runs on synthetic frames. 3D viewer, threshold sweep, per-sensor error attribution, and the decision memo. |
| World Model Benchmark | v0.2 | Private | "Looks realistic" and "is a good world model" are different things. World foundation model evaluation: six metrics, six failure modes, closed form baselines so the harness itself can be validated, toy suite leaderboard. |
| SAR Intelligence Pipeline | Scaffold | Private | Radar works at night and through cloud, but the tooling is scattered across research code. A designed five notebook workflow from Sentinel-1 tiles to a shareable GeoJSON intelligence product, free data only. Nineteen functions are written and no cell has run yet. |
| SAR VLM | Prototype | Private | Natural language analyst console for radar scenes: counts with a confidence trace, refusals where the imaging physics forbids an answer, so no hallucinated counts. A deterministic stand-in encoder answers today, with the SARCLIP radar encoder wired in behind a config flag. |
| Synthetic Data Generation | Planned | Future | Domain randomized pipelines for long tail coverage with NVIDIA Omniverse Replicator and procedural scenario generation. |
| Deep RL for Robotics | Planned | Future | Legged locomotion and manipulation: terrain adaptation, contact rich tasks, sim to real in MuJoCo and Isaac Lab. |

---

## How I Work

I run an AI augmented **PM Operating System** across two environments:

| Context | Tooling | Use Case |
| :--- | :--- | :--- |
| **Personal / AI Builder** | Claude Code (personalized) | GitHub projects, research synthesis, personal productivity |
| **Enterprise PM** | M365 Copilot | Product strategy, roadmaps, business models, stakeholder communication |

---

## Tech Stack

| Layer | Technologies |
| :--- | :--- |
| **Evals & Assurance** | pydantic, numpy, scipy, YAML gate files, Jinja2 report generation, Inspect (LLM safety evals), Clopper Pearson bounds, scene clustered bootstraps, UL 4600, SOTIF (ISO 21448) |
| **Autonomy & Simulation** | Waymax (JAX), Waymo Open Motion Dataset, PettingZoo, Gymnasium, pygame |
| **Perception & Data Engines** | PyTorch, CLIP, Grounding DINO, OWLv2, PandaSet, CVAT, shapely, scikit-image |
| **SAR / EO** | UP42 Python SDK, Rasterio, GeoPandas, Folium, Sentinel-1 (ESA Copernicus) |
| **Serving & Publishing** | FastAPI, SQLModel, plotly.js 3D viewer, static HTML on Cloudflare Pages, Hugging Face Spaces |
| **AI Tooling** | Claude Code, M365 Copilot |
| **Planned** | NVIDIA Omniverse Replicator, Isaac Lab, MuJoCo |

---

## What I Believe

AI is moving into the physical world. Models will commoditize; the platforms that make them safe to deploy will not. That is where to build and where to bet.
