
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Chroma — Color Toolkit</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;700&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="css/shared.css">a
  <style>
    .hero {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 2rem;
      position: relative;
      overflow: hidden;
    }
    .hero-gradient {
      position: absolute;
      inset: 0;
      background: linear-gradient(135deg, #0f0f0f 0%, #1a0a2e 40%, #0d1a2e 70%, #0f0f0f 100%);
      z-index: 0;
    }
    .color-blobs {
      position: absolute;
      inset: 0;
      z-index: 1;
      pointer-events: none;
    }
    .blob {
      position: absolute;
      border-radius: 50%;
      filter: blur(80px);
      opacity: 0.25;
      animation: drift 8s ease-in-out infinite;
    }
    .blob-1 { width: 400px; height: 400px; background: #7c3aed; top: -100px; left: -100px; animation-delay: 0s; }
    .blob-2 { width: 300px; height: 300px; background: #ec4899; top: 50%; right: -80px; animation-delay: 2s; }
    .blob-3 { width: 250px; height: 250px; background: #06b6d4; bottom: -80px; left: 30%; animation-delay: 4s; }
    @keyframes drift {
      0%, 100% { transform: translate(0, 0) scale(1); }
      50% { transform: translate(20px, -20px) scale(1.05); }
    }
    .hero-content { position: relative; z-index: 2; }
    .eyebrow {
      font-family: 'Space Mono', monospace;
      font-size: 0.75rem;
      letter-spacing: 0.2em;
      color: #a78bfa;
      text-transform: uppercase;
      margin-bottom: 1.5rem;
    }
    .hero h1 {
      font-size: clamp(3rem, 10vw, 7rem);
      font-weight: 700;
      line-height: 0.9;
      margin-bottom: 1.5rem;
      background: linear-gradient(135deg, #fff 0%, #c4b5fd 50%, #818cf8 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    .hero p {
      font-size: 1.15rem;
      color: #94a3b8;
      max-width: 460px;
      margin: 0 auto 3rem;
      line-height: 1.7;
    }
    .tools-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1.25rem;
      max-width: 900px;
      width: 100%;
      margin-top: 1rem;
    }
    .tool-card {
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.08);
      border-radius: 16px;
      padding: 2rem 1.5rem;
      text-decoration: none;
      color: inherit;
      transition: all 0.25s ease;
      text-align: left;
      position: relative;
      overflow: hidden;
    }
    .tool-card::before {
      content: '';
      position: absolute;
      inset: 0;
      opacity: 0;
      transition: opacity 0.25s;
      border-radius: 16px;
    }
    .tool-card:hover { transform: translateY(-4px); border-color: rgba(255,255,255,0.18); }
    .tool-card:hover::before { opacity: 1; }
    .card-1::before { background: linear-gradient(135deg, rgba(124,58,237,0.12), transparent); }
    .card-2::before { background: linear-gradient(135deg, rgba(236,72,153,0.12), transparent); }
    .card-3::before { background: linear-gradient(135deg, rgba(6,182,212,0.12), transparent); }
    .card-4::before { background: linear-gradient(135deg, rgba(251,146,60,0.12), transparent); }
    .tool-icon { font-size: 2rem; margin-bottom: 1rem; display: block; }
    .tool-card h3 { font-size: 1.1rem; font-weight: 600; color: #f1f5f9; margin-bottom: 0.5rem; }
    .tool-card p { font-size: 0.875rem; color: #64748b; line-height: 1.5; margin: 0; }
    .tool-tag {
      display: inline-block;
      margin-top: 1rem;
      font-family: 'Space Mono', monospace;
      font-size: 0.65rem;
      letter-spacing: 0.1em;
      color: #a78bfa;
      text-transform: uppercase;
    }
  </style>
</head>
<body>
  <div class="hero">
    <div class="hero-gradient"></div>
    <div class="color-blobs">
      <div class="blob blob-1"></div>
      <div class="blob blob-2"></div>
      <div class="blob blob-3"></div>
    </div>
    <div class="hero-content">
      <p class="eyebrow">Color Toolkit</p>
      <h1>Chroma</h1>
      <p>Four precision tools for designers and developers who take color seriously.</p>
      <div class="tools-grid">
        <a href="pages/palette.html" class="tool-card card-1">
          <span class="tool-icon">🎨</span>
          <h3>Palette Generator</h3>
          <p>Generate harmonious color palettes from any base color instantly.</p>
          <span class="tool-tag">→ Open tool</span>
        </a>
        <a href="pages/gradient.html" class="tool-card card-2">
          <span class="tool-icon">🌈</span>
          <h3>Gradient Maker</h3>
          <p>Craft smooth gradients and copy the CSS in one click.</p>
          <span class="tool-tag">→ Open tool</span>
        </a>
        <a href="pages/converter.html" class="tool-card card-3">
          <span class="tool-icon">🔄</span>
          <h3>Color Converter</h3>
          <p>Instantly convert between HEX, RGB, HSL, and CMYK formats.</p>
          <span class="tool-tag">→ Open tool</span>
        </a>
        <a href="pages/picker.html" class="tool-card card-4">
          <span class="tool-icon">💧</span>
          <h3>Color Picker</h3>
          <p>Pick any color visually with real-time preview and copy values.</p>
          <span class="tool-tag">→ Open tool</span>
        </a>
      </div>
    </div>
  </div>
</body>
</html>
