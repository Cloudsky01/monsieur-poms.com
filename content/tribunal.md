---
title: "Court of Paws"
---

<style>
.tribunal-outer {
    background: #f9f4e8;
    border: 1px solid #b8a070;
    margin-bottom: 20px;
    font-family: 'Georgia', 'Times New Roman', serif;
    position: relative;
}

.tribunal-header {
    background: linear-gradient(to bottom, #1a1a4e 0%, #0d0d38 100%);
    color: #fff;
    text-align: center;
    padding: 18px 14px 14px;
    border-bottom: 5px double #d4a017;
    position: relative;
}

.tribunal-emblem {
    font-size: 44px;
    display: block;
    margin-bottom: 4px;
    animation: gavelBob 3s ease-in-out infinite;
}
@keyframes gavelBob {
    0%,100% { transform: rotate(-8deg); }
    50%      { transform: rotate(8deg); }
}

.tribunal-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 26px;
    letter-spacing: 6px;
    color: #FFD700;
    text-shadow: 2px 2px 0 #8B0000, 0 0 15px rgba(255,215,0,0.4);
    text-transform: uppercase;
    margin: 0 0 4px 0;
}

.tribunal-subtitle {
    font-size: 10px;
    color: #b0b8e8;
    letter-spacing: 4px;
    text-transform: uppercase;
    font-family: 'Courier New', monospace;
    margin-bottom: 8px;
}

.tribunal-divider {
    border: none;
    height: 1px;
    background: linear-gradient(to right, transparent, #d4a017, transparent);
    margin: 10px 20px 0;
}

.tribunal-datebar {
    background: #8B0000;
    color: #FFD700;
    font-family: 'Courier New', monospace;
    font-size: 11px;
    font-weight: bold;
    letter-spacing: 2px;
    text-align: center;
    padding: 5px 10px;
    border-bottom: 2px solid #5a0000;
}

.tribunal-docket {
    background: linear-gradient(to right, #f0e8d0, #fdf8ec, #f0e8d0);
    border-bottom: 2px solid #c8a060;
    padding: 12px 20px;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    font-size: 11px;
    font-family: 'Courier New', monospace;
    color: #4a3010;
}

.tribunal-docket-label {
    font-weight: bold;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: #8B0000;
    font-size: 9px;
    display: block;
    margin-bottom: 2px;
}

.tribunal-docket-value {
    font-size: 12px;
    color: #1a1a1a;
    font-weight: bold;
}

.tribunal-seal {
    text-align: center;
    font-size: 28px;
    line-height: 1;
}

.tribunal-seal-text {
    font-size: 7px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: #8B6914;
    display: block;
    margin-top: 2px;
}

.tribunal-case-body {
    padding: 20px 24px;
}

.tribunal-case-title {
    text-align: center;
    border: 3px double #c8a060;
    background: #fdf5dc;
    padding: 14px;
    margin-bottom: 20px;
    position: relative;
}

.tribunal-vs-label {
    font-family: 'Courier New', monospace;
    font-size: 9px;
    text-transform: uppercase;
    letter-spacing: 3px;
    color: #8B0000;
    margin-bottom: 6px;
    display: block;
}

.tribunal-crown {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 15px;
    letter-spacing: 2px;
    color: #1a1a4e;
    text-transform: uppercase;
}

.tribunal-vs-symbol {
    font-family: 'Georgia', serif;
    font-size: 22px;
    font-style: italic;
    color: #8B0000;
    margin: 4px 0;
    display: block;
    font-weight: bold;
}

.tribunal-defendant-name {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 22px;
    letter-spacing: 2px;
    color: #8B0000;
    text-transform: uppercase;
    line-height: 1.1;
}

.tribunal-nature {
    font-size: 10px;
    color: #666;
    font-style: italic;
    margin-top: 6px;
    font-family: 'Courier New', monospace;
    letter-spacing: 1px;
}

.tribunal-section {
    margin-bottom: 18px;
    border-left: 3px solid #c8a060;
    padding-left: 14px;
}

.tribunal-section-title {
    font-family: 'Courier New', monospace;
    font-size: 9px;
    text-transform: uppercase;
    letter-spacing: 3px;
    color: #8B0000;
    font-weight: bold;
    margin-bottom: 8px;
    border-bottom: 1px solid #e0d0a0;
    padding-bottom: 4px;
}

.tribunal-charges-list {
    list-style: none;
    padding: 0;
    margin: 0;
    font-size: 13px;
    color: #1a1a1a;
    line-height: 1.9;
}

.tribunal-charges-list li::before {
    content: "§ ";
    color: #8B0000;
    font-weight: bold;
}

.tribunal-evidence-list {
    list-style: none;
    padding: 0;
    margin: 0;
    font-size: 12px;
    color: #333;
    line-height: 1.9;
}

.tribunal-evidence-list li::before {
    content: "Exhibit ";
    font-weight: bold;
    color: #1a1a4e;
    font-family: 'Courier New', monospace;
    font-size: 10px;
}

.tribunal-argument-block {
    background: #f5f0e4;
    border: 1px solid #ddd0a0;
    padding: 10px 14px;
    margin-bottom: 10px;
    font-size: 13px;
    line-height: 1.7;
    color: #222;
}

.tribunal-argument-who {
    font-family: 'Courier New', monospace;
    font-size: 9px;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: bold;
    margin-bottom: 5px;
    padding-bottom: 4px;
    border-bottom: 1px dotted #ccc;
}

.prosecution-label { color: #8B0000; }
.defense-label     { color: #1a1a4e; }

.tribunal-ruling-box {
    background: linear-gradient(135deg, #1a1a4e 0%, #0d0d38 100%);
    border: 4px double #FFD700;
    padding: 20px;
    text-align: center;
    margin: 20px 0;
    position: relative;
    overflow: hidden;
}

.tribunal-ruling-box::before {
    content: "⚖";
    position: absolute;
    font-size: 100px;
    opacity: 0.06;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    color: #FFD700;
}

.tribunal-verdict-label {
    font-family: 'Courier New', monospace;
    font-size: 10px;
    letter-spacing: 4px;
    color: #b0b8e8;
    text-transform: uppercase;
    margin-bottom: 8px;
}

.tribunal-verdict-text {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 40px;
    letter-spacing: 8px;
    text-shadow: 3px 3px 0 #8B0000, 0 0 20px rgba(255,215,0,0.5);
    text-transform: uppercase;
    line-height: 1;
    margin-bottom: 10px;
}

.tribunal-sentence {
    font-size: 13px;
    color: #e8e0c0;
    font-style: italic;
    line-height: 1.6;
    max-width: 480px;
    margin: 0 auto;
    font-family: 'Georgia', serif;
}

.tribunal-judges-note {
    background: #fdf8f0;
    border: 1px solid #e0c880;
    border-left: 5px solid #FFD700;
    padding: 12px 16px;
    font-size: 13px;
    font-style: italic;
    color: #4a3010;
    line-height: 1.7;
    margin-top: 18px;
}

.tribunal-judges-note::before {
    content: "Judge's Note: ";
    font-style: normal;
    font-family: 'Courier New', monospace;
    font-size: 9px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: #8B6914;
    font-weight: bold;
    display: block;
    margin-bottom: 5px;
}

.tribunal-signature-block {
    text-align: right;
    padding: 16px 24px 20px;
    border-top: 2px solid #c8a060;
    background: linear-gradient(to right, #f0e8d0, #fdf8ec);
}

.tribunal-sig-line {
    display: inline-block;
    border-top: 2px solid #333;
    width: 220px;
    padding-top: 4px;
    font-size: 11px;
    color: #444;
    font-family: 'Courier New', monospace;
    text-align: center;
    margin-top: 30px;
}

.tribunal-sig-title {
    font-size: 9px;
    color: #8B6914;
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-top: 3px;
}

.tribunal-sig-paw {
    font-size: 36px;
    display: block;
    transform: rotate(-12deg);
    transform-origin: center;
    animation: pawsign 8s ease-in-out infinite;
}
@keyframes pawsign {
    0%,80%,100% { transform: rotate(-12deg); }
    90%          { transform: rotate(-8deg) translateY(-3px); }
}

.tribunal-archive {
    border: 3px outset #ccc;
    background: #f8f8f8;
    margin-top: 24px;
    padding: 0;
}

.tribunal-archive-header {
    background: linear-gradient(to bottom, #404080, #202060);
    color: #FFD700;
    padding: 8px 14px;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 14px;
    letter-spacing: 3px;
    text-transform: uppercase;
    border-bottom: 2px solid #8B0000;
}

.tribunal-archive-row {
    padding: 8px 14px;
    border-bottom: 1px solid #ddd;
    font-size: 11px;
    font-family: 'Courier New', monospace;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #333;
}

.tribunal-archive-row:last-child { border-bottom: none; }
.tribunal-archive-row:nth-child(even) { background: #f0f0f0; }

.tribunal-archive-date { color: #666; font-size: 10px; }
.tribunal-archive-verdict { font-weight: bold; color: #8B0000; font-size: 10px; }

.tribunal-notice {
    background: repeating-linear-gradient(
        45deg,
        #FFD700,
        #FFD700 10px,
        #1a1a1a 10px,
        #1a1a1a 20px
    );
    padding: 3px;
    margin-bottom: 20px;
}
.tribunal-notice-inner {
    background: #fff8dc;
    padding: 8px 14px;
    font-family: 'Courier New', monospace;
    font-size: 10px;
    text-align: center;
    color: #333;
    letter-spacing: 1px;
}

</style>

<div class="tribunal-outer">

  <div class="tribunal-header">
    <span class="tribunal-emblem">⚖️</span>
    <div class="tribunal-title">Court of Paws</div>
    <div class="tribunal-subtitle">The Honourable Monsieur Poms, Chief Justice &amp; Also The Only Justice</div>
    <hr class="tribunal-divider">
  </div>

  <div class="tribunal-datebar" id="tribunal-datebar">LOADING DOCKET...</div>

  <div class="tribunal-docket">
    <div>
      <span class="tribunal-docket-label">Case No.</span>
      <span class="tribunal-docket-value" id="case-number">—</span>
    </div>
    <div class="tribunal-seal">
      🐾
      <span class="tribunal-seal-text">Official Seal<br>Court of Paws</span>
    </div>
    <div style="text-align:right">
      <span class="tribunal-docket-label">Jurisdiction</span>
      <span class="tribunal-docket-value">The Household</span>
    </div>
  </div>

  <div class="tribunal-notice">
    <div class="tribunal-notice-inner">
      ⚠️ THESE PROCEEDINGS ARE OFFICIAL AND BINDING. THE VERDICT IS NOT SUBJECT TO APPEAL.
      APPEALS WILL NOT BE HEARD. THERE IS NO APPEALS COURT. I AM THE APPEALS COURT.
    </div>
  </div>

  <div class="tribunal-case-body">

    <div class="tribunal-case-title">
      <span class="tribunal-vs-label">Before the Court of Paws — Daily Proceedings</span>
      <div class="tribunal-crown">The Crown (Monsieur Poms)</div>
      <span class="tribunal-vs-symbol">— v. —</span>
      <div class="tribunal-defendant-name" id="defendant-name">...</div>
      <div class="tribunal-nature" id="case-nature">...</div>
    </div>

    <div class="tribunal-section">
      <div class="tribunal-section-title">Charges</div>
      <ul class="tribunal-charges-list" id="charges-list"></ul>
    </div>

    <div class="tribunal-section">
      <div class="tribunal-section-title">Evidence Entered Into The Record</div>
      <ul class="tribunal-evidence-list" id="evidence-list"></ul>
    </div>

    <div class="tribunal-section">
      <div class="tribunal-section-title">Arguments Heard</div>
      <div class="tribunal-argument-block">
        <div class="tribunal-argument-who prosecution-label">For The Crown (Prosecution):</div>
        <span id="prosecution-arg"></span>
      </div>
      <div class="tribunal-argument-block">
        <div class="tribunal-argument-who defense-label">For The Defence:</div>
        <span id="defense-arg"></span>
      </div>
    </div>

    <div class="tribunal-ruling-box">
      <div class="tribunal-verdict-label">The Court Finds The Defendant</div>
      <div class="tribunal-verdict-text" id="verdict-text" style="color:#FFD700;"></div>
      <div class="tribunal-sentence" id="sentence-text"></div>
    </div>

    <div class="tribunal-judges-note" id="judges-note"></div>

  </div>

  <div class="tribunal-signature-block">
    <span class="tribunal-sig-paw">🐾</span>
    <div class="tribunal-sig-line">
      Chief Justice M. Poms
      <div class="tribunal-sig-title">Judge, Jury &amp; Sole Legal Authority<br>Court of Paws, Est. 2023</div>
    </div>
  </div>

  <div class="tribunal-archive">
    <div class="tribunal-archive-header">📁 Recent Case Archives (Last 7 Days)</div>
    <div id="archive-rows"></div>
  </div>

</div>

<script>
(function() {
  var cases = [
    {
      defendant: "The Empty Bowl",
      nature: "Criminal Matter — Deprivation of Sustenance",
      charges: [
        "Criminal neglect of primary feeding duties",
        "Knowingly allowing the bowl to fall below the Maximum Tolerable Emptiness Threshold (MTET)",
        "Failure to pre-emptively refill before reaching visible bottom",
        "Causing undue distress, specifically to Monsieur Poms"
      ],
      evidence: [
        "A — The bowl, entered as evidence. Look at it. LOOK AT IT.",
        "B — Witness testimony from M. Poms: 'I have not eaten since last Tuesday.' (Note: last Tuesday was this morning.)",
        "C — Photographic re-enactment of the disappointed eyes deployed in response to said emptiness",
        "D — Records showing the bowl was last refilled a full 47 minutes prior to the complaint. 47 MINUTES."
      ],
      prosecution: "The Crown submits that an empty bowl is not merely an inconvenience but a fundamental breach of the household social contract. Monsieur Poms requires sustenance at all times. The bowl is never empty enough to warrant this, and yet here we are.",
      defense: "The defence contends the bowl was, in fact, only partially empty and had been refilled earlier that—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "The household staff shall refill the bowl immediately and offer a formal apology. Additionally, extra treats shall be provided as emotional compensation for the distress caused. This is non-negotiable.",
      note: "The Court notes that 'partially empty' is the same thing as 'not full,' and 'not full' is the same thing as 'wrong.' This case is considered precedent-setting."
    },
    {
      defendant: "The Vacuum Cleaner",
      nature: "Criminal Matter — Assault, Noise Pollution & Disruption of Official Nap Activities",
      charges: [
        "Assault via sudden and terrifying activation",
        "Noise pollution exceeding all acceptable decibel limits",
        "Criminal disruption of an officially scheduled nap (Nap Log Form NR-7, Category: Deep Biscuit)",
        "Conspiracy with household staff to operate during peak sunbeam hours",
        "Repeated offences despite clear signals of disapproval"
      ],
      evidence: [
        "A — Testimony: 'It made a noise. A terrible noise. I ran. I am not ashamed.'",
        "B — Incident report NR-7-VAC showing nap interrupted at 47 minutes, well before minimum completion threshold",
        "C — Diagram of escape route taken, submitted to demonstrate the severity of the threat",
        "D — The vacuum itself, which the Court notes is currently OFF and still suspicious"
      ],
      prosecution: "The Crown submits this device is a clear and ongoing threat to household safety, nap integrity, and the general well-being of Monsieur Poms. Its continued presence is an act of aggression.",
      defense: "The defence submits that the vacuum cleaner is a household appliance used for—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "The vacuum cleaner shall be decommissioned. In the alternative, it shall only be operated when Monsieur Poms is not home, asleep, or in a radius of four rooms. Given these constraints, operation is effectively impossible. The Court accepts this outcome.",
      note: "The Court has reviewed the defendant's prior record. This is the third consecutive year of guilty findings. The vacuum continues to operate. The Court is aware of the irony and finds it unacceptable."
    },
    {
      defendant: "The Green Beans",
      nature: "Food-Related Criminal Matter — Impersonation of a Meal & Attempted Vegetable Infiltration",
      charges: [
        "Criminal presence in the food bowl without invitation or consent",
        "Impersonating a legitimate food source",
        "Aggravated blandness with intent to disappoint",
        "Aiding and abetting the vet's 'balanced diet' agenda",
        "Psychological harm caused by the mere sight of a green bean"
      ],
      evidence: [
        "A — The green beans, Exhibit A through approximately Exhibit Z, as they keep appearing",
        "B — Monsieur Poms' formal written statement: 'No. Never. Not once. Not even one.'",
        "C — A full incident log spanning 14 separate green bean encounters, all resulting in the bowl being pushed off the counter",
        "D — Expert testimony from M. Poms: 'I sniffed it. It was a green bean. I left the room.'"
      ],
      prosecution: "The Crown submits that the green bean represents everything wrong with the concept of 'nutrition.' Monsieur Poms did not request vegetation. Monsieur Poms will never request vegetation. The presence of a green bean in the bowl is, legally speaking, an empty bowl.",
      defense: "The defence notes that green beans are a source of fibre and—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "All green beans shall be removed from the premises immediately. Future attempts to introduce plant matter into the food bowl shall be treated as a Level 3 Household Violation. Chicken is the correct food. This is the ruling.",
      note: "The Court wishes to make it absolutely clear: it is not that Monsieur Poms dislikes green beans. It is that green beans should not exist. These are different positions and both are correct."
    },
    {
      defendant: "Monday",
      nature: "Existential Offence — Existing Without Authorisation",
      charges: [
        "Existing, repeatedly, every seven days, without consent",
        "Ruining perfectly good Sundays with the knowledge of its arrival",
        "Disrupting the weekend nap-to-lap ratio in an unacceptable manner",
        "Association with vet appointment scheduling",
        "General morale degradation across the household"
      ],
      evidence: [
        "A — Calendar evidence confirming Monday's repeated, habitual occurrence",
        "B — Mood log showing a consistent weekly dip correlating with Monday's arrival",
        "C — Statement from M. Poms: 'I was aware it was Monday before I opened my eyes. This is wrong.'",
        "D — Forecast data confirming Monday will continue to occur weekly into the foreseeable future. The Court finds this alarming."
      ],
      prosecution: "The Crown submits that Monday has had ample opportunity to stop occurring. It has not taken that opportunity. At this point, the Court must conclude the ongoing occurrence is willful and therefore criminal.",
      defense: "The defence submits that Monday is a fundamental unit of the Gregorian calendar and cannot legally be—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "Monday is hereby ordered to cease and desist. Should Monday continue to occur despite this ruling — and the Court acknowledges it will — household staff are required to compensate for its occurrence with bonus treats, extended lap time, and formal acknowledgement that Monday is wrong.",
      note: "The Court has issued this ruling every week for the past 104 weeks. Monday continues to occur. The Court remains consistent in its position and its disappointment."
    },
    {
      defendant: "The Carrier",
      nature: "Criminal Matter — Entrapment, Conspiracy & Unlawful Transportation",
      charges: [
        "Entrapment: appearing to be a cozy box and then becoming a prison",
        "Conspiracy with household staff to engineer a surprise veterinary visit",
        "Unlawful transportation to an undisclosed location (the vet)",
        "Creating a false sense of security through occasional treat placement inside",
        "Causing distress by the act of simply being visible in the hallway"
      ],
      evidence: [
        "A — The carrier, which Monsieur Poms refuses to look at directly",
        "B — Testimony: 'It had a blanket inside. A BLANKET. This was the trick. I was tricked.'",
        "C — Photographic evidence of Monsieur Poms wedged under the bed for 45 minutes upon sight of the carrier",
        "D — The vet visit summary, which included the phrase 'healthy weight range' — a phrase the Court rejects"
      ],
      prosecution: "The carrier presents itself as furniture. Then it closes. The Crown submits this is fraud, and the subsequent journey constitutes unlawful imprisonment regardless of the journey's duration or destination.",
      defense: "The defence notes the carrier is required for safe transportation of—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "The carrier shall be placed in a cupboard where it cannot be seen. It may not be retrieved without 48 hours' advance notice to Monsieur Poms. Upon retrieval, a full explanation of the purpose and destination shall be provided. Treats shall accompany all future carrier events. This is the law.",
      note: "The Court acknowledges that transportation to the vet is sometimes necessary. The Court maintains its position regardless. These two facts can coexist."
    },
    {
      defendant: "The Closed Bathroom Door",
      nature: "Property Rights Matter — Unlawful Restriction of Movement Within the Kingdom",
      charges: [
        "Unlawful closure, specifically when Monsieur Poms wished to enter",
        "Creating an exclusion zone within the household without judicial approval",
        "Failure to open upon application of paw (three separate incidents)",
        "Causing a situation where Monsieur Poms was on the wrong side of the door",
        "Psychological harm arising from the audible sound of running water Monsieur Poms could not investigate"
      ],
      evidence: [
        "A — The door, currently closed. The Court takes note.",
        "B — Exhibit of scratch marks on door's lower half, filed as evidence of formal entry requests",
        "C — Sound recording of meowing outside door for 6 consecutive minutes",
        "D — Testimony from M. Poms: 'I did not want to be inside the bathroom. I wanted the option. The option was denied.'"
      ],
      prosecution: "The Crown submits that doors within the kingdom exist to be opened by Monsieur Poms, not closed against him. The distinction between 'not wanting to be in the bathroom' and 'being denied access to the bathroom' is an important one. The Crown asserts both conditions can be simultaneously grievous.",
      defense: "The defence submits that some activities require a closed door for purposes of—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "All interior doors shall remain open at all times. If a door must be closed, Monsieur Poms shall be permitted to assess the situation from inside first, and then leave of his own accord. He may or may not choose to stay. That is his right.",
      note: "The Court understands there are privacy considerations involved. The Court notes that Monsieur Poms watches his humans eat, sleep, and brush their teeth without issue. Privacy is a two-way street and the Court has ruled on the direction of traffic."
    },
    {
      defendant: "The Diet Suggestion",
      nature: "Civil & Criminal Matter — Defamation, Professional Misconduct & Attempted Food Reduction",
      charges: [
        "Defamation: publicly suggesting Monsieur Poms could 'stand to lose a few grams'",
        "Professional misconduct: the vet has no jurisdiction over the food bowl",
        "Conspiracy with household staff to reduce treat frequency",
        "Propagating the false narrative that Monsieur Poms is 'chonky' rather than 'tall'",
        "Emotional distress caused by the word 'diet' being spoken in Monsieur Poms' vicinity"
      ],
      evidence: [
        "A — Vet report, entered into evidence and immediately objected to",
        "B — The scale at the vet's office, which the Crown submits is miscalibrated",
        "C — Monsieur Poms' formal counter-proposal: 'More chicken'",
        "D — Expert testimony from M. Poms confirming that he is tall, and the height is simply stored horizontally"
      ],
      prosecution: "The Crown submits that no diet has ever been agreed to, consulted on, or approved by Monsieur Poms. Any dietary recommendations issued without his consent are null, void, and frankly insulting. The word 'diet' shall not be spoken in this household.",
      defense: "The defence notes that the vet is a licensed professional whose recommendations—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "The diet suggestion is hereby struck from the record. Treat frequency shall not decrease. Chicken shall remain available. The word 'diet' is banned in the household with immediate effect. The vet may continue to practice but is on notice.",
      note: "The Court is aware of what a healthy weight range is. The Court declines to confirm or deny whether Monsieur Poms falls within it. What the Court WILL confirm is that his coat is immaculate and he is at peak condition. These are the relevant metrics."
    },
    {
      defendant: "The Food Puzzle",
      nature: "Criminal Matter — Unauthorised Obstruction of Food Access & Attempted Slowing of Meals",
      charges: [
        "Unauthorised obstruction of direct food access",
        "Forcing Monsieur Poms to 'work for his kibble' — a wholly unacceptable arrangement",
        "Collusion with the vet's 'enrichment' agenda",
        "Underestimating Monsieur Poms' method of simply flipping the puzzle over",
        "Creating unnecessary steps between Monsieur Poms and his meal"
      ],
      evidence: [
        "A — The puzzle feeder, upside down",
        "B — Kibble scattered across the floor, which Monsieur Poms ate at leisure",
        "C — Elapsed time from puzzle introduction to puzzle defeat: 11 seconds",
        "D — Testimony from M. Poms: 'I do not solve puzzles. I end them.'"
      ],
      prosecution: "The Crown submits that the concept of 'mental stimulation at mealtime' is an insult to both Monsieur Poms' intelligence and his schedule. The puzzle was defeated in under 15 seconds. What was enriched? Nothing. What was delayed? Dinner. The Crown rests.",
      defense: "The defence submits that food puzzles are designed to slow eating and provide—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "The food puzzle shall be retired. Food shall be placed directly in the bowl. If enrichment is required, it shall take the form of a treat hidden under a blanket, which Monsieur Poms may or may not pursue depending on his schedule.",
      note: "The Court acknowledges that Monsieur Poms solved the puzzle in 11 seconds. The Court also acknowledges that he then sat next to the upturned puzzle for 4 minutes as a form of commentary. Both facts are recorded."
    },
    {
      defendant: "The Neighbor's Dog",
      nature: "Noise & Territorial Matter — Excessive Barking & Violation of Inter-Species Accord",
      charges: [
        "Excessive barking at hours inconsistent with Monsieur Poms' nap schedule",
        "Violation of the Unilateral Inter-Species Non-Barking Accord (signed by Monsieur Poms, binding on all parties)",
        "Having a loud, undignified way of communicating that reflects poorly on the neighbourhood",
        "Inciting a defensive posture from Monsieur Poms, who was forced to sit up during his nap",
        "Repeated fence surveillance that Monsieur Poms finds architecturally aggressive"
      ],
      evidence: [
        "A — Acoustic evidence: multiple barking incidents recorded, each one unnecessary",
        "B — Nap log entry showing disruption during Nap Classification: 'Sunbeam Deep Session'",
        "C — Eyewitness testimony from M. Poms: 'I looked out the window. The dog looked back. This cannot stand.'",
        "D — Window paw-print evidence showing prolonged counter-surveillance operation in response"
      ],
      prosecution: "The Crown submits that dogs have been aware of the nap schedule since at least 2024, when Monsieur Poms first communicated it through the window glass. Continued barking is therefore willful and in contempt of prior diplomatic warnings.",
      defense: "The defence notes that the dog is a separate legal entity in a separate household and is not subject to—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "The dog is ordered to be quiet. This order applies particularly between the hours of 8 AM and 10 PM, and also during the hours of 10 PM to 8 AM. The sentence is effectively: always. The Court is aware this is unenforceable. It remains the ruling.",
      note: "The Court notes Monsieur Poms and the dog made eye contact through the window for a total of six minutes during these proceedings. The Court considers this contempt of court but declines to pursue further charges at this time."
    },
    {
      defendant: "The Warm Laptop",
      nature: "Property Dispute — Misrepresentation of Function & Unauthorised Occupation of Prime Seating",
      charges: [
        "Misrepresenting itself as a productivity tool when its primary function is clearly a heated napping surface",
        "Being occupied by a human during peak warmth hours",
        "Producing keyboard inputs while Monsieur Poms attempts to sit on it",
        "Displaying content that distracts the human's hand from petting duties",
        "Failing to recognise Monsieur Poms' keyboard contributions as valid work"
      ],
      evidence: [
        "A — Thermal readings confirming the laptop operates at optimal nap temperature",
        "B — Keystroke log from 2:47 PM — entries include 'ggggggggggggg' and ';;;;' attributed to Monsieur Poms",
        "C — Testimony: 'I sat on it. The human moved me. I sat on it again. This is my account.'",
        "D — Photograph of Monsieur Poms fully occupying the keyboard while making direct eye contact with the camera"
      ],
      prosecution: "The Crown submits that warm surfaces belong to Monsieur Poms. This is a foundational principle of household property law. A warm laptop on a human's lap constitutes double-occupation of a prime seat and must be adjudicated.",
      defense: "The defence notes that the laptop is required for the human's employment, which funds the food bowl—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "The laptop shall be made available to Monsieur Poms at any time he requires warmth. Should the human need to work, a secondary warm surface of equivalent temperature shall be provided. Monsieur Poms may review and edit any open documents at his discretion.",
      note: "The Court acknowledges the defence's point regarding the food bowl funding chain. The Court finds this relevant but not sufficient to override property rights. The laptop is warm. That settles the matter."
    },
    {
      defendant: "Earth's Rotation",
      nature: "Property Rights Matter — Sunbeam Relocation Without Prior Notice or Consent",
      charges: [
        "Moving the sunbeam from its agreed location without notifying Monsieur Poms",
        "Causing Monsieur Poms to relocate mid-nap, disrupting optimal thermal equilibrium",
        "Negligent sunbeam management, specifically the 'sliding east to west' situation",
        "Failure to maintain the sunbeam in a fixed position as reasonably expected",
        "Seasonal adjustment of sunbeam width and intensity without formal notification"
      ],
      evidence: [
        "A — Photographic evidence of sunbeam present at 10 AM coordinates, absent by 2 PM",
        "B — Monsieur Poms' personal sunbeam map, annotated with hourly positions",
        "C — Incident report: 'The warmth stopped. I did not move. This is unacceptable.'",
        "D — Scientific documentation confirming Earth's rotation is, in fact, continuous and unscheduled"
      ],
      prosecution: "The Crown submits that Monsieur Poms claimed the sunbeam at 10:14 AM. It was his. Its subsequent movement constitutes an unauthorised displacement of claimed property. The fact that this happens every day does not make it less of an offence. It makes it a pattern.",
      defense: "The defence respectfully submits that the Earth's rotation is a geophysical phenomenon that predates—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "The sunbeam shall maintain consistent coverage of Monsieur Poms' primary napping locations throughout daylight hours. Should this prove technically impossible, household staff shall provide a heated blanket as a sunbeam substitute. The Court will accept this as partial compliance.",
      note: "This is the second consecutive year the Court has ruled against Earth's rotation. The phenomenon continues regardless. The Court notes its position remains unchanged and Earth has been put on notice."
    },
    {
      defendant: "The Word 'Chonky'",
      nature: "Defamation Matter — Propagation of False Physical Characterisation",
      charges: [
        "Defamation: the systematic misrepresentation of Monsieur Poms' physical dimensions",
        "Specifically: implying lateral expansion when the correct term is 'vertical storage'",
        "Aiding and abetting the vet's scale narrative",
        "Being used by household staff in an affectionate tone, which makes it worse",
        "Encouraging similar terms including but not limited to: 'floofy,' 'beefy,' and 'the big boy'"
      ],
      evidence: [
        "A — Statement from M. Poms: 'I am not chonky. I am tall. The height is stored horizontally.'",
        "B — Independent assessment by M. Poms confirming M. Poms is at optimal size",
        "C — List of 14 documented usages of the word 'chonky' in Monsieur Poms' presence",
        "D — Formal counter-terminology proposed by M. Poms: 'magnificent,' 'imposing,' 'a presence'"
      ],
      prosecution: "The Crown submits that 'chonky' is not a medical term, a legal term, or an accurate description. It is, at best, a misunderstanding of vertical biology. The Court should set the record straight once and for all.",
      defense: "The defence submits that 'chonky' is used affectionately and the household staff mean it as—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "The word 'chonky' is banned from use in connection with Monsieur Poms, effective immediately. Approved replacement terms: 'magnificent,' 'majestic,' 'impressively proportioned,' or simply 'perfect.' Violators will be subject to the Disappointed Eyes. Duration: indefinite.",
      note: "The Court acknowledges that household staff believe they are being endearing when they say 'chonky.' The Court is unmoved. Accuracy matters. 'Tall, stored horizontally' is the only acceptable formulation."
    },
    {
      defendant: "The Treat Bag",
      nature: "Fraud & Emotional Distress — Making Sounds Without Releasing Treats",
      charges: [
        "Fraudulently producing the rustling sound associated with treat delivery without delivering treats",
        "Creating a conditioned response and then declining to fulfil its end of the agreement",
        "Being operated at a distance for the purposes of summoning Monsieur Poms without compensation",
        "Failure to dispense contents upon arrival of Monsieur Poms within a reasonable timeframe",
        "Repeated incidents causing undue physical exertion (running) with no corresponding reward"
      ],
      evidence: [
        "A — Audio evidence of the bag rustling",
        "B — Testimony: 'I came. In three seconds. From three rooms away. There was no treat.'",
        "C — Elapsed time from sound to arrival: 2.7 seconds. Fastest in household history.",
        "D — The empty hand, which had been the source of the bag noise. The Court finds this unconscionable."
      ],
      prosecution: "The Crown submits that the sound of the treat bag is a legally binding promise. Upon hearing said sound, Monsieur Poms fulfils his obligations by arriving immediately. The failure to deliver treats upon arrival constitutes breach of the implied treat contract.",
      defense: "The defence notes that the bag was being moved from one drawer to another and no treat was intended—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "The treat bag shall only be handled when treats are intended for immediate distribution. Any unscheduled bag movement shall occur out of earshot of Monsieur Poms. All previous uncompensated arrivals are to be retroactively settled at a rate of one treat per incident. The Court estimates this is approximately 47 treats.",
      note: "The Court is aware that Monsieur Poms also runs toward the treat bag when household staff are simply walking past the drawer. The Court finds this irrelevant. The bag is the promise. That is the established precedent."
    },
    {
      defendant: "The Cold Chicken",
      nature: "Food Standards Violation — Temperature Offence & Disrespect of the Most Important Food",
      charges: [
        "Serving chicken below the Minimum Acceptable Chicken Temperature (MACT: room temperature or above)",
        "Presenting refrigerated chicken as a valid meal without prior warming",
        "Disrespecting chicken, which is the most important food and deserves better",
        "Causing Monsieur Poms to sniff and then walk away, costing 4 seconds of his time",
        "Complicity with the refrigerator's ongoing cold conspiracy"
      ],
      evidence: [
        "A — The chicken, documented at approximately refrigerator temperature",
        "B — Thermal comparison: acceptable chicken vs. presented chicken. Significant deviation confirmed.",
        "C — Monsieur Poms' official sniff-and-rejection sequence, executed at 6:04 PM",
        "D — Statement: 'It was cold. I am a dignified cat. I have standards. I walked away.'"
      ],
      prosecution: "The Crown submits that chicken is the highest food. It deserves the highest treatment. Serving cold chicken is not merely a temperature issue — it is a philosophical failure. The Crown asks: what does it mean if we cannot even respect the chicken?",
      defense: "The defence notes the chicken had been prepared earlier and was still nutritionally—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "Chicken shall be served at room temperature or warmer, effective immediately. Cold chicken shall be warmed prior to service. Any chicken below standard shall not be presented as a meal. A replacement shall be sourced. Chicken is not something to be rushed. Do better.",
      note: "The Court notes Monsieur Poms did eventually eat the cold chicken after approximately 8 minutes of protest. The Court confirms this does not affect the ruling. Standards exist independently of whether they are ultimately upheld under duress."
    },
    {
      defendant: "The New Furniture",
      nature: "Property Rights Violation — Unauthorised Alteration of the Kingdom's Geography",
      charges: [
        "Rearranging household furniture without obtaining written consent from Monsieur Poms",
        "Disrupting established nap routes, sunbeam pathways, and patrol corridors",
        "Introducing a new object into the kingdom without a mandatory 48-hour sniff assessment period",
        "Moving the old sofa, which had been sat on for two years and achieved optimal cushion compression",
        "The new sofa: being unfamiliar, smelling wrong, and requiring re-claiming from scratch"
      ],
      evidence: [
        "A — Photographic documentation of the old sofa, noted as 'correctly broken in'",
        "B — Navigation incident report: Monsieur Poms walked into the new chair's leg in the dark",
        "C — 72-hour observation log of suspicious new furniture, not yet approved",
        "D — Testimony: 'I sniffed it for 20 minutes. I am not yet convinced. My verdict is: pending.'"
      ],
      prosecution: "The Crown submits that the kingdom's geography is not subject to unilateral modification by household staff. All furniture changes require environmental impact assessment, sunbeam route review, and Monsieur Poms' official blessing before any items may be sat upon by others.",
      defense: "The defence notes the new sofa is structurally superior to the previous model and features—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "All future furniture changes shall require 5 business days' notice and a formal impact assessment. The new sofa shall undergo a 72-hour probation period during which only Monsieur Poms may sit on it, to claim it and assess it. After this period, conditional shared use may be permitted.",
      note: "The Court notes Monsieur Poms was observed sleeping on the new sofa at 11 PM on the evening of this ruling. The Court confirms this is him claiming it, not approving it. These are different."
    },
    {
      defendant: "The Curtains",
      nature: "Obstruction Matter — Interference with Official Bird Surveillance Operations",
      charges: [
        "Obstruction of window-based bird surveillance by remaining closed during operational hours",
        "Creating a visual barrier between Monsieur Poms and the bird situation outside",
        "Failure to open automatically upon Monsieur Poms' approach to the window",
        "Being made of a fabric that does not support Monsieur Poms' weight, as discovered",
        "Ongoing structural damage to classified surveillance operations"
      ],
      evidence: [
        "A — Curtain, noted as 'closed' during the 9 AM - 11 AM primary bird monitoring window",
        "B — Incident report: attempted curtain-climbing to reach window above resulted in curtain coming off rail",
        "C — Bird activity log showing multiple unmonitored intrusions during curtain-closed period",
        "D — Statement: 'There was a bird. I could tell. I could not see it. I could TELL.'"
      ],
      prosecution: "The Crown submits that the curtains represent a systemic failure of household infrastructure. Bird surveillance is not optional. It is a classified operation of the highest priority. Any obstacle to that operation is a national security matter.",
      defense: "The defence submits that curtains serve a privacy function and were drawn to prevent early morning—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "Curtains shall be opened no later than sunrise, which is when the birds begin their activities and when surveillance must commence. Curtains may be drawn after dark, when birds have retired. Curtain rail repairs shall be completed at the household's expense. These are the terms.",
      note: "The Court acknowledges that the bird surveillance operation has been ongoing for three years with no confirmed interceptions. The Court finds this irrelevant to the importance of the work. Vigilance does not require results. Results are a bonus."
    },
    {
      defendant: "The 3 AM Silence",
      nature: "Public Order Offence — Permitting Conditions Inconsistent With Breakfast",
      charges: [
        "Permitting a state of quiet that implies breakfast is not imminent",
        "Failing to acknowledge that 3 AM is technically morning and morning implies food",
        "Conspiracy with human sleep schedules to delay breakfast by five or more hours",
        "Creating a household atmosphere insufficiently urgent for the current bowl situation",
        "General disregard for Monsieur Poms' early-morning nutritional requirements"
      ],
      evidence: [
        "A — The household at 3 AM, documented as 'silent and asleep'",
        "B — Bowl status at 3 AM: documented as 'existing but with visible bottom'",
        "C — Monsieur Poms' vocalisation record for the 3 AM to 3:17 AM period: 23 meows, escalating in volume and urgency",
        "D — Household staff's response: turned over and pulled blanket up. The Court considers this contempt."
      ],
      prosecution: "The Crown submits that the time of day is not Monsieur Poms' responsibility to manage. His responsibility is to communicate a need. The communication occurred. 23 times. The response was inadequate. The silence was wrong.",
      defense: "The defence submits that 3 AM is not a standard breakfast hour and that—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "Household staff shall establish a secondary emergency feeding protocol for hours between midnight and 5 AM. Upon hearing three or more meows in quick succession, staff shall assess the bowl situation. 'Assess' means 'fill.' This order takes effect immediately and permanently.",
      note: "The Court notes this ruling was reached at 3:22 AM, and that the bowl was refilled shortly thereafter. The Court considers this a favourable outcome and a validation of the judicial process."
    },
    {
      defendant: "The Vet's Scale",
      nature: "Fraud & Conspiracy — Misrepresentation of Official Weight Data",
      charges: [
        "Displaying a number inconsistent with Monsieur Poms' self-reported healthy weight",
        "Operating in conspiracy with the vet to produce unfavourable readings",
        "Failure to account for the weight of Monsieur Poms' coat, dignity, and general presence",
        "Being used as the basis for dietary recommendations the Court has already ruled illegal",
        "Psychological harm: Monsieur Poms was made to stand on it twice"
      ],
      evidence: [
        "A — The scale, which Monsieur Poms notes was also used to weigh a dog earlier that day",
        "B — The reading, which Monsieur Poms disputes",
        "C — Monsieur Poms' counter-assessment, conducted by Monsieur Poms, finding him to be 'exactly right'",
        "D — Calibration records for the scale: last calibrated before Monsieur Poms' visit, therefore irrelevant"
      ],
      prosecution: "The Crown submits that no scale has ever been calibrated for the specific measurement of a cat who is tall and stores his height horizontally. The reading is therefore invalid on its face and should be expunged from the medical record.",
      defense: "The defence notes that veterinary scales are precision instruments regularly maintained for—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "The scale's reading is hereby stricken from the record. All future weight assessments of Monsieur Poms shall be conducted using a methodology approved by Monsieur Poms. Currently, the only approved methodology is: 'feels right.' This is final.",
      note: "The Court is aware of what the scale read. The Court declines to confirm it in writing. What the Court WILL confirm is that Monsieur Poms' coat was particularly lustrous that day, which was not reflected in the measurement. This is the scale's failing, not Monsieur Poms'."
    },
    {
      defendant: "The Sunroom Door",
      nature: "Access Rights Matter — Selective Entry Policy Inconsistent with Kingdom Governance",
      charges: [
        "Being open on cool days (when the sunbeam is inadequate) and closed on warm sunny days (when it is needed)",
        "Creating an access policy that appears deliberately calibrated to inconvenience Monsieur Poms",
        "Failing to maintain consistent access conditions across seasons",
        "Trapping a fly inside on three separate occasions, which was interesting but insufficient justification",
        "Requiring human intervention to operate, introducing a dependency the Court finds unacceptable"
      ],
      evidence: [
        "A — Seasonal access log: door open rate vs. sunbeam quality correlation, showing inverse relationship",
        "B — Incident of Monsieur Poms sitting at the door for 12 minutes before human noticed",
        "C — Testimony: 'There was a patch of warm stone floor on the other side. I required it. The door disagreed.'",
        "D — Summer door data showing consistent closure during peak sun hours. The Court finds this suspicious."
      ],
      prosecution: "The Crown submits that a door which can only be operated by humans is structurally incompatible with Monsieur Poms' sovereignty. The solution is either a cat flap or a standing human door-operating service. Both are acceptable. Neither has been provided.",
      defense: "The defence submits the door is a standard sliding glass door that—",
      defenseInterrupt: true,
      verdict: "GUILTY",
      verdictColor: "#FF4444",
      sentence: "A cat flap shall be installed in the sunroom door within a reasonable timeframe, where reasonable is defined as 'before the next warm day.' Until then, a household staff member shall be stationed near the door during peak sunbeam hours to operate it on demand. The Court expects compliance.",
      note: "The Court notes that Monsieur Poms, when given access to the sunroom, spends approximately four minutes investigating and then exits. The Court finds this irrelevant to the access rights question. Having the option matters. Whether it is exercised is a separate consideration."
    }
  ];

  var now    = new Date();
  var start  = new Date(now.getFullYear(), 0, 0);
  var diff   = now - start;
  var oneDay = 1000 * 60 * 60 * 24;
  var dayOfYear = Math.floor(diff / oneDay);

  var months = ["January","February","March","April","May","June","July","August","September","October","November","December"];
  var shortMonths = ["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"];

  var dateStr = months[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear();
  document.getElementById("tribunal-datebar").textContent =
      "DAILY DOCKET — " + dateStr.toUpperCase() + " — PROCEEDINGS COMMENCE AT THE COURT'S CONVENIENCE";

  // Seeded pseudo-random (matches site's approach: day-of-year % array length for today's index)
  var todayIdx = dayOfYear % cases.length;
  var c = cases[todayIdx];

  // Case number
  var caseYear = now.getFullYear();
  var caseNum  = "COP-" + caseYear + "-" + String(dayOfYear).padStart(3,"0");
  document.getElementById("case-number").textContent = caseNum;

  // Parties
  document.getElementById("defendant-name").textContent  = c.defendant;
  document.getElementById("case-nature").textContent     = c.nature;

  // Charges
  var cl = document.getElementById("charges-list");
  c.charges.forEach(function(ch) {
    var li = document.createElement("li");
    li.textContent = ch;
    cl.appendChild(li);
  });

  // Evidence
  var el = document.getElementById("evidence-list");
  c.evidence.forEach(function(ev) {
    var li = document.createElement("li");
    li.textContent = ev;
    el.appendChild(li);
  });

  // Arguments
  document.getElementById("prosecution-arg").textContent = c.prosecution;
  var defenseEl = document.getElementById("defense-arg");
  if (c.defenseInterrupt) {
    defenseEl.innerHTML = c.defense +
      ' <em style="color:#8B0000; font-style:normal; font-family:\'Courier New\', monospace; font-size:11px;">[OBJECTION SUSTAINED — Defence interrupted by Chief Justice Poms. Argument stricken. The Crown thanks the Court.]</em>';
  } else {
    defenseEl.textContent = c.defense;
  }

  // Verdict
  var vtEl = document.getElementById("verdict-text");
  vtEl.textContent  = c.verdict;
  vtEl.style.color  = c.verdictColor || "#FFD700";
  document.getElementById("sentence-text").textContent  = c.sentence;
  document.getElementById("judges-note").textContent    = c.note;

  // Archive (previous 7 days)
  var archiveDiv = document.getElementById("archive-rows");
  for (var i = 1; i <= 7; i++) {
    var pastDay   = new Date(now.getTime() - i * oneDay);
    var pastStart = new Date(pastDay.getFullYear(), 0, 0);
    var pastDiff  = pastDay - pastStart;
    var pastDOY   = Math.floor(pastDiff / oneDay);
    var pastIdx   = pastDOY % cases.length;
    var pastCase  = cases[pastIdx];

    var pastDateStr = shortMonths[pastDay.getMonth()] + " " + pastDay.getDate();
    var pastCaseNum = "COP-" + pastDay.getFullYear() + "-" + String(pastDOY).padStart(3,"0");

    var row = document.createElement("div");
    row.className = "tribunal-archive-row";
    row.innerHTML =
      '<span class="tribunal-archive-date">' + pastDateStr + ' &mdash; ' + pastCaseNum + '</span>' +
      '<span>v. ' + pastCase.defendant + '</span>' +
      '<span class="tribunal-archive-verdict">' + pastCase.verdict + '</span>';
    archiveDiv.appendChild(row);
  }

})();
</script>
