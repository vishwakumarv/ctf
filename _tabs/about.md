---
title: About
icon: fas fa-info-circle
order: 4
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Syne:wght@400;500;600;700&display=swap');

#ab {
  --bg:         #0d1117;
  --surface:    #111820;
  --surface-2:  #161d27;
  --border:     #1e2936;
  --border-hi:  #2a3a4a;
  --fg:         #e6edf3;
  --fg-2:       #8b949e;
  --fg-3:       #3d4f5e;
  --cyan:       #00ffd1;
  --cyan-dim:   rgba(0,255,209,0.07);
  --cyan-glow:  rgba(0,255,209,0.18);
  --orange:     #ff6b35;

  font-family: 'Syne', sans-serif;
  color: var(--fg);
  max-width: 780px;
  margin: 0 auto;
  padding: 2rem 1.5rem 5rem;
  background: transparent;
}

#ab * { box-sizing: border-box; margin: 0; padding: 0; }
#ab a { color: inherit; text-decoration: none; }

mono { font-family: 'Share Tech Mono', monospace; }

/* ── HERO ── */
.hero {
  padding: 2rem 0 2.5rem;
  border-bottom: 1px solid var(--border);
  margin-bottom: 3rem;
}

.hero-label {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.7rem;
  color: var(--cyan);
  letter-spacing: 0.2em;
  text-transform: uppercase;
  margin-bottom: 1rem;
}

.hero-name {
  font-size: clamp(2.4rem, 6vw, 3.8rem);
  font-weight: 700;
  letter-spacing: -0.04em;
  line-height: 0.95;
  color: var(--fg);
  margin-bottom: 1.25rem;
}

.hero-name span {
  color: var(--cyan);
}

.hero-bio {
  font-size: 1rem;
  color: var(--fg-2);
  line-height: 1.8;
  max-width: 520px;
  font-weight: 400;
  margin-bottom: 1.75rem;
}

.hero-bio strong { color: var(--fg); font-weight: 600; }

/* ── LINKS ── */
.links {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.lnk {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.72rem;
  letter-spacing: 0.06em;
  color: var(--fg-2);
  border: 1px solid var(--border);
  padding: 0.4rem 0.9rem;
  border-radius: 4px;
  transition: all 0.18s;
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
}

.lnk:hover {
  color: var(--cyan);
  border-color: var(--cyan);
  background: var(--cyan-dim);
  box-shadow: 0 0 12px var(--cyan-glow);
}

/* ── SECTION ── */
.sec { margin-bottom: 3rem; }

.sec-head {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.68rem;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--fg-3);
  margin-bottom: 1.25rem;
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.sec-head::before {
  content: '//';
  color: var(--cyan);
}

.sec-head::after {
  content: '';
  flex: 1;
  height: 1px;
  background: var(--border);
}

/* ── TERMINAL BLOCK ── */
.term {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  overflow: hidden;
  font-family: 'Share Tech Mono', monospace;
}

.term-bar {
  background: var(--surface-2);
  border-bottom: 1px solid var(--border);
  padding: 0.6rem 1rem;
  display: flex;
  align-items: center;
  gap: 0.45rem;
}

.dot { width: 11px; height: 11px; border-radius: 50%; }
.dot-r { background: #ff5f57; }
.dot-y { background: #febc2e; }
.dot-g { background: #28c840; }

.term-title {
  font-size: 0.7rem;
  color: var(--fg-3);
  margin-left: auto;
  margin-right: auto;
  letter-spacing: 0.04em;
}

.term-body {
  padding: 1.25rem 1.5rem;
  font-size: 0.82rem;
  line-height: 2;
  color: var(--fg-2);
}

.t-prompt { color: var(--cyan); }
.t-dim    { color: var(--fg-3); }
.t-key    { color: var(--cyan); display: inline-block; min-width: 80px; }
.t-val    { color: var(--fg); }
.t-cursor {
  display: inline-block;
  width: 8px; height: 1em;
  background: var(--fg-2);
  vertical-align: text-bottom;
  animation: blink 1s step-end infinite;
  margin-left: 2px;
}

@keyframes blink { 50% { opacity: 0; } }

/* ── STAT STRIP ── */
.stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(110px, 1fr));
  gap: 0.75rem;
  margin: 1.5rem 0;
}

.stat {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 6px;
  padding: 1rem 0.75rem;
  text-align: center;
  transition: border-color 0.2s;
}

.stat:hover { border-color: var(--cyan); }

.stat-n {
  font-family: 'Share Tech Mono', monospace;
  font-size: 2rem;
  font-weight: 400;
  color: var(--cyan);
  display: block;
  line-height: 1;
}

.stat-l {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.62rem;
  color: var(--fg-3);
  text-transform: uppercase;
  letter-spacing: 0.12em;
  margin-top: 0.35rem;
  display: block;
}

/* ── DOMAINS ── */
.domains {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(210px, 1fr));
  gap: 0.6rem;
}

.dom {
  background: var(--surface);
  border: 1px solid var(--border);
  border-left: 2px solid var(--cyan);
  border-radius: 0 6px 6px 0;
  padding: 0.7rem 1rem;
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.78rem;
  color: var(--fg-2);
  transition: all 0.18s;
}

.dom:hover {
  color: var(--fg);
  background: var(--cyan-dim);
  border-color: var(--cyan);
}

.dom-sub {
  font-size: 0.65rem;
  color: var(--fg-3);
  margin-top: 0.2rem;
}

/* ── TOOLS ── */
.tools {
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem;
}

.tool {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.72rem;
  color: var(--fg-2);
  background: var(--surface);
  border: 1px solid var(--border);
  padding: 0.3rem 0.7rem;
  border-radius: 4px;
  transition: all 0.15s;
}

.tool:hover {
  color: var(--cyan);
  border-color: var(--cyan);
  background: var(--cyan-dim);
}

/* ── EXPERIENCE ── */
.exp-item {
  padding: 1.25rem 0;
  border-bottom: 1px solid var(--border);
  display: grid;
  grid-template-columns: 1fr auto;
  gap: 0.25rem 1rem;
}

.exp-item:first-child { padding-top: 0; }
.exp-item:last-child  { border-bottom: none; }

.exp-role {
  font-size: 0.95rem;
  font-weight: 600;
  color: var(--fg);
}

.exp-co {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.72rem;
  color: var(--cyan);
  margin-top: 0.15rem;
}

.exp-yr {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.68rem;
  color: var(--fg-3);
  text-align: right;
  padding-top: 0.2rem;
}

.exp-pts {
  grid-column: 1 / -1;
  list-style: none;
  margin-top: 0.6rem;
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
}

.exp-pts li {
  font-size: 0.82rem;
  color: var(--fg-2);
  padding-left: 1.1rem;
  position: relative;
  line-height: 1.5;
}

.exp-pts li::before {
  content: '▸';
  position: absolute;
  left: 0;
  color: var(--cyan);
  font-size: 0.65rem;
  top: 0.15em;
}

/* ── PROJECTS ── */
.projects { display: grid; gap: 0.7rem; }

.proj {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 1.25rem 1.4rem;
  display: grid;
  grid-template-columns: 1fr auto;
  gap: 0.3rem 1rem;
  align-items: start;
  transition: border-color 0.2s, box-shadow 0.2s;
}

.proj:hover {
  border-color: var(--border-hi);
  box-shadow: 0 4px 24px rgba(0,0,0,0.4);
}

.proj-name {
  font-size: 0.95rem;
  font-weight: 600;
  color: var(--fg);
}

.proj-link {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.68rem;
  color: var(--cyan);
  text-align: right;
  transition: opacity 0.15s;
}

.proj-link:hover { opacity: 0.7; }

.proj-desc {
  grid-column: 1 / -1;
  font-size: 0.82rem;
  color: var(--fg-2);
  line-height: 1.65;
  margin-top: 0.2rem;
}

.proj-tags {
  grid-column: 1 / -1;
  display: flex;
  flex-wrap: wrap;
  gap: 0.35rem;
  margin-top: 0.7rem;
}

.proj-tag {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.65rem;
  color: var(--fg-3);
  border: 1px solid var(--border);
  padding: 0.15rem 0.5rem;
  border-radius: 3px;
}

/* ── CTF TABLE ── */
.ctf-table {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.82rem;
}

.ctf-table th {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.65rem;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--fg-3);
  text-align: left;
  padding: 0 0.75rem 0.75rem;
  border-bottom: 1px solid var(--border);
}

.ctf-table td {
  padding: 0.75rem;
  border-bottom: 1px solid var(--border);
  color: var(--fg-2);
  vertical-align: middle;
}

.ctf-table tr:last-child td { border-bottom: none; }
.ctf-table tr:hover td { background: var(--cyan-dim); }

.ctf-name { color: var(--fg); font-weight: 500; }
.ctf-cat  { font-family: 'Share Tech Mono', monospace; font-size: 0.7rem; color: var(--fg-3); }

.ctf-badge {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.65rem;
  color: var(--cyan);
  border: 1px solid rgba(0,255,209,0.25);
  background: var(--cyan-dim);
  padding: 0.15rem 0.55rem;
  border-radius: 3px;
  white-space: nowrap;
}

/* ── GITHUB STATS ── */
.gh-stats {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.75rem;
}

.gh-stats img {
  width: 100%;
  border-radius: 6px;
  border: 1px solid var(--border);
  display: block;
}

.gh-graph {
  margin-top: 0.75rem;
  border-radius: 6px;
  border: 1px solid var(--border);
  overflow: hidden;
}

.gh-graph img { width: 100%; display: block; }

/* ── FOOTER ── */
.foot {
  margin-top: 3.5rem;
  padding-top: 1.75rem;
  border-top: 1px solid var(--border);
}

.foot-term {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.78rem;
  color: var(--fg-2);
  line-height: 2;
}

.foot-term .t-prompt { color: var(--cyan); }
.foot-term .output   { color: var(--fg); }

.foot-links {
  display: flex;
  gap: 1.25rem;
  margin-top: 1.25rem;
  flex-wrap: wrap;
}

.foot-link {
  font-family: 'Share Tech Mono', monospace;
  font-size: 0.7rem;
  color: var(--fg-3);
  transition: color 0.15s;
}

.foot-link:hover { color: var(--cyan); }

/* ── RESPONSIVE ── */
@media (max-width: 540px) {
  .gh-stats { grid-template-columns: 1fr; }
  .hero-name { font-size: 2.2rem; }
}
</style>

<div id="ab">

<!-- HERO -->
<div class="hero">
  <div class="hero-label">$ whoami</div>
  <div class="hero-name">V <span>Vishwa</span> Kumar</div>
  <p class="hero-bio">
    ECE student obsessed with how systems actually work — and more interestingly, how they break.
    I work at the intersection of <strong>offensive security</strong>, <strong>reverse engineering</strong>,
    and <strong>low-level systems</strong>. Android internals, malware tracing, Frida instrumentation,
    embedded things that probably shouldn't exist. Most of it started as
    <em>"I wonder what happens if..."</em> at 2AM.
  </p>
  <div class="links">
    <a class="lnk" href="https://github.com/vishwakumarv">⌥ GitHub</a>
    <a class="lnk" href="https://www.linkedin.com/in/vishwakumarv/">in LinkedIn</a>
    <a class="lnk" href="https://app.hackthebox.com/users/2569138">⬡ HackTheBox</a>
    <a class="lnk" href="https://tryhackme.com/p/vkumxr">⚑ TryHackMe</a>
    <a class="lnk" href="mailto:vishwakumarv05@gmail.com">✉ Email</a>
    <a class="lnk" href="https://buymeacoffee.com/vishwakumarv">☕ Buy Me Coffee</a>
  </div>
</div>

<!-- WHOAMI TERMINAL -->
<div class="sec">
  <div class="sec-head">init</div>
  <div class="term">
    <div class="term-bar">
      <div class="dot dot-r"></div>
      <div class="dot dot-y"></div>
      <div class="dot dot-g"></div>
      <div class="term-title">vishwa@kali — ~</div>
    </div>
    <div class="term-body">
      <div><span class="t-prompt">vishwa@kali</span><span class="t-dim">:~$ </span>cat whoami.txt</div>
      <br>
      <div><span class="t-key">Name  </span><span class="t-dim">: </span><span class="t-val">V Vishwa Kumar</span></div>
      <div><span class="t-key">Role  </span><span class="t-dim">: </span><span class="t-val">ECE Student → Cybersecurity Researcher</span></div>
      <div><span class="t-key">College</span><span class="t-dim">: </span><span class="t-val">PSG College of Technology, Coimbatore</span></div>
      <div><span class="t-key">Focus </span><span class="t-dim">: </span><span class="t-val">RE · Android Internals · Offensive Security · Embedded</span></div>
      <div><span class="t-key">OS    </span><span class="t-dim">: </span><span class="t-val">Kali Linux / Parrot OS Security</span></div>
      <div><span class="t-key">Motto </span><span class="t-dim">: </span><span style="color:#ffa657;">"Most of my work starts with curiosity."</span></div>
      <br>
      <div><span class="t-prompt">vishwa@kali</span><span class="t-dim">:~$ </span><span class="t-cursor"></span></div>
    </div>
  </div>
</div>

<!-- STATS -->
<div class="stats">
  <div class="stat"><span class="stat-n">8</span><span class="stat-l">CTFs</span></div>
  <div class="stat"><span class="stat-n">3</span><span class="stat-l">Internships</span></div>
  <div class="stat"><span class="stat-n">3</span><span class="stat-l">Projects</span></div>
  <div class="stat"><span class="stat-n">4+</span><span class="stat-l">Years Kali</span></div>
  <div class="stat"><span class="stat-n">12</span><span class="stat-l">Tools</span></div>
</div>

<!-- DOMAINS -->
<div class="sec">
  <div class="sec-head">research domains</div>
  <div class="domains">
    <div class="dom">Reverse Engineering<div class="dom-sub">static &amp; dynamic analysis</div></div>
    <div class="dom">Android Internals<div class="dom-sub">ART, DEX, native layers</div></div>
    <div class="dom">Malware Analysis<div class="dom-sub">behavioral, structural</div></div>
    <div class="dom">Dynamic Instrumentation<div class="dom-sub">Frida, hooking, tracing</div></div>
    <div class="dom">Offensive Security<div class="dom-sub">pentesting, recon, enum</div></div>
    <div class="dom">Embedded / IoT<div class="dom-sub">ESP32, firmware, Matter</div></div>
    <div class="dom">Linux Internals<div class="dom-sub">kernel, ELF, syscalls</div></div>
    <div class="dom">CTF Research<div class="dom-sub">crypto, forensics, web</div></div>
  </div>
</div>

<!-- TOOLS -->
<div class="sec">
  <div class="sec-head">toolchain</div>
  <div class="tools">
    <span class="tool">Ghidra</span>
    <span class="tool">radare2</span>
    <span class="tool">GDB + pwndbg</span>
    <span class="tool">Frida</span>
    <span class="tool">objection</span>
    <span class="tool">apktool / jadx</span>
    <span class="tool">Burp Suite</span>
    <span class="tool">Nmap / ffuf</span>
    <span class="tool">Wireshark</span>
    <span class="tool">Volatility</span>
    <span class="tool">YARA</span>
    <span class="tool">Metasploit</span>
    <span class="tool">Python</span>
    <span class="tool">Bash</span>
    <span class="tool">C</span>
    <span class="tool">Docker</span>
    <span class="tool">QEMU</span>
    <span class="tool">CyberChef</span>
  </div>
</div>

<!-- PROJECTS -->
<div class="sec">
  <div class="sec-head">projects</div>
  <div class="projects">
    <div class="proj">
      <div class="proj-name">ReDroid-AI</div>
      <a class="proj-link" href="https://github.com/vishwakumarv">↗ view</a>
      <div class="proj-desc">LLM-augmented static analysis pipeline for Android APK reverse engineering. Automated decompilation, triage, and reporting workflows powered by large language models.</div>
      <div class="proj-tags">
        <span class="proj-tag">Android</span>
        <span class="proj-tag">Reverse Engineering</span>
        <span class="proj-tag">LLM</span>
        <span class="proj-tag">Python</span>
      </div>
    </div>
    <div class="proj">
      <div class="proj-name">DEADPIXEL</div>
      <a class="proj-link" href="https://github.com/vishwakumarv">↗ view</a>
      <div class="proj-desc">Modular phishing simulation toolkit for security-awareness research in controlled environments. Configurable campaign framework built for red team exercises.</div>
      <div class="proj-tags">
        <span class="proj-tag">Red Team</span>
        <span class="proj-tag">Phishing</span>
        <span class="proj-tag">Python</span>
      </div>
    </div>
    <div class="proj">
      <div class="proj-name">PuBOT</div>
      <a class="proj-link" href="https://github.com/vishwakumarv">↗ view</a>
      <div class="proj-desc">Raspberry Pi–based autonomous navigation robot. Real-time sensor fusion, motor control, and hardware/software boundary exploration.</div>
      <div class="proj-tags">
        <span class="proj-tag">Embedded</span>
        <span class="proj-tag">Raspberry Pi</span>
        <span class="proj-tag">IoT</span>
        <span class="proj-tag">Python</span>
      </div>
    </div>
  </div>
</div>

<!-- EXPERIENCE -->
<div class="sec">
  <div class="sec-head">experience</div>
  <div class="exp-item">
    <div>
      <div class="exp-role">Offensive Cybersecurity Intern</div>
      <div class="exp-co">InlighnX Global</div>
    </div>
    <div class="exp-yr">2024</div>
    <ul class="exp-pts">
      <li>Vulnerability assessment and pentesting labs</li>
      <li>Security scripting and automation in Python / Bash</li>
      <li>Recon, enumeration, and hashing workflows</li>
    </ul>
  </div>
  <div class="exp-item">
    <div>
      <div class="exp-role">Machine Learning Intern</div>
      <div class="exp-co">Saiket Systems</div>
    </div>
    <div class="exp-yr">2024</div>
    <ul class="exp-pts">
      <li>Classification &amp; anomaly-detection workflows</li>
      <li>Applied ML on security-relevant datasets</li>
      <li>Preprocessing &amp; model experimentation</li>
    </ul>
  </div>
  <div class="exp-item">
    <div>
      <div class="exp-role">Embedded Systems Intern</div>
      <div class="exp-co">Wimera Systems</div>
    </div>
    <div class="exp-yr">2023</div>
    <ul class="exp-pts">
      <li>ESP32-based IoT and embedded workflows</li>
      <li>Dashboard monitoring and device testing</li>
      <li>Matter protocol &amp; smart-device communication</li>
    </ul>
  </div>
</div>

<!-- CTF LOG -->
<div class="sec">
  <div class="sec-head">ctf log</div>
  <div class="term">
    <div class="term-bar">
      <div class="dot dot-r"></div>
      <div class="dot dot-y"></div>
      <div class="dot dot-g"></div>
      <div class="term-title">ctf_log.txt</div>
    </div>
    <div class="term-body" style="padding: 0;">
      <table class="ctf-table">
        <thead>
          <tr>
            <th>Competition</th>
            <th>Category</th>
            <th>Status</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td><span class="ctf-name">picoCTF</span><br><span class="ctf-cat">MultiCode · Password Profiler · StegoRSA</span></td>
            <td><span class="ctf-cat">Crypto · Forensics · Stego</span></td>
            <td><span class="ctf-badge">✓ solved</span></td>
          </tr>
          <tr>
            <td><span class="ctf-name">MIRAGE CTF</span></td>
            <td><span class="ctf-cat">OSINT · Forensics</span></td>
            <td><span class="ctf-badge">✓ flagged</span></td>
          </tr>
          <tr>
            <td><span class="ctf-name">HackZero CTF</span><br><span class="ctf-cat">Turla APT series</span></td>
            <td><span class="ctf-cat">Threat Intel · Malware</span></td>
            <td><span class="ctf-badge">✓ completed</span></td>
          </tr>
          <tr>
            <td><span class="ctf-name">DevTrails CTF 2026</span></td>
            <td><span class="ctf-cat">Docker · Web · Misc</span></td>
            <td><span class="ctf-badge">✓ all 5 flags</span></td>
          </tr>
          <tr>
            <td><span class="ctf-name">Bypass CTF 2025</span></td>
            <td><span class="ctf-cat">Multi-category</span></td>
            <td><span class="ctf-badge">participated</span></td>
          </tr>
          <tr>
            <td><span class="ctf-name">Yukthi CTF 2.0</span></td>
            <td><span class="ctf-cat">Multi-category</span></td>
            <td><span class="ctf-badge">participated</span></td>
          </tr>
          <tr>
            <td><span class="ctf-name">BlockChain CTF</span></td>
            <td><span class="ctf-cat">Blockchain · Web3</span></td>
            <td><span class="ctf-badge">participated</span></td>
          </tr>
          <tr>
            <td><span class="ctf-name">Vibe Hack</span></td>
            <td><span class="ctf-cat">Multi-category</span></td>
            <td><span class="ctf-badge">participated</span></td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
  <p style="font-family:'Share Tech Mono',monospace; font-size:0.72rem; color:var(--fg-3); margin-top:0.75rem;">
    → Full writeups: <a href="/tags/" style="color:var(--cyan);">browse by tag</a> · <a href="/archives/" style="color:var(--cyan);">archives</a>
  </p>
</div>

<!-- GITHUB STATS -->
<div class="sec">
  <div class="sec-head">github stats</div>
  <div class="gh-stats">
    <img src="https://github-readme-stats.vercel.app/api?username=vishwakumarv&show_icons=true&theme=transparent&hide_border=true&title_color=00ffd1&icon_color=00ffd1&text_color=8b949e&bg_color=111820" alt="GitHub Stats" />
    <img src="https://github-readme-streak-stats.herokuapp.com/?user=vishwakumarv&theme=transparent&hide_border=true&background=111820&stroke=1e2936&ring=00ffd1&fire=ff6b35&currStreakLabel=00ffd1&sideLabels=8b949e&dates=3d4f5e" alt="GitHub Streak" />
  </div>
  <div class="gh-graph">
    <img src="https://github-readme-activity-graph.vercel.app/graph?username=vishwakumarv&bg_color=111820&color=00ffd1&line=00ffd1&point=ffffff&area=true&hide_border=true&area_color=00ffd1" alt="Activity Graph" />
  </div>
</div>

<!-- FOOTER -->
<div class="foot">
  <div class="foot-term">
    <div><span class="t-prompt">vishwa@kali</span><span class="t-dim">:~$ </span>echo "Thanks for visiting. Now go break something."</div>
    <div class="output">Thanks for visiting. Now go break something.</div>
    <div style="margin-top:0.25rem;"><span class="t-prompt">vishwa@kali</span><span class="t-dim">:~$ </span><span class="t-cursor"></span></div>
  </div>
  <div class="foot-links">
    <a class="foot-link" href="https://github.com/vishwakumarv">GitHub</a>
    <a class="foot-link" href="https://www.linkedin.com/in/vishwakumarv/">LinkedIn</a>
    <a class="foot-link" href="https://app.hackthebox.com/users/2569138">HackTheBox</a>
    <a class="foot-link" href="https://tryhackme.com/p/vkumxr">TryHackMe</a>
    <a class="foot-link" href="mailto:vishwakumarv05@gmail.com">Email</a>
    <a class="foot-link" href="https://buymeacoffee.com/vishwakumarv">Buy Me Coffee</a>
  </div>
</div>

</div>
