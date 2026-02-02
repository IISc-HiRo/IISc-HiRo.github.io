---
layout: main
title: Publications
permalink: /publications/
---

<div class="research-section">
  <h1>Publications</h1>

  <div class="filter-buttons">
    <button class="filter-btn active" data-filter="all">All</button>
    <button class="filter-btn" data-filter="conference">Conference</button>
    <button class="filter-btn" data-filter="journal">Journal</button>
    <button class="filter-btn" data-filter="workshop">Workshop</button>
    <button class="filter-btn" data-filter="other">Other</button>
  </div>

  <div class="publications-list">
    <!-- 2025 Publications -->
    <h2 class="year-header">2025</h2>

    <div class="publication-item" data-category="workshop">
      <div class="pub-content">
        <div class="pub-title">SEAL: Safe and Efficient Abstraction Learning for Robotic Planning</div>
        <div class="pub-authors">Akhil R Kurup and Ravi Prakash</div>
        <div class="pub-venue">CoRL 2025 LEAP Workshop</div>
      </div>
    </div>

    <div class="publication-item" data-category="workshop">
      <div class="pub-content">
        <div class="pub-title">SafeDMPs: Integrating Formal Safety with DMPs for Adaptive HRI</div>
        <div class="pub-authors">Pranav Tiwari, Soumyadipta Nath, and Ravi Prakash</div>
        <div class="pub-venue">CoRL 2025 SAFEROL Workshop</div>
      </div>
    </div>

    <div class="publication-item" data-category="workshop">
      <div class="pub-content">
        <div class="pub-title">PACER: Progress-Aligned Curation for Error-Resilient Imitation Learning</div>
        <div class="pub-authors">Shreyas Kumar and Ravi Prakash</div>
        <div class="pub-venue">CoRL 2025 Making Sense of Data in Robotics Workshop</div>
      </div>
    </div>

    <div class="publication-item" data-category="workshop">
      <div class="pub-content">
        <div class="pub-title">Beyond the Teacher: Leveraging Mixed-Skill Demonstrations for Robust Imitation Learning</div>
        <div class="pub-authors">Saharsh, Shubham Sonkar, Pushpak Jagtap, and Ravi Prakash</div>
        <div class="pub-venue">CoRL 2025 Making Sense of Data in Robotics Workshop</div>
      </div>
    </div>

    <div class="publication-item" data-category="journal">
      <div class="pub-content">
        <div class="pub-title">OVITA: Open Vocabulary Interpretable Trajectory Adaptations</div>
        <div class="pub-authors">Anurag Maurya, Tashmoy Ghosh, Anh Nguyen, and Ravi Prakash</div>
        <div class="pub-venue">IEEE Robotics and Automation Letters, 2025</div>
        <div class="pub-links">
          <a href="https://arxiv.org/abs/2508.17260">arXiv</a>
          <a href="https://anurag1000101.github.io/projects/IISC/">Website</a>
          <a href="https://github.com/anurag1000101/OVITA">Code</a>
        </div>
      </div>
    </div>

    <div class="publication-item" data-category="conference">
      <div class="pub-content">
        <div class="pub-title">Impedance Primitive-augmented Hierarchical Reinforcement Learning for Sequential Tasks</div>
        <div class="pub-authors">Amin Berjaoui Tahmaz, Ravi Prakash, and Jens Kober</div>
        <div class="pub-venue">IEEE International Conference on Robotics and Automation (ICRA), 2025</div>
      </div>
    </div>

    <div class="publication-item" data-category="workshop">
      <div class="pub-content">
        <div class="pub-title">Stability-Aware PI2 for Safe Interaction via Variable Impedance Control</div>
        <div class="pub-authors">Karthik Swaminathan and Ravi Prakash</div>
        <div class="pub-venue">ICRA 2025 SRL Workshop</div>
      </div>
    </div>

    <div class="publication-item" data-category="journal">
      <div class="pub-content">
        <div class="pub-title">Adaptive Critic Optimal Control of an Uncertain Robot Manipulator With Applications</div>
        <div class="pub-authors">Ravi Prakash, Laxmidhar Behera, and Sarangapani Jagannathan</div>
        <div class="pub-venue">IEEE Transactions on Control Systems Technology, Vol. 33, No. 1, pp. 316-326, 2025</div>
      </div>
    </div>

    <div class="publication-item" data-category="journal">
      <div class="pub-content">
        <div class="pub-title">Generalizable Motion Policies Through Keypoint Parameterization and Transportation Maps</div>
        <div class="pub-authors">Giovanni Franzese, Ravi Prakash, Cosimo Della Santina, and Jens Kober</div>
        <div class="pub-venue">IEEE Transactions on Robotics, Vol. 41, pp. 4557-4573, 2025</div>
      </div>
    </div>

    <!-- 2024 Publications -->
    <h2 class="year-header">2024</h2>

    <div class="publication-item" data-category="workshop">
      <div class="pub-content">
        <div class="pub-title">Trajectory Adaptation using Large Language Models</div>
        <div class="pub-authors">Anurag Maurya, Tashmoy Ghosh, and Ravi Prakash</div>
        <div class="pub-venue">CoRL 2024 LangRob Workshop</div>
      </div>
    </div>

  </div>
</div>

<script>
  // Publication filtering functionality
  document.addEventListener('DOMContentLoaded', function() {
    const filterButtons = document.querySelectorAll('.filter-btn');
    const publications = document.querySelectorAll('.publication-item');

    filterButtons.forEach(button => {
      button.addEventListener('click', function() {
        // Update active button
        filterButtons.forEach(btn => btn.classList.remove('active'));
        this.classList.add('active');

        const filterValue = this.getAttribute('data-filter');

        // Filter publications
        publications.forEach(pub => {
          if (filterValue === 'all') {
            pub.style.display = 'block';
          } else {
            const category = pub.getAttribute('data-category');
            pub.style.display = category === filterValue ? 'block' : 'none';
          }
        });
      });
    });
  });
</script>
