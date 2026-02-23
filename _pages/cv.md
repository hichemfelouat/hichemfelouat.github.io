---
layout: archive
title: "CV"
permalink: /cv/
author_profile: false
---

<style>
/* ── Global selectable text ── */
.page__content, .page__content * {
  user-select: text !important;
  -webkit-user-select: text !important;
  -moz-user-select: text !important;
}

/* ── Base variables ── */
:root {
  --blue:    #1a56db;
  --blue-lt: #e8f0fe;
  --teal:    #0891b2;
  --gray:    #64748b;
  --border:  #e2e8f0;
  --bg-soft: #f8fafc;
  --text:    #1e293b;
  --radius:  10px;
  --shadow:  0 2px 12px rgba(0,0,0,0.07);
}

/* ── Download bar ── */
.cv-download-bar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: linear-gradient(135deg, #1a56db 0%, #0891b2 100%);
  border-radius: var(--radius);
  padding: 1em 1.4em;
  margin-bottom: 2em;
  color: white;
}
.cv-download-bar strong { font-size: 1.05em; }
.cv-download-bar small { opacity: 0.85; font-size: 0.82em; }
.cv-dl-btn {
  background: white;
  color: var(--blue);
  font-weight: 700;
  border: none;
  padding: 0.55em 1.2em;
  border-radius: 6px;
  text-decoration: none;
  font-size: 0.9em;
  transition: box-shadow 0.2s;
  white-space: nowrap;
}
.cv-dl-btn:hover { box-shadow: 0 4px 16px rgba(0,0,0,0.15); color: var(--blue); }

/* ── Section headers ── */
.cv-section-header {
  background: linear-gradient(135deg, #1a56db 0%, #0891b2 100%);
  border-radius: 6px;
  padding: 0.45em 0.9em;
  margin: 2em 0 1em 0;
}
.cv-section-header h2 {
  margin: 0;
  font-size: 1.05em;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  color: #ffffff !important;
  font-weight: 700;
  border: none !important;
  padding: 0 !important;
}


/* ── Entry cards ── */
.cv-entry {
  display: flex;
  gap: 1em;
  padding: 0.9em 1.1em;
  border: 1px solid var(--border);
  border-radius: var(--radius);
  margin-bottom: 0.7em;
  background: white;
  transition: box-shadow 0.18s, border-color 0.18s;
  position: relative;
}
.cv-entry:hover {
  box-shadow: var(--shadow);
  border-color: #b8d0fa;
}
.cv-entry-left {
  min-width: 130px;
  max-width: 130px;
  text-align: right;
  padding-top: 0.1em;
}
.cv-entry-date {
  font-size: 0.78em;
  color: var(--gray);
  font-weight: 600;
  line-height: 1.4;
  background: var(--bg-soft);
  border-radius: 4px;
  padding: 2px 7px;
  display: inline-block;
}
.cv-entry-body { flex: 1; }
.cv-entry-body strong { color: var(--text); font-size: 0.97em; }
.cv-entry-body .cv-inst {
  color: var(--teal);
  font-size: 0.88em;
  font-weight: 600;
  margin-top: 1px;
}
.cv-entry-body .cv-loc {
  color: var(--gray);
  font-size: 0.82em;
}
.cv-entry-body .cv-bullets {
  margin: 0.45em 0 0 0;
  padding-left: 1.1em;
  font-size: 0.87em;
  color: #334155;
  line-height: 1.6;
}
.cv-entry-body .cv-bullets li { margin-bottom: 2px; }

/* ── Skill tags ── */
.skill-group { margin-bottom: 0.85em; }
.skill-group-label {
  font-size: 0.8em;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  color: var(--gray);
  margin-bottom: 0.4em;
}
.skill-tags { display: flex; flex-wrap: wrap; gap: 6px; }
.skill-tag {
  background: var(--bg-soft);
  border: 1px solid var(--border);
  color: var(--text);
  border-radius: 20px;
  padding: 3px 12px;
  font-size: 0.82em;
  font-weight: 500;
  transition: all 0.15s;
  cursor: default;
}
.skill-tag:hover {
  background: var(--blue-lt);
  border-color: #93b8fa;
  color: var(--blue);
}
.skill-tag.highlight {
  background: var(--blue-lt);
  border-color: #93b8fa;
  color: var(--blue);
  font-weight: 600;
}

/* ── Language bars ── */
.lang-row {
  display: flex;
  align-items: center;
  gap: 0.8em;
  margin-bottom: 0.55em;
}
.lang-name { width: 90px; font-size: 0.9em; font-weight: 600; }
.lang-level { font-size: 0.78em; color: var(--gray); width: 80px; }
.lang-bar { flex: 1; height: 7px; background: var(--border); border-radius: 4px; overflow: hidden; }
.lang-fill { height: 100%; border-radius: 4px; background: linear-gradient(90deg, var(--blue), var(--teal)); }

/* ── Awards ── */
.award-item {
  display: flex;
  align-items: flex-start;
  gap: 0.8em;
  padding: 0.7em 1em;
  border-radius: var(--radius);
  background: linear-gradient(135deg, #fffbeb, #fef3c7);
  border: 1px solid #fcd34d;
  margin-bottom: 0.6em;
}
.award-year {
  background: #f59e0b;
  color: white;
  font-weight: 700;
  font-size: 0.78em;
  padding: 2px 8px;
  border-radius: 4px;
  white-space: nowrap;
  margin-top: 1px;
}
.award-text { font-size: 0.9em; color: #78350f; }

/* ── Responsive ── */
@media (max-width: 600px) {
  .cv-entry { flex-direction: column; }
  .cv-entry-left { min-width: unset; max-width: unset; text-align: left; }
  .cv-download-bar { flex-direction: column; gap: 0.8em; text-align: center; }
}
</style>

<div class="cv-download-bar">
  <div>
    <strong>Hichem Felouat — Curriculum Vitae</strong><br>
    <small>PhD Student · National Institute of Informatics, Tokyo · Last updated February 2026</small>
  </div>
  <a href="/files/cv.pdf" class="cv-dl-btn">⬇ Download PDF</a>
</div>

<!-- ─────────────── EDUCATION ─────────────── -->
<div class="cv-section-header">
  <h2>🎓 Education</h2>
</div>
<div id="sec-edu">

<div class="cv-entry">
  <div class="cv-entry-left"><span class="cv-entry-date">10/2022 – 07/2027</span></div>
  <div class="cv-entry-body">
    <strong>PhD2 in Information Security</strong> <em>(Current)</em>
    <div class="cv-inst">National Institute of Informatics (NII) · SOKENDAI</div>
    <div class="cv-loc">📍 Tokyo, Japan — Echizen Laboratory</div>
  </div>
</div>

<div class="cv-entry">
  <div class="cv-entry-left"><span class="cv-entry-date">2016 – 2021</span></div>
  <div class="cv-entry-body">
    <strong>PhD1 in Data Science and Computing</strong>
    <div class="cv-inst">Blida University · LRDSI Laboratory</div>
    <div class="cv-loc">📍 Blida, Algeria</div>
  </div>
</div>

<div class="cv-entry">
  <div class="cv-entry-left"><span class="cv-entry-date">2013 – 2015</span></div>
  <div class="cv-entry-body">
    <strong>Master of Science in Artificial Intelligence</strong>
    <div class="cv-inst">Jijel University</div>
    <div class="cv-loc">📍 Jijel, Algeria</div>
  </div>
</div>

<div class="cv-entry">
  <div class="cv-entry-left"><span class="cv-entry-date">2010 – 2013</span></div>
  <div class="cv-entry-body">
    <strong>Bachelor of Science in Computer Science</strong>
    <div class="cv-inst">Jijel University</div>
    <div class="cv-loc">📍 Jijel, Algeria</div>
  </div>
</div>

</div>

<!-- ─────────────── RESEARCH EXPERIENCE ─────────────── -->
<div class="cv-section-header">
  <h2>🔬 Research Experience</h2>
</div>
<div id="sec-research">

<div class="cv-entry">
  <div class="cv-entry-left"><span class="cv-entry-date">10/2022 – Present</span></div>
  <div class="cv-entry-body">
    <strong>PhD Student Researcher</strong>
    <div class="cv-inst">National Institute of Informatics (NII)</div>
    <div class="cv-loc">📍 Tokyo, Japan — Echizen Laboratory</div>
    <ul class="cv-bullets">
      <li>3D face recognition and deepfake detection</li>
      <li>Privacy-preserving biometric systems</li>
      <li>Multimodal vision-language models</li>
      <li>eKYC systems security</li>
    </ul>
  </div>
</div>

<div class="cv-entry">
  <div class="cv-entry-left"><span class="cv-entry-date">2019 – Present</span></div>
  <div class="cv-entry-body">
    <strong>Machine Learning and Deep Learning Trainer</strong>
    <div class="cv-inst">Independent / Consulting</div>
    <ul class="cv-bullets">
      <li>Training and consulting on ML/DL applications</li>
      <li>Computer vision and AI projects</li>
    </ul>
  </div>
</div>

<div class="cv-entry">
  <div class="cv-entry-left"><span class="cv-entry-date">2018 – 2019</span></div>
  <div class="cv-entry-body">
    <strong>Teaching Assistant</strong>
    <div class="cv-inst">Jijel University</div>
    <div class="cv-loc">📍 Jijel, Algeria</div>
    <ul class="cv-bullets">
      <li>Course instruction and student support</li>
    </ul>
  </div>
</div>

<div class="cv-entry">
  <div class="cv-entry-left"><span class="cv-entry-date">2011 – 2018</span></div>
  <div class="cv-entry-body">
    <strong>Co-founder and President</strong>
    <div class="cv-inst">Computer Sciences Club Jijel (CSCJ)</div>
    <div class="cv-loc">📍 Jijel, Algeria</div>
  </div>
</div>

</div>

<!-- ─────────────── AREAS OF EXPERTISE ─────────────── -->
<div class="cv-section-header">
  <h2>💡 Areas of Expertise</h2>
</div>
<div id="sec-expertise">
  <div class="skill-tags" style="margin-bottom:0.5em;">
    <span class="skill-tag highlight">Artificial Intelligence</span>
    <span class="skill-tag highlight">Deep Learning</span>
    <span class="skill-tag highlight">Computer Vision &amp; 3D Vision</span>
    <span class="skill-tag highlight">Deepfake Detection &amp; Generation</span>
    <span class="skill-tag highlight">Information Security</span>
    <span class="skill-tag highlight">Biometric Security</span>
    <span class="skill-tag highlight">Privacy-Preserving AI</span>
    <span class="skill-tag highlight">Federated Learning</span>
    <span class="skill-tag">Data Science</span>
    <span class="skill-tag">Graph Neural Networks</span>
    <span class="skill-tag">Geometric Deep Learning</span>
    <span class="skill-tag">Neural Networks</span>
  </div>
</div>

<!-- ─────────────── TECHNICAL SKILLS ─────────────── -->
<div class="cv-section-header">
  <h2>🛠 Technical Skills</h2>
</div>
<div id="sec-skills">

<div class="skill-group">
  <div class="skill-group-label">Deep Learning Frameworks</div>
  <div class="skill-tags">
    <span class="skill-tag highlight">PyTorch</span>
    <span class="skill-tag highlight">TensorFlow</span>
    <span class="skill-tag">OpenCV</span>
  </div>
</div>

<div class="skill-group">
  <div class="skill-group-label">3D Vision &amp; Graphics</div>
  <div class="skill-tags">
    <span class="skill-tag highlight">3D Face Reconstruction</span>
    <span class="skill-tag highlight">3D Mesh Processing</span>
    <span class="skill-tag">3D CNNs</span>
    <span class="skill-tag">Graph Neural Networks</span>
    <span class="skill-tag">Point Cloud Processing</span>
  </div>
</div>

<div class="skill-group">
  <div class="skill-group-label">Machine Learning</div>
  <div class="skill-tags">
    <span class="skill-tag highlight">Computer Vision</span>
    <span class="skill-tag">Natural Language Processing</span>
    <span class="skill-tag">Time Series Analysis</span>
    <span class="skill-tag">Graph Learning</span>
  </div>
</div>

<div class="skill-group">
  <div class="skill-group-label">Data Science</div>
  <div class="skill-tags">
    <span class="skill-tag">Data Analysis &amp; Visualization</span>
    <span class="skill-tag">Statistical Analysis</span>
    <span class="skill-tag">Data Preprocessing</span>
  </div>
</div>

</div>

<!-- ─────────────── LANGUAGES ─────────────── -->
<div class="cv-section-header">
  <h2>🌐 Languages</h2>
</div>
<div id="sec-lang">

<div class="lang-row">
  <div class="lang-name">English</div>
  <div class="lang-level">Advanced</div>
  <div class="lang-bar"><div class="lang-fill" style="width:88%"></div></div>
</div>
<div class="lang-row">
  <div class="lang-name">French</div>
  <div class="lang-level">Advanced</div>
  <div class="lang-bar"><div class="lang-fill" style="width:85%"></div></div>
</div>
<div class="lang-row">
  <div class="lang-name">Arabic</div>
  <div class="lang-level">Native</div>
  <div class="lang-bar"><div class="lang-fill" style="width:100%"></div></div>
</div>

</div>

<!-- ─────────────── HONORS & AWARDS ─────────────── -->
<div class="cv-section-header">
  <h2>🏆 Honors &amp; Awards</h2>
</div>
<div id="sec-awards">

<div class="award-item">
  <span class="award-year">2022</span> 
  <span class="award-text">Awarded second place in the <strong> My Thesis in 180 Seconds competition </strong> (Algeria).</span>
</div>

</div>
