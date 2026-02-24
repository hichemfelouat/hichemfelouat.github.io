---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<style>
/* ── Selectable text ── */
.page__content, .page__content * {
  user-select: text !important;
  -webkit-user-select: text !important;
}

/* ── Animations ── */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(14px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* ── Filter bar ── */
.pub-filters {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 1.8em;
}
.pub-filter-btn {
  border: 1px solid rgba(128,128,128,0.3);
  background: transparent;
  border-radius: 20px;
  padding: 4px 14px;
  font-size: 0.82em;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.18s;
  color: inherit;
}
.pub-filter-btn:hover {
  border-color: #0ea5e9;
  color: #0ea5e9;
}
.pub-filter-btn.active {
  background: #0ea5e9;
  border-color: #0ea5e9;
  color: #fff;
}

/* ── Stats row ── */
.pub-stats {
  display: flex;
  gap: 1.2em;
  margin-bottom: 1.8em;
  flex-wrap: wrap;
}
.pub-stat {
  border: 1px solid rgba(128,128,128,0.2);
  border-left: 3px solid #0ea5e9;
  border-radius: 0 8px 8px 0;
  padding: 0.45em 1em;
  font-size: 0.82em;
}
.pub-stat strong { font-size: 1.3em; display: block; color: #0ea5e9; }
.pub-stat span   { opacity: 0.6; font-size: 0.9em; }

/* ── Paper card ── */
.pub-card {
  border: 1px solid rgba(128,128,128,0.2);
  border-left: 3px solid #0ea5e9;
  border-radius: 0 10px 10px 0;
  padding: 1.1em 1.3em;
  margin-bottom: 1em;
  transition: box-shadow 0.18s, border-color 0.2s;
  opacity: 0;
  animation: fadeUp 0.45s ease forwards;
}
.pub-card:hover {
  box-shadow: 0 3px 14px rgba(0,0,0,0.1);
  border-left-color: #38bdf8;
}
.pub-card:nth-child(1) { animation-delay: 0.05s; }
.pub-card:nth-child(2) { animation-delay: 0.13s; }
.pub-card:nth-child(3) { animation-delay: 0.21s; }
.pub-card:nth-child(4) { animation-delay: 0.29s; }
.pub-card:nth-child(5) { animation-delay: 0.37s; }

/* hidden by filter */
.pub-card.hidden { display: none; }

/* ── Card top row ── */
.pub-card-meta {
  display: flex;
  align-items: center;
  gap: 0.6em;
  flex-wrap: wrap;
  margin-bottom: 0.5em;
}
.pub-type {
  font-size: 0.68em;
  font-weight: 700;
  padding: 2px 9px;
  border-radius: 5px;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
.pub-type.conference {
  background: rgba(99,102,241,0.12);
  border: 1px solid rgba(99,102,241,0.35);
  color: #818cf8;
}
.pub-type.journal {
  background: rgba(20,184,166,0.1);
  border: 1px solid rgba(20,184,166,0.35);
  color: #2dd4bf;
}
.pub-type.preprint {
  background: rgba(245,158,11,0.1);
  border: 1px solid rgba(245,158,11,0.35);
  color: #fbbf24;
}
.pub-venue {
  font-size: 0.78em;
  font-weight: 700;
  color: #0ea5e9;
}
.pub-date {
  font-size: 0.75em;
  opacity: 0.5;
  margin-left: auto;
}

/* ── Title ── */
.pub-title {
  font-size: 0.98em;
  font-weight: 700;
  line-height: 1.4;
  margin-bottom: 0.45em;
}

/* ── Abstract ── */
.pub-abstract {
  font-size: 0.84em;
  line-height: 1.6;
  opacity: 0.75;
  margin-bottom: 0.7em;
}

/* ── Action buttons ── */
.pub-actions {
  display: flex;
  gap: 0.5em;
  flex-wrap: wrap;
}
.pub-btn {
  font-size: 0.75em;
  font-weight: 600;
  padding: 4px 12px;
  border-radius: 6px;
  border: 1px solid rgba(128,128,128,0.3);
  text-decoration: none;
  color: inherit;
  transition: all 0.15s;
  cursor: pointer;
  background: transparent;
}
.pub-btn:hover {
  border-color: #0ea5e9;
  color: #0ea5e9;
  text-decoration: none;
}
.pub-btn.primary {
  background: #0ea5e9;
  border-color: #0ea5e9;
  color: #fff;
}
.pub-btn.primary:hover {
  background: #38bdf8;
  border-color: #38bdf8;
  color: #fff;
}

/* ── BibTeX popup ── */
.pub-bibtex {
  display: none;
  margin-top: 0.8em;
  background: rgba(128,128,128,0.07);
  border: 1px solid rgba(128,128,128,0.2);
  border-radius: 6px;
  padding: 0.8em 1em;
  font-family: monospace;
  font-size: 0.78em;
  line-height: 1.6;
  white-space: pre;
  overflow-x: auto;
}
.pub-bibtex.open { display: block; }

/* ── Year divider ── */
.pub-year-divider {
  font-size: 0.72em;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  opacity: 0.4;
  margin: 1.8em 0 0.7em 0;
  display: flex;
  align-items: center;
  gap: 0.6em;
}
.pub-year-divider::after {
  content: '';
  flex: 1;
  height: 1px;
  background: rgba(128,128,128,0.2);
}

/* ── Responsive ── */
@media (max-width: 560px) {
  .pub-date { margin-left: 0; }
  .pub-stats { gap: 0.7em; }
}
</style>

<!-- ═══════ STATS ═══════ -->
<div class="pub-stats">
  <div class="pub-stat"><strong>3</strong><span>Total Papers</span></div>
  <div class="pub-stat"><strong>1</strong><span>Conference</span></div>
  <div class="pub-stat"><strong>2</strong><span>Journal Articles</span></div>
</div>

<!-- ═══════ FILTERS ═══════ -->
<div class="pub-filters">
  <button class="pub-filter-btn active" onclick="filterPubs('all', this)">All</button>
  <button class="pub-filter-btn" onclick="filterPubs('conference', this)">Conference</button>
  <button class="pub-filter-btn" onclick="filterPubs('journal', this)">Journal</button>
  <button class="pub-filter-btn" onclick="filterPubs('preprint', this)">Preprint</button>
</div>

<!-- ═══════════════════════════════════════
     PAPERS — add new entries following
     the same .pub-card block structure
════════════════════════════════════════ -->

<div class="pub-year-divider">2026</div>

<!-- PAPER 1 -->
<div class="pub-card" data-type="conference">
  <div class="pub-card-meta">
    <span class="pub-type conference">Conference</span>
    <span class="pub-venue">WACV 2026</span>
    <span class="pub-date">January 2026</span>
  </div>
  <div class="pub-title">
    GFT-GCN: Privacy-Preserving 3D Face Mesh Recognition with Spectral Diffusion
  </div>
  <div class="pub-abstract">
    3D face recognition provides strong security but requires protection of stored biometric templates. We propose GFT-GCN, a privacy-preserving framework that combines spectral graph learning and diffusion-based template protection to generate secure, irreversible templates. Experiments on BU-3DFE and FaceScape show high accuracy and strong resistance to reconstruction attacks, achieving a good balance between privacy and performance.
  </div>
  <div class="pub-actions">
    <a href="https://arxiv.org/pdf/2511.19958" target="_blank" class="pub-btn primary">📄 Paper</a>
    <button class="pub-btn" onclick="toggleBibtex(this)">📋 BibTeX</button>
  </div>
  <div class="pub-bibtex">@inproceedings{felouat2026gftgcn,
  title     = {GFT-GCN: Privacy-Preserving 3D Face Mesh Recognition with Spectral Diffusion},
  author    = {Felouat, Hichem and others},
  booktitle = {Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)},
  year      = {2026}
}</div>
</div>

<div class="pub-year-divider">2025</div>

<!-- PAPER 2 -->
<div class="pub-card" data-type="journal">
  <div class="pub-card-meta">
    <span class="pub-type journal">Journal</span>
    <span class="pub-venue">IEEE Access</span>
    <span class="pub-date">2025</span>
  </div>
  <div class="pub-title">
    3DDGD: 3D Deepfake Generation and Detection Using 3D Face Meshes
  </div>
  <div class="pub-abstract">
    3D face technology offers stronger security than 2D methods in biometric authentication. This study enhances 3D facial systems against deepfakes by demonstrating the superiority of 3D over 2D, creating a real/fake 3D face dataset, and developing deepfake detection models using MLP, self-attention, and TabTransformer. Results show that 3D face meshes significantly improve deepfake detection robustness.
  </div>
  <div class="pub-actions">
    <a href="https://ieeexplore.ieee.org/abstract/document/11039631/" target="_blank" class="pub-btn primary">📄 Paper</a>
    <button class="pub-btn" onclick="toggleBibtex(this)">📋 BibTeX</button>
  </div>
  <div class="pub-bibtex">@article{felouat2025_3ddgd,
  title   = {3DDGD: 3D Deepfake Generation and Detection Using 3D Face Meshes},
  author  = {Felouat, Hichem and others},
  journal = {IEEE Access},
  year    = {2025}
}</div>
</div>

<div class="pub-year-divider">2024</div>

<!-- PAPER 3 -->
<div class="pub-card" data-type="journal">
  <div class="pub-card-meta">
    <span class="pub-type journal">Journal</span>
    <span class="pub-venue">IEEE Access</span>
    <span class="pub-date">2024</span>
  </div>
  <div class="pub-title">
    eKYC-DF: A Large-Scale Deepfake Dataset for Developing and Evaluating eKYC Systems
  </div>
  <div class="pub-abstract">
    eKYC systems are vulnerable to advanced deepfakes, and existing datasets are not suitable for evaluating such attacks. To address this, a large-scale dataset of 228,000+ diverse fake videos with proper evaluation protocols was created specifically for eKYC systems.
  </div>
  <div class="pub-actions">
    <a href="https://ieeexplore.ieee.org/abstract/document/10444105" target="_blank" class="pub-btn primary">📄 Paper</a>
    <button class="pub-btn" onclick="toggleBibtex(this)">📋 BibTeX</button>
  </div>
  <div class="pub-bibtex">@article{felouat2024_ekyc,
  title   = {eKYC-DF: A Large-Scale Deepfake Dataset for Developing and Evaluating eKYC Systems},
  author  = {Felouat, Hichem and others},
  journal = {IEEE Access},
  year    = {2024}
}</div>
</div>

<!--
═══════════════════════════════════════════
  HOW TO ADD A NEW PAPER:
  1. Add a .pub-year-divider if it's a new year
  2. Copy one .pub-card block below
  3. Set data-type="conference" | "journal" | "preprint"
  4. Fill in venue, date, title, abstract, paper URL, bibtex
═══════════════════════════════════════════
-->

<script>
function filterPubs(type, btn) {
  document.querySelectorAll('.pub-filter-btn').forEach(function(b) {
    b.classList.remove('active');
  });
  btn.classList.add('active');

  document.querySelectorAll('.pub-card').forEach(function(card) {
    if (type === 'all' || card.dataset.type === type) {
      card.classList.remove('hidden');
    } else {
      card.classList.add('hidden');
    }
  });

  // hide year dividers with no visible cards after them
  document.querySelectorAll('.pub-year-divider').forEach(function(div) {
    var next = div.nextElementSibling;
    var hasVisible = false;
    while (next && !next.classList.contains('pub-year-divider')) {
      if (next.classList.contains('pub-card') && !next.classList.contains('hidden')) {
        hasVisible = true; break;
      }
      next = next.nextElementSibling;
    }
    div.style.display = hasVisible ? '' : 'none';
  });
}

function toggleBibtex(btn) {
  var bib = btn.closest('.pub-card').querySelector('.pub-bibtex');
  bib.classList.toggle('open');
  btn.textContent = bib.classList.contains('open') ? '✕ BibTeX' : '📋 BibTeX';
}
</script>
