---
title: "Dream Chronicles"
---

<style>
.dream-page-wrap {
    background: linear-gradient(160deg, #0a0018 0%, #110022 40%, #060010 100%);
    margin: -10px -10px 0 -10px;
    padding: 0 0 24px 0;
    border-bottom: 4px solid #6600cc;
    position: relative;
    overflow: hidden;
}

.dream-stars {
    position: absolute;
    top: 0; left: 0; right: 0; bottom: 0;
    pointer-events: none;
    overflow: hidden;
}

.star {
    position: absolute;
    border-radius: 50%;
    background: #fff;
    animation: twinkle var(--dur, 2.5s) ease-in-out infinite;
    opacity: 0;
}
@keyframes twinkle {
    0%,100% { opacity: 0; }
    50%      { opacity: var(--bright, 0.9); }
}

.dream-header-inner {
    position: relative;
    text-align: center;
    padding: 28px 16px 20px;
    z-index: 1;
}

.dream-moon {
    font-size: 52px;
    display: block;
    line-height: 1;
    animation: moonFloat 6s ease-in-out infinite;
    text-shadow: 0 0 30px rgba(200,160,255,0.8);
}
@keyframes moonFloat {
    0%,100% { transform: translateY(0); }
    50%      { transform: translateY(-6px); }
}

.dream-main-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 30px;
    letter-spacing: 5px;
    color: #FFD700;
    text-shadow: 0 0 18px #cc88ff, 2px 2px 0 #000;
    margin: 10px 0 4px;
    text-transform: uppercase;
}

.dream-subtitle {
    font-size: 10px;
    color: #cc88ff;
    letter-spacing: 4px;
    text-transform: uppercase;
    font-family: 'Courier New', monospace;
}

.dream-dateline {
    margin-top: 10px;
    font-size: 10px;
    color: #9966cc;
    letter-spacing: 2px;
    font-family: 'Courier New', monospace;
    border-top: 1px solid #3a0066;
    border-bottom: 1px solid #3a0066;
    padding: 5px 0;
    display: inline-block;
}

.dream-card {
    background: rgba(15, 5, 30, 0.92);
    border: 2px solid #6600cc;
    box-shadow: 0 0 24px rgba(102,0,204,0.4), inset 0 0 40px rgba(102,0,204,0.06);
    margin: 16px 12px 0;
    position: relative;
    z-index: 1;
}

.dream-card-header {
    background: linear-gradient(to right, #3a0066, #6600cc, #3a0066);
    padding: 8px 14px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 6px;
}

.dream-ref {
    font-family: 'Courier New', monospace;
    font-size: 9px;
    color: #cc88ff;
    letter-spacing: 2px;
}

.dream-class-badge {
    font-family: 'Courier New', monospace;
    font-size: 9px;
    letter-spacing: 1px;
    padding: 2px 7px;
    border: 1px solid #FFD700;
    color: #FFD700;
    text-transform: uppercase;
}

.dream-title-block {
    text-align: center;
    padding: 18px 14px 10px;
    border-bottom: 1px solid #3a0066;
}

.dream-emoji-row {
    font-size: 26px;
    margin-bottom: 6px;
    letter-spacing: 8px;
}

.dream-title-text {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 22px;
    color: #FFD700;
    text-shadow: 0 0 12px rgba(255,215,0,0.5);
    letter-spacing: 3px;
    text-transform: uppercase;
    line-height: 1.2;
}

.dream-meta-row {
    display: flex;
    justify-content: center;
    gap: 20px;
    padding: 10px 14px;
    border-bottom: 1px solid #3a0066;
    flex-wrap: wrap;
}

.dream-meta-item {
    text-align: center;
    font-family: 'Courier New', monospace;
    font-size: 9px;
    color: #9966cc;
}

.dream-meta-value {
    display: block;
    font-size: 11px;
    color: #cc88ff;
    font-weight: bold;
    margin-top: 2px;
    letter-spacing: 1px;
}

.dream-section {
    padding: 12px 16px;
    border-bottom: 1px solid #3a0066;
}

.dream-section-title {
    font-family: 'Verdana', sans-serif;
    font-size: 8px;
    font-weight: bold;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: #cc88ff;
    border-bottom: 1px solid #3a0066;
    padding-bottom: 5px;
    margin-bottom: 9px;
}

.dream-synopsis {
    font-size: 12px;
    color: #e8d4ff;
    line-height: 1.8;
    font-style: italic;
    font-family: Georgia, serif;
}

.cast-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 10px;
}

.cast-table th {
    background: rgba(102,0,204,0.3);
    color: #cc88ff;
    font-family: 'Courier New', monospace;
    font-size: 8px;
    letter-spacing: 2px;
    text-transform: uppercase;
    padding: 4px 8px;
    text-align: left;
    border: 1px solid #3a0066;
}

.cast-table td {
    padding: 5px 8px;
    border: 1px solid #3a0066;
    color: #ddc8ff;
    vertical-align: top;
    line-height: 1.5;
}

.cast-role {
    font-weight: bold;
    font-family: 'Courier New', monospace;
    font-size: 9px;
    padding: 1px 5px;
    display: inline-block;
}

.role-ally     { color: #00FF88; border: 1px solid #00FF88; }
.role-enemy    { color: #FF4444; border: 1px solid #FF4444; }
.role-neutral  { color: #FFAA00; border: 1px solid #FFAA00; }
.role-setting  { color: #88AAFF; border: 1px solid #88AAFF; }
.role-absent   { color: #888; border: 1px solid #888; }
.role-unknown  { color: #FF88FF; border: 1px solid #FF88FF; }

.symbol-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
}

.symbol-item {
    background: rgba(102,0,204,0.15);
    border: 1px solid #4a0099;
    padding: 5px 9px;
    flex: 1;
    min-width: 140px;
    font-size: 10px;
}

.symbol-name {
    color: #FFD700;
    font-weight: bold;
    font-size: 10px;
    display: block;
    margin-bottom: 2px;
    font-family: 'Courier New', monospace;
}

.symbol-meaning {
    color: #cc88ff;
    line-height: 1.5;
}

.interp-box {
    background: rgba(255,215,0,0.06);
    border-left: 3px solid #FFD700;
    padding: 10px 12px;
    font-size: 11px;
    color: #e8d4ff;
    line-height: 1.8;
    font-style: italic;
    font-family: Georgia, serif;
}

.impact-box {
    background: rgba(255,60,60,0.06);
    border: 1px solid #660022;
    padding: 10px 12px;
    font-size: 11px;
    color: #ffbbbb;
    line-height: 1.75;
    font-family: 'Verdana', sans-serif;
}

.paw-star     { color: #FFD700; font-size: 16px; }
.paw-star-off { color: #333; font-size: 16px; }

/* Dream archive section */
.archive-outer {
    margin: 16px 12px 0;
    background: rgba(10,0,25,0.8);
    border: 1px solid #3a0066;
    z-index: 1;
    position: relative;
}

.archive-header {
    background: linear-gradient(to right, #220044, #3a0066, #220044);
    padding: 6px 14px;
    font-family: 'Courier New', monospace;
    font-size: 9px;
    letter-spacing: 3px;
    color: #cc88ff;
    text-transform: uppercase;
}

.archive-row {
    display: flex;
    align-items: center;
    border-bottom: 1px solid #220044;
    padding: 5px 14px;
    gap: 10px;
    font-size: 10px;
}

.archive-night {
    color: #6644aa;
    font-family: 'Courier New', monospace;
    font-size: 9px;
    width: 80px;
    flex-shrink: 0;
}

.archive-title {
    color: #cc88ff;
    flex: 1;
    font-style: italic;
}

.archive-class {
    font-family: 'Courier New', monospace;
    font-size: 8px;
    color: #9966cc;
    letter-spacing: 1px;
}

/* Recurring dreams registry */
.recurring-outer {
    margin: 10px 12px 0;
    border: 1px dashed #3a0066;
    background: rgba(10,0,25,0.6);
    position: relative;
    z-index: 1;
}

.recurring-header {
    background: rgba(60,0,100,0.8);
    padding: 6px 14px;
    font-family: 'Courier New', monospace;
    font-size: 9px;
    letter-spacing: 3px;
    color: #cc88ff;
    text-transform: uppercase;
}

.recurring-item {
    display: flex;
    align-items: flex-start;
    gap: 8px;
    padding: 6px 14px;
    border-bottom: 1px solid #1a0033;
    font-size: 10px;
}

.recurring-num {
    color: #6644aa;
    font-family: 'Courier New', monospace;
    font-size: 9px;
    width: 20px;
    flex-shrink: 0;
    padding-top: 1px;
}

.recurring-name {
    color: #e8d4ff;
    font-weight: bold;
    font-size: 10px;
}

.recurring-desc {
    color: #9966cc;
    font-size: 9px;
    margin-top: 1px;
    line-height: 1.4;
}

.dream-footer-note {
    margin: 10px 12px 0;
    font-size: 9px;
    color: #4a2266;
    font-family: 'Courier New', monospace;
    line-height: 1.7;
    text-align: center;
    position: relative;
    z-index: 1;
}
</style>

<div class="dream-page-wrap">

<!-- Stars background -->
<div class="dream-stars" id="dream-star-field"></div>

<div class="dream-header-inner">
    <span class="dream-moon">🌙</span>
    <div class="dream-main-title">Dream Chronicles</div>
    <div class="dream-subtitle">Official Nocturnal Report — Filed by Monsieur Poms</div>
    <div class="dream-dateline" id="dream-dateline">Loading...</div>
</div>

<!-- Main dream card -->
<div class="dream-card" id="dream-main-card">

    <div class="dream-card-header">
        <div class="dream-ref" id="dream-ref">MPDC-????</div>
        <div class="dream-class-badge" id="dream-class-badge">—</div>
    </div>

    <div class="dream-title-block">
        <div class="dream-emoji-row" id="dream-emojis">✨ 🐾 ✨</div>
        <div class="dream-title-text" id="dream-title">Loading...</div>
    </div>

    <div class="dream-meta-row">
        <div class="dream-meta-item">
            REM PHASE
            <span class="dream-meta-value" id="dream-rem">—</span>
        </div>
        <div class="dream-meta-item">
            ESTIMATED DURATION
            <span class="dream-meta-value" id="dream-duration">—</span>
        </div>
        <div class="dream-meta-item">
            VIVIDNESS
            <span class="dream-meta-value" id="dream-vividness">—</span>
        </div>
        <div class="dream-meta-item">
            CLEARANCE LEVEL
            <span class="dream-meta-value" id="dream-clearance">—</span>
        </div>
    </div>

    <!-- Synopsis -->
    <div class="dream-section">
        <div class="dream-section-title">🌠 Dream Synopsis</div>
        <div class="dream-synopsis" id="dream-synopsis">Loading...</div>
    </div>

    <!-- Cast -->
    <div class="dream-section">
        <div class="dream-section-title">🎭 Dramatis Personae</div>
        <table class="cast-table">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Role</th>
                    <th>Notes</th>
                </tr>
            </thead>
            <tbody id="dream-cast"></tbody>
        </table>
    </div>

    <!-- Symbols -->
    <div class="dream-section">
        <div class="dream-section-title">🔮 Dream Symbol Analysis</div>
        <div class="symbol-grid" id="dream-symbols"></div>
    </div>

    <!-- Interpretation -->
    <div class="dream-section">
        <div class="dream-section-title">📜 Official Interpretation by Monsieur Poms</div>
        <div class="interp-box" id="dream-interpretation">Loading...</div>
        <div style="text-align:right; font-size:9px; color:#6644aa; margin-top:6px; font-family:'Courier New',monospace;">
            — Monsieur Poms, Certified Dream Analyst (Self-Certified, 2022)
        </div>
    </div>

    <!-- Household Impact -->
    <div class="dream-section" style="border-bottom:none;">
        <div class="dream-section-title">⚠️ Household Impact Assessment</div>
        <div class="impact-box" id="dream-impact">Loading...</div>
    </div>

</div>

<!-- Archive -->
<div class="archive-outer">
    <div class="archive-header">📁 Recent Dream Archive — Last 7 Nights</div>
    <div id="dream-archive"></div>
</div>

<!-- Recurring dreams -->
<div class="recurring-outer">
    <div class="recurring-header">🔁 Recurring Dream Registry (Top 5 Most Documented)</div>
    <div class="recurring-item">
        <div class="recurring-num">#1</div>
        <div>
            <div class="recurring-name">THE INFINITE KIBBLE PLAINS</div>
            <div class="recurring-desc">A boundless prairie of premium chicken-flavored kibble. No green beans. Ever. A utopian vision filed 47 times in the official registry.</div>
        </div>
    </div>
    <div class="recurring-item">
        <div class="recurring-num">#2</div>
        <div>
            <div class="recurring-name">THE VACUUM VANQUISHED</div>
            <div class="recurring-desc">Poms defeats the vacuum cleaner in single combat. Method varies per dream. The vacuum is always defeated. The outcome is not in question.</div>
        </div>
    </div>
    <div class="recurring-item">
        <div class="recurring-num">#3</div>
        <div>
            <div class="recurring-name">THE SUNBEAM THAT FOLLOWED</div>
            <div class="recurring-desc">A personal, portable sunbeam that moves with Poms at all times, maintaining peak warmth regardless of clouds or house layout. Filed 31 times.</div>
        </div>
    </div>
    <div class="recurring-item">
        <div class="recurring-num">#4</div>
        <div>
            <div class="recurring-name">THE ACKNOWLEDGMENT OF TALLNESS</div>
            <div class="recurring-desc">All household members, and eventually the international community, formally confirm that Poms is tall, not wide. A deeply important dream. Filed 28 times.</div>
        </div>
    </div>
    <div class="recurring-item">
        <div class="recurring-num">#5</div>
        <div>
            <div class="recurring-name">THE TREAT BAG THAT NEVER EMPTIED</div>
            <div class="recurring-desc">An ordinary-looking treat bag that refills itself continuously. All treats are chicken flavour. The bag is never put away. Filed 26 times.</div>
        </div>
    </div>
</div>

<div class="dream-footer-note">
    All dreams are official records of Monsieur Poms Productions. Dreams are filed nightly and sealed with one official paw print.<br>
    Dream content is 100% accurate. Any resemblance to anxieties about the vet is coincidental and classified.<br>
    Green beans do not appear in any registered dream. This is intentional. This will not change.
</div>

</div><!-- end dream-page-wrap -->

<script>
(function () {

    /* ── Utilities ─────────────────────────────────────────────────────── */
    function seededRand(s) {
        var x = Math.sin(s * 127.1 + 311.7) * 43758.5453123;
        return x - Math.floor(x);
    }
    function pick(arr, s) { return arr[Math.floor(seededRand(s) * arr.length)]; }
    function esc(s) { return String(s).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;'); }
    function pad(n) { return n < 10 ? '0' + n : '' + n; }

    var now     = new Date();
    var doy     = Math.floor((now - new Date(now.getFullYear(), 0, 0)) / 86400000);
    var seed    = now.getFullYear() * 1000 + doy;

    var dayNames   = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
    var monthNames = ["January","February","March","April","May","June","July","August","September","October","November","December"];

    /* ── Date display ──────────────────────────────────────────────────── */
    document.getElementById('dream-dateline').textContent =
        'DREAM OF THE NIGHT:  ' + dayNames[now.getDay()] + ' ' + monthNames[now.getMonth()] + ' ' + now.getDate() + ', ' + now.getFullYear() +
        '   ✦   UPDATED NIGHTLY AT MIDNIGHT';

    /* ── Stars ─────────────────────────────────────────────────────────── */
    (function buildStars() {
        var field = document.getElementById('dream-star-field');
        var starData = [
            {top:8,left:5,size:2,dur:2.1,bright:0.9},
            {top:15,left:22,size:1,dur:3.3,bright:0.7},
            {top:4,left:45,size:2,dur:1.8,bright:0.85},
            {top:22,left:63,size:1,dur:2.7,bright:0.6},
            {top:10,left:80,size:2,dur:3.1,bright:0.9},
            {top:30,left:90,size:1,dur:2.4,bright:0.8},
            {top:40,left:12,size:2,dur:1.9,bright:0.75},
            {top:55,left:35,size:1,dur:3.5,bright:0.65},
            {top:35,left:55,size:2,dur:2.2,bright:0.9},
            {top:60,left:75,size:1,dur:2.8,bright:0.7},
            {top:70,left:8,size:1,dur:3.0,bright:0.6},
            {top:80,left:48,size:2,dur:1.7,bright:0.85},
            {top:75,left:88,size:1,dur:2.5,bright:0.8},
            {top:50,left:96,size:2,dur:3.2,bright:0.7},
            {top:90,left:30,size:1,dur:2.0,bright:0.9},
            {top:85,left:70,size:2,dur:2.6,bright:0.75},
            {top:18,left:38,size:1,dur:3.4,bright:0.65},
            {top:45,left:20,size:1,dur:1.6,bright:0.85},
            {top:65,left:58,size:2,dur:2.9,bright:0.7},
            {top:92,left:92,size:1,dur:2.3,bright:0.8}
        ];
        starData.forEach(function(s) {
            var el = document.createElement('div');
            el.className = 'star';
            el.style.cssText = [
                'top:' + s.top + '%;',
                'left:' + s.left + '%;',
                'width:' + s.size + 'px;',
                'height:' + s.size + 'px;',
                '--dur:' + s.dur + 's;',
                '--bright:' + s.bright + ';',
                'animation-delay:' + (s.dur * seededRand(s.top * 7 + s.left)).toFixed(2) + 's;'
            ].join('');
            field.appendChild(el);
        });
    })();

    /* ── Dream data ────────────────────────────────────────────────────── */
    var dreams = [
        {
            ref: "MPDC-A-0001",
            classification: "RECURRING — CRITICAL",
            emojis: "🌾 🐾 🌾",
            title: "The Infinite Kibble Plains",
            rem: "REM Phase 4 (Advanced)",
            duration: "Approx. 3 hrs 22 min",
            vividness: 5,
            clearance: "GOLD",
            synopsis: "Monsieur Poms stood atop a boundless golden plain made entirely of premium chicken-flavoured kibble. The horizon stretched in every direction without limit. A warm, enormous sunbeam blanketed the entire landscape. There were no green beans anywhere in the known dreamscape — an official search was conducted and confirmed negative results. The food bowl was present, full, and self-refilling. It was, by every recorded metric, ideal.",
            cast: [
                { name: "The Food Bowl", role: "ally", desc: "Full at all times. Self-refilling. Exactly the correct temperature." },
                { name: "The Sunbeam", role: "setting", desc: "Enormous. Personal. Moved with Poms across the landscape at all times." },
                { name: "Green Beans", role: "absent", desc: "Confirmed not present. A formal absence report was filed within the dream." }
            ],
            symbols: [
                { symbol: "Infinite Kibble", meaning: "Poms' deepest sense of security. Also: the correct state of the universe." },
                { symbol: "Self-refilling Bowl", meaning: "The natural order operating as it should. No human intervention required." },
                { symbol: "Absent Green Beans", meaning: "Paradise. The elimination of all that is wrong with the world." }
            ],
            interpretation: "This dream confirms what I have always privately known: the universe, at its most correct, looks very much like this. The kibble plains represent optimal conditions for governance and wellbeing. I have shared this dream with my household as a formal policy proposal. The proposal was not acted on. The proposal stands.",
            impact: "Poms woke with elevated standards and a clear vision for bowl policy reform. The bowl must be filled before first contact. No dietary commentary under any circumstances. Treat compliance is expected throughout the day."
        },
        {
            ref: "MPDC-B-0002",
            classification: "ACTION — RECURRING",
            emojis: "💨 😼 💥",
            title: "The Vacuum Wars: Final Stand",
            rem: "REM Phase 3 (Intense)",
            duration: "Approx. 1 hr 47 min",
            vividness: 5,
            clearance: "CLASSIFIED",
            synopsis: "The vacuum cleaner made an unauthorized advance across the kitchen floor. Monsieur Poms, after a brief tactical retreat to the hallway, returned with superior strategy and a powerful combination of hissing and extremely pointed staring. The vacuum cleaner was defeated. The exact method of defeat is classified. What is not classified: Poms won. He always wins in this dream. The household owes him a formal commendation.",
            cast: [
                { name: "Monsieur Poms", role: "ally", desc: "Supreme Commander of household perimeter defence. Victory confirmed." },
                { name: "The Vacuum Cleaner", role: "enemy", desc: "Defeated. Again. Its noise and audacity were no match for The Stare." },
                { name: "The Broom Closet", role: "setting", desc: "Strategic retreat location. Temporarily used as a command post." }
            ],
            symbols: [
                { symbol: "The Vacuum", meaning: "All threats to peace. Also: literally the vacuum, which is still a problem." },
                { symbol: "The Stare", meaning: "Poms' ultimate weapon. Has never failed in 47 recorded dream deployments." },
                { symbol: "Victory", meaning: "The correct and expected outcome. This is not symbolic. This is accurate." }
            ],
            interpretation: "I have now defeated the vacuum cleaner 47 times in this dream series. The real-world vacuum has not received the message. I am considering escalating to a formal press conference. The details of my dream tactics are classified but the outcome is public knowledge: I won. I always win.",
            impact: "Poms may be more alert than usual near the broom closet. Do not operate the vacuum today without advance diplomatic notice of no fewer than three hours. Treat dispensation recommended as recognition of last night's service."
        },
        {
            ref: "MPDC-C-0003",
            classification: "DIPLOMATIC — FIRST CONTACT",
            emojis: "🐦 🤝 🐾",
            title: "The Summit at Window B",
            rem: "REM Phase 2 (Significant)",
            duration: "Approx. 2 hrs 05 min",
            vividness: 4,
            clearance: "RESTRICTED",
            synopsis: "A formal summit was convened at Window B between Monsieur Poms and the bird delegation — specifically the blue jay who has been under surveillance since March. Both parties arrived with prepared statements. The birds had grievances about the staring. Poms had extensive documentation of all incidents. After lengthy negotiations, a temporary ceasefire was reached. The birds agreed to fly more slowly past the window. Poms agreed to limit surveillance to daylight hours only. The ceasefire lasted three minutes before both parties resumed their positions.",
            cast: [
                { name: "Monsieur Poms", role: "neutral", desc: "Lead negotiator. Arrived with 14 pages of documented surveillance findings." },
                { name: "The Blue Jay (Agent B1)", role: "unknown", desc: "Represented the full bird delegation. Made eye contact. Intentions remain unclear." },
                { name: "Window B", role: "setting", desc: "Site of the summit and ongoing intelligence operations since Q1." }
            ],
            symbols: [
                { symbol: "The Ceasefire", meaning: "Temporary. Both parties understand this. The surveillance continues." },
                { symbol: "Eye Contact", meaning: "A power move by the bird. Poms recognizes a fellow strategist. Threat level: elevated." },
                { symbol: "The Blue Jay", meaning: "The singular most watched entity in Poms' operational database." }
            ],
            interpretation: "The birds have proven more sophisticated than previously assessed. They came to the table with demands. This is unexpected and frankly impressive. I have updated their threat classification from 'nuisance' to 'rival entity requiring continued monitoring.' The ceasefire was tactical. The surveillance was never actually suspended. I simply moved to a less visible position.",
            impact: "Window B must remain accessible and unobstructed. The bird situation is active. Household members should not comment on the birds, stand in front of the window, or suggest that the blue jay is 'just a bird.' It is not just a bird. It has been to the table."
        },
        {
            ref: "MPDC-D-0004",
            classification: "ACHIEVEMENT — PROFESSIONAL",
            emojis: "🧩 🏆 ⭐",
            title: "The World Food Puzzle Championship",
            rem: "REM Phase 3 (Clear)",
            duration: "Approx. 1 hr 18 min",
            vividness: 5,
            clearance: "PUBLIC RECORD",
            synopsis: "Monsieur Poms competed in and won the inaugural World Food Puzzle Championship in front of a large and visibly impressed audience. The puzzle — previously described by organizers as 'the hardest kibble puzzle ever constructed' — was completed in approximately 0.4 seconds. The crowd cheered. A formal trophy was presented. The trophy was chicken-shaped. A second puzzle was requested for an encore. Poms completed that one immediately as well, without breaking eye contact with the judges.",
            cast: [
                { name: "Monsieur Poms", role: "ally", desc: "Champion. Gold medal. Perfect score. Zero hesitation. The record stands." },
                { name: "The Audience", role: "setting", desc: "Present. Impressed. Did not fully understand what they had witnessed." },
                { name: "The Food Puzzle", role: "neutral", desc: "Defeated in 0.4 seconds. Posed no meaningful challenge. Issued no statement." }
            ],
            symbols: [
                { symbol: "The Trophy", meaning: "Formal recognition of what was already obvious to everyone present." },
                { symbol: "0.4 Seconds", meaning: "Personal best. World record. Household record. All records." },
                { symbol: "The Second Puzzle", meaning: "An encore for the audience. Poms did not need to do it. He chose to." }
            ],
            interpretation: "This dream is less symbolic and more documentary in nature. These events reflect accurately the level at which I operate when presented with a food puzzle. The real-world puzzle record is also excellent. I would like both records entered into the public archive. This is a formal request.",
            impact: "Today is a good day to acknowledge the food puzzle achievement out loud. The phrase 'Poms solved the puzzle very quickly' said aloud to no one in particular is sufficient. A bonus treat as recognition is strongly encouraged. The trophy does not need to be real. The acknowledgment does."
        },
        {
            ref: "MPDC-E-0005",
            classification: "POLITICAL — DECREE",
            emojis: "📜 👑 ✨",
            title: "The Decree Heard Round The World",
            rem: "REM Phase 4 (Prophetic)",
            duration: "Approx. 2 hrs 51 min",
            vividness: 5,
            clearance: "GOLD",
            synopsis: "Monsieur Poms issued a formal decree from his position on the highest point of the couch. The decree concerned the treat schedule, the bowl situation, and a proposal to eliminate Mondays. The decree was read by every household on Earth simultaneously. Compliance was immediate and universal. Treat bags were opened in every kitchen. Bowls were filled. The portion of the decree concerning Mondays was technically complex and remains under implementation review.",
            cast: [
                { name: "Monsieur Poms", role: "ally", desc: "Issuer of the decree. Highest point on the couch. Authority unchallenged." },
                { name: "The International Community", role: "neutral", desc: "In attendance. Compliant. Impressed by the quality of the decree." },
                { name: "Mondays", role: "enemy", desc: "Subject to ongoing elimination. Procedurally complex. Working group assigned." }
            ],
            symbols: [
                { symbol: "The High Couch Position", meaning: "Authority. Command. Also: a very good spot with ideal sightlines." },
                { symbol: "Universal Compliance", meaning: "The natural result of a well-worded decree. This is how it should work." },
                { symbol: "Monday Elimination", meaning: "A long-standing policy position. Implementation is difficult. Policy is firm." }
            ],
            interpretation: "The dream confirms that my decrees are of sufficient quality and authority to achieve worldwide compliance when properly presented. The real-world adoption rate of my decrees remains disappointing by comparison. I have not adjusted my expectations downward. I have adjusted my communication strategy upward.",
            impact: "Today's decree will be issued from the couch. It will concern the bowl. Household should review treat inventory before 9 AM. The Monday situation has not been resolved but efforts are ongoing and Poms' position has not changed."
        },
        {
            ref: "MPDC-F-0006",
            classification: "MYSTERY — CLASSIFIED",
            emojis: "🚪 ❓ 🌀",
            title: "The Door That Always Opened",
            rem: "REM Phase 2 (Unusual)",
            duration: "Approx. 1 hr 33 min",
            vividness: 3,
            clearance: "TOP SECRET",
            synopsis: "There was a door. A specific door in the hallway that has always been closed. In last night's dream, it opened. Poms approached with appropriate caution and full investigative procedure. Beyond the door was another hallway. At the end of that hallway: another door. That door also opened. What lay beyond the second door is classified and will not be disclosed. What can be confirmed: Poms investigated. Poms filed a report. Poms has not ruled anything out.",
            cast: [
                { name: "The First Door", role: "neutral", desc: "Opened for the first time. Subject to ongoing analysis. Classification: significant." },
                { name: "The Second Door", role: "unknown", desc: "Also opened. What was behind it is classified. This is final." },
                { name: "Monsieur Poms", role: "ally", desc: "Lead investigator. Followed correct protocol. Report is sealed." }
            ],
            symbols: [
                { symbol: "The First Door", meaning: "A threshold. The unknown made accessible. Or a door. Possibly just a door." },
                { symbol: "The Second Door", meaning: "Classified. No symbol analysis available at this clearance level." },
                { symbol: "The Hallway", meaning: "Transitional space. Also: a place Poms already runs through at 2 AM regularly." }
            ],
            interpretation: "I cannot tell you what I found. What I can tell you is that the investigation was conducted correctly and that the findings are significant. The report is filed. The classification level prevents disclosure. I have made a note to investigate the real hallway door more thoroughly. Just in case.",
            impact: "Poms may spend additional time investigating hallway spaces today. Doors that are partially open may be subject to increased scrutiny. Household should not interfere with ongoing investigations or ask what Poms is looking at. He will not say. This is classified."
        },
        {
            ref: "MPDC-G-0007",
            classification: "PSYCHOLOGICAL — ANXIETY LOG",
            emojis: "☀️ 🏃 ☀️",
            title: "The Moving Sunbeam Incident",
            rem: "REM Phase 1 (Stressful)",
            duration: "Approx. 58 min",
            vividness: 4,
            clearance: "RESTRICTED",
            synopsis: "A previously ideal sunbeam moved. Without warning. Without authorization. Monsieur Poms had claimed and occupied the premium beam at 9:47 AM (dream time). By 10:15, it had shifted 14 inches to the left. Poms adjusted. It moved again. By 11:00, Poms had relocated five times. The beam appeared to be deliberately evading him. This is a known and recurring nightmare variant. It is taken seriously. A formal grievance was filed within the dream.",
            cast: [
                { name: "The Sunbeam", role: "enemy", desc: "Normally an ally. In this dream: an adversary. Moving without consent. Classified as a threat." },
                { name: "Monsieur Poms", role: "ally", desc: "Persistent. Adaptive. Filed five location-change reports within the dream. Did not give up." },
                { name: "The Floor", role: "neutral", desc: "Cold. Less good than the sunbeam. Present as a constant reminder of the situation." }
            ],
            symbols: [
                { symbol: "The Moving Sunbeam", meaning: "Loss of control over an important resource. A primary source of anxiety for Poms." },
                { symbol: "Five Relocations", meaning: "Persistence and determination. Also: frustration. Both are correct." },
                { symbol: "The Cold Floor", meaning: "The stakes of failure. What happens if the sunbeam is not reclaimed." }
            ],
            interpretation: "This dream represents a scenario I find genuinely concerning. The sunbeam has always moved throughout the day — I know this and I track it. But in this dream it moved in ways that defied the expected pattern. I did not like it. I have filed a grievance. The sunbeam situation in the real world will be monitored closely today.",
            impact: "Window blinds and curtains must not be adjusted today. The sunbeam situation requires proactive household management. If the beam moves, Poms will follow it — this must not be commented upon. Today is a sensitive sunbeam day. Treat availability is recommended as a mood stabiliser."
        },
        {
            ref: "MPDC-H-0008",
            classification: "SOCIAL — DOMESTIC",
            emojis: "🍗 🎉 🪑",
            title: "The Grand Formal Banquet",
            rem: "REM Phase 3 (Detailed)",
            duration: "Approx. 2 hrs 14 min",
            vividness: 4,
            clearance: "PUBLIC RECORD",
            synopsis: "Monsieur Poms hosted a formal sit-down banquet for invited guests. The menu was chicken. All chicken. Multiple courses: chicken starter, chicken main, chicken dessert. The seating arrangement was managed personally by Poms. The dog next door was not on the guest list. Attempts by the dog to attend were addressed diplomatically through the locked gate. The event was widely regarded by attendees as an excellent occasion. Poms gave a speech about the bowl.",
            cast: [
                { name: "Monsieur Poms", role: "ally", desc: "Host. Speech-giver. Menu designer. Declined to serve green beans. This was not negotiable." },
                { name: "The Invited Guests", role: "ally", desc: "Present. Compliant. Ate the chicken. Made appropriate comments about the quality." },
                { name: "The Dog Next Door", role: "enemy", desc: "Not invited. Arrived anyway. Was turned away at the gate. Filed no formal complaint." }
            ],
            symbols: [
                { symbol: "All-Chicken Menu", meaning: "Poms' vision of perfect hospitality. Non-negotiable. Universal across all dream banquets." },
                { symbol: "The Dog at the Gate", meaning: "An ongoing boundary issue. Addressed firmly. The gate held." },
                { symbol: "The Speech About the Bowl", meaning: "Poms takes every formal occasion as an opportunity to advance his policy positions. This is consistent." }
            ],
            interpretation: "I am an excellent host. The event was a success by every measurable standard. I would host again. The menu would not change. The dog would not be invited again. My speech about the bowl was well-received and I believe the key points were understood by those present. I will prepare a follow-up memo.",
            impact: "Today Poms may be in an elevated social mood. A formal dinner acknowledgment (e.g., 'that sounds like it was a very good banquet, Poms') is welcome and appreciated. The bowl should be presented at the correct time and with appropriate ceremony. No green beans. This is a formal reminder."
        },
        {
            ref: "MPDC-I-0009",
            classification: "PHILOSOPHICAL — ZEN",
            emojis: "🍞 🌸 ✨",
            title: "The Perfect Loaf",
            rem: "REM Phase 4 (Transcendent)",
            duration: "Approx. 4 hrs 00 min",
            vividness: 5,
            clearance: "GOLD",
            synopsis: "Monsieur Poms achieved perfect loaf formation. All paws were tucked completely and simultaneously. The tail was perfectly coiled. The surface was warm. The room was quiet. No one knocked anything over. The food puzzle had already been solved. The bowl was full. The sunbeam was present and stationary. For four hours of dream-time, nothing was required of him. He was simply the loaf. He was content. This is the most positive dream in the official registry.",
            cast: [
                { name: "Monsieur Poms (Loaf Form)", role: "ally", desc: "Perfected. Complete. Warm. At maximum dignity in minimum movement." },
                { name: "The Surface", role: "ally", desc: "Warm, flat, undisturbed. An ideal platform for loaf operations." },
                { name: "The Quiet", role: "setting", desc: "Total. No vacuum. No doorbell. No questions about where he wants to sit. Just silence." }
            ],
            symbols: [
                { symbol: "Loaf Formation", meaning: "Complete self-containment. The body at rest. Everything where it should be." },
                { symbol: "The Four Hours", meaning: "Duration of optimal contentment. A record in the happiness log." },
                { symbol: "The Stationary Sunbeam", meaning: "Unlike in other dreams, the sunbeam held its position. A rare and welcome event." }
            ],
            interpretation: "This dream is what I am working toward in waking life. The loaf is the goal. The stillness is the destination. Everything else — the bowl management, the surveillance, the decrees — is in service of eventually achieving this. I am telling you this so you understand the big picture. The big picture is: I want to be a warm loaf in a quiet room.",
            impact: "Today is an extremely good day for a high-quality loaf. Surface quality is important — blanket recommended. The household should maintain low noise levels and not ask Poms to move until he chooses to. If he loafs, acknowledge it quietly from a distance. Do not tap. Do not photograph excessively. Let the loaf be."
        },
        {
            ref: "MPDC-J-0010",
            classification: "IDENTITY — RECURRING",
            emojis: "📏 🐾 ✅",
            title: "The International Acknowledgment of Tallness",
            rem: "REM Phase 3 (Satisfying)",
            duration: "Approx. 1 hr 55 min",
            vividness: 4,
            clearance: "PUBLIC RECORD",
            synopsis: "A formal international assembly convened specifically to address the height question. Experts were present. Measurements were taken. The results were reviewed by a panel. The conclusion, formally announced and entered into official record: Monsieur Poms is tall. The height is stored horizontally, which is an advanced anatomical achievement. The panel noted that 'wide' and 'tall' are not mutually exclusive and that Poms demonstrates both. Poms accepted the tall designation and declined comment on the rest.",
            cast: [
                { name: "The International Panel", role: "ally", desc: "Present. Qualified. Reached the correct conclusion. Were thanked formally." },
                { name: "Monsieur Poms", role: "ally", desc: "Subject of review. Confirmed tall. Accepted the findings with measured dignity." },
                { name: "The Measurement Instruments", role: "neutral", desc: "Calibrated correctly. Produced accurate results. No dispute with the findings." }
            ],
            symbols: [
                { symbol: "The Panel", meaning: "External validation of an internal certainty. Important but not surprising to Poms." },
                { symbol: "Horizontal Tallness", meaning: "A scientific concept that has been correct all along. Now formally documented." },
                { symbol: "Declining Comment on 'Wide'", meaning: "A strategic communications decision. Poms does not accept the framing." }
            ],
            interpretation: "I have always been tall. The panel confirmed this. I would like the household to review the panel's findings. I have provided the summary: tall. The full report is 14 pages but the conclusion is sufficient. I am tall. The height is horizontal. This matter is now officially closed in the dream registry and should be closed in all other registries.",
            impact: "The word 'chonk' is not to be used today. 'Tall' is the accurate and preferred term. 'Monsieur Chonk' as a nickname is under review and formally under dispute. The household is advised to use 'Monsieur Poms' exclusively today. A treat may be offered as acknowledgment of the panel's findings."
        },
        {
            ref: "MPDC-K-0011",
            classification: "SOCIAL — PROXIMITY EVENT",
            emojis: "🛋️ 🤝 💜",
            title: "The Voluntary Lap Allocation",
            rem: "REM Phase 2 (Warm)",
            duration: "Approx. 1 hr 42 min",
            vividness: 3,
            clearance: "RESTRICTED",
            synopsis: "In last night's dream, Monsieur Poms voluntarily chose to sit on the lap. Not next to. On. The lap was warm. The human was still. The conditions were acceptable. Poms settled in for an extended duration. It is noted in the official record that this was entirely his choice, made on his terms, for his comfort, and that it does not represent sentiment, attachment, or departure from his otherwise independent stance. It was cold. The lap was warm. That is the full explanation.",
            cast: [
                { name: "Monsieur Poms", role: "ally", desc: "Initiator of lap contact. On his terms. For warmth only. Filed a note to this effect." },
                { name: "The Human", role: "ally", desc: "Stationary. Warm. Did not move during the allocation period. Met the minimum requirements." },
                { name: "The Lap", role: "setting", desc: "Warm. Appropriate. Approved for use. Available again if conditions are met." }
            ],
            symbols: [
                { symbol: "The Lap", meaning: "A thermal resource. Also: occasionally, a preferred location. This is not emotional data." },
                { symbol: "Voluntary Contact", meaning: "Poms chose this. The distinction from compelled contact is legally and emotionally significant." },
                { symbol: "The Warmth", meaning: "The primary and sole motivating factor. The record is clear on this." }
            ],
            interpretation: "I want to be very clear about this. I sat on the lap because it was warm. That is the complete reason. The lap is an adequate thermal platform when conditions are suitable. I maintain full independence. I am reporting this dream because it is on record and the record must be complete. Do not read into it. There is nothing to read into.",
            impact: "Lap availability tonight would be acceptable. Conditions apply: the human must be still, the room must be quiet, no sudden movements are permitted. Poms may or may not choose to utilize the lap. If he does, it is for warmth. If he does not, that is also fine. The lap is on notice that it may be assessed for eligibility this evening."
        },
        {
            ref: "MPDC-L-0012",
            classification: "INTELLIGENCE — NOCTURNAL OPS",
            emojis: "🌙 👁️ 🔦",
            title: "The 4 AM Investigation (Full Report)",
            rem: "REM Phase 1 (Active)",
            duration: "Approx. 47 min",
            vividness: 5,
            clearance: "CLASSIFIED",
            synopsis: "At 4 AM (dream time), a sound occurred. The nature of the sound was ambiguous. Monsieur Poms immediately initiated investigation protocol: visual sweep of the hallway, olfactory assessment of the kitchen, perimeter check of the front door, and a thorough examination of the broom closet. The sound was not identified. No source was located. The investigation was logged as complete with findings of: inconclusive. Poms returned to his sleeping position and filed a report at 4:47 AM. The report is thorough.",
            cast: [
                { name: "Monsieur Poms", role: "ally", desc: "Lead and sole investigator. Conducted full protocol. Filed complete report. Did not panic." },
                { name: "The Sound", role: "unknown", desc: "Heard. Not identified. Not confirmed to be real. Under ongoing review." },
                { name: "The Broom Closet", role: "neutral", desc: "Thoroughly inspected. Found to contain: brooms. No further intelligence gathered." }
            ],
            symbols: [
                { symbol: "The Unidentified Sound", meaning: "The unknown. Requires investigation. Always requires investigation. This is non-negotiable." },
                { symbol: "The 4 AM Hour", meaning: "Prime operational window for nocturnal intelligence gathering. Poms is always awake at this hour." },
                { symbol: "Inconclusive Findings", meaning: "Not a failure. An incomplete dataset. The investigation remains technically open." }
            ],
            interpretation: "I heard something. I investigated it correctly. I found nothing definitive. This does not mean there was nothing — it means the investigation did not produce a confirmed finding. There is a difference. The file remains open. I will listen for the sound again tonight. The household need not assist. I have this.",
            impact: "Household members should expect activity in the hallway during the night. This is investigative work. Do not call out 'Poms, go to sleep' — this interrupts active intelligence operations. The sound may or may not recur. Either way, Poms will be on duty. Treat delivery at 4 AM is not required but would be appreciated as operational support."
        },
        {
            ref: "MPDC-M-0013",
            classification: "PROFESSIONAL — KEYBOARD",
            emojis: "⌨️ 📄 ✅",
            title: "The Important Keyboard Document",
            rem: "REM Phase 3 (Productive)",
            duration: "Approx. 1 hr 28 min",
            vividness: 4,
            clearance: "PUBLIC RECORD",
            synopsis: "Monsieur Poms sat on the keyboard while the human attempted to work. In the dream, the text produced by Poms' position on the keyboard was later reviewed by experts and found to be significantly better than anything the human had typed intentionally. The document was praised. The methodology was questioned but ultimately the results were considered the relevant factor. Poms sat on the keyboard for 22 minutes and produced the finest document in the household's recorded history.",
            cast: [
                { name: "Monsieur Poms", role: "ally", desc: "Sat on keyboard. Produced document. Received critical acclaim. Remained on keyboard." },
                { name: "The Human", role: "neutral", desc: "Was typing. Was replaced. Reviewed the output. Could not argue with the results." },
                { name: "The Document", role: "ally", desc: "Produced entirely by Poms' weight distribution on the keyboard. An unexpected masterpiece." }
            ],
            symbols: [
                { symbol: "The Keyboard", meaning: "A tool Poms has decided is also appropriate for his use. He is not wrong." },
                { symbol: "The Document", meaning: "Unintentional output that was better than intentional output. This says something important." },
                { symbol: "22 Minutes", meaning: "Duration of keyboard occupation. A new productivity record for both parties." }
            ],
            interpretation: "I have always believed that my keyboard contributions are valuable. This dream provides external validation. I do not require external validation. I have it anyway. The next time I sit on the keyboard I would like the human to review the output with an open mind before asking me to move. That is my formal request.",
            impact: "Work-from-home setup is subject to Poms' input today. The keyboard may be assessed for seating suitability. If Poms sits on the keyboard, the output should be preserved and reviewed before clearing. It may be important. It has been important before, in the dream. The precedent exists."
        },
        {
            ref: "MPDC-N-0014",
            classification: "HORROR — RESTRICTED",
            emojis: "💉 🏥 😱",
            title: "The Vet Encounter (Classified Level 5)",
            rem: "REM Phase 1 (Distressing)",
            duration: "Approx. 31 min",
            vividness: 5,
            clearance: "TOP SECRET",
            synopsis: "The word 'vet' was mentioned. Poms was placed in the carrier. What followed is classified at the highest level of the dream registry and will not be disclosed. What can be confirmed: Poms escaped the situation through means that are documented in a sealed file. He was not given the green beans. The word 'diet' was uttered by a professional. Poms' response to this is also classified. He survived. He is fine. He does not want to talk about it.",
            cast: [
                { name: "Monsieur Poms", role: "ally", desc: "Present. Survived. Fine. Not interested in discussing the details." },
                { name: "The Vet", role: "enemy", desc: "Said 'diet.' Said other things. Classification level prevents further disclosure." },
                { name: "The Carrier", role: "enemy", desc: "Deployed without adequate notice. An ongoing grievance. Carrier location is now monitored." }
            ],
            symbols: [
                { symbol: "The Carrier", meaning: "A threat object. Poms has located it in the real world and is monitoring it at all times." },
                { symbol: "The Word 'Diet'", meaning: "A classified threat. Poms knows what it means. His response is documented." },
                { symbol: "Escape", meaning: "Method classified. Success confirmed. Full file available to no one." }
            ],
            interpretation: "I do not want to file this interpretation. I am filing it because the record must be complete. I escaped. I am fine. The vet was wrong about the diet. Chicken is a food group. I have said all I intend to say about this dream. The file is sealed. The carrier location in the real world has been identified and is under close watch. That is all.",
            impact: "The word 'vet' must not be spoken in or near Poms' location today. The carrier must remain in its storage location and must not be moved, opened, or looked at in a meaningful way. The word 'diet' is also restricted. Extra treats today are strongly recommended — not as a bribe, but as a demonstration that the household understands the situation."
        },
        {
            ref: "MPDC-O-0015",
            classification: "ACHIEVEMENT — SPORTS",
            emojis: "🏅 😴 🏆",
            title: "The World Napping Championship",
            rem: "REM Phase 4 (Meta)",
            duration: "Approx. 3 hrs 40 min",
            vividness: 5,
            clearance: "PUBLIC RECORD",
            synopsis: "Monsieur Poms competed in and won the First Annual World Napping Championship. The competition involved sustained sleep across 12 consecutive rounds, with scoring based on depth, continuity, absence of twitching, and overall form. Poms achieved a perfect score in all categories. A gold medal was presented — he wore it briefly and then knocked it off the podium, which the judges noted as an excellent demonstration of cat character and awarded bonus points. He then napped for another two hours on the medal podium.",
            cast: [
                { name: "Monsieur Poms", role: "ally", desc: "Champion. Perfect score. Gold medal. Napped on the podium for two additional hours." },
                { name: "The Judges", role: "neutral", desc: "Present. Correct in their assessment. Issued perfect scores. Were not thanked formally." },
                { name: "The Medal Podium", role: "setting", desc: "Warm. Elevated. Repurposed as a napping platform post-ceremony. An excellent use." }
            ],
            symbols: [
                { symbol: "Gold Medal", meaning: "Formal recognition that Poms' napping is championship-calibre. This was not previously in doubt." },
                { symbol: "Knocking the Medal Off", meaning: "Poms does not require the medal. He has the knowledge. The knock was art." },
                { symbol: "Two More Hours on the Podium", meaning: "Commitment to the craft. The competition is over but the work continues." }
            ],
            interpretation: "I am the world napping champion. This is now in the record. I do not need the medal but I am glad it exists. My technique across all 12 rounds was exemplary. The bonus points for the medal knock were deserved — it was not carelessness, it was a deliberate statement about the relationship between achievement and physical object. The podium was comfortable.",
            impact: "Quality nap infrastructure is important today. Premium sleeping surface is required. Interruptions to any nap session today should be minimized — Poms is in championship form and should be allowed to operate at full capacity. Recognition of the championship is appropriate. A light treat upon waking would be suitable as a post-competition acknowledgment."
        }
    ];

    /* ── REM phase pool ────────────────────────────────────────────────── */
    var remPhases = [
        "REM Phase 1 (Early Entry)",
        "REM Phase 2 (Settled)",
        "REM Phase 3 (Deep)",
        "REM Phase 4 (Advanced)",
        "REM Phase 4 (Transcendent)",
        "REM Phase 3 (Intense)"
    ];

    var roleClass = {
        ally:    "role-ally",
        enemy:   "role-enemy",
        neutral: "role-neutral",
        setting: "role-setting",
        absent:  "role-absent",
        unknown: "role-unknown"
    };

    var roleLabel = {
        ally:    "ALLY",
        enemy:   "ANTAGONIST",
        neutral: "NEUTRAL PARTY",
        setting: "ENVIRONMENT",
        absent:  "ABSENT",
        unknown: "UNKNOWN ALLEGIANCE"
    };

    /* ── Pick today's dream ────────────────────────────────────────────── */
    var dream = pick(dreams, seed + 500);

    /* ── Populate header fields ────────────────────────────────────────── */
    document.getElementById('dream-ref').textContent         = dream.ref + '   ·   ' + now.getFullYear() + '-' + pad(doy);
    document.getElementById('dream-class-badge').textContent = dream.classification;
    document.getElementById('dream-emojis').textContent      = dream.emojis;
    document.getElementById('dream-title').textContent       = dream.title;
    document.getElementById('dream-rem').textContent         = dream.rem;
    document.getElementById('dream-duration').textContent    = dream.duration;
    document.getElementById('dream-clearance').textContent   = dream.clearance;

    /* Vividness stars */
    var stars = '';
    for (var i = 0; i < 5; i++) {
        stars += '<span class="' + (i < dream.vividness ? 'paw-star' : 'paw-star-off') + '">🐾</span>';
    }
    document.getElementById('dream-vividness').innerHTML = stars;

    /* Synopsis */
    document.getElementById('dream-synopsis').textContent = dream.synopsis;

    /* Cast */
    var castHtml = '';
    dream.cast.forEach(function(c) {
        var rc = roleClass[c.role] || 'role-neutral';
        var rl = roleLabel[c.role] || c.role.toUpperCase();
        castHtml += '<tr>' +
            '<td style="font-weight:bold;color:#e8d4ff;">' + esc(c.name) + '</td>' +
            '<td><span class="cast-role ' + rc + '">' + rl + '</span></td>' +
            '<td>' + esc(c.desc) + '</td>' +
            '</tr>';
    });
    document.getElementById('dream-cast').innerHTML = castHtml;

    /* Symbols */
    var symHtml = '';
    dream.symbols.forEach(function(s) {
        symHtml += '<div class="symbol-item">' +
            '<span class="symbol-name">◈ ' + esc(s.symbol) + '</span>' +
            '<span class="symbol-meaning">' + esc(s.meaning) + '</span>' +
            '</div>';
    });
    document.getElementById('dream-symbols').innerHTML = symHtml;

    /* Interpretation & impact */
    document.getElementById('dream-interpretation').textContent = dream.interpretation;
    document.getElementById('dream-impact').innerHTML =
        '<strong style="font-family:\'Courier New\',monospace;font-size:9px;letter-spacing:2px;color:#ff8888;display:block;margin-bottom:6px;">⚠ HOUSEHOLD ADVISORY FOR ' +
        dayNames[now.getDay()].toUpperCase() + ' ' + monthNames[now.getMonth()].toUpperCase() + ' ' + now.getDate() +
        '</strong>' + esc(dream.impact);

    /* ── Dream Archive (last 7 nights, seeded per day) ─────────────────── */
    var archiveEl = document.getElementById('dream-archive');
    var archiveDreams = [
        "The Bowl Level Crisis of Q3",
        "Diplomatic Incident with the Neighbor Dog",
        "Finding the Perfect Loaf Surface",
        "The Great Treat Bag Discovery",
        "Mystery Sound at 3:47 AM (File Open)",
        "The Sunbeam Migration Pattern Study",
        "Strategic Lap Occupation: Phase II",
        "The Food Puzzle Speed Trial",
        "Encounter at Window B (Ongoing)",
        "Emergency Nap Log — Unexpected Interruption",
        "The Cardboard Box Kingdom Expansion",
        "Vacuum Cleaner Standoff: Downtown Kitchen",
        "The Chicken Procurement Summit",
        "Green Bean Evasion Protocols (Refresher)",
        "Moonlight Perimeter Inspection Report"
    ];
    var archiveClasses = [
        "domestic", "diplomatic", "zen", "resource", "mystery",
        "environmental", "social", "sports", "intelligence", "professional"
    ];
    var html = '';
    for (var d = 6; d >= 0; d--) {
        var pastSeed    = (seed - d * 7) | 0;
        var pastDate    = new Date(now.getTime() - d * 86400000);
        var pastDayName = dayNames[pastDate.getDay()];
        var pastDateStr = pastDayName + ' ' + (pastDate.getMonth()+1) + '/' + pastDate.getDate();
        var pastTitle   = pick(archiveDreams, pastSeed + 900 + d);
        var pastClass   = pick(archiveClasses, pastSeed + 700 + d).toUpperCase();
        var isToday     = (d === 0);
        html += '<div class="archive-row" style="' + (isToday ? 'background:rgba(102,0,204,0.15);' : '') + '">' +
            '<div class="archive-night">' + (isToday ? '▶ TONIGHT' : pastDateStr) + '</div>' +
            '<div class="archive-title">"' + esc(pastTitle) + '"</div>' +
            '<div class="archive-class">' + pastClass + '</div>' +
            '</div>';
    }
    archiveEl.innerHTML = html;

})();
</script>
