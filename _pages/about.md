---
permalink: /
title: "Guolin Yang (杨国林)"
excerpt: "Robotics & Autonomous Systems, World Models, Planning and Safe Control"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<div class="profile-hero">
  <p class="profile-kicker">ROBOTICS & AUTONOMOUS SYSTEMS</p>
  <p class="profile-tagline">World Models · Model-Based RL · MPPI · Safe Control</p>
  <p class="profile-intro">I build predictive planning and safe-control systems for autonomous robots and vehicles operating in dynamic, interactive environments.</p>
  <p class="profile-affiliation">PhD Researcher, University of Manchester · Expected PhD completion: Dec 2026</p>
  <p class="hero-actions">
    <a class="btn btn--primary" href="/research/">Research</a>
    <a class="btn" href="/files/Guolin_Yang_CV_2026.pdf">Download CV</a>
    <a class="btn" href="https://www.linkedin.com/in/guolin-yang-hnu">LinkedIn</a>
  </p>
</div>

<div class="metric-grid">
  <div class="metric-card"><span class="metric-value">+4.8 pp</span><span class="metric-label">OOD success improvement in interaction-aware planning experiments</span></div>
  <div class="metric-card"><span class="metric-value">99.9%</span><span class="metric-label">success in the reported benchmark for the best evaluated configuration</span></div>
  <div class="metric-card"><span class="metric-value">7.8% → 3.8%</span><span class="metric-label">collision-rate reduction with a multi-obstacle discrete-time CBF filter</span></div>
  <div class="metric-card"><span class="metric-value">9.30 ms</span><span class="metric-label">reported safety-filter runtime in the 500-scenario evaluation</span></div>
</div>

## Selected research

<div class="project-grid">
  <article class="project-card">
    <img src="/images/project-pipcn.svg" alt="PIP-CN interaction-aware world model and MPPI planning architecture">
    <div class="project-card__body">
      <p class="project-card__eyebrow">World Models · MBRL · MPPI</p>
      <h3>Interaction-Aware World Models</h3>
      <p>Action-conditioned latent dynamics for multi-step predictive planning in vehicle–pedestrian interaction.</p>
      <p><strong>+4.8 pp OOD success · 99.9% benchmark success</strong></p>
      <a href="/research/#pip-cn">Project details →</a>
    </div>
  </article>

  <article class="project-card">
    <img src="/images/project-safe-mppi.svg" alt="Safety-aware MPPI architecture with CVaR and control barrier functions">
    <div class="project-card__body">
      <p class="project-card__eyebrow">MPPI · CBF · CVaR</p>
      <h3>Safe MPPI under Prediction Uncertainty</h3>
      <p>Long-horizon risk-aware trajectory shaping combined with execution-level safe filtering for uncertain pedestrian motion.</p>
      <p><strong>Up to 65.7% fewer collisions vs. nominal controller</strong></p>
      <a href="/research/#safe-mppi">Project details →</a>
    </div>
  </article>

  <article class="project-card">
    <img src="/images/project-cbf-filter.svg" alt="Real-time multi-obstacle CBF safety filter">
    <div class="project-card__body">
      <p class="project-card__eyebrow">Real-Time Control · CBF · QP</p>
      <h3>Multi-Obstacle Safety Filtering</h3>
      <p>A compact discrete-time CBF correction layer designed to keep online computation small as nearby obstacle count grows.</p>
      <p><strong>7.8% → 3.8% collision rate · 9.30 ms runtime</strong></p>
      <a href="/research/#cbf-filter">Project details →</a>
    </div>
  </article>
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

## Experience at a glance

| Period | Role | Focus |
|---|---|---|
| 2023–Present | PhD Researcher, University of Manchester | World models, MBRL, MPPI/MPC, safe control, autonomous navigation |
| 2023–Present | Graduate Teaching Assistant | Robotics, applied mechanics, industrial robotics, digital control, MPC |
| 2022 | ADAS Engineer, Lotus Technology | C++, camera + HD-map feature logic, CANoe, diagnostics, DFMEA |
| 2021 | BMS Software Intern, NIO | Simulink, CAN/DBC, insulation detection, chamber/bench/vehicle validation |
| 2017–2019 | High-Voltage Lead, Formula Student EV | EV HV architecture, modelling, safety and lightweight battery design |

<p class="status-note"><strong>PhD status:</strong> PhD Researcher / Candidate, 2023–Present. Expected completion: <strong>December 2026</strong>.</p>

## Technical stack

<div class="tech-groups">
  <div class="tech-group">
    <h3>AI & Learning</h3>
    <div class="skill-tags"><span>PyTorch</span><span>Model-Based RL</span><span>World Models</span><span>Learned Dynamics</span><span>Representation Learning</span></div>
  </div>
  <div class="tech-group">
    <h3>Planning & Control</h3>
    <div class="skill-tags"><span>MPPI</span><span>MPC</span><span>Motion Planning</span><span>CBF</span><span>CVaR</span><span>Risk-Aware Control</span></div>
  </div>
  <div class="tech-group">
    <h3>Programming</h3>
    <div class="skill-tags"><span>Python</span><span>C++</span><span>MATLAB / Simulink</span><span>SciPy</span><span>Git</span><span>Docker</span></div>
  </div>
  <div class="tech-group">
    <h3>Simulation & Automotive</h3>
    <div class="skill-tags"><span>CARLA</span><span>IPG CarMaker</span><span>Vector CANoe</span><span>CAN / DBC</span><span>DFMEA</span></div>
  </div>
</div>

## Selected publications & highlights

- **2026:** *A Safety Framework for Uncertainty-Aware Model Predictive Path Integral Control in Shared-Space Navigation* — IEEE CDC 2026, accepted.
- **2026:** *PIP-CN: Prediction-Integrated Planning for Crowd Navigation* — IEEE/RSJ IROS 2026, accepted.
- **2026:** *Risk-Bounded Predictive Control for Automated Vehicles in Shared-Space Areas* — presented at AVEC 2026.
- **2025:** Co-authored work published in *Applied Energy* on intelligent PV-panel cleaning recommendation.
- **2024:** *A Hierarchical Forecasting Model of Pedestrian Crossing Behaviour for Autonomous Vehicle* — *IEEE Access*.

<p class="page-cta">
  <a class="btn btn--primary" href="/research/">Explore research</a>
  <a class="btn" href="/publications/">Publications</a>
  <a class="btn" href="/cv/">CV</a>
</p>
