---
title: "Achievement Unlocked"
---

<style>
.ach-header-strip {
    background: linear-gradient(to right, #0a0a20, #141450, #0a0a20);
    color: #FFD700;
    text-align: center;
    padding: 18px 10px;
    margin: -10px -10px 0 -10px;
    border-bottom: 3px solid #FFD700;
}

.ach-xp-window {
    background: #ECE9D8;
    border: 3px outset #FFFFFF;
    border-radius: 8px 8px 0 0;
    max-width: 520px;
    margin: 14px auto 0;
    box-shadow: 5px 5px 0 #888;
    font-family: 'Tahoma', 'Verdana', sans-serif;
    font-size: 11px;
    overflow: hidden;
}

.ach-xp-titlebar {
    background: linear-gradient(to bottom,
        #5aacff 0%, #3285f5 4%,
        #0058e8 40%, #0048c0 92%,
        #0033a0 100%
    );
    padding: 4px 6px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    color: #fff;
    font-size: 11px;
    font-weight: bold;
    text-shadow: 1px 1px 1px rgba(0,0,0,0.6);
    user-select: none;
}

.ach-xp-btn {
    width: 18px;
    height: 16px;
    border-radius: 3px;
    border: 1px outset #88bbee;
    background: linear-gradient(to bottom, #d8eeff 0%, #90bbee 100%);
    color: #000080;
    font-size: 9px;
    font-weight: bold;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    margin-left: 2px;
    cursor: default;
    line-height: 1;
}

.ach-xp-btn.close-btn {
    background: linear-gradient(to bottom, #ffaaaa 0%, #ee4444 100%);
    border-color: #cc3333;
    color: #fff;
}

.ach-xp-content {
    padding: 14px 16px 16px;
}

.ach-unlock-banner {
    background: linear-gradient(to right, #0040BB, #0058e8, #0040BB);
    color: #FFD700;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 13px;
    letter-spacing: 3px;
    text-align: center;
    padding: 5px 10px;
    text-shadow: 1px 1px 0 #000;
    margin-bottom: 12px;
    animation: achBlink 2.4s ease-in-out 3;
}

@keyframes achBlink {
    0%, 100% { opacity: 1; }
    50%       { opacity: 0.65; }
}

.ach-card-row {
    display: flex;
    gap: 12px;
    align-items: flex-start;
    background: #fff;
    border: 2px inset #aaa;
    padding: 12px;
    margin-bottom: 10px;
}

.ach-icon-box {
    width: 72px;
    height: 72px;
    flex-shrink: 0;
    background: radial-gradient(circle at 35% 30%, #2a2a55 0%, #080818 100%);
    border: 3px inset #666;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 38px;
    box-shadow: inset 0 2px 8px rgba(0,0,0,0.5);
    position: relative;
    overflow: hidden;
}

.ach-icon-box::after {
    content: '';
    position: absolute;
    top: 7px; left: 8px;
    width: 22px; height: 11px;
    background: radial-gradient(ellipse, rgba(255,255,255,0.22) 0%, transparent 70%);
    border-radius: 50%;
    pointer-events: none;
}

.ach-name {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 17px;
    color: #000080;
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-bottom: 5px;
    line-height: 1.2;
}

.ach-desc {
    font-size: 11px;
    color: #333;
    line-height: 1.65;
    margin-bottom: 7px;
}

.ach-pts-badge {
    display: inline-block;
    background: #000080;
    color: #FFD700;
    font-family: 'Courier New', monospace;
    font-size: 12px;
    font-weight: bold;
    padding: 2px 9px;
    border: 2px outset #4444CC;
    letter-spacing: 2px;
    margin-right: 6px;
}

.ach-cat-tag {
    font-size: 9px;
    color: #666;
    font-family: 'Verdana', sans-serif;
    font-style: italic;
}

.ach-xp-bar-outer {
    background: #C0C0C0;
    border: 2px inset #888;
    height: 16px;
    width: 100%;
    overflow: hidden;
    margin: 4px 0;
}

.ach-xp-bar-inner {
    height: 100%;
    background: repeating-linear-gradient(
        90deg,
        #0044dd 0px, #4488ff 5px, #0044dd 10px
    );
    animation: achBarFill 1.1s ease-out forwards;
}

@keyframes achBarFill { from { width: 0%; } }

.ach-profile-card {
    background: linear-gradient(to bottom, #0e0e2a, #04041a);
    border: 3px solid #2233aa;
    padding: 12px 14px;
    margin: 14px 0;
    color: #fff;
    font-family: 'Verdana', sans-serif;
    font-size: 11px;
    box-shadow: 4px 4px 0 #000;
}

.ach-stat-num {
    font-family: 'Courier New', monospace;
    font-weight: bold;
    font-size: 20px;
    line-height: 1.1;
    margin-top: 2px;
}

.ach-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
    padding: 12px;
    background: linear-gradient(135deg, #111120, #1a1a30, #111120);
    border: 3px solid #2a2a4a;
}

.ach-tile {
    width: 116px;
    background: #1a1a2e;
    border: 2px solid #2a2a4a;
    padding: 7px 6px;
    text-align: center;
    font-size: 9px;
    font-family: 'Verdana', sans-serif;
    color: #aaa;
    line-height: 1.3;
    transition: border-color 0.15s;
    cursor: default;
}

.ach-tile:hover {
    border-color: #4455aa;
}

.ach-tile.ach-today {
    background: #1a1400;
    border: 2px solid #FFD700;
    box-shadow: 0 0 10px rgba(255, 215, 0, 0.35);
    color: #fff;
}

.ach-tile-icon {
    font-size: 26px;
    margin-bottom: 4px;
    display: block;
}

.ach-tile-name {
    font-weight: bold;
    color: #ddd;
    font-size: 8px;
    margin-bottom: 2px;
    line-height: 1.35;
}

.ach-today .ach-tile-name {
    color: #FFD700;
}

.ach-tile-pts {
    font-size: 8px;
    color: #666;
}

.ach-today .ach-tile-pts {
    color: #FFD700;
}

.ach-today-tag {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 7px;
    color: #FFD700;
    letter-spacing: 1px;
    display: block;
    margin-top: 2px;
}

@keyframes achReveal {
    from { opacity: 0; transform: scale(0.94) translateY(-6px); }
    to   { opacity: 1; transform: scale(1) translateY(0); }
}
.ach-reveal { animation: achReveal 0.5s ease-out forwards; }

@keyframes achGlow {
    0%, 100% { box-shadow: 5px 5px 0 #888; }
    50%       { box-shadow: 5px 5px 0 #888, 0 0 20px rgba(255, 215, 0, 0.25); }
}
.ach-xp-window { animation: achGlow 3s ease-in-out infinite; }
</style>

<div style="border: 1px solid #CCC; overflow: hidden; margin-bottom: 20px; background: #F9F9F9;">

<div class="ach-header-strip">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 28px; letter-spacing: 4px; text-shadow: 2px 2px 0 #000, 0 0 22px rgba(255,215,0,0.5);">
        🏆 ACHIEVEMENT UNLOCKED 🏆
    </div>
    <div style="font-size: 10px; color: #9999FF; margin-top: 5px; letter-spacing: 3px; text-transform: uppercase;">
        Official Poms Gamerscore Tracker &nbsp;|&nbsp; Accumulating Since January 2010
    </div>
    <div style="margin-top: 8px; font-size: 17px; letter-spacing: 5px; color: #3366FF;">
        ★ ★ ★ ★ ★
    </div>
</div>

<div style="background: #D8DCF0; border-bottom: 3px double #3333AA; padding: 6px 12px; font-size: 10px; color: #000080; text-align: center;">
    CATEGORY: Achievements &amp; Accomplishments &nbsp;|&nbsp; Poms Gamerscore Tracker &nbsp;|&nbsp; New Achievement Every Day &nbsp;|&nbsp; Today: <strong id="ach-date"></strong>
</div>

<div style="padding: 14px;">

<p style="font-size: 11px; color: #444; text-align: center; line-height: 1.75; font-style: italic;">
    Each day, Monsieur Poms earns a new Achievement in formal recognition of his extraordinary daily accomplishments.<br>
    His Gamerscore has been accumulating since January 2010. It is extremely high. He is extremely proud.<br>
    There is no achievement for eating a green bean. There will never be one. This is non-negotiable and constitutional.
</p>

<!-- Windows XP-style Achievement Popup -->
<div class="ach-xp-window ach-reveal">
    <div class="ach-xp-titlebar">
        <div style="display:flex;align-items:center;gap:5px;">
            <span style="font-size:13px;">🏆</span>
            <span>Monsieur Poms — Achievement Tracker v2.0</span>
        </div>
        <div>
            <span class="ach-xp-btn">_</span>
            <span class="ach-xp-btn">□</span>
            <span class="ach-xp-btn close-btn">✕</span>
        </div>
    </div>
    <div class="ach-xp-content">
        <div class="ach-unlock-banner">🏆 &nbsp; ACHIEVEMENT UNLOCKED &nbsp; 🏆</div>
        <div class="ach-card-row">
            <div class="ach-icon-box" id="ach-icon-main">🐾</div>
            <div style="flex:1;">
                <div class="ach-name" id="ach-name-main">Loading&hellip;</div>
                <div class="ach-desc" id="ach-desc-main"></div>
                <div>
                    <span class="ach-pts-badge" id="ach-pts-main">—G</span>
                    <span class="ach-cat-tag" id="ach-cat-main"></span>
                </div>
            </div>
        </div>

        <div style="font-size:10px;color:#444;font-family:'Verdana',sans-serif;margin-bottom:3px;letter-spacing:1px;text-transform:uppercase;">
            Gamerscore Progress:
        </div>
        <div class="ach-xp-bar-outer">
            <div class="ach-xp-bar-inner" id="ach-progress-bar"></div>
        </div>
        <div style="display:flex;justify-content:space-between;font-size:9px;color:#666;font-family:'Verdana',sans-serif;margin-top:2px;margin-bottom:10px;">
            <span>0G</span>
            <span id="ach-progress-label">—</span>
            <span id="ach-progress-max">—</span>
        </div>

        <div style="font-size:10px;color:#555;font-family:'Verdana',sans-serif;font-style:italic;border-top:1px solid #ccc;padding-top:8px;">
            ✅ Achievement added to Monsieur Poms' profile &nbsp;|&nbsp; <span id="ach-date-footer"></span>
        </div>
    </div>
</div>

<!-- Gamer profile card -->
<div class="ach-profile-card">
    <div style="display:flex;justify-content:space-between;align-items:flex-start;flex-wrap:wrap;gap:8px;margin-bottom:10px;">
        <div>
            <div style="font-family:'Impact','Arial Black',sans-serif;font-size:18px;color:#FFD700;letter-spacing:2px;">monsieur_poms</div>
            <div style="font-size:9px;color:#6677AA;margin-top:2px;letter-spacing:1px;text-transform:uppercase;font-style:italic;">Unofficial Apple Soda Brand Ambassador &nbsp;|&nbsp; Professional Talker</div>
        </div>
        <div style="text-align:right;">
            <div style="font-size:9px;color:#6677AA;letter-spacing:1px;text-transform:uppercase;margin-bottom:2px;">Total Gamerscore</div>
            <div style="font-family:'Courier New',monospace;font-size:24px;font-weight:bold;color:#FFD700;letter-spacing:3px;text-shadow:0 0 10px rgba(255,215,0,0.4);" id="ach-gamerscore">—</div>
        </div>
    </div>
    <div style="border-top:1px solid #222;margin-bottom:10px;"></div>
    <div style="display:flex;gap:0;flex-wrap:wrap;">
        <div style="text-align:center;flex:1;min-width:90px;padding:4px 8px;border-right:1px solid #222;">
            <div style="font-size:8px;color:#6677AA;text-transform:uppercase;letter-spacing:1px;margin-bottom:3px;">Achievements</div>
            <div class="ach-stat-num" style="color:#AAFFAA;" id="ach-count-display">—</div>
        </div>
        <div style="text-align:center;flex:1;min-width:90px;padding:4px 8px;border-right:1px solid #222;">
            <div style="font-size:8px;color:#6677AA;text-transform:uppercase;letter-spacing:1px;margin-bottom:3px;">Complaints Filed</div>
            <div class="ach-stat-num" style="color:#FFAAAA;" id="ach-complaints-display">—</div>
        </div>
        <div style="text-align:center;flex:1;min-width:90px;padding:4px 8px;border-right:1px solid #222;">
            <div style="font-size:8px;color:#6677AA;text-transform:uppercase;letter-spacing:1px;margin-bottom:3px;">Nap Hours (Lifetime)</div>
            <div class="ach-stat-num" style="color:#AAAAFF;" id="ach-nap-display">—</div>
        </div>
        <div style="text-align:center;flex:1;min-width:90px;padding:4px 8px;">
            <div style="font-size:8px;color:#6677AA;text-transform:uppercase;letter-spacing:1px;margin-bottom:3px;">Rank</div>
            <div style="font-family:'Impact','Arial Black',sans-serif;font-size:11px;font-weight:bold;color:#FFD700;margin-top:4px;letter-spacing:1px;" id="ach-rank-display">—</div>
        </div>
    </div>
</div>

<!-- Full achievement collection -->
<div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 14px; color: #000080; letter-spacing: 2px; border-bottom: 2px solid #000080; padding-bottom: 4px; margin: 14px 0 6px;">
    📋 COMPLETE ACHIEVEMENT COLLECTION
</div>
<p style="font-size: 10px; color: #666; margin: 0 0 8px; font-style: italic;">
    All achievements earned by Monsieur Poms since 2010. Hover any tile for full details. Today's achievement is highlighted in gold.
</p>

<div class="ach-grid" id="ach-grid"></div>

<hr>
<p style="font-size: 10px; color: #888; text-align: center; line-height: 1.75;">
    <em>Achievements update daily at midnight. Gamerscore accumulates since January 2, 2010.<br>
    Monsieur Poms accepts no disputes regarding achievement validity. All achievements are final, certified, and above reproach.<br>
    A "Voluntary Green Bean Consumption" achievement has been proposed exactly zero times. This will not change.</em>
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
    document.getElementById('ach-date').textContent       = dateStr;
    document.getElementById('ach-date-footer').textContent = dateStr;

    // ── Achievement pool ──────────────────────────────────────────────────────
    var achievements = [
        { icon: "🍗", pts: 50, cat: "Food & Nourishment",
          name: "CHICKEN ACQUISITION SPECIALIST",
          desc: "Obtained chicken through sustained eye contact alone, without deploying a single meow. Pure psychological mastery. Impressive even by Poms' own firmly established standards." },
        { icon: "😤", pts: 25, cat: "Governance",
          name: "FIRST COMPLAINT BEFORE 7 AM",
          desc: "Filed a formal grievance regarding bowl fill levels before the household was fully operational. Pre-dawn regulatory enforcement at its finest and most consistent." },
        { icon: "☀️", pts: 30, cat: "Physical Operations",
          name: "SUNBEAM SOVEREIGN",
          desc: "Claimed the morning sunbeam on the first attempt, without requiring three consecutive failed relocations. Exceptional territorial instinct. Beam: secured. Warmth: maximum." },
        { icon: "🧩", pts: 75, cat: "Intellectual Achievements",
          name: "FOOD PUZZLE DOMINATOR",
          desc: "Completed the food puzzle in a new personal record time. The treat had no chance. The puzzle was outmatched before it was even set down. Achievement formally entered into the public record." },
        { icon: "👀", pts: 35, cat: "Diplomacy",
          name: "MASTER OF THE DISAPPOINTED EYES",
          desc: "Deployed the disappointed eyes at full operational intensity with 100% effectiveness. Treat secured. No meow was required. Outcome was, of course, never meaningfully in doubt." },
        { icon: "🍞", pts: 45, cat: "Sleep & Restoration",
          name: "LOAF FORM CERTIFIED",
          desc: "Maintained perfect loaf formation for over 4 consecutive hours. All limbs fully and correctly tucked. Not a single structural violation detected by any qualified observer." },
        { icon: "🐕", pts: 55, cat: "Foreign Affairs",
          name: "DIPLOMATIC STANDOFF CHAMPION",
          desc: "Maintained unbroken eye contact with the dog next door through Window B for the full duration of the session. Did not blink first. Undefeated. Status: ongoing standoff." },
        { icon: "🧱", pts: 20, cat: "Intelligence",
          name: "WALL WATCHER SUPREME",
          desc: "Stared at the living room wall for 14 consecutive minutes. What was observed is classified at the highest household security level. It was significant. That is all that will be confirmed." },
        { icon: "💤", pts: 60, cat: "Sleep & Restoration",
          name: "NAP MARATHON CHAMPION",
          desc: "Completed an uninterrupted 6-hour nap. New personal record. Disturbance count: zero. Dignity maintained throughout the entire duration. Strategic excellence at the highest level." },
        { icon: "🌙", pts: 30, cat: "Governance",
          name: "3 AM VOCAL OPERATIONS",
          desc: "Successfully refilled the bowl via an overnight vocalization campaign. Human response time logged at 7 minutes — technically an improvement. A formal complaint was filed regardless." },
        { icon: "⌨️", pts: 25, cat: "Professional",
          name: "KEYBOARD CONTRIBUTOR",
          desc: "Made substantive editorial contributions to an official work document. Contributions included several j's, a semicolon, and what may have been an email to accounting. Peer review was not requested." },
        { icon: "🎯", pts: 50, cat: "Physical Operations",
          name: "TREAT SPEED RECORD",
          desc: "Arrived at the treat bag within 0.3 seconds of the first detectable rustle. From three rooms away. Reflexes officially unmatched. Record self-certified, announced, and archived." },
        { icon: "🛋️", pts: 35, cat: "Physical Operations",
          name: "SOFA TERRITORY COMMANDER",
          desc: "Occupied 82% of available sofa surface area simultaneously. Remaining 18% allocated to household residents as a courtesy. The courtesy may be revoked at any time without prior notice." },
        { icon: "📦", pts: 30, cat: "Governance",
          name: "BOX HEADQUARTERS SECURED",
          desc: "Officially requisitioned a newly arrived cardboard box as operational headquarters. Security measures implemented. Jurisdiction: absolute. Staff: none required. Efficiency: total." },
        { icon: "🏃", pts: 40, cat: "Physical Operations",
          name: "MIDNIGHT ZOOMIE PROTOCOL",
          desc: "Completed a full-corridor high-speed run at 11:58 PM. Reason: classified at the absolute highest level. No comment was made then. No comment will be made now or at any future time." },
        { icon: "🔬", pts: 20, cat: "Scientific Research",
          name: "COUNTER SOCIAL EXPERIMENT",
          desc: "Knocked an item off the kitchen counter in a carefully observed social experiment. Results were recorded as 'interesting.' Zero remorse was detected at any stage of the process." },
        { icon: "🏃", pts: 65, cat: "Diplomatic Immunity",
          name: "VET EVASION MASTER",
          desc: "Became unavailable within 15 seconds of the word 'vet' being spoken within range. Current location: classified. The carrier's location: also classified. Medical status: absolutely fine." },
        { icon: "🚰", pts: 15, cat: "Food & Nourishment",
          name: "TAP WATER CONNOISSEUR",
          desc: "Rejected the bowl, the fountain, and the dish — all producing chemically identical water — in favour of the tap exclusively. Standards maintained. Aesthetic preferences: non-negotiable." },
        { icon: "🤚", pts: 45, cat: "Diplomacy",
          name: "BELLY TRAP DEPLOYED",
          desc: "Presented the belly and activated the consent assessment framework. Multiple parties were assessed. Results: monitored. The trap operates as designed. No further comment at this time." },
        { icon: "📋", pts: 70, cat: "Governance",
          name: "COUNTER-PROPOSAL ACCEPTED",
          desc: "Submitted a formal counter-proposal to the vet's dietary recommendations. Counter-proposal content: 'more chicken.' The counter-proposal was accepted. The diet was rejected. Outcome: correct." },
        { icon: "😴", pts: 25, cat: "Physical Operations",
          name: "FACE PRESS SPECIALIST",
          desc: "Executed a precise face-press against a sleeping household member at 4:47 AM. Official stated reason: temperature regulation. Supporting thermal data: unavailable. Position: maintained." },
        { icon: "🎙️", pts: 30, cat: "Professional",
          name: "PRESS CONFERENCE VETERAN",
          desc: "Conducted another in a long and distinguished series of official press conferences from the food bowl. The topic was the bowl. The topic has not changed since 2010. Consistency is a virtue." },
        { icon: "🎵", pts: 20, cat: "Cultural",
          name: "NYAN CAT OFFICIAL ENDORSER",
          desc: "Issued a formal letter of endorsement for Nyan Cat following an extended listening session. Musical opinion: final. Position: not open for further discussion. Nyan Cat: indefinitely endorsed." },
        { icon: "🌟", pts: 25, cat: "Governance",
          name: "FORMAL CLARITY CAMPAIGN",
          desc: "Corrected the use of the term 'chonky' to 'tall' for the 37th documented time this year. Height stored horizontally is still height. This clarification is permanent and fully constitutional." },
        { icon: "🥱", pts: 15, cat: "Physical Operations",
          name: "MAXIMUM YAWN ACHIEVED",
          desc: "Produced a yawn of documented exceptional width at 7:14 AM. Household members laughed. The yawn was dignified and entirely proportionate. The laughter was not warranted. Officially noted." },
        { icon: "🥤", pts: 50, cat: "Professional",
          name: "APPLE SODA AMBASSADOR",
          desc: "Embodied the spirit of POMS apple soda with full authority — refreshing, iconic, and bubbling with personality. Named after a legendary soda. The naming was entirely prescient." },
        { icon: "🎤", pts: 30, cat: "Professional",
          name: "PROFESSIONAL CHATTY ACHIEVEMENT",
          desc: "Spoken at length, at considerable volume, and with great purpose for the majority of the day. Everyone was informed of everything. Not everyone understood. That is their limitation, not Poms'." },
        { icon: "🏅", pts: 80, cat: "Intellectual Achievements",
          name: "ABSOLUTE PUZZLE RECORD",
          desc: "Solved the food puzzle in a new all-time personal record time. Record immediately self-certified, formally entered into the public record, and announced at a specially convened press conference." },
        { icon: "🌞", pts: 35, cat: "Physical Operations",
          name: "SUNBEAM MIGRATION EXPERT",
          desc: "Followed the sunbeam through all four of its scheduled daily locations without missing a single transition window. Dedication to warmth: complete, professional, and fully documented." },
        { icon: "💼", pts: 40, cat: "Governance",
          name: "ELITE COMPLAINT FILER",
          desc: "Filed complaints at the established average rate of 3.47 per day. The rate was maintained with full consistency. It has not decreased since 2010. It will not decrease. This is governance." }
    ];

    // ── Today's achievement ───────────────────────────────────────────────────
    var todayIdx = Math.floor(seededRand(seed + 42) * achievements.length);
    var today    = achievements[todayIdx];

    document.getElementById('ach-icon-main').textContent = today.icon;
    document.getElementById('ach-name-main').textContent = today.name;
    document.getElementById('ach-desc-main').textContent = today.desc;
    document.getElementById('ach-pts-main').textContent  = '+' + today.pts + 'G';
    document.getElementById('ach-cat-main').textContent  = '[ ' + today.cat + ' ]';

    // ── Gamerscore & progress bar ─────────────────────────────────────────────
    var startDate  = new Date(2010, 0, 2);
    var daysSince  = Math.floor((now - startDate) / 86400000);
    var gamerscore = daysSince * 36 + 1250;
    var milestone  = Math.ceil(gamerscore / 10000) * 10000;
    var prevMilestone = milestone - 10000;
    var progressPct  = Math.min(98, ((gamerscore - prevMilestone) / 10000) * 100);

    document.getElementById('ach-progress-bar').style.width = progressPct + '%';
    document.getElementById('ach-progress-label').textContent = gamerscore.toLocaleString() + 'G';
    document.getElementById('ach-progress-max').textContent   = 'Next: ' + milestone.toLocaleString() + 'G';
    document.getElementById('ach-gamerscore').textContent     = gamerscore.toLocaleString() + 'G';

    // ── Profile stats ─────────────────────────────────────────────────────────
    document.getElementById('ach-count-display').textContent =
        achievements.length + ' / ' + achievements.length;
    document.getElementById('ach-complaints-display').textContent =
        Math.floor(daysSince * 3.47 + 127).toLocaleString();
    document.getElementById('ach-nap-display').textContent =
        (daysSince * 14).toLocaleString() + 'h';

    var ranks = [
        "SUNBEAM SOVEREIGN",
        "GRAND MASTER OF THE BOWL",
        "SUPREME NAP STRATEGIST",
        "LORD HIGH CHICKEN OFFICER",
        "CHAMPION OF THE CARDBOARD BOX",
        "ELITE TREAT ACQUISITION AGENT",
        "CERTIFIED WALL OBSERVER, FIRST CLASS"
    ];
    document.getElementById('ach-rank-display').textContent = pick(ranks, seed + 9999);

    // ── Build achievement grid ────────────────────────────────────────────────
    var grid = document.getElementById('ach-grid');
    achievements.forEach(function (a, i) {
        var isToday = (i === todayIdx);
        var tile = document.createElement('div');
        tile.className = 'ach-tile' + (isToday ? ' ach-today' : '');
        tile.title = a.name + ' — ' + a.pts + 'G\n\n' + a.desc + '\n\nCategory: ' + a.cat;

        var todayTag = isToday
            ? '<span class="ach-today-tag">★ TODAY\'S ACHIEVEMENT</span>'
            : '';

        tile.innerHTML =
            '<span class="ach-tile-icon">' + esc(a.icon) + '</span>' +
            '<div class="ach-tile-name">' + esc(a.name) + '</div>' +
            '<div class="ach-tile-pts">+' + a.pts + 'G &nbsp;|&nbsp; ' + esc(a.cat) + '</div>' +
            todayTag;

        grid.appendChild(tile);
    });

})();
</script>
