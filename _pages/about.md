---
permalink: /
title: "Guolin Yang (杨国林)"
excerpt: "Robotics, world models, model-based reinforcement learning, planning and safe control"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<div class="profile-lead">
  <p class="profile-kicker">ROBOTICS · WORLD MODELS · PLANNING · SAFE CONTROL</p>
  <p class="profile-intro">
    I am a PhD researcher in the Control Systems & Robotics / Robotics and AI community at the
    <a href="https://www.manchester.ac.uk/">University of Manchester</a>. My work focuses on
    <strong>world models, model-based reinforcement learning, predictive planning, and safety-aware control</strong>
    for autonomous systems operating in dynamic, interactive environments.
  </p>
</div>

My research asks a practical question: **how can an autonomous system learn what may happen next, reason about how its own actions change that future, and use those predictions to plan safely in real time?** I work on action-conditioned learned dynamics, latent world models, MPPI/MPC, Control Barrier Functions (CBFs), and risk-aware planning under uncertain pedestrian motion.

Before my PhD, I worked on ADAS software at **Lotus Technology** and battery-management-system software and validation at **NIO**. My earlier vehicle-engineering work included four-wheel vehicle dynamics, Pacejka tyre modelling, MPC-based trajectory control, IPG CarMaker, and Formula Student EV high-voltage systems.

<div class="metric-grid">
  <div class="metric-card"><span class="metric-value">+4.8 pp</span><span class="metric-label">OOD success improvement in interaction-aware planning experiments</span></div>
  <div class="metric-card"><span class="metric-value">99.9%</span><span class="metric-label">success in the reported benchmark for the best evaluated configuration</span></div>
  <div class="metric-card"><span class="metric-value">7.8% → 3.8%</span><span class="metric-label">collision-rate reduction with a multi-obstacle discrete-time CBF filter</span></div>
  <div class="metric-card"><span class="metric-value">9.30 ms</span><span class="metric-label">reported safety-filter runtime in the 500-scenario evaluation</span></div>
</div>

## Research focus

<div class="research-grid">
  <div class="research-card">
    <h3>World Models & Model-Based RL</h3>
    <p>Learning compact latent representations and action-conditioned dynamics for multi-step prediction in interactive environments.</p>
  </div>
  <div class="research-card">
    <h3>Predictive Planning</h3>
    <p>Using MPC / MPPI and sampling-based optimisation to evaluate candidate actions through predicted future system evolution.</p>
  </div>
  <div class="research-card">
    <h3>Safe & Risk-Aware Control</h3>
    <p>Combining Control Barrier Functions, CVaR and robust constraints with sampling-based control under prediction uncertainty.</p>
  </div>
  <div class="research-card">
    <h3>Autonomous Systems</h3>
    <p>Closed-loop evaluation in custom simulators, CARLA and vehicle-oriented environments, with emphasis on dynamic multi-agent interaction.</p>
  </div>
</div>

## Technical stack

<div class="skill-tags">
  <span>Python</span><span>C++</span><span>PyTorch</span><span>MATLAB / Simulink</span>
  <span>MPPI</span><span>MPC</span><span>Model-Based RL</span><span>World Models</span>
  <span>CBF</span><span>CVaR</span><span>CARLA</span><span>IPG CarMaker</span>
  <span>Vector CANoe</span><span>CAN / DBC</span><span>Git</span><span>Docker</span>
</div>

## Selected work

**Prediction-Integrated Planning for Crowd Navigation (PIP-CN).** I developed an interaction-aware, recurrent latent world model in which planned ego actions influence future state predictions. The model combines pedestrian-interaction modelling, collision-risk prediction, reward/value estimation, and sampling-based planning. [Research details →](/research/#pip-cn)

**Safety-aware MPPI under uncertain pedestrian prediction.** I developed execution-level safety mechanisms for sampling-based control using discrete-time CBFs, robust safety constraints, and CVaR-based tail-risk reasoning. [Research details →](/research/#safe-mppi)

**Pedestrian behaviour prediction and simulation.** My earlier work developed a hierarchical forecasting pedestrian model for autonomous-vehicle simulation, combining dynamics, path planning and decision layers. [Publication →](https://doi.org/10.1109/ACCESS.2024.3352499)

## Experience at a glance

| Period | Role | Focus |
|---|---|---|
| 2023–Present | PhD Researcher, University of Manchester | World models, MBRL, MPPI/MPC, safe control, autonomous navigation |
| 2023–Present | Graduate Teaching Assistant | Robotics, applied mechanics, industrial robotics, digital control, MPC |
| 2022 | ADAS Engineer, Lotus Technology | C++, camera + HD-map feature logic, CANoe, diagnostics, DFMEA |
| 2021 | BMS Software Intern, NIO | Simulink, CAN/DBC, insulation detection, chamber/bench/vehicle validation |
| 2017–2019 | High-Voltage Lead, Formula Student EV | EV HV architecture, modelling, safety and lightweight battery design |

## Education

- **PhD in Electrical Engineering**, University of Manchester, 2023–2026. Research in world models, model-based reinforcement learning, predictive planning and safety-critical control. Supervisors: Prof. Guido Herrmann and Prof. Alessandra Parisio.
- **MSc in Advanced Control and Systems Engineering**, University of Manchester, 2020–2022. Research Excellence Award and Top Student Award (2022).
- **BEng in Vehicle Engineering**, Hunan University, 2016–2020. Thesis on motion planning and dynamics control of an autonomous racing car.

## Recent highlights

- **2026:** Paper accepted to the IEEE Conference on Decision and Control (CDC): *A Safety Framework for Uncertainty-Aware Model Predictive Path Integral Control in Shared-Space Navigation*.
- **2026:** *PIP-CN: Prediction-Integrated Planning for Crowd Navigation* accepted to IEEE/RSJ IROS 2026.
- **2026:** *Risk-Bounded Predictive Control for Automated Vehicles in Shared-Space Areas* presented at AVEC 2026.
- **2025:** Co-authored work published in *Applied Energy* on intelligent PV-panel cleaning recommendation.
- **2024:** Published *A Hierarchical Forecasting Model of Pedestrian Crossing Behaviour for Autonomous Vehicle* in *IEEE Access*.

<p class="page-cta">
  <a class="btn btn--primary" href="/research/">Research</a>
  <a class="btn btn--primary" href="/publications/">Publications</a>
  <a class="btn btn--primary" href="/cv/">CV</a>
</p>
