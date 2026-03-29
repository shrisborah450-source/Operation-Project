<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shristi Salini Borah — Operations Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --ink: #1c1c1c; --mid: #555; --muted: #888;
    --border: #e8e4df; --bg: #faf9f7; --card: #fff;
    --blue: #1a56a0; --blue-light: #e8f0fb;
    --green: #166534; --green-light: #dcfce7; --accent: #c9773a;
  }
  body { font-family: 'DM Sans', sans-serif; background: var(--bg); color: var(--ink); line-height: 1.7; font-size: 15px; }
  body p { color: var(--mid); }

  .hero { background: var(--card); border-bottom: 1px solid var(--border); padding: 72px 0 56px; text-align: center; }
  .avatar { width: 96px; height: 96px; border-radius: 50%; background: var(--blue-light); border: 3px solid var(--blue); margin: 0 auto 24px; display: flex; align-items: center; justify-content: center; font-family: 'DM Serif Display', serif; font-size: 36px; color: var(--blue); }
  .hero h1 { font-family: 'DM Serif Display', serif; font-size: clamp(32px, 5vw, 52px); font-weight: 400; color: var(--ink); letter-spacing: -1px; margin-bottom: 8px; }
  .hero-role { font-size: 15px; color: var(--mid); font-weight: 300; margin-bottom: 28px; }
  .hero-links { display: flex; justify-content: center; gap: 12px; flex-wrap: wrap; }
  .hero-links a { text-decoration: none; font-size: 13px; color: var(--blue); background: var(--blue-light); padding: 6px 16px; border-radius: 100px; font-weight: 500; }

  .container { max-width: 860px; margin: 0 auto; padding: 0 24px; }

  .intro { padding: 56px 0 0; text-align: center; }
  .intro-text { font-family: 'DM Serif Display', serif; font-size: clamp(18px, 3vw, 24px); font-style: italic; color: var(--mid); max-width: 640px; margin: 0 auto 12px; line-height: 1.5; }
  .intro-sub { font-size: 14px; color: var(--muted); }

  .section { padding: 64px 0 0; }
  .section-label { font-size: 11px; font-weight: 500; letter-spacing: 2px; color: var(--muted); text-transform: uppercase; margin-bottom: 8px; }
  .section-title { font-family: 'DM Serif Display', serif; font-size: clamp(24px, 4vw, 36px); font-weight: 400; color: var(--ink); letter-spacing: -0.5px; margin-bottom: 24px; }
  .divider { border: none; border-top: 1px solid var(--border); margin: 56px 0 0; }

  .achievement-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 16px; margin-top: 8px; }
  .achievement-card { background: var(--card); border: 1px solid var(--border); border-radius: 12px; padding: 24px 20px; }
  .achievement-card .number { font-family: 'DM Serif Display', serif; font-size: 38px; color: var(--blue); line-height: 1; margin-bottom: 4px; }
  .achievement-card .label { font-size: 13px; color: var(--mid); line-height: 1.4; }
  .achievement-card .sublabel { font-size: 12px; color: var(--muted); margin-top: 4px; }

  .styled-table { width: 100%; border-collapse: collapse; margin-top: 8px; font-size: 14px; }
  .styled-table th { text-align: left; padding: 10px 16px; font-size: 11px; font-weight: 500; letter-spacing: 1px; text-transform: uppercase; color: #fff; background: var(--blue); }
  .styled-table th:first-child { border-radius: 8px 0 0 0; }
  .styled-table th:last-child { border-radius: 0 8px 0 0; }
  .styled-table td { padding: 12px 16px; border-bottom: 1px solid var(--border); vertical-align: top; color: var(--ink); }
  .styled-table tr:nth-child(even) td { background: #faf9f7; }
  .styled-table tr:last-child td { border-bottom: none; }
  .styled-table .row-label { font-weight: 500; color: var(--blue); white-space: nowrap; }

  .kpi-table { margin-top: 8px; border: 1px solid var(--border); border-radius: 8px; overflow: hidden; }
  .kpi-row { display: grid; grid-template-columns: 2fr 1fr 1fr 1.2fr; border-bottom: 1px solid var(--border); font-size: 14px; }
  .kpi-row.header { background: var(--blue); border-bottom: none; }
  .kpi-row.header span { color: #fff; font-size: 11px; font-weight: 500; letter-spacing: 1px; text-transform: uppercase; padding: 10px 16px; }
  .kpi-row span { padding: 11px 16px; color: var(--ink); }
  .kpi-row:nth-child(even) span { background: #faf9f7; }
  .kpi-row:last-child { border-bottom: none; }
  .status-badge { display: inline-block; background: var(--green-light); color: var(--green); font-size: 11px; font-weight: 500; padding: 2px 10px; border-radius: 100px; }

  .insight { background: var(--blue-light); border-left: 3px solid var(--blue); padding: 16px 20px; border-radius: 0 8px 8px 0; margin-top: 24px; }
  .insight strong { display: block; font-size: 11px; font-weight: 500; letter-spacing: 1px; text-transform: uppercase; color: var(--blue); margin-bottom: 4px; }
  .insight p { font-size: 14px; color: var(--mid); font-style: italic; line-height: 1.6; }

  .bottleneck-grid { display: grid; gap: 16px; margin-top: 8px; }
  .bottleneck-card { background: var(--card); border: 1px solid var(--border); border-radius: 12px; padding: 24px; }
  .bottleneck-card h4 { font-family: 'DM Serif Display', serif; font-size: 18px; font-weight: 400; color: var(--ink); margin-bottom: 16px; padding-bottom: 12px; border-bottom: 1px solid var(--border); }
  .bottleneck-row { display: grid; grid-template-columns: 100px 1fr; gap: 8px 16px; font-size: 14px; margin-bottom: 8px; align-items: start; }
  .bottleneck-row .bl { font-size: 11px; font-weight: 500; letter-spacing: 0.5px; text-transform: uppercase; color: var(--muted); padding-top: 2px; }
  .bottleneck-row .bv { color: var(--ink); }
  .bottleneck-card .outcome { margin-top: 12px; padding: 10px 14px; background: var(--green-light); border-radius: 8px; font-size: 13px; color: var(--green); font-weight: 500; }

  .tools-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 12px; margin-top: 8px; }
  .tool-card { background: var(--card); border: 1px solid var(--border); border-radius: 10px; padding: 18px 16px; }
  .tool-card .tool-name { font-weight: 500; font-size: 14px; color: var(--ink); margin-bottom: 6px; }
  .tool-card .tool-desc { font-size: 13px; color: var(--mid); line-height: 1.5; }

  .learnings-list { list-style: none; margin-top: 8px; display: grid; gap: 12px; }
  .learnings-list li { display: flex; gap: 12px; font-size: 14px; color: var(--mid); align-items: flex-start; }
  .learnings-list li::before { content: ''; width: 6px; height: 6px; min-width: 6px; border-radius: 50%; background: var(--blue); margin-top: 8px; }

  .budget-list { list-style: none; margin-top: 8px; display: grid; gap: 10px; }
  .budget-list li { display: flex; gap: 12px; font-size: 14px; color: var(--mid); padding: 12px 16px; background: var(--card); border: 1px solid var(--border); border-radius: 8px; }
  .budget-list li::before { content: ''; width: 4px; min-width: 4px; background: var(--accent); border-radius: 4px; }

  .sub-h { font-family: 'DM Serif Display', serif; font-size: 20px; font-weight: 400; color: var(--ink); margin: 32px 0 16px; }

  .footer { margin-top: 80px; padding: 40px 0; border-top: 1px solid var(--border); text-align: center; }
  .footer p { font-size: 13px; color: var(--muted); margin-bottom: 4px; }
  .footer a { color: var(--blue); text-decoration: none; }

  @media (max-width: 600px) {
    .kpi-row { grid-template-columns: 1.5fr 1fr; }
    .kpi-row span:nth-child(3), .kpi-row span:nth-child(4) { display: none; }
    .bottleneck-row { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<div class="hero">
  <div class="avatar">SS</div>
  <h1>Shristi Salini Borah</h1>
  <p class="hero-role">Operations Associate &nbsp;·&nbsp; Fintech &amp; Service Operations &nbsp;·&nbsp; Bengaluru, India</p>
  <div class="hero-links">
    <a href="mailto:shrisborah450@gmail.com">shrisborah450@gmail.com</a>
    <a href="https://www.linkedin.com/in/shristi-salini-borah-170122253" target="_blank">LinkedIn</a>
    <a href="https://github.com/shrisborah450-source/Operation-Project" target="_blank">GitHub Project</a>
  </div>
</div>

<div class="container">

  <div class="intro">
    <p class="intro-text">"This is not a textbook summary. This is how I actually work."</p>
    <p class="intro-sub">Everything here is drawn from real experience — real problems, real fixes, real outcomes.</p>
  </div>

  <hr class="divider">

  <div class="section">
    <p class="section-label">At a glance</p>
    <h2 class="section-title">Key achievements</h2>
    <div class="achievement-grid">
      <div class="achievement-card"><div class="number">30%</div><div class="label">Faster urgent ticket resolution</div><div class="sublabel">via priority triage system</div></div>
      <div class="achievement-card"><div class="number">0</div><div class="label">Regulatory breaches</div><div class="sublabel">KYC across 5 categories, 6 months</div></div>
      <div class="achievement-card"><div class="number">40%</div><div class="label">Faster leadership reporting</div><div class="sublabel">through structured MIS dashboards</div></div>
      <div class="achievement-card"><div class="number">500+</div><div class="label">Student workstreams managed</div><div class="sublabel">in Advanced Excel, Kaziranga University</div></div>
      <div class="achievement-card"><div class="number">10+</div><div class="label">Events per year</div><div class="sublabel">200+ attendees each, zero delays</div></div>
      <div class="achievement-card"><div class="number">200+</div><div class="label">Transactions reconciled</div><div class="sublabel">Zero GST revision requests via Tally ERP</div></div>
    </div>
  </div>

  <hr class="divider">

  <div class="section">
    <p class="section-label">Section 1</p>
    <h2 class="section-title">Supply chain &amp; demand-supply management</h2>
    <p>In service operations, the supply is your team's capacity. The demand is the incoming volume of tickets, cases, and approvals. The job is to make sure supply never falls too far behind demand.</p>
    <br>
    <p>At Capslock Marketplaces, ticket volumes were not uniform. Some days were quiet, some had spikes from product changes or compliance deadlines. My job was to make sure those spikes never became SLA breaches.</p>
    <br>
    <table class="styled-table">
      <thead><tr><th>Step</th><th>What I did</th><th>Result</th></tr></thead>
      <tbody>
        <tr><td class="row-label">Demand tracking</td><td>Monitored daily ticket inflow and flagged unusual spikes early</td><td>Prevented 3 potential SLA breach events</td></tr>
        <tr><td class="row-label">Capacity mapping</td><td>Tracked each team member's processing speed to estimate real throughput</td><td>Realistic workload distribution instead of uniform assignment</td></tr>
        <tr><td class="row-label">Priority tagging</td><td>Tagged tickets as urgent, standard, or low-priority at intake</td><td>Urgent resolution time reduced by 30%</td></tr>
        <tr><td class="row-label">Backlog monitoring</td><td>Tracked age of open tickets daily so nothing sat unresolved</td><td>Consistent SLA adherence across all workflows</td></tr>
        <tr><td class="row-label">Cross-team coordination</td><td>Flagged supply gaps to leads before demand exceeded capacity</td><td>Prevented downstream failures before escalation</td></tr>
      </tbody>
    </table>
    <div class="insight"><strong>My insight</strong><p>The problem almost never announces itself. Waiting for an SLA breach to react is too late. I got into the habit of checking queue depth every morning, not at the end of the day.</p></div>

    <h3 class="sub-h">Budget vs actuals</h3>
    <ul class="budget-list">
      <li>Always negotiate vendor quotes before locking budgets — the first price is rarely the best</li>
      <li>Track actuals weekly, not monthly — by the time monthly reviews happen it is too late to correct overspend</li>
      <li>Build a 10 to 15 percent contingency into every budget for unforeseen costs</li>
      <li>When actuals exceeded budget, I flagged it immediately with a root cause — never buried it in the numbers</li>
    </ul>
  </div>

  <hr class="divider">

  <div class="section">
    <p class="section-label">Section 2</p>
    <h2 class="section-title">MIS reporting &amp; KPI dashboards</h2>
    <p>I have seen what happens when reporting is treated as a checkbox. Leadership makes decisions on incomplete data, problems get noticed too late, and teams lose credibility.</p>
    <br>
    <p>At Capslock, I owned the weekly MIS reports for senior leadership. At Kaziranga, the dashboards I built were adopted as the standard format across all university departments — because I focused on making data readable, not just accurate.</p>
    <div class="insight" style="margin-top:20px;"><strong>Key principle</strong><p>A dashboard that is accurate but unreadable is not useful. A dashboard that tells a story — with clear highs, lows, and actions — is what leadership actually needs.</p></div>

    <h3 class="sub-h">How I structure a weekly MIS report</h3>
    <table class="styled-table">
      <thead><tr><th>Section</th><th>What I include</th><th>Why</th></tr></thead>
      <tbody>
        <tr><td class="row-label">Opening snapshot</td><td>3 numbers that matter most — one up, one flat, one needs attention</td><td>Sets the tone immediately</td></tr>
        <tr><td class="row-label">SLA adherence</td><td>Percent on-time, percent breached, top 3 breach reasons</td><td>Non-negotiable metric — always first</td></tr>
        <tr><td class="row-label">Quality metrics</td><td>Error rate, rework percent, first-time-right rate</td><td>Tracks if speed is costing accuracy</td></tr>
        <tr><td class="row-label">Escalations and risks</td><td>Open escalations, aged items, upcoming risks</td><td>Keeps leadership informed before crises</td></tr>
        <tr><td class="row-label">Actions and owners</td><td>What needs to happen, who owns it, by when</td><td>Every report ends with clear next steps</td></tr>
      </tbody>
    </table>

    <h3 class="sub-h">Sample KPI dashboard</h3>
    <div class="kpi-table">
      <div class="kpi-row header"><span>Metric</span><span>Target</span><span>Actual</span><span>Status</span></div>
      <div class="kpi-row"><span>SLA adherence</span><span>Above 95%</span><span>97.2%</span><span><span class="status-badge">On Track</span></span></div>
      <div class="kpi-row"><span>Urgent ticket resolution</span><span>Under 4 hrs</span><span>2.8 hrs</span><span><span class="status-badge">On Track</span></span></div>
      <div class="kpi-row"><span>First-time-right rate</span><span>Above 90%</span><span>93.1%</span><span><span class="status-badge">On Track</span></span></div>
      <div class="kpi-row"><span>KYC validation accuracy</span><span>100%</span><span>100%</span><span><span class="status-badge">On Track</span></span></div>
      <div class="kpi-row"><span>Backlog open items</span><span>Under 50</span><span>38 items</span><span><span class="status-badge">On Track</span></span></div>
      <div class="kpi-row"><span>Rework rate</span><span>Under 5%</span><span>3.2%</span><span><span class="status-badge">On Track</span></span></div>
      <div class="kpi-row"><span>Cross-team escalations</span><span>Under 5/week</span><span>3</span><span><span class="status-badge">On Track</span></span></div>
    </div>

    <h3 class="sub-h">Tools I use</h3>
    <div class="tools-grid">
      <div class="tool-card"><div class="tool-name">Advanced Excel</div><div class="tool-desc">Pivot Tables, VLOOKUP, Macros to automate data pulls and save 3 to 4 hours per cycle</div></div>
      <div class="tool-card"><div class="tool-name">Power BI</div><div class="tool-desc">Drill-through dashboards so leadership can go from summary to root cause in two clicks</div></div>
      <div class="tool-card"><div class="tool-name">Google Sheets</div><div class="tool-desc">Real-time collaboration with conditional formatting and data validation</div></div>
      <div class="tool-card"><div class="tool-name">Tally ERP</div><div class="tool-desc">GST filing, AP/AR ledgers, journal entries and monthly financial reports</div></div>
      <div class="tool-card"><div class="tool-name">ClickUp and Notion</div><div class="tool-desc">Action items from reports linked directly to live tasks, not just words on a slide</div></div>
      <div class="tool-card"><div class="tool-name">SAP MM</div><div class="tool-desc">Materials management, purchase orders, vendor and inventory tracking</div></div>
    </div>
    <div class="insight"><strong>My insight</strong><p>Once I automated the weekly data pull with Macros, I got back 3 to 4 hours every cycle. I used that time to actually analyse the data instead of just formatting it.</p></div>
  </div>

  <hr class="divider">

  <div class="section">
    <p class="section-label">Section 3</p>
    <h2 class="section-title">Process improvement</h2>
    <p>I do not wait to be asked to find problems. I look at the data and ask why things are breaking before leadership has to ask me. At Capslock, I identified and fixed 3 recurring bottlenecks.</p>
    <br>
    <div class="bottleneck-grid">
      <div class="bottleneck-card">
        <h4>Bottleneck 1 — Ticket routing delays</h4>
        <div class="bottleneck-row"><span class="bl">Problem</span><span class="bv">Urgent tickets were processed in the same order as low-priority ones. SLA breach risk was high.</span></div>
        <div class="bottleneck-row"><span class="bl">Root cause</span><span class="bv">No differentiation at intake. Everything entered the same queue.</span></div>
        <div class="bottleneck-row"><span class="bl">Fix</span><span class="bv">Designed a priority-tagging system at ticket creation. Urgent items go to a dedicated fast-track queue immediately.</span></div>
        <div class="outcome">Result: Urgent resolution time reduced by 30 percent</div>
      </div>
      <div class="bottleneck-card">
        <h4>Bottleneck 2 — KYC rework due to unclear criteria</h4>
        <div class="bottleneck-row"><span class="bl">Problem</span><span class="bv">Documents were sent back for resubmission because validators had different standards.</span></div>
        <div class="bottleneck-row"><span class="bl">Root cause</span><span class="bv">The existing SOP had gaps — edge cases were not documented.</span></div>
        <div class="bottleneck-row"><span class="bl">Fix</span><span class="bv">Rewrote the KYC validation procedure with explicit criteria for all 5 document types and examples of acceptable and rejected submissions.</span></div>
        <div class="outcome">Result: Zero regulatory breaches and a measurable drop in rework</div>
      </div>
      <div class="bottleneck-card">
        <h4>Bottleneck 3 — Cross-team escalations taking too long</h4>
        <div class="bottleneck-row"><span class="bl">Problem</span><span class="bv">Tickets needing Tech or Compliance input sat in a grey zone with no clear owner.</span></div>
        <div class="bottleneck-row"><span class="bl">Root cause</span><span class="bv">No defined escalation protocol. People did not know who to contact or by when.</span></div>
        <div class="bottleneck-row"><span class="bl">Fix</span><span class="bv">Built an escalation matrix with named owners per issue type, SLA per level, and a daily blocker check-in.</span></div>
        <div class="outcome">Result: Cross-team resolution improved, downstream SLA failures reduced</div>
      </div>
    </div>
    <div class="insight"><strong>My insight</strong><p>Every bottleneck had the same root cause — a process designed for a simpler environment that was never updated as the team grew. The fix is rarely more people. The fix is a clearer process.</p></div>

    <h3 class="sub-h">What I have learned about operations</h3>
    <ul class="learnings-list">
      <li>Data without action is just noise — every report I build ends with clear next steps</li>
      <li>Speed without accuracy is dangerous — in KYC and compliance, errors have real consequences</li>
      <li>The best process improvement is the one that sticks — I always train the team on changes, not just document them</li>
      <li>Cross-functional trust is built by being reliable — I never missed a reporting deadline in either role</li>
      <li>Operations is a leadership function — the people who do it well shape how the entire business runs</li>
    </ul>
    <div class="insight" style="margin-top:28px;"><strong>Closing thought</strong><p>The moment I stopped thinking of operations as a support role and started thinking of it as the engine of the business, my work changed. That shift is what I bring to every team I work with.</p></div>
  </div>

  <div class="footer">
    <p>Shristi Salini Borah &nbsp;·&nbsp; Operations Associate &nbsp;·&nbsp; Bengaluru</p>
    <p><a href="mailto:shrisborah450@gmail.com">shrisborah450@gmail.com</a> &nbsp;·&nbsp; <a href="https://www.linkedin.com/in/shristi-salini-borah-170122253" target="_blank">LinkedIn</a> &nbsp;·&nbsp; <a href="https://github.com/shrisborah450-source/Operation-Project" target="_blank">GitHub</a></p>
    <p style="margin-top:12px;">Last updated: March 2026</p>
  </div>

</div>
</body>
</html>
