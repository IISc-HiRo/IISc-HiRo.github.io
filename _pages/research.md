---
layout: main
title: Research
permalink: /research/
---

<div class="research-section">
  <h1>Research</h1>

  <style>
    #researchCarousel .carousel-caption {
      background: rgba(0, 0, 0, 0.55);
      border-radius: 6px;
      padding: 0.4rem 0.75rem;
      left: 10%;
      right: 10%;
      bottom: 1rem;
    }
    #researchCarousel .carousel-caption a.work-link {
      color: #fff;
      font-weight: 600;
      text-decoration: none;
    }
    #researchCarousel .carousel-caption a.work-link:hover {
      text-decoration: underline;
    }
  </style>

  <!-- Research Videos Carousel -->
  <div class="research-video-carousel" style="max-width: 960px; margin: 1.5rem auto 2.5rem;">
    <div id="researchCarousel" class="carousel slide" data-bs-ride="carousel" data-bs-interval="7000" data-bs-pause="hover">
      <div class="carousel-indicators">
        <button type="button" data-bs-target="#researchCarousel" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Gripper-aware VLA"></button>
        <button type="button" data-bs-target="#researchCarousel" data-bs-slide-to="1" aria-label="Beyond Visual Grasping"></button>
        <button type="button" data-bs-target="#researchCarousel" data-bs-slide-to="2" aria-label="Beyond the Teacher"></button>
        <button type="button" data-bs-target="#researchCarousel" data-bs-slide-to="3" aria-label="Certified RL for Variable Impedance"></button>
        <button type="button" data-bs-target="#researchCarousel" data-bs-slide-to="4" aria-label="SafeDMPs"></button>
      </div>
      <div class="carousel-inner" style="background:#000; border-radius:8px;">
        <div class="carousel-item active">
          <video class="d-block w-100" style="height:480px; object-fit:contain; background:#000;" muted loop playsinline preload="none">
            <source src="/assets/videos/eccv_2026_5218.mp4" type="video/mp4">
          </video>
          <div class="carousel-caption">
            <a href="/publications/#gripper-aware-vla" class="work-link">Gripper-aware Vision Language Action Models (ECCV'26)</a>
          </div>
        </div>
        <div class="carousel-item">
          <video class="d-block w-100" style="height:480px; object-fit:contain; background:#000;" muted loop playsinline preload="none">
            <source src="/assets/videos/iros_2026.mp4" type="video/mp4">
          </video>
          <div class="carousel-caption">
            <a href="/publications/#beyond-visual-grasping" class="work-link">Beyond Visual Grasping: Complex Grasping from Detection to Execution (IROS'26)</a>
          </div>
        </div>
        <div class="carousel-item">
          <video class="d-block w-100" style="height:480px; object-fit:contain; background:#000;" muted loop playsinline preload="none">
            <source src="/assets/videos/icra_2026_beyond_the_teacher.mp4" type="video/mp4">
          </video>
          <div class="carousel-caption">
            <a href="/publications/#beyond-the-teacher-icra26" class="work-link">Beyond the Teacher: Mixed-Skill Demonstrations for Robust Imitation (ICRA'26)</a>
          </div>
        </div>
        <div class="carousel-item">
          <video class="d-block w-100" style="height:480px; object-fit:contain; background:#000;" muted loop playsinline preload="none">
            <source src="/assets/videos/icra_2026_certified_rl.mp4" type="video/mp4">
          </video>
          <div class="carousel-caption">
            <a href="/publications/#variable-impedance-icra26" class="work-link">Certified RL for Variable Impedance Control (ICRA'26)</a>
          </div>
        </div>
        <div class="carousel-item">
          <video class="d-block w-100" style="height:480px; object-fit:contain; background:#000;" muted loop playsinline preload="none">
            <source src="/assets/videos/icra_2026_safedmps.mp4" type="video/mp4">
          </video>
          <div class="carousel-caption">
            <a href="/publications/#safedmps-icra26" class="work-link">SafeDMPs: Formal Safety with DMPs for Adaptive HRI (ICRA'26)</a>
          </div>
        </div>
      </div>
      <button class="carousel-control-prev" type="button" data-bs-target="#researchCarousel" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#researchCarousel" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
    <p style="text-align:center; font-size:0.85rem; color:#666; margin-top:0.5rem;">
      Videos play continuously; hover to pause the carousel, or use the arrows to browse.
    </p>
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
          task-specific retraining. Building on VLA models directly,
          <a href="/publications/#gripper-aware-vla" class="work-link">Gripper-aware Vision Language Action Models (ECCV'26)</a>
          make the policy aware of the robot's end-effector, improving grasping and manipulation across
          diverse gripper embodiments.
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
          and how a robot should act in complex, cluttered spaces. Complementing this,
          <a href="/publications/#beyond-visual-grasping" class="work-link">Beyond Visual Grasping (IROS'26)</a>
          benchmarks the full pipeline of complex grasping from detection to execution, exposing where perception-to-action
          systems break down on challenging, real-world grasps.
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
    // Only play the video on the currently visible carousel slide (saves bandwidth)
    const carousel = document.getElementById('researchCarousel');
    if (carousel) {
      const playActive = function () {
        carousel.querySelectorAll('.carousel-item').forEach(function (item) {
          const video = item.querySelector('video');
          if (!video) return;
          if (item.classList.contains('active')) {
            video.play().catch(function () {});
          } else {
            video.pause();
          }
        });
      };
      // Play the first slide once, and switch playback whenever the slide changes
      playActive();
      carousel.addEventListener('slid.bs.carousel', playActive);
    }

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
