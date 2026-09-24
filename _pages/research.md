---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
redirect_from:
  - /project/
---

My research sits at the intersection of **learned predictive models, planning, and safety-critical control**. The common structure is closed-loop: observe the environment, predict how it may evolve under candidate actions, choose a control action, execute it, and replan from new observations.

<div class="research-timeline">
  <div><strong>World model</strong><span>learn compact state and action-conditioned dynamics</span></div>
  <div><strong>Prediction</strong><span>roll candidate futures forward over multiple steps</span></div>
  <div><strong>Planning</strong><span>rank control sequences with MPPI / MPC</span></div>
  <div><strong>Safety</strong><span>constrain risk with CBF / CVaR mechanisms</span></div>
</div>

<a id="pip-cn"></a>
## 1. Interaction-aware world models for predictive planning — PIP-CN

**Problem.** In crowd navigation, prediction and planning should not be treated as independent modules: a vehicle slowing, turning, or continuing forward can change nearby pedestrian behaviour. A useful predictive model therefore needs to be conditioned on the ego action and retain information that matters for downstream decisions.

**Approach.** I developed a recurrent latent world-model architecture for dynamic multi-agent navigation. It combines an encoder, action-conditioned latent transition model, pedestrian interaction modelling, reward/value estimation, and a collision-prediction head. Candidate action sequences are rolled through the learned model and evaluated by a sampling-based planner.

**Outcome.** In the reported benchmark, the best evaluated configuration reached **99.9% success**, while the proposed approach improved out-of-distribution success by **4.8 percentage points** in the evaluated transfer setting.

**Methods / tools:** Model-Based RL · TD-MPC-style latent prediction · recurrent dynamics · attention · collision prediction · MPPI/MPC · PyTorch · CARLA · custom simulation

**Publication:** G. Yang, A. S. Chen, A. Parisio, and G. Herrmann, “PIP-CN: Prediction-Integrated Planning for Crowd Navigation,” IEEE/RSJ IROS 2026. [Repository record](https://nottingham-repository.worktribe.com/output/66916793)

<a id="safe-mppi"></a>
## 2. Uncertainty-aware safe MPPI with CBF and CVaR

**Problem.** MPPI is effective for nonlinear, non-convex planning, but the executed command is an importance-weighted average of sampled first-step controls. Cost penalties alone therefore do not directly impose a hard safety condition on the final applied action, especially when pedestrian prediction is uncertain.

**Approach.** I developed a two-layer safety framework that combines long-horizon trajectory shaping with execution-level filtering. Robust CBF-based costs and CVaR emphasise tail-critical pedestrian interactions during planning, while a current-time local convex safe set constrains the action that is actually applied.

**Outcome.** The broader safety-aware control studies reduced collisions by **up to 65.7%** relative to the nominal controller in evaluated benchmarks.

**Methods / tools:** MPPI · discrete-time CBF · CVaR · robust optimisation · local linearisation · uncertainty sampling · nonlinear vehicle dynamics

**Publication:** G. Yang, A. S. Chen, A. Parisio, and G. Herrmann, “A Safety Framework for Uncertainty-Aware Model Predictive Path Integral Control in Shared-Space Navigation,” IEEE CDC 2026. [Repository record](https://nottingham-repository.worktribe.com/output/70308951)

<a id="cbf-filter"></a>
## 3. Efficient multi-obstacle safety filtering

**Problem.** Applying one safety constraint per moving obstacle can increase the online optimisation burden as the number of nearby pedestrians grows.

**Approach.** I developed a computationally efficient discrete-time CBF formulation that aggregates moving-obstacle safety information into a compact online correction layer for sampling-based predictive control.

**Outcome.** Across **500 evaluated scenarios**, the filter reduced collision rate from **7.8% to 3.8%** with a reported **9.30 ms** filtering runtime.

**Methods / tools:** discrete-time CBF · multi-obstacle constraints · quadratic programming · real-time control · scenario-based evaluation

<a id="risk-bounded"></a>
## 4. Risk-bounded predictive control in shared spaces

This work studies uncertain pedestrian forecasts through a local, sample-based CVaR safety interpretation. A nominal MPPI command is corrected when predicted tail risk exceeds a prescribed risk budget, using a convex quadratic program with vehicle-input bounds.

**Publication:** G. Yang, A. S. Chen, A. Parisio, and G. Herrmann, “Risk-Bounded Predictive Control for Automated Vehicles in Shared-Space Areas,” International Symposium on Advanced Vehicle Control (AVEC), 2026.

<a id="hfpm"></a>
## 5. Hierarchical pedestrian forecasting for autonomous-vehicle simulation

Before the world-model work, I developed a hierarchical pedestrian model for shared-space simulation. The model combines a pedestrian dynamics layer, path-planning layer, and decision layer so that simulated pedestrians can respond to vehicle behaviour rather than following fixed trajectories.

**Publication:** G. Yang, E. J. Lopez Pulgarin, and G. Herrmann, “A Hierarchical Forecasting Model of Pedestrian Crossing Behaviour for Autonomous Vehicle,” *IEEE Access*, vol. 12, pp. 9025–9037, 2024. [DOI](https://doi.org/10.1109/ACCESS.2024.3352499)

<a id="vehicle-dynamics"></a>
## 6. Vehicle dynamics, MPC and autonomous racing

My vehicle-engineering foundation includes four-wheel vehicle dynamics, Pacejka tyre-force modelling, MPC-based trajectory planning / tracking, and IPG CarMaker closed-loop simulation. This work established the physical modelling and control background that later connected naturally to learned predictive models and sampling-based planning.

**Methods / tools:** MATLAB · MPC · Pacejka tyre model · IPG CarMaker · vehicle dynamics
