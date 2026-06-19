---
title: "Security Briefing"
---

<style>
.mphsd-wrapper {
    background: #000;
    color: #00CC00;
    font-family: 'Courier New', monospace;
    border: 3px solid #00AA00;
    margin-bottom: 20px;
    overflow: hidden;
}

.mphsd-header {
    background: linear-gradient(to bottom, #001800, #002600);
    text-align: center;
    padding: 18px 10px 14px;
    border-bottom: 3px solid #00AA00;
}

.mphsd-logo-text {
    font-size: 9px;
    letter-spacing: 3px;
    color: #005500;
    margin-bottom: 6px;
    text-transform: uppercase;
}

.mphsd-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 26px;
    letter-spacing: 6px;
    color: #00FF00;
    text-shadow: 0 0 12px rgba(0,255,0,0.5), 2px 2px 0 #000;
}

.mphsd-subtitle {
    font-size: 10px;
    letter-spacing: 3px;
    color: #009900;
    margin-top: 5px;
}

.mphsd-live-badge {
    display: inline-block;
    background: #CC0000;
    color: #FFF;
    font-family: 'Impact', sans-serif;
    font-size: 10px;
    letter-spacing: 2px;
    padding: 2px 6px;
    margin-left: 8px;
    animation: liveBlink 1.1s step-end infinite;
    vertical-align: middle;
}

@keyframes liveBlink {
    0%, 100% { opacity: 1; }
    50%       { opacity: 0; }
}

.mphsd-ticker {
    background: #001100;
    border-top: 1px solid #004400;
    border-bottom: 1px solid #004400;
    padding: 4px 0;
    overflow: hidden;
    white-space: nowrap;
    font-size: 10px;
    color: #00CC00;
}

.mphsd-ticker-inner {
    display: inline-block;
    animation: mphsdTicker 32s linear infinite;
}

@keyframes mphsdTicker {
    from { transform: translateX(100%); }
    to   { transform: translateX(-100%); }
}

.mphsd-section-header {
    background: #002200;
    border-top: 1px solid #00AA00;
    border-bottom: 1px solid #004400;
    padding: 6px 12px;
    font-size: 10px;
    letter-spacing: 4px;
    color: #00FF00;
    text-transform: uppercase;
}

/* Camera grid */
.cam-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4px;
    padding: 10px;
    background: #000;
}

.cam-screen {
    position: relative;
    height: 88px;
    background: #000d00;
    overflow: hidden;
    border: 1px solid #004400;
}

.cam-scanlines {
    position: absolute;
    top: 0; left: 0; right: 0; bottom: 0;
    background: repeating-linear-gradient(
        0deg,
        rgba(0,0,0,0)    0px,
        rgba(0,0,0,0)    1px,
        rgba(0,0,0,0.35) 1px,
        rgba(0,0,0,0.35) 2px
    );
    pointer-events: none;
    z-index: 2;
}

.cam-sweep {
    position: absolute;
    top: -3px;
    left: 0;
    right: 0;
    height: 3px;
    background: linear-gradient(to bottom, rgba(0,255,0,0.12), transparent);
    animation: camSweep 3.5s linear infinite;
    z-index: 3;
}

@keyframes camSweep {
    from { top: -3px; }
    to   { top: 100%; }
}

.cam-label {
    position: absolute;
    top: 5px;
    left: 5px;
    font-size: 7px;
    color: #00FF00;
    letter-spacing: 1px;
    z-index: 4;
    text-shadow: 0 0 4px rgba(0,255,0,0.9);
}

.cam-status-text {
    position: absolute;
    bottom: 5px;
    left: 5px;
    font-size: 7px;
    letter-spacing: 1px;
    z-index: 4;
}

.cam-ts {
    position: absolute;
    bottom: 5px;
    right: 5px;
    font-size: 7px;
    color: #004400;
    z-index: 4;
}

.cam-rec-dot {
    position: absolute;
    top: 5px;
    right: 5px;
    width: 5px;
    height: 5px;
    background: #FF0000;
    border-radius: 50%;
    z-index: 4;
    animation: liveBlink 1.1s step-end infinite;
}

.cam-icon {
    position: absolute;
    font-size: 24px;
    z-index: 1;
    opacity: 0.45;
    filter: grayscale(1) brightness(0.45) sepia(1) hue-rotate(90deg) saturate(3);
}

/* Threat level */
.threat-display {
    background: #001100;
    border: 2px solid #006600;
    padding: 14px;
    margin: 10px;
}

.threat-labels {
    display: flex;
    justify-content: space-between;
    font-size: 8px;
    color: #004400;
    letter-spacing: 1px;
    margin-bottom: 5px;
    text-transform: uppercase;
}

.threat-bar-outer {
    height: 20px;
    background: #000;
    border: 2px inset #004400;
    overflow: hidden;
}

.threat-bar-fill {
    height: 100%;
    animation: threatGrow 1.4s ease-out forwards;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: flex-end;
}

@keyframes threatGrow { from { width: 0%; } }

.threat-bar-fill-label {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 10px;
    letter-spacing: 2px;
    color: #000;
    padding-right: 8px;
    white-space: nowrap;
}

.threat-name-display {
    text-align: center;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 22px;
    letter-spacing: 5px;
    margin-top: 10px;
    text-shadow: 0 0 16px currentColor;
}

.threat-description {
    font-size: 10px;
    color: #009900;
    text-align: center;
    margin-top: 6px;
    line-height: 1.65;
}

/* Suspect dossier */
.suspect-card {
    border: 2px solid #00AA00;
    background: #001100;
    margin: 10px;
    padding: 14px;
    overflow: hidden;
}

.suspect-mugshot {
    float: left;
    width: 68px;
    height: 68px;
    background: #002200;
    border: 2px solid #009900;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 30px;
    margin-right: 12px;
    position: relative;
    overflow: hidden;
}

.suspect-mugshot::after {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0; bottom: 0;
    background: repeating-linear-gradient(0deg, rgba(0,0,0,0), rgba(0,0,0,0) 1px, rgba(0,0,0,0.3) 1px, rgba(0,0,0,0.3) 2px);
    pointer-events: none;
}

.suspect-meta {
    font-size: 10px;
    color: #00BB00;
    line-height: 1.8;
}

.suspect-name-display {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 15px;
    letter-spacing: 3px;
    color: #00FF00;
    margin-bottom: 3px;
}

.suspect-clearfix { clear: both; }

.suspect-assessment-box {
    margin-top: 10px;
    font-size: 10px;
    color: #009900;
    line-height: 1.7;
    border-top: 1px dashed #004400;
    padding-top: 8px;
}

/* Incident log */
.incident-log-wrap {
    padding: 0 10px 10px;
}

.incident-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 10px;
}

.incident-table th {
    background: #002200;
    color: #00FF00;
    padding: 5px 7px;
    text-align: left;
    font-size: 9px;
    letter-spacing: 2px;
    text-transform: uppercase;
    border-bottom: 1px solid #005500;
}

.incident-table td {
    padding: 5px 7px;
    border-bottom: 1px solid #002200;
    vertical-align: top;
    color: #00AA00;
    line-height: 1.5;
}

.incident-table tr:nth-child(even) td { background: #000800; }
.sev-high { color: #FF5555 !important; }
.sev-med  { color: #FFAA00 !important; }
.sev-low  { color: #00AA00; }

/* Sector grid */
.sector-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 6px;
    padding: 10px;
}

.sector-cell {
    background: #001100;
    border: 1px solid #004400;
    padding: 8px 10px;
}

.sector-cell-name {
    font-size: 9px;
    letter-spacing: 2px;
    color: #00FF00;
    margin-bottom: 4px;
    text-transform: uppercase;
}

.sector-cell-status {
    font-size: 9px;
    color: #009900;
    line-height: 1.5;
}

/* Recommendation + field notes */
.rec-box {
    background: #001800;
    border: 2px solid #00FF00;
    padding: 14px;
    margin: 10px;
    font-size: 11px;
    color: #00EE00;
    line-height: 1.8;
    box-shadow: inset 0 0 20px rgba(0,100,0,0.15);
}

.rec-box-label {
    font-size: 9px;
    letter-spacing: 3px;
    margin-bottom: 8px;
    color: #007700;
    border-bottom: 1px dashed #004400;
    padding-bottom: 5px;
    text-transform: uppercase;
}

.field-notes-box {
    background: #001100;
    border: 2px solid #006600;
    border-left: 6px solid #00FF00;
    padding: 14px;
    margin: 10px;
    font-size: 11px;
    color: #00CC00;
    line-height: 1.8;
    font-style: italic;
}

.field-notes-label {
    font-size: 9px;
    letter-spacing: 2px;
    color: #005500;
    margin-bottom: 8px;
    font-style: normal;
    text-transform: uppercase;
}

.field-notes-sig {
    text-align: right;
    font-size: 9px;
    color: #005500;
    margin-top: 8px;
    font-style: normal;
}

.mphsd-auth-footer {
    background: #001100;
    border-top: 2px solid #004400;
    padding: 10px 12px;
    font-size: 9px;
    color: #005500;
    text-align: center;
    line-height: 1.9;
    letter-spacing: 1px;
}
</style>

<div class="mphsd-wrapper">

<!-- HEADER -->
<div class="mphsd-header">
    <div class="mphsd-logo-text">MPHSD &mdash; EST. 2010 &mdash; CARDBOARD BOX COMMAND CENTER &mdash; POMS AUTHORIZED ACCESS ONLY</div>
    <div class="mphsd-title">&#128062; HOUSEHOLD SECURITY &#128062;</div>
    <div style="font-family: 'Georgia', serif; font-size: 12px; color: #00BB00; letter-spacing: 1px; margin: 4px 0;">
        Monsieur Poms Household Security Division
    </div>
    <div class="mphsd-subtitle">
        CHIEF SURVEILLANCE OFFICER: M. POMS
        <span class="mphsd-live-badge">&#9679; LIVE</span>
    </div>
    <div style="font-size: 9px; color: #005500; margin-top: 6px; letter-spacing: 2px;">
        DAILY BRIEFING &mdash; <span id="sec-date"></span> &mdash; REPORT NO. <span id="sec-report-num"></span>
    </div>
</div>

<!-- TICKER -->
<div class="mphsd-ticker">
    <span class="mphsd-ticker-inner">
        &nbsp;&nbsp;&nbsp; &#9889; MPHSD LIVE INTELLIGENCE FEED &nbsp;|&nbsp; ALL SECTORS UNDER ACTIVE SURVEILLANCE &nbsp;|&nbsp; CHIEF POMS: ON DUTY &nbsp;|&nbsp; VACUUM THREAT LEVEL: MONITORED &nbsp;|&nbsp; WINDOW POSTS: OCCUPIED &nbsp;|&nbsp; TREAT SITUATION: CRITICAL &nbsp;|&nbsp; SQUIRREL ACTIVITY: REPORTED &nbsp;|&nbsp; GREEN BEAN THREAT: ONGOING AND UNACCEPTABLE &nbsp;|&nbsp; DO NOT APPROACH THE CHIEF DURING ACTIVE STARING OPERATIONS &nbsp;&nbsp;&nbsp;
    </span>
</div>

<!-- CAMERA GRID -->
<div class="mphsd-section-header">&#128249; LIVE CAMERA FEEDS &mdash; HOUSEHOLD PERIMETER</div>
<div class="cam-grid">
    <div class="cam-screen">
        <div class="cam-scanlines"></div>
        <div class="cam-sweep"></div>
        <div class="cam-rec-dot"></div>
        <div class="cam-label">CAM-1 // WINDOW POST ALPHA</div>
        <div class="cam-status-text" id="cam1-status">&#8212;</div>
        <div class="cam-ts" id="cam1-ts">&#8212;</div>
        <div class="cam-icon" style="bottom: 14px; left: 50%; transform: translateX(-50%);">&#128049;</div>
    </div>
    <div class="cam-screen">
        <div class="cam-scanlines"></div>
        <div class="cam-sweep" style="animation-delay: -1.4s;"></div>
        <div class="cam-rec-dot"></div>
        <div class="cam-label">CAM-2 // KITCHEN PERIMETER</div>
        <div class="cam-status-text" id="cam2-status">&#8212;</div>
        <div class="cam-ts" id="cam2-ts">&#8212;</div>
        <div class="cam-icon" style="bottom: 14px; right: 8px;">&#127859;</div>
    </div>
    <div class="cam-screen">
        <div class="cam-scanlines"></div>
        <div class="cam-sweep" style="animation-delay: -0.7s;"></div>
        <div class="cam-rec-dot"></div>
        <div class="cam-label">CAM-3 // MAIN CORRIDOR</div>
        <div class="cam-status-text" id="cam3-status">&#8212;</div>
        <div class="cam-ts" id="cam3-ts">&#8212;</div>
        <div class="cam-icon" style="bottom: 14px; left: 12px;">&#129510;</div>
    </div>
    <div class="cam-screen">
        <div class="cam-scanlines"></div>
        <div class="cam-sweep" style="animation-delay: -2.1s;"></div>
        <div class="cam-rec-dot"></div>
        <div class="cam-label">CAM-4 // FRONT DOOR APPROACH</div>
        <div class="cam-status-text" id="cam4-status">&#8212;</div>
        <div class="cam-ts" id="cam4-ts">&#8212;</div>
        <div class="cam-icon" style="bottom: 14px; right: 10px;">&#128230;</div>
    </div>
</div>

<!-- THREAT LEVEL -->
<div class="mphsd-section-header">&#9888; CURRENT THREAT ASSESSMENT</div>
<div class="threat-display">
    <div class="threat-labels">
        <span>MELLOW</span>
        <span>ELEVATED</span>
        <span>HIGH POOF</span>
        <span>YOWL ALERT</span>
        <span>DEFCON ZOOMIES</span>
    </div>
    <div class="threat-bar-outer">
        <div class="threat-bar-fill" id="threat-bar-fill">
            <span class="threat-bar-fill-label" id="threat-bar-label">&#8212;</span>
        </div>
    </div>
    <div class="threat-name-display" id="threat-name">&#8212;</div>
    <div class="threat-description" id="threat-desc">&#8212;</div>
</div>

<!-- PRIMARY SUSPECT -->
<div class="mphsd-section-header">&#128269; TODAY'S PRIMARY SUBJECT OF INTEREST</div>
<div class="suspect-card">
    <div class="suspect-mugshot"><span id="suspect-icon">?</span></div>
    <div class="suspect-meta">
        <div class="suspect-name-display" id="suspect-name">LOADING&hellip;</div>
        <div><strong>Classification:</strong> <span id="suspect-class">&#8212;</span></div>
        <div><strong>Threat Vector:</strong> <span id="suspect-vector">&#8212;</span></div>
        <div><strong>Last Observed:</strong> <span id="suspect-last">&#8212;</span></div>
        <div><strong>Status:</strong> <span id="suspect-status">&#8212;</span></div>
    </div>
    <div class="suspect-clearfix"></div>
    <div class="suspect-assessment-box">
        <strong style="color: #00FF00;">CHIEF'S ASSESSMENT:</strong><br>
        <span id="suspect-assessment">&#8212;</span>
    </div>
</div>

<!-- INCIDENT LOG -->
<div class="mphsd-section-header">&#128203; TODAY'S INCIDENT LOG</div>
<div class="incident-log-wrap">
    <table class="incident-table">
        <thead>
            <tr>
                <th style="width: 14%;">TIME</th>
                <th style="width: 14%;">SEVERITY</th>
                <th style="width: 22%;">SECTOR</th>
                <th>INCIDENT DESCRIPTION</th>
            </tr>
        </thead>
        <tbody id="incident-tbody"></tbody>
    </table>
</div>

<!-- SECTOR STATUS -->
<div class="mphsd-section-header">&#128506; SECTOR STATUS &mdash; FULL PERIMETER REPORT</div>
<div class="sector-grid">
    <div class="sector-cell">
        <div class="sector-cell-name">&#9632; WINDOW POST ALPHA</div>
        <div class="sector-cell-status" id="sector-window">&#8212;</div>
    </div>
    <div class="sector-cell">
        <div class="sector-cell-name">&#9632; KITCHEN PERIMETER</div>
        <div class="sector-cell-status" id="sector-kitchen">&#8212;</div>
    </div>
    <div class="sector-cell">
        <div class="sector-cell-name">&#9632; MAIN CORRIDOR</div>
        <div class="sector-cell-status" id="sector-corridor">&#8212;</div>
    </div>
    <div class="sector-cell">
        <div class="sector-cell-name">&#9632; FRONT DOOR APPROACH</div>
        <div class="sector-cell-status" id="sector-front">&#8212;</div>
    </div>
    <div class="sector-cell">
        <div class="sector-cell-name">&#9632; ELEVATED OBS. PLATFORM</div>
        <div class="sector-cell-status" id="sector-elevated">&#8212;</div>
    </div>
    <div class="sector-cell">
        <div class="sector-cell-name">&#9632; OUTDOOR ZONE (WINDOW)</div>
        <div class="sector-cell-status" id="sector-outdoor">&#8212;</div>
    </div>
</div>

<!-- OFFICIAL RECOMMENDATION -->
<div class="mphsd-section-header">&#128204; CHIEF'S OFFICIAL RECOMMENDATION</div>
<div class="rec-box">
    <div class="rec-box-label">MPHSD DIRECTIVE &mdash; FOR HOUSEHOLD DISTRIBUTION &mdash; DO NOT SHARE WITH THE VACUUM</div>
    <span id="sec-recommendation">&#8212;</span>
</div>

<!-- FIELD NOTES -->
<div class="mphsd-section-header">&#128062; CHIEF POMS &mdash; PERSONAL FIELD NOTES (CLASSIFIED)</div>
<div class="field-notes-box">
    <div class="field-notes-label">Field notes &mdash; dictated to self &mdash; for internal review only</div>
    &ldquo;<span id="sec-field-notes">&#8212;</span>&rdquo;
    <div class="field-notes-sig">
        &mdash; M. Poms, Chief Surveillance Officer, MPHSD &nbsp;|&nbsp; <span id="sec-date2"></span>
    </div>
</div>

<!-- AUTH FOOTER -->
<div class="mphsd-auth-footer">
    BRIEFING AUTHENTICATED BY DIRECT PAW CONTACT &bull; CLEARANCE LEVEL: TOP SECRET (CHICKEN) &bull; REPORT NO. <span id="sec-report-footer">&#8212;</span><br>
    THIS BRIEFING IS VALID FOR THE CURRENT CALENDAR DAY ONLY &bull; NEW ASSESSMENT ISSUED EACH MORNING AT 00:00<br>
    <em>MPHSD accepts no liability for missed threats, unauthorized vacuuming, or squirrel-related incidents outside assessed parameters.</em>
</div>

</div>

<script>
(function () {

    function seededRand(s) {
        var x = Math.sin(s * 127.1 + 311.7) * 43758.5453123;
        return x - Math.floor(x);
    }
    function pick(arr, s) { return arr[Math.floor(seededRand(s) * arr.length)]; }
    function esc(s) { return String(s).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;'); }

    var now  = new Date();
    var doy  = Math.floor((now - new Date(now.getFullYear(), 0, 0)) / 86400000);
    var seed = now.getFullYear() * 1000 + doy;

    var dayNames   = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
    var monthNames = ["January","February","March","April","May","June","July","August","September","October","November","December"];
    var dateStr    = dayNames[now.getDay()] + ", " + monthNames[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear();
    var h = now.getHours(), m = now.getMinutes();
    var timeStr    = (h < 10 ? '0' + h : h) + ':' + (m < 10 ? '0' + m : m);

    document.getElementById('sec-date').textContent  = dateStr;
    document.getElementById('sec-date2').textContent = dateStr;

    var reportNum = "MPHSD-" + now.getFullYear() + "-" + String(doy).padStart(3, '0') + "-" + String(Math.floor(seededRand(seed + 333) * 9000) + 1000);
    document.getElementById('sec-report-num').textContent    = reportNum;
    document.getElementById('sec-report-footer').textContent = reportNum;

    // ── Threat levels ─────────────────────────────────────────────────────────
    var threats = [
        {
            name: "MELLOW",
            pct: 10,
            color: "#00CC00",
            desc: "All sectors quiet. Primary threat (the vacuum) is confirmed stationary in the hall closet. Optimal nap deployment window is currently active. The Chief has been informed and has assumed a horizontal position."
        },
        {
            name: "ELEVATED",
            pct: 30,
            color: "#99DD00",
            desc: "Anomalous activity has been flagged in the kitchen sector. Possible unauthorized can opener usage detected via acoustic intelligence. The Chief is monitoring the situation from an elevated observation post with one eye open."
        },
        {
            name: "HIGH POOF",
            pct: 55,
            color: "#FFAA00",
            desc: "Multiple incidents logged this operational period. Tail puff index currently at 60%. The Chief has suspended napping operations and is conducting active perimeter surveillance from Window Post Alpha. Approach with caution."
        },
        {
            name: "YOWL ALERT",
            pct: 78,
            color: "#FF6600",
            desc: "A significant threat has triggered full vocalization protocol. Two formal complaints have been broadcast via meow. All sectors under heightened observation. Household members have been briefed involuntarily via proximity."
        },
        {
            name: "DEFCON ZOOMIES",
            pct: 97,
            color: "#FF2222",
            desc: "MAXIMUM ALERT. A threat of unknown origin has triggered the Chief's full emergency response. Rapid deployment across all sectors is currently underway. Do NOT attempt to intercept or redirect the Chief at this time. Stand clear of all corridors."
        }
    ];

    // ── Suspects ──────────────────────────────────────────────────────────────
    var suspects = [
        {
            name: "THE VACUUM CLEANER",
            icon: "🌀",
            classification: "Domestic Threat — Class 1 (Longstanding, Unresolved)",
            vector: "Acoustic disruption, suction proximity, unpredictable mobilization schedule",
            last: "Last confirmed in hall closet — current status unverified and concerning",
            status: "ACTIVE FILE — UNDER CONTINUOUS MONITORING",
            assessment: "The Vacuum remains the most consistent threat in the Chief's operational history. Despite formal objections filed since 2022, it continues to be deployed at irregular intervals with no advance notice. A restraining order has been drafted but remains unexecuted due to a lack of legal claw-print certification."
        },
        {
            name: "THE MAIL CARRIER",
            icon: "📬",
            classification: "External Threat — Category: Daily Perimeter Aggressor",
            vector: "Predictable approach schedule, letterbox breach, premature departure before interrogation",
            last: "Approximately 10:30 AM — departed south on foot without debriefing",
            status: "RECURRING — DAILY PATTERN ESTABLISHED, MOTIVE UNKNOWN",
            assessment: "Subject approaches the front door each day at consistent intervals, inserts objects into the letterbox, and departs before the Chief can complete a proper identification. The motivation for this behavior remains unclear. The Chief has memorized the sound of their footsteps and considers this an ongoing act of evasion."
        },
        {
            name: "SQUIRREL UNIT ALPHA",
            icon: "🐿️",
            classification: "External Wildlife — Territorial Aggressor, Repeat Offender",
            vector: "Window post trespassing, unauthorized garden access, suspicious nut relocation",
            last: "Last observed at Window Post Alpha — departed east into the large tree",
            status: "AT LARGE — 14 CONFIRMED PERIMETER VIOLATIONS ON RECORD",
            assessment: "Squirrel Unit Alpha has been documented violating the outer perimeter on at least 14 confirmed occasions this season. The Chief has issued 14 corresponding tail-puff responses and 6 vocalized warnings. The squirrel continues to show no remorse. An escalation package is being prepared for submission to the relevant wildlife authorities."
        },
        {
            name: "THE DELIVERY DRIVER",
            icon: "📦",
            classification: "External Threat — Category: Surprise Arrival, High Disruption",
            vector: "Unscheduled perimeter approach, doorbell activation, package drop, rapid unauthorized retreat",
            last: "Vehicle observed outside for 4 minutes — no advance warning given whatsoever",
            status: "INTERMITTENT — HIGH DISRUPTION SCORE — PACKAGES PENDING CLEARANCE",
            assessment: "Subject arrives without clearance, activates the doorbell (a known acoustic disturbance), drops an unidentified package at the perimeter, and retreats before the Chief can conduct a thorough inspection. Each package requires approximately 6 minutes of dedicated sniffing to clear. The Chief has not yet been satisfied with any of them."
        },
        {
            name: "THE NEIGHBOR'S DOG",
            icon: "🐕",
            classification: "External Wildlife — Noise Pollution, Territorial Confusion, Ongoing",
            vector: "Auditory aggression, unsolicited barking, visible presence from Window Post Alpha",
            last: "Visible from Window Post Alpha at approximately 2:15 PM — unacceptably cheerful",
            status: "ACTIVE — FORMAL COMPLAINT FILED, RESPONSE PENDING",
            assessment: "Subject is large, loud, and operates as if exterior territory is uncontested. This is factually incorrect. The Chief has logged 3.5 accumulated hours of staring at the dog this week and considers the matter clearly communicated. The dog has not acknowledged the stare. The Chief has not finished staring."
        },
        {
            name: "THE GHOST SOCK",
            icon: "🧦",
            classification: "Internal Anomaly — Category: Unexplained Textile Event",
            vector: "Unexplained corridor appearance, suspicious stillness, persistent refusal to explain itself",
            last: "Discovered in Main Corridor at 07:22 AM — has not moved, has not spoken",
            status: "UNDER ACTIVE INVESTIGATION — BATTING PROTOCOL DEPLOYED",
            assessment: "A lone sock of unknown origin appeared in the corridor this morning. It has been stared at for over 40 minutes. It has not provided an account of itself. The Chief conducted a preliminary batting investigation which yielded no conclusive intelligence. The sock remains at large, technically speaking, in that it continues to exist."
        },
        {
            name: "THE BROOM",
            icon: "🧹",
            classification: "Domestic Threat — Category: Unexpected Mobilization Event",
            vector: "Unpredictable deployment timing, bristle proximity, sweeping operations near designated loaf zone",
            last: "Mobilized in kitchen at 10:15 AM — currently leaned against wall, status: provisional",
            status: "NEUTRALIZED (PROVISIONAL) — MONITORING CONTINUES INDEFINITELY",
            assessment: "The Broom was mobilized this morning without any advance briefing to the Chief. It swept within 0.8 metres of the designated loaf zone before operations ceased. An informal protest has been filed. The Broom is currently resting against the kitchen wall in what the Chief describes as a 'suspicious posture.' It is being watched."
        },
        {
            name: "THE BIRD (WINDOW POST B)",
            icon: "🐦",
            classification: "External Wildlife — Aerial Territorial Aggressor, Serial Offender",
            vector: "Window ledge occupation, chirping aggression, apparent mockery of ground-based surveillance",
            last: "Occupied external window ledge for 22 minutes — departed northwest without authorization",
            status: "INTERMITTENT — PROVOCATION ON RECORD, DETERRENCE CLAIMED",
            assessment: "A bird of medium size and significant audacity occupied the external window ledge this morning. The Chief responded with an elevated chitter response and full tail deployment. The bird departed at approximately 10:03. The Chief has logged this as a successful deterrence operation. The bird has not yet confirmed this interpretation, which the Chief finds telling."
        },
        {
            name: "THE PHANTOM CAN OPENER",
            icon: "🥫",
            classification: "Acoustic Signal — Category: High Priority, Immediate Response Required",
            vector: "Irregular can opener sound events, correlation with Poms' rapid tactical repositioning",
            last: "Sound event detected at 17:30 — source confirmed as kitchen, content: classified",
            status: "ACTIVE SIGNAL — IMMEDIATE RESPONSE DEPLOYED, OUTCOME PENDING",
            assessment: "Acoustic intelligence detected a can opener activation event this operational period. The Chief's response was immediate, highly professional, and involved appearing in the kitchen at top speed before the event had fully resolved. Whether the can opener yielded relevant strategic intelligence (i.e. chicken) remains classified at the Chief's personal discretion."
        },
        {
            name: "THE VISITING HUMAN",
            icon: "👤",
            classification: "External Contact — Unvetted Household Entrant, Provisional Threat",
            vector: "Unknown scent profile, unexpected petting approach, failure to read the room accurately",
            last: "Arrived at 15:00 — sat on the couch — made prolonged and unearned eye contact",
            status: "UNDER OBSERVATION — TRUST VERDICT PENDING (PROVISIONAL: 2/10)",
            assessment: "An unscheduled human entered the premises this operational period. The Chief conducted an initial distance assessment of approximately 2.3 metres from the hallway. The subject sat down without formal authorization. After 18 minutes of observation, the Chief has tentatively assigned a provisional trust rating of 2 out of 10. A sniff-based clearance hearing has not yet been scheduled."
        }
    ];

    // ── Camera statuses ───────────────────────────────────────────────────────
    var camStatuses = [
        { text: "CLEAR",           color: "#00FF00" },
        { text: "MONITORING",      color: "#99DD00" },
        { text: "MOTION DETECTED", color: "#FFAA00" },
        { text: "INCIDENT LOGGED", color: "#FF8800" },
        { text: "THREAT DETECTED", color: "#FF4444" },
        { text: "NOMINAL",         color: "#009900" },
        { text: "SUSPICIOUS",      color: "#FFDD00" }
    ];

    // ── All incidents pool ────────────────────────────────────────────────────
    var allIncidents = [
        { time: "06:14", sev: "LOW",  sector: "BEDROOM",       desc: "Chief completed pre-shift stretch routine. Duration: 11 minutes. Yawn confirmed. Operations formally initiated for the day." },
        { time: "07:22", sev: "MED",  sector: "CORRIDOR",      desc: "Unidentified fabric entity (sock) discovered in main corridor. Staring protocol activated. Batting investigation conducted. Result: inconclusive." },
        { time: "08:05", sev: "LOW",  sector: "KITCHEN",       desc: "Morning food bowl audit conducted. Rating: Inadequate. Formal vocal complaint issued at elevated volume. Household member notified involuntarily." },
        { time: "08:47", sev: "LOW",  sector: "KITCHEN",       desc: "Second bowl inspection. Contents unchanged from first audit. A further vocalized statement was delivered. Bowl status: still insufficient." },
        { time: "09:14", sev: "LOW",  sector: "WINDOW POST A", desc: "Chief assumed surveillance position at Window Post Alpha. Exterior territory assessment commenced. Tail at rest. Weather: noted. Squirrel count: zero (so far)." },
        { time: "09:38", sev: "MED",  sector: "WINDOW POST A", desc: "Squirrel Unit Alpha detected at outer perimeter. Chitter response deployed at maximum intensity. Squirrel showed no immediate sign of retreat. Staring escalation initiated." },
        { time: "10:15", sev: "HIGH", sector: "KITCHEN",       desc: "Broom mobilized without advance notice to the Chief. Rapid relocation to elevated observation post executed. Threat neutralized after 4 minutes. Formal complaint: drafted and filed." },
        { time: "10:32", sev: "LOW",  sector: "LIVING ROOM",   desc: "Sunbeam located on living room floor. Occupation commenced per standard territorial protocol. Beam quality rated: Acceptable to Good. The Chief is satisfied, provisionally." },
        { time: "11:05", sev: "MED",  sector: "FRONT APPROACH",desc: "Mail carrier approached and breached front perimeter via letterbox. Chief monitored from corridor position. Carrier departed without interview. Investigation: ongoing." },
        { time: "11:47", sev: "LOW",  sector: "CORRIDOR",      desc: "Nap session initiated in a corridor sunbeam. Duration: 47 minutes. Quality: satisfactory. No incidents recorded during this window. One of the better 47 minutes on record." },
        { time: "13:22", sev: "HIGH", sector: "FRONT APPROACH",desc: "Delivery vehicle approached. Doorbell activated. Package deposited at perimeter without clearance. Chief deployed full sniffing protocol. Contents: cardboard (suspicious). Verdict: pending." },
        { time: "14:09", sev: "LOW",  sector: "LIVING ROOM",   desc: "Household member watched television at an unrequested volume. Chief observed screen for 6 minutes, determined content irrelevant to security operations, and relocated to the kitchen." },
        { time: "14:55", sev: "MED",  sector: "WINDOW POST A", desc: "Bird occupied external window ledge without authorization. Chief responded with full chitter battery. Bird departed at 15:03. Logged as successful deterrence. Bird's perspective unconfirmed." },
        { time: "15:30", sev: "LOW",  sector: "KITCHEN",       desc: "Afternoon food bowl inspection. Status: still below required levels. Three formal statements delivered. Situation partially resolved via treat substitution. The Chief is dissatisfied but fed." },
        { time: "16:44", sev: "MED",  sector: "LIVING ROOM",   desc: "Visiting human confirmed on premises. Chief performed observation from 2.3m. Subject sat on couch without authorization. Trust rating assigned: 2/10. Verdict: still pending." },
        { time: "17:30", sev: "HIGH", sector: "KITCHEN",       desc: "Can opener event detected via acoustic monitoring. Chief responded at maximum speed. Arrived before the situation had fully resolved. Content secured. Operation status: classified." },
        { time: "18:02", sev: "LOW",  sector: "ALL SECTORS",   desc: "Evening patrol completed. All sectors checked. Vacuum confirmed stationary. Chief has assumed loaf position on couch. Situation stable. This is a professional assessment." },
        { time: "20:14", sev: "LOW",  sector: "BEDROOM",       desc: "Pre-sleep territory negotiation commenced on the bed. Optimal position secured. Household member reminded of their subordinate spatial claim via strategic occupancy." },
        { time: "02:47", sev: "HIGH", sector: "ALL SECTORS",   desc: "Spontaneous zoomies event. Cause: officially unknown. Duration: approximately 4 minutes. Several items briefly displaced. The Chief has no comment on this and will not be taking questions." }
    ];

    function pickIncidents(arr, s, count) {
        var shuffled = arr.slice();
        for (var i = shuffled.length - 1; i > 0; i--) {
            var j = Math.floor(seededRand(s + i * 17) * (i + 1));
            var tmp = shuffled[i]; shuffled[i] = shuffled[j]; shuffled[j] = tmp;
        }
        return shuffled.slice(0, count).sort(function(a, b) { return a.time < b.time ? -1 : 1; });
    }

    // ── Sector statuses ───────────────────────────────────────────────────────
    var sectorStatuses = [
        "ALL CLEAR — No incidents recorded in this sector during the current operational period.",
        "MONITORING — Routine observation active. No confirmed threats at this time. Chief is watching.",
        "INCIDENT LOGGED — One or more incidents recorded. See incident log for full details and timestamp.",
        "SUSPICIOUS ACTIVITY — Unexplained movement detected. Nature of activity under investigation.",
        "THREAT PRESENT — Subject identified in sector. Chief has assumed staring position. Approach with awareness.",
        "NOMINAL — Standard patrol checks completed. Area declared secure pending next scheduled review.",
        "UNDER WATCH — Low-level concern flagged by the Chief. The situation is being observed. Carefully."
    ];

    // ── Recommendations ───────────────────────────────────────────────────────
    var recommendations = [
        "Household members are advised to maintain continuous awareness of the food bowl's status. Failure to fill within four minutes of an audit will result in escalating vocal briefings delivered at close range. This is not a request.",
        "The Chief has reviewed today's threat assessment and advises all household members to maintain a 0.5-metre exclusion zone around the vacuum at all times. Unauthorized vacuum mobilization must be preceded by a 20-minute formal written warning, minimum.",
        "All incoming packages must be submitted to the Chief for sniffing clearance before being opened or relocated. Cleared packages may be repurposed as auxiliary seating platforms. Packages that fail inspection will be sat upon regardless, as a security measure.",
        "The Chief hereby recommends that the kitchen perimeter be checked at 90-minute intervals and that the current treat reserves be audited and replenished with immediate effect. The existing situation is, frankly, several weeks overdue for resolution.",
        "Today's threat level warrants increased household vigilance. Avoid sudden movements, loud noises, and any vacuum-related activities without a minimum 24-hour advance notice submitted to the Chief in a format of their choosing.",
        "In response to this morning's window post assessment, the Chief recommends the installation of additional deterrents on the external ledge. The Chief's preferred method involves being granted permanent, unobstructed window access as a matter of security protocol.",
        "Following today's corridor textile anomaly, the Chief recommends a comprehensive household fabric audit. All unidentified items must be reported immediately. Non-compliance will result in sustained staring at said items until the situation is resolved to the Chief's satisfaction.",
        "The Chief's official recommendation following today's briefing is that all is reasonably in order, the sunbeam was adequate, the chicken was acceptable, and household members may consider this a relatively positive operational day. This assessment will not be repeated.",
        "The treat situation requires urgent escalation. The Chief is prepared to vocalize persistently and at intervals of the Chief's choosing until a satisfactory resolution is reached. Household members have been pre-briefed by virtue of existing in the same building.",
        "All household members are reminded that the Chief's afternoon nap window is a designated protected period. Vacuum operations, doorbell activation, and television at any volume are to be postponed. The Chief extends provisional thanks in advance, subject to compliance."
    ];

    // ── Field notes ───────────────────────────────────────────────────────────
    var fieldNotes = [
        "The vacuum has not moved in three days. I have not lowered my guard. I have never lowered my guard. This is what professionalism looks like. The vacuum knows this. That is why it stays in the closet.",
        "I stared at the squirrel for 22 continuous minutes today. It eventually left. This was a direct result of my sustained psychological deterrence. The squirrel may disagree, but the squirrel's field reports are inadmissible in this household.",
        "The sock remains unexplained. I have batted it twice and observed it from three different angles. It has provided no useful intelligence. I will continue the investigation tomorrow. The sock knows what it did.",
        "Someone opened a can in the kitchen at 17:30. I arrived before they had fully processed the situation. I consider this my personal best response time this quarter. Speed is a tactical asset. So is chicken.",
        "Conducted a full perimeter sweep today. All sectors checked. Found nothing suspicious except the food bowl, which was at approximately 40% capacity at that hour. This is below operational minimums and has been logged accordingly.",
        "The delivery driver came again. Left a box. I sniffed the box for six minutes. The box smelled of cardboard, evasion, and something that was definitely not chicken. The investigation continues. I am sitting on the box. This is standard protocol.",
        "I was in the sunbeam from 10:30 to 12:15. I was still technically on duty. Intelligence gathering from a horizontal thermal position is a methodology that I believe to be underutilized in the wider security community. I recommend it strongly.",
        "Household member watched a program featuring a dog. I observed for nine minutes, registered my professional objection via tail movement, and relocated to the kitchen. The program was not improved by my departure. That is a matter for them.",
        "Three separate people have tried to give me a bath in my operational history. None achieved their objective. This information has been archived as evidence of the Chief's superior operational effectiveness and will be cited in my annual self-review.",
        "Today's perimeter was quiet. Too quiet. I do not trust quiet. Quiet is what happens before the vacuum. I am watching from the corridor. The household believes I am napping. I am not napping. I am executing a long-duration surveillance posture."
    ];

    // ── Pick today's content ──────────────────────────────────────────────────
    var threat    = pick(threats,         seed + 10);
    var suspect   = pick(suspects,        seed + 20);
    var incidents = pickIncidents(allIncidents, seed, 5);
    var rec       = pick(recommendations, seed + 30);
    var note      = pick(fieldNotes,      seed + 40);

    var cam1 = pick(camStatuses, seed + 51);
    var cam2 = pick(camStatuses, seed + 52);
    var cam3 = pick(camStatuses, seed + 53);
    var cam4 = pick(camStatuses, seed + 54);

    var secWindow   = pick(sectorStatuses, seed + 61);
    var secKitchen  = pick(sectorStatuses, seed + 62);
    var secCorridor = pick(sectorStatuses, seed + 63);
    var secFront    = pick(sectorStatuses, seed + 64);
    var secElevated = pick(sectorStatuses, seed + 65);
    var secOutdoor  = pick(sectorStatuses, seed + 66);

    // ── Populate DOM ──────────────────────────────────────────────────────────

    // Threat bar
    document.getElementById('threat-bar-fill').style.width      = threat.pct + '%';
    document.getElementById('threat-bar-fill').style.background = threat.color;
    document.getElementById('threat-bar-label').textContent     = threat.name;
    document.getElementById('threat-name').textContent          = threat.name;
    document.getElementById('threat-name').style.color          = threat.color;
    document.getElementById('threat-desc').textContent          = threat.desc;

    // Suspect
    document.getElementById('suspect-icon').textContent       = suspect.icon;
    document.getElementById('suspect-name').textContent       = suspect.name;
    document.getElementById('suspect-class').textContent      = suspect.classification;
    document.getElementById('suspect-vector').textContent     = suspect.vector;
    document.getElementById('suspect-last').textContent       = suspect.last;
    document.getElementById('suspect-status').textContent     = suspect.status;
    document.getElementById('suspect-assessment').textContent = suspect.assessment;

    // Cameras
    function setCam(id, stat) {
        document.getElementById(id + '-status').textContent = stat.text;
        document.getElementById(id + '-status').style.color = stat.color;
        document.getElementById(id + '-ts').textContent     = timeStr + ' LOCAL';
    }
    setCam('cam1', cam1);
    setCam('cam2', cam2);
    setCam('cam3', cam3);
    setCam('cam4', cam4);

    // Incidents
    var tbody = document.getElementById('incident-tbody');
    incidents.forEach(function (inc) {
        var tr = document.createElement('tr');
        var sevClass = inc.sev === 'HIGH' ? 'sev-high' : inc.sev === 'MED' ? 'sev-med' : 'sev-low';
        tr.innerHTML =
            '<td>' + esc(inc.time) + '</td>' +
            '<td class="' + sevClass + '">' + esc(inc.sev) + '</td>' +
            '<td>' + esc(inc.sector) + '</td>' +
            '<td>' + esc(inc.desc) + '</td>';
        tbody.appendChild(tr);
    });

    // Sectors
    document.getElementById('sector-window').textContent   = secWindow;
    document.getElementById('sector-kitchen').textContent  = secKitchen;
    document.getElementById('sector-corridor').textContent = secCorridor;
    document.getElementById('sector-front').textContent    = secFront;
    document.getElementById('sector-elevated').textContent = secElevated;
    document.getElementById('sector-outdoor').textContent  = secOutdoor;

    // Recommendation + field notes
    document.getElementById('sec-recommendation').textContent = rec;
    document.getElementById('sec-field-notes').textContent    = note;

}());
</script>
