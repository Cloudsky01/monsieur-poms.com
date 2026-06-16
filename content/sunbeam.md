---
title: "Sunbeam Report"
---

<style>
.mpiss-header {
    background: linear-gradient(135deg, #1a0a00 0%, #3d2200 40%, #1a0a00 100%);
    color: #FFD700;
    text-align: center;
    padding: 20px 10px 14px;
    margin: -10px -10px 0 -10px;
    border-bottom: 4px solid #FFD700;
    position: relative;
    overflow: hidden;
}

.mpiss-header::before {
    content: '';
    position: absolute;
    top: 0; left: -100%;
    width: 40%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255,215,0,0.08), transparent);
    animation: shimmerHeader 4s linear infinite;
    pointer-events: none;
}

@keyframes shimmerHeader {
    0%   { left: -40%; }
    100% { left: 140%; }
}

.beam-visualizer {
    position: relative;
    height: 120px;
    background: linear-gradient(to bottom, #0a0a1a 0%, #1a1a2e 100%);
    overflow: hidden;
    border-top: 2px solid #444;
    border-bottom: 2px solid #444;
    margin: 0 0 0 0;
}

.beam-ray {
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 0;
    height: 0;
    border-left: 0px solid transparent;
    border-right: 0px solid transparent;
    border-bottom: 120px solid rgba(255,215,0,0.0);
    animation: beamPulse 3s ease-in-out infinite;
    filter: blur(18px);
}

.beam-glow {
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 160px;
    height: 80px;
    background: radial-gradient(ellipse at 50% 100%,
        rgba(255,215,0,0.55) 0%,
        rgba(255,160,0,0.3) 35%,
        rgba(255,100,0,0.1) 65%,
        transparent 100%);
    animation: glowPulse 3s ease-in-out infinite;
    border-radius: 50%;
}

.beam-shaft {
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 80px;
    height: 120px;
    background: linear-gradient(to bottom,
        transparent 0%,
        rgba(255,230,100,0.08) 30%,
        rgba(255,215,0,0.22) 70%,
        rgba(255,215,0,0.5) 100%);
    clip-path: polygon(30% 0%, 70% 0%, 100% 100%, 0% 100%);
    animation: shaftPulse 3s ease-in-out infinite;
}

.beam-floor {
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 200px;
    height: 22px;
    background: radial-gradient(ellipse at 50% 50%,
        rgba(255,215,0,0.6) 0%,
        rgba(255,200,0,0.3) 40%,
        transparent 75%);
    border-radius: 50%;
}

.beam-cat {
    position: absolute;
    bottom: 8px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 28px;
    animation: catBreathe 3s ease-in-out infinite;
    z-index: 2;
    filter: drop-shadow(0 0 6px rgba(255,215,0,0.7));
}

.beam-label {
    position: absolute;
    top: 8px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 9px;
    font-family: 'Courier New', monospace;
    color: rgba(255,215,0,0.6);
    letter-spacing: 3px;
    text-transform: uppercase;
    white-space: nowrap;
}

@keyframes beamPulse {
    0%,100% { opacity: 0.7; }
    50%      { opacity: 1.0; }
}
@keyframes glowPulse {
    0%,100% { opacity: 0.7; transform: translateX(-50%) scaleX(1); }
    50%      { opacity: 1.0; transform: translateX(-50%) scaleX(1.15); }
}
@keyframes shaftPulse {
    0%,100% { opacity: 0.6; }
    50%      { opacity: 1.0; }
}
@keyframes catBreathe {
    0%,100% { transform: translateX(-50%) translateY(0px); }
    50%      { transform: translateX(-50%) translateY(-3px); }
}

.quality-badge {
    display: inline-block;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 20px;
    letter-spacing: 3px;
    padding: 8px 20px;
    border: 4px solid currentColor;
    text-transform: uppercase;
    position: relative;
}

.report-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 11px;
    margin: 12px 0;
}

.report-table td {
    padding: 5px 8px;
    border-bottom: 1px solid #DDD;
    vertical-align: top;
    line-height: 1.6;
}

.report-table td:first-child {
    font-family: 'Courier New', monospace;
    font-size: 9px;
    font-weight: bold;
    letter-spacing: 1px;
    text-transform: uppercase;
    color: #666;
    width: 36%;
    padding-top: 7px;
}

.report-table tr:nth-child(even) td {
    background: #FAFAFA;
}

.findings-box {
    background: #FFFFF0;
    border: 2px solid #D4AC00;
    border-left: 6px solid #D4AC00;
    padding: 12px 14px;
    margin: 14px 0;
    font-size: 12px;
    line-height: 1.8;
    color: #3a2800;
}

.cert-seal {
    display: inline-flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 110px;
    height: 110px;
    border-radius: 50%;
    border: 5px double #D4AC00;
    background: radial-gradient(circle, #fff9e0 0%, #fff0c0 60%, #ffe080 100%);
    box-shadow: 0 0 0 3px #D4AC00, 0 0 14px rgba(212,172,0,0.4);
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 8px;
    letter-spacing: 1px;
    text-transform: uppercase;
    text-align: center;
    color: #5a3a00;
    line-height: 1.4;
    padding: 8px;
    animation: sealPulse 4s ease-in-out infinite;
}

@keyframes sealPulse {
    0%,100% { box-shadow: 0 0 0 3px #D4AC00, 0 0 14px rgba(212,172,0,0.4); }
    50%      { box-shadow: 0 0 0 3px #FFD700, 0 0 28px rgba(255,215,0,0.6); }
}

.meter-out {
    background: #DDD;
    border: 2px inset #AAA;
    height: 16px;
    width: 100%;
    margin: 4px 0 2px;
    overflow: hidden;
    border-radius: 2px;
}

.meter-in {
    height: 100%;
    animation: meterFill 1.2s ease-out forwards;
    border-radius: 2px;
}

@keyframes meterFill { from { width: 0%; } }

.report-reveal {
    animation: reportReveal 0.6s ease-out forwards;
}

@keyframes reportReveal {
    from { opacity: 0; transform: translateY(-6px); }
    to   { opacity: 1; transform: translateY(0); }
}

.ticker-text {
    display: inline-block;
    animation: tickerScroll 22s linear infinite;
    white-space: nowrap;
}
@keyframes tickerScroll {
    from { transform: translateX(100%); }
    to   { transform: translateX(-100%); }
}
</style>

<div style="border: 1px solid #CCC; overflow: hidden; margin-bottom: 20px; background: #F9F9F9;">

<div class="mpiss-header">
    <div style="font-size: 9px; letter-spacing: 4px; color: #B8860B; margin-bottom: 6px; font-family: 'Courier New', monospace;">
        ESTABLISHED 2010 &bull; EST. GENÈVE, CARDBOARD BOX DIVISION &bull; ACCREDITED SINCE NAP ONE
    </div>
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 30px; letter-spacing: 5px; text-shadow: 2px 2px 0 #000, 0 0 20px rgba(255,215,0,0.4);">
        ☀️ MONSIEUR POMS ☀️
    </div>
    <div style="font-family: 'Georgia', serif; font-size: 13px; letter-spacing: 2px; color: #E8C000; margin: 4px 0;">
        Institute of Sunbeam Sciences
    </div>
    <div style="font-size: 9px; letter-spacing: 3px; color: #A08020; margin-top: 4px; text-transform: uppercase;">
        Official Daily Sunbeam Quality Assessment &amp; Certification Report
    </div>
</div>

<div style="background: #111; overflow: hidden;">
    <div style="overflow: hidden; white-space: nowrap; padding: 3px 0; font-size: 9px; font-family: 'Courier New', monospace; color: #FFD700;">
        <span class="ticker-text">
            &nbsp;&nbsp;&nbsp; ☀ MPISS LIVE SOLAR FEED &nbsp;|&nbsp; TODAY'S ASSESSMENT IN PROGRESS &nbsp;|&nbsp; POMS ON-SITE VERIFICATION COMPLETE &nbsp;|&nbsp; GREEN BEAN INDEX: NOT APPLICABLE &nbsp;|&nbsp; HOUSEHOLD SUNBEAM AUTHORITY REPORTING &nbsp;|&nbsp; CLOUD THREAT LEVEL: MONITORED &nbsp;|&nbsp; TREAT RESERVES: STABLE &nbsp;|&nbsp; BEAM CLAIM STATUS: ACTIVE &nbsp;|&nbsp; CARDBOARD BOX ADJACENT BEAM: SEPARATELY CLASSIFIED &nbsp;&nbsp;&nbsp;
        </span>
    </div>
</div>

<div class="beam-visualizer">
    <div class="beam-shaft" id="beam-shaft"></div>
    <div class="beam-glow" id="beam-glow"></div>
    <div class="beam-floor" id="beam-floor"></div>
    <div class="beam-label">☀ ACTIVE BEAM — FIELD VERIFIED BY M. POMS</div>
    <div class="beam-cat">🐱</div>
</div>

<div style="background: #EEE; border-bottom: 2px solid #CCC; padding: 5px 12px; font-size: 10px; color: #555; text-align: center; font-family: 'Courier New', monospace;">
    REPORT CLASS: Solar Intelligence &nbsp;|&nbsp; CLEARANCE: Poms-Authorized &nbsp;|&nbsp; ISSUED DAILY AT MIDNIGHT &nbsp;|&nbsp; DATE: <strong id="sb-date"></strong>
</div>

<div style="padding: 16px;">

<p style="font-size: 11px; color: #444; text-align: center; line-height: 1.75; font-style: italic;">
    The Monsieur Poms Institute of Sunbeam Sciences conducts rigorous daily assessments of all household solar phenomena.<br>
    Each beam is evaluated on warmth, coverage, duration, and strategic napping potential.<br>
    Results are certified by Monsieur Poms personally via direct occupancy testing. Green beans are not a solar phenomenon and will not be assessed.
</p>

<div class="report-reveal" id="sb-report">

<!-- Quality badge + cert seal -->
<div style="display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 12px; margin: 14px 0;">
    <div>
        <div style="font-size: 9px; font-family: 'Courier New', monospace; color: #888; letter-spacing: 2px; margin-bottom: 6px; text-transform: uppercase;">
            Today's Quality Classification:
        </div>
        <div class="quality-badge" id="quality-badge">—</div>
        <div style="font-size: 10px; color: #888; margin-top: 5px; font-family: 'Courier New', monospace;">
            Score: <strong id="quality-score">—</strong> &nbsp;|&nbsp; Report No.: <span id="report-number">—</span>
        </div>
    </div>
    <div class="cert-seal" id="cert-seal">
        <div style="font-size: 18px; margin-bottom: 2px;">🐾</div>
        <div style="font-size: 7px; font-weight: normal; font-family: 'Verdana', sans-serif; letter-spacing: 0;">CERTIFIED</div>
        <div style="font-size: 9px;">MPISS</div>
        <div style="font-size: 7px; font-weight: normal; font-family: 'Verdana', sans-serif; letter-spacing: 0;">PAW VERIFIED</div>
    </div>
</div>

<hr>

<!-- Data readings -->
<div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 12px; letter-spacing: 3px; color: #3a2800; border-bottom: 2px solid #D4AC00; padding-bottom: 4px; margin-bottom: 8px;">
    📋 FIELD READINGS — TODAY'S ASSESSMENT
</div>

<table class="report-table">
    <tr>
        <td>Beam Location:</td>
        <td id="sb-location">—</td>
    </tr>
    <tr>
        <td>Room:</td>
        <td id="sb-room">—</td>
    </tr>
    <tr>
        <td>Surface Coordinates:</td>
        <td id="sb-coords">—</td>
    </tr>
    <tr>
        <td>Warmth Reading:</td>
        <td id="sb-warmth">—</td>
    </tr>
    <tr>
        <td>Estimated Duration:</td>
        <td id="sb-duration">—</td>
    </tr>
    <tr>
        <td>Paw Coverage Area:</td>
        <td id="sb-coverage">—</td>
    </tr>
    <tr>
        <td>Nap Potential Index:</td>
        <td id="sb-nap">—</td>
    </tr>
    <tr>
        <td>Incident on Record:</td>
        <td id="sb-incident">—</td>
    </tr>
</table>

<!-- Warmth meter -->
<div style="max-width: 480px; margin: 10px 0 16px;">
    <div style="font-size: 9px; font-family: 'Verdana', sans-serif; color: #666; letter-spacing: 1px; margin-bottom: 2px;">
        WARMTH COEFFICIENT (%):
    </div>
    <div class="meter-out">
        <div class="meter-in" id="warmth-meter"
             style="background: linear-gradient(to right, #FFD700, #FF8C00);"></div>
    </div>
    <div style="font-size: 9px; color: #888; text-align: right;" id="warmth-label">—</div>
</div>

<!-- Official findings -->
<div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 12px; letter-spacing: 3px; color: #3a2800; border-bottom: 2px solid #D4AC00; padding-bottom: 4px; margin-bottom: 8px;">
    🔬 OFFICIAL INSTITUTE FINDINGS
</div>

<div class="findings-box">
    <div style="font-size: 9px; font-family: 'Verdana', sans-serif; font-weight: bold; letter-spacing: 2px; color: #8B6914; text-transform: uppercase; margin-bottom: 6px; border-bottom: 1px dotted #D4AC00; padding-bottom: 4px;">
        Assessment Summary — for internal household distribution only
    </div>
    <div id="sb-finding">—</div>
</div>

<!-- Quality description -->
<div style="background: #FFF8E8; border: 2px solid #E8CC80; padding: 12px 14px; margin: 14px 0; font-size: 12px; line-height: 1.75; color: #3a2800;">
    <div style="font-family: 'Verdana', sans-serif; font-weight: bold; font-size: 10px; letter-spacing: 2px; color: #8B6914; margin-bottom: 6px; text-transform: uppercase;">
        ☀ Quality Classification Details:
    </div>
    <div id="sb-quality-desc">—</div>
</div>

<!-- Official recommendation -->
<div style="background: #1a0a00; color: #FFD700; border: 3px solid #D4AC00; padding: 12px 14px; margin: 14px 0; font-size: 11px; line-height: 1.75;">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 12px; letter-spacing: 3px; margin-bottom: 8px; border-bottom: 1px solid #D4AC00; padding-bottom: 5px;">
        📌 OFFICIAL MPISS RECOMMENDATION
    </div>
    <div id="sb-recommendation" style="color: #FFE080;">—</div>
</div>

<!-- Poms personal verdict -->
<div style="background: #FFFFF0; border: 2px inset #CCC; padding: 10px 14px; margin: 14px 0; font-size: 11px; color: #333; font-style: italic; line-height: 1.8;">
    <div style="font-family: 'Verdana', sans-serif; font-weight: bold; font-size: 10px; color: #3a2800; display: block; margin-bottom: 5px; font-style: normal; letter-spacing: 1px;">
        🐱 POMS' PERSONAL FIELD NOTES (CLASSIFIED — HOUSEHOLD EYES ONLY):
    </div>
    &ldquo;<span id="sb-verdict">—</span>&rdquo;
    <div style="font-size: 9px; color: #888; text-align: right; margin-top: 6px; font-style: normal;">
        — M. Poms, Director, Institute of Sunbeam Sciences &nbsp;|&nbsp; <span id="sb-date2"></span>
    </div>
</div>

<!-- Footer cert line -->
<div style="border-top: 2px dotted #D4AC00; margin-top: 16px; padding-top: 10px; font-size: 9px; color: #888; text-align: center; line-height: 1.8; font-family: 'Courier New', monospace;">
    Report authenticated by paw contact &bull; MPISS Report No. <span id="sb-report-footer">—</span> &bull; Valid for current calendar day only<br>
    Sunbeam data expires at midnight — new assessment issued automatically &bull; Do not extrapolate yesterday's beam to today's conditions<br>
    <em>The Institute accepts no liability for nap quality, cloud cover, or unsolicited green bean offers.</em>
</div>

</div>
</div>

<hr>
<p style="font-size: 10px; color: #888; text-align: center; line-height: 1.75;">
    <em>The Monsieur Poms Institute of Sunbeam Sciences operates independently of meteorological authorities.<br>
    All findings reflect Poms' direct occupancy assessment and are final. The cloud will be hearing from us.<br>
    New report issued at midnight. Previous reports filed in the cardboard box archives.</em>
</p>

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
    document.getElementById('sb-date').textContent  = dateStr;
    document.getElementById('sb-date2').textContent = dateStr;

    // ── Locations ──────────────────────────────────────────────────────────────
    var locations = [
        { name: "Window B — Eastern Panel", room: "Living Room", coords: "Approx. 2.3m from east wall, sofa-adjacent, south-facing" },
        { name: "Kitchen Floor — Corner Patch", room: "Kitchen", coords: "Tile surface near radiator, triangular footprint, morning-optimal" },
        { name: "Hallway Strip — Central Corridor", room: "Hallway", coords: "1.1m corridor section, afternoon-only beam, no shade interference" },
        { name: "Bedroom Carpet Zone A", room: "Bedroom", coords: "Foot-of-bed sector, morning window alignment, warm pile confirmed" },
        { name: "Sofa Armrest — Right Side", room: "Living Room", coords: "Elevated surface, south-facing, padded, premium comfort rating" },
        { name: "Living Room Floor — Main Patch", room: "Living Room", coords: "Central rug, maximum coverage zone, historically contested territory" },
        { name: "Kitchen Windowsill", room: "Kitchen", coords: "Narrow strip, high-intensity beam, vertical orientation, worth it" },
        { name: "Bookshelf Top — Elevated Survey Post", room: "Study", coords: "Top shelf, south window exposure, excellent sightline bonus, access: vertical" },
        { name: "Rug Sector 7 — Primary Domain", room: "Living Room", coords: "Central rug, maximum area, confirmed claim on file since 2022" },
        { name: "Bathroom Tile — Morning Slant", room: "Bathroom", coords: "East window slant, morning hours only, excellent warmth-per-square-inch ratio" },
        { name: "Couch Corner — Wedge Position", room: "Living Room", coords: "Back-left cushion, beam enters approx. 9:40 AM, duration: moderate" },
        { name: "Dining Chair — Padded Seat", room: "Dining Room", coords: "South window adjacent, seat surface claimed pre-noon, cushion: excellent" }
    ];

    // ── Quality ratings ────────────────────────────────────────────────────────
    var qualities = [
        {
            rating: "EXCEPTIONAL",
            score: "9.7 / 10",
            color: "#D4AC00",
            borderColor: "#D4AC00",
            desc: "Today's sunbeam represents a pinnacle of solar achievement. Warmth distribution is optimal. Coverage exceeds 94% of the standard assessment area. Poms has rated this beam personally and awarded it his highest designation. This is a red-letter day on the sunbeam calendar.",
            rec: "Occupy immediately and defend vigorously. Do not leave for any reason, including meals. Meals can be relocated. This beam cannot."
        },
        {
            rating: "EXCELLENT",
            score: "8.8 / 10",
            color: "#FFA500",
            borderColor: "#FFA500",
            desc: "A high-quality beam with strong warmth output and reliable duration. Minor cloud interference was noted but ultimately resolved in Poms' favour. This beam met or exceeded all seven MPISS evaluation criteria.",
            rec: "Primary occupation strongly recommended. Brief departures for treats are permissible, but return within 4 minutes. Do not test the beam's patience."
        },
        {
            rating: "ACCEPTABLE",
            score: "6.4 / 10",
            color: "#888888",
            borderColor: "#888888",
            desc: "An adequate beam by most standards. Poms has accepted it under formal protest. Warmth coefficient falls within operational parameters but lacks the distinction of premium-tier beams. A supplemental audit is pending subject to cloud conditions.",
            rec: "Occupation approved. Enthusiasm is not required today. Approach this beam as a professional duty rather than a personal pleasure."
        },
        {
            rating: "SUBSTANDARD",
            score: "4.1 / 10",
            color: "#AA4400",
            borderColor: "#AA4400",
            desc: "Today's beam showed early promise but failed to deliver on its core metrics. Duration was insufficient and warmth inconsistent due to unacceptable cloud activity. A formal letter of complaint has been issued to the meteorological office.",
            rec: "Temporary occupation only. Maintain full protest posture. Reserve napping commitment for a better-qualified beam. Vocalize dissatisfaction at regular intervals."
        },
        {
            rating: "SCANDALOUS",
            score: "2.3 / 10",
            color: "#CC0000",
            borderColor: "#CC0000",
            desc: "This is completely unacceptable. The beam was narrow, cold, and relocated before an adequate nap session could be established. Cloud interference was sustained and unresolved. Monsieur Poms has issued a formal public statement. The sky is on notice.",
            rec: "Do not occupy. The Institute recommends a standing protest position only. File a household complaint immediately. Demand better from tomorrow's solar conditions in clear and direct terms."
        },
        {
            rating: "CERTIFIED PREMIUM",
            score: "10.0 / 10",
            color: "#00AA55",
            borderColor: "#00AA55",
            desc: "An extremely rare designation. Today's beam has been awarded the highest possible rating by the MPISS. Coverage is total, warmth is maximal, and duration extends into the optimal post-lunch window. This is a historic solar event.",
            rec: "All other activities are suspended. Full-body occupation is mandatory. Notify no one. This beam is a private achievement between Poms and the sun and should be treated with appropriate reverence."
        },
        {
            rating: "UNDER REVIEW",
            score: "7.1 / 10",
            color: "#4444CC",
            borderColor: "#4444CC",
            desc: "Today's beam is currently under active MPISS investigation. Preliminary readings indicate above-average warmth but the coverage area displayed irregular migration patterns inconsistent with standard solar drift. Poms is monitoring the situation personally.",
            rec: "Cautious occupation is approved. Maintain situational awareness. Be prepared to relocate if the beam shifts further east. Keep one eye on the beam at all times. The other eye may nap."
        }
    ];

    // ── Warmth readings ────────────────────────────────────────────────────────
    var warmths = [
        { text: "41.2°C — Exceptional — rare solar event; direct exposure, premium tier", pct: 97 },
        { text: "38.4°C — Certified Maximum Warmth Achievement for this location", pct: 91 },
        { text: "36.7°C — High — extended occupancy protocol recommended", pct: 85 },
        { text: "34.1°C — Excellent — full-body thermal coverage confirmed", pct: 78 },
        { text: "29.8°C — Adequate — supplemental blanket acceptable if required", pct: 62 },
        { text: "25.3°C — Borderline — protest-level warmth; beam put on formal notice", pct: 44 },
        { text: "22.4°C — Below Standard — complaint filed with meteorological office", pct: 30 }
    ];

    // ── Coverage area ──────────────────────────────────────────────────────────
    var coverages = [
        "Full-body coverage (4 paws + tail) — assessed as optimal",
        "Torso and forepaws confirmed — tail in partial shade (logged)",
        "Loaf configuration — all tucked limbs confirmed within beam radius",
        "Head and right side only — positional adjustment filed for review",
        "98% full coverage — left ear technically in shadow; within tolerance",
        "Sprawl configuration — maximum surface area claimed, 6-paw spread",
        "Compact curl — core warmth maintained, extremities monitoring pending"
    ];

    // ── Nap potential ──────────────────────────────────────────────────────────
    var napPotentials = [
        "MAXIMUM — Full deployment authorised; all nap conditions met",
        "HIGH — Excellent conditions; minor cloud risk noted but manageable",
        "ELEVATED — Good conditions; recommend initiating within the next 20 minutes",
        "MODERATE — Satisfactory; nap quality guaranteed but duration uncertain",
        "LIMITED — Conditions below standard; brief session only recommended",
        "EXCEPTIONAL — Rare alignment of warmth, position, and silence; deploy immediately"
    ];

    // ── Incidents ──────────────────────────────────────────────────────────────
    var incidents = [
        "A passing cloud cast a shadow at 10:47 AM. Duration: 3 minutes. Poms waited it out with evident and documented displeasure.",
        "None on record. A flawless session from first light to beam termination. This is noted as an event of exceptional rarity.",
        "A household member walked through the beam at 9:22 AM without acknowledging its occupant. A formal notice is being prepared.",
        "The beam relocated 0.4 metres due to solar drift at 11:15 AM. Poms tracked and reclaimed the new position within 90 seconds.",
        "A vacuum cleaner was operated in proximity to the beam at 2:30 PM. This is being treated as a hostile act. Investigation ongoing.",
        "A delivery to the front door caused a 47-second beam interruption via door shadow. Compensation has been demanded in writing.",
        "An unsolicited 'oh you're in the sun!' commentary was delivered by a household member. The beam was not disrupted but the comment was logged.",
        "The beam was briefly investigated by a patch of reflected car-window light. Poms assessed it and found it a secondary concern.",
        "Beam terminated 14 minutes early due to cloud cover. Poms remained in the vacated area for a further 8 minutes as a formal protest."
    ];

    // ── Findings ──────────────────────────────────────────────────────────────
    var findings = [
        "Analysis confirms prime beaming conditions today. The Institute recommends full occupation with standard treat supplementation to sustain extended napping operations.",
        "Today's beam ranks in the top 23% of seasonal assessments at this location. Full nap commitment is authorised for up to 4 hours without a formal reapplication.",
        "Following a rigorous 12-point assessment, the Institute confirms today's beam meets baseline certification standards. Occupancy is approved. Enthusiasm level is at Poms' discretion.",
        "The Institute has classified today's beam as diplomatically complex due to timing conflicts with the scheduled meal delivery window. Occupants are advised to proceed with awareness.",
        "Today's solar conditions are among the most significant observed this calendar quarter. The Institute strongly recommends immediate and extended occupation. This opportunity may not recur for several days.",
        "Assessment indicates a satisfactory beam with minor reservations regarding lateral thermal consistency. Poms has been briefed and has accepted the situation under protest.",
        "The Institute has reviewed all seven evaluation criteria and found today's beam adequate for standard napping operations. No supplemental warming apparatus is required at this time."
    ];

    // ── Personal field notes ──────────────────────────────────────────────────
    var verdicts = [
        "The beam was adequate. I have claimed it. I will remain in this position until it moves, at which point I will follow it. This is called dedication.",
        "I have assessed the situation. The warmth is acceptable. The location is correct. I am now horizontal. Do not disturb me.",
        "This beam is satisfactory and I have taken ownership of it in the traditional manner, which is to say I sat on it. It is mine now.",
        "I located this beam at 9:02 AM. I claimed it at 9:02 AM. There was no gap between these events. I am a professional.",
        "The sun has chosen me today. I do not question the sun's methods. I only occupy its results. This is my gift to the household.",
        "I have been in this position for some time now. The warmth is correct. My posture is excellent. I am peak cat.",
        "Today's beam is an exceptional one. I have given it my full attention and my complete body weight. The floor is grateful.",
        "I moved with the beam as it shifted. Some would call this chasing sunlight. I call it territorial jurisdiction management.",
        "The beam was not ideal at first. I filed an internal complaint and waited. The situation improved. Patience is a virtue when you have nowhere else to be.",
        "I have conducted a full assessment of this sunbeam from the inside. My methodology is occupancy-based. My conclusions are warm."
    ];

    // ── Durations ────────────────────────────────────────────────────────────
    var durations = [
        "2 hr 14 min (forecast: extended with intermittent cloud breaks)",
        "3 hr 07 min (optimal window: 9 AM — 12 PM; post-noon: reduced)",
        "1 hr 43 min (condensed schedule; increased intensity partially compensates)",
        "4 hr 22 min (full-day prime — exceptional value, rare classification)",
        "47 min (brief but intense; the Institute notes: quality over quantity)",
        "2 hr 55 min (peak warmth at 11:30 AM; early arrival strongly recommended)",
        "1 hr 20 min (morning-only beam; afternoon re-evaluation pending cloud data)"
    ];

    // ── Pick today's content ──────────────────────────────────────────────────
    var loc       = pick(locations,    seed + 10);
    var quality   = pick(qualities,    seed + 20);
    var warmth    = pick(warmths,      seed + 30);
    var coverage  = pick(coverages,    seed + 40);
    var nap       = pick(napPotentials, seed + 50);
    var incident  = pick(incidents,    seed + 60);
    var finding   = pick(findings,     seed + 70);
    var verdict   = pick(verdicts,     seed + 80);
    var duration  = pick(durations,    seed + 90);

    var reportNum = "MPISS-" + now.getFullYear() + "-" + String(doy).padStart(3, '0') +
                    "-" + String(Math.floor(seededRand(seed + 777) * 9000) + 1000);

    // ── Populate DOM ──────────────────────────────────────────────────────────
    document.getElementById('quality-badge').textContent = quality.rating;
    document.getElementById('quality-badge').style.color       = quality.color;
    document.getElementById('quality-badge').style.borderColor = quality.borderColor;

    document.getElementById('quality-score').textContent = quality.score;
    document.getElementById('report-number').textContent  = reportNum;
    document.getElementById('sb-report-footer').textContent = reportNum;

    document.getElementById('sb-location').textContent = loc.name;
    document.getElementById('sb-room').textContent     = loc.room;
    document.getElementById('sb-coords').textContent   = loc.coords;
    document.getElementById('sb-warmth').textContent   = warmth.text;
    document.getElementById('sb-duration').textContent = duration;
    document.getElementById('sb-coverage').textContent = coverage;
    document.getElementById('sb-nap').textContent      = nap;
    document.getElementById('sb-incident').textContent = incident;

    document.getElementById('warmth-meter').style.width = warmth.pct + '%';
    document.getElementById('warmth-label').textContent = warmth.pct + '% coefficient';

    document.getElementById('sb-finding').innerHTML    = esc(finding);
    document.getElementById('sb-quality-desc').innerHTML = esc(quality.desc);
    document.getElementById('sb-recommendation').innerHTML = esc(quality.rec);
    document.getElementById('sb-verdict').innerHTML    = esc(verdict);

    // Tint the beam shaft to match quality color
    var shaft = document.getElementById('beam-shaft');
    if (shaft) {
        shaft.style.background = 'linear-gradient(to bottom, transparent 0%, ' +
            quality.color + '15 30%, ' +
            quality.color + '40 70%, ' +
            quality.color + '80 100%)';
    }
    var glow = document.getElementById('beam-glow');
    if (glow) {
        glow.style.background = 'radial-gradient(ellipse at 50% 100%, ' +
            quality.color + '99 0%, ' +
            quality.color + '55 35%, ' +
            quality.color + '22 65%, transparent 100%)';
    }
    var floor = document.getElementById('beam-floor');
    if (floor) {
        floor.style.background = 'radial-gradient(ellipse at 50% 50%, ' +
            quality.color + '99 0%, ' +
            quality.color + '55 40%, transparent 75%)';
    }

}());
</script>
