

  .modal-col-right {
   
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
  let enemie
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
