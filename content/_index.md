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
<h3>PICTURE OF THE DAY</h3>
<img id="potd-img" src="" alt="Poms" style="width: 100%; max-width: 400px; border: 2px solid #000; display: block; margin: 0 auto;">
<p><em id="potd-caption"></em></p>
<div style="font-size: 10px; color: #888;" id="potd-date"></div>
</div>

<script>
(function() {
    var images = [
        {src: 'poms_sleeping.jpg',    caption: "Me 'working' hard lol!!! xD"},
        {src: 'poms_loaf.jpg',        caption: 'Perfect Orange Loaf mode activated'},
        {src: 'poms_yawn.jpg',        caption: 'RAAAWR!! (Big yawn)'},
        {src: 'poms_stare.jpg',       caption: 'Staring into your soul... do you feel it?'},
        {src: 'poms_box.jpg',         caption: 'If I fits, I sits. This is science.'},
        {src: 'poms_judging.jpg',     caption: 'Judging your life choices (and finding them lacking)'},
        {src: 'poms_profile.jpg',     caption: 'Distinguished Gentleman Profile Shot'},
        {src: 'poms_curious.jpg',     caption: 'Investigating suspicious activity in the vicinity'},
        {src: 'poms_looking_up.jpg',  caption: 'Looking up the ceiling bug situation'},
        {src: 'poms_avatar.jpg',      caption: 'My official portrait. Hang it in the Louvre.'},
        {src: 'poms_drink.jpg',       caption: 'Official POMS Apple Soda Brand Ambassador photo!!!'}
    ];
    var baseURL = 'https://cloudsky01.github.io/monsieur-poms.com/images/';
    var now = new Date();
    var start = new Date(now.getFullYear(), 0, 0);
    var dayOfYear = Math.floor((now - start) / 86400000);
    var pic = images[dayOfYear % images.length];
    document.getElementById('potd-img').src = baseURL + pic.src;
    document.getElementById('potd-caption').textContent = pic.caption;
    var months = ['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec'];
    document.getElementById('potd-date').textContent =
        'Photo of the Day for ' + months[now.getMonth()] + ' ' + now.getDate() + ', ' + now.getFullYear();
})();
</script>

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
