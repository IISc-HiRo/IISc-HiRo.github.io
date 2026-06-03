---
layout: main
title: Home
permalink: /
---

<div class="hero-section">
  <div class="hero-text">
    <h1>Human-interactive Robotics Lab</h1>
    
    <p>
      The Human-interactive Robotics (HiRo) Lab is a research group in the <a href='https://cps.iisc.ac.in'>Department of Cyber-Physical Systems</a> at the <a href='https://iisc.ac.in'>Indian Institute of Science Bangalore</a> set up and led by <a href='/people/drraviprakash/'>Prof. Ravi Prakash</a>.
    </p>
    
    <p>
      The group's research interests lie at the intersection of robotics, machine learning, and human-robot interaction, with a focus on robot manipulation for real-world applications, including healthcare, retail, and space robots. The central principle is to enable humans with varying levels of robotic expertise to transfer their knowledge and experience of skills and tasks to the robot, enabling it to explore and execute tasks in unstructured, novel scenarios.
    </p>
    
    <div class="hero-links">
      <a href="https://www.linkedin.com/company/hiro-iisc/">LinkedIn</a>
      <a href="https://github.com/IISc-HiRo">Github</a>
      <a href="https://www.youtube.com/@HiRo-IISc">YouTube</a>
      <a href="https://hiro.cps.iisc.ac.in/contact/">Open Position</a>
    </div>
  </div>
  
  <div class="hero-media">
    <img src="/assets/img/logos/hiro_lab.jpg" alt="HiRo Lab">
  </div>
</div>

<div class="funding-section">
  <h2>Funding & Support</h2>
  <div class="funding-carousel">
    <div class="carousel-container">
      <div class="carousel-track">
        <div class="funding-logo">
          <img src="/assets/img/logos/drdo.png" alt="DRDO">
        </div>
        <div class="funding-logo">
          <img src="/assets/img/logos/isro.svg" alt="ISRO">
        </div>
        <div class="funding-logo">
          <img src="/assets/img/logos/artpark.png" alt="ARTPARK">
        </div>
        <div class="funding-logo">
          <img src="/assets/img/logos/kiac.png" alt="KIAC">
        </div>
        <div class="funding-logo">
          <img src="/assets/img/logos/iisc.jpg" alt="IISc">
        </div>
        <div class="funding-logo">
          <img src="/assets/img/logos/govtofkarnataka.png" alt="Government of Karnataka">
        </div>
        <div class="funding-logo">
          <img src="/assets/img/logos/dst.jpg" alt="DST">
        </div>
        <!-- Duplicate for seamless loop -->
        <div class="funding-logo">
          <img src="/assets/img/logos/drdo.png" alt="DRDO">
        </div>
        <div class="funding-logo">
          <img src="/assets/img/logos/isro.svg" alt="ISRO">
        </div>
        <div class="funding-logo">
          <img src="/assets/img/logos/artpark.png" alt="ARTPARK">
        </div>
        <div class="funding-logo">
          <img src="/assets/img/logos/kiac.png" alt="KIAC">
        </div>
        <div class="funding-logo">
          <img src="/assets/img/logos/iisc.jpg" alt="IISc">
        </div>
        <div class="funding-logo">
          <img src="/assets/img/logos/govtofkarnataka.png" alt="Government of Karnataka">
        </div>
        <div class="funding-logo">
          <img src="/assets/img/logos/dst.jpg" alt="DST">
        </div>
      </div>
    </div>
  </div>
</div>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    const track = document.querySelector('.carousel-track');
    const logos = document.querySelectorAll('.funding-logo');
    const totalLogos = logos.length / 2; // Original count before duplication
    let position = 0;
    
    function animate() {
      position -= 0.5; // Scroll speed
      
      // Reset position when halfway through (when original logos are fully scrolled)
      if (Math.abs(position) >= (totalLogos * 200)) {
        position = 0;
      }
      
      track.style.transform = `translateX(${position}px)`;
      requestAnimationFrame(animate);
    }
    
    animate();
  });
</script>
