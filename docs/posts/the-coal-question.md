---
title: "The Coal Question"
description: "Why every efficiency gain in sales has made everyone's job harder."
date: 2026-02-02
tags: [sales, outbound, email, economics, history]
---

# The Coal Question¹

**Why every efficiency gain in sales has made everyone's job harder**

<!--
<span style="font-size: 0.65rem; color: #888;">Published: February 2, 2026</span>
-->

<span style="color: #777;">
Every tool in the sales tech stack was built to make outbound more efficient. Every one of them made the channel worse. The pattern is not new. An economist identified it in 1865, studying coal.
</span>

<p style="margin-top: 1.5rem;"><strong>The Good SDR</strong></p>

He was the best SDR in his cohort. Three years ago, his sequences got replies when no one else's did. He had an intuition for it, pattern recognition built over thousands of sends. He knew which 6sense signals meant a prospect was actually in-market and which were noise. His manager asked him to train new hires. His Salesloft templates made it into the onboarding deck.

Now the title is GTM engineer—a term that barely existed when he started—but he thinks of it as the same craft, elevated. The intuition he used to apply manually now lives in Clay workflows that run while he sleeps. AI drafts messages using patterns he trained it on. Each email is different. Personalized, just like it should be.

He checks LinkedIn. Seventy-six likes on the diagram he posted last week. It's a beautiful schematic: signal capture, enrichment waterfall, branching logic based on intent scores. A VP of Sales he respects has commented: "This is gold 🔥." A dozen others are asking for the template.

He clicks to the next tab. His dashboard. Opens in the single digits. Two replies this week. One out-of-office. One that just says "PIZZA."²

He adjusts a confidence threshold, tightens a signal filter, and queues the next batch.

<p style="margin-top: 1.5rem;"><strong>The World of Aaron</strong></p>

It's the end of summer, 2002. Aaron Ross drives through the morning fog of San Francisco on his way to his new gig at Salesforce. In his mind, a system is taking shape. Three years later, after huge success, he'll write it down and call it *Predictable Revenue*.

His timing is perfect. By the turn of the century, email had replaced fax as the default mode of corporate communication.³ The channel was open, uncrowded, and ready to be used.

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

<p style="margin-top: 1.5rem;"><strong>Newcomen's Engine</strong></p>

In 1769, the bottleneck was the engine. The Newcomen, named after the Baptist ironmonger who built it in 1712 to pump water out of a coal mine, was so hungry for fuel that it could only operate where coal was essentially free — sitting on top of the pit it was draining.⁸ For sixty years it stayed there. Too hungry to move.

James Watt removed the bottleneck.⁹ His separate condenser kept the cylinder hot while the steam collapsed elsewhere. Fuel consumption fell by roughly two-thirds. By 1781 he had converted the engine's motion into rotation. A machine that had spent six decades chained to a coal mine could now drive a loom in Manchester, a hammer in Birmingham, a lathe anywhere the price of coal was no longer prohibitive.¹⁰

Parliament expected the efficient engine to conserve coal. The opposite happened: cheap steam made power available to industries and places where it had never been economical. New mills, new factories, new uses. Coal consumption rose from roughly 16 million tons in 1829 to 72 million tons by 1861.¹¹ In 1865, a twenty-nine-year-old economist at Owens College in Manchester published a book explaining why.

William Stanley Jevons had spent years with the national accounts, tracing what happened after each improvement in the efficiency of coal use. He began with iron. Early coke-smelting furnaces consumed eight tons of coal to produce a single ton of pig iron. By the 1860s, furnace design had driven that ratio below three. The saving per ton was enormous. But instead of contracting, the Scottish iron industry exploded: total coal consumption increased tenfold.¹² Efficiency had made iron cheap enough to use for things no one had previously built from iron: bridges, rails, ships, columns, pipe.

He saw the same pattern in steam itself. Watt's engine used a third of the coal. But there were now a thousand engines where there had been a hundred, driving industries that hadn't existed under Newcomen's economics.

"It is wholly a confusion of ideas to suppose that the economical use of fuel is equivalent to a diminished consumption," Jevons wrote in *The Coal Question*. "The very contrary is the truth."¹³

Jevons believed he had discovered something terrible. Britain, he argued, was innovating its way toward exhaustion. The better the engine, the more coal Britain burned.

Jevons was wrong about the exhaustion. Britain did not run out of coal.¹⁴ But the pattern he identified — that efficiency increases total consumption by making a resource useful to new users in new ways — has replicated so reliably across two centuries that economists named it after him. The Jevons paradox.¹⁵

<p style="margin-top: 1.5rem;"><strong>Jevons in Your Stack</strong></p>

The Jevons paradox is everywhere. Efficient lighting gave us Times Square, video conferencing multiplied meetings.⁴ Outbound tooling is no exception.

Predictable Revenue had made the pipeline legible as a system, but throughput was still bounded by humans. Organizational design could only go so far. Tools followed, gradually accreting what we now reverentially call "the sales tech stack."

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

    .co-exhibit--stack thead th:last-child {
      width: 72%;
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
          <th>What it solved and how volume followed</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>
            <span class="layer-name">Contact data aggregation</span>
            <span class="layer-examples">ZoomInfo, Apollo, Lusha, Clearbit</span>
          </td>
          <td>Unified databases replaced guesswork about email formats. More contacts accessible meant more contacts pursued.</td>
        </tr>
        <tr>
          <td>
            <span class="layer-name">Sequencing</span>
            <span class="layer-examples">Outreach, Salesloft, Apollo, Instantly</span>
          </td>
          <td>Automated cadences replaced manual sends. One rep could now run hundreds of prospects simultaneously.</td>
        </tr>
        <tr>
          <td>
            <span class="layer-name">Intent data</span>
            <span class="layer-examples">Bombora, 6sense, G2, TrustRadius</span>
          </td>
          <td>Behavioral signals replaced guesswork about timing. Each signal became permission to reach a new prospect.</td>
        </tr>
        <tr>
          <td>
            <span class="layer-name">Enrichment</span>
            <span class="layer-examples">Clearbit, Clay, UserGems, BuiltWith</span>
          </td>
          <td>Auto-filled profiles replaced manual research. The number of accounts a rep could work stopped having a ceiling.</td>
        </tr>
        <tr>
          <td>
            <span class="layer-name">Email warming</span>
            <span class="layer-examples">Instantly, Warmbox, Lemwarm, Mailreach</span>
          </td>
          <td>Simulated engagement bypassed domain sending limits. More volume was the point from the start.</td>
        </tr>
        <tr>
          <td>
            <span class="layer-name">AI writing</span>
            <span class="layer-examples">Lavender, Regie.ai, Copy.ai, Jasper</span>
          </td>
          <td>Generated copy replaced manual writing. Less time to personalize, more personalized emails.</td>
        </tr>
        <tr>
          <td>
            <span class="layer-name">Signals / triggers</span>
            <span class="layer-examples">Common Room, Koala, Pocus, UserGems</span>
          </td>
          <td>Automated alerts replaced manual monitoring. Every trigger became a reason to send.</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

Each row is a Watt engine. A constraint that made volume expensive was replaced by a tool that made it cheap. And each time, the efficiency was not banked. It was spent. The savings became sends, because sends were what the system rewarded.

<div style="text-align: center; margin: 2rem 0;">
  <img src="../../assets/frankenstein.png"
       alt="Frankenstein-style creatures multiplying after the switch is flipped"
       style="max-width: 70%; height: auto;">
</div>

<p style="margin-top: 1.5rem;"><strong>Saturation</strong></p>

It's striking how similar the promise is for every new tool in the stack: decouple quality from volume, and results will scale. The hypothesis always appears correct at first, and never stays correct for long.

Each new adopter sends more. So does the next. And the next. When volume across the channel compounds, the same quality stops yielding the same results.

This is what's going on at the moment. The inbox has filled. The recipient who once received a handful of cold emails per week now receives dozens per day. Open rates down double digits year over year.⁵ SDR headcount cut by more than a third.⁶

Saturation pushes senders to adjacent channels. Look around. Google Doc invitations with a pitch in the first paragraph. Slack Connect requests.⁷ Calendar invites (Google has thankfully caught up with this). When the front door stops working, the bold are the ones who climb through the window.

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

<p style="margin-top: 1.5rem;"><strong>End of the Day</strong></p>

The GTM engineer adjusts a confidence threshold, tightens a signal filter, and queues the next batch. Downstairs, a few folks on the sales team are celebrating a closed deal — one that didn't come from his sequences.

His inbox pings. A college friend, working at a Series B in Austin, has forwarded a link with a one-line message: "have you seen this?"

The link points to 11x.¹⁶ He closes the laptop, eager to join the team for a beer. Reopens the laptop.

He clicks.

<div class="co-exhibit co-exhibit--takeaways">
  <style>
    .co-exhibit--takeaways {
      margin: 2.5rem 0;
      display: flex;
      justify-content: center;
    }

    .co-exhibit--takeaways * {
      box-sizing: border-box;
    }

    .co-exhibit--takeaways .box {
      max-width: 720px;
      width: 100%;
      background: #f5f5f5;
      padding: 28px 32px;
    }

    .co-exhibit--takeaways .title {
      font-family: 'IBM Plex Sans', system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      font-size: 13px;
      font-weight: 600;
      letter-spacing: 0.4px;
      text-transform: uppercase;
      color: #222;
      margin: 0 0 18px 0;
    }

    .co-exhibit--takeaways p {
      font-family: 'IBM Plex Sans', system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      font-size: 14px;
      line-height: 1.7;
      color: #222;
      margin: 0 0 14px 0;
    }

    .co-exhibit--takeaways p:last-child {
      margin-bottom: 0;
    }

    .co-exhibit--takeaways ul {
      margin: 0;
      padding: 0 0 0 18px;
      list-style: disc;
    }

    .co-exhibit--takeaways li {
      font-family: 'IBM Plex Sans', system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      font-size: 14px;
      line-height: 1.7;
      color: #222;
      margin: 0 0 12px 0;
      padding-left: 4px;
    }

    .co-exhibit--takeaways li:last-child {
      margin-bottom: 0;
    }

    .co-exhibit--takeaways strong {
      font-weight: 600;
    }

    @media (max-width: 600px) {
      .co-exhibit--takeaways .box {
        padding: 22px 20px;
      }
      .co-exhibit--takeaways li {
        font-size: 13px;
      }
    }
  </style>

  <div class="box">
    <div class="title">Takeaways</div>

    <ul>
      <li><strong>The bottleneck was the human.</strong> When Aaron Ross wrote Predictable Revenue, labor was the binding constraint on outreach. Quality and volume were inversely linked.</li>
      <li><strong>Every layer of the stack removed a constraint on sending.</strong> Contact data, sequencing, enrichment, AI writing — each made volume cheaper.</li>
      <li><strong>Jevons paradox: when something becomes cheaper to use, people use more of it, not less.</strong> Jevons documented this with coal in 19th century Britain. </li>
      <li><strong>The efficiency was not banked. It was spent.</strong> Every saving in sending cost translated into more sends, because... Jevons.</li>
      <li><strong>Increased sending volume saturates the channel.</strong> As the inbox fills, performance declines regardless of quality. Sending better matters less in saturation.</li>
    </ul>
  </div>
</div>

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

<p>¹ The title refers to William Stanley Jevons, <em>The Coal Question: An Inquiry Concerning the Progress of the Nation, and the Probable Exhaustion of Our Coal Mines</em> (Macmillan, 1865).

<p>² "Reply PIZZA" was a viral opt-out tactic from 2023. It started as a pattern interrupt—something unexpected to break through inbox fatigue. It ended as a marker of exactly the kind of email people were trying to avoid.

<p>³ Multiple contemporaneous surveys and industry reports place the standardization of email in U.S. corporate communication at the turn of the century. By 2001–2002, email was near-universal among white-collar workers and had overtaken fax as the default medium for routine business correspondence (Pew Internet & American Life Project; IDC; Radicati Group).

<p>⁴ I could swear this increase feels like it's been by orders of magnitude, though of course it hasn't.

<p>⁵ B2B cold email open rates fell from ~36% to ~27-28% year over year. Reply rates dropped from ~6.8% in 2023 to ~5.8% in 2024. (Belkins 2025 B2B Cold Email Study; Martal Group 2025 Cold Email Statistics)

<p>⁶ Emergence Capital's 2024 "Beyond Benchmarks" study of 560+ B2B SaaS companies found 36% decreased SDR/BDR headcount—the highest reduction rate of any sales role. Only 19% increased SDR teams, the lowest expansion rate across sales functions. (SaaStr)

<p>⁷ Slack Connect requests come with embedded sequencing: Slack sends up to four reminders to accept a pending invitation before it expires. Unlike email, these notifications always pass through—no spam filter to clear. Please don't tell the SDRs.

<p>⁸ Newcomen's engine, erected at a colliery near Dudley Castle in 1712, is generally credited as the first practical steam engine. "Practical" is doing real work in that sentence — earlier devices existed, but they had an alarming tendency to explode. The Newcomen's thermal efficiency was roughly 0.5%: for every hundred units of energy in the coal it burned, it converted about half a unit into useful work. At any distance from the coal face, the economics were impossible. At the mine mouth, the fuel was waste rock. The engine survived not on engineering merit but on zero-cost inputs — a structure that will reappear later in this series.

<p>⁹ Watt's insight reportedly came during a Sunday walk on Glasgow Green in 1765, four years before the patent. He was thinking about a Newcomen model he had been asked to repair for the university's natural philosophy department. The story has the suspiciously clean shape of founding mythology, but Watt told it consistently for the rest of his life, and no one has been able to improve on it.

<p>¹⁰ The partnership between Watt and Matthew Boulton, a Birmingham manufacturer with the capital and business sense Watt lacked, is one of the great complementary pairings in industrial history. Boulton built the business model: licensing Watt engines and charging a royalty based on the fuel savings compared to a Newcomen. They literally priced their product as a fraction of the efficiency gain. Sales engineers have been doing this ever since.

<p>¹¹ These figures are drawn from Jevons's own tabulations in <em>The Coal Question</em>, Chapter III. The trajectory is not linear but exponential — consumption roughly doubling every twenty years through the first half of the nineteenth century.

<p>¹² Jevons, <em>The Coal Question</em>, Chapter VII. The specific passage: "The reduction of the consumption of coal, per ton of iron, to less than one-third of its former amount, was followed, in Scotland, by a tenfold total increase of consumption." He treats this not as an anomaly but as the central exhibit in his argument.

<p>¹³ Jevons, <em>The Coal Question</em>, Chapter VII. The full passage continues: "As a rule, new modes of economy will lead to an increase of consumption."

<p>¹⁴ His alarm reached Gladstone, who found it persuasive enough to appoint a Royal Commission. The Commission confirmed Jevons's numbers but not his despair. Britain had more coal than he thought. The paradox outlived the panic.

<p>¹⁵ Economists sometimes distinguish between the "Jevons paradox" (total consumption increases) and the weaker "rebound effect" (efficiency gains are partially offset by increased use, but total consumption may still fall). The distinction matters in energy policy and is vigorously debated. In the context of cold email, the strong form applies without controversy: every efficiency improvement has been fully converted into volume. No rebound. Full Jevons.

<p>¹⁶ 11x is one of a growing number of companies selling AI agents that perform the SDR's job autonomously: finding prospects, writing emails, sending sequences, handling replies. Another, but very special for specific reasons, Watt engine.
</div>