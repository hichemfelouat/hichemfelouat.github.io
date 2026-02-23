---
permalink: /
title: "About Me"
author_profile: true
---

<style>
/* Make ALL text selectable and copyable */
.page__content * {
  user-select: text !important;
  -webkit-user-select: text !important;
}

.bio-card {
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
  border-left: 4px solid #4285f4;
  border-radius: 8px;
  padding: 1.2em 1.5em;
  margin-bottom: 1.5em;
}

.news-item {
  padding: 0.5em 0;
  border-bottom: 1px solid #eee;
  display: flex;
  align-items: center;
  gap: 0.7em;
}

.news-badge {
  background: #4285f4;
  color: white;
  padding: 2px 8px;
  border-radius: 12px;
  font-size: 0.8em;
  white-space: nowrap;
  font-weight: bold;
}

.interest-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 0.5em;
}

.interest-tag {
  background: #e8f0fe;
  color: #1a73e8;
  padding: 4px 12px;
  border-radius: 16px;
  font-size: 0.85em;
  transition: background 0.2s;
}

.interest-tag:hover {
  background: #1a73e8;
  color: white;
  cursor: default;
}

.copy-btn {
  background: none;
  border: 1px solid #ccc;
  border-radius: 4px;
  padding: 2px 8px;
  font-size: 0.75em;
  cursor: pointer;
  float: right;
  margin-top: 0.3em;
}

.copy-btn:hover { background: #eee; }
</style>

<div class="bio-card">
  <button class="copy-btn" onclick="copyText('bio-text')">📋 Copy</button>
  <p id="bio-text">I am a PhD Student at the <strong>Echizen Laboratory</strong>, 
  <strong>National Institute of Informatics (NII)</strong>, 
  Graduate University for Advanced Studies (SOKENDAI), Tokyo, Japan.
  My research lies at the intersection of <strong>3D computer vision</strong>, 
  <strong>biometric security</strong>, and 
  <strong>multimodal large vision-language models (LVLMs)</strong>. 
  I focus on developing <strong>privacy-preserving 3D face recognition systems</strong> 
  that remain robust against deepfake and reconstruction attacks.</p>
</div>

## 🔬 Research Interests

<div class="interest-tags">
  <span class="interest-tag">3D Computer Vision</span>
  <span class="interest-tag">Biometric Security</span>
  <span class="interest-tag">Vision Language Models</span>
  <span class="interest-tag">Privacy-Preserving ML</span>
  <span class="interest-tag">Deepfake Detection</span>
  <span class="interest-tag">Federated Learning</span>
  <span class="interest-tag">3D Face Recognition</span>
  <span class="interest-tag">Graph Neural Networks</span>
</div>

## 📰 News

<div class="news-item">
  <span class="news-badge">2025.11</span>
  <span>One 1st-authored paper accepted at <strong>WACV 2026</strong>. 🎉</span>
</div>

<script>
function copyText(id) {
  const el = document.getElementById(id);
  navigator.clipboard.writeText(el.innerText).then(() => {
    const btn = el.parentElement.querySelector('.copy-btn');
    btn.textContent = '✅ Copied!';
    setTimeout(() => btn.textContent = '📋 Copy', 2000);
  });
}
</script>
