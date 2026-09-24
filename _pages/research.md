---
layout: archive
title: "Research"
permalink: /research/
author_profile: false
redirect_from:
  - /project/
---

My research focuses on predictive autonomy for robots and autonomous vehicles operating in dynamic, interactive environments. The main themes are world models, model-based reinforcement learning, sampling-based model predictive control, and safety-aware planning under uncertain human motion.

## Interaction-Aware World Models for Predictive Planning — PIP-CN
<a id="pip-cn"></a>

**Problem.** In crowd navigation, prediction and planning are coupled: a vehicle slowing, turning, or continuing forward can change nearby pedestrian behaviour. Predicting other agents independently from the ego action can therefore lead to poor planning decisions.

**Contribution.** I developed a recurrent latent world-model architecture that combines action-conditioned dynamics, pedestrian-interaction modelling, collision-risk prediction, reward/value estimation, and sampling-based predictive planning. Candidate action sequences are rolled forward in latent space and evaluated through MPPI-style control.

**Results.** The best reported configuration reached **99.9% success** in the evaluated benchmark and improved out-of-distribution success by **4.8 percentage points** in the reported transfer setting.

**Tech:** PyTorch · Model-Based RL · TD-MPC-style latent prediction · recurrent dynamics · attention · collision prediction · MPPI/MPC · CARLA · custom simulation

**Publication:** G. Yang, A. S. Chen, A. Parisio, and G. Herrmann, “PIP-CN: Prediction-Integrated Planning for Crowd Navigation,” IEEE/RSJ IROS 2026. [Repository record](https://nottingham-repository.worktribe.com/output/66916793)

---

## Safety-Aware MPPI under Prediction Uncertainty
<a id="safe-mppi"></a>

**Problem.** Standard MPPI can penalise risky trajectories, but the command finally applied to the system is an importance-weighted combination of sampled controls. Soft trajectory penalties alone do not directly guarantee that the executed first-step action satisfies a safety condition, especially with uncertain pedestrian forecasts.

**Contribution.** I developed a two-layer safety framework that separates long-horizon risk-aware trajectory shaping from execution-level action filtering. Robust CBF-based costs and CVaR emphasise tail-critical interactions during planning, while a current-time convex safe set constrains the action that is actually executed.

**Results.** Across the broader safety-aware control studies, the proposed methods reduced collisions by **up to 65.7%** relative to the nominal controller in the evaluated benchmarks.

**Tech:** MPPI · discrete-time CBF · CVaR · robust optimisation · uncertainty sampling · nonlinear vehicle dynamics · quadratic programming

**Publication:** G. Yang, A. S. Chen, A. Parisio, and G. Herrmann, “A Safety Framework for Uncertainty-Aware Model Predictive Path Integral Control in Shared-Space Navigation,” IEEE CDC 2026. [Repository record](https://nottingham-repository.worktribe.com/output/70308951)

---

## Real-Time Multi-Obstacle Safety Filtering
<a id="cbf-filter"></a>

**Problem.** Applying one online safety constraint per moving obstacle can increase computational burden as pedestrian density grows.

**Contribution.** I developed a compact discrete-time CBF safety-filter formulation that aggregates moving-obstacle safety information into a small online correction layer for sampling-based predictive control.

**Results.** Across **500 evaluated scenarios**, the filter reduced collision rate from **7.8% to 3.8%** with a reported **9.30 ms** runtime.

**Tech:** discrete-time CBF · multi-obstacle constraints · quadratic programming · real-time control · scenario-based evaluation

---

## Risk-Bounded Predictive Control in Shared Spaces
<a id="risk-bounded"></a>

This work studies uncertain pedestrian forecasts using a local, sample-based CVaR safety interpretation. A nominal MPPI command is corrected when predicted tail risk exceeds a prescribed risk budget, using a convex quadratic program with vehicle-input bounds.

**Publication:** G. Yang, A. S. Chen, A. Parisio, and G. Herrmann, “Risk-Bounded Predictive Control for Automated Vehicles in Shared-Space Areas,” International Symposium on Advanced Vehicle Control (AVEC), 2026.

---

## Hierarchical Pedestrian Forecasting for Autonomous-Vehicle Simulation
<a id="hfpm"></a>

Before the world-model work, I developed a hierarchical pedestrian model for shared-space simulation. The model combines pedestrian dynamics, path planning, and decision layers so simulated pedestrians can respond to vehicle behaviour rather than following fixed trajectories.

**Publication:** G. Yang, E. J. Lopez Pulgarin, and G. Herrmann, “A Hierarchical Forecasting Model of Pedestrian Crossing Behaviour for Autonomous Vehicle,” *IEEE Access*, vol. 12, pp. 9025–9037, 2024. [DOI](https://doi.org/10.1109/ACCESS.2024.3352499)

---

## Vehicle Dynamics, MPC and Autonomous Racing
<a id="vehicle-dynamics"></a>

My vehicle-engineering foundation includes four-wheel vehicle dynamics, Pacejka tyre-force modelling, MPC-based trajectory planning and tracking, and IPG CarMaker closed-loop simulation. This physical modelling and control background later connected naturally to learned predictive models and sampling-based planning.

**Tech:** MATLAB · MPC · Pacejka tyre model · IPG CarMaker · vehicle dynamics
