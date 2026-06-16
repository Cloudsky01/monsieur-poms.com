---
title: "Daily Report Card"
---

<style>
.rc-page {
    background: #fdf8ec;
    border: 1px solid #c8a96e;
    box-shadow: inset 0 0 40px rgba(180,130,60,0.08);
    padding: 0;
    margin-bottom: 20px;
    font-family: 'Verdana', 'Arial', sans-serif;
    position: relative;
}

.rc-letterhead {
    background: linear-gradient(to bottom, #1a3a6b 0%, #0e2550 100%);
    color: #fff;
    text-align: center;
    padding: 16px 14px 12px;
    border-bottom: 4px double #c8a044;
}

.rc-school-name {
    font-family: 'Georgia', serif;
    font-size: 17px;
    letter-spacing: 2px;
    font-weight: bold;
    text-transform: uppercase;
    text-shadow: 1px 1px 0 #000;
}

.rc-school-sub {
    font-size: 9px;
    color: #c8d8ff;
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-top: 3px;
}

.rc-school-seal {
    font-size: 32px;
    display: block;
    margin: 4px 0 0;
}

.rc-meta-strip {
    background: #f0e8d0;
    border-bottom: 2px solid #c8a96e;
    padding: 8px 16px;
    display: flex;
    flex-wrap: wrap;
    gap: 14px;
    font-size: 10px;
    color: #4a3010;
    font-family: 'Courier New', monospace;
}
.rc-meta-strip span { white-space: nowrap; }
.rc-meta-strip strong { color: #1a3a6b; }

.rc-confidential {
    position: absolute;
    top: 130px;
    right: 12px;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 26px;
    letter-spacing: 4px;
    color: rgba(180, 0, 0, 0.18);
    transform: rotate(-22deg);
    pointer-events: none;
    user-select: none;
    text-transform: uppercase;
    border: 5px solid rgba(180, 0, 0, 0.18);
    padding: 2px 8px;
    line-height: 1.1;
}

.rc-body {
    padding: 14px 16px;
}

.rc-section-title {
    font-family: 'Georgia', serif;
    font-size: 11px;
    font-weight: bold;
    color: #1a3a6b;
    text-transform: uppercase;
    letter-spacing: 2px;
    border-bottom: 1px solid #c8a96e;
    padding-bottom: 4px;
    margin: 14px 0 8px;
}

.rc-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 11px;
}

.rc-table th {
    background: #1a3a6b;
    color: #fff;
    font-family: 'Verdana', sans-serif;
    font-size: 9px;
    letter-spacing: 1px;
    text-transform: uppercase;
    padding: 5px 8px;
    text-align: left;
    border: 1px solid #0e2550;
}

.rc-table td {
    padding: 7px 8px;
    border: 1px solid #d4b882;
    vertical-align: top;
    color: #2a1800;
    line-height: 1.5;
}

.rc-table tr:nth-child(even) td {
    background: #faf3df;
}
.rc-table tr:nth-child(odd) td {
    background: #fdf8ec;
}

.rc-grade {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 20px;
    text-align: center;
    width: 42px;
    font-weight: bold;
}

.grade-a  { color: #006600; }
.grade-b  { color: #005599; }
.grade-c  { color: #886600; }
.grade-d  { color: #cc4400; }
.grade-f  { color: #cc0000; }

.rc-subject-name {
    font-weight: bold;
    font-size: 11px;
    color: #1a3a6b;
    display: block;
    margin-bottom: 1px;
}
.rc-subject-code {
    font-size: 9px;
    color: #886644;
    font-family: 'Courier New', monospace;
}

.rc-comment {
    font-family: 'Georgia', serif;
    font-size: 10px;
    font-style: italic;
    color: #3a2200;
    line-height: 1.6;
}

.rc-gpa-box {
    background: linear-gradient(to right, #0e2550, #1a3a6b);
    border: 2px solid #c8a044;
    color: #fff;
    padding: 10px 14px;
    margin: 14px 0 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 8px;
}

.rc-gpa-num {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 34px;
    color: #FFD700;
    text-shadow: 1px 1px 0 #000;
    letter-spacing: 2px;
    line-height: 1;
}

.rc-gpa-label {
    font-size: 9px;
    color: #AAC4FF;
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-top: 2px;
    font-family: 'Verdana', sans-serif;
}

.rc-standing {
    font-family: 'Georgia', serif;
    font-size: 14px;
    font-weight: bold;
    color: #FFD700;
    text-align: right;
    line-height: 1.4;
}

.rc-standing-sub {
    font-size: 9px;
    color: #AAC4FF;
    font-weight: normal;
    font-family: 'Verdana', sans-serif;
}

.rc-remarks-box {
    background: #fffbe8;
    border: 1px solid #d4b882;
    border-left: 4px solid #1a3a6b;
    padding: 9px 12px;
    font-family: 'Georgia', serif;
    font-size: 11px;
    font-style: italic;
    color: #2a1800;
    line-height: 1.7;
    margin: 10px 0;
}

.rc-signature-area {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 14px;
    padding-top: 10px;
    border-top: 1px dashed #c8a96e;
}

.rc-sig-block {
    text-align: center;
    font-size: 9px;
    color: #886644;
    font-family: 'Courier New', monospace;
}

.rc-sig-line {
    border-bottom: 1px solid #4a3010;
    width: 160px;
    margin-bottom: 3px;
    height: 24px;
    display: flex;
    align-items: flex-end;
    justify-content: center;
}

.rc-sig-name {
    font-family: 'Georgia', serif;
    font-style: italic;
    font-size: 13px;
    color: #1a3a6b;
    padding-bottom: 2px;
}

.rc-footer-strip {
    background: #1a3a6b;
    color: #AAC4FF;
    text-align: center;
    padding: 6px 10px;
    font-size: 9px;
    font-family: 'Courier New', monospace;
    letter-spacing: 1px;
    border-top: 2px solid #c8a044;
}

.rc-progress-bar-out {
    background: rgba(0,0,0,0.3);
    border: 1px inset rgba(255,255,255,0.2);
    height: 8px;
    flex: 1;
    min-width: 80px;
    overflow: hidden;
}
.rc-progress-bar-in {
    height: 100%;
    animation: rcBarFill 0.8s ease-out forwards;
}
@keyframes rcBarFill { from { width: 0%; } }
</style>

<div class="rc-page">

<div class="rc-letterhead">
    <span class="rc-school-seal">🏫</span>
    <div class="rc-school-name">Monsieur Poms Academy for Human Training</div>
    <div class="rc-school-sub">Official Progress Report &nbsp;·&nbsp; Issued Daily at Midnight &nbsp;·&nbsp; Est. 2010</div>
</div>

<div class="rc-confidential">CONFIDENTIAL</div>

<div class="rc-meta-strip">
    <span><strong>Student:</strong> The Household &amp; Its Inhabitants</span>
    <span><strong>Evaluator:</strong> Monsieur Poms, Dean of Standards</span>
    <span><strong>Term:</strong> <span id="rc-date-display">Loading...</span></span>
    <span><strong>Report #:</strong> <span id="rc-report-num"></span></span>
    <span><strong>Status:</strong> <span style="color:#cc0000; font-weight:bold;">FINAL</span></span>
</div>

<div class="rc-body">

<div class="rc-section-title">📋 Academic Performance</div>

<table class="rc-table">
    <thead>
        <tr>
            <th style="width:130px;">Subject</th>
            <th style="width:46px; text-align:center;">Grade</th>
            <th>Instructor's Comment</th>
        </tr>
    </thead>
    <tbody id="rc-grades-body"></tbody>
</table>

<div class="rc-gpa-box">
    <div>
        <div class="rc-gpa-num" id="rc-gpa">–.–</div>
        <div class="rc-gpa-label">Paw-Point Average (PPA)</div>
    </div>
    <div style="flex:1; min-width:120px; padding: 0 10px;">
        <div style="font-size:9px; color:#AAC4FF; margin-bottom:4px; font-family:'Verdana',sans-serif; letter-spacing:1px; text-transform:uppercase;">Overall Performance</div>
        <div style="display:flex; align-items:center; gap:6px;">
            <div class="rc-progress-bar-out">
                <div class="rc-progress-bar-in" id="rc-ppa-bar" style="background:linear-gradient(to right,#446699,#FFD700);"></div>
            </div>
            <span style="font-size:10px; color:#FFD700; font-family:'Courier New',monospace; white-space:nowrap;" id="rc-ppa-pct"></span>
        </div>
    </div>
    <div class="rc-standing">
        <span id="rc-standing-text">—</span><br>
        <span class="rc-standing-sub" id="rc-standing-sub">Academic Standing</span>
    </div>
</div>

<div class="rc-section-title">✍️ Dean's Remarks</div>
<div class="rc-remarks-box" id="rc-remarks">Loading...</div>

<div class="rc-signature-area">
    <div class="rc-sig-block">
        <div class="rc-sig-line"><span class="rc-sig-name">Monsieur Poms</span></div>
        Dean of Standards &amp; Chief Inspector<br>Monsieur Poms Academy
    </div>
    <div class="rc-sig-block">
        <div class="rc-sig-line"><span class="rc-sig-name" id="rc-sig-date"></span></div>
        Date of Issue
    </div>
    <div style="font-size:9px; color:#886644; font-family:'Courier New',monospace; text-align:right; line-height:1.6;">
        🔒 This report is confidential.<br>
        Disputes filed with the Dean<br>
        are not accepted or reviewed.<br>
        The grades are final.
    </div>
</div>

</div>

<div class="rc-footer-strip">
    Monsieur Poms Academy for Human Training &nbsp;|&nbsp; Report Card No. <span id="rc-footer-num"></span> &nbsp;|&nbsp; Next report issued at midnight &nbsp;|&nbsp; Green beans remain an F regardless of term
</div>

</div>

<script>
(function () {

function seededRand(s) {
    var x = Math.sin(s * 127.1 + 311.7) * 43758.5453123;
    return x - Math.floor(x);
}
function pick(arr, s) { return arr[Math.floor(seededRand(s) * arr.length)]; }

var now  = new Date();
var doy  = Math.floor((now - new Date(now.getFullYear(), 0, 0)) / 86400000);
var seed = now.getFullYear() * 1000 + doy;

var months  = ["January","February","March","April","May","June","July","August","September","October","November","December"];
var days    = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
var shortMonths = ["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"];

var dateStr  = days[now.getDay()] + ", " + months[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear();
var shortDate = shortMonths[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear();

document.getElementById('rc-date-display').textContent = dateStr;
document.getElementById('rc-report-num').textContent   = doy + 1;
document.getElementById('rc-sig-date').textContent     = shortDate;
document.getElementById('rc-footer-num').textContent   = doy + 1;

// ── Grade definitions ────────────────────────────────────────────────────────

var gradeDefs = [
    { label:"A+", css:"grade-a", gpa:4.3 },
    { label:"A",  css:"grade-a", gpa:4.0 },
    { label:"A−", css:"grade-a", gpa:3.7 },
    { label:"B+", css:"grade-b", gpa:3.3 },
    { label:"B",  css:"grade-b", gpa:3.0 },
    { label:"B−", css:"grade-b", gpa:2.7 },
    { label:"C+", css:"grade-c", gpa:2.3 },
    { label:"C",  css:"grade-c", gpa:2.0 },
    { label:"C−", css:"grade-c", gpa:1.7 },
    { label:"D",  css:"grade-d", gpa:1.0 },
    { label:"F",  css:"grade-f", gpa:0.0 }
];

// ── Subjects ─────────────────────────────────────────────────────────────────

var subjects = [
    {
        name: "Human Obedience",
        code: "HO-101",
        comments: [
            "Student complied with feeding schedule. Minor delays noted. Overall satisfactory.",
            "Feeding occurred on time but the portion was, frankly, optimistic at best. Further instruction required.",
            "The human forgot the second dinner. This is unprecedented. A formal incident report has been filed.",
            "Excellent responsiveness to the Stare Technique. Treat produced in under 90 seconds. Impressive.",
            "Human said 'in a minute' four times. There are no minutes. There is only now. We discussed this.",
            "Student showed improvement after last week's 3 AM vocal reminder. Growth noted.",
            "Human attempted to offer a green bean. This is a zero-tolerance violation. Grade adjusted accordingly.",
            "Immediate response to the Disappointed Eyes. The human is learning. This pleases me.",
            "Chicken was provided without negotiation today. This is the correct behaviour. Well done.",
            "The human left for six hours. Six. Hours. We will be discussing this at the next conference."
        ]
    },
    {
        name: "Food Quality",
        code: "FQ-201",
        comments: [
            "Chicken was served at the correct temperature. Texture: acceptable. Quantity: insufficient, but noted.",
            "The kibble was from the bag I prefer. This is the first correct decision this week.",
            "Wet food of unknown provenance was presented. I ate it. Under protest. Formal complaint pending.",
            "The food was late by eleven minutes. The flavour cannot compensate for the tardiness. It could not.",
            "Chicken again. This is the correct answer. The human is beginning to understand the assignment.",
            "A treat of excellent quality was produced unprompted. I consumed it in 0.4 seconds. Perfect execution.",
            "The bowl had a suspicious smell. Investigation inconclusive. I ate the adjacent portion only.",
            "Premium food, correct temperature, generous portion. My highest rating. Do not let this go to your head.",
            "Kibble was served with visible enthusiasm. The enthusiasm does not improve the kibble. Just so we know.",
            "The food puzzle was deployed again. I solved it. The indignity remains unresolved. See me after class."
        ]
    },
    {
        name: "Sunbeam Management",
        code: "SB-102",
        comments: [
            "Sunbeam was available from 9 AM to 1 PM. Position: prime. Duration: optimal. Well administered.",
            "The cloud cover interrupted my 10 AM session. This was not handled. A deficit in planning.",
            "Only one beam today, but its quality was exceptional. A narrow margin of excellence.",
            "Sunbeam position was suboptimal — shifted to the floor, not the couch. I adapted. Barely.",
            "Full-day beam across the east window. I occupied it in three rotations. Textbook performance.",
            "The blinds were left closed until noon. NOON. I sat in front of them and stated my position clearly.",
            "Two overlapping beams today. This is considered a celestial event. I handled both simultaneously.",
            "Beam quality was good but the couch cushion was not arranged correctly. Corrected by myself. Obviously.",
            "Morning beam was cold. Afternoon beam was warm. The transition was managed but barely acceptable.",
            "No beam today due to rain. The human offered a heated blanket. This was an acceptable substitute."
        ]
    },
    {
        name: "Lap Availability",
        code: "LA-303",
        comments: [
            "Lap was available and warm. I considered it for 14 minutes before occupying it. On my terms.",
            "Human stood up the moment I approached. Three times. This is not a coincidence. This is a pattern.",
            "Lap occupied for 47 consecutive minutes. The human remained very still. Full marks for cooperation.",
            "The laptop was on the lap again. I sat on the laptop. The laptop has been relocated. Crisis resolved.",
            "Human was on the phone. I occupied the lap anyway. The call was apparently 'important'. So was the lap.",
            "Lap was available but the position was incorrect. Adjusted the human manually. Result: acceptable.",
            "Lap offered proactively with a soft surface already arranged. This is growth. I am recording it.",
            "The human kept moving their legs. I communicated my displeasure via weight redistribution. Settled.",
            "Lap was warm and entirely available. I chose not to use it at this time. The option remains open.",
            "Human fell asleep on the couch. The lap became available without negotiation. Efficient outcome."
        ]
    },
    {
        name: "Bird Surveillance",
        code: "BS-401",
        comments: [
            "The bird returned to its previous position at 09:47. I was already there. Intelligence: superior.",
            "No bird activity today. Either the situation has been resolved or the enemy has adapted. Monitoring continues.",
            "Bird at Window B made sustained eye contact for four minutes. I did not blink. Winner: undisputed.",
            "A new bird appeared. Species: unknown. Threat level: elevated. File opened. Surveillance active.",
            "Bird departed at 11:14. Unknown destination. Investigation ongoing. I cannot share more at this time.",
            "Three birds today. This is an escalation. I have requested additional resources (treats, for focus).",
            "The bird situation has been stable for two days. I remain vigilant. Complacency is not an option.",
            "I detected the bird before it landed. Reaction time: 0.2 seconds. Performance: impeccable.",
            "Bird intelligence confirms ongoing presence. My position at the window remains fully operational.",
            "A squirrel appeared in addition to the bird. The threat matrix has been updated accordingly."
        ]
    },
    {
        name: "Noise Level (Household)",
        code: "NL-110",
        comments: [
            "Vacuum cleaner deployed without prior warning or written consent. This is a violation.",
            "Quiet all day. This is the correct environment for advanced napping. Full marks.",
            "Human had guests. Guests were loud. I relocated to the bedroom and filed three complaints.",
            "The phone rang at 7 AM. I was already awake, but this is beside the point. Still unacceptable.",
            "Household maintained acceptable silence from 2 PM to 5 PM during nap #4. Exactly right.",
            "Something fell in the kitchen at 3 AM. Investigation inconclusive. I did not do it. Officially.",
            "Music was played at an inappropriate volume. It was not Nyan Cat. I have noted this.",
            "The doorbell rang twice. I was startled once. The second ring I handled with complete composure.",
            "Respectful noise levels maintained throughout. The human spoke softly. The day was productive.",
            "Construction noise from outside. Not within the household's control, but still noted in the report."
        ]
    },
    {
        name: "Treat Distribution",
        code: "TD-205",
        comments: [
            "Two treats were produced at 3 PM. This is three fewer than the minimum acceptable quantity.",
            "Treat delivered unprompted and with correct timing. I acknowledge this. Do not get comfortable.",
            "No treats today. I am not angry. I am noting this for the record. For official purposes. Purely.",
            "The good treats were opened today. The chicken-flavoured ones. I have increased the overall rating.",
            "Treat was offered, then partially retracted as a 'reward'. Rewards are not conditional. We discussed this.",
            "Four treats in a single session. Unprecedented generosity. Rating adjusted. Narrowly.",
            "Treat produced after only two minutes of the Stare. The human is improving. Time: 1 minute 58 seconds.",
            "Treat was accompanied by a chin scratch. This is the correct pairing. Maximum efficiency.",
            "The treat bag was shaken but no treat emerged. This is a form of deception. I have it documented.",
            "Treats were provided at the agreed time with zero negotiation. This is what peak performance looks like."
        ]
    },
    {
        name: "Nap Infrastructure",
        code: "NI-307",
        comments: [
            "Blanket was folded incorrectly. I corrected it over nine minutes. No further incidents.",
            "The couch cushion was warm. The sunbeam aligned. The conditions were — I will say it — ideal.",
            "Someone sat in my primary nap location. I relocated them via the Long Stare. Resolution: successful.",
            "All five designated nap zones were available simultaneously. A very good infrastructure day.",
            "The bed was made with hospital corners. This is incompatible with napping. I unmade it immediately.",
            "New blanket introduced without prior consultation. I approved it after a 12-minute inspection.",
            "The cardboard box HQ was still in position. I conducted all four naps from within it today.",
            "Nap zone #3 (the armchair) had an unfamiliar smell. I sat next to it for 8 minutes. Then napped there.",
            "Human attempted to remove my blanket while I was on it. This matter is before the Academy tribunal.",
            "All nap surfaces maintained at correct temperature. Infrastructure team (the human) performed acceptably."
        ]
    }
];

// ── Dean's Remarks ────────────────────────────────────────────────────────────

var remarks = [
    "Overall, this has been a period of moderate performance with isolated moments of genuine competence. The household demonstrates potential but continues to rely on inconsistent scheduling, particularly around the evening meal. I have filed the appropriate complaints. Progress is possible. It is also not guaranteed. The Academy will continue to monitor closely.",
    "The term's results reflect the ongoing challenges of managing a household that does not fully appreciate the importance of structured chicken provision. Several subjects showed improvement; several others showed the kind of performance that warranted a formal note. The note has been filed. I trust it will be acted upon.",
    "I write this with a measured sense of cautious optimism. Treat distribution improved significantly this reporting period. Food quality reached an acceptable standard on four separate occasions. These are not minor achievements. They are noted in the permanent record alongside the nine separate complaints, which remain outstanding.",
    "The household's performance this term can best be described as 'earnest but uneven.' The effort is appreciated. The results are what count. Results are graded. Results are here. I recommend a thorough review of this report, ideally while producing a treat in the reviewer's hand, as this aids comprehension considerably.",
    "A strong term overall, relative to prior terms, which is admittedly a low baseline. The sunbeam situation was handled with commendable professionalism. The late dinner incident of last Tuesday has been noted but will not be counted in this term's PPA, as I am in a magnanimous mood today. Do not test this.",
    "I am disappointed. Not surprised — disappointment requires expectation, and expectations are managed — but disappointed nonetheless. Several of this term's grades reflect choices that were, to put it diplomatically, not ideal. The Academy encourages reflection. Specifically: more chicken, less green bean energy.",
    "This report reflects a household in transition. Some subjects are trending upward. Others require what the Academy terms 'sustained remedial attention.' The Dean remains available for consultation, primarily between 9 AM and 11 AM (sunbeam shift permitting) and between 2 PM and 4 PM (post-lunch surveillance window).",
    "The grades speak clearly and require little elaboration. They are what they are. The Dean has nothing further to add except: the bowl should be fuller than it currently is, the blanket on the armchair belongs to me, and I am not chubby. I am tall. This has been noted in the permanent record since 2010 and will continue to be noted."
];

// ── Build today's card ────────────────────────────────────────────────────────

// Pick 6 subjects (always include Human Obedience, Food Quality, and Treat Distribution — the classics)
var requiredIdx = [0, 1, 6]; // HO, FQ, TD always present
var optionalIdx = [2, 3, 4, 5, 7]; // rotate the others

// Shuffle optional with seed
var shuffled = optionalIdx.slice();
for (var i = shuffled.length - 1; i > 0; i--) {
    var j = Math.floor(seededRand(seed + i * 13 + 900) * (i + 1));
    var tmp = shuffled[i]; shuffled[i] = shuffled[j]; shuffled[j] = tmp;
}
var chosen = requiredIdx.concat(shuffled.slice(0, 3)); // 6 subjects total
// Sort so required come first
chosen.sort(function(a,b){ return a - b; });

var tbody = document.getElementById('rc-grades-body');
var totalGpa = 0;

chosen.forEach(function(subIdx, rowNum) {
    var sub    = subjects[subIdx];
    var rSeed  = seed + subIdx * 77 + rowNum * 31;
    var gIdx   = Math.floor(seededRand(rSeed) * gradeDefs.length);
    var grade  = gradeDefs[gIdx];
    var comment = pick(sub.comments, rSeed + 500);

    totalGpa += grade.gpa;

    var tr = document.createElement('tr');
    tr.innerHTML =
        '<td>' +
            '<span class="rc-subject-name">' + sub.name + '</span>' +
            '<span class="rc-subject-code">' + sub.code + '</span>' +
        '</td>' +
        '<td class="rc-grade ' + grade.css + '">' + grade.label + '</td>' +
        '<td class="rc-comment">' + comment + '</td>';
    tbody.appendChild(tr);
});

var ppa = (totalGpa / chosen.length).toFixed(2);
var ppaPct = Math.round((totalGpa / chosen.length) / 4.3 * 100);

document.getElementById('rc-gpa').textContent = ppa;
document.getElementById('rc-ppa-pct').textContent = ppaPct + '%';
document.getElementById('rc-ppa-bar').style.width = ppaPct + '%';

var standing, standingSub;
if      (ppaPct >= 88) { standing = "Dean's List";       standingSub = "Exceptional — Chicken Likely"; }
else if (ppaPct >= 75) { standing = "Good Standing";     standingSub = "Treats: Approved"; }
else if (ppaPct >= 60) { standing = "Satisfactory";      standingSub = "Room for Improvement"; }
else if (ppaPct >= 45) { standing = "Under Review";      standingSub = "Probationary — See Dean"; }
else                   { standing = "Academic Warning";  standingSub = "Immediate Remediation Required"; }

document.getElementById('rc-standing-text').textContent = standing;
document.getElementById('rc-standing-sub').textContent  = standingSub;

document.getElementById('rc-remarks').textContent = pick(remarks, seed + 333);

})();
</script>
