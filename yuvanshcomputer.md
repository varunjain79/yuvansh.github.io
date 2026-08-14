---
layout: default
title: "Yuvansh's Computer"
permalink: /yuvanshcomputer/
---

<style>
  .computer-page {
    padding: 0 !important;
    overflow: hidden;
    background: #05080d !important;
    border-color: rgba(56, 189, 248, 0.35) !important;
  }

  .computer-shell {
    min-height: 680px;
    background:
      radial-gradient(circle at 20% 10%, rgba(56, 189, 248, 0.13), transparent 25%),
      radial-gradient(circle at 80% 90%, rgba(34, 197, 94, 0.10), transparent 30%),
      #05080d;
    color: #dff7ff;
    font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
  }

  .computer-topbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 12px;
    padding: 12px 16px;
    background: rgba(7, 14, 24, 0.96);
    border-bottom: 1px solid rgba(56, 189, 248, 0.20);
    position: sticky;
    top: 0;
    z-index: 5;
  }

  .computer-title { font-weight: 800; letter-spacing: 0.08em; }
  .computer-status { color: #86efac; font-size: 0.82rem; }

  .computer-body {
    display: grid;
    grid-template-columns: 230px 1fr;
    min-height: 625px;
  }

  .desktop {
    padding: 18px;
    border-right: 1px solid rgba(56, 189, 248, 0.16);
    background: rgba(3, 8, 14, 0.75);
  }

  .desktop h3 {
    margin: 0 0 14px;
    font-size: 0.9rem;
    color: #7dd3fc;
  }

  .desktop-button {
    width: 100%;
    border: 1px solid rgba(96, 165, 250, 0.18);
    background: rgba(15, 23, 42, 0.72);
    color: #e0f2fe;
    padding: 11px;
    border-radius: 10px;
    text-align: left;
    font: inherit;
    cursor: pointer;
    margin-bottom: 9px;
    transition: 0.18s ease;
  }

  .desktop-button:hover {
    transform: translateX(3px);
    border-color: rgba(56, 189, 248, 0.55);
    background: rgba(14, 45, 65, 0.82);
  }

  .workspace { padding: 20px; min-width: 0; }

  .terminal {
    min-height: 330px;
    border: 1px solid rgba(56, 189, 248, 0.20);
    border-radius: 14px;
    background: #020407;
    box-shadow: inset 0 0 35px rgba(0, 0, 0, 0.55), 0 12px 35px rgba(0, 0, 0, 0.25);
    overflow: hidden;
  }

  .terminal-head {
    padding: 9px 12px;
    background: #0a1018;
    border-bottom: 1px solid rgba(255,255,255,0.06);
    color: #94a3b8;
    font-size: 0.78rem;
  }

  #terminal-output {
    padding: 14px;
    min-height: 275px;
    max-height: 275px;
    overflow: auto;
    white-space: pre-wrap;
    color: #bbf7d0;
    font-size: 0.82rem;
    line-height: 1.55;
  }

  .command-row {
    display: flex;
    gap: 8px;
    padding: 10px 12px;
    border-top: 1px solid rgba(255,255,255,0.06);
  }

  #command-input {
    flex: 1;
    min-width: 0;
    border: 0;
    outline: 0;
    background: transparent;
    color: #e2e8f0;
    font: inherit;
  }

  .run-command {
    border: 1px solid rgba(34, 197, 94, 0.35);
    border-radius: 8px;
    background: rgba(34, 197, 94, 0.10);
    color: #bbf7d0;
    padding: 6px 10px;
    cursor: pointer;
    font: inherit;
  }

  .info-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 10px;
    margin-top: 12px;
  }

  .info-card {
    padding: 13px;
    border: 1px solid rgba(96, 165, 250, 0.15);
    border-radius: 12px;
    background: rgba(15, 23, 42, 0.58);
  }

  .info-card small { color: #94a3b8; display: block; margin-bottom: 5px; }
  .info-card strong { color: #e0f2fe; }

  .notice {
    margin-top: 12px;
    color: #94a3b8;
    font-size: 0.75rem;
    line-height: 1.5;
  }

  @media (max-width: 760px) {
    .computer-body { grid-template-columns: 1fr; }
    .desktop { border-right: 0; border-bottom: 1px solid rgba(56, 189, 248, 0.16); }
    .info-grid { grid-template-columns: 1fr; }
    .computer-shell { min-height: auto; }
  }
</style>

<div class="computer-page">
  <div class="computer-shell">
    <div class="computer-topbar">
      <div class="computer-title">YUVANSH COMPUTER // YJ-OS</div>
      <div class="computer-status">● ONLINE</div>
    </div>

    <div class="computer-body">
      <aside class="desktop">
        <h3>APPLICATIONS</h3>
        <button class="desktop-button" data-command="help">▣ Terminal</button>
        <button class="desktop-button" data-command="projects">▣ Projects</button>
        <button class="desktop-button" data-command="storage">▣ Storage</button>
        <button class="desktop-button" data-command="about">▣ System Info</button>
        <button class="desktop-button" data-command="secret">▣ Unknown</button>
      </aside>

      <section class="workspace">
        <div class="terminal">
          <div class="terminal-head">yuvansh@yj-os:~</div>
          <div id="terminal-output">YJ-OS boot sequence complete.\nWelcome to Yuvansh's Computer.\n\nType "help" to see available commands.\n</div>
          <div class="command-row">
            <span style="color:#38bdf8">&gt;</span>
            <input id="command-input" autocomplete="off" spellcheck="false" placeholder="type a command...">
            <button class="run-command" id="run-command">Run</button>
          </div>
        </div>

        <div class="info-grid">
          <div class="info-card"><small>STORAGE</small><strong>11 PB / 11 PB</strong></div>
          <div class="info-card"><small>MEMORY</small><strong>∞-ish</strong></div>
          <div class="info-card"><small>STATUS</small><strong>Everything is suspicious</strong></div>
        </div>

        <div class="notice">
          This is an interactive website simulation. The storage number and fictional projects are part of the experience; this page does not claim to provide 11 PB of real browser storage or access to private systems.
        </div>
      </section>
    </div>
  </div>
</div>

<script>
(() => {
  const output = document.getElementById('terminal-output');
  const input = document.getElementById('command-input');
  const run = document.getElementById('run-command');

  const commands = {
    help: [
      'Available commands:',
      '  help      - show this list',
      '  projects  - inspect the project archive',
      '  storage   - inspect the completely normal storage',
      '  about     - system information',
      '  secret    - attempt something questionable',
      '  clear     - clear the terminal'
    ],
    projects: [
      'PROJECT ARCHIVE',
      '----------------',
      '[001] YJ Assistant             STATUS: REAL',
      '[002] WaterElephant Browser    STATUS: REAL',
      '[003] Project Nebula           STATUS: DOES NOT EXIST',
      '[004] YJ Quantum Desktop       STATUS: DOES NOT EXIST',
      '[005] ???                       STATUS: CLASSIFIED',
      '',
      'Some project names are deliberately fictional.'
    ],
    storage: [
      'STORAGE DIAGNOSTICS',
      '-------------------',
      'Capacity:       11 PB',
      'Used:           11 PB',
      'Free:            0 bytes',
      'Filesystem:      YJ-FS',
      '',
      'WARNING: The displayed capacity is part of the simulation.'
    ],
    about: [
      'YJ-OS SYSTEM INFORMATION',
      '-------------------------',
      'Computer:       Yuvansh Computer',
      'Operating Sys:  YJ-OS',
      'Build:          SECRET-0xYJ',
      'Network:        WEBSITE',
      'Reality level:  Questionable'
    ],
    secret: [
      'ACCESSING UNKNOWN APPLICATION...',
      'Checking permissions...',
      'Checking reality...',
      'Reality check: FAILED',
      '',
      'You found something that was not supposed to be interesting.',
      'Congratulations. 🌀'
    ]
  };

  function print(lines) {
    output.textContent += (Array.isArray(lines) ? lines.join('\n') : lines) + '\n';
    output.scrollTop = output.scrollHeight;
  }

  function execute(raw) {
    const command = raw.trim().toLowerCase();
    if (!command) return;
    print('yuvansh@yj-os:~$ ' + command);
    if (command === 'clear') {
      output.textContent = '';
      return;
    }
    if (commands[command]) {
      print(commands[command]);
    } else {
      print('Command not found. Try "help".');
    }
  }

  run.addEventListener('click', () => {
    execute(input.value);
    input.value = '';
    input.focus();
  });

  input.addEventListener('keydown', event => {
    if (event.key === 'Enter') {
      execute(input.value);
      input.value = '';
    }
  });

  document.querySelectorAll('[data-command]').forEach(button => {
    button.addEventListener('click', () => execute(button.dataset.command));
  });
})();
</script>
