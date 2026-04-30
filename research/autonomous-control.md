---
layout: default
title: LLM Application in Agriculture
---

<section class="page-hero">
  <div class="container page-hero__inner">
    <div class="page-hero__text">
      <p class="page-hero__label">Track 2 · Engineering Systems</p>
      <h1 class="page-hero__title">LLM Application<br>in Agriculture</h1>
      <p class="page-hero__desc">Encoding expert knowledge into language models for agricultural decision-making</p>
    </div>
    <div class="page-hero__visual">
      <svg viewBox="0 0 400 280" fill="none" xmlns="http://www.w3.org/2000/svg" class="hero__diagram">
        <!-- Terminal frame -->
        <rect x="20" y="16" width="360" height="248" rx="12" fill="rgba(255,255,255,.04)" stroke="rgba(255,255,255,.18)" stroke-width="1.2"/>
        <rect x="20" y="16" width="360" height="28" rx="12" fill="rgba(255,255,255,.06)"/>
        <rect x="20" y="32" width="360" height="12" fill="rgba(255,255,255,.06)"/>
        <circle cx="38" cy="30" r="4" fill="rgba(255,100,100,.5)"/>
        <circle cx="52" cy="30" r="4" fill="rgba(255,200,80,.5)"/>
        <circle cx="66" cy="30" r="4" fill="rgba(100,220,120,.5)"/>
        <text x="200" y="34" text-anchor="middle" fill="rgba(255,255,255,.35)" font-size="9" font-family="monospace">llm-agri-reasoning</text>

        <!-- Step 1: Encode knowledge -->
        <text x="36" y="66" fill="rgba(130,170,255,.7)" font-size="10" font-family="monospace">&#x276F;</text>
        <text x="48" y="66" fill="rgba(255,255,255,.55)" font-size="10" font-family="monospace">model.encode(domain_knowledge)</text>
        <text x="36" y="82" fill="rgba(255,255,255,.3)" font-size="9" font-family="monospace">  papers: 5,000  &#x2022;  expert rules: 128</text>
        <text x="36" y="96" fill="rgba(255,255,255,.25)" font-size="8" font-family="monospace">  embedding &#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2588;&#x2593;&#x2591;&#x2591; 84%</text>

        <!-- Step 2: Reason -->
        <text x="36" y="120" fill="rgba(130,170,255,.7)" font-size="10" font-family="monospace">&#x276F;</text>
        <text x="48" y="120" fill="rgba(255,255,255,.55)" font-size="10" font-family="monospace">model.reason(observation)</text>
        <text x="36" y="136" fill="rgba(255,255,255,.3)" font-size="9" font-family="monospace">  input: {EC: 2.8, moisture: 62%}</text>
        <text x="36" y="152" fill="rgba(255,255,255,.3)" font-size="9" font-family="monospace">  &#x2192; retrieving relevant knowledge...</text>
        <text x="36" y="166" fill="rgba(255,255,255,.3)" font-size="9" font-family="monospace">  &#x2192; cross-referencing 12 experiences</text>

        <!-- Step 3: Act + Learn -->
        <text x="36" y="190" fill="rgba(130,170,255,.7)" font-size="10" font-family="monospace">&#x276F;</text>
        <text x="48" y="190" fill="rgba(255,255,255,.55)" font-size="10" font-family="monospace">model.act_and_learn()</text>
        <text x="36" y="206" fill="rgba(100,220,160,.5)" font-size="9" font-family="monospace">  &#x2713; decision: adjust irrigation &#x2212;15%</text>
        <text x="36" y="220" fill="rgba(100,220,160,.4)" font-size="9" font-family="monospace">  &#x2713; memory updated  &#x2022;  cycle #37</text>

        <!-- Blinking cursor -->
        <rect x="36" y="234" width="7" height="13" rx="1" fill="rgba(130,170,255,.6)">
          <animate attributeName="opacity" values="1;0;1" dur="1.2s" repeatCount="indefinite"/>
        </rect>
        <!-- Status bar -->
        <rect x="20" y="248" width="360" height="16" rx="0" fill="rgba(255,255,255,.05)"/>
        <text x="36" y="259" fill="rgba(130,170,255,.5)" font-size="7" font-family="monospace">&#x25CF; REASONING</text>
        <text x="340" y="259" fill="rgba(255,255,255,.3)" font-size="7" font-family="monospace">cycle 37</text>
      </svg>
    </div>
  </div>
</section>

<!-- ───── Overview (split) ───── -->
<section class="rd-overview-split">
  <div class="rd-overview-split__text">
    <h2 class="rd-overview-split__heading">Encoding expert knowledge into language models</h2>
    <p class="rd-overview-split__desc">Skilled growers and researchers accumulate domain knowledge over years of experience. We explore whether large language models can capture that expertise — and apply it to real agricultural tasks. Our LLM-based irrigation agent reads substrate sensors, decides when and how much to water, and refines its strategy through an experience-memory mechanism across successive growing cycles.</p>
  </div>
  <div class="rd-overview-split__visual">
    <div class="rd-overview-split__circle"></div>
    <svg viewBox="0 0 400 280" fill="none" xmlns="http://www.w3.org/2000/svg" class="rd-overview-split__illustration">
      <!-- Circular feedback loop diagram -->
      <circle cx="200" cy="140" r="105" fill="none" stroke="rgba(255,255,255,.1)" stroke-width="1" stroke-dasharray="6 4"/>
      <circle cx="200" cy="140" r="72" fill="none" stroke="rgba(255,255,255,.06)" stroke-width="1"/>
      <!-- Center node: LLM Agent -->
      <circle cx="200" cy="140" r="32" fill="rgba(255,255,255,.06)" stroke="rgba(255,255,255,.3)" stroke-width="1.5"/>
      <text x="200" y="136" text-anchor="middle" fill="rgba(255,255,255,.8)" font-size="11" font-weight="700">LLM</text>
      <text x="200" y="150" text-anchor="middle" fill="rgba(255,255,255,.45)" font-size="8">Agent</text>
      <!-- Orbit nodes -->
      <circle cx="200" cy="35" r="22" fill="rgba(100,220,160,.08)" stroke="rgba(100,220,160,.4)" stroke-width="1"/>
      <text x="200" y="33" text-anchor="middle" fill="rgba(100,220,160,.8)" font-size="8" font-weight="600">Sense</text>
      <text x="200" y="43" text-anchor="middle" fill="rgba(255,255,255,.4)" font-size="7">substrate</text>
      <circle cx="305" cy="140" r="22" fill="rgba(130,170,255,.08)" stroke="rgba(130,170,255,.4)" stroke-width="1"/>
      <text x="305" y="138" text-anchor="middle" fill="rgba(130,170,255,.8)" font-size="8" font-weight="600">Decide</text>
      <text x="305" y="148" text-anchor="middle" fill="rgba(255,255,255,.4)" font-size="7">volume</text>
      <circle cx="200" cy="245" r="22" fill="rgba(255,180,80,.08)" stroke="rgba(255,180,80,.4)" stroke-width="1"/>
      <text x="200" y="243" text-anchor="middle" fill="rgba(255,180,80,.8)" font-size="8" font-weight="600">Irrigate</text>
      <text x="200" y="253" text-anchor="middle" fill="rgba(255,255,255,.4)" font-size="7">pump</text>
      <circle cx="95" cy="140" r="22" fill="rgba(200,140,255,.08)" stroke="rgba(200,140,255,.4)" stroke-width="1"/>
      <text x="95" y="138" text-anchor="middle" fill="rgba(200,140,255,.8)" font-size="8" font-weight="600">Reflect</text>
      <text x="95" y="148" text-anchor="middle" fill="rgba(255,255,255,.4)" font-size="7">memory</text>
      <!-- Connecting arcs -->
      <path d="M218 42 Q270 60 298 122" fill="none" stroke="rgba(255,255,255,.2)" stroke-width="1"/>
      <circle cx="298" cy="120" r="2" fill="rgba(255,255,255,.4)"/>
      <path d="M298 158 Q270 220 218 238" fill="none" stroke="rgba(255,255,255,.2)" stroke-width="1"/>
      <circle cx="220" cy="237" r="2" fill="rgba(255,255,255,.4)"/>
      <path d="M182 238 Q130 220 102 158" fill="none" stroke="rgba(255,255,255,.2)" stroke-width="1"/>
      <circle cx="103" cy="160" r="2" fill="rgba(255,255,255,.4)"/>
      <path d="M102 122 Q130 60 182 42" fill="none" stroke="rgba(255,255,255,.2)" stroke-width="1"/>
      <circle cx="180" cy="43" r="2" fill="rgba(255,255,255,.4)"/>
      <!-- Inner connecting lines -->
      <line x1="200" y1="57" x2="200" y2="108" stroke="rgba(255,255,255,.12)" stroke-width="1" stroke-dasharray="3 3"/>
      <line x1="283" y1="140" x2="232" y2="140" stroke="rgba(255,255,255,.12)" stroke-width="1" stroke-dasharray="3 3"/>
      <line x1="200" y1="223" x2="200" y2="172" stroke="rgba(255,255,255,.12)" stroke-width="1" stroke-dasharray="3 3"/>
      <line x1="117" y1="140" x2="168" y2="140" stroke="rgba(255,255,255,.12)" stroke-width="1" stroke-dasharray="3 3"/>
      <!-- Animated pulse -->
      <circle r="3" fill="rgba(100,220,160,.6)">
        <animateMotion dur="6s" repeatCount="indefinite" path="M200,35 Q305,35 305,140 Q305,245 200,245 Q95,245 95,140 Q95,35 200,35"/>
      </circle>
    </svg>
  </div>
</section>

<!-- ───── Research Topics (3-card layout) ───── -->
<section class="rd-band rd-band--dark">
  <div class="rd-band__inner">
    <h2>Research Topics</h2>
    <p class="rd-band__subtitle">Two current research directions applying LLMs to agricultural knowledge and production systems.</p>

    <div class="rd-topics-grid rd-topics-grid--2col">
      <div class="rd-topics-grid__card">
        <div class="rd-topics-grid__placeholder-img"><span>Photo</span></div>
        <div class="rd-topics-grid__caption">
          <h3>Autonomous Irrigation</h3>
          <div class="rd-topics-grid__keywords">
            <span class="badge">Function Calling</span>
            <span class="badge">Experience Memory</span>
            <span class="badge">Substrate Sensing</span>
          </div>
        </div>
        <p class="rd-topics-grid__desc">LLM agents read sensors, decide irrigation volume, and learn from outcomes over successive growing cycles</p>
      </div>

      <div class="rd-topics-grid__card">
        <div class="rd-topics-grid__placeholder-img"><span>Photo</span></div>
        <div class="rd-topics-grid__caption">
          <h3>Knowledge Graph Construction</h3>
          <div class="rd-topics-grid__keywords">
            <span class="badge">Literature Mining</span>
            <span class="badge">Entity Extraction</span>
            <span class="badge">Research Discovery</span>
          </div>
        </div>
        <p class="rd-topics-grid__desc">Automated mining of scientific literature to build large-scale knowledge networks for research discovery</p>
      </div>
    </div>
  </div>
</section>
