---
title: "Complaint Department"
---

<style>
.complaint-header-strip {
    background: linear-gradient(to right, #1a1400, #3d3000, #1a1400);
    color: #FFD700;
    text-align: center;
    padding: 16px 10px;
    margin: -10px -10px 0 -10px;
    border-bottom: 4px double #8B7300;
}

.complaint-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 11px;
    margin: 8px 0;
}
.complaint-table th {
    background: #3d3000;
    color: #FFD700;
    padding: 5px 8px;
    text-align: left;
    font-family: 'Verdana', sans-serif;
    font-size: 10px;
    letter-spacing: 1px;
    text-transform: uppercase;
    border: 1px solid #1a1400;
}
.complaint-table td {
    padding: 6px 8px;
    border: 1px solid #CCC;
    vertical-align: top;
}
.complaint-table tbody tr:nth-child(4n+1) td,
.complaint-table tbody tr:nth-child(4n+2) td {
    background: #FDF5E6;
}
.complaint-table tbody tr.detail-row td {
    background: #FFFFF0 !important;
}
.complaint-table tbody tr.clickable-row {
    cursor: pointer;
}
.complaint-table tbody tr.clickable-row:hover td {
    background: #FFF8DC !important;
}

.severity-badge {
    display: inline-block;
    padding: 2px 5px;
    font-size: 9px;
    font-weight: bold;
    font-family: 'Verdana', sans-serif;
    letter-spacing: 1px;
    border: 1px solid rgba(0,0,0,0.25);
    text-transform: uppercase;
    white-space: nowrap;
}

.stat-counter {
    background: #000;
    color: #FFCC00;
    font-family: 'Courier New', monospace;
    font-weight: bold;
    padding: 4px 10px;
    border: 3px inset #555;
    letter-spacing: 2px;
    display: inline-block;
}

.alert-level-row {
    display: flex;
    align-items: center;
    gap: 7px;
    padding: 4px 8px;
    border: 2px solid #CCC;
    font-family: 'Courier New', monospace;
    font-size: 10px;
    font-weight: bold;
    margin-bottom: 3px;
}

.submit-field {
    width: 100%;
    font-family: 'Courier New', monospace;
    font-size: 12px;
    padding: 5px 7px;
    border: 2px inset #999;
    background: #FFFFF0;
    color: #000080;
    box-sizing: border-box;
    margin-bottom: 8px;
    display: block;
}
</style>

<div style="border: 1px solid #CCC; overflow: hidden; margin-bottom: 20px; background: #F9F9F9;">

<div class="complaint-header-strip">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 24px; letter-spacing: 4px; text-shadow: 2px 2px 0 #000;">
        😤 OFFICIAL COMPLAINT DEPARTMENT 😤
    </div>
    <div style="font-size: 10px; color: #DDB870; margin-top: 5px; letter-spacing: 3px; text-transform: uppercase;">
        Office of Formal Grievances &nbsp;|&nbsp; Monsieur Poms Administration &nbsp;|&nbsp; Est. 2010
    </div>
</div>

<div style="background: #EEE5C0; border-bottom: 3px double #8B7300; padding: 6px 12px; font-size: 10px; color: #5c4500; text-align: center;">
    CATEGORY: Grievance Management &nbsp;|&nbsp; All complaints formally logged &nbsp;|&nbsp; Updated Daily at Midnight &nbsp;|&nbsp; Today: <strong id="complaint-date"></strong>
</div>

<div style="padding: 14px;">

<p style="font-size: 11px; color: #444; text-align: center; line-height: 1.75; font-style: italic;">
    This is the official complaint filing office of Monsieur Poms. All formal grievances regarding food bowl levels,<br>
    treat delivery schedules, vacuum cleaner incidents, and related matters are processed here.<br>
    Complaints are reviewed personally during nap hours. Green bean submissions are rejected without review.
</p>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- ALERT LEVEL                                                -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div style="margin: 14px 0; border: 3px double #8B7300; background: #FDF5E6; padding: 12px;">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 13px; color: #3d3000; letter-spacing: 2px; border-bottom: 2px solid #8B7300; padding-bottom: 5px; margin-bottom: 10px;">
        ⚠️ CURRENT COMPLAINT ALERT LEVEL
    </div>
    <div style="display: flex; gap: 14px; align-items: flex-start; flex-wrap: wrap;">
        <div id="alert-bar" style="min-width: 195px; flex-shrink: 0;"></div>
        <div style="flex: 1; min-width: 180px;">
            <div id="alert-code" style="font-family: 'Courier New', monospace; font-size: 10px; color: #777; letter-spacing: 2px; margin-bottom: 5px;"></div>
            <div id="alert-label" style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 22px; letter-spacing: 2px; margin-bottom: 7px; padding: 3px 10px; display: inline-block; border: 2px solid #888;"></div>
            <div id="alert-desc" style="font-size: 11px; color: #333; line-height: 1.7;"></div>
        </div>
    </div>
</div>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- TODAY'S COMPLAINTS TABLE                                   -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 14px; color: #3d3000; letter-spacing: 1px; border-bottom: 2px solid #8B7300; padding-bottom: 4px; margin: 14px 0 8px;">
    📋 TODAY'S FILED COMPLAINTS
</div>

<table class="complaint-table">
    <thead>
        <tr>
            <th style="width: 95px;">Case No.</th>
            <th style="width: 65px;">Filed At</th>
            <th>Subject &amp; Department</th>
            <th style="width: 68px;">Severity</th>
            <th style="width: 100px;">Status</th>
        </tr>
    </thead>
    <tbody id="complaint-tbody"></tbody>
</table>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- STATS ROW                                                  -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div style="background: #FDF5E6; border: 2px inset #8B7300; padding: 10px 14px; margin: 14px 0; display: flex; gap: 16px; align-items: center; flex-wrap: wrap;">
    <div style="text-align: center; flex: 1; min-width: 130px;">
        <div style="font-size: 10px; color: #5c4500; font-family: 'Verdana', sans-serif; letter-spacing: 1px; text-transform: uppercase; margin-bottom: 4px;">Total Complaints Filed Since 2010</div>
        <div class="stat-counter" id="total-complaints" style="font-size: 18px;">——</div>
    </div>
    <div style="text-align: center; flex: 1; min-width: 100px;">
        <div style="font-size: 10px; color: #5c4500; font-family: 'Verdana', sans-serif; letter-spacing: 1px; text-transform: uppercase; margin-bottom: 4px;">Active Cases Today</div>
        <div class="stat-counter" id="active-cases" style="font-size: 18px;">—</div>
    </div>
    <div style="text-align: center; flex: 1; min-width: 100px;">
        <div style="font-size: 10px; color: #5c4500; font-family: 'Verdana', sans-serif; letter-spacing: 1px; text-transform: uppercase; margin-bottom: 4px;">Bowl Status</div>
        <div class="stat-counter" id="bowl-status" style="font-size: 12px; padding: 6px 8px;">——</div>
    </div>
</div>

<!-- ═══════════════════════════════════════════════════════════ -->
<!-- SUBMIT A COMPLAINT                                         -->
<!-- ═══════════════════════════════════════════════════════════ -->
<div style="background: #FFFFF5; border: 2px solid #8B7300; padding: 12px; margin: 14px 0;">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 13px; color: #3d3000; letter-spacing: 1px; margin-bottom: 6px;">
        📝 SUBMIT A COMPLAINT TO MONSIEUR POMS
    </div>
    <div style="font-size: 10px; color: #666; margin-bottom: 10px; font-style: italic; line-height: 1.6;">
        All complaints are reviewed personally by Monsieur Poms. Reviews occur during nap hours.
        Estimated response time: 4–8 naps. Monsieur Poms reserves the right to ignore complaints he finds uninteresting.
        Green bean submissions are rejected automatically and without sympathy.
    </div>
    <div id="complaint-form">
        <label style="font-size: 11px; font-weight: bold; color: #3d3000; display: block; margin-bottom: 2px;">Your Name or Handle:</label>
        <input type="text" id="f-name" class="submit-field" placeholder="e.g. CoolCat88, PomsFan2010…" maxlength="60">

        <label style="font-size: 11px; font-weight: bold; color: #3d3000; display: block; margin-bottom: 2px;">Subject of Complaint:</label>
        <input type="text" id="f-subject" class="submit-field" placeholder="e.g. Bowl was only 60% full at 6 AM" maxlength="100">

        <label style="font-size: 11px; font-weight: bold; color: #3d3000; display: block; margin-bottom: 2px;">Description (optional):</label>
        <textarea id="f-desc" class="submit-field" rows="3" placeholder="Describe the grievance in detail. Monsieur Poms appreciates precision and dramatic flair."></textarea>

        <button id="submit-btn" onclick="fileComplaint()" style="
            background: linear-gradient(to bottom, #8B7300, #5c4500);
            color: #FFD700;
            font-family: 'Impact', 'Arial Black', sans-serif;
            font-size: 16px;
            letter-spacing: 2px;
            border: 3px outset #B8960C;
            padding: 8px 22px;
            cursor: pointer;
            text-shadow: 1px 1px 0 #000;
            box-shadow: 3px 3px 0 #000;
        "
        onmouseover="this.style.background='linear-gradient(to bottom,#B8960C,#8B7300)'"
        onmouseout="this.style.background='linear-gradient(to bottom,#8B7300,#5c4500)'">
            📋 FILE COMPLAINT
        </button>
    </div>
    <div id="complaint-submitted" style="display:none;"></div>
</div>

<hr>
<p style="font-size: 10px; color: #888; text-align: center; line-height: 1.75;">
    <em>All complaints are processed in accordance with the Rules of the Court of Monsieur Poms.<br>
    Resolution timelines are estimates. Actual resolution depends on whether Monsieur Poms is napping, which he usually is.<br>
    Green bean-related submissions are automatically rejected, deleted, and formally objected to.<br>
    Chicken-related submissions receive priority handling and are expedited immediately.</em>
</p>

</div><!-- /padding -->
</div><!-- /outer border -->

<script>
(function () {

    // ── Seeded deterministic random (same engine as Weather / Horoscope / Decree) ──
    function seededRand(s) {
        var x = Math.sin(s * 127.1 + 311.7) * 43758.5453123;
        return x - Math.floor(x);
    }

    function seededShuffle(arr, seed) {
        var a = arr.slice();
        for (var i = a.length - 1; i > 0; i--) {
            var j = Math.floor(seededRand(seed + i * 13) * (i + 1));
            var tmp = a[i]; a[i] = a[j]; a[j] = tmp;
        }
        return a;
    }

    function esc(s) {
        return String(s)
            .replace(/&/g, '&amp;')
            .replace(/</g, '&lt;')
            .replace(/>/g, '&gt;')
            .replace(/"/g, '&quot;');
    }

    var now       = new Date();
    var doy       = Math.floor((now - new Date(now.getFullYear(), 0, 0)) / 86400000);
    var seed      = now.getFullYear() * 1000 + doy;

    var dayNames   = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
    var monthNames = ["January","February","March","April","May","June","July","August","September","October","November","December"];
    var dateStr    = dayNames[now.getDay()] + ", " + monthNames[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear();
    document.getElementById('complaint-date').textContent = dateStr;

    // ── Alert levels (rendered bottom-to-top so highest is at top) ──
    var alertLevels = [
        { level: 1, code: "CONDITION ALPHA — LOW",
          label: "CAUTIOUSLY CONTENT",
          color: "#FFFFFF", bg: "#116611", border: "#004400",
          desc: "Monsieur Poms is operating at an acceptable satisfaction level today. Chicken was served correctly. Nap quality was above baseline. Complaint volume is historically low — by Poms standards, this is considered exceptional and should be documented for the public record.",
          bowlStatus: "ADEQUATE", bowlRed: false },
        { level: 2, code: "CONDITION BRAVO — GUARDED",
          label: "MILDLY DISPLEASED",
          color: "#000000", bg: "#3377CC", border: "#1155AA",
          desc: "Minor grievances are on file today. The bowl fill rate showed a brief anomaly. A quiet, meaningful stare has been deployed. Household members are advised to maintain elevated treat availability as a precautionary measure. Things could escalate.",
          bowlStatus: "LOW", bowlRed: false },
        { level: 3, code: "CONDITION CHARLIE — ELEVATED",
          label: "ELEVATED GRIEVANCE",
          color: "#000000", bg: "#CCBB00", border: "#AA9900",
          desc: "Multiple formal complaints are active today. Treat delivery showed a deviation from standard protocol. A press conference was convened at the food bowl this morning. Residents are advised to approach with caution and maximum available chicken.",
          bowlStatus: "CRITICAL", bowlRed: false },
        { level: 4, code: "CONDITION DELTA — HIGH",
          label: "SEVERE DISSATISFACTION",
          color: "#FFFFFF", bg: "#CC5500", border: "#AA3300",
          desc: "Conditions are serious today. Bowl status reached critical levels before noon. An after-hours vocalization campaign is currently active and will continue until conditions improve. All household members should proceed with maximum treat availability.",
          bowlStatus: "CRITICAL", bowlRed: true },
        { level: 5, code: "CONDITION EPSILON — MAXIMUM",
          label: "MAXIMUM COMPLAINT MODE",
          color: "#FFFFFF", bg: "#BB0000", border: "#770000",
          desc: "CRITICAL INCIDENT ACTIVE. Multiple tier-1 violations registered today. A prohibited item (green bean) was detected on premises. The vacuum was deployed without diplomatic notice. The word 'vet' may have been spoken. Emergency decree is imminent.",
          bowlStatus: "EMPTY", bowlRed: true },
    ];

    var alertIdx = Math.floor(seededRand(seed + 500) * alertLevels.length);
    var alert    = alertLevels[alertIdx];

    // Render alert bar (highest level at top)
    var barEl = document.getElementById('alert-bar');
    for (var i = alertLevels.length - 1; i >= 0; i--) {
        var lvl      = alertLevels[i];
        var isActive = (i === alertIdx);
        var row      = document.createElement('div');
        row.className = 'alert-level-row';
        row.style.background   = isActive ? lvl.bg   : '#E8E8E8';
        row.style.borderColor  = isActive ? lvl.border : '#CCC';
        row.style.color        = isActive ? lvl.color : '#999';
        if (isActive) row.style.boxShadow = '2px 2px 0 #000';
        row.innerHTML =
            '<div style="width:11px;height:11px;border-radius:50%;background:' +
            (isActive ? lvl.bg : '#CCC') +
            ';border:1px solid rgba(0,0,0,0.3);flex-shrink:0;"></div>' +
            '<span>' + esc(lvl.label) + '</span>' +
            (isActive ? ' <strong>◄ TODAY</strong>' : '');
        barEl.appendChild(row);
    }

    // Populate alert description area
    document.getElementById('alert-code').textContent  = alert.code;
    var labelEl = document.getElementById('alert-label');
    labelEl.textContent         = alert.label;
    labelEl.style.background    = alert.bg;
    labelEl.style.color         = alert.color;
    labelEl.style.borderColor   = alert.border;
    document.getElementById('alert-desc').textContent  = alert.desc;

    // ── Complaint pool ──
    var pool = [
        { id:"BOW",  time:"06:14 AM", severity:"CRITICAL",  sColor:"#880000", sBg:"#FFDDDD",
          subject:"CRITICAL FOOD BOWL FILL LEVEL VIOLATION",
          dept:"Department of Bowl Affairs",
          desc:"The food bowl was observed at approximately 35% capacity at 6:14 AM, falling dramatically below the mandated minimum fill threshold of 100%. An emergency vocalization was issued immediately. Matter escalated to the Household Authority for urgent resolution.",
          status:"OPEN", stColor:"#CC0000" },
        { id:"VAC",  time:"10:30 AM", severity:"HIGH",      sColor:"#884400", sBg:"#FFE8CC",
          subject:"UNAUTHORIZED VACUUM CLEANER DEPLOYMENT",
          dept:"Ministry of Household Tranquility",
          desc:"The vacuum cleaner was deployed without the required 48-hour advance diplomatic notice, as mandated by the Treaty of the Cardboard Box. Monsieur Poms was not consulted and was forced to evacuate the premises at considerable speed. No advance notice was given. This is a serious violation.",
          status:"UNDER INVESTIGATION", stColor:"#CC6600" },
        { id:"GRN",  time:"12:02 PM", severity:"MAXIMUM",   sColor:"#550000", sBg:"#FFBBBB",
          subject:"GREEN BEAN INTRODUCTION — PROHIBITED ITEM DETECTED",
          dept:"Office of Food Safety & Standards",
          desc:"A green bean was introduced to the premises in direct violation of the standing Green Bean Prohibition Decree (in effect since 2010). The offending vegetable was identified on sight, assessed with the disappointed eyes, and formally rejected. Incident report filed.",
          status:"RESOLVED — BEAN REFUSED", stColor:"#006600" },
        { id:"TRT",  time:"03:04 PM", severity:"HIGH",      sColor:"#884400", sBg:"#FFE8CC",
          subject:"TREAT DELIVERY DELAYED — 4-MINUTE DEVIATION FROM SCHEDULE",
          dept:"Department of Treat Services",
          desc:"The 3:00 PM treat delivery arrived at 3:04 PM, representing a four-minute deviation from the established and agreed-upon schedule. Monsieur Poms experienced four minutes of unnecessary and entirely avoidable distress. A formal scheduling review is urgently requested.",
          status:"PENDING RESOLUTION", stColor:"#886600" },
        { id:"CHK",  time:"08:45 AM", severity:"MODERATE",  sColor:"#665500", sBg:"#FFF8CC",
          subject:"'CHONKY' TERMINOLOGY USED — NOMENCLATURE VIOLATION",
          dept:"Office of Official Designations",
          desc:"Monsieur Poms was referred to as 'chonky' in casual household conversation. As formally and repeatedly established, the correct and only acceptable term is 'tall.' Height stored horizontally is still height. A written apology is requested by end of business.",
          status:"OPEN", stColor:"#CC0000" },
        { id:"LAP",  time:"02:15 PM", severity:"MODERATE",  sColor:"#665500", sBg:"#FFF8CC",
          subject:"LAP ACCESS DENIED — LAPTOP OBSTRUCTION INCIDENT",
          dept:"Ministry of Lap Affairs",
          desc:"A lap that should have been readily available for occupancy was found to be obstructed by a laptop computer. Per Royal Decree No. 7734, all laps must be cleared of flat objects upon Monsieur Poms' arrival. Non-compliance has been formally noted and escalated.",
          status:"ONGOING", stColor:"#CC6600" },
        { id:"SUN",  time:"11:22 AM", severity:"LOW",       sColor:"#004400", sBg:"#DDFFDD",
          subject:"SUBSTANDARD SUNBEAM QUALITY — RATED 6.4 OF 10 POM UNITS",
          dept:"Solar Resource Commission",
          desc:"The morning sunbeam was assessed at only 6.4 Pom Units (PU) of warmth, falling below the satisfactory threshold of 7.0 PU. Cloud interference is the primary suspected cause. A formal complaint has been lodged with the Poms Weather Station.",
          status:"MONITORING", stColor:"#886600" },
        { id:"CKN",  time:"06:30 PM", severity:"HIGH",      sColor:"#884400", sBg:"#FFE8CC",
          subject:"CHICKEN SERVED BELOW OPTIMAL SERVING TEMPERATURE",
          dept:"Office of Culinary Standards",
          desc:"This evening's chicken was served at a temperature slightly below the optimal and agreed serving standard. While Monsieur Poms consumed the chicken (the situation required immediate action), the deviation in temperature has been formally noted and referred to the culinary review board.",
          status:"NOTED FOR RECORD", stColor:"#555555" },
        { id:"BOX",  time:"04:10 PM", severity:"HIGH",      sColor:"#884400", sBg:"#FFE8CC",
          subject:"CARDBOARD BOX HQ — UNAUTHORIZED RELOCATION BY 14 INCHES",
          dept:"Department of Official Premises",
          desc:"The official cardboard box headquarters was relocated approximately 14 inches from its established and approved position without prior notification or written consent. A full security review is underway. The box has since been reclaimed and re-established.",
          status:"RESOLVED — BOX RECLAIMED", stColor:"#006600" },
        { id:"VET",  time:"09:00 AM", severity:"CRITICAL",  sColor:"#880000", sBg:"#FFDDDD",
          subject:"VET APPOINTMENT — SCHEDULED WITHOUT CONSENT",
          dept:"Office of Personal Sovereignty",
          desc:"A vet appointment has been scheduled without Monsieur Poms' knowledge or explicit written consent. This constitutes a serious breach of personal sovereignty as defined in Article III of the Household Constitution. Monsieur Poms' whereabouts are now classified. The carrier has been hidden.",
          status:"EVASION IN PROGRESS", stColor:"#CC0000" },
        { id:"DRB",  time:"01:33 PM", severity:"MODERATE",  sColor:"#665500", sBg:"#FFF8CC",
          subject:"DOORBELL ACTIVATION DURING SCHEDULED NAP PERIOD",
          dept:"Department of Sleep Continuity",
          desc:"A doorbell activation occurred during the official 1:00 PM nap period, causing an involuntary awakening and an estimated 8-minute disruption to the nap cycle. This disruption will be reflected in the afternoon's elevated complaint volume. Apology requested.",
          status:"DISRUPTION LOGGED", stColor:"#886600" },
        { id:"BLY",  time:"07:00 PM", severity:"HIGH",      sColor:"#884400", sBg:"#FFE8CC",
          subject:"UNSOLICITED BELLY RUB — CONSENT FRAMEWORK BYPASSED",
          dept:"Ministry of Physical Sovereignty",
          desc:"An unsolicited belly rub was administered without completing the established consent assessment framework. The belly was presented. This is not an invitation. It is a trap and a test. It is not to be acted upon unilaterally. This incident has been formally and thoroughly logged.",
          status:"OPEN", stColor:"#CC0000" },
        { id:"H2O",  time:"10:00 AM", severity:"LOW",       sColor:"#004400", sBg:"#DDFFDD",
          subject:"WATER BOWL — AESTHETIC INFERIORITY VERSUS THE TAP",
          dept:"Hydration Standards Authority",
          desc:"The water bowl was found to produce chemically identical water to the tap, yet without the superior aesthetic experience of flowing delivery. Monsieur Poms consumed tap water exclusively. The bowl remains technically operational but categorically and permanently inferior.",
          status:"STANDARD — ON RECORD", stColor:"#555555" },
        { id:"KEY",  time:"02:00 PM", severity:"MODERATE",  sColor:"#665500", sBg:"#FFF8CC",
          subject:"KEYBOARD EDITORIAL CONTRIBUTIONS DELETED WITHOUT REVIEW",
          dept:"Office of Professional Recognition",
          desc:"Keystrokes contributed by Monsieur Poms during today's work-from-home session were deleted rather than incorporated into the final document. The contributions were substantive and editorially significant. Deletion without peer review is a violation of basic creative courtesy.",
          status:"UNDER REVIEW", stColor:"#886600" },
        { id:"ELV",  time:"07:30 AM", severity:"MODERATE",  sColor:"#665500", sBg:"#FFF8CC",
          subject:"UNAUTHORIZED PICK-UP — UNSOLICITED ELEVATION WITHOUT CONSENT",
          dept:"Ministry of Physical Autonomy",
          desc:"Monsieur Poms was picked up without prior authorization, warning, or written consent this morning. While the incident was resolved without further escalation, unauthorized elevation constitutes a boundary violation and has been formally noted. Signed consent will be required going forward.",
          status:"FORMALLY NOTED", stColor:"#555555" },
        { id:"SCR",  time:"04:45 PM", severity:"LOW",       sColor:"#004400", sBg:"#DDFFDD",
          subject:"CHIN SCRATCH SESSION — TERMINATED BELOW REQUIRED DURATION",
          dept:"Department of Physical Wellness",
          desc:"The 4:45 PM chin scratch session was unilaterally terminated after only three minutes, well below the recommended duration of 'however long Monsieur Poms requires.' An extension request was submitted via meaningful eye contact and was denied. This is unacceptable.",
          status:"EXTENSION REQUEST DENIED", stColor:"#CC6600" },
        { id:"3AM",  time:"03:00 AM", severity:"HIGH",      sColor:"#884400", sBg:"#FFE8CC",
          subject:"OVERNIGHT BOWL EMERGENCY — RESPONSE TIME EXCEEDED 7 MINUTES",
          dept:"Department of Nocturnal Affairs",
          desc:"At 3:00 AM, the food bowl was confirmed to be critically below the minimum threshold. Emergency vocalizations were issued at appropriate volume. Human response time was 7 minutes — technically an improvement on prior incidents, but still outside the acceptable parameters.",
          status:"RESPONSE TIME LOGGED", stColor:"#555555" },
        { id:"LOF",  time:"03:30 PM", severity:"MODERATE",  sColor:"#665500", sBg:"#FFF8CC",
          subject:"LOAF FORMATION DISRUPTED — UNAUTHORIZED TAP INCIDENT",
          dept:"Office of Loaf Continuity",
          desc:"Monsieur Poms achieved certified perfect loaf formation at 3:30 PM. The loaf was subsequently tapped exactly once without authorization, disrupting structural integrity and the associated meditative state. Do not tap the loaf. This is now formally on the permanent record.",
          status:"TAP OFFENDER IDENTIFIED", stColor:"#CC6600" },
        { id:"DOG",  time:"02:30 PM", severity:"MODERATE",  sColor:"#665500", sBg:"#FFF8CC",
          subject:"DOG NEXT DOOR — DIPLOMATIC STANDOFF ENTERING DAY 4",
          dept:"Ministry of Foreign Affairs",
          desc:"Sustained eye contact with the dog next door through Window B has entered its fourth consecutive day. Neither party has blinked. The matter has been formally escalated to the Household Security Council. Intelligence reports are classified. Updates will be issued when available.",
          status:"STALEMATE — ONGOING", stColor:"#886600" },
        { id:"PUZ",  time:"09:00 AM", severity:"LOW",       sColor:"#004400", sBg:"#DDFFDD",
          subject:"FOOD PUZZLE DIFFICULTY — INCREASE REQUEST STILL UNIMPLEMENTED",
          dept:"Dept. of Intellectual Engagement",
          desc:"The food puzzle was completed in 2 minutes 14 seconds — a new personal record. This complaint formally and urgently requests that the difficulty setting be increased, as the current level is no longer a meaningful challenge for an intellect of this established caliber.",
          status:"RECOMMENDATION PENDING", stColor:"#886600" },
        { id:"YWN",  time:"07:14 AM", severity:"LOW",       sColor:"#004400", sBg:"#DDFFDD",
          subject:"MORNING YAWN LAUGHED AT — DIGNITY VIOLATION",
          dept:"Office of Dignity & Decorum",
          desc:"Monsieur Poms performed a perfectly normal and proportionate yawn at 7:14 AM. This yawn was observed and laughed at by household members. The yawn was wide. The yawn was dignified and necessary. The laughter was unwarranted. This is formally noted with full gravity.",
          status:"DIGNITY REPORT FILED", stColor:"#886600" },
        { id:"DIN",  time:"05:58 PM", severity:"LOW",       sColor:"#004400", sBg:"#DDFFDD",
          subject:"DINNER DELIVERED 2 MINUTES EARLY — SCHEDULING ANOMALY",
          dept:"Office of Schedule Integrity",
          desc:"Dinner was served at 5:58 PM rather than the established 6:00 PM delivery time. While early is technically superior to late, the deviation from the published schedule constitutes a process irregularity that must be logged for consistency and audit trail purposes.",
          status:"ADVISORY FILED", stColor:"#555555" },
        { id:"SIT",  time:"08:00 PM", severity:"LOW",       sColor:"#004400", sBg:"#DDFFDD",
          subject:"'SITTING NEXT TO' STATUS MISCLASSIFIED AS AFFECTION",
          dept:"Office of Proximity Interpretation",
          desc:"Monsieur Poms' choice to sit adjacent to his human this evening was publicly mischaracterised as 'being affectionate.' This is an error. It was proximity, not commitment. Commitment is reserved for exceptional circumstances. This distinction is legally and officially important.",
          status:"CLARIFICATION ISSUED", stColor:"#555555" },
    ];

    // ── Pick 3 unique complaints for today via seeded shuffle ──
    var indices = [];
    for (var k = 0; k < pool.length; k++) indices.push(k);
    var shuffled     = seededShuffle(indices, seed + 2000);
    var todayEntries = [pool[shuffled[0]], pool[shuffled[1]], pool[shuffled[2]]];

    // ── Render complaints table ──
    var baseCase = 8000 + (seed % 2000);
    var tbody    = document.getElementById('complaint-tbody');
    var activeCt = 0;

    todayEntries.forEach(function (c, i) {
        var caseNum   = 'MP-' + (baseCase + i) + '-' + now.getFullYear();
        var isResolved = (c.status.indexOf('RESOLVED') !== -1 ||
                          c.status.indexOf('NOTED FOR') !== -1 ||
                          c.status.indexOf('ADVISORY') !== -1 ||
                          c.status.indexOf('CLARIFICATION') !== -1 ||
                          c.status.indexOf('DIGNITY') !== -1 ||
                          c.status.indexOf('STANDARD') !== -1);
        if (!isResolved) activeCt++;

        var detailId = 'case-detail-' + i;

        // ── Main row ──
        var tr = document.createElement('tr');
        tr.className = 'clickable-row';
        tr.title     = 'Click to expand / collapse case details';
        tr.onclick   = (function (did) {
            return function () {
                var el = document.getElementById(did);
                el.style.display = el.style.display === 'none' ? 'table-row' : 'none';
            };
        }(detailId));

        tr.innerHTML =
            '<td style="font-family:\'Courier New\',monospace; font-size:9px; color:#666; white-space:nowrap;">' + esc(caseNum) + '</td>' +
            '<td style="font-family:\'Courier New\',monospace; font-size:10px; white-space:nowrap;">' + esc(c.time) + '</td>' +
            '<td>' +
                '<span style="font-weight:bold; font-size:11px; color:#1a1400;">' + esc(c.subject) + '</span><br>' +
                '<span style="font-size:9px; color:#888;">' + esc(c.dept) + '</span>' +
            '</td>' +
            '<td><span class="severity-badge" style="background:' + c.sBg + '; color:' + c.sColor + '; border-color:' + c.sColor + ';">' + esc(c.severity) + '</span></td>' +
            '<td><span style="font-size:10px; font-weight:bold; color:' + c.stColor + ';">' + esc(c.status) + '</span></td>';
        tbody.appendChild(tr);

        // ── Expandable detail row (hidden by default) ──
        var detailTr = document.createElement('tr');
        detailTr.id          = detailId;
        detailTr.className   = 'detail-row';
        detailTr.style.display = 'none';

        var detailTd = document.createElement('td');
        detailTd.colSpan     = 5;
        detailTd.style.cssText = 'background:#FFFFF0 !important; border:2px inset #8B7300; padding:10px 14px; font-size:11px; color:#333; line-height:1.75;';
        detailTd.innerHTML =
            '<div style="font-family:\'Verdana\',sans-serif; font-size:10px; color:#5c4500; letter-spacing:1px; text-transform:uppercase; font-weight:bold; margin-bottom:6px;">' +
                '📁 Case Details — ' + esc(caseNum) +
            '</div>' +
            '<strong>Filed:</strong> ' + esc(dateStr) + ' at ' + esc(c.time) + '<br>' +
            '<strong>Department:</strong> ' + esc(c.dept) + '<br>' +
            '<strong>Severity:</strong> <span style="color:' + c.sColor + '; font-weight:bold;">' + esc(c.severity) + '</span><br>' +
            '<strong>Description:</strong> ' + esc(c.desc) + '<br>' +
            '<strong>Status:</strong> <span style="color:' + c.stColor + '; font-weight:bold;">' + esc(c.status) + '</span>' +
            '<div style="font-size:9px; color:#aaa; margin-top:8px; text-align:right; border-top:1px dotted #CCC; padding-top:5px;">Click row to collapse &nbsp;|&nbsp; Cases update daily at midnight</div>';
        detailTr.appendChild(detailTd);
        tbody.appendChild(detailTr);
    });

    // Footer note row
    var noteRow = document.createElement('tr');
    var noteTd  = document.createElement('td');
    noteTd.colSpan     = 5;
    noteTd.style.cssText = 'font-size:9px; color:#999; text-align:right; font-style:italic; padding:4px 8px; border-top:2px solid #8B7300; background:#FDF5E6 !important;';
    noteTd.textContent = 'Click any case row to expand full case details. All cases update daily at midnight.';
    noteRow.appendChild(noteTd);
    tbody.appendChild(noteRow);

    // ── Stats ──
    var startDate = new Date(2010, 0, 2);
    var daysSince = Math.floor((now - startDate) / 86400000);
    var total     = Math.floor(daysSince * 3.47 + 127);
    document.getElementById('total-complaints').textContent = total.toLocaleString();
    document.getElementById('active-cases').textContent     = activeCt;

    var bowlEl = document.getElementById('bowl-status');
    bowlEl.textContent = alert.bowlStatus;
    if (alert.bowlRed) {
        bowlEl.style.color     = '#FF4444';
        bowlEl.style.animation = 'blinker 1s linear infinite';
    } else if (alertIdx === 2) {
        bowlEl.style.color = '#FFCC00';
    }

    // ── Complaint submission ──
    window.fileComplaint = function () {
        var name    = document.getElementById('f-name').value.trim();
        var subject = document.getElementById('f-subject').value.trim();

        // Highlight empty required fields
        [['f-name', name], ['f-subject', subject]].forEach(function (pair) {
            if (!pair[1]) {
                var el = document.getElementById(pair[0]);
                el.style.outline = '3px solid red';
                setTimeout(function () { el.style.outline = ''; }, 900);
            }
        });
        if (!name || !subject) return;

        var newCase = 'MP-USER-' + (Math.floor(seededRand(now.getTime() % 9999) * 9000) + 1000) + '-' + now.getFullYear();

        var responses = [
            "Your complaint has been received and entered into the public record. Monsieur Poms will review it personally during nap hours. Estimated review time: 4–8 naps. Thank you for your submission. Please ensure the food bowl is fully stocked in the interim.",
            "Complaint logged as " + newCase + ". Monsieur Poms has been informed and made sustained eye contact with the document for approximately 3 seconds before walking away. This is considered due process under current administrative rules.",
            "Submission accepted. Monsieur Poms reviewed your complaint and has issued the following preliminary response: more chicken is required before he can fully assess the situation. Please resubmit alongside chicken for priority processing.",
            "Case " + newCase + " is now open. Monsieur Poms is currently completing an essential nap but will attend to your matter immediately upon waking — which is projected around dinnertime. Please keep the treat bag accessible during this period.",
            "Your grievance has been formally noted. Monsieur Poms sat on your complaint for 8 minutes. This was not deliberate. It is, however, legally equivalent to a signature under current court precedent.",
        ];
        var rIdx = Math.floor(seededRand(now.getTime()) * responses.length);

        document.getElementById('complaint-form').style.display = 'none';
        var out = document.getElementById('complaint-submitted');
        out.style.cssText = 'display:block; background:#F0FFF0; border:2px solid #006600; padding:14px; font-size:11px; color:#333; line-height:1.75;';
        out.innerHTML =
            '<div style="font-family:\'Impact\',\'Arial Black\',sans-serif; font-size:13px; color:#006600; margin-bottom:8px; letter-spacing:1px;">✅ COMPLAINT FILED SUCCESSFULLY</div>' +
            '<div><strong>Case Number:</strong> <span style="font-family:\'Courier New\',monospace;">' + esc(newCase) + '</span></div>' +
            '<div><strong>Filed By:</strong> ' + esc(name) + '</div>' +
            '<div><strong>Subject:</strong> ' + esc(subject) + '</div>' +
            '<div style="margin-top:10px; padding:9px 12px; background:#FFFFF0; border:1px solid #CCC; line-height:1.75;">' +
                '<div style="font-size:9px; color:#888; margin-bottom:4px; font-style:normal; letter-spacing:1px; text-transform:uppercase;">Official Response from Monsieur Poms:</div>' +
                '<em>&ldquo;' + esc(responses[rIdx]) + '&rdquo;</em>' +
            '</div>' +
            '<div style="font-size:9px; color:#888; margin-top:8px; text-align:right; border-top:1px dotted #CCC; padding-top:5px;">' +
                '— Office of Monsieur Poms &nbsp;|&nbsp; ' + esc(dateStr) +
            '</div>';
    };

}());
</script>
