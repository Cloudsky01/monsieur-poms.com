---
title: "Daily Nap Report"
---

<style>
.naplog-header-strip {
    background: linear-gradient(to right, #1a3a1a, #2d5a2d, #1a3a1a);
    color: #c8e6c8;
    text-align: center;
    padding: 14px 10px;
    margin: -10px -10px 0 -10px;
    border-bottom: 3px solid #5a9a5a;
}

.form-paper {
    background: linear-gradient(to bottom, #FEFCF0, #FAF6E4, #FEFCF0);
    border: 2px solid #333;
    padding: 22px 26px;
    margin: 14px 0;
    font-family: 'Courier New', monospace;
    box-shadow: 4px 4px 0 #888, inset 0 0 30px rgba(180,160,80,0.07);
    position: relative;
}

.form-section-header {
    background: #2a2a2a;
    color: #FFF;
    font-family: 'Verdana', sans-serif;
    font-size: 9px;
    font-weight: bold;
    letter-spacing: 3px;
    text-transform: uppercase;
    padding: 4px 10px;
    margin: 14px -26px 0;
}

.form-row {
    display: flex;
    align-items: flex-start;
    border-bottom: 1px solid #aaa;
    padding: 5px 2px;
    gap: 10px;
    min-height: 28px;
}

.form-label {
    font-size: 8px;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: #555;
    font-family: 'Verdana', sans-serif;
    font-weight: bold;
    width: 155px;
    flex-shrink: 0;
    line-height: 1.35;
    padding-top: 3px;
}

.form-value {
    font-size: 12px;
    color: #000080;
    font-family: 'Courier New', monospace;
    flex: 1;
    font-weight: bold;
    line-height: 1.45;
}

.star-on  { color: #BB5500; font-size: 17px; }
.star-off { color: #BBBBBB; font-size: 17px; }

.cb-row {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
    padding: 6px 2px 4px;
    border-bottom: 1px solid #aaa;
}

.cb-item {
    font-size: 11px;
    font-family: 'Courier New', monospace;
    color: #333;
    display: flex;
    align-items: center;
    gap: 4px;
}

.cb-box {
    width: 13px;
    height: 13px;
    border: 2px solid #444;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    font-size: 10px;
    font-weight: bold;
    color: #000080;
    line-height: 1;
    flex-shrink: 0;
}

.stamp {
    position: absolute;
    top: 34px;
    right: 18px;
    border: 4px solid red;
    color: red;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 20px;
    letter-spacing: 3px;
    padding: 5px 10px;
    transform: rotate(-12deg);
    opacity: 0.5;
    pointer-events: none;
    text-align: center;
    line-height: 1.2;
}

.official-seal {
    display: inline-flex;
    width: 78px;
    height: 78px;
    border-radius: 50%;
    background: radial-gradient(circle at 38% 33%, #8B4513, #5c2d0a 60%);
    border: 4px solid #8B4513;
    align-items: center;
    justify-content: center;
    font-size: 32px;
    box-shadow: 2px 2px 8px rgba(0,0,0,0.3), inset 0 2px 8px rgba(255,180,60,0.15);
    outline: 3px dashed rgba(139,69,19,0.55);
    outline-offset: 4px;
}

.sig-line {
    font-family: 'Georgia', serif;
    font-size: 24px;
    font-style: italic;
    color: #000080;
    border-bottom: 1px solid #333;
    display: inline-block;
    padding: 0 24px 2px 2px;
    margin-bottom: 3px;
    letter-spacing: 1px;
}

@keyframes napReveal {
    from { opacity: 0; transform: translateY(-6px); }
    to   { opacity: 1; transform: translateY(0); }
}
.nap-reveal { animation: napReveal 0.45s ease-out forwards; }
</style>

<div style="border: 1px solid #CCC; overflow: hidden; margin-bottom: 20px; background: #F9F9F9;">

<div class="naplog-header-strip">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 26px; letter-spacing: 4px; text-shadow: 1px 1px 0 #000;">
        📋 OFFICIAL DAILY NAP REPORT 📋
    </div>
    <div style="font-size: 10px; color: #99CC99; margin-top: 5px; letter-spacing: 3px; text-transform: uppercase;">
        Filed by the Office of Monsieur Poms · Updated Every Midnight
    </div>
</div>

<div style="background: #DFF0DF; border-bottom: 3px double #5a9a5a; padding: 6px 12px; font-size: 10px; color: #1a4a1a; text-align: center;">
    CATEGORY: Official Documentation &amp; Records &nbsp;|&nbsp; Dept. of Nap Affairs, Office of M. Poms &nbsp;|&nbsp; Est. 2010 &nbsp;|&nbsp; Today: <strong id="naplog-date"></strong>
</div>

<div style="padding: 14px;">

<p style="font-size: 11px; color: #444; text-align: center; line-height: 1.75; font-style: italic;">
    Each day, Monsieur Poms files an official report documenting the quality, duration, and conditions of his primary nap session.<br>
    These records are maintained for administrative, archival, and potential future legal proceedings, as appropriate.<br>
    Reports are legally binding in all jurisdictions where chicken is the official currency.
</p>

<div class="form-paper nap-reveal" id="nap-form">

    <!-- Header row -->
    <div style="display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 14px; gap: 12px;">
        <div>
            <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 15px; letter-spacing: 3px; color: #1a3a1a; text-transform: uppercase;">
                Department of Nap Affairs
            </div>
            <div style="font-size: 8px; font-family: 'Verdana', sans-serif; color: #555; letter-spacing: 2px; margin-top: 3px; text-transform: uppercase;">
                Official Household Nap Activity Report — Form NR-7
            </div>
            <div style="font-size: 9px; font-family: 'Courier New', monospace; color: #777; margin-top: 4px;">
                Session No. <span id="session-num" style="font-weight:bold; color:#333;"></span>
            </div>
        </div>
        <div class="official-seal" style="flex-shrink:0;">🐾</div>
    </div>

    <div class="form-section-header">Section A — Session Identification</div>

    <div class="form-row">
        <div class="form-label">Reporting Entity</div>
        <div class="form-value">MONSIEUR POMS (Primary Napper & Sole Authority)</div>
    </div>
    <div class="form-row">
        <div class="form-label">Date of Report</div>
        <div class="form-value" id="form-date-val"></div>
    </div>
    <div class="form-row">
        <div class="form-label">Session Classification</div>
        <div class="form-value" id="session-class-val"></div>
    </div>
    <div class="form-row">
        <div class="form-label">Nap Initiated At</div>
        <div class="form-value" id="nap-start-val"></div>
    </div>
    <div class="form-row" style="border-bottom: none;">
        <div class="form-label">Approx. Duration</div>
        <div class="form-value" id="nap-duration-val"></div>
    </div>

    <div class="form-section-header">Section B — Position &amp; Location</div>

    <div class="form-row">
        <div class="form-label">Position Classification</div>
        <div class="form-value" id="nap-position-val"></div>
    </div>
    <div class="form-row">
        <div class="form-label">Location on Record</div>
        <div class="form-value" id="nap-location-val"></div>
    </div>
    <div class="form-row">
        <div class="form-label">Sunbeam Status</div>
        <div class="form-value" id="sunbeam-val"></div>
    </div>

    <!-- Warmth checkboxes -->
    <div style="padding: 5px 2px 0;">
        <div class="form-label" style="margin-bottom: 5px;">Surface Warmth Sources</div>
        <div class="cb-row" id="warmth-boxes"></div>
    </div>

    <div class="form-section-header">Section C — Interruption Log</div>

    <div class="form-row">
        <div class="form-label">Interruptions Recorded</div>
        <div class="form-value" id="interruptions-val"></div>
    </div>
    <div class="form-row">
        <div class="form-label">Disruption Severity</div>
        <div class="form-value" id="disruption-severity-val"></div>
    </div>
    <div class="form-row" style="border-bottom: none;">
        <div class="form-label">Official Response Filed</div>
        <div class="form-value" id="official-response-val"></div>
    </div>

    <div class="form-section-header">Section D — Quality Assessment</div>

    <div class="form-row">
        <div class="form-label">Overall Nap Quality</div>
        <div class="form-value" id="quality-val"></div>
    </div>
    <div class="form-row">
        <div class="form-label">Star Rating (out of 5)</div>
        <div class="form-value" id="star-rating-val"></div>
    </div>
    <div class="form-row" style="border-bottom: none;">
        <div class="form-label">Official Field Notes</div>
        <div class="form-value" id="official-notes-val" style="font-weight: normal; font-size: 11px; line-height: 1.75; font-style: italic; color: #333;"></div>
    </div>

    <!-- Signature block -->
    <div style="border-top: 2px double #444; margin-top: 18px; padding-top: 14px; display: flex; justify-content: space-between; align-items: flex-end; flex-wrap: wrap; gap: 10px;">
        <div>
            <div class="sig-line">Monsieur Poms</div>
            <div style="font-size: 9px; font-family: 'Verdana', sans-serif; color: #555; line-height: 1.6; margin-top: 2px;">
                Signed: Monsieur Poms<br>
                Chief Nap Officer &amp; Sovereign Authority<br>
                Dept. of Nap Affairs, Household Division
            </div>
        </div>
        <div style="text-align: right; font-size: 9px; font-family: 'Courier New', monospace; color: #666; line-height: 1.75;">
            Date Filed: <span id="sig-date"></span><br>
            Form NR-7 (Rev. 2010)<br>
            Dept. of Nap Affairs<br>
            <strong style="color: #CC0000;" id="clearance-level"></strong>
        </div>
    </div>

</div>

<hr>
<p style="font-size: 10px; color: #888; text-align: center; line-height: 1.75;">
    <em>All nap reports are filed in triplicate and archived in the Official Cardboard Box Records Division.<br>
    Appeals regarding session quality or noted interruptions may be submitted via the Guestbook.<br>
    They will be reviewed during next available nap hours, which is to say: continuously and without urgency.<br>
    Green bean disturbances are automatically escalated to CRITICAL and referred to the press conference division.</em>
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
    var monthNames = ["January","February","March","April","May","June",
                      "July","August","September","October","November","December"];
    var dateStr = dayNames[now.getDay()] + ", " + monthNames[now.getMonth()] +
                  " " + now.getDate() + ", " + now.getFullYear();

    document.getElementById('naplog-date').textContent = dateStr;
    document.getElementById('form-date-val').textContent = dateStr;
    document.getElementById('sig-date').textContent = dateStr;

    var paddedDoy = String(doy).padStart(3, '0');
    document.getElementById('session-num').textContent =
        'NR-' + now.getFullYear() + '-' + paddedDoy;

    // ── Data pools ─────────────────────────────────────────────────────────

    var classifications = [
        "ROUTINE — Standard Post-Breakfast Morning Session",
        "TACTICAL — Pre-Dinner Strategic Rest Period",
        "EMERGENCY — Post-Vacuum Incident Recovery",
        "OPERATIONAL — Victory Nap Following Puzzle Defeat",
        "RESTORATIVE — Post-Extended Vocalization Recovery",
        "CEREMONIAL — Prime Sunbeam Occupation Protocol",
        "INTENSIVE — Marathon Duration Session (No Further Comment)",
        "ROUTINE — Standard Afternoon Decompression Nap",
        "CLASSIFIED — Classification: Classified. Do Not Inquire.",
        "TACTICAL — Pre-Zoomie Energy Conservation Protocol",
    ];

    var napTimes = [
        "9:03 AM — immediately following breakfast proceedings",
        "10:47 AM — post-morning surveillance, pre-lunch",
        "12:00 PM — noon strategic withdrawal",
        "2:18 PM — afternoon thermal management session",
        "4:00 PM — pre-dinner positioning and anticipation",
        "6:34 PM — post-dinner loaf formation initiation",
        "8:11 PM — evening consolidation nap",
        "Immediately after treat bag rustled — exact time classified",
        "Unknown — I was already there when noticed",
        "1:30 PM — scheduled according to my internal calendar",
    ];

    var durations = [
        "47 minutes (brief cycle — treat-related interruption suspected)",
        "2 hours, 14 minutes (standard issue session)",
        "3 hours, 40 minutes (extended — high quality achieved)",
        "1 hour, 22 minutes (tactical pause — main session pending)",
        "6 hours (marathon — no further comment will be offered)",
        "4 hours, 5 minutes (strategic stillness — precision maintained)",
        "Indeterminate — tracking was not attempted and will not be",
        "55 minutes (preliminary session — primary nap still incoming)",
        "3 hours exactly (not a coincidence; this was intentional)",
        "2 hours, 58 minutes (optimal household diplomacy window)",
    ];

    var positions = [
        "THE LOAF — All limbs fully and professionally tucked",
        "THE SPRAWL — Maximum territorial surface area coverage",
        "THE SHOULDER PRESS — Head on primary human shoulder",
        "THE KEYBOARD ANCHOR — Active laptop surface occupancy",
        "THE SUNBEAM STRETCH — Full-body solar alignment achieved",
        "THE BOX COIL — Standard cardboard box interior occupancy",
        "THE PILLOW CLAIM — Acquired without notice or negotiation",
        "THE LAP ANCHOR — Lap availability confirmed and secured",
        "THE DRAWER NEST — Open drawer: repurposed as operations base",
        "THE BOOKSHELF AUTHORITY — Top shelf, elevated position",
        "THE CLEAN LAUNDRY MOUNTAIN — Quality assurance protocol",
    ];

    var locations = [
        "Prime Sunbeam Position — Living Room Floor, Sector 3",
        "Human Pillow — Acquired under Standard Acquisition Protocol",
        "Official Cardboard Box HQ — Central Corridor, Door Left",
        "Sofa, Right Armrest — Prime Sovereign Territory (Claimed)",
        "Directly on the Laptop — Keyboard Occupancy Mode Active",
        "Bathroom Tile — Thermal Regulation Session (Cool Floor)",
        "Under the Bed — Private Strategy Meeting in Progress",
        "Kitchen Observation Ledge — Eyes Technically Open",
        "Inside the Laundry Basket — Active Quality Control Review",
        "Clean Laundry Pile — Claimed for Formal Assessment Purposes",
        "Top of Bookshelf — Elevated Surveillance + Premium Napping",
    ];

    var sunbeams = [
        "☀️ PRESENT AND SECURED — Full body coverage, uninterrupted",
        "☀️ PARTIAL — Beam migrated; repositioned twice. Acceptable.",
        "☁️ ABSENT — Overcast. Formally noted. Management will hear of this.",
        "☀️ OPTIMAL — Prime beam, perfect duration, zero disruption",
        "☀️ DETECTED — Angle suboptimal; claimed regardless. Standards.",
        "☀️ EXCELLENT — Thermal output: 9/10. Very satisfactory rating.",
        "☁️ UNAVAILABLE — Location selected for strategic reasons instead",
        "☀️ CONFIRMED — Location was chosen specifically for beam access",
        "☀️ LATE ARRIVAL — Beam appeared 22 minutes into session. Noted.",
    ];

    var warmthLabels = [
        "Sunbeam (Direct)", "Human Body Heat", "Ambient Lap Warmth",
        "Fresh Laundry Heap", "Radiator Proximity"
    ];

    // Interruptions with their matching severity + response
    var interruptionSets = [
        {
            interruption: "NONE — Flawless, uninterrupted session. Rare. Cherished.",
            severity:     "NONE — Perfect conditions maintained throughout",
            response:     "No response required — session was flawless"
        },
        {
            interruption: "1 — Vacuum cleaner incident. Evacuated under protest.",
            severity:     "HIGH — Formal complaint escalated to press conference",
            response:     "Disappointed Eyes deployed (Duration: 11 minutes). Report filed."
        },
        {
            interruption: "1 — Doorbell intrusion. Resolved via sustained withering stare.",
            severity:     "MODERATE — Sleep cycle disrupted. Compensation owed.",
            response:     "Stare of Judgment administered. Human compliance achieved."
        },
        {
            interruption: "1 — Human attempted to pick me up. This was addressed.",
            severity:     "HIGH — Breach of Nap Sovereignty Protocol",
            response:     "Formal memo dictated for the public record. Disappointment logged."
        },
        {
            interruption: "SUSPENDED — Treat bag rustled. Nap voluntarily abandoned.",
            severity:     "LOW — Suspension was self-initiated and completely worth it",
            response:     "No complaint filed — outcome was favourable."
        },
        {
            interruption: "1 — Bird Alert, Window B. Brief tactical pause. Session resumed.",
            severity:     "LOW — Interruption was classified as operationally necessary",
            response:     "Intelligence gathered. Nap resumed. Full debrief pending."
        },
        {
            interruption: "1 — Human checked 'if I was okay'. I was fine. I am still fine.",
            severity:     "MODERATE — Unnecessary wellness check, sleep cycle disturbed",
            response:     "Silent but meaningful look administered. Duration: 6 minutes."
        },
        {
            interruption: "2 — Phone vibration + human laughing. Two reports filed.",
            severity:     "HIGH — Compounded disruption. Press conference strongly likely.",
            response:     "Emergency Disappointed Eyes (Full Intensity). Incident logged."
        },
        {
            interruption: "NONE — All threats pre-emptively neutralised. No incidents.",
            severity:     "NONE — Threat assessment confirmed clear for full duration",
            response:     "No response required — this is what optimal looks like."
        },
        {
            interruption: "1 — Unknown hallway event. Nature: classified. Outcome: handled.",
            severity:     "MODERATE — Details remain classified at this time",
            response:     "Response: classified. I handled it. That is sufficient."
        },
    ];

    var qualities = [
        "EXCELLENT — Premium session. Conditions were optimal throughout.",
        "GOOD — Fully satisfactory. Minor environmental notes on file.",
        "EXCEPTIONAL — Best session of Q3. Possibly the year. Archive this.",
        "ADEQUATE — Completed successfully given the documented conditions.",
        "OUTSTANDING — No notes necessary. This is the benchmark.",
        "COMPROMISED — See Section C. Compensation remains outstanding.",
        "PERFECT — Category invented specifically for this rating. It is this.",
        "VERY GOOD — Above standard. Slight sunbeam migration noted only.",
        "REMARKABLE — Duration, position, and conditions all rated exemplary.",
    ];

    var officialNotes = [
        "The session was conducted with full professionalism and characteristic dignity. Ambient temperature was assessed upon arrival and confirmed acceptable. Duration exceeded the minimum standard. No further action is required at this time.",
        "Despite the noted interruption in Section C, composure was maintained throughout and operations resumed with minimal delay. This level of adaptability is to be formally noted in the household record as evidence of exceptional character.",
        "Today's session was, objectively, a personal milestone. The surface was ideal, the position precise, and the ambient temperature within my exacting specifications. I am satisfied. This is not a statement I make with any frequency.",
        "Session completed without incident. I would like it on the record that I was not asleep — I was engaged in eyes-closed strategic planning. The bowl situation and the treat schedule were both reviewed at length during this time.",
        "The sunbeam alignment this morning was, by any metric, perfect. I occupied it from the moment of arrival and held position for the full duration. This is called dedication. Please acknowledge this formally in your next household review.",
        "I was in the cardboard box. I will not be explaining further. I was comfortable, warm, and the investigation was proceeding according to plan. That is the complete statement and no additional disclosure will be forthcoming.",
        "Session quality was slightly affected by human proximity, which was tolerable. Not comfortable, not particularly welcome, but tolerable. Do not turn this into something it is not. I was cold. They were available. That is the full context.",
        "This was a preparation nap. The primary session is scheduled for later and will be of considerably greater duration. Please ensure bowl levels, lap availability, and sunbeam conditions are all optimised in advance of my arrival.",
        "Exceptional stillness was achieved and maintained. The loaf position was perfect. Four hours of zero movement was recorded. This is not laziness. This is a discipline that very few are capable of at this level. I do not expect you to fully understand.",
        "Despite the classified interruption noted in Section C, full operational continuity was maintained. Details of the incident and my response cannot be shared at this time. What I can confirm is that the situation has been fully handled.",
    ];

    var clearanceLevels = [
        "CLEARANCE: GENERAL PUBLIC",
        "CLEARANCE: HOUSEHOLD EYES ONLY",
        "CLEARANCE: HOUSEHOLD EYES ONLY",
        "CLEARANCE: CLASSIFIED",
        "CLEARANCE: CLASSIFIED",
        "CLEARANCE: GENERAL PUBLIC",
        "CLEARANCE: GENERAL PUBLIC",
        "CLEARANCE: HOUSEHOLD EYES ONLY",
        "CLEARANCE: GENERAL PUBLIC",
    ];

    // ── Pick today's values ────────────────────────────────────────────────

    var classification  = pick(classifications, seed + 1);
    var napTime         = pick(napTimes,        seed + 2);
    var duration        = pick(durations,       seed + 3);
    var position        = pick(positions,       seed + 4);
    var location        = pick(locations,       seed + 5);
    var sunbeam         = pick(sunbeams,        seed + 6);
    var intrSet         = pick(interruptionSets,seed + 7);
    var quality         = pick(qualities,       seed + 8);
    var starNum         = 3 + Math.floor(seededRand(seed + 9) * 3);  // 3, 4, or 5
    var notes           = pick(officialNotes,   seed + 10);
    var clearance       = pick(clearanceLevels, seed + 11);

    // ── Populate ──────────────────────────────────────────────────────────

    document.getElementById('session-class-val').textContent        = classification;
    document.getElementById('nap-start-val').textContent            = napTime;
    document.getElementById('nap-duration-val').textContent         = duration;
    document.getElementById('nap-position-val').textContent         = position;
    document.getElementById('nap-location-val').textContent         = location;
    document.getElementById('sunbeam-val').textContent              = sunbeam;
    document.getElementById('interruptions-val').textContent        = intrSet.interruption;
    document.getElementById('disruption-severity-val').textContent  = intrSet.severity;
    document.getElementById('official-response-val').textContent    = intrSet.response;
    document.getElementById('quality-val').textContent              = quality;
    document.getElementById('official-notes-val').textContent       = notes;
    document.getElementById('clearance-level').textContent          = clearance;

    // Star rating
    var starHTML = '';
    for (var i = 0; i < 5; i++) {
        starHTML += '<span class="' + (i < starNum ? 'star-on' : 'star-off') + '">★</span>';
    }
    starHTML += ' <span style="font-size:11px; color:#555;">(' + starNum + ' / 5)</span>';
    document.getElementById('star-rating-val').innerHTML = starHTML;

    // Warmth checkboxes — seeded
    var wBox = document.getElementById('warmth-boxes');
    warmthLabels.forEach(function (label, idx) {
        var checked = seededRand(seed + 20 + idx) > 0.42;
        var div = document.createElement('div');
        div.className = 'cb-item';
        div.innerHTML =
            '<span class="cb-box">' + (checked ? '&#x2713;' : '&nbsp;') + '</span> ' +
            esc(label);
        wBox.appendChild(div);
    });

    // Classified stamp overlay
    if (clearance === "CLEARANCE: CLASSIFIED") {
        var stamp = document.createElement('div');
        stamp.className = 'stamp';
        stamp.textContent = 'CLASSIFIED';
        document.getElementById('nap-form').appendChild(stamp);
    }
})();
</script>
