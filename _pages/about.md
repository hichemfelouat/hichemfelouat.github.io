---
permalink: /
title: "About Me"
author_profile: true
---

<style>
/* ── Selectable text everywhere ── */
.page__content,
.page__content * {
  user-select: text !important;
  -webkit-user-select: text !important;
  -moz-user-select: text !important;
}

/* ── Animations ── */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(16px); }
  to   { opacity: 1; transform: translateY(0); }
}
@keyframes pulse {
  0%, 100% { box-shadow: 0 0 0 0 rgba(59,130,246,0.4); }
  50%       { box-shadow: 0 0 0 6px rgba(59,130,246,0); }
}

/* ══════════════════════════════════════
   BIO CARDS
══════════════════════════════════════ */
.bio-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.85em;
  margin: 1.4em 0 2em 0;
}
.bio-card {
  border: 1px solid rgba(128,128,128,0.2);
  border-radius: 12px;
  padding: 1.1em 1.25em;
  position: relative;
  overflow: hidden;
  opacity: 0;
  animation: fadeUp 0.5s ease forwards;
  transition: border-color 0.2s, transform 0.2s;
}
.bio-card:hover { border-color: rgba(128,128,128,0.5); transform: translateY(-2px); }
.bio-card:nth-child(1) { animation-delay: 0.05s; }
.bio-card:nth-child(2) { animation-delay: 0.15s; }
.bio-card:nth-child(3) { animation-delay: 0.25s; }
.bio-card:nth-child(4) { animation-delay: 0.35s; }
.bio-card::before {
  content: '';
  position: absolute;
  left: 0; top: 0; bottom: 0;
  width: 3px;
  border-radius: 12px 0 0 12px;
}
.bio-card.accent-blue::before   { background: #3b82f6; }
.bio-card.accent-teal::before   { background: #14b8a6; }
.bio-card.accent-indigo::before { background: #6366f1; }
.bio-card.accent-cyan::before   { background: #06b6d4; }
.bio-card-icon  { font-size: 1.4em; margin-bottom: 0.35em; display: block; line-height: 1; }
.bio-card-label { font-size: 0.7em; font-weight: 700; text-transform: uppercase; letter-spacing: 0.1em; opacity: 0.5; margin-bottom: 0.3em; }
.bio-card-text  { font-size: 0.9em; line-height: 1.55; opacity: 0.9; }

/* ══════════════════════════════════════
   RESEARCH INTERESTS — EXPANDABLE GRID
══════════════════════════════════════ */
.interest-section { margin: 0 0 2em 0; }
.interest-section > h2 {
  font-size: 0.75em; font-weight: 700; text-transform: uppercase;
  letter-spacing: 0.12em; opacity: 0.5; margin-bottom: 0.9em;
  padding: 0; border: none;
}

.interest-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
  gap: 8px;
}

.interest-card {
  border: 1px solid rgba(128,128,128,0.22);
  border-radius: 10px;
  padding: 0.7em 0.9em;
  cursor: pointer;
  opacity: 0;
  animation: fadeUp 0.4s ease forwards;
  animation-fill-mode: forwards;
  transition: border-color 0.18s, transform 0.18s;
  position: relative;
  overflow: hidden;
}
.interest-card:hover { border-color: rgba(128,128,128,0.55); transform: translateY(-2px); }
.interest-card.active {
  border-color: rgba(59,130,246,0.6);
  grid-column: 1 / -1;
}

.interest-card:nth-child(1) { animation-delay: 0.40s; }
.interest-card:nth-child(2) { animation-delay: 0.47s; }
.interest-card:nth-child(3) { animation-delay: 0.54s; }
.interest-card:nth-child(4) { animation-delay: 0.61s; }
.interest-card:nth-child(5) { animation-delay: 0.68s; }
.interest-card:nth-child(6) { animation-delay: 0.75s; }
.interest-card:nth-child(7) { animation-delay: 0.82s; }

.ic-header { display: flex; align-items: center; gap: 0.5em; }
.ic-emoji  { font-size: 1.1em; flex-shrink: 0; }
.ic-name   { font-size: 0.82em; font-weight: 600; line-height: 1.3; }

.ic-desc {
  display: none;
  font-size: 0.8em;
  line-height: 1.55;
  margin-top: 0.6em;
  padding-top: 0.6em;
  border-top: 1px solid rgba(128,128,128,0.18);
  opacity: 0.8;
}
.interest-card.active .ic-desc { display: block; }

.ic-toggle {
  position: absolute;
  top: 0.6em; right: 0.75em;
  font-size: 0.7em;
  opacity: 0.35;
  transition: transform 0.2s, opacity 0.2s;
  pointer-events: none;
}
.interest-card.active .ic-toggle { transform: rotate(180deg); opacity: 0.7; }

/* ══════════════════════════════════════
   NEWS — TIMELINE
══════════════════════════════════════ */
.news-section { margin: 0 0 1em 0; }
.news-section > h2 {
  font-size: 0.75em; font-weight: 700; text-transform: uppercase;
  letter-spacing: 0.12em; opacity: 0.5; margin-bottom: 0.9em;
  border: none; padding: 0;
}

.news-timeline {
  position: relative;
  padding-left: 1.6em;
}
.news-timeline::before {
  content: '';
  position: absolute;
  left: 6px; top: 10px; bottom: 0;
  width: 1px;
  background: rgba(128,128,128,0.2);
}

.news-entry {
  position: relative;
  margin-bottom: 1em;
  opacity: 0;
  animation: fadeUp 0.45s ease forwards;
}
.news-entry:nth-child(1) { animation-delay: 0.90s; }
.news-entry:nth-child(2) { animation-delay: 1.00s; }
.news-entry:nth-child(3) { animation-delay: 1.10s; }

.news-entry::before {
  content: '';
  position: absolute;
  left: -1.38em;
  top: 0.65em;
  width: 10px; height: 10px;
  border-radius: 50%;
  background: rgba(128,128,128,0.3);
  border: 2px solid rgba(128,128,128,0.4);
  transition: background 0.2s;
}
.news-entry.is-new::before {
  background: #3b82f6;
  border-color: #3b82f6;
  animation: pulse 1.8s ease infinite;
}

.news-bubble {
  border: 1px solid rgba(128,128,128,0.18);
  border-radius: 10px;
  padding: 0.7em 1em;
  transition: border-color 0.2s, transform 0.18s;
}
.news-bubble:hover { border-color: rgba(128,128,128,0.4); transform: translateX(3px); }

.news-meta {
  display: flex;
  align-items: center;
  gap: 0.6em;
  margin-bottom: 0.3em;
  flex-wrap: wrap;
}
.news-date-badge {
  font-size: 0.7em; font-weight: 700; letter-spacing: 0.04em;
  padding: 2px 8px; border-radius: 5px;
  border: 1px solid rgba(59,130,246,0.4);
  color: #3b82f6; white-space: nowrap;
}
.news-tag {
  font-size: 0.68em; font-weight: 600;
  padding: 2px 7px; border-radius: 5px;
  background: rgba(20,184,166,0.1);
  color: #14b8a6;
  border: 1px solid rgba(20,184,166,0.3);
}
.news-body { font-size: 0.87em; line-height: 1.5; opacity: 0.88; }

/* ── Responsive ── */
@media (max-width: 580px) {
  .bio-grid { grid-template-columns: 1fr; }
  .interest-grid { grid-template-columns: 1fr 1fr; }
}
</style>

<!-- ═══════════ BIO CARDS ═══════════ -->
<div class="bio-grid">

  <div class="bio-card accent-blue">
    <span class="bio-card-icon">🏛️</span>
    <div class="bio-card-label">Affiliation</div>
    <div class="bio-card-text">
      PhD Student at the <strong>Echizen Laboratory</strong>,
      <strong>National Institute of Informatics (NII)</strong> &amp;
      <strong>Graduate University for Advanced Studies, SOKENDAI</strong> - <i class="fas fa-location-dot"></i> Tokyo, Japan.
    </div>
  </div>

  <div class="bio-card accent-teal">
    <span class="bio-card-icon">🔬</span>
    <div class="bio-card-label">Research Focus</div>
    <div class="bio-card-text">
      Working at the intersection of <strong>3D computer vision</strong>,
      <strong>biometric security</strong>, and
      <strong>multimodal large vision-language models</strong>.
    </div>
  </div>

  <div class="bio-card accent-indigo">
    <span class="bio-card-icon">🛡️</span>
    <div class="bio-card-label">Core Problem</div>
    <div class="bio-card-text">
      Developing <strong>privacy-preserving 3D face recognition systems</strong>
      that stay robust against deepfake and reconstruction attacks.
    </div>
  </div>

  <div class="bio-card accent-cyan">
    <span class="bio-card-icon">🎯</span>
    <div class="bio-card-label">Mission</div>
    <div class="bio-card-text">
      Building secure, irreversible biometric templates that balance
      <strong>high recognition accuracy</strong> with
      <strong>strong privacy guarantees</strong>.
    </div>
  </div>

</div>

<!-- ═══════════ RESEARCH INTERESTS ═══════════ -->
<div class="interest-section">
<h2>Research Interests</h2>
<div class="interest-grid">

  <div class="interest-card" onclick="toggleInterest(this)">
    <span class="ic-toggle">▼</span>
    <div class="ic-header"><span class="ic-emoji">🧊</span><span class="ic-name">3D Computer Vision</span></div>
    <div class="ic-desc">Analyzing and reconstructing 3D scenes from images or sensors — including 3D face meshes, point clouds, and depth estimation for secure biometric applications.</div>
  </div>

  <div class="interest-card" onclick="toggleInterest(this)">
    <span class="ic-toggle">▼</span>
    <div class="ic-header"><span class="ic-emoji">🔐</span><span class="ic-name">Biometric Security &amp; Authentication</span></div>
    <div class="ic-desc">Designing robust systems that verify identity using physiological traits while defending against spoofing, replay, and presentation attacks.</div>
  </div>

  <div class="interest-card" onclick="toggleInterest(this)">
    <span class="ic-toggle">▼</span>
    <div class="ic-header"><span class="ic-emoji">🤖</span><span class="ic-name">Multimodal Vision-Language Models</span></div>
    <div class="ic-desc">Combining visual and textual understanding in large foundation models (LVLMs) to enable richer, context-aware reasoning about images, faces, and 3D content.</div>
  </div>

  <div class="interest-card" onclick="toggleInterest(this)">
    <span class="ic-toggle">▼</span>
    <div class="ic-header"><span class="ic-emoji">🛡️</span><span class="ic-name">Privacy-Preserving Machine Learning</span></div>
    <div class="ic-desc">Building ML pipelines that protect sensitive data through cancelable biometrics, secure template transformation, and differential privacy techniques.</div>
  </div>

  <div class="interest-card" onclick="toggleInterest(this)">
    <span class="ic-toggle">▼</span>
    <div class="ic-header"><span class="ic-emoji">🎭</span><span class="ic-name">Deepfake Detection &amp; Generation</span></div>
    <div class="ic-desc">Studying how synthetic faces are created (GANs, diffusion, 3D morphing) and developing detection models that expose manipulation artifacts in 2D and 3D.</div>
  </div>

  <div class="interest-card" onclick="toggleInterest(this)">
    <span class="ic-toggle">▼</span>
    <div class="ic-header"><span class="ic-emoji">🌐</span><span class="ic-name">Federated Learning</span></div>
    <div class="ic-desc">Training models collaboratively across decentralized devices without sharing raw data — critical for privacy-preserving biometric systems across institutions.</div>
  </div>

  <div class="interest-card" onclick="toggleInterest(this)">
    <span class="ic-toggle">▼</span>
    <div class="ic-header"><span class="ic-emoji">👤</span><span class="ic-name">3D Face Recognition</span></div>
    <div class="ic-desc">Recognizing individuals from 3D facial geometry (meshes, point clouds) rather than 2D images, achieving stronger liveness and anti-spoofing guarantees.</div>
  </div>

</div>
</div>

<!-- ═══════════ NEWS TIMELINE ═══════════ -->
<div class="news-section">
<h2>News</h2>
<div class="news-timeline">

  <div class="news-entry is-new">
    <div class="news-bubble">
      <div class="news-meta">
        <span class="news-date-badge">2025.11</span>
        <span class="news-tag">📄 Publication</span>
      </div>
      <div class="news-body">
        1st-authored paper accepted at <strong>WACV 2026</strong> —
        <em>GFT-GCN: Privacy-Preserving 3D Face Mesh Recognition with Spectral Diffusion</em>. 🎉
      </div>
    </div>
  </div>

</div>
</div>

<script>
function toggleInterest(card) {
  var wasActive = card.classList.contains('active');
  document.querySelectorAll('.interest-card').forEach(function(c) {
    c.classList.remove('active');
  });
  if (!wasActive) card.classList.add('active');
}
</script>
