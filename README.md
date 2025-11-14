## Hi there 👋

<!doctype html>
<html>
<head>
<meta charset="utf-8" />
<title>Neuron workflow animation — example</title>
<style>
  body { background:#0f1720; display:flex; height:100vh; align-items:center; justify-content:center; margin:0; }
  svg { width:760px; height:420px; }
  .dendrite { stroke:#7aa3ff; stroke-width:6; fill:none; stroke-linecap:round; opacity:0.75; }
  .neuron { fill:#2b2d42; stroke:#101214; stroke-width:2; }
  .nucleus { fill:#111827; opacity:0.95; }
  .pulse { stroke:#ffb86b; stroke-width:8; stroke-linecap:round; fill:none; stroke-dasharray:12 200; animation:travel 1s linear infinite; }
  .glow { filter:url(#f1); opacity:0; transform-origin:center; animation:flash 1s linear infinite; }
  .label { fill:#cbd5e1; font-family:Inter, Arial, sans-serif; font-size:14px; }
  @keyframes travel {
    0% { stroke-dashoffset:220; opacity:0 }
    10% { opacity:1 }
    50% { stroke-dashoffset:0; opacity:1 }
    90% { opacity:1 }
    100% { stroke-dashoffset:-220; opacity:0 }
  }
  @keyframes flash {
    0% { opacity:0; transform:scale(0.9) }
    40% { opacity:0.9; transform:scale(1.12) }
    70% { opacity:0.4; transform:scale(1.02) }
    100% { opacity:0; transform:scale(0.9) }
  }
  /* Stagger pulses by adding classes */
  .pulse.delay1 { animation-delay:0.2s }
  .pulse.delay2 { animation-delay:0.45s }
  .glow.delay1 { animation-delay:0.2s }
  .glow.delay2 { animation-delay:0.45s }
</style>
</head>
<body>
<svg viewBox="0 0 760 420" xmlns="http://www.w3.org/2000/svg" aria-label="AI neuron workflow animation">
  <defs>
    <!-- soft glow filter -->
    <filter id="f1" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="8" result="b"/>
      <feMerge>
        <feMergeNode in="b"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>

  <!-- path from left input to neuron1 -->
  <path id="p1" d="M90 200 C170 140, 230 140, 280 200" class="dendrite"/>
  <!-- traveling pulse on p1 -->
  <path d="M90 200 C170 140, 230 140, 280 200" class="pulse"/>

  <!-- neuron1 -->
  <g transform="translate(280,200)">
    <circle cx="0" cy="0" r="36" class="neuron"/>
    <circle cx="0" cy="0" r="12" class="nucleus"/>
    <circle cx="0" cy="0" r="56" class="glow"/>
    <text x="0" y="70" text-anchor="middle" class="label">Neuron 1</text>
  </g>

  <!-- path p2: neuron1 -> neuron2 -->
  <path id="p2" d="M316 238 C380 300, 460 300, 520 238" class="dendrite"/>
  <path d="M316 238 C380 300, 460 300, 520 238" class="pulse delay1"/>

  <!-- neuron2 -->
  <g transform="translate(520,238)">
    <circle cx="0" cy="0" r="36" class="neuron"/>
    <circle cx="0" cy="0" r="12" class="nucleus"/>
    <circle cx="0" cy="0" r="56" class="glow delay1"/>
    <text x="0" y="70" text-anchor="middle" class="label">Neuron 2</text>
  </g>

  <!-- path p3: neuron2 -> neuron3 (downwards) -->
  <path id="p3" d="M556 276 C620 340, 620 420, 620 420" class="dendrite"/>
  <path d="M556 276 C620 340, 620 420, 620 420" class="pulse delay2"/>

  <!-- neuron3 -->
  <g transform="translate(620,420)">
    <circle cx="0" cy="0" r="36" class="neuron"/>
    <circle cx="0" cy="0" r="12" class="nucleus"/>
    <circle cx="0" cy="0" r="56" class="glow delay2"/>
    <text x="0" y="70" text-anchor="middle" class="label">Output</text>
  </g>

  <!-- optional labels for inputs -->
  <text x="30" y="180" class="label">Input</text>
  <text x="360" y="120" class="label">Weights → Activation</text>
</svg>
</body>
</html>


<p align="center" width="100%">
  <a href="https://github.com/DenverCoder1/readme-typing-svg" width="100%"><img src="https://readme-typing-svg.herokuapp.com/?lines=Hey%20👋;I'm%20Dinusara%20Nethmal;SLIIT%20Undergraduate%20🎓&font=Calibri&center=true&width=440&height=45&weight=700&color=#00ddff&vCenter=true&size=28" width="100%"></a>
</p>
<!--
**DinusaraNethmal/DinusaraNethmal** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
