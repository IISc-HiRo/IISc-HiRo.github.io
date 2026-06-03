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
          learning and imitation learning. Our work on
          <a href="/publications/#imphrl" class="work-link">Impedance Primitive-Augmented Hierarchical RL (ICRA'25)</a>
          augments high-level RL policies with impedance control primitives to solve long-horizon sequential tasks,
          enabling compliant and adaptive skill acquisition. We also investigate robust imitation learning that
          exploits mixed-quality demonstrations to improve generalization from imperfect human teachers, as in
          <a href="/publications/#beyond-the-teacher-icra26" class="work-link">Beyond the Teacher (ICRA'26)</a>.
        </p>
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
          robot-human interaction. Our work on
          <a href="/publications/#ovita" class="work-link">OVITA (RA-L'25)</a>
          uses vision-language models to adapt robot trajectories in real time based on open-vocabulary human
          language instructions, providing interpretable trajectory modifications without retraining.
        </p>
      </div>
      <div class="research-area-image">
        <img src="/assets/img/publication_preview/ovita_25.gif" alt="OVITA Trajectory Adaptation">
      </div>
    </div>

    <div class="research-area">
      <div class="research-area-content">
        <h2>Safe and Compliant Human-Robot Interaction</h2>
        <p>
          Safety and compliance are essential when robots work alongside humans. Our work on
          <a href="/publications/#safedmps-icra26" class="work-link">SafeDMPs (ICRA'26)</a>
          integrates Signal Temporal Logic (STL)-based formal safety specifications directly into Dynamic
          Movement Primitives, enabling adaptive robot motions that are provably safe during physical human-robot
          contact. We also develop
          <a href="/publications/#variable-impedance-icra26" class="work-link">certified reinforcement learning for variable impedance control (ICRA'26)</a>,
          which combines Lyapunov-based stability certificates with RL to achieve optimal, safe impedance modulation
          during interaction. More recently, we study how safety can be learned directly from offline data:
          <a href="/publications/#safe-flow-q-learning" class="work-link">Safe Flow Q-Learning (RLC'26)</a>
          couples reachability analysis with flow-based policies for offline safe reinforcement learning, while
          <a href="/publications/#v-ocbf" class="work-link">V-OCBF (TMLR'26)</a>
          learns value-guided control barrier functions as safety filters from offline datasets.
        </p>
      </div>
      <div class="research-area-image">
        <img src="/assets/img/publication_preview/safedmps_26.png" alt="Safe DMPs for HRI">
      </div>
    </div>

    <div class="research-area">
      <div class="research-area-content">
        <h2>Optimization and Optimal Control</h2>
        <p>
          We develop optimization-based and data-driven approaches for robot motion planning and control.
          Our <a href="/publications/#adaptive-critic" class="work-link">Adaptive Critic (T-CST'24)</a>
          framework learns optimal controllers for uncertain robot manipulators using neural network-based value
          function approximation, achieving data-efficient online adaptation without explicit system identification.
          Our work on
          <a href="/publications/#transportation-maps" class="work-link">generalizable motion policies through keypoint parameterization and transportation maps (T-RO'25)</a>
          enables one-shot generalization of manipulation skills to novel object configurations. We also develop
          <a href="/publications/#st2" class="work-link">ST² (RA-M'26)</a>, a framework for teaching robots
          long-horizon manipulation skills through sequential human demonstrations.
        </p>
      </div>
      <div class="research-area-image">
        <img src="/assets/img/publication_preview/tcst_ac_24.gif" alt="Adaptive Critic Optimal Control">
      </div>
    </div>

    <div class="research-area">
      <div class="research-area-content">
        <h2>3D Vision, SLAM and World Models</h2>
        <p>
          We develop methods for robots to build accurate 3D models of their environment through active perception,
          including SLAM (Simultaneous Localization and Mapping), real-time scene reconstruction, world models for
          spatial understanding, and object-level mapping integrated with manipulation planning. Our work on
          <a href="/publications/#affordmatcher" class="work-link">AffordMatcher (CVPR'26)</a>
          learns object affordances in 3D scenes from visual signifiers, connecting 3D scene understanding to
          manipulation in complex, unstructured spaces.
        </p>
      </div>
      <div class="research-area-image">
        <img src="/assets/img/publication_preview/affordmatcher_cvpr_26.png" alt="AffordMatcher: Affordance Learning in 3D Scenes">
      </div>
    </div>

  </div>
</div>

<!-- Image Modal -->
<div id="imageModal" style="display:none; position:fixed; z-index:1000; left:0; top:0; width:100%; height:100%; background-color:rgba(0,0,0,0.9); cursor:pointer;">
  <span style="position:absolute; top:20px; right:40px; color:#fff; font-size:40px; font-weight:bold; cursor:pointer;">&times;</span>
  <img id="modalImage" style="display:block; width:92vw; height:90vh; object-fit:contain; position:absolute; top:50%; left:50%; transform:translate(-50%, -50%);">
</div>

<script>
  document.addEventListener('DOMContentLoaded', function () {
    const modal = document.getElementById('imageModal');
    const modalImg = document.getElementById('modalImage');
    const images = document.querySelectorAll('.research-area-image img, .research-header-image img');

    images.forEach(img => {
      img.style.cursor = 'pointer';
      img.addEventListener('click', function () {
        modal.style.display = 'block';
        modalImg.src = this.src;
      });
    });

    modal.addEventListener('click', function () {
      modal.style.display = 'none';
    });

    document.addEventListener('keydown', function (e) {
      if (e.key === 'Escape' && modal.style.display === 'block') {
        modal.style.display = 'none';
      }
    });
  });
</script>
