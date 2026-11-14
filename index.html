<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BOUNCE//BACK : ACE INTERCEPTOR</title>
<style>
  :root {
    --bg-void: #03040a;
    --neon-cyan: #00f3ff;
    --neon-magenta: #ff0055;
    --neon-yellow: #ffe600;
    --neon-lime: #00ff88;
    --neon-purple: #b829ff;
    --neon-orange: #ff6a00;
    --panel-bg: rgba(7, 11, 24, 0.86);
    --font-main: 'Segoe UI', 'Orbitron', 'Rajdhani', system-ui, -apple-system, monospace, sans-serif;
  }

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    user-select: none;
    -webkit-user-select: none;
  }

  html, body {
    width: 100%;
    height: 100%;
    overflow: hidden;
    background-color: var(--bg-void);
    font-family: var(--font-main);
    color: #fff;
  }

  canvas {
    display: block;
    width: 100vw;
    height: 100vh;
    cursor: crosshair;
  }

  .crt-overlay {
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 5;
    background:
      radial-gradient(circle at center, transparent 58%, rgba(1, 2, 8, 0.84) 100%),
      repeating-linear-gradient(
        0deg,
        rgba(0, 243, 255, 0.012) 0px,
        rgba(0, 243, 255, 0.012) 1px,
        transparent 1px,
        transparent 3px
      );
  }

  #hud {
    position: fixed;
    top: 16px;
    left: 22px;
    right: 22px;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 20px;
    z-index: 10;
    pointer-events: none;
  }

  .hud-panel {
    background: var(--panel-bg);
    border: 1px solid rgba(0, 243, 255, 0.3);
    box-shadow: 0 0 24px rgba(0, 243, 255, 0.12), inset 0 0 18px rgba(0, 243, 255, 0.05);
    backdrop-filter: blur(8px);
    padding: 12px 18px;
    border-radius: 8px;
    position: relative;
  }

  .hud-panel::before {
    content: '';
    position: absolute;
    top: -1px;
    left: 12px;
    width: 36px;
    height: 2px;
    background: var(--neon-cyan);
    box-shadow: 0 0 8px var(--neon-cyan);
  }

  .bars-container {
    display: flex;
    flex-direction: column;
    gap: 10px;
    flex: 1;
    max-width: 440px;
  }

  .pilot-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 11px;
    letter-spacing: 2px;
    color: rgba(255, 255, 255, 0.65);
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
    padding-bottom: 5px;
  }

  .pilot-header strong {
    color: var(--neon-cyan);
    font-weight: 900;
    text-shadow: 0 0 8px rgba(0, 243, 255, 0.6);
  }

  .bar-group {
    display: flex;
    flex-direction: column;
    gap: 4px;
  }

  .bar-label {
    display: flex;
    justify-content: space-between;
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 2px;
    text-transform: uppercase;
  }

  .label-hp { color: var(--neon-magenta); text-shadow: 0 0 8px var(--neon-magenta); }
  .label-bounce { color: var(--neon-cyan); text-shadow: 0 0 8px var(--neon-cyan); }

  .bar-track {
    position: relative;
    width: 100%;
    height: 14px;
    background: rgba(255, 255, 255, 0.05);
    border: 1px solid rgba(255, 255, 255, 0.18);
    border-radius: 3px;
    overflow: hidden;
  }

  .bar-fill-ghost {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    background: rgba(255, 255, 255, 0.45);
    transition: width 0.35s ease-out;
  }

  .bar-fill {
    position: relative;
    height: 100%;
    transition: width 0.08s linear;
  }

  #hp-fill {
    background: linear-gradient(90deg, #ff0040, #ff0088);
    box-shadow: 0 0 14px var(--neon-magenta);
    width: 100%;
  }

  #bounce-fill {
    background: linear-gradient(90deg, #0077ff, #00f3ff, #ffe600);
    box-shadow: 0 0 16px var(--neon-cyan);
    width: 0%;
  }

  .bounce-ready #bounce-fill {
    background: linear-gradient(90deg, #00f3ff, #ffe600, #ff0055);
    animation: pulseGlow 0.45s infinite alternate;
  }

  @keyframes pulseGlow {
    from { filter: brightness(1); box-shadow: 0 0 12px #00f3ff; }
    to { filter: brightness(1.45); box-shadow: 0 0 25px #ffe600; }
  }

  .space-prompt {
    margin-top: 2px;
    font-size: 10px;
    letter-spacing: 1.4px;
    color: rgba(255, 255, 255, 0.5);
    display: flex;
    justify-content: space-between;
    font-weight: 700;
  }

  .space-prompt.active {
    color: var(--neon-yellow);
    text-shadow: 0 0 10px var(--neon-yellow);
    animation: blinkText 0.45s infinite alternate;
  }

  @keyframes blinkText {
    from { opacity: 0.68; }
    to { opacity: 1; }
  }

  .center-hud-col {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
  }

  .wave-panel {
    text-align: center;
    min-width: 190px;
    padding: 10px 22px;
    border-color: rgba(184, 41, 255, 0.45);
  }

  .wave-title {
    font-size: 10px;
    letter-spacing: 3px;
    color: #c89eff;
    text-transform: uppercase;
  }

  .wave-num {
    font-size: 28px;
    font-weight: 900;
    letter-spacing: 3px;
    color: #fff;
    text-shadow: 0 0 14px var(--neon-purple);
  }

  /* Boss Bar */
  #boss-hud {
    min-width: 340px;
    padding: 8px 14px;
    border-color: rgba(255, 0, 85, 0.6);
    box-shadow: 0 0 25px rgba(255, 0, 85, 0.25);
    transition: opacity 0.25s ease, transform 0.25s ease;
  }

  #boss-hud.hidden {
    opacity: 0;
    transform: translateY(-10px);
    pointer-events: none;
  }

  .boss-label {
    display: flex;
    justify-content: space-between;
    font-size: 10px;
    font-weight: 900;
    letter-spacing: 2px;
    color: var(--neon-magenta);
    margin-bottom: 4px;
    text-shadow: 0 0 8px var(--neon-magenta);
  }

  #boss-fill {
    background: linear-gradient(90deg, #ff0055, #ff6a00, #ffe600);
    box-shadow: 0 0 14px var(--neon-magenta);
    width: 100%;
  }

  .score-panel {
    text-align: right;
    min-width: 250px;
  }

  .score-row {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 16px;
  }

  .score-label {
    font-size: 11px;
    letter-spacing: 2px;
    color: rgba(255, 255, 255, 0.6);
  }

  .score-value {
    font-size: 26px;
    font-weight: 900;
    color: var(--neon-cyan);
    text-shadow: 0 0 12px var(--neon-cyan);
    font-variant-numeric: tabular-nums;
  }

  .sub-stats {
    margin-top: 6px;
    display: flex;
    justify-content: space-between;
    font-size: 11px;
    letter-spacing: 1.5px;
    color: var(--neon-yellow);
    font-weight: 700;
  }

  .buff-row {
    margin-top: 6px;
    display: flex;
    justify-content: flex-end;
    gap: 6px;
    min-height: 18px;
  }

  .buff-pill {
    font-size: 9px;
    font-weight: 900;
    letter-spacing: 1.2px;
    padding: 2px 7px;
    border-radius: 3px;
    text-transform: uppercase;
  }

  .buff-shield {
    background: rgba(0, 243, 255, 0.2);
    border: 1px solid var(--neon-cyan);
    color: var(--neon-cyan);
  }

  .buff-overclock {
    background: rgba(255, 230, 0, 0.2);
    border: 1px solid var(--neon-yellow);
    color: var(--neon-yellow);
  }

  .bottom-bar {
    position: fixed;
    bottom: 16px;
    right: 20px;
    left: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 20;
    pointer-events: none;
  }

  .gamepad-status {
    background: rgba(7, 11, 24, 0.85);
    border: 1px solid rgba(255, 255, 255, 0.15);
    color: rgba(255, 255, 255, 0.5);
    padding: 7px 12px;
    font-size: 10px;
    font-weight: 800;
    letter-spacing: 1.5px;
    border-radius: 6px;
  }

  .gamepad-status.connected {
    border-color: var(--neon-lime);
    color: var(--neon-lime);
    box-shadow: 0 0 12px rgba(0, 255, 136, 0.25);
  }

  .hud-btns {
    display: flex;
    gap: 10px;
    pointer-events: auto;
  }

  .hud-btn {
    background: rgba(7, 11, 24, 0.88);
    border: 1px solid rgba(0, 243, 255, 0.35);
    color: var(--neon-cyan);
    padding: 8px 14px;
    font-family: var(--font-main);
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 1.5px;
    border-radius: 6px;
    cursor: pointer;
    transition: all 0.15s ease;
  }

  .hud-btn:hover {
    background: rgba(0, 243, 255, 0.15);
    box-shadow: 0 0 15px rgba(0, 243, 255, 0.4);
  }

  .overlay-screen {
    position: fixed;
    inset: 0;
    z-index: 30;
    display: flex;
    align-items: center;
    justify-content: center;
    background: radial-gradient(circle at center, rgba(8, 12, 28, 0.74) 0%, rgba(2, 3, 8, 0.95) 100%);
    backdrop-filter: blur(10px);
    padding: 20px;
    transition: opacity 0.25s ease;
  }

  .overlay-screen.hidden {
    opacity: 0;
    pointer-events: none;
  }

  .modal-wide {
    background: rgba(8, 12, 26, 0.95);
    border: 1px solid rgba(0, 243, 255, 0.55);
    box-shadow:
      0 0 50px rgba(0, 243, 255, 0.2),
      inset 0 0 35px rgba(0, 243, 255, 0.06);
    border-radius: 14px;
    padding: 30px 34px;
    max-width: 980px;
    width: 100%;
    display: grid;
    grid-template-columns: 1.3fr 0.9fr;
    gap: 28px;
    position: relative;
  }

  .modal-col-left {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    text-align: left;
  }

  .modal-col-right {
    background: rgba(3, 5, 14, 0.78);
    border: 1px solid rgba(255, 255, 255, 0.12);
    border-radius: 10px;
    padding: 20px;
    display: flex;
    flex-direction: column;
  }

  .game-logo {
    font-size: 44px;
    font-weight: 900;
    letter-spacing: 5px;
    line-height: 1;
    margin-bottom: 6px;
    color: #fff;
    text-shadow:
      -3px 0 0 var(--neon-magenta),
      3px 0 0 var(--neon-cyan),
      0 0 22px rgba(0, 243, 255, 0.65);
  }

  .game-logo span {
    color: var(--neon-yellow);
    text-shadow: 0 0 18px var(--neon-yellow);
  }

  .tagline {
    font-size: 11px;
    letter-spacing: 3.5px;
    text-transform: uppercase;
    color: var(--neon-cyan);
    margin-bottom: 16px;
    font-weight: 800;
  }

  .callsign-box {
    margin-bottom: 16px;
    background: rgba(0, 243, 255, 0.05);
    border: 1px solid rgba(0, 243, 255, 0.35);
    border-radius: 8px;
    padding: 10px 14px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .callsign-label {
    font-size: 11px;
    font-weight: 900;
    letter-spacing: 2px;
    color: var(--neon-cyan);
    white-space: nowrap;
  }

  .callsign-input {
    pointer-events: auto;
    user-select: text;
    -webkit-user-select: text;
    flex: 1;
    background: rgba(0, 0, 0, 0.55);
    border: 1px solid rgba(255, 255, 255, 0.22);
    border-radius: 5px;
    padding: 8px 12px;
    color: var(--neon-yellow);
    font-family: var(--font-main);
    font-size: 15px;
    font-weight: 900;
    letter-spacing: 2.5px;
    text-transform: uppercase;
    outline: none;
    transition: all 0.15s ease;
  }

  .callsign-input:focus {
    border-color: var(--neon-yellow);
    box-shadow: 0 0 14px rgba(255, 230, 0, 0.35);
  }

  .section-head {
    font-size: 11px;
    font-weight: 900;
    letter-spacing: 2.5px;
    color: rgba(255, 255, 255, 0.55);
    text-transform: uppercase;
    margin-bottom: 8px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .section-head::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, rgba(0, 243, 255, 0.35), transparent);
  }

  .objectives-list {
    display: flex;
    flex-direction: column;
    gap: 7px;
    margin-bottom: 14px;
  }

  .obj-card {
    background: rgba(255, 255, 255, 0.03);
    border-left: 3px solid var(--neon-cyan);
    padding: 8px 12px;
    border-radius: 0 6px 6px 0;
    font-size: 12px;
    line-height: 1.38;
    color: rgba(255, 255, 255, 0.85);
  }

  .obj-card.magenta { border-left-color: var(--neon-magenta); }
  .obj-card.yellow { border-left-color: var(--neon-yellow); }

  .obj-card strong {
    color: #fff;
    letter-spacing: 0.5px;
  }

  .controls-strip {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 8px;
    margin-bottom: 18px;
  }

  .ctrl-badge {
    background: rgba(255, 255, 255, 0.035);
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 6px;
    padding: 9px 6px;
    text-align: center;
  }

  .key-pill {
    display: inline-block;
    background: rgba(0, 243, 255, 0.14);
    border: 1px solid var(--neon-cyan);
    color: var(--neon-cyan);
    font-size: 10px;
    font-weight: 900;
    letter-spacing: 1.2px;
    padding: 3px 7px;
    border-radius: 4px;
    margin-bottom: 5px;
    box-shadow: 0 0 10px rgba(0, 243, 255, 0.2);
  }

  .key-pill.space {
    background: rgba(255, 230, 0, 0.15);
    border-color: var(--neon-yellow);
    color: var(--neon-yellow);
    box-shadow: 0 0 10px rgba(255, 230, 0, 0.25);
  }

  .key-pill.rail {
    background: rgba(255, 0, 85, 0.15);
    border-color: var(--neon-magenta);
    color: var(--neon-magenta);
    box-shadow: 0 0 10px rgba(255, 0, 85, 0.25);
  }

  .ctrl-desc {
    font-size: 10.5px;
    color: rgba(255, 255, 255, 0.72);
    line-height: 1.25;
  }

  .neon-btn {
    pointer-events: auto;
    width: 100%;
    background: linear-gradient(90deg, rgba(0, 243, 255, 0.15), rgba(0, 255, 136, 0.15));
    color: #fff;
    border: 2px solid var(--neon-cyan);
    padding: 14px 28px;
    font-size: 16px;
    font-weight: 900;
    letter-spacing: 4px;
    text-transform: uppercase;
    border-radius: 7px;
    cursor: pointer;
    box-shadow: 0 0 22px rgba(0, 243, 255, 0.3), inset 0 0 12px rgba(0, 243, 255, 0.2);
    transition: all 0.18s ease;
    font-family: var(--font-main);
  }

  .neon-btn:hover {
    background: var(--neon-cyan);
    color: #03040a;
    box-shadow: 0 0 35px var(--neon-cyan);
    transform: translateY(-2px);
  }

  .lb-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 12px;
    padding-bottom: 8px;
    border-bottom: 1px solid rgba(0, 243, 255, 0.25);
  }

  .lb-title {
    font-size: 14px;
    font-weight: 900;
    letter-spacing: 2.5px;
    color: var(--neon-yellow);
    text-shadow: 0 0 10px rgba(255, 230, 0, 0.45);
  }

  .lb-sub {
    font-size: 10px;
    letter-spacing: 1.5px;
    color: rgba(255, 255, 255, 0.5);
  }

  .lb-list {
    display: flex;
    flex-direction: column;
    gap: 6px;
    flex: 1;
    overflow-y: auto;
  }

  .lb-row {
    display: grid;
    grid-template-columns: 34px 1fr 64px 86px;
    align-items: center;
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(255, 255, 255, 0.07);
    padding: 8px 10px;
    border-radius: 5px;
    font-size: 12px;
  }

  .lb-row.top-1 {
    background: linear-gradient(90deg, rgba(255, 230, 0, 0.16), rgba(255, 230, 0, 0.03));
    border-color: rgba(255, 230, 0, 0.5);
  }

  .lb-row.current-run {
    border-color: var(--neon-cyan);
    box-shadow: 0 0 12px rgba(0, 243, 255, 0.35);
    background: rgba(0, 243, 255, 0.12);
  }

  .lb-rank {
    font-weight: 900;
    color: rgba(255, 255, 255, 0.5);
  }

  .lb-row.top-1 .lb-rank { color: var(--neon-yellow); }

  .lb-name {
    font-weight: 800;
    letter-spacing: 1.5px;
    color: #fff;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }

  .lb-wave {
    font-size: 11px;
    color: #c89eff;
    text-align: center;
    font-weight: 700;
  }

  .lb-score {
    font-weight: 900;
    color: var(--neon-cyan);
    text-align: right;
    font-variant-numeric: tabular-nums;
  }

  .lb-clear-btn {
    pointer-events: auto;
    margin-top: 10px;
    background: transparent;
    border: 1px solid rgba(255, 255, 255, 0.15);
    color: rgba(255, 255, 255, 0.45);
    font-size: 10px;
    letter-spacing: 1.5px;
    padding: 6px;
    border-radius: 4px;
    cursor: pointer;
    font-family: var(--font-main);
  }

  .lb-clear-btn:hover {
    color: var(--neon-magenta);
    border-color: var(--neon-magenta);
  }

  .stats-summary {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
    margin: 14px 0 20px;
  }

  .stat-box {
    background: rgba(255, 255, 255, 0.035);
    border: 1px solid rgba(255, 255, 255, 0.12);
    padding: 12px;
    border-radius: 8px;
    text-align: center;
  }

  .stat-box .lbl {
    font-size: 10px;
    letter-spacing: 2px;
    color: rgba(255, 255, 255, 0.55);
    text-transform: uppercase;
  }

  .stat-box .val {
    font-size: 24px;
    font-weight: 900;
    margin-top: 4px;
    color: var(--neon-cyan);
    text-shadow: 0 0 10px rgba(0, 243, 255, 0.5);
  }

  @media (max-width: 860px) {
    .modal-wide {
      grid-template-columns: 1fr;
      max-height: 92vh;
      overflow-y: auto;
      padding: 22px;
    }
    .controls-strip {
      grid-template-columns: repeat(2, 1fr);
    }
    #hud {
      flex-direction: column;
      align-items: stretch;
      gap: 8px;
    }
    .bars-container { max-width: 100%; }
  }
</style>
</head>
<body>

<div class="crt-overlay"></div>

<!-- FLIGHT HUD -->
<div id="hud">
  <div class="hud-panel bars-container" id="bars-panel">
    <div class="pilot-header">
      <span>CALLSIGN: <strong id="hud-pilot-name">MAVERICK</strong></span>
      <span>AIRFRAME: <strong>VX-9 VALKYRIE</strong></span>
    </div>

    <div class="bar-group">
      <div class="bar-label">
        <span class="label-hp">AIRFRAME INTEGRITY</span>
        <span id="hp-text">100 / 100</span>
      </div>
      <div class="bar-track">
        <div class="bar-fill-ghost" id="hp-ghost" style="width: 100%;"></div>
        <div class="bar-fill" id="hp-fill"></div>
      </div>
    </div>

    <div class="bar-group">
      <div class="bar-label">
        <span class="label-bounce">KINETIC BOUNCE // CORE</span>
        <span id="bounce-text">0%</span>
      </div>
      <div class="bar-track">
        <div class="bar-fill" id="bounce-fill"></div>
      </div>
      <div class="space-prompt" id="space-prompt">
        <span id="nova-status-text">ABSORB DAMAGE OR CORES [25% MIN]</span>
        <span>[SHIFT / R-CLICK] RAILGUN (15%)</span>
      </div>
    </div>
  </div>

  <div class="center-hud-col">
    <div class="hud-panel wave-panel">
      <div class="wave-title" id="wave-label">AIRSPACE WAVE</div>
      <div class="wave-num" id="wave-text">01</div>
    </div>

    <div class="hud-panel hidden" id="boss-hud">
      <div class="boss-label">
        <span id="boss-name">AETHER-X DREADNOUGHT</span>
        <span id="boss-hp-pct">100%</span>
      </div>
      <div class="bar-track" style="height: 10px;">
        <div class="bar-fill" id="boss-fill"></div>
      </div>
    </div>
  </div>

  <div class="hud-panel score-panel">
    <div class="score-row">
      <span class="score-label">SCORE</span>
      <span class="score-value" id="score-text">0</span>
    </div>
    <div class="sub-stats">
      <span id="combo-text">MULT x1.0</span>
      <span id="best-text">TOP ACE: 0</span>
    </div>
    <div class="buff-row" id="buff-row"></div>
  </div>
</div>

<div class="bottom-bar">
  <div class="gamepad-status" id="gamepad-indicator">GAMEPAD: STANDBY (PLUG & PLAY)</div>
  <div class="hud-btns">
    <button class="hud-btn" id="pause-btn">PAUSE [P]</button>
    <button class="hud-btn" id="audio-btn">SFX: ON</button>
  </div>
</div>

<!-- START & BRIEFING OVERLAY -->
<div class="overlay-screen" id="start-screen">
  <div class="modal-wide">
    <div class="modal-col-left">
      <div>
        <div class="game-logo">BOUNCE<span>//</span>BACK</div>
        <div class="tagline">Tactical Jet Interceptor Arena // v2.0</div>

        <div class="callsign-box">
          <label class="callsign-label" for="pilot-input">PILOT CALLSIGN //</label>
          <input
            type="text"
            id="pilot-input"
            class="callsign-input"
            maxlength="12"
            placeholder="ENTER NAME..."
            autocomplete="off"
          />
        </div>

        <div class="section-head">TACTICAL OBJECTIVES</div>
        <div class="objectives-list">
          <div class="obj-card">
            <strong>01 // INTERCEPT SQUADRONS & BOSS CARRIERS:</strong> Dogfight hostile Vipers, Su-47 Berkuts, Stealth Wraiths, and Boss Dreadnoughts (every 3 waves).
          </div>
          <div class="obj-card magenta">
            <strong>02 // PAIN IS KINETIC FUEL:</strong> Enemy collisions & flak knock your jet back and supercharge your <strong>BOUNCE CORE</strong>. Grab <strong>Aegis Shields</strong> & <strong>Overclock</strong> pods!
          </div>
          <div class="obj-card yellow">
            <strong>03 // NOVA & RAILGUN LANCE:</strong> Spend <strong>15% Core</strong> for a piercing Railgun beam, or unleash <strong>25%–100% Core</strong> for an EMP Nova + Hull Repair!
          </div>
        </div>

        <div class="section-head">FLIGHT & WEAPON CONTROLS (KEYBOARD / GAMEPAD)</div>
        <div class="controls-strip">
          <div class="ctrl-badge">
            <div class="key-pill">WASD / L-STICK</div>
            <div class="ctrl-desc">Vector Thrusters & Banking</div>
          </div>
          <div class="ctrl-badge">
            <div class="key-pill">MOUSE / R-STICK</div>
            <div class="ctrl-desc">Vulcan Cannon Aim & Auto-Lock</div>
          </div>
          <div class="ctrl-badge">
            <div class="key-pill rail">R-CLICK / SHIFT</div>
            <div class="ctrl-desc">EMP Railgun Lance (15% Core)</div>
          </div>
          <div class="ctrl-badge">
            <div class="key-pill space">SPACE / BTN-A</div>
            <div class="ctrl-desc">BOUNCE//BACK Nova + Heal</div>
          </div>
        </div>
      </div>

      <button class="neon-btn" id="start-btn">SCRAMBLE INTERCEPTOR // LAUNCH</button>
    </div>

    <div class="modal-col-right">
      <div class="lb-header">
        <span class="lb-title">TOP ACES // LEADERBOARD</span>
        <span class="lb-sub">HALL OF FAME</span>
      </div>
      <div class="lb-list" id="start-leaderboard"></div>
      <button class="lb-clear-btn" id="reset-lb-btn">RESET LOCAL RECORDS</button>
    </div>
  </div>
</div>

<!-- GAME OVER OVERLAY -->
<div class="overlay-screen hidden" id="gameover-screen">
  <div class="modal-wide">
    <div class="modal-col-left">
      <div>
        <div class="game-logo" style="font-size: 38px;">JET<span>//</span>DOWNED</div>
        <div class="tagline" style="color: var(--neon-magenta);">Blackbox Flight Telemetry Recorded</div>

        <div class="stats-summary">
          <div class="stat-box">
            <div class="lbl">PILOT CALLSIGN</div>
            <div class="val" id="final-pilot" style="color: var(--neon-yellow);">ACE</div>
          </div>
          <div class="stat-box">
            <div class="lbl">FINAL SCORE</div>
            <div class="val" id="final-score">0</div>
          </div>
          <div class="stat-box">
            <div class="lbl">WAVE REACHED</div>
            <div class="val" id="final-wave">01</div>
          </div>
          <div class="stat-box">
            <div class="lbl">BOGEYS SPLASHED</div>
            <div class="val" id="final-kills">0</div>
          </div>
        </div>
      </div>

      <button class="neon-btn" id="restart-btn">BOUNCE // BACK (SORTIE AGAIN)</button>
    </div>

    <div class="modal-col-right">
      <div class="lb-header">
        <span class="lb-title">TOP ACES // STANDINGS</span>
        <span class="lb-sub">UPDATED</span>
      </div>
      <div class="lb-list" id="gameover-leaderboard"></div>
    </div>
  </div>
</div>

<canvas id="gameCanvas"></canvas>

<script>
(() => {
  'use strict';

  const canvas = document.getElementById('gameCanvas');
  const ctx = canvas.getContext('2d', { alpha: false });

  // Cache computed font once at startup to avoid layout thrashing in render loop
  const FONT_FAMILY = getComputedStyle(document.body).fontFamily;

  // Cached DOM References
  const UI = {
    hpFill: document.getElementById('hp-fill'),
    hpGhost: document.getElementById('hp-ghost'),
    hpText: document.getElementById('hp-text'),
    bounceFill: document.getElementById('bounce-fill'),
    bounceText: document.getElementById('bounce-text'),
    barsPanel: document.getElementById('bars-panel'),
    spacePrompt: document.getElementById('space-prompt'),
    novaStatusText: document.getElementById('nova-status-text'),
    waveLabel: document.getElementById('wave-label'),
    waveText: document.getElementById('wave-text'),
    bossHud: document.getElementById('boss-hud'),
    bossName: document.getElementById('boss-name'),
    bossHpPct: document.getElementById('boss-hp-pct'),
    bossFill: document.getElementById('boss-fill'),
    scoreText: document.getElementById('score-text'),
    comboText: document.getElementById('combo-text'),
    bestText: document.getElementById('best-text'),
    buffRow: document.getElementById('buff-row'),
    hudPilotName: document.getElementById('hud-pilot-name'),
    gamepadIndicator: document.getElementById('gamepad-indicator'),
    pilotInput: document.getElementById('pilot-input'),
    startScreen: document.getElementById('start-screen'),
    gameoverScreen: document.getElementById('gameover-screen'),
    startBtn: document.getElementById('start-btn'),
    restartBtn: document.getElementById('restart-btn'),
    resetLbBtn: document.getElementById('reset-lb-btn'),
    pauseBtn: document.getElementById('pause-btn'),
    audioBtn: document.getElementById('audio-btn'),
    startLb: document.getElementById('start-leaderboard'),
    gameoverLb: document.getElementById('gameover-leaderboard'),
    finalPilot: document.getElementById('final-pilot'),
    finalScore: document.getElementById('final-score'),
    finalWave: document.getElementById('final-wave'),
    finalKills: document.getElementById('final-kills')
  };

  // --- O(1) SWAP-AND-POP ARRAY REMOVAL (Eliminates O(N) splice GC stalls) ---
  function removeAtSwap(arr, index) {
    const lastIdx = arr.length - 1;
    if (index !== lastIdx) {
      arr[index] = arr[lastIdx];
    }
    arr.pop();
  }

  function rand(min, max) {
    return Math.random() * (max - min) + min;
  }

  function moveToward(current, target, maxDelta) {
    if (Math.abs(target - current) <= maxDelta) return target;
    return current + Math.sign(target - current) * maxDelta;
  }

  function angleDiff(a, b) {
    let d = (b - a) % (Math.PI * 2);
    if (d > Math.PI) d -= Math.PI * 2;
    if (d < -Math.PI) d += Math.PI * 2;
    return d;
  }

  // --- VIEWPORT & PARALLAX STARFIELD ---
  let W = window.innerWidth;
  let H = window.innerHeight;
  let stars = [];

  function initStars() {
    stars = [];
    for (let i = 0; i < 115; i++) {
      stars.push({
        x: Math.random() * W,
        y: Math.random() * H,
        size: Math.random() * 2 + 0.6,
        depth: Math.random() * 0.65 + 0.15,
        alpha: Math.random() * 0.65 + 0.25
      });
    }
  }

  function resize() {
    W = canvas.width = window.innerWidth;
    H = canvas.height = window.innerHeight;
    initStars();
  }
  window.addEventListener('resize', resize);
  resize();

  // --- LEADERBOARD STORAGE (Cached in memory during gameplay) ---
  const LB_KEY = 'bounceback_aces_leaderboard_v2';
  const PILOT_KEY = 'bounceback_last_callsign';
  const defaultLeaderboard = [
    { name: 'VORTEX', score: 22400, wave: 8 },
    { name: 'CIPHER', score: 16800, wave: 6 },
    { name: 'VALKYRIE', score: 11900, wave: 5 },
    { name: 'STRIKER', score: 7800, wave: 4 },
    { name: 'ROOKIE', score: 4200, wave: 2 }
  ];

  let cachedTopScore = 22400;
  UI.pilotInput.value = localStorage.getItem(PILOT_KEY) || '';

  function getLeaderboard() {
    try {
      const raw = localStorage.getItem(LB_KEY);
      if (!raw) {
        localStorage.setItem(LB_KEY, JSON.stringify(defaultLeaderboard));
        return [...defaultLeaderboard];
      }
      return JSON.parse(raw);
    } catch {
      return [...defaultLeaderboard];
    }
  }

  function saveScoreToLeaderboard(name, finalScore, finalWave) {
    const list = getLeaderboard();
    const entry = {
      name: (name || 'ACE PILOT').toUpperCase().slice(0, 12),
      score: finalScore,
      wave: finalWave,
      isCurrent: true
    };
    list.forEach(item => delete item.isCurrent);
    list.push(entry);
    list.sort((a, b) => b.score - a.score);
    const trimmed = list.slice(0, 8);
    try {
      localStorage.setItem(LB_KEY, JSON.stringify(trimmed));
    } catch {}
    return trimmed;
  }

  function escapeHtml(str) {
    return String(str).replace(/[&<>"']/g, s => ({
      '&': '&amp;', '<': '&lt;', '>': '&gt;', '"': '&quot;', "'": '&#39;'
    }[s]));
  }

  function renderLeaderboardUI() {
    const list = getLeaderboard();
    cachedTopScore = list.length > 0 ? list[0].score : 0;
    UI.bestText.textContent = `TOP ACE: ${cachedTopScore.toLocaleString()}`;

    const html = list.map((item, idx) => {
      const classes = ['lb-row'];
      if (idx === 0) classes.push('top-1');
      if (item.isCurrent) classes.push('current-run');
      return `
        <div class="${classes.join(' ')}">
          <span class="lb-rank">#${idx + 1}</span>
          <span class="lb-name">${escapeHtml(item.name)}</span>
          <span class="lb-wave">W-${String(item.wave).padStart(2, '0')}</span>
          <span class="lb-score">${Number(item.score).toLocaleString()}</span>
        </div>
      `;
    }).join('');

    UI.startLb.innerHTML = html;
    UI.gameoverLb.innerHTML = html;
  }

  UI.resetLbBtn.addEventListener('click', () => {
    localStorage.setItem(LB_KEY, JSON.stringify(defaultLeaderboard));
    renderLeaderboardUI();
  });

  renderLeaderboardUI();

  // --- SYNTHESIZED WEB AUDIO ENGINE ---
  class SoundEngine {
    constructor() {
      this.ctx = null;
      this.enabled = true;
    }
    init() {
      if (!this.ctx) {
        const AudioCtx = window.AudioContext || window.webkitAudioContext;
        if (AudioCtx) this.ctx = new AudioCtx();
      }
      if (this.ctx && this.ctx.state === 'suspended') {
        this.ctx.resume();
      }
    }
    play(type, power = 1) {
      if (!this.enabled || !this.ctx) return;
      const now = this.ctx.currentTime;
      const osc = this.ctx.createOscillator();
      const gain = this.ctx.createGain();
      osc.connect(gain);
      gain.connect(this.ctx.destination);

      if (type === 'shoot') {
        osc.type = 'triangle';
        osc.frequency.setValueAtTime(610, now);
        osc.frequency.exponentialRampToValueAtTime(155, now + 0.055);
        gain.gain.setValueAtTime(0.065, now);
        gain.gain.exponentialRampToValueAtTime(0.001, now + 0.055);
        osc.start(now);
        osc.stop(now + 0.06);
      } else if (type === 'railgun') {
        osc.type = 'sawtooth';
        osc.frequency.setValueAtTime(920, now);
        osc.frequency.exponentialRampToValueAtTime(65, now + 0.28);
        gain.gain.setValueAtTime(0.22, now);
        gain.gain.exponentialRampToValueAtTime(0.001, now + 0.28);
        osc.start(now);
        osc.stop(now + 0.29);
      } else if (type === 'hurt') {
        osc.type = 'sawtooth';
        osc.frequency.setValueAtTime(180, now);
        osc.frequency.exponentialRampToValueAtTime(45, now + 0.22);
        gain.gain.setValueAtTime(0.24, now);
        gain.gain.exponentialRampToValueAtTime(0.001, now + 0.22);
        osc.start(now);
        osc.stop(now + 0.23);

        const osc2 = this.ctx.createOscillator();
        const g2 = this.ctx.createGain();
        osc2.connect(g2);
        g2.connect(this.ctx.destination);
        osc2.type = 'sine';
        osc2.frequency.setValueAtTime(460, now + 0.03);
        osc2.frequency.exponentialRampToValueAtTime(920, now + 0.18);
        g2.gain.setValueAtTime(0.11, now + 0.03);
        g2.gain.exponentialRampToValueAtTime(0.001, now + 0.19);
        osc2.start(now + 0.03);
        osc2.stop(now + 0.2);
      } else if (type === 'bounceNova') {
        osc.type = 'sawtooth';
        osc.frequency.setValueAtTime(160 * (0.8 + power * 0.4), now);
        osc.frequency.exponentialRampToValueAtTime(26, now + 0.55);
        gain.gain.setValueAtTime(0.32, now);
        gain.gain.exponentialRampToValueAtTime(0.001, now + 0.55);
        osc.start(now);
        osc.stop(now + 0.56);

        const osc2 = this.ctx.createOscillator();
        const g2 = this.ctx.createGain();
        osc2.connect(g2);
        g2.connect(this.ctx.destination);
        osc2.type = 'square';
        osc2.frequency.setValueAtTime(280, now);
        osc2.frequency.exponentialRampToValueAtTime(1180, now + 0.36);
        g2.gain.setValueAtTime(0.15, now);
        g2.gain.exponentialRampToValueAtTime(0.001, now + 0.37);
        osc2.start(now);
        osc2.stop(now + 0.38);
      } else if (type === 'kill') {
        osc.type = 'square';
        osc.frequency.setValueAtTime(250, now);
        osc.frequency.exponentialRampToValueAtTime(70, now + 0.12);
        gain.gain.setValueAtTime(0.11, now);
        gain.gain.exponentialRampToValueAtTime(0.001, now + 0.12);
        osc.start(now);
        osc.stop(now + 0.13);
      } else if (type === 'pickup') {
        osc.type = 'sine';
        osc.frequency.setValueAtTime(600, now);
        osc.frequency.exponentialRampToValueAtTime(1180, now + 0.1);
        gain.gain.setValueAtTime(0.11, now);
        gain.gain.exponentialRampToValueAtTime(0.001, now + 0.1);
        osc.start(now);
        osc.stop(now + 0.11);
      } else if (type === 'ricochet') {
        osc.type = 'triangle';
        osc.frequency.setValueAtTime(740, now);
        osc.frequency.exponentialRampToValueAtTime(1280, now + 0.045);
        gain.gain.setValueAtTime(0.055, now);
        gain.gain.exponentialRampToValueAtTime(0.001, now + 0.045);
        osc.start(now);
        osc.stop(now + 0.05);
      }
    }
  }

  const sfx = new SoundEngine();
  UI.audioBtn.addEventListener('click', () => {
    sfx.init();
    sfx.enabled = !sfx.enabled;
    UI.audioBtn.textContent = `SFX: ${sfx.enabled ? 'ON' : 'OFF'}`;
  });

  // --- UNIFIED INPUT (KEYBOARD + MOUSE + HTML5 GAMEPAD) ---
  const keys = {};
  const mouse = { x: W / 2, y: H / 2, down: false, rightDown: false, active: false };
  const gamepadState = {
    connected: false,
    moveX: 0,
    moveY: 0,
    aimX: 0,
    aimY: 0,
    aimActive: false,
    novaPressedLast: false,
    railPressedLast: false
  };

  window.addEventListener('gamepadconnected', (e) => {
    gamepadState.connected = true;
    UI.gamepadIndicator.classList.add('connected');
    UI.gamepadIndicator.textContent = `GAMEPAD ACTIVE: ${e.gamepad.id.slice(0, 22).toUpperCase()}`;
  });

  window.addEventListener('gamepaddisconnected', () => {
    gamepadState.connected = false;
    UI.gamepadIndicator.classList.remove('connected');
    UI.gamepadIndicator.textContent = 'GAMEPAD: STANDBY (PLUG & PLAY)';
  });

  function pollGamepad() {
    if (!navigator.getGamepads) return;
    const pads = navigator.getGamepads();
    const gp = pads && (pads[0] || pads[1] || pads[2] || pads[3]);
    if (!gp) return;

    if (!gamepadState.connected) {
      gamepadState.connected = true;
      UI.gamepadIndicator.classList.add('connected');
      UI.gamepadIndicator.textContent = 'GAMEPAD ACTIVE // TWIN-STICK MODE';
    }

    const deadzone = 0.18;
    const lx = gp.axes[0] || 0;
    const ly = gp.axes[1] || 0;
    gamepadState.moveX = Math.abs(lx) > deadzone ? lx : 0;
    gamepadState.moveY = Math.abs(ly) > deadzone ? ly : 0;

    const rx = gp.axes[2] || 0;
    const ry = gp.axes[3] || 0;
    if (Math.hypot(rx, ry) > deadzone) {
      gamepadState.aimX = rx;
      gamepadState.aimY = ry;
      gamepadState.aimActive = true;
      mouse.active = false;
    } else {
      gamepadState.aimActive = false;
    }

    // Button 0 (A/Cross) or Button 4 (LB) -> Bounce Nova
    const novaBtn = Boolean((gp.buttons[0] && gp.buttons[0].pressed) || (gp.buttons[4] && gp.buttons[4].pressed));
    if (novaBtn && !gamepadState.novaPressedLast) {
      if (gameState === 'PLAYING') triggerBounceBack();
      else if (gameState === 'START' || gameState === 'GAMEOVER') startGame();
    }
    gamepadState.novaPressedLast = novaBtn;

    // Button 6 (LT) or Button 5 (RB) -> Railgun Lance
    const railBtn = Boolean((gp.buttons[6] && gp.buttons[6].pressed) || (gp.buttons[5] && gp.buttons[5].pressed));
    if (railBtn && !gamepadState.railPressedLast && gameState === 'PLAYING') {
      fireRailgunLance();
    }
    gamepadState.railPressedLast = railBtn;
  }

  window.addEventListener('keydown', (e) => {
    if (document.activeElement === UI.pilotInput) {
      if (e.code === 'Enter') {
        UI.pilotInput.blur();
        startGame();
      }
      return;
    }

    keys[e.code] = true;
    if (e.code === 'Space') {
      e.preventDefault();
      if (gameState === 'PLAYING') triggerBounceBack();
      else if (gameState === 'START' || gameState === 'GAMEOVER') startGame();
    } else if ((e.code === 'ShiftLeft' || e.code === 'ShiftRight' || e.code === 'KeyE') && gameState === 'PLAYING') {
      e.preventDefault();
      fireRailgunLance();
    } else if (e.code === 'KeyP' || e.code === 'Escape') {
      togglePause();
    }
  });

  window.addEventListener('keyup', (e) => {
    keys[e.code] = false;
  });

  window.addEventListener('mousemove', (e) => {
    mouse.x = e.clientX;
    mouse.y = e.clientY;
    mouse.active = true;
  });

  window.addEventListener('mousedown', (e) => {
    if (e.target.tagName === 'INPUT' || e.target.tagName === 'BUTTON') return;
    sfx.init();
    if (e.button === 2) {
      if (gameState === 'PLAYING') fireRailgunLance();
    } else {
      mouse.down = true;
      mouse.active = true;
    }
  });

  window.addEventListener('contextmenu', (e) => e.preventDefault());

  window.addEventListener('mouseup', (e) => {
    if (e.button === 0) mouse.down = false;
  });

  // --- GAME STATE & ENTITY CONTAINERS ---
  let gameState = 'START'; // START, PLAYING, PAUSED, GAMEOVER
  let currentPilot = 'MAVERICK';
  let score = 0;
  let wave = 1;
  let waveKillsRequired = 8;
  let waveKills = 0;
  let totalKills = 0;
  let totalNovas = 0;
  let spawnTimer = 0;
  let multiplier = 1.0;
  let multiplierTimer = 0;
  let hitStopTimer = 0;
  let bossActive = null;

  let shakeTrauma = 0;
  let screenFlash = 0;
  let screenFlashColor = '#00f3ff';
  let gridPulse = 0;
  let hudDirty = true;

  const TRAIL_LEN = 14;
  const player = {
    x: W / 2,
    y: H / 2,
    vx: 0,
    vy: 0,
    radius: 19,
    maxSpeed: 410,
    accel: 2600,
    friction: 1700,
    hp: 100,
    maxHp: 100,
    bounceEnergy: 45,
    maxBounce: 100,
    invulnTimer: 0,
    fireTimer: 0,
    railCooldown: 0,
    angle: -Math.PI / 2,
    bankRoll: 0,
    shieldCharges: 0,
    overclockTimer: 0,
    trailTimer: 0,
    wingL: new Array(TRAIL_LEN),
    wingR: new Array(TRAIL_LEN),
    trailHead: 0,
    trailCount: 0
  };

  let bullets = [];
  let laserBeams = [];
  let enemies = [];
  let enemyProjectiles = [];
  let particles = [];
  let shockwaves = [];
  let floatingTexts = [];
  let pickups = [];
  let banners = [];

  function togglePause() {
    if (gameState === 'PLAYING') {
      gameState = 'PAUSED';
      UI.pauseBtn.textContent = 'RESUME [P]';
    } else if (gameState === 'PAUSED') {
      gameState = 'PLAYING';
      UI.pauseBtn.textContent = 'PAUSE [P]';
      lastTime = performance.now();
    }
  }
  UI.pauseBtn.addEventListener('click', togglePause);

  function addShake(amount) {
    shakeTrauma = Math.min(1.4, shakeTrauma + amount);
  }

  function addFloatingText(x, y, text, color = '#fff', size = 16) {
    if (floatingTexts.length > 40) removeAtSwap(floatingTexts, 0);
    floatingTexts.push({
      x, y,
      vx: rand(-30, 30),
      vy: rand(-95, -55),
      text, color, size,
      life: 0.85,
      maxLife: 0.85
    });
  }

  function addBanner(title, subtitle, color = '#00f3ff') {
    banners.push({ title, subtitle, color, life: 2.3, maxLife: 2.3 });
  }

  function spawnParticles(x, y, count, color, speedMin = 60, speedMax = 340, sizeMin = 2, sizeMax = 5, life = 0.52) {
    const cap = 260;
    for (let i = 0; i < count; i++) {
      if (particles.length >= cap) removeAtSwap(particles, 0);
      const ang = rand(0, Math.PI * 2);
      const spd = rand(speedMin, speedMax);
      particles.push({
        x, y,
        vx: Math.cos(ang) * spd,
        vy: Math.sin(ang) * spd,
        size: rand(sizeMin, sizeMax),
        color,
        life: rand(life * 0.6, life * 1.15),
        maxLife: life * 1.15,
        drag: 0.94
      });
    }
  }

  // --- ENEMY & BOSS DREADNOUGHT SPAWNER ---
  function spawnBossDreadnought() {
    const scaleHp = 1 + (wave - 1) * 0.28;
    const boss = {
      type: 'AETHER_CARRIER',
      isBoss: true,
      x: W / 2,
      y: -70,
      vx: 0,
      vy: 120,
      radius: 44,
      hp: Math.round(520 * scaleHp),
      maxHp: Math.round(520 * scaleHp),
      speed: 115,
      color: '#ff0055',
      damage: 26,
      scoreValue: 2000,
      bounceGrant: 65,
      angle: Math.PI / 2,
      flash: 0,
      shootTimer: 1.4,
      patternPhase: 0
    };
    enemies.push(boss);
    bossActive = boss;
    UI.bossHud.classList.remove('hidden');
    UI.bossName.textContent = `SECTOR-${String(wave).padStart(2, '0')} AETHER DREADNOUGHT`;
    addBanner('WARNING // BOSS CARRIER', 'AETHER-X DREADNOUGHT ENTERING AIRSPACE', '#ff0055');
    hudDirty = true;
  }

  function spawnEnemy() {
    const margin = 55;
    let x, y;
    if (Math.random() < 0.5) {
      x = Math.random() < 0.5 ? -margin : W + margin;
      y = rand(0, H);
    } else {
      x = rand(0, W);
      y = Math.random() < 0.5 ? -margin : H + margin;
    }

    const roll = Math.random();
    let type = 'VIPER';
    if (wave >= 2 && roll > 0.58 && roll <= 0.80) {
      type = 'BERKUT';
    } else if (wave >= 3 && roll > 0.80 && roll <= 0.93) {
      type = 'WRAITH';
    } else if (wave >= 4 && roll > 0.93) {
      type = 'VALKYRIE_BOSS';
    }

    const scaleHp = 1 + (wave - 1) * 0.16;
    const scaleSpd = 1 + Math.min(0.6, (wave - 1) * 0.04);
    const initAngle = Math.atan2(player.y - y, player.x - x);

    if (type === 'VIPER') {
      enemies.push({
        type, x, y, vx: 0, vy: 0,
        radius: 17,
        hp: 28 * scaleHp,
        maxHp: 28 * scaleHp,
        speed: rand(175, 225) * scaleSpd,
        color: '#ff0055',
        damage: 14,
        scoreValue: 100,
        bounceGrant: 34,
        angle: initAngle,
        flash: 0
      });
    } else if (type === 'BERKUT') {
      enemies.push({
        type, x, y, vx: 0, vy: 0,
        radius: 19,
        hp: 40 * scaleHp,
        maxHp: 40 * scaleHp,
        speed: 155 * scaleSpd,
        color: '#ffe600',
        damage: 18,
        scoreValue: 185,
        bounceGrant: 42,
        angle: initAngle,
        flash: 0,
        dashState: 'CHASE',
        dashTimer: rand(1.4, 2.4),
        aimAngle: initAngle
      });
    } else if (type === 'WRAITH') {
      enemies.push({
        type, x, y, vx: 0, vy: 0,
        radius: 20,
        hp: 45 * scaleHp,
        maxHp: 45 * scaleHp,
        speed: 160 * scaleSpd,
        color: '#ff6a00',
        damage: 15,
        scoreValue: 230,
        bounceGrant: 38,
        angle: initAngle,
        flash: 0,
        shootTimer: rand(1.2, 2.1)
      });
    } else if (type === 'VALKYRIE_BOSS') {
      enemies.push({
        type, x, y, vx: 0, vy: 0,
        radius: 30,
        hp: 130 * scaleHp,
        maxHp: 130 * scaleHp,
        speed: 108 * scaleSpd,
        color: '#b829ff',
        damage: 24,
        scoreValue: 450,
        bounceGrant: 55,
        angle: initAngle,
        flash: 0
      });
    }
  }

  // --- PLAYER WEAPON SYSTEMS ---
  function getAimAngle() {
    if (gamepadState.aimActive) {
      return Math.atan2(gamepadState.aimY, gamepadState.aimX);
    }
    if (!mouse.active && enemies.length > 0) {
      let nearest = null;
      let minDist = Infinity;
      for (let i = 0; i < enemies.length; i++) {
        const e = enemies[i];
        const d = Math.hypot(e.x - player.x, e.y - player.y);
        if (d < minDist) {
          minDist = d;
          nearest = e;
        }
      }
      if (nearest) return Math.atan2(nearest.y - player.y, nearest.x - player.x);
    }
    return Math.atan2(mouse.y - player.y, mouse.x - player.x);
  }

  function firePrimaryWeapon() {
    const targetAngle = getAimAngle();
    const diff = angleDiff(player.angle, targetAngle);
    player.angle = targetAngle;
    player.bankRoll = Math.max(-1, Math.min(1, diff * 4.5));

    const isEmpowered = player.bounceEnergy >= 50 || player.overclockTimer > 0;
    const perpX = -Math.sin(targetAngle);
    const perpY = Math.cos(targetAngle);
    const noseX = player.x + Math.cos(targetAngle) * 16;
    const noseY = player.y + Math.sin(targetAngle) * 16;

    const offsets = player.overclockTimer > 0 ? [-10, 0, 10] : (isEmpowered ? [-8, 8] : [0]);
    for (let i = 0; i < offsets.length; i++) {
      const off = offsets[i];
      bullets.push({
        x: noseX + perpX * off,
        y: noseY + perpY * off,
        vx: Math.cos(targetAngle) * 860,
        vy: Math.sin(targetAngle) * 860,
        angle: targetAngle,
        radius: isEmpowered ? 5 : 4,
        damage: isEmpowered ? 16 : 14,
        knockback: 210,
        bouncesLeft: isEmpowered ? 2 : 1,
        color: player.overclockTimer > 0 ? '#00ff88' : (isEmpowered ? '#ffe600' : '#00f3ff'),
        isSuper: false,
        life: 1.35
      });
    }

    sfx.play('shoot');
  }

  // Secondary Tactical Weapon: Piercing EMP Railgun Lance (Costs 15% Bounce Energy)
  function fireRailgunLance() {
    if (player.railCooldown > 0) return;
    if (player.bounceEnergy < 15) {
      addFloatingText(player.x, player.y - 28, 'RAILGUN NEEDS 15% CORE!', '#ff0055', 13);
      return;
    }

    player.bounceEnergy -= 15;
    player.railCooldown = 0.45;
    hudDirty = true;

    const ang = getAimAngle();
    player.angle = ang;
    const dirX = Math.cos(ang);
    const dirY = Math.sin(ang);

    // Slight recoil kickback
    player.vx -= dirX * 260;
    player.vy -= dirY * 260;

    const beamLength = Math.hypot(W, H);
    const endX = player.x + dirX * beamLength;
    const endY = player.y + dirY * beamLength;

    laserBeams.push({
      x1: player.x + dirX * 20,
      y1: player.y + dirY * 20,
      x2: endX,
      y2: endY,
      color: '#ff0055',
      life: 0.25,
      maxLife: 0.25
    });

    sfx.play('railgun');
    addShake(0.32);

    // Line-circle intersection against all enemies along beam
    for (let i = enemies.length - 1; i >= 0; i--) {
      const e = enemies[i];
      const toEx = e.x - player.x;
      const toEy = e.y - player.y;
      const proj = toEx * dirX + toEy * dirY;
      if (proj > 0) {
        const closestX = player.x + dirX * proj;
        const closestY = player.y + dirY * proj;
        const perpDist = Math.hypot(e.x - closestX, e.y - closestY);
        if (perpDist <= e.radius + 14) {
          const dmg = 85;
          e.hp -= dmg;
          e.flash = 0.14;
          e.vx += dirX * 480;
          e.vy += dirY * 480;
          spawnParticles(e.x, e.y, 14, '#ff0055', 80, 320, 2, 5, 0.4);
          addFloatingText(e.x, e.y - 16, `RAIL ${dmg}!`, '#ff0055', 16);
          if (e.hp <= 0) killEnemy(i, true);
        }
      }
    }
  }

  function triggerBounceBack() {
    if (player.bounceEnergy < 25) {
      addFloatingText(player.x, player.y - 30, 'CORE BELOW 25%!', '#ff0055', 14);
      return;
    }

    const chargeRatio = player.bounceEnergy / player.maxBounce;
    const isOverdrive = player.bounceEnergy >= 95;
    player.bounceEnergy = 0;
    totalNovas++;

    player.invulnTimer = Math.max(player.invulnTimer, 0.9);
    hitStopTimer = isOverdrive ? 0.065 : 0.035;

    const healAmount = Math.round(9 + chargeRatio * 25);
    player.hp = Math.min(player.maxHp, player.hp + healAmount);

    const novaRadius = 220 + chargeRatio * 350;
    const novaDamage = 65 + chargeRatio * 155;
    const novaColor = isOverdrive ? '#ffe600' : '#00f3ff';

    sfx.play('bounceNova', chargeRatio);
    addShake(0.6 + chargeRatio * 0.65);
    screenFlash = 0.45 + chargeRatio * 0.35;
    screenFlashColor = novaColor;
    gridPulse = 1.0;

    shockwaves.push({
      x: player.x,
      y: player.y,
      radius: 20,
      maxRadius: novaRadius,
      color: novaColor,
      lineWidth: isOverdrive ? 15 : 10,
      alpha: 1
    });

    if (isOverdrive) {
      shockwaves.push({
        x: player.x,
        y: player.y,
        radius: 6,
        maxRadius: novaRadius * 1.28,
        color: '#ff0055',
        lineWidth: 6,
        alpha: 1
      });
    }

    spawnParticles(player.x, player.y, Math.floor(40 + chargeRatio * 55), novaColor, 130, 650, 3, 7, 0.72);

    addFloatingText(
      player.x,
      player.y - 36,
      isOverdrive ? `MAX BOUNCE//BACK! +${healAmount} HP` : `BOUNCE//BACK! +${healAmount} HP`,
      novaColor,
      isOverdrive ? 22 : 18
    );

    for (let i = enemyProjectiles.length - 1; i >= 0; i--) {
      const ep = enemyProjectiles[i];
      if (Math.hypot(ep.x - player.x, ep.y - player.y) <= novaRadius * 1.15) {
        spawnParticles(ep.x, ep.y, 6, '#00f3ff', 40, 180, 2, 4, 0.35);
        removeAtSwap(enemyProjectiles, i);
      }
    }

    const missileCount = Math.floor(10 + chargeRatio * 14);
    for (let i = 0; i < missileCount; i++) {
      const ang = (Math.PI * 2 * i) / missileCount;
      bullets.push({
        x: player.x + Math.cos(ang) * 22,
        y: player.y + Math.sin(ang) * 22,
        vx: Math.cos(ang) * 940,
        vy: Math.sin(ang) * 940,
        angle: ang,
        radius: isOverdrive ? 8 : 6,
        damage: 36 + chargeRatio * 38,
        knockback: 600,
        bouncesLeft: isOverdrive ? 5 : 3,
        color: isOverdrive ? '#ffe600' : '#00ff88',
        isSuper: true,
        life: 2.3
      });
    }

    for (let i = enemies.length - 1; i >= 0; i--) {
      const e = enemies[i];
      const dx = e.x - player.x;
      const dy = e.y - player.y;
      const dist = Math.hypot(dx, dy) || 1;
      if (dist <= novaRadius + e.radius) {
        const falloff = 1 - (dist / (novaRadius + e.radius)) * 0.45;
        const dmg = novaDamage * falloff;
        e.hp -= dmg;
        e.flash = 0.16;

        const pushForce = (800 + chargeRatio * 680) * falloff * (e.isBoss ? 0.25 : 1);
        e.vx = (dx / dist) * pushForce;
        e.vy = (dy / dist) * pushForce;

        addFloatingText(e.x, e.y - 16, `${Math.round(dmg)}`, novaColor, 15);
        if (e.hp <= 0) killEnemy(i, true);
      }
    }

    hudDirty = true;
  }

  function applyPlayerHit(sourceX, sourceY, damage, bounceGain) {
    if (player.invulnTimer > 0) return;

    const dx = player.x - sourceX;
    const dy = player.y - sourceY;
    const dist = Math.hypot(dx, dy) || 1;
    const knockbackForce = 880;
    player.vx = (dx / dist) * knockbackForce;
    player.vy = (dy / dist) * knockbackForce;

    // Aegis Shield absorbs hull damage while granting 1.5x Bounce Energy!
    if (player.shieldCharges > 0) {
      player.shieldCharges--;
      const boostedGain = Math.round(bounceGain * 1.4);
      player.bounceEnergy = Math.min(player.maxBounce, player.bounceEnergy + boostedGain);
      player.invulnTimer = 0.65;
      sfx.play('pickup');
      addShake(0.35);
      screenFlash = 0.28;
      screenFlashColor = '#00f3ff';
      spawnParticles(player.x, player.y, 24, '#00f3ff', 100, 400, 3, 6, 0.5);
      addFloatingText(player.x, player.y - 28, `AEGIS BLOCKED! +${boostedGain}% BOUNCE`, '#00f3ff', 17);
      hudDirty = true;
      return;
    }

    player.hp = Math.max(0, player.hp - damage);
    player.bounceEnergy = Math.min(player.maxBounce, player.bounceEnergy + bounceGain);
    player.invulnTimer = 0.58;
    hitStopTimer = 0.04;

    sfx.play('hurt');
    addShake(0.52);
    screenFlash = 0.38;
    screenFlashColor = '#ff0055';

    spawnParticles(player.x, player.y, 24, '#ff0055', 90, 390, 3, 6, 0.5);
    spawnParticles(player.x, player.y, 16, '#00f3ff', 110, 430, 2, 5, 0.55);

    shockwaves.push({
      x: player.x,
      y: player.y,
      radius: 10,
      maxRadius: 120,
      color: '#ff0055',
      lineWidth: 5,
      alpha: 0.9
    });

    addFloatingText(player.x, player.y - 28, `+${bounceGain}% BOUNCE!`, '#00f3ff', 18);

    if (player.hp <= 0) {
      triggerGameOver();
    }
    hudDirty = true;
  }

  function killEnemy(index, fromBounceNova = false) {
    const e = enemies[index];
    if (!e) return;

    sfx.play('kill');
    totalKills++;
    waveKills++;

    if (e.isBoss) {
      bossActive = null;
      UI.bossHud.classList.add('hidden');
      addShake(0.9);
      screenFlash = 0.6;
      screenFlashColor = '#ffe600';
      addBanner('DREADNOUGHT DESTROYED', 'FULL BOUNCE CORE +35 HULL RESTORED', '#ffe600');
      player.hp = Math.min(player.maxHp, player.hp + 35);
      player.bounceEnergy = player.maxBounce;
    }

    multiplier = Math.min(8.0, +(multiplier + (fromBounceNova ? 0.25 : 0.1)).toFixed(1));
    multiplierTimer = 4.2;

    const pts = Math.round(e.scoreValue * multiplier);
    score += pts;

    spawnParticles(e.x, e.y, e.isBoss ? 55 : 24, e.color, 75, 420, 2.5, 6.5, 0.62);
    shockwaves.push({
      x: e.x,
      y: e.y,
      radius: 6,
      maxRadius: e.radius * 3.4,
      color: e.color,
      lineWidth: e.isBoss ? 8 : 4,
      alpha: 0.85
    });

    addFloatingText(e.x, e.y, `+${pts}`, '#ffe600', 15);

    // Drop Core or Power-up Pod (Shield / Overclock)
    const dropRoll = Math.random();
    if (dropRoll < 0.58 || e.isBoss) {
      let podType = 'CORE';
      if (e.isBoss || dropRoll < 0.08) podType = 'SHIELD';
      else if (dropRoll < 0.17) podType = 'OVERCLOCK';

      pickups.push({
        podType,
        x: e.x,
        y: e.y,
        vx: rand(-60, 60),
        vy: rand(-60, 60),
        radius: podType === 'CORE' ? 8 : 11,
        energy: 14,
        heal: 4,
        life: 8.5
      });
    }

    if (e.type === 'VALKYRIE_BOSS') {
      for (let k = 0; k < 2; k++) {
        enemies.push({
          type: 'VIPER',
          x: e.x + rand(-20, 20),
          y: e.y + rand(-20, 20),
          vx: rand(-220, 220),
          vy: rand(-220, 220),
          radius: 16,
          hp: 26,
          maxHp: 26,
          speed: 230,
          color: '#ff0055',
          damage: 12,
          scoreValue: 90,
          bounceGrant: 25,
          angle: e.angle,
          flash: 0
        });
      }
    }

    removeAtSwap(enemies, index);

    if (waveKills >= waveKillsRequired && !bossActive) {
      wave++;
      waveKills = 0;
      waveKillsRequired = Math.floor(8 + wave * 4.5);
      player.hp = Math.min(player.maxHp, player.hp + 15);
      player.bounceEnergy = Math.min(player.maxBounce, player.bounceEnergy + 20);

      if (wave % 3 === 0) {
        spawnBossDreadnought();
      } else {
        addBanner(`AIRSPACE WAVE ${String(wave).padStart(2, '0')}`, 'AIRFRAME +15 // BOUNCE CORE +20%', '#00ff88');
      }
    }

    hudDirty = true;
  }

  function flushHUD() {
    if (!hudDirty) return;
    hudDirty = false;

    const hpPct = Math.max(0, (player.hp / player.maxHp) * 100);
    UI.hpFill.style.width = `${hpPct}%`;
    UI.hpGhost.style.width = `${hpPct}%`;
    UI.hpText.textContent = `${Math.ceil(player.hp)} / ${player.maxHp}`;

    const bouncePct = Math.min(100, Math.floor((player.bounceEnergy / player.maxBounce) * 100));
    UI.bounceFill.style.width = `${bouncePct}%`;
    UI.bounceText.textContent = `${bouncePct}%`;

    if (bouncePct >= 25) {
      UI.barsPanel.classList.add('bounce-ready');
      UI.spacePrompt.classList.add('active');
      UI.novaStatusText.textContent = bouncePct >= 95
        ? '[SPACE] MAX OVERDRIVE READY // DETONATE!'
        : `[SPACE] BOUNCE//BACK READY (${bouncePct}%)`;
    } else {
      UI.barsPanel.classList.remove('bounce-ready');
      UI.spacePrompt.classList.remove('active');
      UI.novaStatusText.textContent = 'ABSORB HITS OR CORES [25% MIN]';
    }

    if (bossActive) {
      const bPct = Math.max(0, Math.ceil((bossActive.hp / bossActive.maxHp) * 100));
      UI.bossFill.style.width = `${bPct}%`;
      UI.bossHpPct.textContent = `${bPct}%`;
    }

    UI.waveText.textContent = String(wave).padStart(2, '0');
    UI.scoreText.textContent = score.toLocaleString();
    UI.comboText.textContent = `MULT x${multiplier.toFixed(1)}`;
    UI.bestText.textContent = `TOP ACE: ${Math.max(score, cachedTopScore).toLocaleString()}`;

    let buffsHtml = '';
    if (player.shieldCharges > 0) {
      buffsHtml += `<span class="buff-pill buff-shield">AEGIS SHIELD x${player.shieldCharges}</span>`;
    }
    if (player.overclockTimer > 0) {
      buffsHtml += `<span class="buff-pill buff-overclock">OVERCLOCK ${player.overclockTimer.toFixed(1)}S</span>`;
    }
    UI.buffRow.innerHTML = buffsHtml;
  }

  function startGame() {
    sfx.init();
    const enteredName = UI.pilotInput.value.trim().toUpperCase();
    currentPilot = enteredName || 'MAVERICK';
    localStorage.setItem(PILOT_KEY, currentPilot);
    UI.hudPilotName.textContent = currentPilot;

    gameState = 'PLAYING';
    UI.pauseBtn.textContent = 'PAUSE [P]';
    UI.startScreen.classList.add('hidden');
    UI.gameoverScreen.classList.add('hidden');
    UI.bossHud.classList.add('hidden');

    score = 0;
    wave = 1;
    waveKills = 0;
    waveKillsRequired = 8;
    totalKills = 0;
    totalNovas = 0;
    multiplier = 1.0;
    multiplierTimer = 0;
    spawnTimer = 0.4;
    bossActive = null;

    player.x = W / 2;
    player.y = H / 2;
    player.vx = 0;
    player.vy = 0;
    player.hp = player.maxHp;
    player.bounceEnergy = 45;
    player.invulnTimer = 1.0;
    player.shieldCharges = 0;
    player.overclockTimer = 0;
    player.trailHead = 0;
    player.trailCount = 0;

    bullets.length = 0;
    laserBeams.length = 0;
    enemies.length = 0;
    enemyProjectiles.length = 0;
    particles.length = 0;
    shockwaves.length = 0;
    floatingTexts.length = 0;
    pickups.length = 0;
    banners.length = 0;

    addBanner(`SORTIE // ${currentPilot}`, 'SPACE: BOUNCE NOVA // SHIFT: RAILGUN LANCE', '#00f3ff');
    hudDirty = true;
    flushHUD();
  }

  function triggerGameOver() {
    gameState = 'GAMEOVER';
    UI.finalPilot.textContent = currentPilot;
    UI.finalScore.textContent = score.toLocaleString();
    UI.finalWave.textContent = String(wave).padStart(2, '0');
    UI.finalKills.textContent = totalKills;

    saveScoreToLeaderboard(currentPilot, score, wave);
    renderLeaderboardUI();
    UI.gameoverScreen.classList.remove('hidden');
  }

  UI.startBtn.addEventListener('click', startGame);
  UI.restartBtn.addEventListener('click', startGame);

  // --- MAIN UPDATE LOOP ---
  let lastTime = performance.now();

  function update(dt) {
    pollGamepad();
    if (gameState !== 'PLAYING') return;

    if (hitStopTimer > 0) {
      hitStopTimer -= dt;
      return;
    }

    if (shakeTrauma > 0) shakeTrauma = Math.max(0, shakeTrauma - dt * 2.2);
    if (screenFlash > 0) screenFlash = Math.max(0, screenFlash - dt * 1.8);
    if (gridPulse > 0) gridPulse = Math.max(0, gridPulse - dt * 1.6);
    if (player.railCooldown > 0) player.railCooldown -= dt;
    player.bankRoll *= Math.pow(0.08, dt);

    if (player.overclockTimer > 0) {
      player.overclockTimer = Math.max(0, player.overclockTimer - dt);
      hudDirty = true;
    }

    if (multiplierTimer > 0) {
      multiplierTimer -= dt;
      if (multiplierTimer <= 0) {
        multiplier = 1.0;
        hudDirty = true;
      }
    }

    // 1. PLAYER JET MOVEMENT (Keyboard + Gamepad Analog Stick)
    let ix = gamepadState.moveX;
    let iy = gamepadState.moveY;
    if (keys['KeyD'] || keys['ArrowRight']) ix += 1;
    if (keys['KeyA'] || keys['ArrowLeft']) ix -= 1;
    if (keys['KeyS'] || keys['ArrowDown']) iy += 1;
    if (keys['KeyW'] || keys['ArrowUp']) iy -= 1;

    const len = Math.hypot(ix, iy);
    if (len > 0) {
      if (len > 1) {
        ix /= len;
        iy /= len;
      }
      player.vx = moveToward(player.vx, ix * player.maxSpeed, player.accel * dt);
      player.vy = moveToward(player.vy, iy * player.maxSpeed, player.accel * dt);
    } else {
      player.vx = moveToward(player.vx, 0, player.friction * dt);
      player.vy = moveToward(player.vy, 0, player.friction * dt);
    }

    player.x += player.vx * dt;
    player.y += player.vy * dt;

    const pad = player.radius + 8;
    if (player.x < pad) {
      player.x = pad;
      player.vx = Math.abs(player.vx) * 0.75;
    } else if (player.x > W - pad) {
      player.x = W - pad;
      player.vx = -Math.abs(player.vx) * 0.75;
    }
    if (player.y < pad) {
      player.y = pad;
      player.vy = Math.abs(player.vy) * 0.75;
    } else if (player.y > H - pad) {
      player.y = H - pad;
      player.vy = -Math.abs(player.vy) * 0.75;
    }

    if (player.invulnTimer > 0) player.invulnTimer -= dt;

    // Circular Buffer Wingtip Contrails (Zero array shifting overhead)
    const cosA = Math.cos(player.angle);
    const sinA = Math.sin(player.angle);
    const wingX = -6;
    const wingY = 19 * (1 - Math.abs(player.bankRoll) * 0.25);
    player.wingL[player.trailHead] = {
      x: player.x + wingX * cosA - (-wingY) * sinA,
      y: player.y + wingX * sinA + (-wingY) * cosA
    };
    player.wingR[player.trailHead] = {
      x: player.x + wingX * cosA - wingY * sinA,
      y: player.y + wingX * sinA + wingY * cosA
    };
    player.trailHead = (player.trailHead + 1) % TRAIL_LEN;
    if (player.trailCount < TRAIL_LEN) player.trailCount++;

    // Afterburner Exhaust Particles
    player.trailTimer -= dt;
    if (player.trailTimer <= 0 && Math.hypot(player.vx, player.vy) > 65) {
      player.trailTimer = 0.024;
      const tailX = player.x - cosA * 18;
      const tailY = player.y - sinA * 18;
      spawnParticles(tailX, tailY, 1, player.bounceEnergy >= 25 ? '#00f3ff' : '#ff8800', 60, 140, 2.2, 4.2, 0.18);
    }

    // Auto-fire primary cannon
    player.fireTimer -= dt;
    if (player.fireTimer <= 0 && (enemies.length > 0 || mouse.down || gamepadState.aimActive)) {
      const fireDelay = player.overclockTimer > 0 ? 0.085 : (player.bounceEnergy >= 75 ? 0.13 : 0.165);
      player.fireTimer = fireDelay;
      firePrimaryWeapon();
    }

    // 2. UPDATE PLAYER BULLETS
    for (let i = bullets.length - 1; i >= 0; i--) {
      const b = bullets[i];
      b.x += b.vx * dt;
      b.y += b.vy * dt;
      b.angle = Math.atan2(b.vy, b.vx);
      b.life -= dt;

      let bounced = false;
      if (b.x <= b.radius || b.x >= W - b.radius) {
        if (b.bouncesLeft > 0) {
          b.vx *= -1;
          b.x = Math.max(b.radius, Math.min(W - b.radius, b.x));
          b.bouncesLeft--;
          bounced = true;
        } else {
          b.life = 0;
        }
      }
      if (b.y <= b.radius || b.y >= H - b.radius) {
        if (b.bouncesLeft > 0) {
          b.vy *= -1;
          b.y = Math.max(b.radius, Math.min(H - b.radius, b.y));
          b.bouncesLeft--;
          bounced = true;
        } else {
          b.life = 0;
        }
      }

      if (bounced) {
        sfx.play('ricochet');
        spawnParticles(b.x, b.y, 4, b.color, 50, 160, 1.5, 3.2, 0.22);
      }

      for (let j = enemies.length - 1; j >= 0; j--) {
        const e = enemies[j];
        const dist = Math.hypot(e.x - b.x, e.y - b.y);
        if (dist < e.radius + b.radius) {
          e.hp -= b.damage;
          e.flash = 0.09;

          const bSpeed = Math.hypot(b.vx, b.vy) || 1;
          const kbScale = e.isBoss ? 0.15 : 1;
          e.vx += (b.vx / bSpeed) * b.knockback * kbScale;
          e.vy += (b.vy / bSpeed) * b.knockback * kbScale;

          spawnParticles(b.x, b.y, 5, b.color, 60, 210, 2, 3.8, 0.25);

          player.bounceEnergy = Math.min(player.maxBounce, player.bounceEnergy + 1.2);
          hudDirty = true;

          if (e.hp <= 0) {
            killEnemy(j, b.isSuper);
          }

          if (b.isSuper && b.bouncesLeft > 0) {
            b.bouncesLeft--;
            b.vx = -b.vx + rand(-180, 180);
            b.vy = -b.vy + rand(-180, 180);
          } else {
            b.life = 0;
          }
          break;
        }
      }

      if (b.life <= 0) removeAtSwap(bullets, i);
    }

    // 3. SPAWN & UPDATE ENEMY FIGHTERS
    spawnTimer -= dt;
    const maxConcurrent = Math.min(28, 6 + wave * 3);
    if (spawnTimer <= 0 && enemies.length < maxConcurrent) {
      spawnEnemy();
      spawnTimer = Math.max(0.32, 1.35 - wave * 0.09);
    }

    for (let i = enemies.length - 1; i >= 0; i--) {
      const e = enemies[i];
      if (e.flash > 0) e.flash -= dt;

      const dx = player.x - e.x;
      const dy = player.y - e.y;
      const dist = Math.hypot(dx, dy) || 1;
      const dirX = dx / dist;
      const dirY = dy / dist;
      const targetAngle = Math.atan2(dy, dx);

      if (e.type === 'AETHER_CARRIER') {
        // Boss AI: Hover & strafe while firing radial flak barrages
        const desiredDist = 240;
        const push = dist > desiredDist ? 1 : -0.4;
        e.vx = moveToward(e.vx, (dirX * push - dirY * 0.7) * e.speed, 380 * dt);
        e.vy = moveToward(e.vy, (dirY * push + dirX * 0.7) * e.speed, 380 * dt);
        e.angle = targetAngle;

        e.shootTimer -= dt;
        if (e.shootTimer <= 0) {
          e.shootTimer = 1.55;
          e.patternPhase = (e.patternPhase + 1) % 2;
          const count = e.patternPhase === 0 ? 8 : 5;
          for (let k = 0; k < count; k++) {
            const spreadAng = e.patternPhase === 0
              ? (Math.PI * 2 * k) / count
              : targetAngle + (k - 2) * 0.22;
            enemyProjectiles.push({
              x: e.x + Math.cos(spreadAng) * 28,
              y: e.y + Math.sin(spreadAng) * 28,
              vx: Math.cos(spreadAng) * 290,
              vy: Math.sin(spreadAng) * 290,
              radius: 8,
              damage: 14,
              bounceGrant: 34,
              life: 4.0
            });
          }
        }
      } else if (e.type === 'VIPER' || e.type === 'VALKYRIE_BOSS') {
        e.vx = moveToward(e.vx, dirX * e.speed, 650 * dt);
        e.vy = moveToward(e.vy, dirY * e.speed, 650 * dt);
        e.angle = targetAngle;
      } else if (e.type === 'BERKUT') {
        e.dashTimer -= dt;
        if (e.dashState === 'CHASE') {
          e.vx = moveToward(e.vx, dirX * e.speed, 600 * dt);
          e.vy = moveToward(e.vy, dirY * e.speed, 600 * dt);
          e.angle = targetAngle;
          if (e.dashTimer <= 0 && dist < 460) {
            e.dashState = 'AIM';
            e.dashTimer = 0.48;
            e.aimAngle = targetAngle;
            e.angle = targetAngle;
            e.vx *= 0.2;
            e.vy *= 0.2;
          }
        } else if (e.dashState === 'AIM') {
          e.vx *= 0.88;
          e.vy *= 0.88;
          e.angle = e.aimAngle;
          if (e.dashTimer <= 0) {
            e.dashState = 'LUNGE';
            e.dashTimer = 0.38;
            e.vx = Math.cos(e.aimAngle) * (e.speed * 3.7);
            e.vy = Math.sin(e.aimAngle) * (e.speed * 3.7);
            spawnParticles(e.x, e.y, 10, '#ffe600', 50, 210, 2, 4, 0.3);
          }
        } else if (e.dashState === 'LUNGE') {
          e.angle = e.aimAngle;
          if (e.dashTimer <= 0) {
            e.dashState = 'CHASE';
            e.dashTimer = rand(1.3, 2.2);
          }
        }
      } else if (e.type === 'WRAITH') {
        const desiredDist = 250;
        const radialPush = dist > desiredDist ? 1 : -0.7;
        const targetVx = (dirX * radialPush - dirY * 0.9) * e.speed;
        const targetVy = (dirY * radialPush + dirX * 0.9) * e.speed;
        e.vx = moveToward(e.vx, targetVx, 550 * dt);
        e.vy = moveToward(e.vy, targetVy, 550 * dt);
        e.angle = Math.atan2(e.vy, e.vx);

        e.shootTimer -= dt;
        if (e.shootTimer <= 0) {
          e.shootTimer = rand(1.6, 2.5);
          enemyProjectiles.push({
            x: e.x,
            y: e.y,
            vx: dirX * 320,
            vy: dirY * 320,
            radius: 7,
            damage: 12,
            bounceGrant: 30,
            life: 3.5
          });
        }
      }

      e.x += e.vx * dt;
      e.y += e.vy * dt;

      for (let j = i - 1; j >= 0; j--) {
        const o = enemies[j];
        const sdx = e.x - o.x;
        const sdy = e.y - o.y;
        const sdist = Math.hypot(sdx, sdy);
        const minSep = e.radius + o.radius;
        if (sdist > 0 && sdist < minSep) {
          const push = (minSep - sdist) * 0.5;
          const nx = sdx / sdist;
          const ny = sdy / sdist;
          e.x += nx * push;
          e.y += ny * push;
          o.x -= nx * push;
          o.y -= ny * push;
        }
      }

      const pDist = Math.hypot(player.x - e.x, player.y - e.y);
      if (pDist < player.radius + e.radius) {
        const nx = (e.x - player.x) / (pDist || 1);
        const ny = (e.y - player.y) / (pDist || 1);
        e.vx = nx * (e.isBoss ? 180 : 540);
        e.vy = ny * (e.isBoss ? 180 : 540);

        e.hp -= 18;
        e.flash = 0.12;
        applyPlayerHit(e.x, e.y, e.damage, e.bounceGrant);

        if (e.hp <= 0) killEnemy(i, false);
      }
    }

    // 4. UPDATE ENEMY PROJECTILES
    for (let i = enemyProjectiles.length - 1; i >= 0; i--) {
      const ep = enemyProjectiles[i];
      ep.x += ep.vx * dt;
      ep.y += ep.vy * dt;
      ep.life -= dt;

      if (Math.hypot(ep.x - player.x, ep.y - player.y) < ep.radius + player.radius) {
        applyPlayerHit(ep.x, ep.y, ep.damage, ep.bounceGrant);
        removeAtSwap(enemyProjectiles, i);
        continue;
      }

      if (ep.life <= 0 || ep.x < -30 || ep.x > W + 30 || ep.y < -30 || ep.y > H + 30) {
        removeAtSwap(enemyProjectiles, i);
      }
    }

    // 5. UPDATE PICKUPS & POWER-UPS
    for (let i = pickups.length - 1; i >= 0; i--) {
      const p = pickups[i];
      p.life -= dt;
      p.vx *= 0.94;
      p.vy *= 0.94;

      const dx = player.x - p.x;
      const dy = player.y - p.y;
      const dist = Math.hypot(dx, dy) || 1;
      if (dist < 210) {
        p.vx += (dx / dist) * 1020 * dt;
        p.vy += (dy / dist) * 1020 * dt;
      }

      p.x += p.vx * dt;
      p.y += p.vy * dt;

      if (dist < player.radius + p.radius + 6) {
        sfx.play('pickup');
        if (p.podType === 'SHIELD') {
          player.shieldCharges = Math.min(3, player.shieldCharges + 1);
          spawnParticles(p.x, p.y, 14, '#00f3ff', 60, 220, 2, 4.5, 0.35);
          addFloatingText(p.x, p.y - 12, 'AEGIS SHIELD ACTIVE!', '#00f3ff', 15);
        } else if (p.podType === 'OVERCLOCK') {
          player.overclockTimer = Math.min(12, player.overclockTimer + 6.5);
          spawnParticles(p.x, p.y, 14, '#ffe600', 60, 220, 2, 4.5, 0.35);
          addFloatingText(p.x, p.y - 12, 'TRI-CANNON OVERCLOCK!', '#ffe600', 15);
        } else {
          player.bounceEnergy = Math.min(player.maxBounce, player.bounceEnergy + p.energy);
          player.hp = Math.min(player.maxHp, player.hp + p.heal);
          spawnParticles(p.x, p.y, 8, '#00ff88', 50, 180, 2, 4, 0.3);
          addFloatingText(p.x, p.y - 10, `+${p.energy}% BOUNCE`, '#00ff88', 13);
        }
        removeAtSwap(pickups, i);
        hudDirty = true;
        continue;
      }

      if (p.life <= 0) removeAtSwap(pickups, i);
    }

    // 6. UPDATE PARTICLES, BEAMS, SHOCKWAVES, TEXTS & BANNERS
    for (let i = particles.length - 1; i >= 0; i--) {
      const pt = particles[i];
      pt.x += pt.vx * dt;
      pt.y += pt.vy * dt;
      pt.vx *= pt.drag;
      pt.vy *= pt.drag;
      pt.life -= dt;
      if (pt.life <= 0) removeAtSwap(particles, i);
    }

    for (let i = laserBeams.length - 1; i >= 0; i--) {
      laserBeams[i].life -= dt;
      if (laserBeams[i].life <= 0) removeAtSwap(laserBeams, i);
    }

    for (let i = shockwaves.length - 1; i >= 0; i--) {
      const sw = shockwaves[i];
      sw.radius += (sw.maxRadius - sw.radius) * 11 * dt;
      sw.alpha -= dt * 2.1;
      if (sw.alpha <= 0) removeAtSwap(shockwaves, i);
    }

    for (let i = floatingTexts.length - 1; i >= 0; i--) {
      const ft = floatingTexts[i];
      ft.x += ft.vx * dt;
      ft.y += ft.vy * dt;
      ft.life -= dt;
      if (ft.life <= 0) removeAtSwap(floatingTexts, i);
    }

    for (let i = banners.length - 1; i >= 0; i--) {
      banners[i].life -= dt;
      if (banners[i].life <= 0) removeAtSwap(banners, i);
    }

    flushHUD();
  }

  // --- FIGHTER JET RENDERERS ---
  function drawPlayerFighterJet(time) {
    ctx.save();
    ctx.translate(player.x, player.y);

    // Aegis Shield Bubble
    if (player.shieldCharges > 0) {
      ctx.beginPath();
      ctx.arc(0, 0, player.radius + 17, 0, Math.PI * 2);
      ctx.strokeStyle = 'rgba(0, 243, 255, 0.75)';
      ctx.fillStyle = 'rgba(0, 243, 255, 0.08)';
      ctx.lineWidth = 2;
      ctx.fill();
      ctx.stroke();
    }

    // Outer Kinetic Bounce Core Ring
    const chargeRatio = player.bounceEnergy / player.maxBounce;
    if (chargeRatio > 0.02) {
      ctx.beginPath();
      ctx.arc(0, 0, player.radius + 12, -Math.PI / 2, -Math.PI / 2 + Math.PI * 2 * chargeRatio);
      ctx.strokeStyle = player.bounceEnergy >= 25
        ? (player.bounceEnergy >= 95 ? '#ffe600' : '#00f3ff')
        : 'rgba(0, 243, 255, 0.32)';
      ctx.lineWidth = 3;
      ctx.stroke();
    }

    if (player.invulnTimer > 0 && Math.floor(time / 45) % 2 === 0) {
      ctx.globalAlpha = 0.55;
    }

    ctx.rotate(player.angle);
    // Dynamic 3D banking roll illusion when turning
    ctx.scale(1, 1 - Math.abs(player.bankRoll) * 0.24);

    const isOverdrive = player.bounceEnergy >= 95;
    const trimColor = isOverdrive ? '#ffe600' : (player.overclockTimer > 0 ? '#00ff88' : '#00f3ff');
    const speedRatio = Math.min(1, Math.hypot(player.vx, player.vy) / player.maxSpeed);
    const flameLen = 11 + speedRatio * 14 + Math.sin(time * 0.06) * 4;

    // Twin Afterburner Plumes
    ctx.fillStyle = trimColor;
    for (const ny of [-5.5, 5.5]) {
      ctx.beginPath();
      ctx.moveTo(-16, ny - 2.6);
      ctx.lineTo(-16 - flameLen, ny);
      ctx.lineTo(-16, ny + 2.6);
      ctx.closePath();
      ctx.fill();
    }

    // Swept Stealth Wings & Stabilizers
    ctx.fillStyle = '#0a1529';
    ctx.strokeStyle = trimColor;
    ctx.lineWidth = 2.2;

    ctx.beginPath();
    ctx.moveTo(24, 0);
    ctx.lineTo(7, 6);
    ctx.lineTo(11, 11);
    ctx.lineTo(4, 10);
    ctx.lineTo(-5, 22);
    ctx.lineTo(-13, 20);
    ctx.lineTo(-10, 9);
    ctx.lineTo(-19, 13);
    ctx.lineTo(-17, 4);
    ctx.lineTo(-15, 0);
    ctx.lineTo(-17, -4);
    ctx.lineTo(-19, -13);
    ctx.lineTo(-10, -9);
    ctx.lineTo(-13, -20);
    ctx.lineTo(-5, -22);
    ctx.lineTo(4, -10);
    ctx.lineTo(11, -11);
    ctx.lineTo(7, -6);
    ctx.closePath();
    ctx.fill();
    ctx.stroke();

    // Inner Fuselage Spine
    ctx.fillStyle = '#142847';
    ctx.beginPath();
    ctx.moveTo(18, 0);
    ctx.lineTo(-4, 6.5);
    ctx.lineTo(-14, 4);
    ctx.lineTo(-14, -4);
    ctx.lineTo(-4, -6.5);
    ctx.closePath();
    ctx.fill();

    // Bubble Canopy Glass
    ctx.fillStyle = '#b8ffff';
    ctx.beginPath();
    ctx.ellipse(3, 0, 7.5, 2.8, 0, 0, Math.PI * 2);
    ctx.fill();

    ctx.restore();
  }

  function drawEnemyFighter(e, time) {
    ctx.save();
    ctx.translate(e.x, e.y);

    if (e.type === 'BERKUT' && e.dashState === 'AIM') {
      ctx.save();
      ctx.strokeStyle = 'rgba(255, 230, 0, 0.75)';
      ctx.lineWidth = 2;
      ctx.setLineDash([7, 6]);
      ctx.beginPath();
      ctx.moveTo(0, 0);
      ctx.lineTo(Math.cos(e.aimAngle) * 400, Math.sin(e.aimAngle) * 400);
      ctx.stroke();
      ctx.restore();
    }

    ctx.rotate(e.angle);

    const drawColor = e.flash > 0 ? '#ffffff' : e.color;
    const fillDark = e.flash > 0 ? '#ffffff' : '#180818';
    const flame = 8 + Math.sin(time * 0.05 + e.x) * 3;

    ctx.fillStyle = drawColor;
    ctx.beginPath();
    ctx.moveTo(-e.radius * 0.75, -3);
    ctx.lineTo(-e.radius * 0.75 - flame, 0);
    ctx.lineTo(-e.radius * 0.75, 3);
    ctx.closePath();
    ctx.fill();

    ctx.strokeStyle = drawColor;
    ctx.fillStyle = fillDark;
    ctx.lineWidth = 2.2;

    if (e.type === 'VIPER') {
      ctx.beginPath();
      ctx.moveTo(19, 0);
      ctx.lineTo(3, 5);
      ctx.lineTo(-9, 16);
      ctx.lineTo(-15, 14);
      ctx.lineTo(-11, 4);
      ctx.lineTo(-15, 0);
      ctx.lineTo(-11, -4);
      ctx.lineTo(-15, -14);
      ctx.lineTo(-9, -16);
      ctx.lineTo(3, -5);
      ctx.closePath();
      ctx.fill();
      ctx.stroke();
    } else if (e.type === 'BERKUT') {
      ctx.beginPath();
      ctx.moveTo(21, 0);
      ctx.lineTo(6, 5);
      ctx.lineTo(5, 19);
      ctx.lineTo(-4, 17);
      ctx.lineTo(-8, 6);
      ctx.lineTo(-16, 10);
      ctx.lineTo(-15, -10);
      ctx.lineTo(-8, -6);
      ctx.lineTo(-4, -17);
      ctx.lineTo(5, -19);
      ctx.lineTo(6, -5);
      ctx.closePath();
      ctx.fill();
      ctx.stroke();
    } else if (e.type === 'WRAITH') {
      ctx.beginPath();
      ctx.moveTo(14, 0);
      ctx.lineTo(-4, 22);
      ctx.lineTo(-13, 18);
      ctx.lineTo(-8, 9);
      ctx.lineTo(-14, 4);
      ctx.lineTo(-9, 0);
      ctx.lineTo(-14, -4);
      ctx.lineTo(-8, -9);
      ctx.lineTo(-13, -18);
      ctx.lineTo(-4, -22);
      ctx.closePath();
      ctx.fill();
      ctx.stroke();
    } else if (e.type === 'VALKYRIE_BOSS' || e.type === 'AETHER_CARRIER') {
      const sc = e.type === 'AETHER_CARRIER' ? 1.48 : 1.0;
      ctx.scale(sc, sc);
      ctx.beginPath();
      ctx.moveTo(30, 0);
      ctx.lineTo(12, 9);
      ctx.lineTo(4, 28);
      ctx.lineTo(-12, 26);
      ctx.lineTo(-10, 12);
      ctx.lineTo(-24, 16);
      ctx.lineTo(-22, 5);
      ctx.lineTo(-18, 0);
      ctx.lineTo(-22, -5);
      ctx.lineTo(-24, -16);
      ctx.lineTo(-10, -12);
      ctx.lineTo(-12, -26);
      ctx.lineTo(4, -28);
      ctx.lineTo(12, -9);
      ctx.closePath();
      ctx.fill();
      ctx.stroke();
    }

    ctx.fillStyle = e.flash > 0 ? '#ffffff' : drawColor;
    ctx.beginPath();
    ctx.ellipse(2, 0, 5.5, 2.2, 0, 0, Math.PI * 2);
    ctx.fill();

    ctx.restore();
  }

  // --- MAIN RENDER PIPELINE ---
  function draw(time) {
    ctx.save();

    ctx.fillStyle = '#03040a';
    ctx.fillRect(0, 0, W, H);

    if (shakeTrauma > 0) {
      const shakeMag = shakeTrauma * shakeTrauma * 24;
      ctx.translate(rand(-shakeMag, shakeMag), rand(-shakeMag, shakeMag));
    }

    // Parallax Starfield
    for (let i = 0; i < stars.length; i++) {
      const s = stars[i];
      const sx = ((s.x - player.x * s.depth * 0.25) % W + W) % W;
      const sy = ((s.y - player.y * s.depth * 0.25) % H + H) % H;
      ctx.fillStyle = `rgba(200, 235, 255, ${s.alpha})`;
      ctx.fillRect(sx, sy, s.size, s.size);
    }

    // Reactive Tactical Radar Grid
    const spacing = 60;
    const pulseAlpha = 0.05 + gridPulse * 0.16;
    ctx.strokeStyle = `rgba(0, 243, 255, ${pulseAlpha})`;
    ctx.lineWidth = 1;
    ctx.beginPath();
    const offsetX = (-player.x * 0.15) % spacing;
    const offsetY = (-player.y * 0.15) % spacing;
    for (let x = offsetX; x < W; x += spacing) {
      ctx.moveTo(x, 0);
      ctx.lineTo(x, H);
    }
    for (let y = offsetY; y < H; y += spacing) {
      ctx.moveTo(0, y);
      ctx.lineTo(W, y);
    }
    ctx.stroke();

    ctx.strokeStyle = player.bounceEnergy >= 25 ? 'rgba(0, 243, 255, 0.5)' : 'rgba(255, 0, 85, 0.35)';
    ctx.lineWidth = 4;
    ctx.strokeRect(2, 2, W - 4, H - 4);

    // Wingtip Contrails (Circular Buffer Read)
    if (gameState === 'PLAYING' && player.trailCount > 2) {
      for (const ring of [player.wingL, player.wingR]) {
        ctx.beginPath();
        for (let i = 0; i < player.trailCount; i++) {
          const idx = (player.trailHead - player.trailCount + i + TRAIL_LEN) % TRAIL_LEN;
          const pt = ring[idx];
          if (i === 0) ctx.moveTo(pt.x, pt.y);
          else ctx.lineTo(pt.x, pt.y);
        }
        ctx.strokeStyle = 'rgba(0, 243, 255, 0.24)';
        ctx.lineWidth = 2;
        ctx.stroke();
      }
    }

    // Pickups & Power-up Pods
    for (let i = 0; i < pickups.length; i++) {
      const p = pickups[i];
      ctx.save();
      ctx.translate(p.x, p.y);
      ctx.rotate(time * 0.005);
      const pCol = p.podType === 'SHIELD' ? '#00f3ff' : (p.podType === 'OVERCLOCK' ? '#ffe600' : '#00ff88');
      ctx.fillStyle = pCol;
      ctx.strokeStyle = '#ffffff';
      ctx.lineWidth = 1.5;
      ctx.beginPath();
      ctx.moveTo(0, -p.radius);
      ctx.lineTo(p.radius, 0);
      ctx.lineTo(0, p.radius);
      ctx.lineTo(-p.radius, 0);
      ctx.closePath();
      ctx.fill();
      if (p.podType !== 'CORE') ctx.stroke();
      ctx.restore();
    }

    // ADDITIVE BLENDING PASS (High-FPS Neon Bloom without per-particle shadowBlur)
    ctx.save();
    ctx.globalCompositeOperation = 'lighter';

    for (let i = 0; i < shockwaves.length; i++) {
      const sw = shockwaves[i];
      ctx.beginPath();
      ctx.arc(sw.x, sw.y, sw.radius, 0, Math.PI * 2);
      ctx.strokeStyle = sw.color;
      ctx.globalAlpha = Math.max(0, sw.alpha);
      ctx.lineWidth = sw.lineWidth * sw.alpha;
      ctx.stroke();
    }

    for (let i = 0; i < laserBeams.length; i++) {
      const lb = laserBeams[i];
      const alpha = Math.max(0, lb.life / lb.maxLife);
      ctx.globalAlpha = alpha;
      ctx.strokeStyle = lb.color;
      ctx.lineWidth = 14 * alpha;
      ctx.beginPath();
      ctx.moveTo(lb.x1, lb.y1);
      ctx.lineTo(lb.x2, lb.y2);
      ctx.stroke();

      ctx.strokeStyle = '#ffffff';
      ctx.lineWidth = 4 * alpha;
      ctx.stroke();
    }

    for (let i = 0; i < particles.length; i++) {
      const pt = particles[i];
      ctx.globalAlpha = Math.max(0, pt.life / pt.maxLife);
      ctx.fillStyle = pt.color;
      ctx.beginPath();
      ctx.arc(pt.x, pt.y, pt.size, 0, Math.PI * 2);
      ctx.fill();
    }

    ctx.globalAlpha = 1;
    for (let i = 0; i < bullets.length; i++) {
      const b = bullets[i];
      ctx.save();
      ctx.translate(b.x, b.y);
      ctx.rotate(b.angle);
      ctx.fillStyle = b.color;
      ctx.beginPath();
      ctx.ellipse(0, 0, b.radius * 2.2, b.radius * 0.8, 0, 0, Math.PI * 2);
      ctx.fill();
      ctx.restore();
    }

    for (let i = 0; i < enemyProjectiles.length; i++) {
      const ep = enemyProjectiles[i];
      ctx.fillStyle = '#ff6a00';
      ctx.beginPath();
      ctx.arc(ep.x, ep.y, ep.radius, 0, Math.PI * 2);
      ctx.fill();
    }

    ctx.restore(); // End Additive Blending Pass

    // Enemy Squadron & Bosses
    for (let i = 0; i < enemies.length; i++) {
      drawEnemyFighter(enemies[i], time);
    }

    // Player Fighter Jet
    if (gameState === 'PLAYING' || gameState === 'PAUSED') {
      drawPlayerFighterJet(time);
    }

    // Floating Combat Telemetry
    ctx.textAlign = 'center';
    for (let i = 0; i < floatingTexts.length; i++) {
      const ft = floatingTexts[i];
      ctx.globalAlpha = Math.max(0, ft.life / ft.maxLife);
      ctx.font = `900 ${ft.size}px ${FONT_FAMILY}`;
      ctx.fillStyle = ft.color;
      ctx.fillText(ft.text, ft.x, ft.y);
    }
    ctx.globalAlpha = 1;

    // Airspace Wave Announcements
    for (let i = 0; i < banners.length; i++) {
      const b = banners[i];
      const alpha = Math.min(1, b.life * 2, (b.maxLife - b.life) * 3);
      ctx.globalAlpha = Math.max(0, alpha);
      ctx.fillStyle = b.color;
      ctx.font = `900 36px ${FONT_FAMILY}`;
      ctx.fillText(b.title, W / 2, H * 0.26);

      ctx.fillStyle = '#ffffff';
      ctx.font = `700 13px ${FONT_FAMILY}`;
      ctx.fillText(b.subtitle, W / 2, H * 0.26 + 26);
    }
    ctx.globalAlpha = 1;

    if (gameState === 'PAUSED') {
      ctx.fillStyle = 'rgba(3, 4, 10, 0.65)';
      ctx.fillRect(0, 0, W, H);
      ctx.fillStyle = '#00f3ff';
      ctx.font = `900 42px ${FONT_FAMILY}`;
      ctx.fillText('FLIGHT PAUSED', W / 2, H / 2);
    }

    if (screenFlash > 0) {
      ctx.globalAlpha = screenFlash * 0.32;
      ctx.fillStyle = screenFlashColor;
      ctx.fillRect(-50, -50, W + 100, H + 100);
      ctx.globalAlpha = 1;
    }

    ctx.restore();
  }

  function loop(now) {
    const dt = Math.min(0.05, (now - lastTime) / 1000);
    lastTime = now;
    update(dt);
    draw(now);
    requestAnimationFrame(loop);
  }

  requestAnimationFrame(loop);
})();
</script>
</body>
</html>
