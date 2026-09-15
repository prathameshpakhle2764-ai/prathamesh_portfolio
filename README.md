<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Prathamesh Pakhale — VLSI Design Verification Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;600;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg-base:#0B0F14;
    --bg-surface:#121821;
    --bg-elevated:#1A222C;
    --border:#25303C;
    --border-soft:#1D2630;
    --text-primary:#E7ECF1;
    --text-muted:#8B98A6;
    --text-dim:#5B6B7A;
    --amber:#E8A33D;
    --amber-dim:#8A6427;
    --cyan:#5FD6C6;
    --green:#5FD68A;
    --mono: 'JetBrains Mono', ui-monospace, monospace;
    --sans: 'Inter', -apple-system, sans-serif;
    --maxw: 920px;
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--bg-base);
    color:var(--text-primary);
    font-family:var(--sans);
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  @media (prefers-reduced-motion: reduce){
    html{scroll-behavior:auto;}
    *{animation-duration:0.001ms !important; animation-iteration-count:1 !important; transition-duration:0.001ms !important;}
  }

  a{color:var(--cyan); text-decoration:none;}
  a:hover{text-decoration:underline;}
  :focus-visible{outline:2px solid var(--amber); outline-offset:2px;}

  .wrap{max-width:var(--maxw); margin:0 auto; padding:0 24px;}

  /* ---------- Editor chrome ---------- */
  .editor-titlebar{
    display:flex; align-items:center; gap:10px;
    padding:10px 18px;
    background:var(--bg-surface);
    border-bottom:1px solid var(--border);
  }
  .dot{width:11px; height:11px; border-radius:50%;}
  .dot.red{background:#4a3030;} .dot.yellow{background:#4a4230;} .dot.green{background:#2f4a35;}
  .titlebar-name{
    margin-left:8px; font-family:var(--mono); font-size:12.5px; color:var(--text-dim);
  }

  .tabbar{
    position:sticky; top:0; z-index:50;
    display:flex; overflow-x:auto;
    background:var(--bg-surface);
    border-bottom:1px solid var(--border);
    scrollbar-width:none;
  }
  .tabbar::-webkit-scrollbar{display:none;}
  .tab{
    font-family:var(--mono); font-size:13px; white-space:nowrap;
    padding:12px 20px; color:var(--text-muted);
    border-right:1px solid var(--border-soft);
    border-bottom:2px solid transparent;
    cursor:pointer; background:transparent;
  }
  .tab:hover{color:var(--text-primary); text-decoration:none;}
  .tab.active{color:var(--amber); border-bottom-color:var(--amber); background:var(--bg-elevated);}
  .tab .dim{color:var(--text-dim);}

  /* ---------- Gutter / line-number panels ---------- */
  section{
    position:relative;
    padding:64px 0 64px 56px;
    border-bottom:1px solid var(--border-soft);
  }
  section::before{
    content:attr(data-ln);
    position:absolute;
    left:0; top:64px;
    width:40px;
    font-family:var(--mono);
    font-size:12px;
    color:var(--text-dim);
    text-align:right;
    padding-right:14px;
    border-right:1px solid var(--border-soft);
    white-space:pre-line;
    line-height:2.1;
  }
  @media (max-width:640px){
    section{padding-left:40px;}
    section::before{width:28px; font-size:10px; padding-right:8px;}
  }

  .kicker{
    font-family:var(--mono); font-size:12.5px; color:var(--cyan);
    margin:0 0 14px 0;
  }
  .kicker::before{content:'// ';}
  h2{
    font-family:var(--sans); font-weight:700; font-size:28px;
    margin:0 0 28px 0; color:var(--text-primary); letter-spacing:-0.01em;
  }

  /* ---------- Hero ---------- */
  .hero{
    padding:72px 0 56px 56px;
    border-bottom:1px solid var(--border-soft);
  }
  @media (max-width:640px){.hero{padding-left:40px;}}
  .hero-grid{
    display:flex; align-items:center; justify-content:space-between; gap:48px;
  }
  .hero-text{flex:1; min-width:280px;}
  .code-line{font-family:var(--mono); font-size:14.5px; color:var(--text-muted);}
  .code-line .kw{color:#C586C0;}
  .code-line .fn{color:var(--cyan);}
  .code-line .str{color:var(--green);}
  .code-line .cm{color:var(--text-dim);}

  .hero-name{
    font-family:var(--sans); font-weight:700;
    font-size:clamp(32px, 5vw, 46px);
    margin:18px 0 6px 0;
    letter-spacing:-0.02em;
  }
  .cursor{
    display:inline-block; width:3px; height:0.85em;
    background:var(--amber); margin-left:4px;
    animation:blink 1s steps(1) infinite;
    vertical-align:-2px;
  }
  @keyframes blink{ 50%{opacity:0;} }

  .hero-role{
    font-family:var(--mono); font-size:15px; color:var(--amber); margin:0 0 18px 0;
  }
  .hero-desc{color:var(--text-muted); max-width:52ch; margin:0 0 28px 0;}

  .status-chip{
    display:inline-flex; align-items:center; gap:8px;
    font-family:var(--mono); font-size:12.5px; color:var(--green);
    background:rgba(95,214,138,0.08);
    border:1px solid rgba(95,214,138,0.25);
    padding:6px 12px; border-radius:3px; margin-bottom:28px;
  }
  .status-chip .pulse{
    width:7px; height:7px; border-radius:50%; background:var(--green);
    animation:pulse 1.8s ease-in-out infinite;
  }
  @keyframes pulse{ 0%,100%{opacity:1;} 50%{opacity:0.35;} }

  .btn-row{display:flex; gap:12px; flex-wrap:wrap;}
  .btn{
    font-family:var(--mono); font-size:13px;
    padding:11px 18px; border-radius:3px;
    border:1px solid var(--border);
    display:inline-flex; align-items:center; gap:8px;
  }
  .btn:hover{text-decoration:none;}
  .btn-primary{background:var(--amber); color:#1a1206; border-color:var(--amber); font-weight:600;}
  .btn-primary:hover{background:#f0b458;}
  .btn-ghost{color:var(--text-primary); background:transparent;}
  .btn-ghost:hover{border-color:var(--cyan); color:var(--cyan);}

  .hero-photo-wrap{
    flex-shrink:0; position:relative; width:180px; height:180px;
  }
  .hero-photo-wrap img{
    width:180px; height:180px; border-radius:50%; object-fit:cover;
    border:2px solid var(--amber-dim);
  }
  @media (max-width:640px){
    .hero-grid{flex-direction:column-reverse; align-items:flex-start;}
    .hero-photo-wrap{width:120px; height:120px;}
    .hero-photo-wrap img{width:120px; height:120px;}
  }

  /* ---------- Waveform divider ---------- */
  .waveform{display:block; width:100%; height:28px; opacity:0.5;}

  /* ---------- About ---------- */
  .about-body{color:var(--text-muted); max-width:68ch;}
  .about-body p{margin:0 0 16px 0;}

  /* ---------- Skills ---------- */
  .skill-group{margin-bottom:32px;}
  .skill-group:last-child{margin-bottom:0;}
  .skill-group-label{
    font-family:var(--mono); font-size:12px; color:var(--text-dim);
    text-transform:lowercase; margin-bottom:12px;
  }
  .pills{display:flex; flex-wrap:wrap; gap:9px;}
  .pill{
    font-family:var(--mono); font-size:13px;
    padding:7px 13px; border-radius:3px;
    border:1px solid var(--border); color:var(--text-primary);
    background:var(--bg-surface);
  }
  .pill.advancing{border-color:rgba(232,163,61,0.35); color:var(--amber); background:rgba(232,163,61,0.06);}

  /* ---------- Projects ---------- */
  .project-card{
    border:1px solid var(--border); border-radius:4px;
    background:var(--bg-surface);
    padding:22px 24px; margin-bottom:18px;
  }
  .project-head{
    display:flex; align-items:baseline; justify-content:space-between; gap:12px;
    flex-wrap:wrap; margin-bottom:10px;
  }
  .project-title{font-family:var(--sans); font-weight:600; font-size:17px; color:var(--text-primary);}
  .project-title .ext{color:var(--text-dim); font-family:var(--mono); font-weight:400; font-size:14px;}
  .wip-chip{
    font-family:var(--mono); font-size:11px; color:var(--amber);
    border:1px solid rgba(232,163,61,0.35); padding:3px 8px; border-radius:3px;
    white-space:nowrap;
  }
  .project-desc{color:var(--text-muted); font-size:14.5px; margin:0 0 14px 0;}
  .tag-row{display:flex; flex-wrap:wrap; gap:8px;}
  .tag{
    font-family:var(--mono); font-size:11.5px; color:var(--cyan);
    background:rgba(95,214,198,0.07); border:1px solid rgba(95,214,198,0.2);
    padding:4px 9px; border-radius:3px;
  }

  /* ---------- Education ---------- */
  .edu-row{
    display:flex; justify-content:space-between; gap:16px;
    padding:16px 0; border-bottom:1px solid var(--border-soft);
  }
  .edu-row:last-child{border-bottom:none;}
  .edu-degree{font-weight:600; font-size:15.5px;}
  .edu-school{color:var(--text-muted); font-size:14px; margin-top:3px;}
  .edu-meta{color:var(--amber); font-family:var(--mono); font-size:13px;}
  .edu-year{color:var(--text-dim); font-family:var(--mono); font-size:12.5px; white-space:nowrap;}

  .cert-line{color:var(--text-muted); font-size:14.5px;}
  .cert-line strong{color:var(--text-primary);}

  /* ---------- Contact / footer ---------- */
  .contact-terminal{
    background:var(--bg-surface); border:1px solid var(--border); border-radius:4px;
    padding:22px 24px; font-family:var(--mono); font-size:14px;
  }
  .contact-terminal .line{margin-bottom:10px; color:var(--text-muted);}
  .contact-terminal .line:last-child{margin-bottom:0;}
  .prompt{color:var(--green);}
  .contact-terminal a{color:var(--text-primary);}
  .contact-terminal a:hover{color:var(--cyan);}

  footer{padding:32px 0 40px 56px; }
  @media (max-width:640px){footer{padding-left:40px;}}
  .footer-note{font-family:var(--mono); font-size:12px; color:var(--text-dim);}
</style>
</head>
<body>

  <div class="editor-titlebar">
    <span class="dot red"></span><span class="dot yellow"></span><span class="dot green"></span>
    <span class="titlebar-name">prathamesh_pakhale — portfolio</span>
  </div>

  <nav class="tabbar" id="tabbar">
    <a class="tab active" href="#about">about<span class="dim">.sv</span></a>
    <a class="tab" href="#skills">skills<span class="dim">.sv</span></a>
    <a class="tab" href="#projects">projects<span class="dim">.sv</span></a>
    <a class="tab" href="#education">education<span class="dim">.sv</span></a>
    <a class="tab" href="#contact">contact<span class="dim">.sv</span></a>
  </nav>

  <header class="hero" id="top">
    <div class="wrap">
      <div class="hero-grid">
        <div class="hero-text">
          <div class="code-line">
            <span class="kw">module</span> <span class="fn">prathamesh_pakhale</span> <span class="cm">#(</span>
          </div>
          <div class="code-line">&nbsp;&nbsp;.ROLE(<span class="str">"VLSI Design Verification Engineer"</span>),</div>
          <div class="code-line">&nbsp;&nbsp;.BASE(<span class="str">"Karad, Maharashtra"</span>)</div>
          <div class="code-line"><span class="cm">);</span></div>

          <h1 class="hero-name">Prathamesh Pakhale<span class="cursor" aria-hidden="true"></span></h1>
          <p class="hero-role">Electronics &amp; Telecommunication Engineer — Aspiring DV Engineer</p>
          <p class="hero-desc">Final-year engineering student building a self-directed path into VLSI Design Verification — SystemVerilog, UVM, and timing-aware RTL — currently assembling a pipelined RISC core to prove it end to end.</p>

          <div><span class="status-chip"><span class="pulse"></span>open to DV roles — Pune / Bengaluru</span></div>

          <div class="btn-row">
            <a class="btn btn-primary" href="Prathamesh_Resume.pdf" download>↓ Download Resume</a>
            <a class="btn btn-ghost" href="#projects">View Projects</a>
            <a class="btn btn-ghost" href="#contact">Get in Touch</a>
          </div>
        </div>

        <div class="hero-photo-wrap">
          <img src="data:image/jpeg;base64,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BBrAAAAAAAAAAARzurXZX/DYSnN6NchXfPy3EakSyqcCU0pBFCAAAAAAAAAAAAmDLBGDfXHtoCP2WdaUP4k9NxyyEaKUAw80gAAAAAAAAAAAAAAmzT8p3DqFpYzgekULe85X494EwAygAwASAAAAAAAAAAAAAAAAACJh5nIDRoVi3YQ3mtVbRWQ0YMghFw5AAAAAAAAAAAAAAAAAAARPQkqGBxoYDb5qD9nggw7Uc6gBKyAAAAAAAAAAAAAAAAAAAAACEue/2Rc1Q7YQdlfPRciA9/X7gAAAAAAAAAAAAAAAAAAAAAAAAQWoeuCW9pDwRTXdfmag/DgAAAAAAAAAAAAAAAAAAAAAAAAAAAAyzgFd7Y0MJMlpB9ERgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAwgxShIee4TiAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA/8QAAv/aAAwDAQACAAMAAAAQ999999999999999999999999999999999999999999999999999999999999999956w9vssccsu/5+99999999999999999999999999999999yd/wDPPPPPPPPPPPPLP9tffffffffffffffffffffffffffen3PPPPPPPPPPPPPPPPPPH8vffffffffffffffffffffffeZfPPPPPPPPPPPPPPPPPPPPPPH+vfffffffffffffffffffanPPPPPPPPPPPNMsvPPPPPPPPPPPNdfffffffffffffffffbnPPPPPPPOOMQ9U5Cpm/tPPPPPPPPPK/fffffffffffffffYfPPPPPPPLbRYt7czzBu+38dPPPPPPPPG/fffffffffffffZPPPPPPPPPN4jfFRYd8p0DOSL9PPPPPPPPG/fffffffffffcvPPPPPPPMhGZ90zi4Lj7ndICq0NPPPPPPPPL9fffffffffevPPPPPPPONapnPppTaLltUOikqzJvPPPPPPPPNffffffffff8Azzzzzzzz0aE5kd+E9etmX2c1uHKzrzzzzzzzzzb3333333TzzzzzzzzyFpOf/wBBBRBPdXrqEnNZc+888888888799999958888888888uxQlv3IU7UOQ0Hoqx22b68888888888e99999t8888888888pyIicI8WGex5VMs0mZ4Ti8888888888619999e88888888888VKDLjBtN1vDDCyklkYBk888888888882999q888888888888nMaC7GtZoaIB28PVulV+88888888888/8AffTfPPPPPPPPPPPLKIoXQ1+GdSyKKx2eU7/PPPPPPPPPPPPPfeXPPPPPPPPPPPPPL23r5PuHmtGvL6rUoAfPPPPPPPPPPPPPvevPPPPPPPPPPPPPPzqsPVlR1O5rA77O8+/PPPPPPPPPPPPHfavPPPPPPPPPPPPPPUE+3XpGSb74VT3pvqfPPPPPPPPPPPPP/cfPPPPPPPPPPPPPL9+PoNutmQKyGkwdiZ/PPPPPPPPPPPPLvdfPPPPPPPPPPPPPPME2NhES7UISaKHMr3/PPPPPPPPPPPPKPVfPPPPPPPPPPPPPPOg5cyuccDsllvLunfPPPPPPPPPPPPPKPV/PPPPPPPPPPPPPPPTAaofn24oJZNGKofPPPPPPPPPPPPPKPffPPPPPPPPPPPPPPPD9PqhE3CoVqcm+fPPPPPPPPPPPPPPKPUfPPPPPPPPPPPPPPPPDJaxq1Jo9YMJH/PPPPPPPPPPPPPPPPaPPPPPPPPPPPPPPPPPPxxpg4lVrv19nPPPPPPPPPPPPPPPP/avPPPPPPPPPPPPPPPPPDZVYs36K4wqPPPPPPPPPPPPPPPPP/efPPPPPPPPPPPPPPPPPN5d8ExmCqKhPPPPPPPPPPPPPPPPFPfd/PPPPPPPPPPPPPPPLFLZCzqAvoaoW/PPPPPPPPPPPPPPHvfXfPPPPPPPPPPPPPPIiouaDAvM3IFKZ2vPPPPPPPPPPPPOnffbvPPPPPPPPPPPPPKQEvAnslvVCqGszHh/dPPPPPPPPPPOffffX/PPPPPPPPPN6MZ9WqAaN/rg9wa0Cr5x4NNvPPPPPPOFvfffWvPPPPPPPN0oh4mMXHkXt5ZpNUHGj6ZhjCd0sf/PPPO/fffffV/PPPt7BaCcfBisyrW+ebIWQC0ej4NtM2tGmjtcdPHvfffffetM3cqBuiLEf50Ev4le08WZkSqtM1bZ/i4+ku4RUWvfffffffTKhvnXVk6zGNbk2uA41xxEbJC98WL0l7wVR015QH/ffffffffbKJtZryUW62SAMWHh97d2GIkvekJWQ17Xvg881/ffffffffffripw94AQkzIPdiRaklyqWIJ34Eg6wJyRowxzffffffffffffWgvqZAwqz9ftM4mAyJlIVX99BmyUDoAiopvffffffffffffffSLf/ADU7mztHY2DwIbhxjQiV/FH862L61Qf3333333333333333/AKVhVPKBFgfnjp+cfb+3I51hkiojHZ+999999999999999999tc/Yk8G9NczAIUqJBk+C/6NhXYDBs999999999999999999999Ohqcd43s/Tv0PLZAYM1ro1ggGd999999999999999999999999s3m++wBVYI3ZnYdFHfKNk/99999999999999999999999999998ZBXEk+RRFvaxXySPd999999999999999999999999999999999fMdgb1Eumsu9999999999999999999999999999999999999999999999999999999999999999999/8QALxEAAgIBAwMDBAIBBQEBAAAAAAECEQMQITEEEjAgQEETIjJhBVFxFCMzUGBCcv/aAAgBAgEBPwD/AMDaO47i36rZbO4tf9DZ3F+e2WveWX7SxP3LfuExP2rdF+WivKn7NvxN0dwmKxUWW9a8afsW/Cxz2LbZFeixSEyytvInXnb8U2URRVDfooURLSKsarxp15W/Cz4GrEhD0WtiaFoh7jj40/G34kNMelemnfoW5ej8ifib8V7DY9LJToeVLkWaIpoT1sQyIpDEPxJ+BvzNmSaRLI2OxNin+xZmLKxZRTTExC9D8SfskPVmV3MWlDRuJkZIjMhK1ohpVoh+NP1S8id6vgm/9x+jnSvkshIxSE7IorWXC8a9T8i4a1lwyf5v0oZQiDaMU0xMvbV8LyLj0PjyokqYib+1sUW3Yon03R9OQ00XTLsimyGJsWEWJIiQlq/IvRLzSEZPwYkktzuSI5X/AESnJolI3bIoiKTR9V0fWZCYufZvzNaZeDJP4Rjx3uzHGCRPtfDM1JGMXJCiPbe41AnCLN4sxu602rzLjR+e63I505UZ3wSVs7mkd8v7HPbknciMajom4imfUf8AZHLQ5KRhbMkqgYcjk2n5o6Pjzz/F/wCDG/vX+TPyhxGmUUKmVURIcdNxEUYzL+B0/wCb8y50l56JQcM9fHcZRbjGyTvgioxQ8qFIUkyap2RkJoizHyZv+NmGFW/MudJe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" alt="Portrait of Prathamesh Pakhale">
        </div>
      </div>
    </div>
  </header>

  <svg class="waveform" viewBox="0 0 920 28" preserveAspectRatio="none" aria-hidden="true">
    <polyline points="0,20 40,20 40,8 120,8 120,20 220,20 220,8 260,8 260,20 380,20 380,8 480,8 480,20 620,20 620,8 680,8 680,20 800,20 800,8 880,8 880,20 920,20"
      fill="none" stroke="#E8A33D" stroke-width="1.5" opacity="0.55"/>
  </svg>

  <section id="about" data-ln="72
73
74
75
76
77
78
79">
    <div class="wrap">
      <p class="kicker">about</p>
      <h2>Why verification</h2>
      <div class="about-body">
        <p>I started with Digital Electronics and Verilog, and building a 4-bit CPU from scratch is what pulled me toward the verification side of the flow — the idea that a design is only as good as your ability to prove it's correct. That's what led me to specialize in VLSI Design Verification: SystemVerilog, UVM methodology, and the timing discipline that connects a good testbench to silicon that actually works.</p>
        <p>I'm currently a final-year student at Government College of Engineering, Kolhapur, treating this as a structured, self-directed second curriculum alongside coursework — with the goal of an off-campus DV role in Pune or Bengaluru.</p>
      </div>
    </div>
  </section>

  <section id="skills" data-ln="80
81
82
83
84
85
86
87
88
89
90
91
92
93
94">
    <div class="wrap">
      <p class="kicker">skills</p>
      <h2>Technical Skills</h2>

      <div class="skill-group">
        <div class="skill-group-label">core</div>
        <div class="pills">
          <span class="pill">Digital Electronics &amp; Circuit Analysis</span>
          <span class="pill">Digital Logic Design</span>
          <span class="pill">Verilog HDL &amp; RTL Design</span>
          <span class="pill">HDL Simulation &amp; Testbench Writing</span>
          <span class="pill">Xilinx Vivado</span>
        </div>
      </div>

      <div class="skill-group">
        <div class="skill-group-label">systemverilog</div>
        <div class="pills">
          <span class="pill">OOP, Randomization &amp; Constraints</span>
          <span class="pill">Functional Coverage &amp; SVA</span>
        </div>
      </div>

      <div class="skill-group">
        <div class="skill-group-label">currently advancing</div>
        <div class="pills">
          <span class="pill advancing">Static Timing Analysis (STA)</span>
          <span class="pill advancing">Computer Architecture &amp; ISA Design</span>
          <span class="pill advancing">UVM</span>
          <span class="pill advancing">Linux / Shell Scripting</span>
          <span class="pill advancing">TCL Scripting</span>
        </div>
      </div>
    </div>
  </section>

  <section id="projects" data-ln="95
96
97
98
99
100
101
102
103
104
105
106
107
108
109
110
111
112">
    <div class="wrap">
      <p class="kicker">projects</p>
      <h2>Projects</h2>

      <div class="project-card">
        <div class="project-head">
          <span class="project-title">32-Bit Pipelined RISC Processor <span class="ext">.sv</span></span>
          <span class="wip-chip">IN PROGRESS</span>
        </div>
        <p class="project-desc">Building a pipelined RISC core end to end — RTL in SystemVerilog, a full UVM verification environment, timing closure with OpenSTA, and TCL-driven regression. The applied project behind the STA and computer-architecture study track.</p>
        <div class="tag-row">
          <span class="tag">SystemVerilog</span><span class="tag">UVM</span><span class="tag">OpenSTA</span><span class="tag">TCL</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-head">
          <span class="project-title">4-Bit CPU Design <span class="ext">.v</span></span>
        </div>
        <p class="project-desc">Designed and simulated a complete 4-bit CPU architecture — ALU, instruction decoder, register file, and program counter — integrated through a CPU top module and verified with custom-written testbenches.</p>
        <div class="tag-row">
          <span class="tag">Verilog HDL</span><span class="tag">Xilinx Vivado</span><span class="tag">Testbench</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-head">
          <span class="project-title">Smart Safety Helmet for Industrial Workers</span>
        </div>
        <p class="project-desc">A helmet embedded with motion, gas, and temperature sensors that detects hazardous conditions and alerts workers in real time, aimed at reducing industrial accidents.</p>
        <div class="tag-row">
          <span class="tag">Embedded Systems</span><span class="tag">Sensors</span><span class="tag">Safety</span>
        </div>
      </div>
    </div>
  </section>

  <section id="education" data-ln="113
114
115
116
117
118
119
120
121
122">
    <div class="wrap">
      <p class="kicker">education</p>
      <h2>Education &amp; Certifications</h2>

      <div class="edu-row">
        <div>
          <div class="edu-degree">B.Tech — Electronics &amp; Telecommunication Engineering</div>
          <div class="edu-school">Government College of Engineering, Kolhapur <span class="edu-meta">| CGPA 7.20</span></div>
        </div>
        <div class="edu-year">2023 – 2027</div>
      </div>
      <div class="edu-row">
        <div>
          <div class="edu-degree">12th Science (PCM)</div>
          <div class="edu-school">Westfield Junior College, Karad <span class="edu-meta">| 71.67%</span></div>
        </div>
        <div class="edu-year">2023</div>
      </div>
      <div class="edu-row">
        <div>
          <div class="edu-degree">10th SSC</div>
          <div class="edu-school">Mahatma Gandhi Vidyalay, Umbraj <span class="edu-meta">| 91.00%</span></div>
        </div>
        <div class="edu-year">2021</div>
      </div>

      <div style="margin-top:24px;" class="cert-line"><strong>Udemy</strong> — System Design Using Verilog</div>
    </div>
  </section>

  <section id="contact" data-ln="123
124
125
126
127
128">
    <div class="wrap">
      <p class="kicker">contact</p>
      <h2>Get in Touch</h2>

      <div class="contact-terminal">
        <div class="line"><span class="prompt">$</span> mail --to <a href="mailto:prathameshpakhle2764@gmail.com">prathameshpakhle2764@gmail.com</a></div>
        <div class="line"><span class="prompt">$</span> call <a href="tel:+917249872764">+91 72498 72764</a></div>
        <div class="line"><span class="prompt">$</span> open <a href="https://linkedin.com/in/prathamesh-pakhale" target="_blank" rel="noopener">linkedin.com/in/prathamesh-pakhale</a></div>
        <div class="line"><span class="prompt">$</span> open <a href="https://github.com/prathameshpakhle2764-ai" target="_blank" rel="noopener">github.com/prathameshpakhle2764-ai</a></div>
      </div>
    </div>
  </section>

  <footer>
    <div class="wrap footer-note">// built by Prathamesh Pakhale — last synced 2026</div>
  </footer>

<script>
  const tabs = document.querySelectorAll('.tab');
  const sections = document.querySelectorAll('section[id]');
  const setActive = (id) => {
    tabs.forEach(t => t.classList.toggle('active', t.getAttribute('href') === '#' + id));
  };
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) setActive(entry.target.id);
    });
  }, { rootMargin: '-45% 0px -50% 0px', threshold: 0 });
  sections.forEach(s => observer.observe(s));
</script>
</body>
</html>
