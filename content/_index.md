---
title: "Home"
---

<!-- POST 1 -->
<div style="border: 1px solid #CCC; padding: 10px; background: #F9F9F9; margin-bottom: 20px;">
<h2 style="margin-top: 0;">✨ WELCOME TO MY DOMAIN ✨</h2>
<div style="font-size: 10px; color: #666;">Posted on: January 22, 2010 @ 4:20 PM | Mood: Excited</div>
<hr>
<p>Hi everyone!!!! Welcome to my <strong>BRAND NEW</strong> website. My human decided to make this for me because I am so famous and cute.</p>

<p>Here you will find:</p>
<ul>
<li>Cute pics of me (obviously)</li>
<li>Facts about why I am the best</li>
<li>A guestbook for you to tell me I am pretty</li>
</ul>

<div style="text-align: center; border: 3px dashed #FF00FF; padding: 10px; background: #FFF0F5; margin: 10px;">
<h3>~*~ WHAT IS POMS DOING RIGHT NOW?? ~*~</h3>
<div id="poms-activity-widget">
<div id="poms-time-display" style="font-family: 'Courier New', monospace; background: #000; color: #00FF00; padding: 4px 10px; display: inline-block; font-size: 13px; border: 2px inset #555; margin-bottom: 8px;"></div>
<br>
<img id="poms-activity-img" src="" alt="Poms activity" style="width: 100%; max-width: 350px; border: 3px solid #000080; margin: 8px 0;">
<div id="poms-activity-label" style="font-size: 18px; font-weight: bold; color: #FF00FF; margin: 4px 0;"></div>
<div id="poms-activity-caption" style="font-style: italic; font-size: 13px; margin: 4px 0;"></div>
<div id="poms-mood-display" style="font-size: 11px; margin-top: 6px;"></div>
</div>
<script>
(function() {
    var BASE = "https://cloudsky01.github.io/monsieur-poms.com/images/";
    var schedule = [
        { hours: [0,1,2,3], img: "poms_sleeping.jpg",     label: "SLEEP MODE ACTIVATED",            caption: "Do not disturb. Charging for tomorrow's complaints.",     mood: "Mood: Deeply unconscious" },
        { hours: [4,5],      img: "poms_looking_up.jpg",  label: "INITIATING WAKE-UP PROTOCOL",      caption: "Sitting on human's face in 3... 2... 1...",                mood: "Mood: Strategically annoying" },
        { hours: [6,7],      img: "poms_stare.jpg",       label: "MORNING PRESS CONFERENCE",         caption: "The food bowl situation is UNACCEPTABLE and heads will roll.", mood: "Mood: Outraged" },
        { hours: [8,9],      img: "poms_yawn.jpg",        label: "POST-BREAKFAST STRETCH",           caption: "Breakfast was consumed. It was adequate. Barely.",          mood: "Mood: Mildly satisfied" },
        { hours: [10,11],    img: "poms_loaf.jpg",        label: "LOAF CONFIGURATION ENGAGED",       caption: "Peak efficiency. All paws tucked. Monitoring the perimeter.", mood: "Mood: Zen loaf energy" },
        { hours: [12,13],    img: "poms_sleeping.jpg",    label: "NAP #1 (THE IMPORTANT ONE)",       caption: "Working hard on absolutely nothing. Please hold.",          mood: "Mood: Professionally asleep" },
        { hours: [14,15],    img: "poms_judging.jpg",     label: "AFTERNOON JUDGING SESSION",        caption: "You have been evaluated and found somewhat acceptable.",    mood: "Mood: Quietly disappointed" },
        { hours: [16,17],    img: "poms_curious.jpg",     label: "PERIMETER INSPECTION UNDERWAY",   caption: "Something moved behind the fridge. INVESTIGATING.",         mood: "Mood: Highly suspicious" },
        { hours: [18,19],    img: "poms_stare.jpg",       label: "PRE-DINNER DEMAND SEQUENCE",       caption: "The bowl is NOT going to fill itself. HELLO. HELLO??",      mood: "Mood: Escalating urgency" },
        { hours: [20,21],    img: "poms_sleeping.jpg",    label: "POST-DINNER RECOVERY COMA",        caption: "Food consumed. Retreating to couch. Do not make eye contact.", mood: "Mood: Food coma achieved" },
        { hours: [22],       img: "poms_profile.jpg",     label: "EVENING BRAND AMBASSADOR DUTIES", caption: "Posing for unsolicited photos. You're welcome, internet.",    mood: "Mood: Photogenic and aware of it" },
        { hours: [23],       img: "poms_sleeping.jpg",    label: "SIMULATING SLEEP (PLOTTING)",      caption: "Definitely not planning anything. Definitely just sleeping. xD", mood: "Mood: Suspiciously still" }
    ];

    function pad(n) { return n < 10 ? "0" + n : n; }

    function update() {
        var now = new Date();
        var h = now.getHours();
        var entry;
        for (var i = 0; i < schedule.length; i++) {
            if (schedule[i].hours.indexOf(h) !== -1) { entry = schedule[i]; break; }
        }
        if (!entry) entry = schedule[0];

        var timeStr = pad(h) + ":" + pad(now.getMinutes()) + ":" + pad(now.getSeconds());
        document.getElementById("poms-time-display").textContent = "[ LOCAL TIME: " + timeStr + " ]";
        document.getElementById("poms-activity-img").src = BASE + entry.img;
        document.getElementById("poms-activity-img").alt = entry.label;
        document.getElementById("poms-activity-label").textContent = entry.label;
        document.getElementById("poms-activity-caption").textContent = '"' + entry.caption + '"';
        document.getElementById("poms-mood-display").innerHTML = "<strong>" + entry.mood + "</strong> &nbsp;|&nbsp; Check back later for updates!!";
    }

    update();
    setInterval(update, 1000);
})();
</script>
</div>

<p>Don't forget to add me to your top 8!!!</p>
<p>xoxo,<br>Monsieur Poms 🐾</p>
</div>

<!-- DAILY STATUS BOARD -->
<div style="border: 3px ridge #FF00FF; padding: 12px; background: #000080; color: white; margin-bottom: 20px; font-family: 'Courier New', monospace;">
<h2 style="margin-top: 0; color: #FFFF00; text-align: center; text-shadow: 2px 2px #FF0000; letter-spacing: 2px;">★ POMS' DAILY STATUS BOARD ★</h2>
<div style="font-size: 9px; color: #AAAAAA; text-align: center; margin-bottom: 8px;">[ auto-updated every day — come back tomorrow!! ]</div>
<hr style="border-color: #FFFF00; margin-bottom: 10px;">
<table width="100%" cellpadding="4" style="font-size: 12px; border-collapse: collapse;">
<tr>
<td width="32%" style="color: #00FFFF; font-weight: bold; vertical-align: top;">STATUS:</td>
<td id="poms-status" style="color: #FFFFFF;">...</td>
</tr>
<tr>
<td style="color: #00FFFF; font-weight: bold; vertical-align: top;">MOOD:</td>
<td id="poms-mood" style="color: #FFFFFF;">...</td>
</tr>
<tr>
<td style="color: #00FFFF; font-weight: bold; vertical-align: top;">CURRENTLY:</td>
<td id="poms-activity" style="color: #FFFFFF;">...</td>
</tr>
<tr>
<td style="color: #00FFFF; font-weight: bold; vertical-align: top;">TODAY'S THOUGHT:</td>
<td id="poms-thought" style="color: #FFFF99; font-style: italic;">...</td>
</tr>
</table>
<div style="text-align: right; margin-top: 8px; font-size: 9px; color: #666666;" id="poms-date"></div>
</div>

<script>
(function() {
  var statuses = [
    "ONLINE (reluctantly)",
    "Away: napping",
    "Busy: judging",
    "In a meeting (food bowl press conference)",
    "Do Not Disturb: loafing",
    "Available for treats ONLY",
    "Offline: refusing vegetables",
    "Busy: strategic treat operations",
    "Away: storing height horizontally",
    "Currently: in the box",
    "Online: surveillance mode",
    "Busy: being professionally cute"
  ];
  var moods = [
    "Chatty 🗣️",
    "Judgmental 🐱",
    "Regal 👑",
    "Thoroughly Indifferent 😒",
    "Hungry (always) 🍗",
    "Smugly Satisfied 😏",
    "Deeply Suspicious 🤨",
    "Disappointed in Everyone 😠",
    "Contemplative 🤔",
    "Aggressively Cute 💕",
    "Philosophical ✨",
    "Strategically Motivated 🎯"
  ];
  var activities = [
    "Occupying the warmest spot on the couch",
    "Conducting a thorough investigation of the food bowl",
    "Staring at the wall (it did something)",
    "Performing quality control on the bed",
    "Holding a solo press conference about dinner",
    "Sitting in a box that appeared from nowhere",
    "Loafing in the sun like the majestic being I am",
    "Critiquing my human's work-from-home outfit",
    "Knocking something off the counter (for science)",
    "Demanding chicken via sustained vocalization",
    "Sleeping. This is content creation.",
    "Judging everyone from the window"
  ];
  var thoughts = [
    "If you give me chicken, I will allow you to pet me.",
    "The green bean incident was a personal attack. I have not forgotten.",
    "I am not fat. I am a cloud. Clouds are not fat.",
    "Every box in this house is my box. This is not negotiable.",
    "Woke up. Chose chaos. Knocked over a cup. Great morning.",
    "The humans keep calling me Binou. I have decided to allow it.",
    "I could be an apple soda brand ambassador. The brand should contact me.",
    "Meowing at 3am is called NETWORKING. You are welcome.",
    "I am simultaneously the smallest and most important thing in this house.",
    "They almost gave me a vegetable today. Almost.",
    "The spinning bottle on this website was my concept. I have excellent ideas.",
    "Today I shall sit like a perfect loaf and think about absolutely nothing."
  ];

  function hashDate(s) {
    var h = 0;
    for (var i = 0; i < s.length; i++) {
      h = Math.imul(31, h) + s.charCodeAt(i) | 0;
    }
    return Math.abs(h);
  }

  var d = new Date();
  var key = d.getFullYear() + '-' + (d.getMonth() + 1) + '-' + d.getDate();
  var seed = hashDate(key);

  document.getElementById('poms-status').textContent   = statuses  [(seed)       % statuses.length];
  document.getElementById('poms-mood').textContent     = moods     [(seed + 7)   % moods.length];
  document.getElementById('poms-activity').textContent = activities[(seed + 13)  % activities.length];
  document.getElementById('poms-thought').textContent  = '\u201C' + thoughts[(seed + 3) % thoughts.length] + '\u201D';
  document.getElementById('poms-date').textContent     = 'last updated: ' + d.toDateString();
})();
</script>

<!-- POST 2 -->
<div style="border: 1px solid #CCC; padding: 10px; background: #F9F9F9; margin-bottom: 20px;">
<h2 style="margin-top: 0;">😡 WHY ARE VEGETABLES?? 😡</h2>
<div style="font-size: 10px; color: #666;">Posted on: January 20, 2010 @ 10:00 AM | Mood: Angry</div>
<hr>
<p>Today my human tried to give me a green bean. A GREEN BEAN. Can you believe it???</p>
<p>I looked at them with my "disappointed eyes" and walked away. I deserve <strong>CHICKEN</strong>. Only chicken.</p>
<p><u>Update:</u> I got chicken later. Victory is mine.</p>
</div>
