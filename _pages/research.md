---
layout: main
title: Research
permalink: /research/
---

<div class="research-section">
  <h1>Research</h1>

  <div class="research-header-image">
    <img src="/assets/img/others/HRT.png" alt="Human-Robot Teams">
  </div>

  <div class="research-intro">
    <p>
      Our mission is to develop theoretical foundations and practical algorithms for human-interactive robotics.
      Our group focuses on enabling robots to learn from and collaborate with humans in real-world environments.
      We leverage tools from machine learning, control theory, and human-robot interaction to build intelligent,
      adaptive, and safe robotic systems.
    </p>
  </div>

  <div class="research-areas">
    <div class="research-area">
      <div class="research-area-content">
        <h2>Interactive Reinforcement Learning</h2>
        <p>
          We develop methods for robots to learn complex manipulation tasks through hierarchical reinforcement
          learning and imitation learning. Our work on <strong>Impedance Primitive-Augmented Hierarchical RL</strong>
          (ICRA 2025) augments high-level RL policies with impedance control primitives to solve long-horizon
          sequential tasks, enabling compliant and adaptive skill acquisition. We also investigate robust imitation
          learning — including methods that exploit <strong>mixed-quality demonstrations</strong> (Beyond the Teacher,
          ICRA 2026) and <strong>progress-aligned data curation</strong> (PACER, CoRL Workshop 2025) to improve
          generalization from imperfect human teachers, as well as stochastic encodings (RISE, IROS Workshop 2025)
          for robust policy learning.
        </p>
        <div class="pub-links-inline">
          <a href="https://ieeexplore.ieee.org/abstract/document/11128462" target="_blank" class="pub-link-text">ImpHRL (ICRA'25)</a>
          <a href="https://focaslab.github.io/beyondtheteacher/" target="_blank" class="pub-link-text">Beyond the Teacher (ICRA'26)</a>
          <a href="https://openreview.net/forum?id=gaYyBvP2Rz" target="_blank" class="pub-link-text">PACER</a>
          <a href="https://openreview.net/forum?id=GEexdUmA67" target="_blank" class="pub-link-text">RISE</a>
        </div>
      </div>
      <div class="research-area-image">
        <img src="/assets/img/publication_preview/icra_imphrl_25.gif" alt="Impedance Hierarchical RL">
      </div>
    </div>

    <div class="research-area">
      <div class="research-area-content">
        <h2>Foundational Models for Robotics</h2>
        <p>
          We explore how large-scale pre-trained vision-language models can enable natural, flexible
          robot-human interaction. Our work on <strong>OVITA</strong> (Open-Vocabulary Interpretable Trajectory
          Adaptations, RA-L 2025) uses vision-language models to adapt robot trajectories in real time based on
          open-vocabulary human language instructions, providing interpretable modifications without retraining.
          We also develop <strong>DiffusionPack</strong> (NeurIPS Workshop 2025), a diffusion-based approach for
          complex bin-packing manipulation tasks that incorporates custom human preferences, bridging language,
          world models, and physical robot execution.
        </p>
        <div class="pub-links-inline">
          <a href="https://ieeexplore.ieee.org/abstract/document/11150730" target="_blank" class="pub-link-text">OVITA (RA-L'25)</a>
          <a href="https://anurag1000101.github.io/projects/IISC/" target="_blank" class="pub-link-text">Project Site</a>
          <a href="https://openreview.net/forum?id=uReNc199fG" target="_blank" class="pub-link-text">DiffusionPack</a>
        </div>
      </div>
      <div class="research-area-image">
        <img src="/assets/img/publication_preview/ovita_25.gif" alt="OVITA Trajectory Adaptation">
      </div>
    </div>

    <div class="research-area">
      <div class="research-area-content">
        <h2>Safe and Compliant Human-Robot Interaction</h2>
        <p>
          Safety and compliance are essential when robots work alongside humans. Our work on <strong>SafeDMPs</strong>
          (ICRA 2026) integrates Signal Temporal Logic (STL)-based formal safety specifications directly into Dynamic
          Movement Primitives, enabling adaptive robot motions that are provably safe during physical human-robot
          contact. We also develop <strong>certified reinforcement learning for variable impedance control</strong>
          (ICRA 2026), which combines Lyapunov-based stability certificates with RL to achieve optimal, safe impedance
          modulation during interaction. Our stability-aware PI² framework (ICRA Workshop 2025) further extends these
          ideas for safe interaction under uncertainty.
        </p>
        <div class="pub-links-inline">
          <a href="https://arxiv.org/abs/2509.16482" target="_blank" class="pub-link-text">SafeDMPs (ICRA'26)</a>
          <a href="https://tiwari-pranav.github.io/SafeDMPs/" target="_blank" class="pub-link-text">Project Site</a>
          <a href="https://openreview.net/forum?id=Xj3V96qTpf" target="_blank" class="pub-link-text">CoRL Workshop</a>
        </div>
      </div>
      <div class="research-area-image">
        <img src="/assets/img/publication_preview/safedmps_26.png" alt="Safe DMPs for HRI">
      </div>
    </div>

    <div class="research-area">
      <div class="research-area-content">
        <h2>3D Reconstruction, SLAM and World Models</h2>
        <p>
          We develop methods for robots to build accurate 3D models of their environment through active perception.
          Our work includes SLAM (Simultaneous Localization and Mapping), real-time scene reconstruction, world models
          for spatial understanding, object-level mapping, and integration with manipulation planning to enable robots
          to operate effectively in complex, unstructured spaces.
        </p>
      </div>
      <div class="research-area-image">
        <img src="/assets/img/others/slam.png" alt="3D Reconstruction and SLAM">
      </div>
    </div>

    <div class="research-area">
      <div class="research-area-content">
        <h2>Optimization and Optimal Control</h2>
        <p>
          We develop optimization-based and data-driven approaches for robot motion planning and control.
          Our <strong>Adaptive Critic</strong> framework (IEEE T-CST 2025) learns optimal controllers for uncertain
          robot manipulators using neural network-based value function approximation, achieving data-efficient online
          adaptation without explicit system identification. Our work on <strong>generalizable motion policies through
          keypoint parameterization and transportation maps</strong> (IEEE T-RO 2025) enables one-shot generalization
          of manipulation skills to novel object configurations. We also develop <strong>ST²</strong> (Sequentially
          Teaching Sequential Tasks, RA-M 2026), a framework for teaching robots long-horizon manipulation skills
          through sequential human demonstrations.
        </p>
        <div class="pub-links-inline">
          <a href="https://ieeexplore.ieee.org/abstract/document/10718695" target="_blank" class="pub-link-text">Adaptive Critic (T-CST'25)</a>
          <a href="https://ieeexplore.ieee.org/abstract/document/11049008" target="_blank" class="pub-link-text">Motion Policies (T-RO'25)</a>
          <a href="https://ieeexplore.ieee.org/document/11369949" target="_blank" class="pub-link-text">ST² (RA-M'26)</a>
        </div>
      </div>
      <div class="research-area-image">
        <img src="/assets/img/publication_preview/tcst_ac_24.gif" alt="Adaptive Critic Optimal Control">
      </div>
    </div>

  </div>
</div>
