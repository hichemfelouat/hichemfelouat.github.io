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

@keyframes fadeUp {
  from { opacity: 0; transform: translateY(14px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* ── Stats ── */
.pub-stats {
  display: flex;
  gap: 1em;
  flex-wrap: wrap;
  margin-bottom: 2em;
}
.pub-stat {
  border: 1px solid rgba(128,128,128,0.2);
  border-left: 3px solid #0ea5e9;
  border-radius: 0 8px 8px 0;
  padding: 0.45em 1.1em;
  font-size: 0.82em;
  min-width: 90px;
}
.pub-stat strong { font-size: 1.35em; display: block; color: #0ea5e9; line-height: 1.2; }
.pub-stat span   { opacity: 0.55; font-size: 0.88em; }

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

/* ── Paper card ── */
.pub-card {
  border: 1px solid rgba(128,128,128,0.2);
  border-left: 3px solid #0ea5e9;
  border-radius: 0 10px 10px 0;
  padding: 1.1em 1.3em;
  margin-bottom: 1em;
  opacity: 0;
  animation: fadeUp 0.45s ease forwards;
  transition: box-shadow 0.18s, border-left-color 0.2s;
}
.pub-card:hover {
  box-shadow: 0 3px 14px rgba(0,0,0,0.1);
  border-left-color: #38bdf8;
}

/* ── Meta row ── */
.pub-meta {
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
.pub-type-conference {
  background: rgba(99,102,241,0.12);
  border: 1px solid rgba(99,102,241,0.35);
  color: #818cf8;
}
.pub-type-journal {
  background: rgba(20,184,166,0.1);
  border: 1px solid rgba(20,184,166,0.35);
  color: #2dd4bf;
}
.pub-type-preprint {
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
  font-size: 0.74em;
  opacity: 0.5;
  margin-left: auto;
}

/* ── Title & abstract ── */
.pub-title {
  font-size: 0.97em;
  font-weight: 700;
  line-height: 1.4;
  margin-bottom: 0.45em;
}
.pub-abstract {
  font-size: 0.84em;
  line-height: 1.65;
  opacity: 0.72;
  margin-bottom: 0.75em;
}

/* ── Paper link button ── */
.pub-btn {
  display: inline-block;
  font-size: 0.76em;
  font-weight: 600;
  padding: 4px 13px;
  border-radius: 6px;
  border: none;
  background: #0ea5e9;
  color: #fff;
  text-decoration: none;
  transition: background 0.15s;
}
.pub-btn:hover {
  background: #38bdf8;
  color: #fff;
  text-decoration: none;
}

@media (max-width: 560px) {
  .pub-date { margin-left: 0; }
}
</style>

<div id="pub-stats" class="pub-stats"></div>
<div id="pub-list"></div>

{% raw %}
<script>
/*
  PUBLICATIONS DICTIONARY
  To add a paper: copy one object and fill in the fields.
  Fields:
    title    - full paper title
    type     - "conference" | "journal" | "preprint"
    venue    - journal/conference name
    month    - e.g. "January" (or "" if unknown)
    year     - number, e.g. 2026
    abstract - short description
    url      - link to paper (use "" if not available)
*/
var PUBLICATIONS = [
  {
    title:    "GFT-GCN: Privacy-Preserving 3D Face Mesh Recognition with Spectral Diffusion",
    type:     "conference",
    venue:    "WACV 2026",
    month:    "March",
    year:     2026,
    abstract: "3D face recognition provides strong security but requires protection of stored biometric templates. We propose GFT-GCN, a privacy-preserving framework that combines spectral graph learning and diffusion-based template protection to generate secure, irreversible templates. Experiments on BU-3DFE and FaceScape show high accuracy and strong resistance to reconstruction attacks, achieving a good balance between privacy and performance.",
    url:      "https://arxiv.org/pdf/2511.19958"
  },
  {
    title:    "3DDGD: 3D Deepfake Generation and Detection Using 3D Face Meshes",
    type:     "journal",
    venue:    "IEEE Access",
    month:    "June",
    year:     2025,
    abstract: "3D face technology offers stronger security than 2D methods in biometric authentication. This study enhances 3D facial systems against deepfakes by demonstrating the superiority of 3D over 2D, creating a real/fake 3D face dataset, and developing deepfake detection models using MLP, self-attention, and TabTransformer. Results show that 3D face meshes significantly improve deepfake detection robustness.",
    url:      "https://ieeexplore.ieee.org/abstract/document/11039631/"
  },
  {
    title:    "eKYC-DF: A Large-Scale Deepfake Dataset for Developing and Evaluating eKYC Systems",
    type:     "journal",
    venue:    "IEEE Access",
    month:    "February",
    year:     2024,
    abstract: "eKYC systems are vulnerable to advanced deepfakes, and existing datasets are not suitable for evaluating such attacks. To address this, a large-scale dataset of 228,000+ diverse fake videos with proper evaluation protocols was created specifically for eKYC systems.",
    url:      "https://ieeexplore.ieee.org/abstract/document/10444105"
  }
];

(function () {
  var papers = PUBLICATIONS.slice().sort(function (a, b) {
    return b.year !== a.year ? b.year - a.year : 0;
  });

  var counts = { total: papers.length, conference: 0, journal: 0, preprint: 0 };
  papers.forEach(function (p) { if (counts[p.type] !== undefined) counts[p.type]++; });

  var statsEl = document.getElementById('pub-stats');
  statsEl.innerHTML =
    stat(counts.total,      'Total Papers') +
    stat(counts.conference, 'Conference')   +
    stat(counts.journal,    'Journal')      +
    (counts.preprint ? stat(counts.preprint, 'Preprint') : '');

  var listEl   = document.getElementById('pub-list');
  var html     = '';
  var lastYear = null;
  var delay    = 0.05;

  papers.forEach(function (p) {
    if (p.year !== lastYear) {
      html += '<div class="pub-year-divider">' + p.year + '</div>';
      lastYear = p.year;
    }
    var dateStr = p.month ? p.month + ' ' + p.year : '' + p.year;
    html += '<div class="pub-card" style="animation-delay:' + delay + 's">'
      + '<div class="pub-meta">'
      +   '<span class="pub-type pub-type-' + p.type + '">' + p.type + '</span>'
      +   '<span class="pub-venue">' + esc(p.venue) + '</span>'
      +   '<span class="pub-date">'  + esc(dateStr)  + '</span>'
      + '</div>'
      + '<div class="pub-title">'    + esc(p.title)    + '</div>'
      + '<div class="pub-abstract">' + esc(p.abstract) + '</div>'
      + (p.url ? '<a href="' + p.url + '" target="_blank" class="pub-btn">Paper</a>' : '')
      + '</div>';
    delay += 0.08;
  });

  listEl.innerHTML = html;

  function stat(n, label) {
    return '<div class="pub-stat"><strong>' + n + '</strong><span>' + label + '</span></div>';
  }
  function esc(s) {
    return String(s)
      .replace(/&/g, '&amp;').replace(/</g, '&lt;')
      .replace(/>/g, '&gt;').replace(/"/g, '&quot;');
  }
})();
</script>
{% endraw %}
