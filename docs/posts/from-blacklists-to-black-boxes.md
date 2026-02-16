---
title: "From Blacklists to Black Boxes"
description: "What is Bayesian filtering, and how it launched the first AI arms race."
date: 2026-02-16
tags: [spam, AI, machine-learning, email, bayesian-filtering]
---

# From Blacklists to Black Boxes

**What is Bayesian filtering, and how it launched the first AI arms race**

<!--
<span style="font-size: 0.65rem; color: #888;">Published: February 16, 2026</span>
-->

<span style="color: #777;">
In 2002, a Lisp programmer wrote an essay about spam. It triggered the first AI vs AI war. The defenders won that war, but the conditions enabling that victory no longer exist.
</span>

<p style="margin-top: 1.5rem;"><strong>Viagra, Mortgages, Webcams and Generals</strong></p>

The spam economy of the early 2000s ran on four products: pills, loans, pornography, and the promise that a deceased Nigerian general had named you in his will. The merchants were a relatively small number of technically competent opportunists who had discovered the same infrastructure vulnerability at roughly the same time.

An open relay was a mail server that would forward any message from anyone to anyone else, no questions asked, no authentication required. The dominant mail transfer agent of the 1990s, Sendmail, shipped with relaying enabled by default — a design inherited from ARPANET, where every node was a trusted colleague. On the open internet, which had inherited ARPANET's architecture but not its manners, this was an unlocked door with a sign reading "please come in."¹ A single operator with a list and a script could push millions of messages through other people's servers without owning a single machine.

The economics were startling. Before botnets, spammers acquired their audiences by purchasing physical CD-ROMs containing millions of email addresses scraped from the web. Ten million addresses for fifty dollars. At that price, a single sale of a sixty-dollar herbal supplement paid for the entire database. A mortgage lead-generation firm could send a million emails, watch 990,000 get deleted, see 9,500 opened, 490 clicked, and one person complete a mortgage application — and turn a profit, because that one qualified lead sold to a lender for fifty to a hundred and fifty dollars, and sending the million emails had cost almost nothing.²

At the top end, Alan Ralsky ran an operation out of suburban Detroit capable of sending one billion emails per day: pump-and-dump stocks, pharmaceutical leads. A billion sends at one-in-a-million conversion still produced a thousand daily hits at fifty to a hundred dollars each, and in a business where the infrastructure was stolen or nearly free, revenue and profit were practically the same number. He was convicted of wire fraud and sentenced to fifty-one months.³ By then he'd already become a folk hero of irony: the Detroit News profiled his $740,000 home and printed his address, Slashdot users signed him up for every physical junk mail list they could find, and Ralsky, buried under hundreds of pounds of daily mail, complained to reporters: "These people are out of their minds."

This was the battlefield: millions of messages per day, sent at near-zero cost, by operators who ranged from outright criminals running advance-fee fraud to grey-market lead brokers selling clicks to real lenders to entirely respectable companies doing their own email marketing, all of whom had simply discovered that the math worked.

In 2001, spam accounted for seven percent of global email traffic. By 2002, twenty-nine percent. By June 2003, Brightmail reported that spam had crossed the fifty percent threshold for the first time.⁴ More than half of all email on the planet was unsolicited.

<p style="margin-top: 1.5rem;"><strong>The Open-Book Exam</strong></p>

The most widely deployed spam filter was SpamAssassin, an open-source scoring framework maintained by a community of volunteers. Humans hand-wrote detection rules and assigned each a point value. A subject line in all capital letters might score 2.0. The phrase "free money" might add 1.5. Excessive exclamation marks, another point. Scores accumulated as a message passed through the ruleset. Cross the threshold (the default was 5.0) and the message was flagged as spam.

<!-- IMAGE: SpamAssassin scoring output -->
<div style="text-align: center; margin: 2rem 0 0.5rem 0;">
  <img src="../../assets/spam_assassin.png" alt="SpamAssassin scoring output, July 2003" style="max-width: 70%; height: auto; border-radius: 6px;">
  <div style="font-size: 0.7rem; color: #666;">Germans. Pioneering livecam porn spam since 2003.⁵</div>
</div>

The screenshot above is a SpamAssassin report from 2003. The score reads 5.3, just above the threshold, with every rule that fired listed alongside its point value: the entire logic of the defense, laid bare in the output. A spammer could compose a message, run it through SpamAssassin, read the score, and adjust until it slipped under the threshold. Rewrite the subject line. Drop a trigger word. Add a line of innocuous text. Check again. 4.9. Send. Defense as open-book exam.

Other filters were simpler and failed in simpler ways. McAfee's SpamKiller relied on keyword matching: scan for forbidden words, flag the message. The evasion was trivial. V1agra. M0rtgage. Fr.ee. A filter built on spelling was beaten by misspelling.⁶

Brightmail, a commercial anti-spam service used by major ISPs, took a different approach. It deployed a global network of decoy email addresses — honeypots. When a message arrived at a honeypot, Brightmail computed a digital fingerprint of it and distributed that fingerprint to subscribers. If a real email matched a known fingerprint, it was spam. The system was elegant against true bulk: identical messages sent to millions of addresses all produced the same fingerprint. But it was blind to variation. Change a single character, a comma or a space or a digit in a phone number, and the fingerprint changed entirely. The match failed. The message sailed through.⁷

All three failed differently, but the root cause was the same. Each assumed that spam was a fixed target: a known word, a known pattern, a known message. The attacker only had to change the surface. None of these systems could learn, and none needed to be broken. The defense logic was visible, so the attacker could study it and work backward to evade it.

<p style="margin-top: 1.5rem;"><strong>A Plan for Spam</strong></p>

In August 2002, Paul Graham published an essay called "A Plan for Spam" on his personal website. Graham was a programmer and essayist who had sold his startup Viaweb to Yahoo in 1998, and had since been designing a new programming language called Arc, building a web-based email client to exercise it. The client needed a spam filter. He tried writing rules by hand, got addicted to the competitive game of spotting spam features. "To recognize individual spam features you have to try to get into the mind of the spammer," he wrote, "and frankly I want to spend as little time inside the minds of spammers as possible." He tried a statistical approach instead, and found immediately that it was much cleverer than he had been. The essay was a report on that experiment.⁸

Instead of rules about what spam says, build a model of what spam looks like statistically. Don't match words. Count tokens. Don't write rules. Learn probabilities. The filter would be trained, not programmed.

Nobody called it machine learning, let alone Artificial Intelligence, but that's what it was: a system that learned patterns from labeled data and made probabilistic predictions on new inputs. Graham's filter was built on Bayes' theorem, a formula published in 1763 that has been terrorizing college freshmen ever since.⁹ The theorem describes how to update your beliefs when you encounter new evidence. The easiest way to understand it is to watch it fight.

<p style="margin-top: 1.5rem;"><strong>The First AI in Your Inbox</strong></p>

A token, in Graham's system, was not a word as a dictionary defines it. It was any character string the parser encountered: a conventional word like "meeting," a cluster of exclamation marks, an HTML fragment like `<font color="red">`, a misspelling, a header artifact, a string of digits. The filter did not care what any of these meant. It cared how often each one appeared in spam versus legitimate email.¹⁰

V1agra was not a clever disguise anymore. It was just another token. The filter had never seen it in ham, had seen it constantly in spam, and assigned it a probability near 1.0. The spammer's instinct, change the spelling, ran into a system that didn't read spelling in the first place. Every new mutation was simply a new token to be counted, classified, and filed.

But the filter learned something else too: what your email looked like.

Before it could classify anything, the filter had to be trained.¹¹ The user fed it two collections: a folder of known spam and a folder of known legitimate messages, which the community began calling "ham." The filter walked through both and counted. How often did each token appear in spam? How often in ham? After training, every token carried a number between 0 and 1 representing how likely a message containing it was to be spam. "Viagra" in three hundred spam messages and zero ham messages: probability near 1.0. "Tonight" in two hundred ham messages and two spam messages: probability near 0.0. A token never seen before was assigned a neutral 0.4, a slight lean toward ham on the assumption that novel words were more likely to appear in legitimate email than in the repetitive vocabulary of spam.

My probability table was different from yours. "Free consultation" was strongly spammy for an engineer and perfectly legitimate for a dentist. The words you used every day formed a shield around your inbox. For the first time, the absence of normal language was itself a signal. Every previous filter was a detector of bad signals. Graham's was equally a detector of good. A message saturated in the vocabulary of your daily work, "invoice," "Tuesday," "the board approved," was not merely unpenalized. It was actively protected.

In traditional programming, a human writes the logic and the machine executes it. In machine learning, a human provides the data. The resulting model, the thousands of weights and probabilities that determine behavior, is produced by the process, not by the programmer. The programmer can inspect the model. But the model is not a set of instructions anyone wrote. It is a statistical artifact, shaped by data, too large and entangled for any human to hold in their head. No single person, not even the person who wrote the code, could look at a trained filter and predict with certainty what it would do with a given message. You could test it. You could not read it.

Graham built this in a few hundred lines of Lisp, running on a single laptop. But the structure was there: training data, probabilistic classification, a verdict that emerged from patterns rather than rules. The first machine to fight for human attention against other machines was a spam filter running in an apartment.

<p style="margin-top: 1.5rem;"><strong>Probing the Black Box</strong></p>

The industry moved fast. Within eighteen months, Graham's approach had been absorbed into infrastructure at every scale. SpamAssassin integrated a Bayesian engine alongside its hand-written rules; sysadmins could now train a local probability map on their own servers.¹² Mozilla Thunderbird placed machine learning at the center of the consumer experience, its "Junk" button quietly reframing the act of deleting spam as an act of training.¹³ Microsoft's SmartScreen aggregated classifications from hundreds of thousands of volunteers to train a single shared model for all of Outlook and Exchange.¹⁴ The trajectory: personal, personal, then centralized. Each step concentrated more labeling power and more compute in fewer hands.

<!-- IMAGE: Thunderbird junk detection -->
<div style="text-align: center; margin: 2rem 0 0.5rem 0;">
  <img src="../../assets/junk_button.png" alt="Thunderbird junk detection interface" style="max-width: 70%; height: auto; border-radius: 6px;">
  <div style="font-size: 0.7rem; color: #666;">Somewhere, Neil is still waiting for a reply.¹³</div>
</div>

But the moment filtering became a learned model, the contest changed. The attacker was no longer reading a rulebook and finding gaps but probing a black box and mapping its shape.

Spammers understood the logic instantly: if ham tokens protect a message, inject ham tokens. They began appending blocks of innocent text to their emails, paragraphs lifted from novels, random dictionary words, fragments of news articles. Some used passages from Moby Dick.¹⁵

The filter would encounter "whale," "Ahab," "doubloon," and "harpoon" sitting beneath an advertisement for discount Viagra, and it would hesitate. The math explains why.

An email arrives. The filter collects the fifteen most "interesting" tokens in the message, the ones whose spam probability is farthest from 0.5 in either direction, and combines them. Fifteen, not all. If the filter weighed every token in the message, a single long paragraph of innocent text could drown the spam signal entirely. By limiting the calculation to the most extreme outliers, Graham forced the attacker to produce very high-quality ham to move the needle. If the email contains "Viagra" (near 1.0) and "pharmacy" (near 1.0), but also "whale" (near 0.0) and "doubloon" (near 0.0) and "harpoon" (near 0.0), the combined probability shifts. Spam tokens pull toward 1. Ham tokens pull toward 0. The final score is the product of the tug-of-war. Without the Melville, the message scores 0.99. With it, the ham tokens dilute the signal, dragging the probability toward the center, away from Graham's 0.9 threshold. The message slips through. Bayesian poisoning: the statistical symmetry at the heart of the filter, weaponized against it.

<!-- IMAGE: Whale illustration -->
<div style="text-align: center; margin: 2rem 0 0.5rem 0;">
  <img src="../../assets/whale.png" alt="Whale in submarine searchlight" style="max-width: 70%; height: auto; border-radius: 6px;">
</div>

The more substantive attack was adversarial probing. Sending was free and the filter was a mathematical function. Understanding the model was unnecessary. Mapping it was enough. They set up test labs with private installations of the most popular open-source filters and ran canary messages through them before launching a campaign. If the local filter caught the message, a script would swap synonyms: "money" for "cash," "opportunity" for "proposition," until the score dropped below the threshold. Machine-learning researchers now call this a substitution attack. In 2003, it was just called getting the email through.

At scale, the logic extended beyond local testing. Send a hundred variants of the same pitch to live inboxes. Observe which ones get through. Adjust the ones that don't. Repeat. Each send was a query against the model's decision boundary, and each result, delivered or filtered, was a data point. Over enough iterations, the attacker could trace the shape of the black box from the outside without ever seeing the inside. This was black-box adversarial attack, conducted at industrial scale by people who had never heard the term.

Step back and watch the picture: every structural advantage favored the attacker. Sending was free; there was no cost for failure. The model was a fixed mathematical function; it could be mapped. The defender couldn't afford aggressive filtering; a false positive meant a missed invoice, a lost job offer, a deal that never happened. The blame for a false positive always fell on the filter, never on the spammer who caused the noise in the first place.

And yet —

<p style="margin-top: 1.5rem;"><strong>One Gigabyte and One Button</strong></p>

In April 2004, Google offered every email user on earth a gigabyte of free storage. Hotmail gave you two megabytes. Miss a few days of housekeeping and new messages bounced. You deleted emails like you took out the trash: constantly, knowing that anything you kept meant something else had to go. Google was offering five hundred times that. The promise was that you would never have to waste time deleting an email again.

A promise like that required a second, quieter one: that the archive wouldn't fill with junk. Google couldn't offer infinite storage without solving spam. So it built a centralized filter trained by its own users. Every time anyone on the platform clicked "Report Spam," the signal updated a model that could vaccinate every other inbox in near-real-time. A campaign that hit a thousand users in the morning could be dead by the afternoon, not because an engineer wrote a new rule, but because the model had learned the pattern from the first hundred clicks and propagated the defense across the entire network.

Gmail layered personalized models on top of the global one. Spam for one user could be ham for another. The system didn't just learn what spam looked like in general. It learned what spam looked like to you, and what your legitimate email looked like to it. The Bayesian insight — that ham is as powerful as spam — was now operating at the scale of hundreds of millions of inboxes, with a self reinforcing feedback loop: users labeled, the model improved, spam declined, users labeled more confidently.¹⁶

It worked. The inbox, which had been nearly unusable, became functional again. The defenders won.

<p style="margin-top: 1.5rem;"><strong>Routing Around</strong></p>

By 2007, spam still accounted for roughly ninety percent of all email sent, but almost none of it reached the inbox.¹⁷ Graham's innovation applied at Google scale had won so decisively that most users quickly forgot there was ever a war. The spammers? Shrugged and moved on.

Within months of Bayesian filters becoming standard, spammers rendered their payloads as JPEGs. The pitch that would have scored 0.99 as text was now a single image file. The filter couldn't parse it, tokenize it, or score it. It had nothing to count.

When filters learned to read images, the attackers moved to botnets, distributing their sending across millions of compromised home computers. When botnets were dismantled, they moved to snowshoe distribution across thousands of IPs and domains. Each defensive victory was real, and addressed exactly one tactic. Each time, the attacker walked to the next undefended front.

The Bayesian victory over text spam was the most impressive. It held. The text front was genuinely won, and it would stay won for twenty years.¹⁸ When it finally reopened, sometime around 2023,¹⁹ it wasn't because the attackers had found a way to beat the filter. The conditions that made the filter work had simply disappeared.

<p style="margin-top: 1.5rem;"><strong>Semantic Zero-Day</strong></p>

The defenders won the first AI war over human attention because of three conditions specific to that era.

The first was bulk. A single campaign sent millions of identical or near-identical messages. The moment one user flagged it, the platform could cluster the pattern and kill the campaign across every inbox. The attacker's volume was both the weapon and the weakness. Today, a sender using a language model generates ten thousand unique, personalized messages. There is no pattern to cluster. No campaign to kill. Every message is a semantic zero-day.²⁰

Then there was compute. No other entity could run probabilistic classification across billions of messages in real time, retrain continuously, and maintain personalized filters for hundreds of millions of users. The defender had a resource advantage the attacker couldn't match. Today, attackers run open-source language models on a single consumer GPU, testing thousands of variations against simulated filters before a single message is sent. The arms are matched. The constraints are not: the defender still can't afford a false positive.

The last was the shape of the data. In 2002, the vocabulary of spam and the vocabulary of legitimate email sat at opposite ends of the probability space with almost nothing in between. "Dear Beloved" and "Q3 revenue forecast" do not share tokens. The statistical distance between the two sides was so vast that even imperfect models worked. You didn't need precision when the target was on the other side of a canyon.

<!-- [EXHIBIT: Twin Peaks — token spam probability distributions, 2002 vs 2025] -->
<div class="co-exhibit co-exhibit--peaks">
  <link href="https://fonts.googleapis.com/css2?family=Source+Serif+4:opsz,wght@8..60,400;8..60,600&family=IBM+Plex+Sans:wght@400;500;600&display=swap" rel="stylesheet">

  <style>
    .co-exhibit--peaks {
      margin: 2.5rem 0;
      display: flex;
      justify-content: center;
    }

    .co-exhibit--peaks * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    .co-exhibit--peaks .chart-container {
      background: #f6f6f6;
      max-width: 720px;
      width: 100%;
      padding: 28px 32px;
    }

    @media (max-width: 600px) {
      .co-exhibit--peaks .chart-container {
        padding: 22px 20px;
      }
    }

    .co-exhibit--peaks .chart-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 20px;
    }

    .co-exhibit--peaks .chart-title {
      font-family: 'Source Serif 4', serif;
      font-size: 14px;
      font-weight: 600;
      color: #1a1a1a;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    .co-exhibit--peaks .chart-label {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 10px;
      font-style: italic;
      color: #bbb;
    }

    .co-exhibit--peaks .charts-row {
      display: flex;
      gap: 24px;
      margin-bottom: 20px;
    }

    @media (max-width: 600px) {
      .co-exhibit--peaks .charts-row {
        flex-direction: column;
        gap: 24px;
      }
    }

    .co-exhibit--peaks .chart-cell {
      flex: 1;
      min-width: 0;
    }

    .co-exhibit--peaks .chart-cell-title {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 11px;
      font-weight: 500;
      color: #888;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      margin-bottom: 8px;
    }

    .co-exhibit--peaks .chart-cell-title span {
      color: #1a1a1a;
    }

    .co-exhibit--peaks .chart-svg {
      width: 100%;
      height: auto;
    }

    .co-exhibit--peaks .axis-line {
      stroke: #e0e0e0;
      stroke-width: 1;
    }

    .co-exhibit--peaks .axis-label {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 9px;
      fill: #999;
    }

    .co-exhibit--peaks .ham-fill {
      fill: #2563eb;
      opacity: 0.12;
    }

    .co-exhibit--peaks .ham-stroke {
      stroke: #2563eb;
      stroke-width: 2;
      fill: none;
    }

    .co-exhibit--peaks .spam-fill {
      fill: #dc2626;
      opacity: 0.12;
    }

    .co-exhibit--peaks .spam-stroke {
      stroke: #dc2626;
      stroke-width: 2;
      fill: none;
    }

    .co-exhibit--peaks .canyon-label {
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 8.5px;
      fill: #999;
      letter-spacing: 0.3px;
    }

    .co-exhibit--peaks .canyon-bracket {
      stroke: #ccc;
      stroke-width: 1;
      fill: none;
    }

    .co-exhibit--peaks .legend {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
      padding-bottom: 12px;
      border-bottom: 1px solid #e5e5e5;
    }

    .co-exhibit--peaks .legend-item {
      display: flex;
      align-items: center;
      gap: 6px;
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 12px;
      color: #666;
    }

    .co-exhibit--peaks .legend-swatch {
      width: 16px;
      height: 2px;
      border-radius: 1px;
    }

    .co-exhibit--peaks .legend-swatch--ham {
      background: #2563eb;
    }

    .co-exhibit--peaks .legend-swatch--spam {
      background: #dc2626;
    }

    .co-exhibit--peaks .chart-footer {
      margin-top: 12px;
      font-family: 'IBM Plex Sans', sans-serif;
      font-size: 13px;
      color: #666;
      line-height: 1.6;
    }
  </style>

  <div class="chart-container">
    <div class="chart-header">
      <div class="chart-title">Twin Peaks</div>
      <div class="chart-label">Conceptual</div>
    </div>

    <div class="charts-row">
      <!-- LEFT: 2002 - Bimodal, separated -->
      <div class="chart-cell">
        <div class="chart-cell-title"><span>2002</span> — The canyon</div>
        <svg class="chart-svg" viewBox="0 0 280 164" preserveAspectRatio="xMidYMid meet">
          <!-- Axes -->
          <line class="axis-line" x1="36" y1="136" x2="260" y2="136"/>
          <line class="axis-line" x1="36" y1="8" x2="36" y2="136"/>
          <!-- Axis labels -->
          <text class="axis-label" x="36" y="150">0</text>
          <text class="axis-label" x="260" y="150" text-anchor="end">1</text>
          <text class="axis-label" x="148" y="162" text-anchor="middle">Token spam probability</text>
          <text class="axis-label" x="12" y="72" text-anchor="middle" transform="rotate(-90, 12, 72)">Frequency</text>

          <!-- Ham curve - fill then stroke -->
          <path class="ham-fill" d="M 36.0,131.7 L 40.5,127.3 L 45.0,120.0 L 49.4,108.9 L 53.9,93.5 L 58.4,74.6 L 62.9,54.3 L 67.4,35.8 L 71.8,22.7 L 76.3,18.0 L 80.8,22.7 L 85.3,35.8 L 89.8,54.3 L 94.2,74.6 L 98.7,93.5 L 103.2,108.9 L 107.7,120.0 L 112.2,127.3 L 116.6,131.7 L 121.1,134.0 L 125.6,135.2 L 130.1,135.7 L 134.6,136.0 L 260.0,136.0 L 260.0,136 L 36.0,136 Z"/>
          <path class="ham-stroke" d="M 36.0,131.7 L 40.5,127.3 L 45.0,120.0 L 49.4,108.9 L 53.9,93.5 L 58.4,74.6 L 62.9,54.3 L 67.4,35.8 L 71.8,22.7 L 76.3,18.0 L 80.8,22.7 L 85.3,35.8 L 89.8,54.3 L 94.2,74.6 L 98.7,93.5 L 103.2,108.9 L 107.7,120.0 L 112.2,127.3 L 116.6,131.7 L 121.1,134.0 L 125.6,135.2 L 130.1,135.7 L 134.6,136.0"/>

          <!-- Spam curve - fill then stroke -->
          <path class="spam-fill" d="M 36.0,136.0 L 161.4,135.9 L 165.9,135.7 L 170.4,135.2 L 174.9,134.0 L 179.4,131.7 L 183.8,127.3 L 188.3,120.0 L 192.8,108.9 L 197.3,93.5 L 201.8,74.6 L 206.2,54.3 L 210.7,35.8 L 215.2,22.7 L 219.7,18.0 L 224.2,22.7 L 228.6,35.8 L 233.1,54.3 L 237.6,74.6 L 242.1,93.5 L 246.6,108.9 L 251.0,120.0 L 255.5,127.3 L 260.0,131.7 L 260.0,136 L 36.0,136 Z"/>
          <path class="spam-stroke" d="M 161.4,135.9 L 165.9,135.7 L 170.4,135.2 L 174.9,134.0 L 179.4,131.7 L 183.8,127.3 L 188.3,120.0 L 192.8,108.9 L 197.3,93.5 L 201.8,74.6 L 206.2,54.3 L 210.7,35.8 L 215.2,22.7 L 219.7,18.0 L 224.2,22.7 L 228.6,35.8 L 233.1,54.3 L 237.6,74.6 L 242.1,93.5 L 246.6,108.9 L 251.0,120.0 L 255.5,127.3 L 260.0,131.7"/>

        </svg>
      </div>

      <!-- RIGHT: 2025 - Merged -->
      <div class="chart-cell">
        <div class="chart-cell-title"><span>2025</span> — The closing</div>
        <svg class="chart-svg" viewBox="0 0 280 164" preserveAspectRatio="xMidYMid meet">
          <!-- Axes -->
          <line class="axis-line" x1="36" y1="136" x2="260" y2="136"/>
          <line class="axis-line" x1="36" y1="8" x2="36" y2="136"/>
          <!-- Axis labels -->
          <text class="axis-label" x="36" y="150">0</text>
          <text class="axis-label" x="260" y="150" text-anchor="end">1</text>
          <text class="axis-label" x="148" y="162" text-anchor="middle">Token spam probability</text>
          <text class="axis-label" x="12" y="72" text-anchor="middle" transform="rotate(-90, 12, 72)">Frequency</text>

          <!-- Ham curve - fill then stroke -->
          <path class="ham-fill" d="M 36.0,133.3 L 40.5,132.2 L 45.0,130.8 L 49.4,129.0 L 53.9,126.6 L 58.4,123.7 L 62.9,120.0 L 67.4,115.7 L 71.8,110.5 L 76.3,104.5 L 80.8,97.7 L 85.3,90.2 L 89.8,82.0 L 94.2,73.3 L 98.7,64.4 L 103.2,55.5 L 107.7,46.9 L 112.2,38.9 L 116.6,31.9 L 121.1,26.0 L 125.6,21.6 L 130.1,18.9 L 134.6,18.0 L 139.0,18.9 L 143.5,21.6 L 148.0,26.0 L 152.5,31.9 L 157.0,38.9 L 161.4,46.9 L 165.9,55.5 L 170.4,64.4 L 174.9,73.3 L 179.4,82.0 L 183.8,90.2 L 188.3,97.7 L 192.8,104.5 L 197.3,110.5 L 201.8,115.7 L 206.2,120.0 L 210.7,123.7 L 215.2,126.6 L 219.7,129.0 L 224.2,130.8 L 228.6,132.2 L 233.1,133.3 L 237.6,134.1 L 242.1,134.7 L 246.6,135.1 L 251.0,135.4 L 255.5,135.6 L 260.0,135.7 L 260.0,136 L 36.0,136 Z"/>
          <path class="ham-stroke" d="M 36.0,133.3 L 40.5,132.2 L 45.0,130.8 L 49.4,129.0 L 53.9,126.6 L 58.4,123.7 L 62.9,120.0 L 67.4,115.7 L 71.8,110.5 L 76.3,104.5 L 80.8,97.7 L 85.3,90.2 L 89.8,82.0 L 94.2,73.3 L 98.7,64.4 L 103.2,55.5 L 107.7,46.9 L 112.2,38.9 L 116.6,31.9 L 121.1,26.0 L 125.6,21.6 L 130.1,18.9 L 134.6,18.0 L 139.0,18.9 L 143.5,21.6 L 148.0,26.0 L 152.5,31.9 L 157.0,38.9 L 161.4,46.9 L 165.9,55.5 L 170.4,64.4 L 174.9,73.3 L 179.4,82.0 L 183.8,90.2 L 188.3,97.7 L 192.8,104.5 L 197.3,110.5 L 201.8,115.7 L 206.2,120.0 L 210.7,123.7 L 215.2,126.6 L 219.7,129.0 L 224.2,130.8"/>

          <!-- Spam curve - fill then stroke -->
          <path class="spam-fill" d="M 36.0,135.4 L 40.5,135.1 L 45.0,134.7 L 49.4,134.1 L 53.9,133.3 L 58.4,132.2 L 62.9,130.8 L 67.4,129.0 L 71.8,126.6 L 76.3,123.7 L 80.8,120.0 L 85.3,115.7 L 89.8,110.5 L 94.2,104.5 L 98.7,97.7 L 103.2,90.2 L 107.7,82.0 L 112.2,73.3 L 116.6,64.4 L 121.1,55.5 L 125.6,46.9 L 130.1,38.9 L 134.6,31.9 L 139.0,26.0 L 143.5,21.6 L 148.0,18.9 L 152.5,18.0 L 157.0,18.9 L 161.4,21.6 L 165.9,26.0 L 170.4,31.9 L 174.9,38.9 L 179.4,46.9 L 183.8,55.5 L 188.3,64.4 L 192.8,73.3 L 197.3,82.0 L 201.8,90.2 L 206.2,97.7 L 210.7,104.5 L 215.2,110.5 L 219.7,115.7 L 224.2,120.0 L 228.6,123.7 L 233.1,126.6 L 237.6,129.0 L 242.1,130.8 L 246.6,132.2 L 251.0,133.3 L 255.5,134.1 L 260.0,134.7 L 260.0,136 L 36.0,136 Z"/>
          <path class="spam-stroke" d="M 67.4,129.0 L 71.8,126.6 L 76.3,123.7 L 80.8,120.0 L 85.3,115.7 L 89.8,110.5 L 94.2,104.5 L 98.7,97.7 L 103.2,90.2 L 107.7,82.0 L 112.2,73.3 L 116.6,64.4 L 121.1,55.5 L 125.6,46.9 L 130.1,38.9 L 134.6,31.9 L 139.0,26.0 L 143.5,21.6 L 148.0,18.9 L 152.5,18.0 L 157.0,18.9 L 161.4,21.6 L 165.9,26.0 L 170.4,31.9 L 174.9,38.9 L 179.4,46.9 L 183.8,55.5 L 188.3,64.4 L 192.8,73.3 L 197.3,82.0 L 201.8,90.2 L 206.2,97.7 L 210.7,104.5 L 215.2,110.5 L 219.7,115.7 L 224.2,120.0 L 228.6,123.7 L 233.1,126.6 L 237.6,129.0 L 242.1,130.8 L 246.6,132.2 L 251.0,133.3 L 255.5,134.1 L 260.0,134.7"/>
        </svg>
      </div>
    </div>

    <div class="legend">
      <div class="legend-item">
        <div class="legend-swatch legend-swatch--ham"></div>
        Ham
      </div>
      <div class="legend-item">
        <div class="legend-swatch legend-swatch--spam"></div>
        Spam
      </div>
    </div>

    <div class="chart-footer">
      In 2002, the token distributions of spam and ham occupied opposite ends of the probability space. Bayes' theorem exploited the canyon between them. Today, AI-generated text is collapsing the two peaks into one. The theorem still works. The separation it depends on doesn't.
    </div>
  </div>
</div>

Today, generative AI occupies the entire linguistic space of legitimacy. The two peaks have collapsed into one. If the defender filters aggressively enough to catch AI-generated outreach, it catches the real thing too. The canyon is closing.²¹

<!-- [EXHIBIT: Takeaways box] -->
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
      <li><strong>A Plan for Spam triggered the first AI war.</strong> Before anyone used the term, spam filters were doing machine learning: training on labeled data, making probabilistic predictions, fighting adversarial attacks at industrial scale. The vocabulary caught up twenty years later.</li>
      <li><strong>Ham is as powerful as spam.</strong> The filter's breakthrough was learning what <em>your</em> email looked like, not just what spam looked like. Your vocabulary became the shield.</li>
      <li><strong>Scale beat structure.</strong> Every structural advantage favored the attacker. Gmail won anyway — because spam was bulk, compute was monopolized, and the gap between junk and legitimate email was a canyon.</li>
      <li><strong>The canyon is closing.</strong> That victory depended on a vast gap between legitimate and illegitimate text. AI is erasing it. The win of 2004 was a truce.</li>
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

<p>¹ The "unlocked door" was a literal design choice. Sendmail, the era's dominant Mail Transfer Agent, prioritized the ARPANET's "trusted node" philosophy over security until Sendmail 8.9 (May 1998) finally disabled relaying by default. For the technical evolution of the "Open Relay" and the first retaliatory blocking efforts, see Paul Vixie, The Mail Abuse Prevention System (MAPS) and the RBL (1996). As Vixie famously noted, the internet had inherited the architecture of a small village but was being populated like a metropolis.

<p>² The $50 price point for ten million addresses was a staple of late-90s "Bulk Email" CD-ROMs, often advertised via the very spam they facilitated. These figures and the $50–$150 mortgage lead "bounties" are documented in FTC, "Report to Congress: National Do Not Email Registry" (2004). For a contemporary look at the "math of annoyance," see "The Economics of Spam," Salon (April 18, 2000), which illustrates how a near-zero marginal cost per send rendered traditional conversion constraints obsolete.

<p>³ U.S. v. Ralsky et al. (2009). The DOJ confirmed his operation netted roughly $3 million in a single quarter of 2005. The Detroit News profile that prompted the Slashdot retaliation was published in December 2002; Ralsky's complaints about the resulting deluge appeared in the Detroit Free Press shortly after.

<p>⁴ The "50% threshold" is sourced to the Brightmail "Spam Index" (June 2003). The broader trend—from 8% in 2001 to 36% in mid-2002—is aggregated in European Commission, COM(2004) 28 final, Section 1.1, and Pew Internet & American Life Project (June 2003). For the subsequent climb toward a 90% "noise floor" by 2007, see the Messaging Anti-Abuse Working Group (MAAWG), Email Metrics Reports. This period represents the "Great Clogging" of the internet, where infrastructure was nearly overwhelmed by its own lack of authentication.

<p>⁵ This specific scoring output—a common sight for system administrators in 2003—captured a German "livecam" porn campaign. The headers illustrate the transition from simple keyword checks to structural analysis, where the filter penalized the message more for its "encoding anomalies" (2.1 points) than its actual content. SpamAssassin, formalized by Justin Mason in 2001, effectively turned email defense into an "open-book exam" because its ruleset was public, allowing spammers to "score" their own messages and iterate until they hit a 4.9. See Justin Mason, "Filtering Spam with SpamAssassin," Proceedings of the USENIX Annual Technical Conference (2002). Image: Wikimedia Commons, "Reco spam.png," created 20 July 2003, Apache License 2.0.

<p>⁶ The shift to "V1agra" and "M0rtgage" was a direct response to the keyword-matching logic of early retail filters like McAfee SpamKiller. By 2003, the Federal Trade Commission noted in its Spam Forum reports that simple text-based filtering had become a "temporary palliative" easily bypassed by trivial misspellings. For an early taxonomy of these linguistic evasions, see John Graham-Cumming, The Spammer's Compendium (2004).

<p>⁷ Brightmail (acquired by Symantec in 2004) pioneered the use of "honeypots," maintaining a global network of over 2 million decoy addresses by 2003. While elegant, the fingerprinting method was defeated by "hash-busting": the practice of appending random, invisible strings of text to the end of a message. This ensured that every individual email in a million-message blast had a unique digital signature, rendering the central fingerprint database blind to the variation.

<p>⁸ Paul Graham, "A Plan for Spam," paulgraham.com (August 2002). The quotes in the main text are drawn directly from the essay, in which Graham describes both his addiction to the "competitive game" of hand-writing rules and his revulsion at the process. Graham's proposal grew out of a programming-language project (Arc) that led him to build a web-based email client, which needed a spam filter. Because Graham already commanded a significant following through essays like "Beating the Averages," the "Plan" functioned as an immediate call to action for the technical community and is widely credited with shifting the industry focus from blacklists and rules to statistical probability models.

<p>⁹ The Reverend Thomas Bayes (1702–1761) never published the theorem himself. It appeared posthumously in "An Essay towards solving a Problem in the Doctrine of Chances," published in <em>Philosophical Transactions of the Royal Society</em> in 1763, edited and submitted by his friend Richard Price. The formula in its modern notation: P(A|B) = P(B|A) × P(A) / P(B). In the spam context: P(spam|tokens) = P(tokens|spam) × P(spam) / P(tokens). If that notation is the reason you avoided statistics in college, the prose version in the main text is functionally equivalent.

<p>¹⁰ Tokenization—the process of splitting text into discrete units—was an established technique in information retrieval decades before its application to spam. The foundational work is attributed to Gerard Salton's Vector Space Model (1960s–70s) at Cornell, where documents were represented as vectors of term frequencies. Graham's specific innovation was applying this to personal email corpora, including non-word tokens like HTML fragments and punctuation. See Gerard Salton, Anita Wong, and C.S. Yang, "A Vector Space Model for Automatic Indexing," Communications of the ACM 18, no. 11 (1975).

<p>¹¹ In this context, "training" refers to supervised learning: a process where a human provides labeled data (spam vs. ham) for an algorithm to analyze. While "training" has since become a cornerstone of AI discourse, in the early 2000s it was a manual user action—typically dragging emails into folders or clicking a "Report Spam" button. Every such click in a modern inbox is a direct descendant of the supervised learning models popularized during this transition.

<p>¹² SpamAssassin 2.50 was a hybrid by design. The Bayesian engine did not replace the existing hand-written heuristics—it sat alongside them as an additional weighted score. A high Bayesian spam probability might contribute 3.5 points to a message's total, often enough on its own to push it past the default 5.0 threshold. The <code>sa-learn</code> command-line utility allowed system administrators to feed the Bayesian component with local mail corpora, meaning each server's model reflected the specific spam landscape of its user base. This hybrid architecture—rules for known patterns, statistics for unknown ones—became the dominant paradigm for server-side filtering through the mid-2000s. See the Apache SpamAssassin documentation and release notes for version 2.50 (March 2003).

<p>¹³ Image sourced from cybertopcops.com, "Thunderbird Junk Mail Training." Thunderbird's Adaptive Junk Mail Controls were based on a Bayesian classifier that required an initial training corpus of approximately 200 messages (100 ham, 100 spam) before reaching reliable accuracy. The design decision to place "Junk" and "Not Junk" buttons prominently in the toolbar was not incidental—it transformed a filtering mechanism into a feedback loop, making the act of classification visible and habitual for ordinary users. Thunderbird was, quietly, the first mass-market application that required its users to teach it before it could work.

<p>¹⁴ Microsoft's SmartScreen filter represented the first large-scale shift from local to centralized training. The Spam Confidence Level (SCL) scoring system rated each message on a 0–9 scale, with Exchange administrators able to set thresholds for delivery, junk folder routing, or outright rejection. The training corpus was built from the classifications of hundreds of thousands of volunteers in Microsoft's Feedback Loop program. This approach—aggregating human judgments at platform scale to train a single shared model—prefigured the architecture Gmail would deploy the following year at vastly greater scale. See Microsoft, "SmartScreen Technology in Outlook 2003," Microsoft TechNet (2003).

<p>¹⁵ Bayesian poisoning, also known as "word salad" or "hash-busting text," became widespread by late 2003. The technique exploited the statistical symmetry at the heart of Graham's design: if the filter weighted ham tokens as heavily as spam tokens, then injecting enough ham tokens could neutralize the spam signal. Common sources for filler text included Project Gutenberg novels, news wire feeds, and random excerpts from Wikipedia. Graham himself addressed the attack in a follow-up essay, "Better Bayesian Filtering" (January 2003), proposing refinements including more aggressive token selection and devaluation of long, context-free text blocks appended to messages. The arms race had begun within months of the original essay's publication.

<p>¹⁶ When Gmail launched on April 1, 2004, its one gigabyte of free storage was roughly 500 times what Hotmail offered. The storage also meant users kept more email for longer, generating a richer ham corpus for the Bayesian models to train on. More legitimate email in the archive meant a more detailed statistical portrait of each user's communication patterns, which made the personalized filter more accurate. The generosity of the storage and the quality of the filter were not separate features. They reinforced each other. See Gmail launch announcement, Google Blog (April 1, 2004); for the competitive context, see Steven Levy, <em>In the Plex: How Google Thinks, Works, and Shapes Our Lives</em> (Simon & Schuster, 2011).

<p>¹⁷ Barracuda Networks, analyzing over one billion daily email messages across 50,000 customers worldwide, estimated that 90–95% of all email sent in 2007 was spam. MAAWG's concurrent estimate, based on over 100 million mailboxes, placed "abusive email" at 85% of incoming traffic. See MAAWG Email Metrics Reports (2007).

<p>¹⁸ The text front was not entirely dormant during this period. Gmail introduced Priority Inbox in 2010, a second model trained not on the difference between spam and ham but on which legitimate emails a user was most likely to care about — who they replied to fastest, which threads they opened immediately. This and similar refinements represented the defense getting smarter within a won position, not responding to a renewed offensive.

<p>¹⁹ OpenAI released ChatGPT in November 2022 and GPT-4 in March 2023. Open-source language models capable of generating personalized outreach at scale proliferated through that year, and the sales and marketing tooling to operationalize them — integrations with CRMs, sequencing platforms, and sending infrastructure — matured through 2024. The "reopening" was not a single event but a gradual capability crossing a threshold: the moment the cost of producing a unique, linguistically legitimate message dropped to near zero.

<p>²⁰ In cybersecurity, a zero-day is a vulnerability that is unknown to the defender and therefore has no existing patch or signature. A "semantic zero-day" here means a message that has never been seen before and shares no linguistic pattern with any previously flagged message, rendering pattern-based detection useless.

<p>²¹ The mathematical structure of the "canyon" is a shift in probability distributions. In 2002, the distribution of token probabilities across spam and ham was bimodal: two distinct peaks with a wide valley between them. Bayes' theorem could exploit this easily because the prior probability of a token like "Ahab" appearing in spam was nearly zero — P(Ahab|Spam) ≈ 0 — so even if the rest of the message looked suspicious, that single token anchored the classification. Today, the distribution is collapsing toward a single peak. A language model can generate a perfectly context-aware email about "Ahab" to a maritime historian, and the P(Ahab|Spam) value is no longer a reliable anchor. The theorem still works. The separation it depends on doesn't.

</div>