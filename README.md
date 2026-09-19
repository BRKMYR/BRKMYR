# Product Manager · Spatial Intelligence · Safe Autonomy · Physical AI

### Product strategist and builder in B2B deep tech: AI & data platforms for autonomous vehicles, Physical and Industrial AI.

Close to a decade in product management. On this GitHub I explore the latest market and technology trends and turn them into AI project prototypes: everything here is personal work, built fully outside of and unrelated to my employment. I build at the intersection of spatial intelligence, autonomous systems and AI safety, with a focus on **Operational Design Domain (ODD) management**: deciding where an automated driving function is cleared to operate and where it must hand back, by road, region and condition, so that agents perceive, reason, and act only where they are cleared to.

Data engines, evals, and RL environments: the data loop behind AD/ADAS, dual use Earth Observation, and industrial automation. Most projects live in private repositories; each one is presented as a case study with a video, leaderboard or live dashboard in my [AI Builder Portfolio](https://brkmyr.com/ai-builder-portfolio/). Public repos are linked where available.

My background in Physical AI goes back to 2016, when I worked with the **iCub humanoid robot** at TU Munich on visual recognition, semantic reasoning, and visual servoing, combining CNNs with structured knowledge so a robot could recognize objects it had never seen. That early work on grounding perception in reasoning shapes how I approach autonomous product development today. See [`icub-visual-recognition`](https://github.com/BRKMYR/icub-visual-recognition), [`icub-semantic-reasoning`](https://github.com/BRKMYR/icub-semantic-reasoning), [`icub-visual-servoing`](https://github.com/BRKMYR/icub-visual-servoing).

---

## Focus Areas

### Safe Autonomy: Assurance, Evals and ODD
ODD management as a clearance question: where an automated driving function may operate, where it must hand back, and how that boundary is maintained in the map rather than discovered in test. Alongside it, safety evaluation for autonomous driving with adversarial scenarios and safety critical metrics on a vendor neutral scorecard, applying **UL 4600** and **SOTIF** (ISO 21448). Real time safety monitoring for robotaxi fleets with teleoperation trigger detection on Waymax and the Waymo Open Motion Dataset. Above the benchmarks sits the decision layer, where thresholds exist before the data and every claim carries its evidence. Live: [Assurance Gate](https://huggingface.co/spaces/N20X/assurance-gate).

### Data Engines: Auto-Labeling Economics and Sensor-Fusion Quality
Models are cheap to call and expensive to trust. The decision that sets the cost and quality of a perception program is where you draw the line between what a machine labels alone and what a human confirms. [`label-quality-engine`](https://github.com/BRKMYR/label-quality-engine) makes that line explicit for 3D: a camera-to-LiDAR fusion labeler and a LiDAR-geometry labeler look at the same frame, agreement is auto-accepted, disagreement is routed, and the engine reports escaped error, per-sensor error attribution and total expected cost as one frontier, so the threshold becomes a decision with a price tag instead of a default. Built on PandaSet, Grounding DINO, OWLv2, CVAT and plotly. Public repo, live 3D viewer, and the decision memo a PM would actually write.

### Spatial Intelligence: SAR and Earth Observation
SAR and EO AI pipelines from satellite tasking to intelligence product: Sentinel-1 acquisition, change and ship detection, damage assessment, and a vision language analyst console that refuses questions the imaging physics cannot answer. Private repos, case studies in the portfolio.

### World Models and Synthetic Data
World foundation model evaluation for the sim to real gap: six metrics, six failure modes, closed form baselines so the harness itself can be validated. Private repo, case study in the portfolio. Next up: domain randomized synthetic data for long tail edge cases with NVIDIA Omniverse Replicator.

### Agentic AI and Human Machine Teaming
Multi agent reinforcement learning for manned unmanned teaming with enforced safety gates, rules of engagement, engagement authorization, and AI decision logs that record every call the system made and why. Private repo, case study in the portfolio. Deep RL foundations completed (Stanford XCS224R).

---

## 2026 AI Projects

Ordered by current priority. Private repos are presented as case studies in the [AI Builder Portfolio](https://brkmyr.com/ai-builder-portfolio/); public repos are linked. The last two rows are planned, not started.

| Project | Status | Repo | Focus |
| :--- | :--- | :--- | :--- |
| Assurance Gate | Shipped | Private | Evaluation results in, release decision out. Gates are hashed and published before the run, every rate is reported as a Clopper Pearson bound, and every claim links to the run behind it. Live dashboard, NO GO on demo data (3 of 9 gates), two tracks: driving scenario runs and LLM safety evals. |
| Waymax Safety Monitor | Shipped | Private | Robotaxi teleoperators cannot watch twenty screens. Risk ranked fleet dashboard that surfaces the specific reason a car needs attention and lets the operator rewind: three scenarios, seven trigger kinds, on the Waymo Open Motion Dataset. |
| INTENT Operator Console | Shipped | Private | One human, several unmanned wingmen, time pressure. Manned unmanned teaming C2 console over a PettingZoo MARL testbed: tasking, engagement authorization, and AI decision logs that record every call the system made and why. |
| AV Safety Benchmark | Shipped | Private | Every AV company claims its planner is safer; none of the claims are comparable. Vendor neutral safety scorecard: 60 scenarios, four families, one composite score; 180 runs against three baselines. |
| Label Quality Engine | v0.1 | Public | Models are cheap to call and expensive to trust. Two labelers look at the same road through different sensors; where they agree the label is kept, where they disagree a human looks, and the engine prices what escapes. 3D viewer, threshold sweep, per-sensor error attribution, and the decision memo. See [`label-quality-engine`](https://github.com/BRKMYR/label-quality-engine). |
| World Model Benchmark | v0.2 | Private | "Looks realistic" and "is a good world model" are different things. World foundation model evaluation: six metrics, six failure modes, closed form baselines so the harness itself can be validated, toy suite leaderboard. |
| SAR Intelligence Pipeline | Shipped | Private | Radar works at night and through cloud, but the tooling is scattered across research code. Five notebooks from Sentinel-1 tiles to a shareable GeoJSON intelligence product, free data only. |
| SAR VLM | Shipped | Private | Natural language analyst console for radar scenes: counts with a confidence trace, refusals where the imaging physics forbids an answer, so no hallucinated counts. Live console mock on real API responses. |
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
