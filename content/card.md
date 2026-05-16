---
title: "Daily Trading Card"
---

<style>
.tcg-header-strip {
    background: linear-gradient(to right, #1a0040, #4400aa, #1a0040);
    color: #FFD700;
    text-align: center;
    padding: 18px 10px;
    margin: -10px -10px 0 -10px;
    border-bottom: 3px solid #FFD700;
}

.card-scene {
    display: flex;
    justify-content: center;
    margin: 20px 0;
    perspective: 900px;
}

.poms-card {
    width: 330px;
    border-radius: 14px;
    position: relative;
    overflow: hidden;
    border-width: 6px;
    border-style: solid;
    box-shadow: 0 0 30px rgba(0,0,0,0.45), 6px 6px 0 rgba(0,0,0,0.25);
    transition: transform 0.4s ease, box-shadow 0.4s ease;
    cursor: default;
    user-select: none;
}

.poms-card:hover {
    transform: rotateY(5deg) rotateX(-2deg) scale(1.02);
    box-shadow: -8px 14px 40px rgba(0,0,0,0.55), 6px 6px 0 rgba(0,0,0,0.25);
}

.card-holo {
    position: absolute;
    top: 0;
    left: -70%;
    width: 60%;
    height: 100%;
    background: linear-gradient(
        to right,
        transparent 0%,
        rgba(255,80,80,0.1) 15%,
        rgba(255,210,0,0.15) 30%,
        rgba(80,255,130,0.1) 50%,
        rgba(80,130,255,0.1) 70%,
        rgba(210,80,255,0.1) 85%,
        transparent 100%
    );
    opacity: 0;
    pointer-events: none;
    z-index: 50;
}

.poms-card:hover .card-holo {
    opacity: 1;
    animation: holoSlide 2.2s ease-in-out infinite alternate;
}

@keyframes holoSlide {
    0%   { left: -70%; }
    100% { left: 130%; }
}

@keyframes legendaryBorder {
    0%   { border-color: #FF0000; box-shadow: 0 0 35px rgba(255,0,0,0.5), 6px 6px 0 rgba(0,0,0,0.25); }
    16%  { border-color: #FF8800; box-shadow: 0 0 35px rgba(255,136,0,0.5), 6px 6px 0 rgba(0,0,0,0.25); }
    33%  { border-color: #FFD700; box-shadow: 0 0 35px rgba(255,215,0,0.5), 6px 6px 0 rgba(0,0,0,0.25); }
    50%  { border-color: #00CC44; box-shadow: 0 0 35px rgba(0,204,68,0.5), 6px 6px 0 rgba(0,0,0,0.25); }
    66%  { border-color: #0088FF; box-shadow: 0 0 35px rgba(0,136,255,0.5), 6px 6px 0 rgba(0,0,0,0.25); }
    83%  { border-color: #AA00FF; box-shadow: 0 0 35px rgba(170,0,255,0.5), 6px 6px 0 rgba(0,0,0,0.25); }
    100% { border-color: #FF0000; box-shadow: 0 0 35px rgba(255,0,0,0.5), 6px 6px 0 rgba(0,0,0,0.25); }
}

.card-header {
    padding: 8px 12px 5px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 6px;
}

.card-left {
    display: flex;
    align-items: center;
    gap: 6px;
    flex: 1;
    min-width: 0;
}

.card-type-badge {
    display: inline-block;
    font-family: 'Verdana', sans-serif;
    font-size: 7px;
    font-weight: bold;
    letter-spacing: 0.5px;
    padding: 2px 5px;
    border-radius: 3px;
    text-transform: uppercase;
    border: 1px solid rgba(0,0,0,0.3);
    white-space: nowrap;
    flex-shrink: 0;
}

.card-name {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 13px;
    letter-spacing: 1.5px;
    text-shadow: 1px 1px 0 rgba(0,0,0,0.25);
    white-space: nowrap;
}

.card-hp {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 12px;
    letter-spacing: 1px;
    white-space: nowrap;
    flex-shrink: 0;
}

.card-image-area {
    padding: 0 8px 4px;
}

.card-image-frame {
    display: block;
    border: 4px solid rgba(0,0,0,0.35);
    box-shadow: inset 0 0 12px rgba(0,0,0,0.25);
    overflow: hidden;
}

.card-image-frame img {
    display: block;
    width: 100%;
    height: 185px;
    object-fit: cover;
    filter: sepia(20%) contrast(1.06) brightness(0.97);
}

.card-subtype {
    font-family: 'Georgia', serif;
    font-size: 8px;
    font-style: italic;
    padding: 3px 12px;
    border-top: 1px solid rgba(0,0,0,0.2);
    border-bottom: 1px solid rgba(0,0,0,0.2);
    text-align: center;
    letter-spacing: 0.5px;
    color: rgba(0,0,0,0.6);
    margin-bottom: 4px;
    background: rgba(255,255,255,0.35);
}

.card-move-box {
    margin: 0 9px 5px;
    background: rgba(255,255,255,0.4);
    border: 1px solid rgba(0,0,0,0.18);
    border-radius: 4px;
    padding: 6px 9px;
}

.card-move-header {
    font-family: 'Verdana', sans-serif;
    font-weight: bold;
    font-size: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 3px;
    color: rgba(0,0,0,0.85);
}

.card-move-cost { font-size: 11px; letter-spacing: 1px; color: #996600; }

.card-move-effect {
    font-family: 'Georgia', serif;
    font-size: 9px;
    color: rgba(0,0,0,0.72);
    line-height: 1.5;
}

.card-stats {
    margin: 0 9px 4px;
    background: rgba(255,255,255,0.3);
    border: 1px solid rgba(0,0,0,0.14);
    border-radius: 4px;
    padding: 5px 7px;
}

.card-stats-title {
    font-family: 'Verdana', sans-serif;
    font-size: 7px;
    font-weight: bold;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: rgba(0,0,0,0.5);
    border-bottom: 1px dotted rgba(0,0,0,0.2);
    margin-bottom: 4px;
    padding-bottom: 2px;
}

.card-stat-row {
    display: flex;
    align-items: center;
    gap: 4px;
    margin-bottom: 3px;
}

.card-stat-lbl {
    font-family: 'Verdana', sans-serif;
    font-size: 7px;
    font-weight: bold;
    width: 80px;
    flex-shrink: 0;
    color: rgba(0,0,0,0.65);
}

.card-stat-bar-out {
    flex: 1;
    height: 7px;
    background: rgba(0,0,0,0.18);
    border-radius: 2px;
    overflow: hidden;
    border: 1px solid rgba(0,0,0,0.12);
}

.card-stat-bar-in {
    height: 100%;
    border-radius: 2px;
    animation: statFill 0.9s ease-out forwards;
}

@keyframes statFill { from { width: 0%; } }

.card-stat-num {
    font-family: 'Courier New', monospace;
    font-size: 8px;
    font-weight: bold;
    width: 20px;
    text-align: right;
    flex-shrink: 0;
}

.card-flavor {
    margin: 3px 9px 5px;
    padding: 4px 7px;
    font-family: 'Georgia', serif;
    font-size: 8.5px;
    font-style: italic;
    color: rgba(0,0,0,0.58);
    border-top: 1px dotted rgba(0,0,0,0.25);
    line-height: 1.55;
    text-align: center;
}

.card-footer {
    padding: 5px 10px 7px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-top: 2px solid rgba(0,0,0,0.18);
}

.card-rarity-label { font-family: 'Impact', 'Arial Black', sans-serif; font-size: 10px; line-height: 1.3; }
.card-num-edition  { font-family: 'Courier New', monospace; font-size: 8px; text-align: right; line-height: 1.5; color: rgba(0,0,0,0.5); }

.tcg-info-box {
    background: linear-gradient(to right, #0d0025, #1a0050);
    border: 3px solid #FFD700;
    color: #FFD700;
    padding: 14px 18px;
    margin: 16px 0 12px;
    text-align: center;
}

.tcg-collect-bar-out {
    background: #000;
    border: 2px inset #444;
    height: 22px;
    margin: 8px 0;
    overflow: hidden;
}

.tcg-collect-bar-in {
    height: 100%;
    background: linear-gradient(to right, #440088, #9933FF, #FFD700);
    animation: collectFill 1.2s ease-out forwards;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    padding-right: 4px;
    font-family: 'Courier New', monospace;
    font-size: 9px;
    color: #fff;
    font-weight: bold;
    min-width: 30px;
}

@keyframes collectFill { from { width: 0%; } }

.tcg-lore-box {
    background: #F9F9F9;
    border: 2px solid #CCC;
    padding: 10px 14px;
    font-size: 11px;
    font-family: 'Verdana', sans-serif;
    color: #333;
    line-height: 1.7;
    margin-bottom: 12px;
}

.tcg-lore-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 14px;
    color: #4400aa;
    letter-spacing: 2px;
    border-bottom: 2px solid #4400aa;
    margin-bottom: 8px;
    padding-bottom: 4px;
}
</style>

<div style="border: 1px solid #CCC; overflow: hidden; margin-bottom: 20px; background: #F9F9F9;">

<div class="tcg-header-strip">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 28px; letter-spacing: 4px; text-shadow: 2px 2px 0 #000, 0 0 20px rgba(255,215,0,0.4);">
        🃏 MONSIEUR POMS TCG 🃏
    </div>
    <div style="font-size: 10px; color: #DDB870; margin-top: 5px; letter-spacing: 3px; text-transform: uppercase;">
        Collect All 365 &nbsp;|&nbsp; Official Daily Trading Card &nbsp;|&nbsp; New Card Every Midnight
    </div>
    <div style="margin-top: 8px; font-size: 18px; letter-spacing: 4px;">✦ ★ ✦ ★ ✦ ★ ✦</div>
</div>

<div style="background: #EDE0FF; border-bottom: 3px double #4400aa; padding: 6px 12px; font-size: 10px; color: #2a0066; text-align: center;">
    CATEGORY: Collectibles &nbsp;|&nbsp; Poms Trading Card Game (TCG) &nbsp;|&nbsp; Est. 2010 &nbsp;|&nbsp; Today: <strong id="card-date"></strong>
</div>

<div style="padding: 14px;">

<p style="font-size: 11px; color: #444; text-align: center; line-height: 1.75; font-style: italic;">
    A new official Monsieur Poms card is issued every day at midnight.<br>
    Rarities range from Common to <strong>✨ LEGENDARY ✨</strong> (only ~7% of days!).<br>
    Hover the card for the authentic holographic TCG experience. Collect all 365!
</p>

<div class="card-scene">
    <div class="poms-card" id="the-card">
        <div class="card-holo"></div>

        <div class="card-header" id="card-header">
            <div class="card-left">
                <span class="card-type-badge" id="card-type-badge"></span>
                <span class="card-name">MONSIEUR POMS</span>
            </div>
            <div class="card-hp" id="card-hp-display"></div>
        </div>

        <div class="card-image-area">
            <div class="card-image-frame">
                <img id="card-photo" src="" alt="Monsieur Poms">
            </div>
        </div>

        <div class="card-subtype" id="card-subtype-text"></div>

        <div class="card-move-box">
            <div class="card-move-header">
                <span id="card-move-name"></span>
                <span class="card-move-cost" id="card-move-cost"></span>
            </div>
            <div class="card-move-effect" id="card-move-effect"></div>
        </div>

        <div class="card-stats">
            <div class="card-stats-title">Stats</div>
            <div id="card-stats-container"></div>
        </div>

        <div class="card-flavor" id="card-flavor-text"></div>

        <div class="card-footer" id="card-footer">
            <div class="card-rarity-label" id="card-rarity-label"></div>
            <div class="card-num-edition" id="card-num-edition"></div>
        </div>
    </div>
</div>

<div class="tcg-info-box">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 16px; letter-spacing: 2px;">
        📦 COLLECTION PROGRESS
    </div>
    <div style="font-size: 10px; color: #BB99FF; margin-top: 3px; letter-spacing: 2px;">
        Today is card <strong id="card-day-num" style="color:#FFD700;"></strong> of 365
    </div>
    <div class="tcg-collect-bar-out">
        <div class="tcg-collect-bar-in" id="collect-bar"></div>
    </div>
    <div style="font-size: 10px; color: #BB99FF;">
        Visit every day to collect all <strong style="color:#FFD700;">365 cards</strong> by end of year!
    </div>
    <div style="font-size: 9px; color: #886699; margin-top: 6px; font-style: italic;">
        Yesterday was card #<span id="yesterday-num"></span>.
        Come back tomorrow for card #<span id="tomorrow-num"></span>!
    </div>
</div>

<div class="tcg-lore-box">
    <div class="tcg-lore-title">📖 ABOUT THE POMS TCG</div>
    <p style="margin: 0 0 8px 0;">
        The <strong>Monsieur Poms Trading Card Game</strong> was established in 2010 alongside this website.
        Monsieur Poms personally approved the card designs after reviewing them for 45 minutes — from directly on top of them.
    </p>
    <p style="margin: 0 0 8px 0;">
        The set features <strong>365 unique cards</strong>, one per day of the year. Five rarity tiers exist:
        Common (35%), Uncommon (25%), Rare (20%), Ultra Rare (13%), and
        <strong>✨ Legendary</strong> (~7%) — identifiable by its animated rainbow border.
    </p>
    <p style="margin: 0;">
        <strong>World Championship:</strong> The Poms TCG World Championship is held annually.
        Prize: one full chicken, served at optimal temperature.
        Monsieur Poms has been champion every year since 2010.
        He enters himself. He also judges. He sees no conflict of interest here.
    </p>
</div>

<hr>
<p style="font-size: 10px; color: #888; text-align: center; line-height: 1.75;">
    <em>The Monsieur Poms TCG accepts no responsibility for the compulsive desire to visit daily.<br>
    Green bean cards do not exist and will never exist. This is a constitutional guarantee.<br>
    Legendary cards should be shown to no fewer than three people immediately upon discovery.</em>
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
    document.getElementById('card-date').textContent =
        dayNames[now.getDay()] + ", " + monthNames[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear();

    var cardNum = doy + 1;
    document.getElementById('card-day-num').textContent   = cardNum;
    document.getElementById('yesterday-num').textContent  = cardNum > 1   ? cardNum - 1 : 365;
    document.getElementById('tomorrow-num').textContent   = cardNum < 365 ? cardNum + 1 : 1;

    var pct    = Math.round(cardNum / 365 * 100);
    var barEl  = document.getElementById('collect-bar');
    barEl.style.width = pct + '%';
    barEl.textContent = cardNum + ' / 365';

    var avatarImg = document.querySelector('img[alt="Me!"]');
    var imgBase   = avatarImg
        ? avatarImg.src.replace('poms_avatar.jpg', '')
        : 'https://cloudsky01.github.io/monsieur-poms.com/images/';

    // ── Data ──────────────────────────────────────────────────────────────

    var photos = [
        "poms_judging.jpg","poms_stare.jpg","poms_profile.jpg","poms_loaf.jpg",
        "poms_curious.jpg","poms_looking_up.jpg","poms_avatar.jpg",
        "poms_sleeping.jpg","poms_yawn.jpg","poms_box.jpg"
    ];

    var cardTypes = [
        { label:"VOCAL",        emoji:"📢", textColor:"#FFFFFF", badgeBg:"#CC4400" },
        { label:"JUDGEMENTAL",  emoji:"👁️", textColor:"#FFFFFF", badgeBg:"#550077" },
        { label:"HUNGRY",       emoji:"🍗", textColor:"#FFFFFF", badgeBg:"#992200" },
        { label:"SLEEPY",       emoji:"💤", textColor:"#FFFFFF", badgeBg:"#334488" },
        { label:"STRATEGIC",    emoji:"🧠", textColor:"#FFFFFF", badgeBg:"#005544" },
        { label:"LOAF",         emoji:"🍞", textColor:"#000000", badgeBg:"#C8A040" },
        { label:"SURVEILLANCE", emoji:"🔭", textColor:"#FFFFFF", badgeBg:"#003300" },
        { label:"DIPLOMATIC",   emoji:"📋", textColor:"#000000", badgeBg:"#D4B800" }
    ];

    var subtypes = [
        "Cat · Orange · Professional Talker · Apple Soda Brand Ambassador",
        "Cat · Feline · Certified Oracle · Press Conference Specialist",
        "Cat · Vocal · Puzzle Master · Sunbeam Occupation Expert",
        "Cat · Orange · Loaf Formation Practitioner · Treat Strategist",
        "Cat · Handsome · Nocturnal Operations Specialist · Chicken Enthusiast",
        "Cat · Tall (Horizontally) · Chief Meteorologist · Decree Issuer",
        "Cat · Award-Winning Napper · Window Surveillance Officer",
        "Cat · Bine · Binou · Monsieur Chonk · The Tall One"
    ];

    var moves = [
        { name:"Disappointed Eyes",         cost:"★★",  effect:"Lowers target willpower by 80%. Treats produced within 60 seconds. Has never failed. Not once." },
        { name:"3 AM Vocalization",          cost:"★★★", effect:"Immediately awakens all targets. Food bowl refilled. Damage: severe household inconvenience." },
        { name:"Loaf Formation",             cost:"★",   effect:"Becomes completely immovable. Defense +200. Duration: indefinite. This is strategy, not laziness." },
        { name:"Sunbeam Claim Protocol",     cost:"★★",  effect:"Occupies prime territory immediately. Sovereign property effective now. Diplomatic notice: none." },
        { name:"Food Puzzle Blitz",          cost:"★★",  effect:"Defeats any food obstacle in record time. Intellect rating: confirmed genius. Treat: acquired." },
        { name:"Strategic Cuteness",         cost:"★",   effect:"Deploys calibrated cuteness to obtain treats. Effectiveness: 100%. Duration: exactly as long as needed." },
        { name:"Keyboard Oversight",         cost:"★",   effect:"Occupies keyboard. Provides unsolicited editorial input. Deletions are not accepted as peer review." },
        { name:"Zoomie Protocol",            cost:"★★★", effect:"Maximum speed. Full apartment traversal. Reason: classified. Do not follow. Do not ask questions." },
        { name:"Emergency Press Conference", cost:"★★★", effect:"Addresses all grievances at full volume. Duration: indefinite. Topic: the bowl. Attendance: mandatory." },
        { name:"The Belly Trap",             cost:"★★",  effect:"Exposes belly. Target makes contact. Consequence: biting. Effectiveness: legendary. Remorse: none." },
        { name:"Thermal Face Press",         cost:"★",   effect:"Contacts target face for temperature regulation. Non-sentimental. This has never been sentimental." },
        { name:"Wall Staring Event",         cost:"★★★", effect:"Stares at wall for 14+ minutes. What is seen cannot be explained. It was significant. That is all." },
        { name:"Treat Bag Detection",        cost:"★★",  effect:"Detects treat bag at maximum range. Response time: 0.3 seconds. Triggered by rustling through walls." },
        { name:"Window Surveillance",        cost:"★",   effect:"Full bird monitoring activated. Intelligence: classified. Updates: pending. Post: fully occupied." },
        { name:"The Tall Defense",           cost:"★",   effect:"Absorbs all 'chonky' insults with zero damage. Subject is TALL. Height stored horizontally is still height." },
        { name:"The 4 AM Stare",             cost:"★★",  effect:"Stares at target from 3 inches away until woken. Reason: the bowl. Unstated reason: also the bowl." }
    ];

    var flavors = [
        "Named after a legendary apple soda. Refreshing, iconic, and full of opinions about the bowl.",
        "The height is stored horizontally. This is not chonkiness. This is advanced vertical architecture.",
        "Holds daily press conferences at the food bowl. Topic: always the bowl. Audience: mandatory.",
        "Defeated the food puzzle in record time. Again. As expected. He is, after all, a certified genius.",
        "Has been monitoring the bird situation outside Window B. He cannot elaborate. Updates: pending.",
        "Currently in loaf mode. All limbs tucked. Do not tap. Chicken may be offered reverently.",
        "Has filed 9,400+ formal complaints since 2010. Rate: 3.47 per day. Not expected to decrease.",
        "The treat bag rustled. He arrived in 0.3 seconds. Some say he was already there.",
        "Sat next to his human tonight. Proximity only. Not commitment. This distinction is legally important.",
        "Maintained unbroken eye contact with the dog through Window B for four consecutive days.",
        "Knocked something off the counter. Called it a social experiment. Zero remorse was observed.",
        "Invented a new meow specifically for treat urgency. Patent pending. Field effectiveness: perfect.",
        "Pressed face against human's face at 4 AM. Temperature regulation. Do not read into this.",
        "Coat is immaculate. Grooming began at 6 AM. Professionalism is important and non-negotiable.",
        "The sunbeam has been claimed. This is not up for discussion. Security: fully active.",
        "The vet's name was spoken. Monsieur Poms' location is now classified. The carrier: also classified.",
        "Ran at full speed through the apartment at midnight. Reason: classified. He cannot comment.",
        "Occupies approximately 80% of the available sofa. Remaining 20% is a courtesy, revocable at will.",
        "Entered the cardboard box voluntarily. Entry reason: unknown. Exit: not currently imminent.",
        "Ate a bug today. Released it. Reconsidered. Re-caught it. The outcome remains under investigation."
    ];

    var editions = [
        { name:"Orange Edition",
          cardBg:"linear-gradient(160deg,#FFF3CC 0%,#FFE899 40%,#FFD060 100%)",
          borderColor:"#CC7700", headerBg:"#994400", headerColor:"#FFD700",
          footerBg:"#FFD060", footerColor:"#5c2800", statColor:"#CC5500" },
        { name:"Royal Blue Edition",
          cardBg:"linear-gradient(160deg,#E8F0FF 0%,#C0D4FF 40%,#8AABFF 100%)",
          borderColor:"#1133AA", headerBg:"#001188", headerColor:"#FFD700",
          footerBg:"#8AABFF", footerColor:"#000055", statColor:"#0044CC" },
        { name:"Midnight Edition",
          cardBg:"linear-gradient(160deg,#F0E0FF 0%,#D8B8FF 40%,#BB88FF 100%)",
          borderColor:"#5500BB", headerBg:"#220044", headerColor:"#FFD700",
          footerBg:"#BB88FF", footerColor:"#1a0040", statColor:"#7722CC" },
        { name:"Sunbeam Edition",
          cardBg:"linear-gradient(160deg,#FFFDE8 0%,#FFF799 40%,#FFE844 100%)",
          borderColor:"#886600", headerBg:"#4D3800", headerColor:"#FFD700",
          footerBg:"#FFE844", footerColor:"#332500", statColor:"#886600" },
        { name:"Crimson Edition",
          cardBg:"linear-gradient(160deg,#FFE8E8 0%,#FFB8B8 40%,#FF8888 100%)",
          borderColor:"#AA0000", headerBg:"#660000", headerColor:"#FFD700",
          footerBg:"#FF8888", footerColor:"#440000", statColor:"#CC0000" },
        { name:"Forest Edition",
          cardBg:"linear-gradient(160deg,#E8F5E8 0%,#B8DDB8 40%,#88CC88 100%)",
          borderColor:"#224422", headerBg:"#113311", headerColor:"#AAFFAA",
          footerBg:"#88CC88", footerColor:"#1a3300", statColor:"#226622" }
    ];

    var rarityRoll = seededRand(seed + 700);
    var rarity;
    if      (rarityRoll < 0.35) rarity = { name:"COMMON",          stars:1, color:"#888888", legendary:false };
    else if (rarityRoll < 0.60) rarity = { name:"UNCOMMON",        stars:2, color:"#22AA22", legendary:false };
    else if (rarityRoll < 0.80) rarity = { name:"RARE",            stars:3, color:"#1144CC", legendary:false };
    else if (rarityRoll < 0.93) rarity = { name:"ULTRA RARE",      stars:4, color:"#9922CC", legendary:false };
    else                         rarity = { name:"✨ LEGENDARY ✨",  stars:5, color:"#AA6600", legendary:true  };

    // ── Pick today's card ──────────────────────────────────────────────────
    var photo    = pick(photos,    seed + 10);
    var cType    = pick(cardTypes, seed + 20);
    var subtype  = pick(subtypes,  seed + 30);
    var move     = pick(moves,     seed + 40);
    var flavor   = pick(flavors,   seed + 50);
    var edition  = pick(editions,  seed + 60);

    var hp = 40 + Math.floor(seededRand(seed + 1) * 221);

    var statDefs = [
        { label:"CUTENESS ATK", val: 50 + Math.floor(seededRand(seed + 2) * 50), color:"#FF6699" },
        { label:"JUDGMENT DEF", val: 30 + Math.floor(seededRand(seed + 3) * 70), color:"#7722AA" },
        { label:"NAP SPEED",    val: 20 + Math.floor(seededRand(seed + 4) * 80), color:"#3355CC" },
        { label:"VOCAL POWER",  val: 60 + Math.floor(seededRand(seed + 5) * 40), color:"#FF4400" },
        { label:"CHICKEN DMD",  val: 65 + Math.floor(seededRand(seed + 6) * 35), color:"#CC6600" }
    ];

    // ── Render ────────────────────────────────────────────────────────────
    var card = document.getElementById('the-card');
    card.style.background  = edition.cardBg;
    card.style.borderColor = edition.borderColor;
    if (rarity.legendary) {
        card.style.animation   = 'legendaryBorder 3s linear infinite';
        card.style.borderWidth = '7px';
    }

    var hdr = document.getElementById('card-header');
    hdr.style.background = edition.headerBg;
    hdr.style.color      = edition.headerColor;

    var badge = document.getElementById('card-type-badge');
    badge.textContent      = cType.emoji + ' ' + cType.label;
    badge.style.background = cType.badgeBg;
    badge.style.color      = cType.textColor;

    var hpEl = document.getElementById('card-hp-display');
    hpEl.textContent  = 'HP ' + hp;
    hpEl.style.color  = edition.headerColor;

    document.getElementById('card-photo').src = imgBase + photo;
    document.getElementById('card-subtype-text').textContent = subtype;
    document.getElementById('card-move-name').textContent    = move.name;
    document.getElementById('card-move-cost').textContent    = move.cost;
    document.getElementById('card-move-effect').textContent  = move.effect;

    var sc = document.getElementById('card-stats-container');
    statDefs.forEach(function (s) {
        var row = document.createElement('div');
        row.className = 'card-stat-row';
        row.innerHTML =
            '<div class="card-stat-lbl">' + s.label + '</div>' +
            '<div class="card-stat-bar-out">' +
                '<div class="card-stat-bar-in" style="width:' + s.val + '%;background:linear-gradient(to right,' + s.color + '99,' + s.color + ');"></div>' +
            '</div>' +
            '<div class="card-stat-num" style="color:' + s.color + ';">' + s.val + '</div>';
        sc.appendChild(row);
    });

    document.getElementById('card-flavor-text').innerHTML = '&ldquo;' + esc(flavor) + '&rdquo;';

    var ftr = document.getElementById('card-footer');
    ftr.style.background = edition.footerBg;
    ftr.style.color      = edition.footerColor;

    var stars = '';
    for (var i = 0; i < 5; i++) stars += (i < rarity.stars ? '★' : '☆');

    document.getElementById('card-rarity-label').innerHTML =
        '<span style="color:' + rarity.color + ';font-size:12px;">' + stars + '</span>' +
        '<br><span style="color:' + rarity.color + ';font-size:9px;letter-spacing:1px;">' + esc(rarity.name) + '</span>';

    document.getElementById('card-num-edition').innerHTML =
        '<strong>Card #' + cardNum + '</strong> / 365<br>' + esc(edition.name);

}());
</script>
