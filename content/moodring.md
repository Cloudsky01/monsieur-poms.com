---
title: "Daily Mood Ring"
---

<style>
.moodring-header-strip {
    background: linear-gradient(to right, #1a1a1a, #3a3a3a, #1a1a1a);
    color: #C0C0C0;
    text-align: center;
    padding: 18px 10px;
    margin: -10px -10px 0 -10px;
    border-bottom: 3px solid #888888;
}

.ring-scene {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 24px 0 16px;
}

.ring-band {
    width: 220px;
    height: 220px;
    border-radius: 50%;
    background: conic-gradient(
        #d4d4d4 0deg, #f8f8f8 30deg, #b0b0b0 60deg,
        #e8e8e8 90deg, #c8c8c8 120deg, #ffffff 150deg,
        #b8b8b8 180deg, #e4e4e4 210deg, #d0d0d0 240deg,
        #f0f0f0 270deg, #c0c0c0 300deg, #e0e0e0 330deg, #d4d4d4 360deg
    );
    border: 5px solid #999;
    box-shadow: 3px 3px 0 #666, inset 0 0 12px rgba(255,255,255,0.6);
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
}

.ring-stone {
    width: 148px;
    height: 148px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 4px solid rgba(0,0,0,0.35);
    box-shadow: 0 0 0 3px rgba(255,255,255,0.3),
                inset 0 4px 18px rgba(255,255,255,0.25),
                inset 0 -4px 12px rgba(0,0,0,0.3);
    position: relative;
    transition: background 0.5s, box-shadow 0.5s;
}

.ring-stone::before {
    content: '';
    position: absolute;
    top: 16px;
    left: 24px;
    width: 42px;
    height: 22px;
    background: radial-gradient(ellipse, rgba(255,255,255,0.35) 0%, transparent 70%);
    border-radius: 50%;
    pointer-events: none;
}

.ring-facet {
    width: 70px;
    height: 70px;
    border-radius: 50%;
    background: radial-gradient(circle at 40% 35%, #2a2a2a 0%, #111 70%);
    border: 3px solid rgba(255,255,255,0.15);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 28px;
    box-shadow: inset 0 2px 8px rgba(255,255,255,0.1);
    user-select: none;
}

@keyframes ringGlow {
    0%,100% { box-shadow: 0 0 0 3px rgba(255,255,255,0.3), inset 0 4px 18px rgba(255,255,255,0.25), inset 0 -4px 12px rgba(0,0,0,0.3); }
    50%      { box-shadow: 0 0 0 3px rgba(255,255,255,0.5), inset 0 4px 18px rgba(255,255,255,0.35), inset 0 -4px 12px rgba(0,0,0,0.2); }
}

@keyframes ringPulse {
    0%,100% { transform: scale(1); }
    50%      { transform: scale(1.015); }
}

.ring-stone  { animation: ringGlow  2.8s ease-in-out infinite; }
.ring-band   { animation: ringPulse 2.8s ease-in-out infinite; }

.mood-name-block {
    text-align: center;
    margin: 6px 0 18px;
}

.mood-color-name {
    font-family: 'Courier New', monospace;
    font-size: 11px;
    font-weight: bold;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: #888;
    margin-bottom: 4px;
}

.mood-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 26px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: #000080;
    text-shadow: 2px 2px 0 #CCC;
    line-height: 1.2;
}

.mood-intensity-bar-out {
    background: #C0C0C0;
    border: 2px inset #888;
    height: 18px;
    width: 100%;
    margin: 6px 0 2px;
    overflow: hidden;
}

.mood-intensity-bar-in {
    height: 100%;
    animation: moodFill 1s ease-out forwards;
}
@keyframes moodFill { from { width: 0%; } }

.mood-advisory-box {
    border: 3px double #000080;
    background: #F0F0FF;
    padding: 12px 14px;
    margin: 12px 0;
    font-size: 12px;
    line-height: 1.75;
    color: #000080;
}

.mood-advisory-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 13px;
    letter-spacing: 2px;
    color: #000080;
    border-bottom: 2px solid #000080;
    padding-bottom: 4px;
    margin-bottom: 8px;
}

.do-dont-grid {
    display: flex;
    gap: 12px;
    margin: 12px 0;
    flex-wrap: wrap;
}

.do-box, .dont-box {
    flex: 1;
    min-width: 160px;
    border: 2px solid #CCC;
    padding: 8px 10px;
    font-size: 11px;
    line-height: 1.65;
}

.do-box {
    background: #F0FFF0;
    border-color: #00AA00;
}

.dont-box {
    background: #FFF0F0;
    border-color: #AA0000;
}

.do-box-title, .dont-box-title {
    font-family: 'Verdana', sans-serif;
    font-weight: bold;
    font-size: 10px;
    letter-spacing: 2px;
    text-transform: uppercase;
    border-bottom: 1px solid #CCC;
    margin-bottom: 5px;
    padding-bottom: 3px;
}

.do-box-title  { color: #005500; }
.dont-box-title { color: #770000; }

.mood-chart-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 4px;
    justify-content: center;
    padding: 10px;
    background: linear-gradient(135deg, #1a1a1a, #333, #1a1a1a);
    border: 3px solid #555;
}

.chart-swatch {
    display: flex;
    align-items: center;
    gap: 5px;
    background: rgba(255,255,255,0.07);
    border: 1px solid rgba(255,255,255,0.12);
    padding: 4px 7px;
    width: 185px;
    font-size: 9px;
    font-family: 'Verdana', sans-serif;
    color: #DDD;
    line-height: 1.3;
}

.chart-swatch.today-swatch {
    background: rgba(255,255,255,0.18);
    border-color: rgba(255,255,255,0.5);
    box-shadow: 0 0 6px rgba(255,255,255,0.2);
}

.swatch-dot {
    width: 22px;
    height: 22px;
    border-radius: 50%;
    flex-shrink: 0;
    border: 2px solid rgba(255,255,255,0.3);
    box-shadow: 0 0 6px rgba(255,255,255,0.15);
}

.today-arrow {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 9px;
    color: #FFD700;
    letter-spacing: 1px;
    white-space: nowrap;
}

@keyframes moodReveal {
    from { opacity: 0; transform: translateY(-8px); }
    to   { opacity: 1; transform: translateY(0); }
}
.mood-reveal { animation: moodReveal 0.5s ease-out forwards; }
</style>

<div style="border: 1px solid #CCC; overflow: hidden; margin-bottom: 20px; background: #F9F9F9;">

<div class="moodring-header-strip">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 28px; letter-spacing: 4px; text-shadow: 2px 2px 0 #000, 0 0 12px rgba(192,192,192,0.4);">
        💍 POMS DAILY MOOD RING 💍
    </div>
    <div style="font-size: 10px; color: #AAAAAA; margin-top: 5px; letter-spacing: 3px; text-transform: uppercase;">
        Emotional State Forecasting via Authentic 90s Crystal Technology
    </div>
    <div style="margin-top: 8px; font-size: 16px; letter-spacing: 4px; color: #888;">
        ✦ ✦ ✦ ✦ ✦
    </div>
</div>

<div style="background: #E0E0E0; border-bottom: 3px double #888; padding: 6px 12px; font-size: 10px; color: #444; text-align: center;">
    CATEGORY: Emotional Intelligence &amp; Crystal Science &nbsp;|&nbsp; Calibrated Daily Since 2010 &nbsp;|&nbsp; Updated at Midnight &nbsp;|&nbsp; Today: <strong id="ring-date"></strong>
</div>

<div style="padding: 14px;">

<p style="font-size: 11px; color: #444; text-align: center; line-height: 1.75; font-style: italic;">
    The authentic Monsieur Poms Mood Ring reads the day's emotional vibrations and reports Poms' precise inner state.<br>
    Crystal accuracy is guaranteed. Monsieur Poms has personally verified the ring's calibration by staring at it for several minutes.<br>
    Results update daily at midnight. Green bean moods are not a registered ring state. They never will be.
</p>

<div class="mood-reveal" id="mood-reveal-container">

    <div class="ring-scene">
        <div class="ring-band">
            <div class="ring-stone" id="the-stone">
                <div class="ring-facet">🐾</div>
            </div>
        </div>
    </div>

    <div class="mood-name-block">
        <div class="mood-color-name" id="color-name-display"></div>
        <div class="mood-title" id="mood-title-display"></div>
    </div>

    <div style="max-width: 480px; margin: 0 auto;">
        <div style="font-size: 10px; font-family: 'Verdana', sans-serif; color: #666; margin-bottom: 3px; letter-spacing: 1px;">
            MOOD INTENSITY TODAY:
        </div>
        <div class="mood-intensity-bar-out">
            <div class="mood-intensity-bar-in" id="intensity-bar"></div>
        </div>
        <div style="font-size: 9px; color: #888; text-align: right; margin-bottom: 14px;" id="intensity-label"></div>
    </div>

    <div class="mood-advisory-box" id="advisory-box" style="max-width: 480px; margin: 0 auto;">
        <div class="mood-advisory-title">📋 OFFICIAL HOUSEHOLD ADVISORY</div>
        <div id="advisory-text"></div>
    </div>

    <div style="max-width: 480px; margin: 0 auto;">
        <div class="do-dont-grid">
            <div class="do-box">
                <div class="do-box-title">✅ Recommended Today</div>
                <div id="do-list"></div>
            </div>
            <div class="dont-box">
                <div class="dont-box-title">❌ Strictly Avoid</div>
                <div id="dont-list"></div>
            </div>
        </div>
    </div>

    <div style="max-width: 480px; margin: 14px auto 0; background: #FFFFF0; border: 2px inset #CCC; padding: 10px 12px; font-size: 11px; color: #444; font-style: italic; line-height: 1.75;">
        <span style="font-family: 'Verdana', sans-serif; font-weight: bold; font-size: 10px; color: #000080; display: block; margin-bottom: 4px; font-style: normal;">💬 POMS' PERSONAL NOTE ON TODAY'S READING:</span>
        &ldquo;<span id="poms-note"></span>&rdquo;
        <div style="font-size: 9px; color: #888; text-align: right; margin-top: 6px; font-style: normal;">— Monsieur Poms, Certified Crystal Interpreter</div>
    </div>

</div>

<hr style="margin: 20px 0;">

<div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 13px; color: #333; letter-spacing: 2px; border-bottom: 2px solid #888; padding-bottom: 4px; margin-bottom: 10px;">
    🌈 OFFICIAL POMS MOOD RING COLOR CHART
</div>

<p style="font-size: 10px; color: #666; margin: 0 0 8px 0; font-style: italic;">
    Reference guide for interpreting today's reading. Today's active mood is highlighted below.
</p>

<div class="mood-chart-grid" id="mood-chart"></div>

<hr>
<p style="font-size: 10px; color: #888; text-align: center; line-height: 1.75;">
    <em>The Poms Mood Ring uses patented crystal technology developed in the 1990s and since declared a household treasure.<br>
    Readings are 100% accurate. Monsieur Poms accepts no disputes. The ring has spoken and the ring is final.<br>
    Green bean-based emotional states are not available, recognisable, or tolerated by the crystal at any sensitivity level.</em>
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
    document.getElementById('ring-date').textContent = dateStr;

    // ── Mood data ──────────────────────────────────────────────────────────────
    var moods = [
        {
            id: "contemplation",
            colorName: "Midnight Blue",
            stoneColor: "#0a0a3a",
            glowColor: "#3333aa",
            title: "DEEP CONTEMPLATION",
            chartLabel: "Deep Contemplation — Something significant was seen on the wall",
            advisory: "Monsieur Poms has entered a state of deep philosophical inquiry. He has been staring at the wall for an extended period. The nature of what he perceives there cannot be disclosed at this time. It is significant. That is all that can be said.",
            dos: ["Leave treats within reach and withdraw silently", "Avoid blocking his sightline to the wall", "Speak only in low, respectful tones"],
            donts: ["Ask what he is looking at — you would not understand", "Make sudden movements near the wall", "Interpret the staring as confusion — it is not confusion"],
            note: "I have seen things today that cannot be unseen. The wall is aware of this. Do not ask me to elaborate. I will not elaborate."
        },
        {
            id: "royal",
            colorName: "Deep Purple",
            stoneColor: "#2a0044",
            glowColor: "#9922ee",
            title: "ROYAL DISPOSITION",
            chartLabel: "Royal Disposition — Feeling particularly aristocratic and correct",
            advisory: "Monsieur Poms is operating at maximum regal capacity today. He is acutely aware of his status as the household's supreme authority and expects all interactions to reflect this appropriately. Informal address will not be tolerated.",
            dos: ["Use the formal title 'Monsieur Poms' at all times", "Present treats on a clean, flat surface — no hand-delivery today", "Bow slightly when entering his occupied room"],
            donts: ["Use the nicknames 'Bine' or 'Binou' — today is not that kind of day", "Make direct eye contact unless he initiates it", "Suggest that any other cat is also good"],
            note: "I am feeling very correct today. More correct than usual, which is saying something. Please address me properly."
        },
        {
            id: "hunger",
            colorName: "Amber Gold",
            stoneColor: "#3a1a00",
            glowColor: "#DD8800",
            title: "STRATEGIC HUNGER MODE",
            chartLabel: "Strategic Hunger Mode — All cognition is food-adjacent",
            advisory: "Every thought, movement, and decision Monsieur Poms makes today is oriented around the food situation. Bowl levels will be monitored with extraordinary vigilance. Treat yield will be unusually high today — the disappointed eyes are already warmed up.",
            dos: ["Pre-emptively fill the bowl before it drops below 80%", "Have backup treats available in two separate locations", "Acknowledge the bowl's importance aloud"],
            donts: ["Be in the kitchen without producing food", "Leave an empty treat bag where he can see it", "Mention a diet — this is a classified hostile act today"],
            note: "The bowl situation requires my full attention today. Do not mistake this for greed. This is governance."
        },
        {
            id: "surveillance",
            colorName: "Emerald Green",
            stoneColor: "#002214",
            glowColor: "#00AA44",
            title: "ACTIVE SURVEILLANCE",
            chartLabel: "Active Surveillance — Intelligence operations are at maximum capacity",
            advisory: "Window surveillance operations are at full intensity today. The bird situation remains ongoing and requires Monsieur Poms' sustained and undivided attention. Do not obstruct Window B under any circumstances. A diplomatic standoff with the dog next door may also be in an active phase.",
            dos: ["Keep Window B unobstructed and clean", "Acknowledge that the bird situation is serious", "Report any unusual perimeter activity immediately"],
            donts: ["Walk in front of the window during active surveillance", "Make sounds that could interfere with intelligence gathering", "Ask if the dog was 'just being friendly' — it was not"],
            note: "I cannot comment on what I have observed. What I can say is that it is significant and that I am handling it personally."
        },
        {
            id: "vocalization",
            colorName: "Crimson Red",
            stoneColor: "#2a0000",
            glowColor: "#CC0000",
            title: "MAXIMUM VOCALIZATION",
            chartLabel: "Maximum Vocalization — Multiple press conferences confirmed for today",
            advisory: "Today's vocal output will be elevated. Multiple press conferences have been scheduled — all concerning the bowl and/or treat situation. Ear protection is not available but may be advisable. Response to all vocalizations must occur within 60 seconds to prevent escalation.",
            dos: ["Respond promptly to all vocalizations", "Ask what the press conference is about — chicken, usually", "Keep a full-length treat response available at all times"],
            donts: ["Say 'oh, you're being so loud today' — this is not commentary, this is governance", "Ignore the 3 AM vocalization — it is not optional", "Suggest he uses an indoor voice"],
            note: "I have a lot to say today. The bowl is involved. There may also be a secondary agenda regarding the treat schedule. I will be thorough."
        },
        {
            id: "stillness",
            colorName: "Silver White",
            stoneColor: "#2a2a2a",
            glowColor: "#AAAAAA",
            title: "STRATEGIC STILLNESS",
            chartLabel: "Strategic Stillness — Stationary operations are in full effect",
            advisory: "Monsieur Poms has not moved in approximately four hours. This is not laziness. This is strategic stillness — a highly advanced technique requiring full commitment and an impressive absence of motivation to relocate. He is, in fact, doing something very important.",
            dos: ["Place treats within direct reach — 12 inches maximum", "Quietly admire the stillness from a respectful distance", "Ensure the current surface remains warm and undisturbed"],
            donts: ["Ask if he is okay — he is more than okay", "Pick him up 'to get him moving' — absolutely not", "Tap the loaf under any circumstances"],
            note: "I am not sleeping. I am not lazy. I am conducting strategic stillness operations. The results will be significant. Do not interrupt."
        },
        {
            id: "proximity",
            colorName: "Rose Quartz",
            stoneColor: "#3a0a18",
            glowColor: "#DD3366",
            title: "PROXIMITY MODE",
            chartLabel: "Proximity Mode — Adjacent presence is available (terms apply)",
            advisory: "Monsieur Poms may choose to sit near his human tonight. Not on — near. This is a significant concession and must not be misinterpreted as full commitment. The distinction between sitting adjacent and sitting on is legally and emotionally important. Treat with appropriate weight.",
            dos: ["Accept the proximity with quiet gratitude", "Remain still once proximity is established", "Maintain a warm and comfortable ambient temperature"],
            donts: ["Announce to anyone that he is 'being cuddly today' — he is not", "Attempt to escalate proximity to full contact without consent", "Laugh — proximity is not funny, it is meaningful"],
            note: "I have chosen to sit next to you today. This is proximity only. It is not commitment. It is not sentimentality. I was cold. That is the full and complete explanation."
        },
        {
            id: "zoomies",
            colorName: "Electric Orange",
            stoneColor: "#2a0d00",
            glowColor: "#FF5500",
            title: "ZOOMIE ANTICIPATION",
            chartLabel: "Zoomie Anticipation — Kinetic event probability: very high",
            advisory: "High probability of a zoomie episode tonight between 10 PM and 2 AM. The cause of the upcoming event is fully classified and will not be disclosed before, during, or after the event. Clear the hallway. Do not follow. Do not ask what happened.",
            dos: ["Clear the hallway of all obstacles before bedtime", "Ensure all lights have been tested and are functional", "Accept that you will hear running and it will be unexplained"],
            donts: ["Follow him during the event — this is strictly prohibited", "Ask what he saw or heard — there will be no comment", "Attempt to calm him — this is not a situation requiring calming"],
            note: "Something has occurred. I cannot tell you what. I must run. The hallway needs to be clear. That is all I am prepared to say at this time."
        },
        {
            id: "intelligence",
            colorName: "Ocean Teal",
            stoneColor: "#001a1a",
            glowColor: "#00AAAA",
            title: "PUZZLE GENIUS MODE",
            chartLabel: "Puzzle Genius Mode — Intellectual output at record levels",
            advisory: "Monsieur Poms is operating at peak intellectual capacity today. He has already assessed, solved, and defeated any available food puzzle well ahead of schedule. This achievement must be formally acknowledged and entered into the public record before noon.",
            dos: ["Acknowledge out loud that the puzzle was solved very quickly", "Provide a second puzzle or a bonus treat as recognition", "Describe his intelligence using accurate and suitably grand terms"],
            donts: ["Suggest that the puzzle 'wasn't that hard'", "Compare his puzzle time to any other cat's time — there is no comparison", "Forget to log this for the public record"],
            note: "I completed the food puzzle in record time. Again. As expected. I would like this formally entered into the record. Thank you."
        },
        {
            id: "serenity",
            colorName: "Sunbeam Gold",
            stoneColor: "#2a1a00",
            glowColor: "#FFD700",
            title: "SUNBEAM SERENITY",
            chartLabel: "Sunbeam Serenity — Prime beam secured; contentment at maximum",
            advisory: "Monsieur Poms has successfully located and claimed the premium sunbeam position of the day. He is warm. He is correct. He is, by all reasonable measures, at peak contentment. This is a rare and good day. Do not disrupt it.",
            dos: ["Ensure no objects create shadows across his sunbeam", "Bring a treat quietly and place it nearby without comment", "Take this opportunity to appreciate how handsome he looks"],
            donts: ["Move curtains, blinds, or any light-affecting elements", "Announce 'the sun's moved' — he is already tracking it", "Mistake contentment for an invitation to pick him up"],
            note: "The sunbeam is perfect. I have claimed it. I am warm. This is a satisfactory day and I am choosing to enjoy it professionally."
        }
    ];

    // ── Intensity pools ────────────────────────────────────────────────────────
    var intensityLevels = [
        { pct: 62, label: "Moderate — Household should be alert but not alarmed" },
        { pct: 74, label: "Elevated — Treat reserves should be kept at full capacity" },
        { pct: 81, label: "High — Household advisory in effect; proceed with treats" },
        { pct: 88, label: "Very High — Full compliance strongly recommended today" },
        { pct: 95, label: "Maximum — Emergency chicken protocol may be required" },
        { pct: 55, label: "Mild — An exceptionally manageable day by Poms standards" },
        { pct: 70, label: "Significant — Normal precautions apply across all departments" }
    ];

    // ── Pick today's mood ──────────────────────────────────────────────────────
    var moodIdx    = Math.floor(seededRand(seed + 99) * moods.length);
    var mood       = moods[moodIdx];
    var intensity  = pick(intensityLevels, seed + 88);

    // ── Apply stone color + glow ──────────────────────────────────────────────
    var stone = document.getElementById('the-stone');
    stone.style.background = 'radial-gradient(circle at 38% 32%, ' +
        mood.glowColor + '88 0%, ' + mood.stoneColor + ' 62%)';
    stone.style.boxShadow  = [
        '0 0 0 3px rgba(255,255,255,0.3)',
        '0 0 20px ' + mood.glowColor + '99',
        'inset 0 4px 18px rgba(255,255,255,0.25)',
        'inset 0 -4px 12px rgba(0,0,0,0.3)'
    ].join(', ');

    // Update ring-band glow to match
    var band = stone.parentElement;
    band.style.boxShadow = '3px 3px 0 #666, inset 0 0 12px rgba(255,255,255,0.6), 0 0 28px ' + mood.glowColor + '55';

    // ── Populate page ─────────────────────────────────────────────────────────
    document.getElementById('color-name-display').textContent  = mood.colorName;
    document.getElementById('mood-title-display').textContent  = mood.title;
    document.getElementById('advisory-text').innerHTML         = esc(mood.advisory);
    document.getElementById('poms-note').innerHTML             = esc(mood.note);

    var intensityBar = document.getElementById('intensity-bar');
    intensityBar.style.width      = intensity.pct + '%';
    intensityBar.style.background = 'linear-gradient(to right, ' + mood.glowColor + '88, ' + mood.glowColor + ')';
    document.getElementById('intensity-label').textContent = intensity.pct + '% — ' + intensity.label;

    // Do list
    var doHtml = '';
    mood.dos.forEach(function(d) { doHtml += '• ' + esc(d) + '<br>'; });
    document.getElementById('do-list').innerHTML = doHtml;

    // Don't list
    var dontHtml = '';
    mood.donts.forEach(function(d) { dontHtml += '• ' + esc(d) + '<br>'; });
    document.getElementById('dont-list').innerHTML = dontHtml;

    // Advisory box border color
    document.getElementById('advisory-box').style.borderColor = mood.glowColor;
    document.getElementById('advisory-box').style.background  = mood.stoneColor + '11';

    // ── Build color chart ──────────────────────────────────────────────────────
    var chartEl = document.getElementById('mood-chart');
    moods.forEach(function (m, i) {
        var isToday = (i === moodIdx);
        var div = document.createElement('div');
        div.className = 'chart-swatch' + (isToday ? ' today-swatch' : '');

        var dot = document.createElement('div');
        dot.className = 'swatch-dot';
        dot.style.background = 'radial-gradient(circle at 38% 35%, ' + m.glowColor + '99, ' + m.stoneColor + ')';
        dot.style.boxShadow  = '0 0 8px ' + m.glowColor + '66';
        div.appendChild(dot);

        var label = document.createElement('div');
        label.style.flex = '1';
        label.innerHTML =
            '<div style="font-weight:bold;font-size:10px;color:' + (isToday ? '#FFD700' : '#DDD') + ';margin-bottom:1px;">' +
                esc(m.colorName) + (isToday ? ' &nbsp;<span class="today-arrow">◄ TODAY</span>' : '') +
            '</div>' +
            '<div style="color:#AAA;">' + esc(m.chartLabel) + '</div>';
        div.appendChild(label);
        chartEl.appendChild(div);
    });

})();
</script>
