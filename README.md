<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Brain &amp; Mind Academy • DHANANJAYA - Functions: The Domain and Range</title>

  <!-- MathJax v3 Configuration & Loader -->
  <script>
    window.MathJax = {
      tex: {
        inlineMath: [['\\(', '\\)']],
        displayMath: [['\\[', '\\]']],
        processEscapes: true
      },
      svg: { fontCache: 'global' }
    };
  </script>
  <script type="text/javascript" id="MathJax-script" async
    src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>

  <style>
    :root {
      --navy-dark: #0c4a6e;
      --brand-blue: #0284c7;
      --accent-cyan: #0ea5e9;
      --bg-tint: #f0f9ff;
      --card-surf: #ffffff;
      --border-accent: #7dd3fc;
      --border-soft: #bae6fd;
      --green-ok: #059669;
      --green-surf: #d1fae5;
      --red-fail: #dc2626;
      --red-surf: #fee2e2;
      --brand-gold: #f59e0b;
      --gold-dark: #d97706;
      --gold-surf: #fef3c7;
      --text-main: #0f172a;
      --text-muted: #475569;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    }

    body {
      background-color: var(--bg-tint);
      color: var(--text-main);
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    header {
      background: var(--navy-dark);
      color: #fff;
      padding: 12px 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 4px 12px rgba(12, 74, 110, 0.15);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .brand-wrap {
      display: flex;
      align-items: center;
      gap: 14px;
    }

    .logo-badge {
      width: 46px;
      height: 46px;
      background: #ffffff;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }

    .brand-title h1 {
      font-size: 1.15rem;
      font-weight: 700;
      letter-spacing: 0.5px;
    }

    .brand-title p {
      font-size: 0.78rem;
      color: var(--accent-cyan);
      font-weight: 500;
    }

    .header-controls {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .chip {
      background: rgba(255, 255, 255, 0.15);
      border: 1px solid var(--border-accent);
      padding: 6px 14px;
      border-radius: 20px;
      font-size: 0.88rem;
      color: #ffffff;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .chip strong {
      color: #ffffff;
      font-weight: 800;
      letter-spacing: 0.3px;
    }

    .btn-icon {
      background: transparent;
      border: 1px solid var(--border-accent);
      color: #fff;
      border-radius: 50%;
      width: 36px;
      height: 36px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1rem;
    }

    nav {
      background: #ffffff;
      border-bottom: 1px solid var(--border-soft);
      display: flex;
      justify-content: center;
      gap: 8px;
      padding: 8px 16px;
    }

    nav button {
      background: none;
      border: none;
      outline: none;
      padding: 10px 20px;
      font-size: 0.95rem;
      font-weight: 600;
      color: var(--text-muted);
      cursor: pointer;
      border-radius: 8px;
      transition: all 0.2s;
    }

    nav button.active {
      background: var(--bg-tint);
      color: var(--brand-blue);
      border-bottom: 3px solid var(--brand-blue);
    }

    main {
      flex: 1;
      padding: 24px;
      max-width: 1400px;
      margin: 0 auto;
      width: 100%;
    }

    .view {
      display: none;
    }

    .view.active {
      display: block;
    }

    #loginGateView {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(12, 74, 110, 0.9);
      backdrop-filter: blur(6px);
      z-index: 1000;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .login-box {
      background: #fff;
      padding: 36px;
      border-radius: 16px;
      width: 100%;
      max-width: 440px;
      text-align: center;
      box-shadow: 0 14px 35px rgba(0,0,0,0.3);
    }

    .login-box h2 {
      font-size: 1.45rem;
      color: var(--navy-dark);
      margin-bottom: 6px;
    }

    .login-box p {
      font-size: 0.88rem;
      color: var(--text-muted);
      margin-bottom: 24px;
    }

    .login-box input {
      width: 100%;
      padding: 12px 16px;
      border: 1px solid var(--border-soft);
      border-radius: 8px;
      font-size: 1rem;
      margin-bottom: 16px;
      outline: none;
    }

    .btn-primary {
      background: var(--brand-blue);
      color: #fff;
      border: none;
      padding: 12px 24px;
      font-size: 1rem;
      font-weight: 600;
      border-radius: 8px;
      cursor: pointer;
      width: 100%;
      transition: background 0.2s;
    }

    .btn-primary:hover {
      background: var(--navy-dark);
    }

    .theory-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 24px;
      margin-bottom: 24px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.02);
    }

    .theory-card h3 {
      color: var(--navy-dark);
      margin-bottom: 14px;
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 1.25rem;
    }

    .theory-intro-text {
      color: var(--text-main);
      line-height: 1.65;
      margin-bottom: 18px;
      font-size: 0.95rem;
    }

    .compendium-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 20px;
      margin: 16px 0;
    }

    .comp-card {
      background: #ffffff;
      border: 1px solid var(--border-soft);
      border-radius: 10px;
      padding: 18px;
      display: flex;
      flex-direction: column;
      box-shadow: 0 2px 6px rgba(12, 74, 110, 0.04);
    }

    .comp-card h4 {
      color: var(--navy-dark);
      border-bottom: 2px solid var(--border-soft);
      padding-bottom: 8px;
      margin-bottom: 12px;
      font-size: 1.05rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .recap-body {
      font-size: 0.92rem;
      line-height: 1.65;
      color: var(--text-main);
    }

    .formula-box {
      background: #f8fafc;
      border-left: 4px solid var(--brand-blue);
      border-radius: 0 6px 6px 0;
      padding: 10px 14px;
      margin-top: 10px;
    }

    .sheet-grid {
      display: grid;
      grid-template-columns: 1fr 360px;
      gap: 24px;
    }

    @media (max-width: 990px) {
      .sheet-grid {
        grid-template-columns: 1fr;
      }
    }

    .question-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 26px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.03);
    }

    .concept-tag {
      display: inline-block;
      padding: 4px 10px;
      border-radius: 14px;
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.4px;
      text-transform: uppercase;
      margin-bottom: 8px;
    }

    .concept-tag.def {
      background: #e0f2fe;
      color: #0369a1;
      border: 1px solid #7dd3fc;
    }

    .concept-tag.ex {
      background: #fef3c7;
      color: #b45309;
      border: 1px solid #fde68a;
    }

    .concept-tag.exc {
      background: #d1fae5;
      color: #059669;
      border: 1px solid #a7f3d0;
    }

    .step-box {
      margin-top: 16px;
      padding: 18px;
      border: 1px solid var(--border-soft);
      border-radius: 8px;
      background: #fff;
      display: none;
    }

    .step-box.unlocked {
      display: block;
      animation: fadeIn 0.3s ease-in;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(6px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .step-box.success {
      border-color: var(--green-ok);
      background: var(--green-surf);
    }

    .step-text-wrap {
      font-size: 1rem;
      line-height: 1.8;
      display: flex;
      align-items: center;
      flex-wrap: wrap;
      gap: 8px;
    }

    .inline-blank {
      width: 170px;
      padding: 6px 10px;
      font-size: 0.95rem;
      border: 2px dashed var(--brand-blue);
      border-radius: 6px;
      outline: none;
      background: #fff;
      color: var(--navy-dark);
      font-weight: 600;
      text-align: center;
    }

    .inline-blank:focus {
      border-style: solid;
      border-color: var(--accent-cyan);
      box-shadow: 0 0 0 3px rgba(14,165,233,0.2);
    }

    .inline-blank:disabled {
      border: 1px solid var(--green-ok);
      background: #fff;
      color: var(--green-ok);
      cursor: not-allowed;
    }

    .btn-verify {
      background: var(--accent-cyan);
      color: #fff;
      border: none;
      padding: 7px 16px;
      border-radius: 6px;
      font-weight: 600;
      cursor: pointer;
    }

    .btn-verify:hover {
      background: var(--brand-blue);
    }

    .btn-reveal {
      background: var(--brand-gold);
      color: #fff;
      border: none;
      padding: 6px 12px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.85rem;
      cursor: pointer;
      margin-left: 6px;
    }

    .btn-reveal:hover {
      background: var(--gold-dark);
    }

    .attempts-badge {
      font-size: 0.8rem;
      font-weight: 700;
      padding: 3px 8px;
      border-radius: 12px;
      background: #f1f5f9;
      color: #64748b;
      margin-left: 6px;
    }

    .svg-container {
      display: flex;
      justify-content: center;
      margin: 16px 0;
      padding: 16px;
      background: var(--bg-tint);
      border-radius: 8px;
      border: 1px solid var(--border-soft);
      overflow-x: auto;
    }

    .nav-toolbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 26px;
      padding-top: 18px;
      border-top: 1px solid var(--border-soft);
    }

    .nav-btn-group {
      display: flex;
      gap: 10px;
    }

    .btn-nav-action {
      background: #f8fafc;
      border: 1px solid var(--border-accent);
      color: var(--navy-dark);
      padding: 8px 18px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.9rem;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: all 0.15s;
    }

    .btn-nav-action:hover:not(:disabled) {
      background: var(--bg-tint);
      border-color: var(--brand-blue);
    }

    .btn-nav-action:disabled {
      opacity: 0.45;
      cursor: not-allowed;
    }

    .btn-skip {
      border-color: var(--brand-gold);
      color: var(--gold-dark);
      background: var(--gold-surf);
    }

    .btn-skip:hover {
      background: #fde68a;
    }

    .palette-box {
      background: #fff;
      border: 1px solid var(--border-soft);
      border-radius: 12px;
      padding: 16px;
      margin-bottom: 20px;
    }

    .palette-legend {
      display: flex;
      justify-content: space-between;
      font-size: 0.75rem;
      margin: 8px 0 12px 0;
      padding: 6px 8px;
      background: var(--bg-tint);
      border-radius: 6px;
    }

    .legend-item {
      display: flex;
      align-items: center;
      gap: 4px;
      font-weight: 600;
    }

    .legend-dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
    }

    .palette-section-title {
      font-size: 0.8rem;
      font-weight: 700;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin: 12px 0 6px 0;
    }

    .palette-grid {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 6px;
      margin-bottom: 12px;
    }

    .palette-btn {
      aspect-ratio: 1;
      border: 1px solid var(--border-soft);
      background: var(--bg-tint);
      border-radius: 6px;
      font-weight: 600;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all 0.15s;
      font-size: 0.82rem;
      color: var(--navy-dark);
    }

    .palette-btn.active {
      border: 2px solid var(--navy-dark) !important;
      background: var(--border-accent);
      color: #fff;
      font-weight: 800;
    }

    .palette-btn.completed {
      background: var(--green-ok) !important;
      color: #fff !important;
      border-color: var(--green-ok) !important;
    }

    .palette-btn.skipped {
      background: var(--brand-gold) !important;
      color: #fff !important;
      border-color: var(--gold-dark) !important;
    }

    .tool-tabs {
      display: flex;
      border-bottom: 1px solid var(--border-soft);
      margin-bottom: 12px;
    }

    .tool-tabs button {
      flex: 1;
      border: none;
      background: none;
      padding: 8px;
      font-weight: 600;
      font-size: 0.85rem;
      cursor: pointer;
      color: var(--text-muted);
    }

    .tool-tabs button.active {
      color: var(--brand-blue);
      border-bottom: 2px solid var(--brand-blue);
    }

    .keypad-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 6px;
    }

    .keypad-btn {
      padding: 8px 4px;
      border: 1px solid var(--border-soft);
      background: #fff;
      border-radius: 4px;
      font-weight: 600;
      font-size: 0.85rem;
      cursor: pointer;
      text-align: center;
    }

    .keypad-btn:hover {
      background: var(--bg-tint);
    }

    #calcDisplay {
      width: 100%;
      padding: 8px;
      border: 1px solid var(--border-soft);
      border-radius: 4px;
      font-size: 1rem;
      text-align: right;
      margin-bottom: 8px;
      background: #f8fafc;
    }

    .hero-score-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 28px;
      text-align: center;
      margin-bottom: 24px;
      box-shadow: 0 4px 14px rgba(0,0,0,0.03);
    }

    .student-badge {
      display: inline-block;
      background: var(--bg-tint);
      border: 1px solid var(--border-accent);
      padding: 6px 18px;
      border-radius: 20px;
      font-size: 1rem;
      margin-bottom: 14px;
      color: var(--navy-dark);
    }

    .student-badge strong {
      color: var(--brand-blue);
    }

    .score-badge {
      font-size: 2.8rem;
      font-weight: 800;
      color: var(--brand-blue);
      margin: 8px 0;
    }

    .toast {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: var(--navy-dark);
      color: #fff;
      padding: 12px 20px;
      border-radius: 8px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.2);
      display: none;
      z-index: 1000;
    }

    @media print {
      header, nav, .palette-box, #toolsPanel, .btn-primary, .btn-verify, #loginGateView, .nav-toolbar {
        display: none !important;
      }
      body { background: #fff; }
      main { width: 100%; max-width: 100%; padding: 0; }
      .sheet-grid { display: block; }
      .view { display: block !important; }
    }
  </style>
</head>
<body>

  <!-- Brand Header -->
  <header>
    <div class="brand-wrap">
      <div class="logo-badge">
        <svg width="34" height="34" viewBox="0 0 100 100" fill="none">
          <path d="M 20 30 Q 50 10 80 30" stroke="#f59e0b" stroke-width="8" stroke-linecap="round"/>
          <path d="M 26 40 Q 50 22 74 40" stroke="#f59e0b" stroke-width="8" stroke-linecap="round"/>
          <path d="M 32 50 Q 50 36 68 50" stroke="#f59e0b" stroke-width="7" stroke-linecap="round"/>
          <path d="M 18 80 Q 50 68 50 82 Q 50 68 82 80 L 82 52 Q 50 42 50 56 Q 50 42 18 52 Z" fill="#ffffff" stroke="#334155" stroke-width="7" stroke-linejoin="round"/>
        </svg>
      </div>
      <div class="brand-title">
        <h1>Brain &amp; Mind Academy</h1>
        <p>B&amp;M – The Experts • DHANANJAYA (Functions: The Domain and Range)</p>
      </div>
    </div>
    <div class="header-controls">
      <div class="chip" id="timerChip">⏱️ 00:00</div>
      <div class="chip" id="userPill"><strong>Student: Guest</strong></div>
      <button class="btn-icon" id="audioToggleBtn" title="Toggle Audio">🔊</button>
    </div>
  </header>

  <!-- Navigation Bar -->
  <nav>
    <button class="tab-btn active" onclick="switchView('theoryView')">📖 Concept &amp; Graphical Guide</button>
    <button class="tab-btn" onclick="switchView('sheetView')">✍️ Interactive Practice Sheet</button>
    <button class="tab-btn" onclick="switchView('solutionsView')">📋 Test Results &amp; Complete Solutions</button>
  </nav>

  <!-- Student Authentication Modal -->
  <div id="loginGateView">
    <div class="login-box">
      <h2>DHANANJAYA Portal</h2>
      <p>Mathematics Learning Centre • Functions: The Domain and Range</p>
      <input type="text" id="studentNameInput" placeholder="Enter Student Name" />
      <input type="password" id="passInput" placeholder="Passcode (Optional)" />
      <button class="btn-primary" onclick="initDirectLogin()">Start Practice Session</button>
    </div>
  </div>

  <main>
    <!-- View 1: Concept & Graphical Guide -->
    <div id="theoryView" class="view active">
      <div class="theory-card">
        <h3>📐 Theory Compendium: Definition, Domain, Range &amp; Vertical Line Test</h3>
        <p class="theory-intro-text">
          A function \(f\) from a set of elements \(X\) to a set of elements \(Y\) is a rule that assigns to each element \(x\) in \(X\) exactly one element \(y\) in \(Y\).
        </p>

        <div class="compendium-grid">
          <!-- Card 1 -->
          <div class="comp-card">
            <h4>1. Arrow Mappings &amp; Ordered Pairs</h4>
            <div class="recap-body">
              <p>• A relation cannot have repeated \(x\)-values paired with distinct \(y\)-values.</p>
              <p>• \(F = \{(1,5), (3,3), (2,3), (4,2)\}\) is a function because every \(x\) is mapped uniquely.</p>
              <p>• \(G = \{(1,5), (4,2), (2,3), (3,3), (1,6)\}\) is <strong>not</strong> a function because \(x = 1\) is assigned both 5 and 6.</p>
            </div>
          </div>

          <!-- Card 2 -->
          <div class="comp-card">
            <h4>2. The Vertical Line Test</h4>
            <div class="recap-body">
              <p>If it is not possible to draw a vertical line through a graph so that it cuts the graph in more than one point, then the graph represents a function.</p>
              <div class="formula-box">
                <p>• \(y = x^2\) passes the vertical line test (Function).</p>
                <p>• \(x = y^2\) or \(y^2 = x^3\) intersects vertical lines twice (Not a function).</p>
              </div>
            </div>
          </div>

          <!-- Card 3 -->
          <div class="comp-card">
            <h4>3. Natural vs. Specified Domain</h4>
            <div class="recap-body">
              <p>• <strong>Natural Domain:</strong> Largest set of real numbers \(x\) for which the algebraic rule is defined.</p>
              <div class="formula-box">
                <p>• Even radicals: \(\sqrt{A} \implies A \ge 0\).</p>
                <p>• Denominators: \(\frac{1}{B} \implies B \ne 0\).</p>
                <p>• <strong>Specified Domain:</strong> A restricted subset, such as \(y = x^2\) for \(0 \le x \le 2\), giving range \(0 \le y \le 4\).</p>
              </div>
            </div>
          </div>

          <!-- Card 4 -->
          <div class="comp-card">
            <h4>4. Range of a Function</h4>
            <div class="recap-body">
              <p>The range is the complete set of resulting \(y\)-values produced by evaluating the function across its domain:</p>
              <div class="formula-box">
                \[\text{Range} = \{y \in Y \mid y = f(x) \text{ for some } x \in X\}\]
                <p style="font-size:0.86rem; margin-top:4px;">Always determined by algebraic boundaries, vertex heights, or horizontal asymptotes.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- View 2: Interactive Practice Workstation -->
    <div id="sheetView" class="view">
      <div class="sheet-grid">
        <div class="question-card" id="activeQuestionCard"></div>

        <aside>
          <div class="palette-box">
            <div style="display: flex; justify-content: space-between; align-items: center;">
              <h4>Question Palette</h4>
              <span style="font-size:0.8rem; color:var(--text-muted);" id="paletteCount">0 / 22</span>
            </div>

            <div class="palette-legend">
              <div class="legend-item"><span class="legend-dot" style="background:#059669;"></span> Done</div>
              <div class="legend-item"><span class="legend-dot" style="background:#f59e0b;"></span> Skipped</div>
              <div class="legend-item"><span class="legend-dot" style="background:#7dd3fc;"></span> Active</div>
              <div class="legend-item"><span class="legend-dot" style="background:#f0f9ff; border:1px solid #bae6fd;"></span> Unseen</div>
            </div>
            
            <div class="palette-section-title">Core Definitions &amp; Examples (Q1 – Q9)</div>
            <div class="palette-grid" id="paletteSec1Grid"></div>

            <div class="palette-section-title">Exercises 1.3: Part 1 (Q10 – Q15)</div>
            <div class="palette-grid" id="paletteSec2Grid"></div>

            <div class="palette-section-title">Exercises 1.3: Part 2 (Q16 – Q22)</div>
            <div class="palette-grid" id="paletteSec3Grid"></div>
          </div>

          <div class="palette-box" id="toolsPanel">
            <div class="tool-tabs">
              <button id="tabKeypadBtn" class="active" onclick="toggleTool('keypad')">Math Keypad</button>
              <button id="tabCalcBtn" onclick="toggleTool('calc')">Calculator</button>
            </div>

            <div id="toolKeypad">
              <div class="keypad-grid">
                <button class="keypad-btn" onclick="insertSymbol('≥')">≥</button>
                <button class="keypad-btn" onclick="insertSymbol('≤')">≤</button>
                <button class="keypad-btn" onclick="insertSymbol('≠')">≠</button>
                <button class="keypad-btn" onclick="insertSymbol('√')">√</button>
                <button class="keypad-btn" onclick="insertSymbol('^2')">\(^2\)</button>
                <button class="keypad-btn" onclick="insertSymbol('/')">/</button>
                <button class="keypad-btn" onclick="insertSymbol('-')">-</button>
                <button class="keypad-btn" onclick="insertSymbol('x')">x</button>
                <button class="keypad-btn" onclick="insertSymbol('y')">y</button>
                <button class="keypad-btn" onclick="insertSymbol('all real x')">all real x</button>
                <button class="keypad-btn" onclick="insertSymbol('Yes')">Yes</button>
                <button class="keypad-btn" onclick="insertSymbol('No')">No</button>
              </div>
            </div>

            <div id="toolCalc" style="display: none;">
              <input type="text" id="calcDisplay" readonly value="" />
              <div class="keypad-grid">
                <button class="keypad-btn" onclick="pressCalc('7')">7</button>
                <button class="keypad-btn" onclick="pressCalc('8')">8</button>
                <button class="keypad-btn" onclick="pressCalc('9')">9</button>
                <button class="keypad-btn" onclick="pressCalc('/')">/</button>
                <button class="keypad-btn" onclick="pressCalc('4')">4</button>
                <button class="keypad-btn" onclick="pressCalc('5')">5</button>
                <button class="keypad-btn" onclick="pressCalc('6')">6</button>
                <button class="keypad-btn" onclick="pressCalc('*')">*</button>
                <button class="keypad-btn" onclick="pressCalc('1')">1</button>
                <button class="keypad-btn" onclick="pressCalc('2')">2</button>
                <button class="keypad-btn" onclick="pressCalc('3')">3</button>
                <button class="keypad-btn" onclick="pressCalc('-')">-</button>
                <button class="keypad-btn" onclick="pressCalc('0')">0</button>
                <button class="keypad-btn" onclick="pressCalc('.')">.</button>
                <button class="keypad-btn" onclick="calcEval()">=</button>
                <button class="keypad-btn" onclick="pressCalc('+')">+</button>
                <button class="keypad-btn" style="grid-column: span 2;" onclick="calcClear()">C</button>
                <button class="keypad-btn" style="grid-column: span 2;" onclick="calcSqrt()">√</button>
              </div>
            </div>
          </div>
        </aside>
      </div>
    </div>

    <!-- View 3: Complete Solutions & Final Results -->
    <div id="solutionsView" class="view">
      <div class="hero-score-card">
        <h2>Functions Diagnostic Assessment Report</h2>
        <div class="student-badge" id="reportStudentBadge"><strong>Student: Guest</strong></div>
        <div class="score-badge" id="scoreValue">0 / 22</div>
        <p id="scoreSubtitle">Complete all problems in the workstation to view your performance metrics.</p>
        <button class="btn-primary" style="margin-top: 14px; max-width: 220px;" onclick="window.print()">🖨️ Print Report &amp; Solutions</button>
      </div>
      <div id="completeSolutionsContainer"></div>
    </div>
  </main>

  <div class="toast" id="toastMessage"></div>

  <script>
    /* ==========================================================================
       COMPLETE 22-QUESTION DATASET (SEQUENTIALLY NUMBERED 1 TO 22)
       Source: Mathematics Learning Centre, University of Sydney
       ========================================================================== */
    const CHAPTER_QUESTIONS = [
      // ---------- SECTION 1: CORE DEFINITIONS & EXAMPLES (Q1 - Q9) ----------
      {
        id: 1,
        section: "Section 1.1: What is a Function?",
        source: "Mathematics Learning Centre: Section 1.1.1, Page 1",
        tag: "def",
        title: "Arrow Diagrams: Testing Mapping Rules",
        prompt: "Examine the arrow diagrams for mappings \\(f: X \\to Y\\) and \\(g: X \\to Y\\). Determine whether each mapping represents a valid function (Yes/No).",
        svg: `<svg width="100%" height="180" viewBox="0 0 460 170" style="max-width:440px;">
          <!-- Left Mapping: f -->
          <g transform="translate(10, 5)">
            <ellipse cx="50" cy="85" rx="35" ry="70" fill="#f0f9ff" stroke="#0c4a6e" stroke-width="1.5"/>
            <ellipse cx="160" cy="85" rx="35" ry="70" fill="#f0f9ff" stroke="#0c4a6e" stroke-width="1.5"/>
            <text x="45" y="45" font-size="12" font-weight="600">1</text>
            <text x="45" y="75" font-size="12" font-weight="600">2</text>
            <text x="45" y="105" font-size="12" font-weight="600">3</text>
            <text x="45" y="135" font-size="12" font-weight="600">4</text>
            <text x="155" y="55" font-size="12" font-weight="600">5</text>
            <text x="155" y="95" font-size="12" font-weight="600">3</text>
            <text x="155" y="130" font-size="12" font-weight="600">2</text>
            <!-- Arrows for f -->
            <line x1="60" y1="41" x2="148" y2="51" stroke="#0284c7" stroke-width="1.8"/>
            <polygon points="148,51 140,47 141,54" fill="#0284c7"/>
            <line x1="60" y1="71" x2="148" y2="92" stroke="#0284c7" stroke-width="1.8"/>
            <polygon points="148,92 140,88 141,95" fill="#0284c7"/>
            <line x1="60" y1="101" x2="148" y2="95" stroke="#0284c7" stroke-width="1.8"/>
            <polygon points="148,95 140,92 140,99" fill="#0284c7"/>
            <line x1="60" y1="131" x2="148" y2="128" stroke="#0284c7" stroke-width="1.8"/>
            <polygon points="148,128 140,124 140,131" fill="#0284c7"/>
            <text x="100" y="25" font-size="14" font-weight="bold" fill="#0c4a6e">f</text>
            <text x="45" y="10" font-size="12" fill="#64748b">X</text><text x="155" y="10" font-size="12" fill="#64748b">Y</text>
          </g>
          <!-- Right Mapping: g -->
          <g transform="translate(240, 5)">
            <ellipse cx="50" cy="85" rx="35" ry="70" fill="#f0f9ff" stroke="#0c4a6e" stroke-width="1.5"/>
            <ellipse cx="160" cy="85" rx="35" ry="70" fill="#f0f9ff" stroke="#0c4a6e" stroke-width="1.5"/>
            <text x="45" y="45" font-size="12" font-weight="600">1</text>
            <text x="45" y="75" font-size="12" font-weight="600">2</text>
            <text x="45" y="105" font-size="12" font-weight="600">3</text>
            <text x="45" y="135" font-size="12" font-weight="600">4</text>
            <text x="155" y="45" font-size="12" font-weight="600">5</text>
            <text x="155" y="75" font-size="12" font-weight="600">6</text>
            <text x="155" y="105" font-size="12" font-weight="600">3</text>
            <text x="155" y="135" font-size="12" font-weight="600">2</text>
            <!-- Arrows for g -->
            <line x1="60" y1="41" x2="148" y2="41" stroke="#dc2626" stroke-width="1.8"/>
            <polygon points="148,41 140,38 140,44" fill="#dc2626"/>
            <line x1="60" y1="41" x2="148" y2="71" stroke="#dc2626" stroke-width="1.8"/>
            <polygon points="148,71 140,66 141,73" fill="#dc2626"/>
            <line x1="60" y1="71" x2="148" y2="101" stroke="#dc2626" stroke-width="1.8"/>
            <polygon points="148,101 140,96 141,103" fill="#dc2626"/>
            <line x1="60" y1="101" x2="148" y2="103" stroke="#dc2626" stroke-width="1.8"/>
            <polygon points="148,103 140,100 140,106" fill="#dc2626"/>
            <line x1="60" y1="131" x2="148" y2="133" stroke="#dc2626" stroke-width="1.8"/>
            <polygon points="148,133 140,130 140,136" fill="#dc2626"/>
            <text x="100" y="25" font-size="14" font-weight="bold" fill="#0c4a6e">g</text>
            <text x="45" y="10" font-size="12" fill="#64748b">X</text><text x="155" y="10" font-size="12" fill="#64748b">Y</text>
          </g>
        </svg>`,
        steps: [
          { prefix: "Step 1: In mapping f, every element in X is assigned to exactly one element of Y. Is f a function? (Yes/No):", expected: "yes", suffix: ".", explanation: "Every element in X has associated with it exactly one element of Y." },
          { prefix: "Step 2: In mapping g, the element 1 in X is assigned two elements (5 and 6). Is g a function? (Yes/No):", expected: "no", suffix: ".", explanation: "The element 1 in set X is assigned two elements, 5 and 6 in set Y, which violates the definition of a function." }
        ]
      },
      {
        id: 2,
        section: "Section 1.1: Sets of Ordered Pairs",
        source: "Mathematics Learning Centre: Section 1.1.1, Page 1",
        tag: "def",
        title: "Functions as Sets of Ordered Pairs",
        prompt: "A function cannot have repeated x-values with different y-values. Consider: \\[F = \\{(1,5), (3,3), (2,3), (4,2)\\}\\] and \\[G = \\{(1,5), (4,2), (2,3), (3,3), (1,6)\\}\\]",
        steps: [
          { prefix: "Step 1: Is set F a function? (Yes/No):", expected: "yes", suffix: ".", explanation: "No two pairs share the same first coordinate with different second coordinates." },
          { prefix: "Step 2: Is set G a function? (Yes/No):", expected: "no", suffix: ".", explanation: "The pairs (1,5) and (1,6) have the same x-value mapped to different y-values." }
        ]
      },
      {
        id: 3,
        section: "Section 1.1: The Vertical Line Test",
        source: "Mathematics Learning Centre: Section 1.1.2, Page 2",
        tag: "def",
        title: "The Vertical Line Test on Curves",
        prompt: "The Vertical Line Test states that if it is not possible to draw a vertical line through a graph cutting it in more than one point, then the graph is a function. Evaluate the two graphs.",
        svg: `<svg width="100%" height="200" viewBox="0 0 460 190" style="max-width:440px;">
          <!-- Graph A: Parabola y = x^2 -->
          <g transform="translate(15, 10)">
            <rect width="200" height="165" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
            <line x1="15" y1="135" x2="185" y2="135" stroke="#64748b" stroke-width="1.5"/>
            <line x1="100" y1="15" x2="100" y2="150" stroke="#64748b" stroke-width="1.5"/>
            <text x="180" y="148" font-size="11" fill="#475569">x</text><text x="106" y="24" font-size="11" fill="#475569">y</text>
            <text x="90" y="148" font-size="11" fill="#64748b">0</text>
            <path d="M 30,25 Q 100,135 170,25" fill="none" stroke="#0284c7" stroke-width="2.2"/>
            <!-- Vertical line test -->
            <line x1="140" y1="15" x2="140" y2="150" stroke="#059669" stroke-width="1.5" stroke-dasharray="4"/>
            <circle cx="140" cy="65" r="3.5" fill="#059669"/>
            <text x="50" y="160" font-size="10" font-weight="600" fill="#0c4a6e">Graph A: y = x²</text>
          </g>
          <!-- Graph B: Sideways Parabola x = y^2 -->
          <g transform="translate(245, 10)">
            <rect width="200" height="165" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
            <line x1="15" y1="85" x2="185" y2="85" stroke="#64748b" stroke-width="1.5"/>
            <line x1="45" y1="15" x2="45" y2="150" stroke="#64748b" stroke-width="1.5"/>
            <text x="180" y="98" font-size="11" fill="#475569">x</text><text x="51" y="24" font-size="11" fill="#475569">y</text>
            <text x="35" y="98" font-size="11" fill="#64748b">0</text>
            <path d="M 170,25 Q 45,85 170,145" fill="none" stroke="#ea580c" stroke-width="2.2"/>
            <!-- Vertical line test cutting twice -->
            <line x1="105" y1="15" x2="105" y2="150" stroke="#dc2626" stroke-width="1.5" stroke-dasharray="4"/>
            <circle cx="105" cy="52" r="3.5" fill="#dc2626"/>
            <circle cx="105" cy="118" r="3.5" fill="#dc2626"/>
            <text x="50" y="160" font-size="10" font-weight="600" fill="#7c2d12">Graph B: x = y²</text>
          </g>
        </svg>`,
        steps: [
          { prefix: "Step 1: All possible vertical lines cut Graph A only once. Is Graph A a function? (Yes/No):", expected: "yes", suffix: ".", explanation: "Graph A passes the vertical line test." },
          { prefix: "Step 2: The vertical line cuts Graph B twice. Is Graph B a function? (Yes/No):", expected: "no", suffix: ".", explanation: "Graph B fails the vertical line test." }
        ]
      },
      {
        id: 4,
        section: "Section 1.1: Examples",
        source: "Mathematics Learning Centre: Section 1.1.4, Example Page 2-3",
        tag: "ex",
        title: "Domain & Range of y = √(x + 4)",
        prompt: "State the domain and range of the function \\(y = \\sqrt{x + 4}\\).",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="120" x2="360" y2="120" stroke="#64748b" stroke-width="1.5"/>
          <line x1="240" y1="15" x2="240" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <!-- Ticks -->
          <line x1="80" y1="117" x2="80" y2="123" stroke="#64748b"/><text x="72" y="135" font-size="10">−4</text>
          <line x1="120" y1="117" x2="120" y2="123" stroke="#64748b"/><text x="112" y="135" font-size="10">−3</text>
          <line x1="160" y1="117" x2="160" y2="123" stroke="#64748b"/><text x="152" y="135" font-size="10">−2</text>
          <line x1="200" y1="117" x2="200" y2="123" stroke="#64748b"/><text x="192" y="135" font-size="10">−1</text>
          <line x1="280" y1="117" x2="280" y2="123" stroke="#64748b"/><text x="278" y="135" font-size="10">1</text>
          <line x1="237" y1="70" x2="243" y2="70" stroke="#64748b"/><text x="247" y="73" font-size="10">2</text>
          <text x="350" y="135" font-size="11">x</text><text x="246" y="25" font-size="11">y</text>
          <text x="228" y="135" font-size="10">0</text>
          <!-- Curve y = sqrt(x + 4) -->
          <path d="M 80,120 Q 150,85 340,40" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="80" cy="120" r="3.5" fill="#0284c7"/>
          <circle cx="240" cy="70" r="3.5" fill="#0284c7"/>
        </svg>`,
        steps: [
          { prefix: "Step 1: Square root functions require \\(x + 4 \\ge 0\\). Domain is all real x such that (enter e.g. x ≥ -4):", expected: "x ≥ -4", suffix: ".", explanation: "\\[x + 4 \\ge 0 \\implies x \\ge -4\\]" },
          { prefix: "Step 2: Since the principal square root is non-negative, the range is all real y such that (enter e.g. y ≥ 0):", expected: "y ≥ 0", suffix: ".", explanation: "\\[y \\ge 0\\]" }
        ]
      },
      {
        id: 5,
        section: "Section 1.1: Examples",
        source: "Mathematics Learning Centre: Section 1.1.4, Example Page 3",
        tag: "ex",
        title: "Domain & Range of Parabola with Vertex (3, -3)",
        prompt: "A parabola with vertex \\((3, -3)\\) and axis of symmetry \\(x = 3\\) is sketched below. Find its domain and range.",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="50" x2="360" y2="50" stroke="#64748b" stroke-width="1.5"/>
          <line x1="90" y1="15" x2="90" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <!-- Ticks -->
          <line x1="140" y1="47" x2="140" y2="53" stroke="#64748b"/><text x="137" y="65" font-size="10">2</text>
          <line x1="190" y1="47" x2="190" y2="53" stroke="#64748b"/><text x="187" y="65" font-size="10">4</text>
          <line x1="240" y1="47" x2="240" y2="53" stroke="#64748b"/><text x="237" y="65" font-size="10">6</text>
          <line x1="87" y1="110" x2="93" y2="110" stroke="#64748b"/><text x="68" y="113" font-size="10">−3</text>
          <text x="350" y="65" font-size="11">x</text><text x="96" y="25" font-size="11">y</text>
          <text x="78" y="65" font-size="10">0</text>
          <!-- Parabola Curve -->
          <path d="M 60,15 Q 165,175 270,15" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="165" cy="110" r="3.5" fill="#0284c7"/>
          <circle cx="90" cy="50" r="3.5" fill="#0284c7"/>
          <circle cx="240" cy="50" r="3.5" fill="#0284c7"/>
          <text x="150" y="125" font-size="10" fill="#0c4a6e">(3, −3)</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: The parabola extends horizontally without bound. Domain is", expected: "all real x", suffix: ".", explanation: "A vertical parabola has domain all real numbers." },
          { prefix: "Step 2: The vertex is a global minimum at \\(y = -3\\). Range is all real y such that (enter e.g. y ≥ -3):", expected: "y ≥ -3", suffix: ".", explanation: "\\[y \\ge -3\\]" }
        ]
      },
      {
        id: 6,
        section: "Section 1.1: Examples",
        source: "Mathematics Learning Centre: Section 1.1.4, Example Page 3-4",
        tag: "ex",
        title: "Domain & Range of f(x) = 3x - x²",
        prompt: "The function \\(f(x) = 3x - x^2\\) opens downwards with vertex at \\((1.5, 2.25)\\). State its domain and range.",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="120" x2="360" y2="120" stroke="#64748b" stroke-width="1.5"/>
          <line x1="90" y1="15" x2="90" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <!-- Ticks -->
          <line x1="140" y1="117" x2="140" y2="123" stroke="#64748b"/><text x="137" y="135" font-size="10">1</text>
          <line x1="190" y1="117" x2="190" y2="123" stroke="#64748b"/><text x="187" y="135" font-size="10">2</text>
          <line x1="240" y1="117" x2="240" y2="123" stroke="#64748b"/><text x="237" y="135" font-size="10">3</text>
          <line x1="87" y1="40" x2="93" y2="40" stroke="#64748b"/><text x="75" y="43" font-size="10">2</text>
          <text x="350" y="135" font-size="11">x</text><text x="96" y="25" font-size="11">y</text>
          <text x="78" y="135" font-size="10">0</text>
          <!-- Parabola Curve -->
          <path d="M 60,150 Q 165,-50 270,150" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="165" cy="32" r="3.5" fill="#0284c7"/>
          <circle cx="90" cy="120" r="3.5" fill="#0284c7"/>
          <circle cx="240" cy="120" r="3.5" fill="#0284c7"/>
          <text x="145" y="26" font-size="10" fill="#0c4a6e">(1.5, 2.25)</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: Domain of the quadratic function is", expected: "all real x", suffix: ".", explanation: "Defined for all real x." },
          { prefix: "Step 2: The vertex is at \\((1.5, 2.25)\\) and the curve opens downwards. Range is all real y such that (enter e.g. y ≤ 2.25):", expected: "y ≤ 2.25", suffix: ".", explanation: "\\[y = -(x - 1.5)^2 + 2.25 \\implies y \\le 2.25\\]" }
        ]
      },
      {
        id: 7,
        section: "Section 1.1: Examples",
        source: "Mathematics Learning Centre: Section 1.1.4, Example Page 3-4",
        tag: "ex",
        title: "Algebraic Evaluations of f(x) = 3x - x²",
        prompt: "For \\(f(x) = 3x - x^2\\), find \\(f(q)\\) and \\(f(x^2)\\).",
        steps: [
          { prefix: "Step 1: Substitute q into the formula: \\(f(q) =\\)", expected: "3q - q^2", suffix: ".", explanation: "\\[f(q) = 3q - q^2\\]" },
          { prefix: "Step 2: Substitute x² into the formula: \\(f(x^2) = 3(x^2) - (x^2)^2 =\\)", expected: "3x^2 - x^4", suffix: ".", explanation: "\\[f(x^2) = 3x^2 - x^4\\]" }
        ]
      },
      {
        id: 8,
        section: "Section 1.1: Examples",
        source: "Mathematics Learning Centre: Section 1.1.4, Example Page 4-5",
        tag: "ex",
        title: "Domain & Range of f(x) = (x - 1)² + 1",
        prompt: "The parabola \\(f(x) = (x - 1)^2 + 1\\) is sketched below with vertex at \\((1, 1)\\). State its domain and range.",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="130" x2="360" y2="130" stroke="#64748b" stroke-width="1.5"/>
          <line x1="120" y1="15" x2="120" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <!-- Ticks -->
          <line x1="170" y1="127" x2="170" y2="133" stroke="#64748b"/><text x="167" y="145" font-size="10">1</text>
          <line x1="220" y1="127" x2="220" y2="133" stroke="#64748b"/><text x="217" y="145" font-size="10">2</text>
          <line x1="117" y1="105" x2="123" y2="105" stroke="#64748b"/><text x="105" y="108" font-size="10">1</text>
          <line x1="117" y1="80" x2="123" y2="80" stroke="#64748b"/><text x="105" y="83" font-size="10">2</text>
          <text x="350" y="145" font-size="11">x</text><text x="126" y="25" font-size="11">y</text>
          <text x="108" y="145" font-size="10">0</text>
          <!-- Parabola Curve -->
          <path d="M 70,25 Q 170,170 270,25" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="170" cy="105" r="3.5" fill="#0284c7"/>
          <circle cx="120" cy="80" r="3.5" fill="#0284c7"/>
          <text x="180" y="105" font-size="10" fill="#0c4a6e">(1, 1)</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: The function is defined for all real x. Domain is", expected: "all real x", suffix: ".", explanation: "Polynomial is defined everywhere." },
          { prefix: "Step 2: The vertex is at \\((1, 1)\\) and the curve opens upwards. Range is all real y such that (enter e.g. y ≥ 1):", expected: "y ≥ 1", suffix: ".", explanation: "Since \\((x-1)^2 \\ge 0\\), \\(y \\ge 1\\)." }
        ]
      },
      {
        id: 9,
        section: "Section 1.2: Restricting the Domain",
        source: "Mathematics Learning Centre: Section 1.2, Page 5",
        tag: "ex",
        title: "Restricted Domain: y = x² for 0 ≤ x ≤ 2",
        prompt: "The function \\(y = x^2\\) is given with specified domain \\(0 \\le x \\le 2\\). State its range.",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="130" x2="360" y2="130" stroke="#64748b" stroke-width="1.5"/>
          <line x1="80" y1="15" x2="80" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <!-- Ticks -->
          <line x1="160" y1="127" x2="160" y2="133" stroke="#64748b"/><text x="157" y="145" font-size="10">1</text>
          <line x1="240" y1="127" x2="240" y2="133" stroke="#64748b"/><text x="237" y="145" font-size="10">2</text>
          <line x1="77" y1="40" x2="83" y2="40" stroke="#64748b"/><text x="65" y="43" font-size="10">4</text>
          <text x="350" y="145" font-size="11">x</text><text x="86" y="25" font-size="11">y</text>
          <text x="68" y="145" font-size="10">0</text>
          <!-- Segment Curve -->
          <path d="M 80,130 Q 160,126 240,40" fill="none" stroke="#0284c7" stroke-width="3"/>
          <circle cx="80" cy="130" r="4" fill="#0284c7"/>
          <circle cx="240" cy="40" r="4" fill="#0284c7"/>
          <text x="248" y="44" font-size="10" fill="#0c4a6e">(2, 4)</text>
        </svg>`,
        steps: [
          { prefix: "Step 1: The endpoints are \\((0,0)\\) and \\((2,4)\\). Range is all real y such that (enter e.g. 0 ≤ y ≤ 4):", expected: "0 ≤ y ≤ 4", suffix: ".", explanation: "\\[0 \\le y \\le 4\\]" }
        ]
      },

      // ---------- SECTION 2: EXERCISES 1.3 PART 1 (Q10 - Q15) ----------
      {
        id: 10,
        section: "Section 1.3: Exercise 1",
        source: "Mathematics Learning Centre: Exercise 1.3, Q1, Page 5, 6",
        tag: "exc",
        title: "Domain & Range of f(x) = √(9 - x²)",
        prompt: "State the domain and range of \\(f(x) = \\sqrt{9 - x^2}\\).",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="130" x2="360" y2="130" stroke="#64748b" stroke-width="1.5"/>
          <line x1="190" y1="15" x2="190" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <!-- Ticks -->
          <line x1="70" y1="127" x2="70" y2="133" stroke="#64748b"/><text x="62" y="145" font-size="10">−3</text>
          <line x1="310" y1="127" x2="310" y2="133" stroke="#64748b"/><text x="307" y="145" font-size="10">3</text>
          <line x1="187" y1="30" x2="193" y2="30" stroke="#64748b"/><text x="175" y="33" font-size="10">3</text>
          <text x="350" y="145" font-size="11">x</text><text x="196" y="25" font-size="11">y</text>
          <text x="178" y="145" font-size="10">0</text>
          <!-- Semicircle -->
          <path d="M 70,130 A 120,100 0 0,1 310,130" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="70" cy="130" r="3.5" fill="#0284c7"/>
          <circle cx="310" cy="130" r="3.5" fill="#0284c7"/>
          <circle cx="190" cy="30" r="3.5" fill="#0284c7"/>
        </svg>`,
        steps: [
          { prefix: "Step 1: \\(9 - x^2 \\ge 0 \\implies x^2 \\le 9\\). Domain is all real x such that (enter e.g. -3 ≤ x ≤ 3):", expected: "-3 ≤ x ≤ 3", suffix: ".", explanation: "\\[-3 \\le x \\le 3\\]" },
          { prefix: "Step 2: The upper semicircle of radius 3 gives range all real y such that (enter e.g. 0 ≤ y ≤ 3):", expected: "0 ≤ y ≤ 3", suffix: ".", explanation: "\\[0 \\le y \\le 3\\]" }
        ]
      },
      {
        id: 11,
        section: "Section 1.3: Exercise 2a",
        source: "Mathematics Learning Centre: Exercise 1.3, Q2a, Page 5, 7",
        tag: "exc",
        title: "Domain & Range of y = √(x - 1)",
        prompt: "State the domain and range of \\(y = \\sqrt{x - 1}\\).",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="130" x2="360" y2="130" stroke="#64748b" stroke-width="1.5"/>
          <line x1="70" y1="15" x2="70" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <line x1="120" y1="127" x2="120" y2="133" stroke="#64748b"/><text x="117" y="145" font-size="10">1</text>
          <line x1="220" y1="127" x2="220" y2="133" stroke="#64748b"/><text x="217" y="145" font-size="10">3</text>
          <line x1="320" y1="127" x2="320" y2="133" stroke="#64748b"/><text x="317" y="145" font-size="10">5</text>
          <text x="350" y="145" font-size="11">x</text><text x="76" y="25" font-size="11">y</text>
          <text x="58" y="145" font-size="10">0</text>
          <!-- Curve -->
          <path d="M 120,130 Q 180,95 350,55" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="120" cy="130" r="3.5" fill="#0284c7"/>
        </svg>`,
        steps: [
          { prefix: "Step 1: Domain is all real x such that (enter e.g. x ≥ 1):", expected: "x ≥ 1", suffix: ".", explanation: "\\[x - 1 \\ge 0 \\implies x \\ge 1\\]" },
          { prefix: "Step 2: Range is all real y such that (enter e.g. y ≥ 0):", expected: "y ≥ 0", suffix: ".", explanation: "\\[y \\ge 0\\]" }
        ]
      },
      {
        id: 12,
        section: "Section 1.3: Exercise 2b",
        source: "Mathematics Learning Centre: Exercise 1.3, Q2b, Page 5, 7",
        tag: "exc",
        title: "Domain & Range of y = |2x|",
        prompt: "State the domain and range of \\(y = |2x|\\).",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="130" x2="360" y2="130" stroke="#64748b" stroke-width="1.5"/>
          <line x1="190" y1="15" x2="190" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <line x1="90" y1="127" x2="90" y2="133" stroke="#64748b"/><text x="82" y="145" font-size="10">−2</text>
          <line x1="290" y1="127" x2="290" y2="133" stroke="#64748b"/><text x="287" y="145" font-size="10">2</text>
          <text x="350" y="145" font-size="11">x</text><text x="196" y="25" font-size="11">y</text>
          <text x="178" y="145" font-size="10">0</text>
          <!-- V-Shape -->
          <path d="M 70,20 L 190,130 L 310,20" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="190" cy="130" r="3.5" fill="#0284c7"/>
        </svg>`,
        steps: [
          { prefix: "Step 1: Absolute value is defined for every real number. Domain is", expected: "all real x", suffix: ".", explanation: "Domain is all real x." },
          { prefix: "Step 2: Absolute value outputs cannot be negative. Range is all real y such that:", expected: "y ≥ 0", suffix: ".", explanation: "\\[y \\ge 0\\]" }
        ]
      },
      {
        id: 13,
        section: "Section 1.3: Exercise 2c",
        source: "Mathematics Learning Centre: Exercise 1.3, Q2c, Page 6, 7",
        tag: "exc",
        title: "Domain & Range of y = 1 / (x - 4)",
        prompt: "State the domain and range of the rational function \\(y = \\frac{1}{x - 4}\\).",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="90" x2="360" y2="90" stroke="#64748b" stroke-width="1.5"/>
          <line x1="70" y1="15" x2="70" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <!-- Asymptote x = 4 -->
          <line x1="190" y1="15" x2="190" y2="145" stroke="#dc2626" stroke-width="1.5" stroke-dasharray="4"/>
          <text x="194" y="25" font-size="10" fill="#dc2626">x = 4</text>
          <text x="350" y="105" font-size="11">x</text><text x="76" y="25" font-size="11">y</text>
          <text x="58" y="105" font-size="10">0</text>
          <!-- Hyperbola Branches -->
          <path d="M 20,95 Q 150,100 180,155" fill="none" stroke="#0284c7" stroke-width="2.2"/>
          <path d="M 200,20 Q 225,80 360,85" fill="none" stroke="#0284c7" stroke-width="2.2"/>
        </svg>`,
        steps: [
          { prefix: "Step 1: Denominator cannot equal zero: \\(x - 4 \\ne 0\\). Domain is all real x such that (enter e.g. x ≠ 4):", expected: "x ≠ 4", suffix: ".", explanation: "\\[x \\ne 4\\]" },
          { prefix: "Step 2: The horizontal asymptote is \\(y = 0\\). Range is all real y such that (enter e.g. y ≠ 0):", expected: "y ≠ 0", suffix: ".", explanation: "\\[y \\ne 0\\]" }
        ]
      },
      {
        id: 14,
        section: "Section 1.3: Exercise 2d",
        source: "Mathematics Learning Centre: Exercise 1.3, Q2d, Page 6, 7",
        tag: "exc",
        title: "Domain & Range of y = |2x| - 1",
        prompt: "State the domain and range of \\(y = |2x| - 1\\).",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="100" x2="360" y2="100" stroke="#64748b" stroke-width="1.5"/>
          <line x1="190" y1="15" x2="190" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <line x1="90" y1="97" x2="90" y2="103" stroke="#64748b"/><text x="82" y="115" font-size="10">−2</text>
          <line x1="290" y1="97" x2="290" y2="103" stroke="#64748b"/><text x="287" y="115" font-size="10">2</text>
          <line x1="187" y1="130" x2="193" y2="130" stroke="#64748b"/><text x="172" y="133" font-size="10">−1</text>
          <text x="350" y="115" font-size="11">x</text><text x="196" y="25" font-size="11">y</text>
          <text x="178" y="115" font-size="10">0</text>
          <!-- Shifted V-Shape -->
          <path d="M 60,20 L 190,130 L 320,20" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="190" cy="130" r="3.5" fill="#0284c7"/>
        </svg>`,
        steps: [
          { prefix: "Step 1: Domain is", expected: "all real x", suffix: ".", explanation: "All real x." },
          { prefix: "Step 2: Since \\(|2x| \\ge 0\\), the minimum value is -1. Range is all real y such that:", expected: "y ≥ -1", suffix: ".", explanation: "\\[y \\ge -1\\]" }
        ]
      },
      {
        id: 15,
        section: "Section 1.3: Exercise 3",
        source: "Mathematics Learning Centre: Exercise 1.3, Q3, Page 6, 7",
        tag: "exc",
        title: "Analysis of the Relation y² = x³",
        prompt: "Discuss whether or not \\(y^2 = x^3\\) represents a function.",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="80" x2="360" y2="80" stroke="#64748b" stroke-width="1.5"/>
          <line x1="70" y1="15" x2="70" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <text x="350" y="95" font-size="11">x</text><text x="76" y="25" font-size="11">y</text>
          <text x="58" y="95" font-size="10">0</text>
          <!-- Cusp Curve -->
          <path d="M 330,15 Q 120,70 70,80 Q 120,90 330,145" fill="none" stroke="#ea580c" stroke-width="2.5"/>
          <!-- Vertical line test -->
          <line x1="200" y1="15" x2="200" y2="145" stroke="#dc2626" stroke-width="1.5" stroke-dasharray="4"/>
          <circle cx="200" cy="45" r="3.5" fill="#dc2626"/>
          <circle cx="200" cy="115" r="3.5" fill="#dc2626"/>
        </svg>`,
        steps: [
          { prefix: "Step 1: If x = 1, then y² = 1 => y = 1 or y = -1. Because a single x maps to two y-values, is y² = x³ a function? (Yes/No):", expected: "no", suffix: ".", explanation: "At x = 1, y = ±1. A vertical line cuts the curve twice, so it is not a function." }
        ]
      },

      // ---------- SECTION 3: EXERCISES 1.3 PART 2 (Q16 - Q22) ----------
      {
        id: 16,
        section: "Section 1.3: Exercise 4a",
        source: "Mathematics Learning Centre: Exercise 1.3, Q4a, Page 6, 8",
        tag: "exc",
        title: "Relation Analysis: y = -√(4 - x²)",
        prompt: "Analyze the relation \\(y = -\\sqrt{4 - x^2}\\). State if it is a function, and give its domain and range.",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="40" x2="360" y2="40" stroke="#64748b" stroke-width="1.5"/>
          <line x1="190" y1="15" x2="190" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <!-- Ticks -->
          <line x1="90" y1="37" x2="90" y2="43" stroke="#64748b"/><text x="82" y="32" font-size="10">−2</text>
          <line x1="290" y1="37" x2="290" y2="43" stroke="#64748b"/><text x="287" y="32" font-size="10">2</text>
          <line x1="187" y1="120" x2="193" y2="120" stroke="#64748b"/><text x="172" y="123" font-size="10">−2</text>
          <text x="350" y="32" font-size="11">x</text><text x="196" y="25" font-size="11">y</text>
          <text x="178" y="32" font-size="10">0</text>
          <!-- Lower Semicircle -->
          <path d="M 90,40 A 100,80 0 0,0 290,40" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="90" cy="40" r="3.5" fill="#0284c7"/>
          <circle cx="290" cy="40" r="3.5" fill="#0284c7"/>
          <circle cx="190" cy="120" r="3.5" fill="#0284c7"/>
        </svg>`,
        steps: [
          { prefix: "Step 1: Does this graph represent a function? (Yes/No):", expected: "yes", suffix: ".", explanation: "It is the lower semicircle and passes the vertical line test." },
          { prefix: "Step 2: Domain is all real x such that (enter e.g. -2 ≤ x ≤ 2):", expected: "-2 ≤ x ≤ 2", suffix: ".", explanation: "\\[-2 \\le x \\le 2\\]" },
          { prefix: "Step 3: Range is all real y such that (enter e.g. -2 ≤ y ≤ 0):", expected: "-2 ≤ y ≤ 0", suffix: ".", explanation: "\\[-2 \\le y \\le 0\\]" }
        ]
      },
      {
        id: 17,
        section: "Section 1.3: Exercise 4b",
        source: "Mathematics Learning Centre: Exercise 1.3, Q4b, Page 6, 8",
        tag: "exc",
        title: "Relation Analysis: |x| - |y| = 0",
        prompt: "Analyze the relation \\(|x| - |y| = 0\\), which corresponds to the pair of lines \\(y = x\\) and \\(y = -x\\).",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="80" x2="360" y2="80" stroke="#64748b" stroke-width="1.5"/>
          <line x1="190" y1="15" x2="190" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <line x1="110" y1="77" x2="110" y2="83" stroke="#64748b"/><text x="102" y="95" font-size="10">−2</text>
          <line x1="270" y1="77" x2="270" y2="83" stroke="#64748b"/><text x="267" y="95" font-size="10">2</text>
          <text x="350" y="95" font-size="11">x</text><text x="196" y="25" font-size="11">y</text>
          <text x="178" y="95" font-size="10">0</text>
          <!-- Intersecting Lines -->
          <line x1="80" y1="140" x2="300" y2="20" stroke="#0284c7" stroke-width="2"/>
          <line x1="80" y1="20" x2="300" y2="140" stroke="#0284c7" stroke-width="2"/>
        </svg>`,
        steps: [
          { prefix: "Step 1: Any vertical line for x ≠ 0 intersects both branches (two values of y). Is this relation a function? (Yes/No):", expected: "no", suffix: ".", explanation: "Fails the vertical line test." }
        ]
      },
      {
        id: 18,
        section: "Section 1.3: Exercise 4c",
        source: "Mathematics Learning Centre: Exercise 1.3, Q4c, Page 6, 8",
        tag: "exc",
        title: "Relation Analysis: y = x³",
        prompt: "Analyze \\(y = x^3\\). Determine if it is a function, and state its domain and range.",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="80" x2="360" y2="80" stroke="#64748b" stroke-width="1.5"/>
          <line x1="190" y1="15" x2="190" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <text x="350" y="95" font-size="11">x</text><text x="196" y="25" font-size="11">y</text>
          <text x="178" y="95" font-size="10">0</text>
          <!-- Cubic Curve -->
          <path d="M 80,145 Q 170,85 190,80 Q 210,75 300,15" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="190" cy="80" r="3.5" fill="#0284c7"/>
        </svg>`,
        steps: [
          { prefix: "Step 1: Is y = x³ a function? (Yes/No):", expected: "yes", suffix: ".", explanation: "Passes the vertical line test." },
          { prefix: "Step 2: Domain is", expected: "all real x", suffix: ", and range is all real y.", explanation: "Defined and continuous across the entire real line." }
        ]
      },
      {
        id: 19,
        section: "Section 1.3: Exercise 4d",
        source: "Mathematics Learning Centre: Exercise 1.3, Q4d, Page 6, 8",
        tag: "exc",
        title: "Relation Analysis: y = x / |x|, x ≠ 0",
        prompt: "Analyze \\(y = \\frac{x}{|x|}\\) for \\(x \\ne 0\\). State if it is a function, its domain, and its range.",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="80" x2="360" y2="80" stroke="#64748b" stroke-width="1.5"/>
          <line x1="190" y1="15" x2="190" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <line x1="187" y1="40" x2="193" y2="40" stroke="#64748b"/><text x="175" y="43" font-size="10">1</text>
          <line x1="187" y1="120" x2="193" y2="120" stroke="#64748b"/><text x="172" y="123" font-size="10">−1</text>
          <text x="350" y="95" font-size="11">x</text><text x="196" y="25" font-size="11">y</text>
          <text x="178" y="95" font-size="10">0</text>
          <!-- Rays with open circles -->
          <line x1="30" y1="120" x2="185" y2="120" stroke="#0284c7" stroke-width="2.5"/>
          <line x1="195" y1="40" x2="350" y2="40" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="190" cy="120" r="4" fill="#ffffff" stroke="#0284c7" stroke-width="2"/>
          <circle cx="190" cy="40" r="4" fill="#ffffff" stroke="#0284c7" stroke-width="2"/>
        </svg>`,
        steps: [
          { prefix: "Step 1: Is this a function on its domain? (Yes/No):", expected: "yes", suffix: ".", explanation: "Each x ≠ 0 produces a unique output." },
          { prefix: "Step 2: Domain is all real x such that (enter e.g. x ≠ 0):", expected: "x ≠ 0", suffix: ".", explanation: "\\[x \\ne 0\\]" },
          { prefix: "Step 3: The only two output values are 1 and -1. Range is (enter e.g. y = ±1):", expected: "y = ±1", suffix: ".", explanation: "\\[y = \\pm 1 \\quad (\\text{or } \\{-1, 1\\})\\]" }
        ]
      },
      {
        id: 20,
        section: "Section 1.3: Exercise 4e",
        source: "Mathematics Learning Centre: Exercise 1.3, Q4e, Page 6, 8",
        tag: "exc",
        title: "Relation Analysis: |y| = x",
        prompt: "Analyze \\(|y| = x\\), which consists of the two rays \\(y = x\\) and \\(y = -x\\) for \\(x \\ge 0\\).",
        svg: `<svg width="100%" height="180" viewBox="0 0 380 160" style="max-width:380px;">
          <rect width="380" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="4"/>
          <line x1="20" y1="80" x2="360" y2="80" stroke="#64748b" stroke-width="1.5"/>
          <line x1="90" y1="15" x2="90" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <text x="350" y="95" font-size="11">x</text><text x="96" y="25" font-size="11">y</text>
          <text x="78" y="95" font-size="10">0</text>
          <!-- Horizontal V -->
          <path d="M 280,15 L 90,80 L 280,145" fill="none" stroke="#ea580c" stroke-width="2.5"/>
          <!-- Vertical Line Test -->
          <line x1="190" y1="15" x2="190" y2="145" stroke="#dc2626" stroke-width="1.5" stroke-dasharray="4"/>
          <circle cx="190" cy="45" r="3.5" fill="#dc2626"/>
          <circle cx="190" cy="115" r="3.5" fill="#dc2626"/>
        </svg>`,
        steps: [
          { prefix: "Step 1: Vertical lines for x > 0 cut the graph at two points. Is |y| = x a function? (Yes/No):", expected: "no", suffix: ".", explanation: "Fails the vertical line test." }
        ]
      },
      {
        id: 21,
        section: "Section 1.3: Exercise 5a",
        source: "Mathematics Learning Centre: Exercise 1.3, Q5a, Page 6, 8",
        tag: "exc",
        title: "Excluded Values for f(x) = √(x² - 4x)",
        prompt: "Write down the values of \\(x\\) which are NOT in the domain of \\(f(x) = \\sqrt{x^2 - 4x}\\).",
        steps: [
          { prefix: "Step 1: The function is undefined when \\(x^2 - 4x < 0 \\implies x(x - 4) < 0\\). Excluded interval is (enter e.g. 0 < x < 4):", expected: "0 < x < 4", suffix: ".", explanation: "The radicand is negative strictly inside the open interval \\(0 < x < 4\\)." }
        ]
      },
      {
        id: 22,
        section: "Section 1.3: Exercise 5b",
        source: "Mathematics Learning Centre: Exercise 1.3, Q5b, Page 6, 8",
        tag: "exc",
        title: "Excluded Values for g(x) = x / (x² - 1)",
        prompt: "Write down the values of \\(x\\) which are NOT in the domain of \\(g(x) = \\frac{x}{x^2 - 1}\\).",
        steps: [
          { prefix: "Step 1: The denominator is zero when \\(x^2 - 1 = 0\\). The values not in the domain are (enter e.g. 1, -1):", expected: "1, -1", suffix: ".", explanation: "\\[x^2 - 1 = 0 \\implies x = 1 \\text{ and } x = -1\\]" }
        ]
      }
    ];

    /* ==========================================================================
       APPLICATION ENGINE, AUDIO SYNTHESIS & TIMERS
       ========================================================================== */
    let currentStudentName = "Guest";
    let currentQuestionIndex = 0;
    let questionStates = CHAPTER_QUESTIONS.map(() => ({ completedSteps: 0, status: "unseen" }));
    let stepAttempts = {};
    let audioMuted = false;
    let totalSeconds = 0;
    let timerInterval = null;
    let activeInputRef = null;

    const AudioEngine = {
      ctx: null,
      init() {
        if (!this.ctx) {
          this.ctx = new (window.AudioContext || window.webkitAudioContext)();
        }
      },
      playTone(freq, type, duration, delay = 0) {
        if (audioMuted || !this.ctx) return;
        setTimeout(() => {
          try {
            const osc = this.ctx.createOscillator();
            const gain = this.ctx.createGain();
            osc.type = type;
            osc.frequency.setValueAtTime(freq, this.ctx.currentTime);
            gain.gain.setValueAtTime(0.12, this.ctx.currentTime);
            gain.gain.exponentialRampToValueAtTime(0.0001, this.ctx.currentTime + duration);
            osc.connect(gain);
            gain.connect(this.ctx.destination);
            osc.start();
            osc.stop(this.ctx.currentTime + duration);
          } catch (e) {
            console.warn("Audio context warning", e);
          }
        }, delay * 1000);
      },
      correct() {
        this.init();
        this.playTone(659.25, 'sine', 0.15, 0);
        this.playTone(880.00, 'sine', 0.25, 0.12);
      },
      incorrect() {
        this.init();
        this.playTone(196.00, 'triangle', 0.2, 0);
        this.playTone(146.83, 'triangle', 0.3, 0.12);
      },
      milestone() {
        this.init();
        [523.25, 659.25, 783.99, 1046.50].forEach((freq, idx) => {
          this.playTone(freq, 'sine', 0.25, idx * 0.1);
        });
      }
    };

    function startTimer() {
      if (timerInterval) clearInterval(timerInterval);
      timerInterval = setInterval(() => {
        totalSeconds++;
        const mins = String(Math.floor(totalSeconds / 60)).padStart(2, '0');
        const secs = String(totalSeconds % 60).padStart(2, '0');
        document.getElementById('timerChip').innerText = `⏱️ ${mins}:${secs}`;
      }, 1000);
    }

    function showToast(msg) {
      const t = document.getElementById('toastMessage');
      t.innerText = msg;
      t.style.display = 'block';
      setTimeout(() => { t.style.display = 'none'; }, 3500);
    }

    function initDirectLogin() {
      const name = document.getElementById('studentNameInput').value.trim() || 'Ankit Agrawal';
      currentStudentName = name;
      sessionStorage.setItem('bm_funcs_final_student', name);
      document.getElementById('userPill').innerHTML = `<strong>Student: ${name}</strong>`;
      document.getElementById('reportStudentBadge').innerHTML = `<strong>Student: ${name}</strong>`;
      document.getElementById('loginGateView').style.display = 'none';
      AudioEngine.init();
      startTimer();
      renderPalettes();
      loadQuestion(0);
      renderSolutions();
    }

    function normalizeInput(str) {
      return str.toLowerCase()
        .replace(/\s+/g, '')
        .replace(/−/g, '-')
        .replace(/>=/g, '≥')
        .replace(/<=/g, '≤')
        .replace(/!=/g, '≠')
        .replace(/and/g, ',')
        .replace(/allreals/g, 'allrealx')
        .replace(/allrealnumbers/g, 'allrealx');
    }

    function parseNumeric(val) {
      if (val.includes('/')) {
        const parts = val.split('/');
        return parseFloat(parts[0]) / parseFloat(parts[1]);
      }
      return parseFloat(val);
    }

    function checkNumericalTolerance(val1, val2) {
      if (val1.includes(',') && val2.includes(',')) {
        const p1 = val1.split(',').sort();
        const p2 = val2.split(',').sort();
        if (p1.length === p2.length) {
          return p1.every((v, i) => checkNumericalTolerance(v, p2[i]));
        }
      }
      const n1 = parseNumeric(val1);
      const n2 = parseNumeric(val2);
      if (isNaN(n1) || isNaN(n2)) return false;
      return Math.abs(n1 - n2) <= 0.05;
    }

    function switchView(viewId) {
      document.querySelectorAll('.view').forEach(v => v.classList.remove('active'));
      document.querySelectorAll('nav button').forEach(b => b.classList.remove('active'));
      document.getElementById(viewId).classList.add('active');

      const btnMap = { 'theoryView': 0, 'sheetView': 1, 'solutionsView': 2 };
      document.querySelectorAll('nav button')[btnMap[viewId]].classList.add('active');

      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function renderPalettes() {
      const sec1Grid = document.getElementById('paletteSec1Grid');
      const sec2Grid = document.getElementById('paletteSec2Grid');
      const sec3Grid = document.getElementById('paletteSec3Grid');
      sec1Grid.innerHTML = '';
      sec2Grid.innerHTML = '';
      sec3Grid.innerHTML = '';

      let doneCount = 0;
      CHAPTER_QUESTIONS.forEach((q, idx) => {
        const state = questionStates[idx];
        if (state.status === "completed") doneCount++;

        const btn = document.createElement('button');
        let stateClass = '';
        if (idx === currentQuestionIndex) {
          stateClass = 'active';
        } else if (state.status === "completed") {
          stateClass = 'completed';
        } else if (state.status === "skipped") {
          stateClass = 'skipped';
        }

        btn.className = `palette-btn ${stateClass}`;
        btn.innerText = idx + 1;
        btn.title = `${q.source}: ${q.title}`;
        btn.onclick = () => loadQuestion(idx);

        if (idx < 9) {
          sec1Grid.appendChild(btn);
        } else if (idx < 15) {
          sec2Grid.appendChild(btn);
        } else {
          sec3Grid.appendChild(btn);
        }
      });
      document.getElementById('paletteCount').innerText = `${doneCount} / ${CHAPTER_QUESTIONS.length}`;
    }

    function loadQuestion(idx) {
      currentQuestionIndex = idx;
      renderPalettes();
      const q = CHAPTER_QUESTIONS[idx];
      const state = questionStates[idx];
      const card = document.getElementById('activeQuestionCard');

      let bodyHtml = '';
      q.steps.forEach((st, sIdx) => {
        const isUnlocked = sIdx <= state.completedSteps;
        const isPassed = sIdx < state.completedSteps;
        const key = `${idx}_${sIdx}`;
        const attempts = stepAttempts[key] || 0;

        bodyHtml += `
          <div class="step-box ${isUnlocked ? 'unlocked' : ''} ${isPassed ? 'success' : ''}" id="stepBox_${idx}_${sIdx}">
            <div class="step-text-wrap">
              <span>${st.prefix}</span>
              <input type="text" class="inline-blank" id="stepInput_${idx}_${sIdx}" 
                value="${isPassed ? st.expected : ''}" 
                placeholder="enter answer"
                ${isPassed ? 'disabled' : ''} 
                onfocus="activeInputRef = this;" />
              <span>${st.suffix}</span>
              ${!isPassed ? `
                <button class="btn-verify" onclick="verifyStep(${idx}, ${sIdx})">Verify</button>
                <span class="attempts-badge">Attempts: ${attempts}/2</span>
                ${attempts >= 2 ? `<button class="btn-reveal" onclick="autoFillStep(${idx}, ${sIdx})">Auto-Fill Answer</button>` : ''}
              ` : `<span style="color: var(--green-ok); font-weight: bold; margin-left: 8px;">✓ Verified</span>`}
            </div>
            ${isPassed ? `<div style="margin-top:10px; padding:10px; background:#eff6ff; border-radius:6px; border-left:4px solid var(--brand-blue); font-size:0.92rem; color:var(--text-main);">${st.explanation}</div>` : ''}
          </div>
        `;
      });

      const prevDisabled = idx === 0 ? 'disabled' : '';
      const nextDisabled = idx === CHAPTER_QUESTIONS.length - 1 ? 'disabled' : '';

      const html = `
        <span class="concept-tag ${q.tag}">${q.section}</span>
        <span style="font-size:0.85rem; font-weight:700; color:var(--text-muted); margin-left: 8px;">[${q.source}]</span>
        <h2 style="color:var(--navy-dark); margin: 6px 0 10px 0;">Problem ${q.id}: ${q.title}</h2>
        <p style="margin-top: 8px; line-height: 1.65; font-size:1.02rem;">${q.prompt}</p>
        ${q.svg ? `<div class="svg-container">${q.svg}</div>` : ''}
        <div id="qBodyContainer">${bodyHtml}</div>

        <div class="nav-toolbar">
          <button class="btn-nav-action" onclick="navigateQuestion(-1)" ${prevDisabled}>
            ⏮ Previous
          </button>
          <div class="nav-btn-group">
            <button class="btn-nav-action btn-skip" onclick="skipQuestion()">
              ⏭ Skip Question
            </button>
            <button class="btn-nav-action" onclick="navigateQuestion(1)" ${nextDisabled}>
              Next ❯
            </button>
          </div>
        </div>
      `;

      card.innerHTML = html;
      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function autoFillStep(qIdx, sIdx) {
      const inputEl = document.getElementById(`stepInput_${qIdx}_${sIdx}`);
      if (inputEl) {
        inputEl.value = CHAPTER_QUESTIONS[qIdx].steps[sIdx].expected;
        verifyStep(qIdx, sIdx);
      }
    }

    function verifyStep(qIdx, sIdx) {
      const inputEl = document.getElementById(`stepInput_${qIdx}_${sIdx}`);
      const val = normalizeInput(inputEl.value);
      const expected = normalizeInput(CHAPTER_QUESTIONS[qIdx].steps[sIdx].expected);
      const key = `${qIdx}_${sIdx}`;

      const isCorrect = (val === expected) || checkNumericalTolerance(val, expected);

      if (isCorrect) {
        AudioEngine.correct();
        questionStates[qIdx].completedSteps++;
        if (questionStates[qIdx].completedSteps >= CHAPTER_QUESTIONS[qIdx].steps.length) {
          questionStates[qIdx].status = "completed";
          AudioEngine.milestone();
          showToast(`Problem ${qIdx + 1} Fully Completed!`);
        }
        renderPalettes();
        loadQuestion(qIdx);
        renderSolutions();
      } else {
        AudioEngine.incorrect();
        stepAttempts[key] = (stepAttempts[key] || 0) + 1;
        inputEl.style.borderColor = "var(--red-fail)";
        if (stepAttempts[key] >= 2) {
          showToast("2 attempts reached. Click 'Auto-Fill Answer' to advance.");
        } else {
          showToast("Incorrect value. Check your interval notation or domain boundary!");
        }
        loadQuestion(qIdx);
      }
    }

    function navigateQuestion(delta) {
      const target = currentQuestionIndex + delta;
      if (target >= 0 && target < CHAPTER_QUESTIONS.length) {
        loadQuestion(target);
      }
    }

    function skipQuestion() {
      if (questionStates[currentQuestionIndex].status !== "completed") {
        questionStates[currentQuestionIndex].status = "skipped";
      }
      showToast(`Problem ${currentQuestionIndex + 1} marked as Skipped (Amber/Gold).`);
      renderPalettes();
      navigateQuestion(1);
    }

    function renderSolutions() {
      const container = document.getElementById('completeSolutionsContainer');
      let completedCount = questionStates.filter(p => p.status === "completed").length;
      document.getElementById('scoreValue').innerText = `${completedCount} / ${CHAPTER_QUESTIONS.length}`;
      document.getElementById('reportStudentBadge').innerHTML = `<strong>Student: ${currentStudentName}</strong>`;

      let html = '';
      let lastSection = '';

      CHAPTER_QUESTIONS.forEach((q) => {
        if (q.section !== lastSection) {
          lastSection = q.section;
          html += `<h2 style="color:var(--navy-dark); margin: 30px 0 14px 0; border-bottom: 2px solid var(--border-soft); padding-bottom: 6px;">${lastSection}</h2>`;
        }

        html += `
          <div class="theory-card">
            <span class="concept-tag ${q.tag}">${q.section}</span>
            <span style="font-size:0.8rem; font-weight:bold; color:var(--text-muted); margin-left:6px;">${q.source}</span>
            <h3 style="margin-top:6px;">Problem ${q.id}: ${q.title}</h3>
            <p>${q.prompt}</p>
            ${q.svg ? `<div class="svg-container" style="max-width:380px; margin:12px 0;">${q.svg}</div>` : ''}
            
            <div class="proof-section" style="margin-top:10px;">
              ${q.steps.map((st, sIdx) => `
                <div style="background:#f8fafc; border-left:4px solid var(--brand-blue); padding:10px 14px; margin-bottom:8px; border-radius:0 6px 6px 0;">
                  <strong>Step ${sIdx + 1}:</strong> ${st.prefix} <strong>[ ${st.expected} ]</strong> ${st.suffix}<br/>
                  <div style="margin-top:6px;">${st.explanation}</div>
                </div>
              `).join('')}
            </div>
          </div>
        `;
      });
      container.innerHTML = html;
      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function toggleTool(tool) {
      if (tool === 'keypad') {
        document.getElementById('toolKeypad').style.display = 'block';
        document.getElementById('toolCalc').style.display = 'none';
        document.getElementById('tabKeypadBtn').classList.add('active');
        document.getElementById('tabCalcBtn').classList.remove('active');
      } else {
        document.getElementById('toolKeypad').style.display = 'none';
        document.getElementById('toolCalc').style.display = 'block';
        document.getElementById('tabCalcBtn').classList.add('active');
        document.getElementById('tabKeypadBtn').classList.remove('active');
      }
    }

    function insertSymbol(sym) {
      if (activeInputRef) {
        activeInputRef.value += sym;
        activeInputRef.focus();
      }
    }

    function pressCalc(val) { document.getElementById('calcDisplay').value += val; }
    function calcClear() { document.getElementById('calcDisplay').value = ''; }
    function calcEval() {
      try {
        document.getElementById('calcDisplay').value = eval(document.getElementById('calcDisplay').value);
      } catch (e) {
        document.getElementById('calcDisplay').value = 'Error';
      }
    }
    function calcSqrt() {
      try {
        document.getElementById('calcDisplay').value = Math.sqrt(parseFloat(document.getElementById('calcDisplay').value));
      } catch (e) {
        document.getElementById('calcDisplay').value = 'Error';
      }
    }

    document.getElementById('audioToggleBtn').onclick = () => {
      audioMuted = !audioMuted;
      document.getElementById('audioToggleBtn').innerText = audioMuted ? '🔇' : '🔊';
    };
  </script>
</body>
</html>
