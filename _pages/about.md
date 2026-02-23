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

/* ── Fade-in animation ── */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(16px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* ── Bio split cards ── */
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
  /* No background — inherits from theme, works in dark & light */
}

.bio-card:hover {
  border-color: rgba(128,128,128,0.5);
  transform: translateY(-2px);
}

/* Staggered animation delays */
.bio-card:nth-child(1) { animation-delay: 0.05s; }
.bio-card:nth-child(2) { animation-delay: 0.15s; }
.bio-card:nth-child(3) { animation-delay: 0.25s; }
.bio-card:nth-child(4) { animation-delay: 0.35s; }

/* Accent left bar — uses a semi-transparent teal that works on any background */
.bio-card::before {
  content: '';
  position: absolute;
  left: 0; top: 0; bottom: 0;
  width: 3px;
  border-radius: 12px 0 0 12px;
  background: currentColor;
  opacity: 0.25;
}
.bio-card.accent-blue::before  { color: #3b82f6; opacity: 1; }
.bio-card.accent-teal::before  { color: #14b8a6; opacity: 1; }
.bio-card.accent-indigo::before { color: #6366f1; opacity: 1; }
.bio-card.accent-cyan::before  { color: #06b6d4; opacity: 1; }

.bio-card-icon {
  font-size: 1.4em;
  margin-bottom: 0.35em;
  display: block;
  line-height: 1;
}

.bio-card-label {
  font-size: 0.7em;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  opacity: 0.5;
  margin-bottom: 0.3em;
}

.bio-card-text {
  font-size: 0.9em;
  line-height: 1.55;
  opacity: 0.9;
}

.bio-card-text strong {
  opacity: 1;
}

/* ── Research interest tags ── */
.interest-section { margin: 0 0 2em 0; }

.interest-section h2 {
  font-size: 0.75em;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  opacity: 0.5;
  margin-bottom: 0.8em;
  padding-bottom: 0;
  border: none;
}

.interest-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 7px;
}

.interest-tag {
  border: 1px solid rgba(128,128,128,0.25);
  border-radius: 99px;
  padding: 4px 13px;
  font-size: 0.8em;
  font-weight: 500;
  opacity: 0;
  animation: fadeUp 0.4s ease forwards;
  transition: border-color 0.18s, opacity 0.18s;
  cursor: default;
}

.interest-tag:hover {
  border-color: rgba(128,128,128,0.6);
  opacity: 1 !important;
}

/* Stagger tags */
.interest-tag:nth-child(1) { animation-delay: 0.4s; }
.interest-tag:nth-child(2) { animation-delay: 0.47s; }
.interest-tag:nth-child(3) { animation-delay: 0.54s; }
.interest-tag:nth-child(4) { animation-delay: 0.61s; }
.interest-tag:nth-child(5) { animation-delay: 0.68s; }
.interest-tag:nth-child(6) { animation-delay: 0.75s; }
.interest-tag:nth-child(7) { animation-delay: 0.82s; }

/* Final opacity after animation */
.interest-tag { animation-fill-mode: forwards; }

/* ── News section ── */
.news-section { margin: 0 0 1em 0; }

.news-section h2 {
  font-size: 0.75em;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  opacity: 0.5;
  margin-bottom: 0.8em;
  border: none;
  padding: 0;
}

.news-item {
  display: flex;
  align-items: flex-start;
  gap: 0.75em;
  padding: 0.75em 1em;
  border-radius: 10px;
  border: 1px solid rgba(128,128,128,0.18);
  margin-bottom: 0.6em;
  opacity: 0;
  animation: fadeUp 0.45s ease 0.9s forwards;
  transition: border-color 0.2s;
}

.news-item:hover { border-color: rgba(128,128,128,0.4); }

.news-date {
  font-size: 0.72em;
  font-weight: 700;
  letter-spacing: 0.04em;
  white-space: nowrap;
  padding: 3px 9px;
  border-radius: 6px;
  border: 1px solid rgba(59,130,246,0.4);
  color: #3b82f6;
  margin-top: 1px;
  flex-shrink: 0;
}

.news-text {
  font-size: 0.88em;
  line-height: 1.5;
  opacity: 0.88;
}

/* ── Responsive ── */
@media (max-width: 580px) {
  .bio-grid { grid-template-columns: 1fr; }
}
</style>

<div class="bio-grid">

  <div class="bio-card accent-blue">
    <span class="bio-card-icon">🏛️</span>
    <div class="bio-card-label">Affiliation</div>
    <div class="bio-card-text">
      PhD Student at the <strong>Echizen Laboratory</strong>,
      <strong>National Institute of Informatics (NII)</strong> &amp;
      <strong>SOKENDAI</strong> — Tokyo, Japan.
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

<div class="interest-section">
<h2>Research Interests</h2>
<div class="interest-tags">
  <span class="interest-tag">3D Computer Vision</span>
  <span class="interest-tag">Biometric Security &amp; Authentication</span>
  <span class="interest-tag">Multimodal Vision-Language Models</span>
  <span class="interest-tag">Privacy-Preserving Machine Learning</span>
  <span class="interest-tag">Deepfake Detection &amp; Generation</span>
  <span class="interest-tag">Federated Learning</span>
  <span class="interest-tag">3D Face Recognition</span>
</div>
</div>

<div class="news-section">
<h2>News</h2>
<div class="news-item">
  <span class="news-date">2025.11</span>
  <span class="news-text">One 1st-authored paper accepted at <strong>WACV 2026</strong>. 🎉</span>
</div>
</div>
