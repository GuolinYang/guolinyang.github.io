---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
redirect_from:
  - /project/
---

My research focuses on **predictive autonomy**: learning or modelling how a dynamic environment may evolve, evaluating candidate actions over that future, and constraining the final decision when safety is uncertain.

<div class="research-timeline">
  <div><strong>Observe</strong><span>vehicle state + surrounding agents</span></div>
  <div><strong>Predict</strong><span>action-conditioned future evolution</span></div>
  <div><strong>Plan</strong><span>MPPI / MPC over candidate controls</span></div>
  <div><strong>Act safely</strong><span>CBF / CVaR execution constraints</span></div>
  <div><strong>Replan</strong><span>closed-loop update from new observations</span></div>
</div>

## Flagship projects

<a id="pip-cn"></a>
<section class="research-project">
  <img class="research-project__image" src="/images/project-pipcn.svg" alt="PIP-CN action-conditioned world model and MPPI planning pipeline">
  <div class="research-project__content">
    <p class="project-card__eyebrow">WORLD MODELS · MODEL-BASED RL · MPPI</p>
    <h2>Interaction-Aware World Models for Predictive Planning — PIP-CN</h2>
    <p><strong>Problem.</strong> In crowd navigation, prediction and planning are coupled: slowing, turning, or continuing forward can change nearby pedestrian behaviour. A useful predictive model therefore needs to represent how the environment evolves <em>under the ego action</em>, not just extrapolate other agents independently.</p>
    <p><strong>My contribution.</strong> I designed and implemented a recurrent latent world model that combines action-conditioned dynamics, pedestrian interaction modelling, collision-risk prediction, reward/value estimation, and sampling-based planning. Candidate action sequences are rolled forward in latent space and evaluated through MPPI-style predictive control.</p>
    <p><strong>Result.</strong> The best reported configuration reached <strong>99.9% success</strong> in the evaluated benchmark, while the proposed approach improved out-of-distribution success by <strong>4.8 percentage points</strong> in the reported transfer setting.</p>
    <p class="project-methods"><strong>Tech:</strong> PyTorch · Model-Based RL · TD-MPC-style latent prediction · recurrent dynamics · attention · collision prediction · MPPI/MPC · CARLA · custom simulation</p>
    <p><strong>Paper:</strong> G. Yang, A. S. Chen, A. Parisio, and G. Herrmann, “PIP-CN: Prediction-Integrated Planning for Crowd Navigation,” IEEE/RSJ IROS 2026. <a href="https://nottingham-repository.worktribe.com/output/66916793">Repository record →</a></p>
  </div>
</section>

<a id="safe-mppi"></a>
<section class="research-project">
  <img class="research-project__image" src="/images/project-safe-mppi.svg" alt="Risk-aware MPPI with long-horizon CVaR shaping and execution-level CBF filtering">
  <div class="research-project__content">
    <p class="project-card__eyebrow">MPPI · CONTROL BARRIER FUNCTIONS · CVAR</p>
    <h2>Safety-Aware MPPI under Prediction Uncertainty</h2>
    <p><strong>Problem.</strong> Standard MPPI can penalise risky trajectories, but its executed command is an importance-weighted average of sampled first-step controls. A soft trajectory penalty therefore does not directly impose a safety condition on the final action, especially when pedestrian forecasts are uncertain.</p>
    <p><strong>My contribution.</strong> I developed a two-layer safety framework that separates <strong>long-horizon risk-aware trajectory shaping</strong> from <strong>execution-level action filtering</strong>. Robust CBF-based costs and CVaR emphasise tail-critical pedestrian interactions during planning, while a current-time local convex safe set constrains the command that is actually applied.</p>
    <p><strong>Result.</strong> Across the broader safety-aware control studies, the proposed methods reduced collisions by <strong>up to 65.7%</strong> relative to the nominal controller in the evaluated benchmarks.</p>
    <p class="project-methods"><strong>Tech:</strong> MPPI · discrete-time CBF · CVaR · robust optimisation · local linearisation · uncertainty sampling · nonlinear vehicle dynamics · quadratic programming</p>
    <p><strong>Paper:</strong> G. Yang, A. S. Chen, A. Parisio, and G. Herrmann, “A Safety Framework for Uncertainty-Aware Model Predictive Path Integral Control in Shared-Space Navigation,” IEEE CDC 2026. <a href="https://nottingham-repository.worktribe.com/output/70308951">Repository record →</a></p>
  </div>
</section>

<a id="cbf-filter"></a>
<section class="research-project">
  <img class="research-project__image" src="/images/project-cbf-filter.svg" alt="Compact multi-obstacle discrete-time control barrier function safety filter">
  <div class="research-project__content">
    <p class="project-card__eyebrow">REAL-TIME CONTROL · CBF · QP</p>
    <h2>Real-Time Multi-Obstacle Safety Filtering</h2>
    <p><strong>Problem.</strong> Applying a separate online safety constraint for every moving obstacle can increase computational burden as pedestrian density grows.</p>
    <p><strong>My contribution.</strong> I developed a compact discrete-time CBF formulation that aggregates moving-obstacle safety information into a small online correction layer for sampling-based predictive control.</p>
    <p><strong>Result.</strong> Across <strong>500 evaluated scenarios</strong>, collision rate decreased from <strong>7.8% to 3.8%</strong>, with a reported <strong>9.30 ms</strong> safety-filter runtime.</p>
    <p class="project-methods"><strong>Tech:</strong> discrete-time CBF · multi-obstacle constraints · quadratic programming · real-time control · scenario-based evaluation</p>
  </div>
</section>

## Additional research

<a id="risk-bounded"></a>
### Risk-Bounded Predictive Control in Shared Spaces

This work studies uncertain pedestrian forecasts through a local, sample-based CVaR safety interpretation. A nominal MPPI command is corrected when predicted tail risk exceeds a prescribed risk budget, using a convex quadratic program with vehicle-input bounds.

**Publication:** G. Yang, A. S. Chen, A. Parisio, and G. Herrmann, “Risk-Bounded Predictive Control for Automated Vehicles in Shared-Space Areas,” International Symposium on Advanced Vehicle Control (AVEC), 2026.

<a id="hfpm"></a>
### Hierarchical Pedestrian Forecasting for Autonomous-Vehicle Simulation

Before the world-model work, I developed a hierarchical pedestrian model for shared-space simulation. The model combines pedestrian dynamics, path planning, and decision layers so simulated pedestrians can respond to vehicle behaviour rather than following fixed trajectories.

**Publication:** G. Yang, E. J. Lopez Pulgarin, and G. Herrmann, “A Hierarchical Forecasting Model of Pedestrian Crossing Behaviour for Autonomous Vehicle,” *IEEE Access*, vol. 12, pp. 9025–9037, 2024. [DOI](https://doi.org/10.1109/ACCESS.2024.3352499)

<a id="vehicle-dynamics"></a>
### Vehicle Dynamics, MPC and Autonomous Racing

My vehicle-engineering foundation includes four-wheel vehicle dynamics, Pacejka tyre-force modelling, MPC-based trajectory planning / tracking, and IPG CarMaker closed-loop simulation. This physical modelling and control background later connected naturally to learned predictive models and sampling-based planning.

**Methods / tools:** MATLAB · MPC · Pacejka tyre model · IPG CarMaker · vehicle dynamics
