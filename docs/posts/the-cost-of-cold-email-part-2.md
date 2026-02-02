---
title: "The Cost of Cold Email (Part II)"
description: "Why reaching people who've never heard of you used to work, but not anymore."
date: 2026-02-02
tags: [sales, outbound, email, economics, ethics]
---

# The Cost of Cold Email (Part II)

**Why reaching people who've never heard of you used to work, but not anymore**

<!--
<span style="font-size: 0.65rem; color: #888;">Published: February 2, 2026</span>
-->

<span style="color: #777;">
Cold outbound was built on a simple formula: more emails, more pipeline. The tools got better. The targeting got sharper. The math held. Then it didn't.
</span>

<p style="margin-top: 1.5rem;"><strong>The Good SDR</strong></p>

He was the best SDR in his cohort. Three years ago, his sequences got replies when no one else's did. He had an intuition for it, pattern recognition built over thousands of sends. He knew which 6sense signals meant a prospect was actually in-market and which were noise. His manager asked him to train new hires. His Salesloft templates made it into the onboarding deck.

Now the title is GTM engineer—a term that barely existed when he started—but he thinks of it as the same craft, elevated. The intuition he used to apply manually now lives in Clay workflows that run while he sleeps. AI drafts messages using patterns he trained it on. Each email is different. Personalized, just like it should be.

He checks LinkedIn. Seventy-six likes on the diagram he posted last week. It's a beautiful schematic: signal capture, enrichment waterfall, branching logic based on intent scores. A VP of Sales he respects has commented: "This is gold 🔥." A dozen others are asking for the template.

He clicks to the next tab. His dashboard. Opens in the single digits. Two replies this week. One out-of-office. One that just says "PIZZA."¹

He adjusts a confidence threshold, tightens a signal filter, and queues the next batch.

<p style="margin-top: 1.5rem;"><strong>The World of Aaron</strong></p>

It's the end of summer, 2002. Aaron Ross drives through the morning fog of San Francisco on his way to his new gig at Salesforce. In his mind, a system is taking shape. Three years later, after huge success, he'll write it down and call it *Predictable Revenue*.

His timing is perfect. By the turn of the century, email had replaced fax as the default mode of corporate communication.² The channel was open, uncrowded, and ready to be used.

The early days felt different from today. People complained about email almost from the beginning, but cold B2B outreach was minuscule compared to what it would become. A well-crafted, properly targeted, personalized email had a good chance of being opened and read.

Labor enforced a natural constraint. A human could write and send a small volume of high-quality emails, or a higher volume of mediocre ones. The tradeoff was real and unavoidable. Quality and volume were inversely linked.

<div class="co-exhibit co-exhibit--baseline">
  <link href="https://fonts.googleapis.com/css2?family=Source+Serif+4:opsz,wght@8..60,400;8..60,600&family=IBM+Plex+Sans:wght@400;500;600&display=swap" rel="stylesheet">

  <style>
    .co-exhibit--baseline {
      margin: 2.5rem 0;
      display: flex;
      justify-content: center;
    }

    .co-exhibit--baseline * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    .co-exhibit--baseline .chart-container {
      background: #f6f6f6;
      max-width: 720px;
      width: 100%;
      padding: 28px 32px;
    }

    @media (max-width: 600px) {
      .co-exhibit--baseline .chart-container {
        padding: 22px 20px;
      }
    }

    .co-exhibit--baseline .chart-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 20px;
    }

    .co-exhibit--baseline .chart-title {
      font-family: 'Source Serif 4', serif;
      font-size: 14px;
      font-weight: 600;
      color: #1a1a1a;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    .co-exhibit--baseline .chart-label {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 10px;
      font-style: italic;
      color: #bbb;
    }

    .co-exhibit--baseline .charts-row {
      display: flex;
      gap: 16px;
      margin-bottom: 20px;
    }

    @media (max-width: 600px) {
      .co-exhibit--baseline .charts-row {
        flex-direction: column;
        gap: 24px;
      }
    }

    .co-exhibit--baseline .chart-cell {
      flex: 1;
      min-width: 0;
    }

    .co-exhibit--baseline .chart-cell-title {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 11px;
      font-weight: 500;
      color: #888;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin-bottom: 8px;
    }

    .co-exhibit--baseline .chart-cell-title span {
      color: #1a1a1a;
    }

    .co-exhibit--baseline .chart-svg {
      width: 100%;
      height: auto;
    }

    .co-exhibit--baseline .axis-line {
      stroke: #e5e5e5;
      stroke-width: 1;
    }

    .co-exhibit--baseline .axis-label {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 9px;
      fill: #888;
    }

    .co-exhibit--baseline .line-pre {
      stroke: #16a34a;
      stroke-width: 2;
      fill: none;
    }

    .co-exhibit--baseline .legend {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
      padding-bottom: 12px;
      border-bottom: 1px solid #e5e5e5;
    }

    .co-exhibit--baseline .legend-item {
      display: flex;
      align-items: center;
      gap: 6px;
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 12px;
      color: #666;
    }

    .co-exhibit--baseline .legend-line {
      width: 16px;
      height: 2px;
      border-radius: 1px;
    }

    .co-exhibit--baseline .legend-line--pre {
      background: #16a34a;
    }

    .co-exhibit--baseline .chart-footer {
      margin-top: 12px;
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 13px;
      color: #666;
      line-height: 1.6;
    }
  </style>

  <div class="chart-container">
    <div class="chart-header">
      <div class="chart-title">A human can only do so much</div>
      <div class="chart-label">Conceptual</div>
    </div>

    <div class="charts-row">
      <div class="chart-cell">
        <div class="chart-cell-title"><span>Quality</span> vs Volume</div>
        <svg class="chart-svg" viewBox="0 0 200 160" preserveAspectRatio="xMidYMid meet">
          <!-- Axes -->
          <line class="axis-line" x1="28" y1="136" x2="192" y2="136"/>
          <line class="axis-line" x1="28" y1="8" x2="28" y2="136"/>
          <!-- Labels -->
          <text class="axis-label" x="110" y="152" text-anchor="middle">Volume</text>
          <text class="axis-label" x="10" y="72" text-anchor="middle" transform="rotate(-90, 10, 72)">Quality</text>
          <!-- Line -->
          <path class="line-pre" d="M 36.2,19.52 L 183.8,117.44"/>
        </svg>
      </div>

      <div class="chart-cell">
        <div class="chart-cell-title"><span>Performance</span> vs Quality</div>
        <svg class="chart-svg" viewBox="0 0 200 160" preserveAspectRatio="xMidYMid meet">
          <!-- Axes -->
          <line class="axis-line" x1="28" y1="136" x2="192" y2="136"/>
          <line class="axis-line" x1="28" y1="8" x2="28" y2="136"/>
          <!-- Labels -->
          <text class="axis-label" x="110" y="152" text-anchor="middle">Quality</text>
          <text class="axis-label" x="10" y="72" text-anchor="middle" transform="rotate(-90, 10, 72)">Performance</text>
          <!-- Line -->
          <path class="line-pre" d="M 36.2,125.76 L 183.8,20.8"/>
        </svg>
      </div>

      <div class="chart-cell">
        <div class="chart-cell-title"><span>Performance</span> vs Volume</div>
        <svg class="chart-svg" viewBox="0 0 200 160" preserveAspectRatio="xMidYMid meet">
          <!-- Axes -->
          <line class="axis-line" x1="28" y1="136" x2="192" y2="136"/>
          <line class="axis-line" x1="28" y1="8" x2="28" y2="136"/>
          <!-- Labels -->
          <text class="axis-label" x="110" y="152" text-anchor="middle">Volume</text>
          <text class="axis-label" x="10" y="72" text-anchor="middle" transform="rotate(-90, 10, 72)">Performance</text>
          <!-- Line -->
          <path class="line-pre" d="M 36.2,28.48 L 183.8,126.4"/>
        </svg>
      </div>
    </div>

    <div class="legend">
      <div class="legend-item">
        <div class="legend-line legend-line--pre"></div>
        Pre-automation
      </div>
    </div>

    <div class="chart-footer">
      In a pre-automation world, quality decreases with volume—a human can only do so much. Scaling volume forces performance to decline in lockstep, since quality drives performance.
    </div>
  </div>
</div>

The only way to increase volume without sacrificing quality was to hire more people. That made labor the binding constraint, which created pressure to get more output from each hire.

This is where Aaron Ross enters the story. His innovation at Salesforce was organizational: split prospecting from closing, create dedicated roles, measure the handoffs. The prospecting role became the SDR. The closing role became the AE. It was a Ford moment for sales. The assembly line applied to pipeline.

Once sales became an assembly line, the logic of the factory took over. How do you make an assembly line better? You speed it up. You remove bottlenecks. You increase throughput.

<p style="margin-top: 1.5rem;"><strong>Jevons</strong></p>

Predictable Revenue made sales legible as a system, but throughput was still bounded by humans. Organizational design could only go so far. Tools followed, gradually accreting what we now reverentially call "the sales tech stack."

Sequencers automated the cadence. Contact databases replaced guesswork with unified lists. Enrichment layers removed the friction of manual research. AI writing compressed email copy from minutes to seconds. Each layer removed a constraint. Every time a constraint was removed, more volume followed.

<div class="co-exhibit co-exhibit--stack">
  <link href="https://fonts.googleapis.com/css2?family=Source+Serif+4:opsz,wght@8..60,400;8..60,600&family=IBM+Plex+Sans:wght@400;500;600&display=swap" rel="stylesheet">

  <style>
    .co-exhibit--stack {
      margin: 2.5rem 0;
      display: flex;
      justify-content: center;
    }

    .co-exhibit--stack * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    .co-exhibit--stack .table-container {
      background: #f6f6f6;
      max-width: 720px;
      width: 100%;
      padding: 28px 32px;
      overflow-x: auto;
    }

    @media (max-width: 600px) {
      .co-exhibit--stack .table-container {
        padding: 22px 20px;
      }
    }

    .co-exhibit--stack .table-title {
      font-family: 'Source Serif 4', serif;
      font-size: 14px;
      font-weight: 600;
      color: #1a1a1a;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin-bottom: 24px;
    }

    .co-exhibit--stack table {
      width: 100%;
      border-collapse: collapse;
      min-width: 500px;
    }

    .co-exhibit--stack thead th {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 11px;
      font-weight: 500;
      color: #888;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      text-align: left;
      padding: 0 12px 12px 0;
      border-bottom: 1px solid #e5e5e5;
    }

    .co-exhibit--stack thead th:first-child {
      width: 28%;
    }

    .co-exhibit--stack thead th:nth-child(2) {
      width: 40%;
    }

    .co-exhibit--stack thead th:last-child {
      width: 32%;
    }

    .co-exhibit--stack tbody td {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 13px;
      color: #666;
      line-height: 1.5;
      padding: 14px 12px 14px 0;
      border-bottom: 1px solid #e5e5e5;
      vertical-align: top;
    }

    .co-exhibit--stack tbody tr:last-child td {
      border-bottom: none;
    }

    .co-exhibit--stack .layer-name {
      font-weight: 600;
      color: #1a1a1a;
      display: block;
      margin-bottom: 2px;
    }

    .co-exhibit--stack .layer-examples {
      font-size: 11px;
      color: #888;
    }

    .co-exhibit--stack .arrow {
      color: #888;
    }
    .co-exhibit--stack .table-title .strikethrough {
      text-decoration: line-through;
      color: #888;
    }
  </style>

  <div class="table-container">
    <div class="table-title">The Stack: Seven layers of <span class="strikethrough">efficiency</span> volume</div>

    <table>
      <thead>
        <tr>
          <th>Layer</th>
          <th>What it solved</th>
          <th>Why volume followed</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>
            <span class="layer-name">Contact data aggregation</span>
            <span class="layer-examples">ZoomInfo, Apollo, Lusha, Clearbit</span>
          </td>
          <td>Guessing email formats, patching multiple lists <span class="arrow">→</span> unified and complete contact database.</td>
          <td>More contacts accessible, more contacts pursued.</td>
        </tr>
        <tr>
          <td>
            <span class="layer-name">Sequencing</span>
            <span class="layer-examples">Outreach, Salesloft, Apollo, Instantly</span>
          </td>
          <td>Sending emails one by one <span class="arrow">→</span> automated cadences that send on schedule and track engagement.</td>
          <td>One rep could run hundreds of prospects simultaneously.</td>
        </tr>
        <tr>
          <td>
            <span class="layer-name">Intent data</span>
            <span class="layer-examples">Bombora, 6sense, G2, TrustRadius</span>
          </td>
          <td>Guessing who was ready to buy <span class="arrow">→</span> signals based on web behavior and content consumption.</td>
          <td>Signals created permission to reach new prospects.</td>
        </tr>
        <tr>
          <td>
            <span class="layer-name">Enrichment</span>
            <span class="layer-examples">Clearbit, Clay, UserGems, BuiltWith</span>
          </td>
          <td>Researching each account manually <span class="arrow">→</span> auto-filled company size, tech stack, funding, job changes.</td>
          <td>Removed friction on how many accounts a rep could work.</td>
        </tr>
        <tr>
          <td>
            <span class="layer-name">Email warming</span>
            <span class="layer-examples">Instantly, Warmbox, Lemwarm, Mailreach</span>
          </td>
          <td>Domain sending limits <span class="arrow">→</span> simulated engagement to accelerate ramp up.</td>
          <td>More volume was the point from the start.</td>
        </tr>
        <tr>
          <td>
            <span class="layer-name">AI writing</span>
            <span class="layer-examples">Lavender, Regie.ai, Copy.ai, Jasper</span>
          </td>
          <td>Writing each email manually <span class="arrow">→</span> generated or rewritten copy at scale.</td>
          <td>Removed the time cost of writing personalized emails.</td>
        </tr>
        <tr>
          <td>
            <span class="layer-name">Signals / triggers</span>
            <span class="layer-examples">Common Room, Koala, Pocus, UserGems</span>
          </td>
          <td>Manually monitoring news and LinkedIn <span class="arrow">→</span> automated alerts for job changes, funding, usage.</td>
          <td>Every trigger became a reason to reach out.</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

One odd feature of efficiency is that it predictably increases total use instead of reducing it. William Stanley Jevons documented why in the 1860s studying Britain's coal industry. When something becomes cheaper to use, people find more uses for it and consume more of it overall. When steam engines became more efficient, coal consumption didn't decline. It spread: to factories, mills, transport. Britain burned more coal, not less.

Efficient lighting gave us Times Square and 24-hour cities. Video conferencing multiplied the number of meetings and attendees.³ Cheaper storage made us hoard data we'll never use. Faster bandwidth gave us infinite streaming.

So every time a new layer of the stack made sending emails cheaper, companies found more reasons to send.

<div style="text-align: center; margin: 2rem 0;">
  <img src="../../assets/frankenstein.png"
       alt="Frankenstein-style creatures multiplying after the switch is flipped"
       style="max-width: 70%; height: auto;">
</div>

<p style="margin-top: 1.5rem;"><strong>Saturation</strong></p>

It's striking how similar the promise is for every new tool in the stack: decouple quality from volume, and results will scale. The hypothesis always appears correct at first, and never stays correct for long.

Each new adopter sends more. So does the next. And the next. When volume across the channel compounds, the same quality stops yielding the same results.

This is what's going on at the moment. The inbox has filled. The recipient who once received a handful of cold emails per week now receives dozens per day. Open rates down double digits year over year.⁴ SDR headcount cut by more than a third.⁵

Saturation pushes senders to adjacent channels. Look around. Google Doc invitations with a pitch in the first paragraph. Slack Connect requests.⁶ Calendar invites (Google has thankfully caught up with this). When the front door stops working, the bold are the ones who climb through the window.

<div class="co-exhibit co-exhibit--saturation">
  <link href="https://fonts.googleapis.com/css2?family=Source+Serif+4:opsz,wght@8..60,400;8..60,600&family=IBM+Plex+Sans:wght@400;500;600&display=swap" rel="stylesheet">

  <style>
    .co-exhibit--saturation {
      margin: 2.5rem 0;
      display: flex;
      justify-content: center;
    }

    .co-exhibit--saturation * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    .co-exhibit--saturation .chart-container {
      background: #f6f6f6;
      max-width: 720px;
      width: 100%;
      padding: 28px 32px;
    }

    @media (max-width: 600px) {
      .co-exhibit--saturation .chart-container {
        padding: 22px 20px;
      }
    }

    .co-exhibit--saturation .chart-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 20px;
    }

    .co-exhibit--saturation .chart-title {
      font-family: 'Source Serif 4', serif;
      font-size: 14px;
      font-weight: 600;
      color: #1a1a1a;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    .co-exhibit--saturation .chart-label {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 10px;
      font-style: italic;
      color: #bbb;
    }

    .co-exhibit--saturation .charts-row {
      display: flex;
      gap: 16px;
      margin-bottom: 20px;
    }

    @media (max-width: 600px) {
      .co-exhibit--saturation .charts-row {
        flex-direction: column;
        gap: 24px;
      }
    }

    .co-exhibit--saturation .chart-cell {
      flex: 1;
      min-width: 0;
    }

    .co-exhibit--saturation .chart-cell-title {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 11px;
      font-weight: 500;
      color: #888;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin-bottom: 8px;
    }

    .co-exhibit--saturation .chart-cell-title span {
      color: #1a1a1a;
    }

    .co-exhibit--saturation .chart-svg {
      width: 100%;
      height: auto;
    }

    .co-exhibit--saturation .axis-line {
      stroke: #e5e5e5;
      stroke-width: 1;
    }

    .co-exhibit--saturation .axis-label {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 9px;
      fill: #888;
    }

    .co-exhibit--saturation .line-pre {
      stroke: #16a34a;
      stroke-width: 2;
      fill: none;
      opacity: 0.25;
    }

    .co-exhibit--saturation .line-first {
      stroke: #2563eb;
      stroke-width: 2;
      fill: none;
    }

    .co-exhibit--saturation .line-first-dotted {
      stroke: #2563eb;
      stroke-width: 2;
      fill: none;
      stroke-dasharray: 4,4;
    }

    .co-exhibit--saturation .arrow-line {
      stroke: #9ca3af;
      stroke-width: 1.5;
      fill: none;
    }

    .co-exhibit--saturation .arrow-label {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 8px;
      fill: #9ca3af;
    }

    .co-exhibit--saturation .arrow-bg {
      fill: #f6f6f6;
    }

    .co-exhibit--saturation .legend {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
      padding-bottom: 12px;
      border-bottom: 1px solid #e5e5e5;
    }

    .co-exhibit--saturation .legend-item {
      display: flex;
      align-items: center;
      gap: 6px;
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 12px;
      color: #666;
    }

    .co-exhibit--saturation .legend-item--dimmed {
      opacity: 0.4;
    }

    .co-exhibit--saturation .legend-line {
      width: 16px;
      height: 2px;
      border-radius: 1px;
    }

    .co-exhibit--saturation .legend-line--pre {
      background: #16a34a;
    }

    .co-exhibit--saturation .legend-line--first {
      background: #2563eb;
    }

    .co-exhibit--saturation .legend-line--dotted {
      background: transparent;
      border-bottom: 2px dashed #2563eb;
      height: 0;
    }

    .co-exhibit--saturation .chart-footer {
      margin-top: 12px;
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 13px;
      color: #666;
      line-height: 1.6;
    }
  </style>

  <div class="chart-container">
    <div class="chart-header">
      <div class="chart-title">When everyone has the same tools</div>
      <div class="chart-label">Conceptual</div>
    </div>

    <div class="charts-row">
      <div class="chart-cell">
        <div class="chart-cell-title"><span>Quality</span> vs Volume</div>
        <svg class="chart-svg" viewBox="0 0 200 160" preserveAspectRatio="xMidYMid meet">
          <defs>
            <marker id="arrowhead-h" markerWidth="4" markerHeight="4" refX="3.5" refY="2" orient="auto">
              <polygon points="0 0, 4 2, 0 4" fill="#9ca3af"/>
            </marker>
          </defs>
          <!-- Axes -->
          <line class="axis-line" x1="28" y1="136" x2="192" y2="136"/>
          <line class="axis-line" x1="28" y1="8" x2="28" y2="136"/>
          <!-- Labels -->
          <text class="axis-label" x="110" y="152" text-anchor="middle">Volume</text>
          <text class="axis-label" x="10" y="72" text-anchor="middle" transform="rotate(-90, 10, 72)">Quality</text>
          <!-- Lines -->
          <path class="line-pre" d="M 36.2,19.52 L 183.8,117.44"/>
          <path class="line-first" d="M 36.2,16.96 L 183.8,91.84"/>
          <!-- Arrow -->
          <rect class="arrow-bg" x="120" y="87" width="44" height="10" rx="1"/>
          <line class="arrow-line" x1="131.32" y1="82.24" x2="155.92" y2="82.24" marker-end="url(#arrowhead-h)"/>
          <text class="arrow-label" x="143.6" y="94" text-anchor="middle">Decoupling</text>
        </svg>
      </div>

      <div class="chart-cell">
        <div class="chart-cell-title"><span>Performance</span> vs Quality</div>
        <svg class="chart-svg" viewBox="0 0 200 160" preserveAspectRatio="xMidYMid meet">
          <defs>
            <marker id="arrowhead-v1" markerWidth="4" markerHeight="4" refX="3.5" refY="2" orient="auto">
              <polygon points="0 0, 4 2, 0 4" fill="#9ca3af"/>
            </marker>
          </defs>
          <!-- Axes -->
          <line class="axis-line" x1="28" y1="136" x2="192" y2="136"/>
          <line class="axis-line" x1="28" y1="8" x2="28" y2="136"/>
          <!-- Labels -->
          <text class="axis-label" x="110" y="152" text-anchor="middle">Quality</text>
          <text class="axis-label" x="10" y="72" text-anchor="middle" transform="rotate(-90, 10, 72)">Performance</text>
          <!-- Lines -->
          <path class="line-pre" d="M 36.2,125.76 L 183.8,20.8"/>
          <path class="line-first" d="M 36.2,125.76 L 183.8,52.8"/>
          <!-- Arrow -->
          <rect class="arrow-bg" x="94" y="54" width="44" height="10" rx="1"/>
          <line class="arrow-line" x1="142.8" y1="51.52" x2="142.8" y2="70.72" marker-end="url(#arrowhead-v1)"/>
          <text class="arrow-label" x="136.8" y="61" text-anchor="end">Decoupling</text>
        </svg>
      </div>

      <div class="chart-cell">
        <div class="chart-cell-title"><span>Performance</span> vs Volume</div>
        <svg class="chart-svg" viewBox="0 0 200 160" preserveAspectRatio="xMidYMid meet">
          <defs>
            <marker id="arrowhead-v2" markerWidth="4" markerHeight="4" refX="3.5" refY="2" orient="auto">
              <polygon points="0 0, 4 2, 0 4" fill="#9ca3af"/>
            </marker>
          </defs>
          <!-- Axes -->
          <line class="axis-line" x1="28" y1="136" x2="192" y2="136"/>
          <line class="axis-line" x1="28" y1="8" x2="28" y2="136"/>
          <!-- Labels -->
          <text class="axis-label" x="110" y="152" text-anchor="middle">Volume</text>
          <text class="axis-label" x="10" y="72" text-anchor="middle" transform="rotate(-90, 10, 72)">Performance</text>
          <!-- Lines -->
          <path class="line-pre" d="M 36.2,28.48 L 183.8,126.4"/>
          <path class="line-first-dotted" d="M 36.2,25.92 L 183.8,100.8"/>
          <path class="line-first" d="M 36.2,45.12 L 183.8,120"/>
          <!-- Arrow -->
          <rect class="arrow-bg" x="58.6" y="38" width="40" height="10" rx="1"/>
          <line class="arrow-line" x1="52.6" y1="36.16" x2="52.6" y2="52.8" marker-end="url(#arrowhead-v2)"/>
          <text class="arrow-label" x="58.6" y="45" text-anchor="start">Saturation</text>
        </svg>
      </div>
    </div>

    <div class="legend">
      <div class="legend-item legend-item--dimmed">
        <div class="legend-line legend-line--pre"></div>
        Pre-automation
      </div>
      <div class="legend-item">
        <div class="legend-line legend-line--first"></div>
        Automation
      </div>
      <div class="legend-item">
        <div class="legend-line legend-line--dotted"></div>
        Expected with Automation
      </div>
    </div>

    <div class="chart-footer">
      Automation decouples quality from volume—quality scales. But when everyone scales, saturation decouples performance from quality. The result: performance falls short of previous expectations at every level of volume.
    </div>
  </div>
</div>

<p style="margin-top: 1.5rem;"><strong>Agents Are Different</strong></p>

An agent is software that pursues an objective on its own. You give it a goal: book meetings with CFOs at mid-market fintechs. It figures out the path: Monitor signals, enrich leads, write messages, send, handle replies.

The stack before agents ran on conditional logic. If open, then send. If click, then enrich. Humans configured the rules, observed the output, adjusted the flow. Humans stood in the center of the loop.

Agents change the control system. They remove the human from the loop. With the human go two brakes on volume.

The first is operational (can't). Humans must review lists, interpret context, adjust what isn't working. Cognitive load, fatigue, management overhead. A team has finite capacity.

The second is reputational (won't). The human has her name on the email, her face on LinkedIn. She carries compliance exposure. She hesitates to burn territory she has to live in.

Agents remove both brakes. No operational constraint: marginal cost approaches zero, cognitive load is eliminated, oversight becomes optional. No reputational constraint: no name attached, no reputation at stake, no reason to hesitate. What remains are chosen limits, written in code that says "do not send more than X per day" or "do not contact if Y."

Chosen constraints are voluntary, making them vulnerable to pressure: from competitors, from your board, from your mortgage. The careful agent books ten meetings. The aggressive one burns a thousand extra prospects but books twenty. You're behind quota so you relax the limits. Then, perhaps, you remove them.

The pressure is already here. Kyle Poyar has recently framed it starkly:⁷

> "We've entered the have and have not era of AI in B2B go-to-market."

Lack of adoption represents an existential threat. So GTM teams read Poyar, study the workflows he documents, and adopt.

<p style="margin-top: 1.5rem;"><strong>How It Breaks</strong></p>

Without human review cycles to spread activity over time, two convergences emerge.

The first is timing. When a prospect posts a job listing, closes a funding round, or installs a new technology, multiple agents detect the signal simultaneously. Each decides this is the moment to reach out. Without human review cycles to stagger the response, they act in the same window.

The second is action. Agents arrive at similar tactics because they share structural constraints. Every agent runs on one of a handful of LLMs. The playbooks are public—GTM engineers share workflows like recipes. The same Clay tables, the same enrichment waterfalls, the same triggers. Independent systems arrive at the same phrasing, the same angle, the same ask.

The inbox fills with similar volume, arriving at once—five emails the same morning, same trigger, same logic. All personalized, just like they should be.

Signaling quality becomes exceedingly hard. When every message looks the same, none stand out. The rational response is more volume. But more volume makes signaling harder. The trap: compensating for declining performance requires doing more of the thing that causes decline.

Other channels hit this trap and survived. Digital ads, influencer marketing, SEO—all saturated, none collapsed. In each case, quality was legible before attention was paid: brand in ads, identity in influencers, domain authority in search.

Cold email has no equivalent. At the subject line, every sender looks identical. To know if an email is worth reading, you have to read it. When saturation crosses a threshold, recipients stop inspecting. They cannot differentiate, so they assume everything is a lemon.⁸ While digital ads, influencer marketing, SEO got harder and more expensive, cold email loses its signaling function for most senders, most of the time.

Good sellers cannot get through. They exit. Only lemons remain.

<div class="co-exhibit co-exhibit--collapse">
  <link href="https://fonts.googleapis.com/css2?family=Source+Serif+4:opsz,wght@8..60,400;8..60,600&family=IBM+Plex+Sans:wght@400;500;600&display=swap" rel="stylesheet">

  <style>
    .co-exhibit--collapse {
      margin: 2.5rem 0;
      display: flex;
      justify-content: center;
    }

    .co-exhibit--collapse * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    .co-exhibit--collapse .chart-container {
      background: #f6f6f6;
      max-width: 720px;
      width: 100%;
      padding: 28px 32px;
    }

    @media (max-width: 600px) {
      .co-exhibit--collapse .chart-container {
        padding: 22px 20px;
      }
    }

    .co-exhibit--collapse .chart-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 20px;
    }

    .co-exhibit--collapse .chart-title {
      font-family: 'Source Serif 4', serif;
      font-size: 14px;
      font-weight: 600;
      color: #1a1a1a;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    .co-exhibit--collapse .chart-label {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 10px;
      font-style: italic;
      color: #bbb;
    }

    .co-exhibit--collapse .charts-row {
      display: flex;
      gap: 16px;
      margin-bottom: 20px;
    }

    @media (max-width: 600px) {
      .co-exhibit--collapse .charts-row {
        flex-direction: column;
        gap: 24px;
      }
    }

    .co-exhibit--collapse .chart-cell {
      flex: 1;
      min-width: 0;
    }

    .co-exhibit--collapse .chart-cell-title {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 11px;
      font-weight: 500;
      color: #888;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin-bottom: 8px;
    }

    .co-exhibit--collapse .chart-cell-title span {
      color: #1a1a1a;
    }

    .co-exhibit--collapse .chart-svg {
      width: 100%;
      height: auto;
    }

    .co-exhibit--collapse .axis-line {
      stroke: #e5e5e5;
      stroke-width: 1;
    }

    .co-exhibit--collapse .axis-label {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 9px;
      fill: #888;
    }

    .co-exhibit--collapse .line-pre {
      stroke: #16a34a;
      stroke-width: 2;
      fill: none;
      opacity: 0.25;
    }

    .co-exhibit--collapse .line-first {
      stroke: #2563eb;
      stroke-width: 2;
      fill: none;
      opacity: 0.25;
    }

    .co-exhibit--collapse .line-second {
      stroke: #9333ea;
      stroke-width: 2;
      fill: none;
      opacity: 0.25;
    }

    .co-exhibit--collapse .line-agent {
      stroke: #dc2626;
      stroke-width: 2;
      fill: none;
    }

    .co-exhibit--collapse .arrow-line {
      stroke: #9ca3af;
      stroke-width: 1.5;
      fill: none;
    }

    .co-exhibit--collapse .arrow-label {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 8px;
      fill: #9ca3af;
    }

    .co-exhibit--collapse .legend {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
      padding-bottom: 12px;
      border-bottom: 1px solid #e5e5e5;
    }

    .co-exhibit--collapse .legend-item {
      display: flex;
      align-items: center;
      gap: 6px;
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 12px;
      color: #666;
    }

    .co-exhibit--collapse .legend-item--dimmed {
      opacity: 0.4;
    }

    .co-exhibit--collapse .legend-line {
      width: 16px;
      height: 2px;
      border-radius: 1px;
    }

    .co-exhibit--collapse .legend-line--pre {
      background: #16a34a;
    }

    .co-exhibit--collapse .legend-line--first {
      background: #2563eb;
    }

    .co-exhibit--collapse .legend-line--second {
      background: #9333ea;
    }

    .co-exhibit--collapse .legend-line--agent {
      background: #dc2626;
    }

    .co-exhibit--collapse .chart-footer {
      margin-top: 12px;
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 13px;
      color: #666;
      line-height: 1.6;
    }
  </style>

  <div class="chart-container">
    <div class="chart-header">
      <div class="chart-title">Agents won't save the day</div>
      <div class="chart-label">Conceptual</div>
    </div>

    <div class="charts-row">
      <div class="chart-cell">
        <div class="chart-cell-title"><span>Quality</span> vs Volume</div>
        <svg class="chart-svg" viewBox="0 0 200 160" preserveAspectRatio="xMidYMid meet">
          <!-- Axes -->
          <line class="axis-line" x1="28" y1="136" x2="192" y2="136"/>
          <line class="axis-line" x1="28" y1="8" x2="28" y2="136"/>
          <!-- Labels -->
          <text class="axis-label" x="110" y="152" text-anchor="middle">Volume</text>
          <text class="axis-label" x="10" y="72" text-anchor="middle" transform="rotate(-90, 10, 72)">Quality</text>
          <!-- Lines -->
          <path class="line-pre" d="M 36.2,19.52 L 183.8,117.44"/>
          <path class="line-first" d="M 36.2,16.96 L 183.8,91.84"/>
          <path class="line-second" d="M 36.2,15.68 L 183.8,38.72"/>
          <path class="line-agent" d="M 36.2,14.4 L 183.8,18.24"/>
        </svg>
      </div>

      <div class="chart-cell">
        <div class="chart-cell-title"><span>Performance</span> vs Quality</div>
        <svg class="chart-svg" viewBox="0 0 200 160" preserveAspectRatio="xMidYMid meet">
          <!-- Axes -->
          <line class="axis-line" x1="28" y1="136" x2="192" y2="136"/>
          <line class="axis-line" x1="28" y1="8" x2="28" y2="136"/>
          <!-- Labels -->
          <text class="axis-label" x="110" y="152" text-anchor="middle">Quality</text>
          <text class="axis-label" x="10" y="72" text-anchor="middle" transform="rotate(-90, 10, 72)">Performance</text>
          <!-- Lines -->
          <path class="line-pre" d="M 36.2,125.76 L 183.8,20.8"/>
          <path class="line-first" d="M 36.2,125.76 L 183.8,52.8"/>
          <path class="line-second" d="M 36.2,125.76 L 183.8,78.4"/>
          <path class="line-agent" d="M 36.2,125.76 L 183.8,120"/>
        </svg>
      </div>

      <div class="chart-cell">
        <div class="chart-cell-title"><span>Performance</span> vs Volume</div>
        <svg class="chart-svg" viewBox="0 0 200 160" preserveAspectRatio="xMidYMid meet">
          <defs>
            <marker id="arrowhead-curved" markerWidth="4" markerHeight="4" refX="3.5" refY="2" orient="auto">
              <polygon points="0 0, 4 2, 0 4" fill="#9ca3af"/>
            </marker>
          </defs>
          <!-- Axes -->
          <line class="axis-line" x1="28" y1="136" x2="192" y2="136"/>
          <line class="axis-line" x1="28" y1="8" x2="28" y2="136"/>
          <!-- Labels -->
          <text class="axis-label" x="110" y="152" text-anchor="middle">Volume</text>
          <text class="axis-label" x="10" y="72" text-anchor="middle" transform="rotate(-90, 10, 72)">Performance</text>
          <!-- Lines -->
          <path class="line-pre" d="M 36.2,28.48 L 183.8,126.4"/>
          <path class="line-first" d="M 36.2,45.12 L 183.8,120"/>
          <path class="line-second" d="M 36.2,82.56 L 183.8,109.06"/>
          <path class="line-agent" d="M 36.2,110.4 L 183.8,113.86"/>
          <!-- Curved Arrow -->
          <rect x="40" y="51" width="32" height="18" fill="#f6f6f6"/>
          <path class="arrow-line" d="M 90.32 69.44 Q 57.52 69.44 52.6 105.28" marker-end="url(#arrowhead-curved)"/>
          <text class="arrow-label" x="53.52" y="60">
            <tspan x="53.52" dy="0">Channel</tspan>
            <tspan x="53.52" dy="9">collapse</tspan>
          </text>
        </svg>
      </div>
    </div>

    <div class="legend">
      <div class="legend-item legend-item--dimmed">
        <div class="legend-line legend-line--pre"></div>
        Pre-automation
      </div>
      <div class="legend-item legend-item--dimmed">
        <div class="legend-line legend-line--first"></div>
        Automation
      </div>
      <div class="legend-item legend-item--dimmed">
        <div class="legend-line legend-line--second"></div>
        More automation
      </div>
      <div class="legend-item">
        <div class="legend-line legend-line--agent"></div>
        Full agentic
      </div>
    </div>

    <div class="chart-footer">
      Agents remove the last constraints. Quality maxes out. But massive convergence makes quality very hard to signal. Declining performance forces more volume, deepening saturation. Performance decouples entirely. Channel collapse is likely.
    </div>
  </div>
</div>

<p style="margin-top: 1.5rem;"><strong>The Eerie Conversation</strong></p>

There is an obvious objection. AI can filter too.

Google and Microsoft are deploying AI to screen inboxes, along with Fyxer, Perplexity, and a growing list of AI assistants for Outlook and Gmail. Instead of the VP scanning fifty subject lines, an AI reads the emails, evaluates relevance, surfaces only the ones worth opening. The attention cost shifts from human to machine.

If this works, the $25 billion attention tax disappears. The burden shifts from human labor to machine computation. The lemons problem is solved, with quality signaling again through a filter. The channel survives. Maybe improves.

If the filter works poorly, too much gets through. The VP still faces a flooded inbox. We're back to square one. But if it works well, senders adapt. They always do. And here's the challenge for Google and the others: AI filters can be reverse-engineered in ways humans cannot.

You can probe an AI filter at scale. Send ten thousand variants, observe what gets through, map the boundary, iterate. With a human, you get one shot per message. No feedback. No systematic learning.

Underneath, an AI filter is an objective function,⁹ a math problem. Enough volume reveals its boundaries. Humans don't work that way. There's no formula for earning someone's attention.

Once a channel is policed by AI, reaching the inbox becomes an engineering problem, not a social one. The senders who win are not the ones who write the most relevant messages. They're the ones who solve the puzzle fastest.

This is where agents return. The sender is no longer a human adapting content. The sender is an agent. The filter is an AI. Two systems negotiate access to human attention while the human sits behind the wall, unaware she's become the subject of a conversation she's not part of.

This echoes email warming, where machines already perform fake civility for other machines. The agent-vs-filter dynamic is the same theater, extended to the inbox itself.

The channel still looks like communication. Messages sent, messages received. But the actual exchange happens between machines. The human is the endpoint, not the participant.

It's hard to see an equilibrium where AI filtering saves cold email for senders. Either the filter fails and the problem remains. Or the filter succeeds and the channel becomes a negotiation between machines, with humans as the nominal destination but not the actual audience.

If cold email loses its ability to signal, you have to bring the signal from somewhere else.

<p style="margin-top: 1.5rem;"><strong>Stored Energy</strong></p>

Cold outreach dies. Everything that survives is warm: warmbound, intros, brand-assisted outreach. None are cold nor permissionless. And definitely not cheap.

All require stored energy: attention earned elsewhere, relationships built before the ask, reputation that preceded you into the room. You are spending access, not creating it.

Those with reserves exit. Leaving a collapsing channel is rational once you're convinced there's no money left on the table. An incumbent doesn't need cold email; they are the destination. A networked founder gets intros. A funded startup invests in content. They have alternatives. They leave.

Those without reserves have no exit. First-time founders with no brand, no network, no capital, and no built-in product virality¹⁰ (most early-stage founders) have nothing to spend. Corporates linger through inertia: teams built, targets set. Recruiters, lead gen agencies, offshore spam shops never leave. They all remain on a path that no longer leads anywhere.

The age of permissionless cheap growth is coming to an end.

<p style="margin-top: 1.5rem;"><strong>Deadweight Loss</strong></p>

But the ones without alternatives keep sending because they have no other path.

Volume rises precisely as results collapse. Sending gets cheaper even as response rates crater. The inbox fills faster precisely because the channel is dying.

Recipients still pay the attention tax. At least $25 billion worth of attention extracted each year from people who never asked for it. But the commerce that once justified the cost no longer follows. Attention wasted, sales not made: Deadweight loss.

Cold email used to be a trade-off. Society grudgingly tolerated the attention tax because the channel provided something in return: a free path to market. The cost was real, the benefit was real. An annoying but functional deal.

The deal is broken.

<p style="margin-top: 1.5rem;"><strong>Thermodynamically Impossible</strong></p>

Somewhere, the good SDR-turned-GTM engineer checks his dashboard. Opens in the single digits. One reply. Out of office. He adjusts a threshold and tries again.

<style>
.co-footnotes {
  font-size: 0.85em;
  color: #777;
  margin-top: 2.5rem;
  line-height: 1.55;
}
.co-footnotes strong {
  color: #666;
}
</style>

<div class="co-footnotes">
<strong>Footnotes</strong>

<p>¹ "Reply PIZZA" was a viral opt-out tactic from 2023. It started as a pattern interrupt—something unexpected to break through inbox fatigue. It ended as a marker of exactly the kind of email people were trying to avoid.

<p>² Multiple contemporaneous surveys and industry reports place the standardization of email in U.S. corporate communication at the turn of the century. By 2001–2002, email was near-universal among white-collar workers and had overtaken fax as the default medium for routine business correspondence (Pew Internet & American Life Project; IDC; Radicati Group).

<p>³ I could swear this increase feels like it's been by orders of magnitude, though of course it hasn't.

<p>⁴ B2B cold email open rates fell from ~36% to ~27-28% year over year. Reply rates dropped from ~6.8% in 2023 to ~5.8% in 2024. (Belkins 2025 B2B Cold Email Study; Martal Group 2025 Cold Email Statistics)

<p>⁵ Emergence Capital's 2024 "Beyond Benchmarks" study of 560+ B2B SaaS companies found 36% decreased SDR/BDR headcount—the highest reduction rate of any sales role. Only 19% increased SDR teams, the lowest expansion rate across sales functions. (SaaStr)

<p>⁶ Slack Connect requests come with embedded sequencing: Slack sends up to four reminders to accept a pending invitation before it expires. Unlike email, these notifications always pass through—no spam filter to clear.

<p>⁷ Kyle Poyar, formerly of OpenView Partners, writes Growth Unhinged, a widely-read newsletter on SaaS and PLG strategy. "2026 State of AI for B2B GTM Report"

<p>⁸ The "market for lemons" is economist George Akerlof's model for what happens when buyers can't verify quality before purchase. Sellers of good products can't credibly signal their quality, so buyers assume the worst. Good sellers exit. Only lemons remain. Akerlof won the Nobel Prize for this insight.

<p>⁹ An objective function is a mathematical formula that defines what "good" means to a system. The model tries to minimize or maximize this number. If you can figure out what the function rewards, you can optimize for it.

<p>¹⁰ Product-led growth (PLG) refers to products that spread through usage rather than sales effort. The product itself creates distribution: users invite other users, free tiers convert to paid, virality is built into the mechanics. Slack, Dropbox, and Notion are canonical examples.
