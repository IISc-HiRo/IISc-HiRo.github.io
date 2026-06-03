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
      Our mission is to build the theoretical foundations and practical algorithms that let robots learn from,
      adapt to, and collaborate with people in unstructured, real-world environments. We draw on machine learning,
      optimal control, and formal methods to make robotic systems data-efficient, generalizable, and provably safe
      during physical human-robot interaction. The themes below summarize our current directions and representative
      results.
    </p>
  </div>

  <div class="research-areas">
    <div class="research-area">
      <div class="research-area-content">
        <h2>Interactive Reinforcement Learning</h2>
        <p>
          Reinforcement learning (RL) and learning from demonstration let robots acquire manipulation skills directly
          from interaction and human guidance. The hard cases are long-horizon, contact-rich tasks and learning
          robustly from limited, imperfect human data. We address the first with
          <a href="/publications/#imphrl" class="work-link">Impedance Primitive-Augmented Hierarchical RL (ICRA'25)</a>,
          which gives a high-level RL policy a low-level action space of parameterized impedance-control primitives,
          yielding compliant, contact-rich skills over extended task sequences. For the second, we make imitation
          robust to the quality of the teacher:
          <a href="/publications/#beyond-the-teacher-icra26" class="work-link">Beyond the Teacher (ICRA'26)</a>
          leverages mixed-skill demonstrations to learn policies that tolerate inconsistent human teachers,
          <a href="/publications/#rise" class="work-link">RISE (IROSW'25)</a> uses stochastic latent encodings for
          robust imitation, and <a href="/publications/#pacer" class="work-link">PACER (CoRLW'25)</a> curates
          demonstrations by task progress to curb the compounding errors that destabilize behavior cloning.
        </p>
      </div>
      <div class="research-area-image">
        <img src="/assets/img/publication_preview/icra_imphrl_25.gif" alt="Impedance Hierarchical RL">
      </div>
    </div>

    <div class="research-area">
      <div class="research-area-content">
        <h2>Foundation Models for Robotics</h2>
        <p>
          Foundation models, including large vision-language models (VLMs) and, increasingly, vision-language-action
          (VLA) models pretrained on web- and robot-scale data, supply semantic priors and broad generalization that
          can ground robot behavior in natural language and perception. We study how to turn these priors into
          natural, flexible human-robot interaction. Our work on
          <a href="/publications/#ovita" class="work-link">OVITA (RA-L'25)</a>
          harnesses pretrained foundation models to adapt reference trajectories from open-vocabulary language
          instructions at execution time, producing interpretable, parameterized edits to robot motion without any
          task-specific retraining.
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
          When robots make physical contact with people, behavior must be both compliant and provably safe, with
          guarantees that hold during interaction and not just on average. We bring formal methods and
          control-theoretic certificates together with learning to enforce this.
          <a href="/publications/#safedmps-icra26" class="work-link">SafeDMPs (ICRA'26)</a>
          embeds Signal Temporal Logic (STL) safety specifications directly into Dynamic Movement Primitives, so
          that adaptive motions remain provably safe during physical human-robot contact, while
          <a href="/publications/#variable-impedance-icra26" class="work-link">certified RL for variable impedance control (ICRA'26)</a>
          pairs RL with Lyapunov-based stability certificates to modulate impedance optimally with guaranteed
          stability. We also learn safety directly from offline data, without online interaction:
          <a href="/publications/#safe-flow-q-learning" class="work-link">Safe Flow Q-Learning (RLC'26)</a>
          couples reachability analysis with flow-based policies for offline safe RL, and
          <a href="/publications/#v-ocbf" class="work-link">V-OCBF (TMLR'26)</a>
          learns value-guided control barrier functions that act as safety filters.
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
          Optimization and optimal control offer principled, data-efficient ways to synthesize controllers and motion
          policies, often with stability or generalization guarantees. Our
          <a href="/publications/#adaptive-critic" class="work-link">Adaptive Critic (T-CST'24)</a>
          framework uses approximate dynamic programming with neural value-function approximation to learn
          near-optimal controllers for uncertain manipulators online, without explicit system identification.
          <a href="/publications/#transportation-maps" class="work-link">Keypoint parameterization with transportation (optimal-transport) maps (T-RO'25)</a>
          yields motion policies that generalize one-shot to novel object configurations, and
          <a href="/publications/#st2" class="work-link">ST² (RA-M'26)</a>
          teaches robots long-horizon manipulation by composing skills from sequential human demonstrations.
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
          Acting in unstructured environments demands spatial understanding from 3D reconstruction, simultaneous
          localization and mapping (SLAM), and world models that capture both geometry and semantics. We are building
          active-perception pipelines that tie real-time scene reconstruction and object-level mapping to
          manipulation planning. A first step in this direction,
          <a href="/publications/#affordmatcher" class="work-link">AffordMatcher (CVPR'26)</a>,
          learns object affordances in 3D scenes from visual signifiers, connecting 3D scene understanding to where
          and how a robot should act in complex, cluttered spaces.
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
