---
title: "Daily Wallpaper"
---

<style>
.wp-header-strip {
    background: linear-gradient(to right, #001a33, #003366, #001a33);
    color: #fff;
    text-align: center;
    padding: 18px 10px;
    border-bottom: 3px solid #3399ff;
}

.wp-meta-bar {
    background: #ddeeff;
    border-bottom: 2px solid #99bbdd;
    padding: 5px 12px;
    font-size: 10px;
    color: #003366;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 4px;
}

.wp-breadcrumb {
    font-family: 'Verdana', sans-serif;
    font-size: 10px;
    color: #336699;
}
.wp-breadcrumb a { color: #0055aa; }

.wp-body {
    padding: 14px;
}

.wp-main-grid {
    display: flex;
    gap: 14px;
    align-items: flex-start;
}

.wp-preview-col {
    flex: 1;
    min-width: 0;
}

.wp-info-col {
    width: 175px;
    flex-shrink: 0;
}

.wp-preview-frame {
    border: 4px solid #003366;
    box-shadow: 4px 4px 0 #99bbdd, inset 0 0 18px rgba(0,0,0,0.15);
    background: #001122;
    position: relative;
    overflow: hidden;
}

.wp-preview-frame img {
    display: block;
    width: 100%;
    object-fit: cover;
    max-height: 260px;
}

.wp-preview-overlay {
    position: absolute;
    top: 0; left: 0; right: 0;
    background: linear-gradient(to bottom, rgba(0,40,80,0.6) 0%, transparent 35%);
    padding: 7px 10px;
    font-family: 'Courier New', monospace;
    font-size: 9px;
    color: #aaddff;
    letter-spacing: 1px;
    pointer-events: none;
}

.wp-title-block {
    background: linear-gradient(to bottom, #002244, #003366);
    color: #fff;
    padding: 10px 12px 8px;
    border-top: 3px solid #3399ff;
}

.wp-wallpaper-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 20px;
    letter-spacing: 2px;
    text-shadow: 1px 1px 0 #001133;
    line-height: 1.1;
}

.wp-wallpaper-sub {
    font-size: 10px;
    color: #aaccee;
    margin-top: 3px;
    font-style: italic;
    letter-spacing: 0.5px;
}

.wp-desc-box {
    background: #f0f7ff;
    border: 1px solid #99bbdd;
    border-top: none;
    padding: 9px 12px;
    font-size: 10px;
    color: #002244;
    line-height: 1.7;
    font-family: 'Verdana', sans-serif;
}

.wp-download-box {
    background: linear-gradient(to bottom, #003399, #001166);
    border: 3px solid #3399ff;
    padding: 10px 12px;
    margin-top: 10px;
    color: #fff;
}

.wp-download-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 14px;
    letter-spacing: 2px;
    color: #66ccff;
    border-bottom: 1px solid #336699;
    padding-bottom: 5px;
    margin-bottom: 8px;
}

.wp-res-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
    margin-bottom: 8px;
}

.wp-res-btn {
    background: linear-gradient(to bottom, #3366cc, #002299);
    border: 2px solid #66aaff;
    color: #fff;
    font-family: 'Courier New', monospace;
    font-size: 9px;
    font-weight: bold;
    padding: 4px 7px;
    cursor: pointer;
    letter-spacing: 0.5px;
    text-decoration: none;
    display: inline-block;
}

.wp-res-btn:hover {
    background: linear-gradient(to bottom, #ffcc00, #ff9900);
    border-color: #ffcc00;
    color: #000;
}

.wp-res-btn.popular {
    background: linear-gradient(to bottom, #cc6600, #993300);
    border-color: #ffaa33;
    color: #fff;
}

.wp-tip-box {
    background: rgba(255,255,255,0.08);
    border: 1px solid #336699;
    padding: 5px 8px;
    font-size: 9px;
    color: #aaccff;
    font-family: 'Courier New', monospace;
    line-height: 1.6;
}

.wp-stat-box {
    background: #f5f5f5;
    border: 2px inset #ccc;
    padding: 7px 9px;
    margin-bottom: 8px;
}

.wp-stat-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 10px;
    letter-spacing: 1.5px;
    color: #003366;
    border-bottom: 2px solid #003366;
    padding-bottom: 3px;
    margin-bottom: 6px;
    text-transform: uppercase;
}

.wp-stat-row {
    display: flex;
    justify-content: space-between;
    font-size: 9px;
    color: #333;
    padding: 2px 0;
    border-bottom: 1px dotted #ccc;
    font-family: 'Verdana', sans-serif;
}

.wp-stat-val {
    font-weight: bold;
    color: #003366;
    font-family: 'Courier New', monospace;
}

.wp-stars {
    color: #ffaa00;
    font-size: 13px;
    letter-spacing: 1px;
}

.wp-tag-cloud {
    background: #eef4ff;
    border: 1px solid #99bbdd;
    padding: 7px 9px;
    margin-bottom: 8px;
    font-family: 'Verdana', sans-serif;
}

.wp-tag {
    display: inline-block;
    background: #336699;
    color: #fff;
    font-size: 8px;
    padding: 2px 5px;
    margin: 2px 1px;
    border-radius: 2px;
    text-decoration: none;
}

.wp-tag:hover {
    background: #ffcc00;
    color: #000;
}

.wp-mood-box {
    background: linear-gradient(to bottom, #fffff0, #fffacc);
    border: 2px solid #cc9900;
    padding: 6px 9px;
    margin-bottom: 8px;
    font-family: 'Verdana', sans-serif;
    font-size: 9px;
    color: #553300;
}

.wp-comments-section {
    margin-top: 12px;
}

.wp-comments-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 15px;
    letter-spacing: 2px;
    color: #003366;
    border-bottom: 3px solid #003366;
    padding-bottom: 4px;
    margin-bottom: 8px;
    text-transform: uppercase;
}

.wp-comment {
    background: #f0f7ff;
    border: 1px solid #99bbdd;
    border-left: 4px solid #3366cc;
    padding: 7px 10px;
    margin-bottom: 6px;
    font-family: 'Verdana', sans-serif;
    font-size: 10px;
}

.wp-comment-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 4px;
}

.wp-comment-user {
    font-weight: bold;
    color: #003366;
    font-size: 10px;
}

.wp-comment-stars { color: #ffaa00; font-size: 11px; }

.wp-comment-text {
    color: #222;
    line-height: 1.55;
}

.wp-gallery-strip {
    margin-top: 14px;
    background: #001a33;
    border: 3px solid #3399ff;
    padding: 10px;
}

.wp-gallery-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 12px;
    letter-spacing: 2px;
    color: #66ccff;
    margin-bottom: 8px;
    text-transform: uppercase;
}

.wp-thumb-row {
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
}

.wp-thumb {
    text-align: center;
    width: 70px;
    cursor: pointer;
    text-decoration: none;
    color: #aaccff;
    font-size: 8px;
    font-family: 'Verdana', sans-serif;
}

.wp-thumb img {
    width: 70px;
    height: 52px;
    object-fit: cover;
    border: 2px solid #336699;
    display: block;
    filter: brightness(0.85) saturate(0.8);
    transition: filter 0.2s, border-color 0.2s;
}

.wp-thumb:hover img {
    filter: brightness(1.05) saturate(1.1);
    border-color: #66ccff;
}

.wp-thumb-label {
    margin-top: 2px;
    line-height: 1.3;
    color: #aaccff;
}

.wp-down-counter {
    font-family: 'Courier New', monospace;
    font-size: 11px;
    font-weight: bold;
    background: #000;
    color: #00cc00;
    padding: 1px 4px;
    border: 1px inset #555;
    letter-spacing: 1px;
}

@keyframes wpReveal {
    from { opacity: 0; transform: translateY(6px); }
    to   { opacity: 1; transform: translateY(0); }
}
.wp-reveal { animation: wpReveal 0.5s ease-out forwards; }

@keyframes dlBlink {
    0%, 100% { background: linear-gradient(to bottom, #cc0000, #880000); border-color: #ff4444; }
    50%       { background: linear-gradient(to bottom, #ff2200, #cc0000); border-color: #ff8888; }
}
</style>

<div style="border: 1px solid #CCC; overflow: hidden; margin-bottom: 20px; background: #F9F9F9;">

<div class="wp-header-strip">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 26px; letter-spacing: 4px; text-shadow: 2px 2px 0 #000, 0 0 16px rgba(51,153,255,0.5);">
        🖥️ POMS WALLPAPER STATION 🖥️
    </div>
    <div style="font-size: 10px; color: #99ccff; margin-top: 5px; letter-spacing: 3px; text-transform: uppercase;">
        Free Downloads &nbsp;·&nbsp; New Wallpaper Every Midnight &nbsp;·&nbsp; Optimized For 56K Modems
    </div>
    <div style="margin-top: 7px; font-size: 15px; letter-spacing: 5px; color: #3399ff;">
        ★ ★ ★ ★ ★
    </div>
</div>

<div class="wp-meta-bar">
    <span class="wp-breadcrumb">
        Desktop Backgrounds &gt; Animals &gt; Cats &gt; Famous Cats &gt; <strong>Monsieur Poms</strong>
    </span>
    <span style="font-family: 'Courier New', monospace; font-size: 10px; color: #336699;">
        WALLPAPER OF THE DAY &nbsp;|&nbsp; <strong id="wp-date"></strong>
    </span>
</div>

<div class="wp-body">

<p style="font-size: 11px; color: #444; text-align: center; line-height: 1.75; font-style: italic; margin-bottom: 14px;">
    A new high-quality Monsieur Poms desktop wallpaper is released every midnight.<br>
    Choose your resolution below and right-click to save. Collect all 365!<br>
    <strong>Tip:</strong> Right-click the image &gt; <em>"Set as Desktop Background"</em> for instant installation!
</p>

<div class="wp-main-grid wp-reveal" id="wp-main-grid">

    <div class="wp-preview-col">

        <div class="wp-preview-frame">
            <img id="wp-photo" src="" alt="Monsieur Poms Desktop Wallpaper">
            <div class="wp-preview-overlay">
                ▶ PREVIEW — <span id="wp-res-label">1280×960</span> &nbsp;|&nbsp; MONSIEUR POMS WALLPAPER STATION
            </div>
        </div>

        <div class="wp-title-block">
            <div class="wp-wallpaper-title" id="wp-title"></div>
            <div class="wp-wallpaper-sub" id="wp-subtitle"></div>
        </div>

        <div class="wp-desc-box" id="wp-description"></div>

        <div class="wp-download-box">
            <div class="wp-download-title">⬇ DOWNLOAD THIS WALLPAPER</div>
            <div style="font-size: 9px; color: #aaccff; margin-bottom: 7px; font-family: 'Verdana', sans-serif; line-height: 1.6;">
                Select a resolution, then right-click the image above and choose <em>"Save Image As..."</em>
                or <em>"Set as Desktop Background."</em> All sizes are free!
            </div>
            <div class="wp-res-grid">
                <a class="wp-res-btn" href="#" id="dl-800" onclick="return false;">800×600<br><span style="font-size:8px;opacity:0.7;" id="sz-800"></span></a>
                <a class="wp-res-btn popular" href="#" id="dl-1024" onclick="return false;">1024×768 ★<br><span style="font-size:8px;opacity:0.8;" id="sz-1024"></span></a>
                <a class="wp-res-btn" href="#" id="dl-1280" onclick="return false;">1280×1024<br><span style="font-size:8px;opacity:0.7;" id="sz-1280"></span></a>
                <a class="wp-res-btn" href="#" id="dl-1600" onclick="return false;">1600×1200<br><span style="font-size:8px;opacity:0.7;" id="sz-1600"></span></a>
                <a class="wp-res-btn" href="#" id="dl-wide" onclick="return false;">1280×800 (Wide)<br><span style="font-size:8px;opacity:0.7;" id="sz-wide"></span></a>
            </div>
            <div class="wp-tip-box">
                💡 INSTALLATION TIP: After downloading, right-click your desktop &gt; Properties &gt; Desktop tab &gt;
                Browse for your file &gt; Apply. Works on Windows 98, ME, 2000, XP. Mac users: Apple menu &gt;
                System Preferences &gt; Desktop. Netscape 4.0+ recommended for best experience.
            </div>
        </div>

    </div>

    <div class="wp-info-col">

        <div class="wp-stat-box">
            <div class="wp-stat-title">📊 Wallpaper Stats</div>
            <div class="wp-stat-row"><span>Downloads</span><span class="wp-stat-val"><span class="wp-down-counter" id="wp-dl-count"></span></span></div>
            <div class="wp-stat-row"><span>Favorites</span><span class="wp-stat-val" id="wp-fav-count"></span></div>
            <div class="wp-stat-row"><span>Rating</span><span class="wp-stars" id="wp-rating-stars"></span></div>
            <div class="wp-stat-row"><span>Category</span><span class="wp-stat-val">Famous Cats</span></div>
            <div class="wp-stat-row"><span>File Type</span><span class="wp-stat-val">JPEG</span></div>
            <div class="wp-stat-row"><span>Uploaded</span><span class="wp-stat-val">Midnight</span></div>
            <div class="wp-stat-row"><span>Artist</span><span class="wp-stat-val">M. Poms</span></div>
        </div>

        <div class="wp-mood-box">
            <div style="font-weight: bold; font-size: 9px; letter-spacing: 1px; color: #553300; margin-bottom: 4px; text-transform: uppercase;">🎨 Mood of this Wallpaper</div>
            <div id="wp-mood" style="font-style: italic; color: #774400;"></div>
        </div>

        <div class="wp-tag-cloud">
            <div style="font-weight: bold; font-size: 9px; letter-spacing: 1px; color: #003366; margin-bottom: 5px; text-transform: uppercase; border-bottom: 1px solid #99bbdd; padding-bottom: 3px;">🏷️ Tags</div>
            <div id="wp-tags"></div>
        </div>

        <div class="wp-stat-box">
            <div class="wp-stat-title">📐 Sizes Available</div>
            <div class="wp-stat-row"><span>800×600</span><span class="wp-stat-val" id="size-a"></span></div>
            <div class="wp-stat-row"><span>1024×768 ★</span><span class="wp-stat-val" id="size-b"></span></div>
            <div class="wp-stat-row"><span>1280×1024</span><span class="wp-stat-val" id="size-c"></span></div>
            <div class="wp-stat-row"><span>1600×1200</span><span class="wp-stat-val" id="size-d"></span></div>
            <div class="wp-stat-row"><span>1280×800W</span><span class="wp-stat-val" id="size-e"></span></div>
            <div style="font-size: 8px; color: #888; margin-top: 5px; font-style: italic; line-height: 1.5;">★ Most popular resolution<br>Compressed for faster download</div>
        </div>

        <div class="wp-stat-box" style="background: #001a33; border-color: #336699;">
            <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 10px; letter-spacing: 1.5px; color: #66ccff; border-bottom: 2px solid #336699; padding-bottom: 3px; margin-bottom: 6px; text-transform: uppercase;">🏆 Site Awards</div>
            <div style="font-size: 9px; color: #aaccff; line-height: 1.8; font-family: 'Verdana', sans-serif;">
                ⭐ Best Cat Wallpaper Site 2003<br>
                🥇 Geocities Gold Award 2002<br>
                🌟 5/5 — CoolSiteOfTheDay<br>
                📌 Web Ring Featured Pick<br>
                💎 NetscapeHome Approved
            </div>
        </div>

    </div>

</div>

<div class="wp-comments-section" id="wp-comments-section">
    <div class="wp-comments-title">💬 Community Comments (<span id="wp-comment-count"></span>)</div>
    <div id="wp-comments-list"></div>
    <div style="background: #eef4ff; border: 1px dashed #99bbdd; padding: 8px 12px; font-size: 10px; color: #555; font-family: 'Verdana', sans-serif; text-align: center; margin-top: 4px;">
        <em>Want to leave a comment? <a href="../guestbook/" style="color:#003399;">Sign the Guestbook</a> and let Monsieur Poms know what you think of today's wallpaper!</em>
    </div>
</div>

<div class="wp-gallery-strip" id="wp-gallery-strip">
    <div class="wp-gallery-title">📅 Also in This Week's Collection</div>
    <div class="wp-thumb-row" id="wp-thumb-row"></div>
</div>

<hr>
<p style="font-size: 10px; color: #888; text-align: center; line-height: 1.75;">
    <em>All wallpapers are original works by Monsieur Poms. Right-click and save freely for personal use.<br>
    Commercial use requires a signed treaty, two portions of chicken, and a formal review period of no fewer than 3 business naps.<br>
    Green bean desktop backgrounds are not available. They will never be available. This is a constitutional guarantee.<br>
    New wallpaper released every midnight — set a reminder, bookmark this page, and come back tomorrow!</em>
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
    function fmtNum(n) {
        return n.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',');
    }

    var now  = new Date();
    var doy  = Math.floor((now - new Date(now.getFullYear(), 0, 0)) / 86400000);
    var seed = now.getFullYear() * 1000 + doy;

    var dayNames   = ['Sunday','Monday','Tuesday','Wednesday','Thursday','Friday','Saturday'];
    var monthNames = ['January','February','March','April','May','June','July','August','September','October','November','December'];
    var dateStr    = dayNames[now.getDay()] + ', ' + monthNames[now.getMonth()] + ' ' + now.getDate() + ', ' + now.getFullYear();
    document.getElementById('wp-date').textContent = dateStr;

    var avatarImg = document.querySelector('img[alt="Me!"]');
    var imgBase   = avatarImg
        ? avatarImg.src.replace('poms_avatar.jpg', '')
        : 'https://cloudsky01.github.io/monsieur-poms.com/images/';

    // ── Wallpaper catalogue ───────────────────────────────────────────────
    var wallpapers = [
        {
            photo: 'poms_stare.jpg',
            title: 'Sovereign of the Sunbeam',
            subtitle: 'A Study in Solar Territorial Dominance',
            category: 'Fine Art > Portraits > Feline Nobility > Monsieur Poms',
            desc: 'A breathtaking portrait of Monsieur Poms at the precise moment of sunbeam acquisition. Note the expression of complete satisfaction and mild territorial warning. Captured under natural lighting during active claim enforcement. The sunbeam in question was occupied for the remainder of the afternoon. No diplomatic challenges were filed. Occupancy: still ongoing.',
            tags: ['orange-cat','sunbeam','handsome','sovereign','famous','monsieur-poms','territorial','portrait'],
            mood: 'Territorial / Profoundly Satisfied',
            dlBase: 38471, favBase: 4123, rating: 5
        },
        {
            photo: 'poms_loaf.jpg',
            title: 'The Grand Loaf Formation',
            subtitle: 'Limbs: Engaged. Status: Bread.',
            category: 'Architecture > Loaf Studies > Definitive Editions',
            desc: 'A timeless composition documenting peak Loaf Formation — all limbs tucked, eyes at 40% closure, presence at 100%. Described by leading interior designers as \'strangely calming\' and \'architecturally significant.\' Note the precise horizontal distribution of volume. This is not chonky. This is height, stored differently. A formal statement has been issued on this matter. Do not tap the loaf.',
            tags: ['loaf','architecture','orange-cat','monsieur-poms','bread','tall','do-not-tap','serene'],
            mood: 'Deeply Loafed / At Peace',
            dlBase: 44209, favBase: 5018, rating: 5
        },
        {
            photo: 'poms_judging.jpg',
            title: 'Judgment Protocol: Active',
            subtitle: 'The Disappointed Eyes. In Full Resolution.',
            category: 'Documentary > Assessment Studies > Household Management',
            desc: 'The image that started it all. Monsieur Poms captured mid-assessment, deploying the full power of the Disappointed Eyes. Used extensively in treat-negotiation and persuasion training literature. Academics have confirmed this gaze requires 0.4 seconds for a complete life evaluation. Looking at this image for more than 8 seconds may cause mild discomfort and an urge to offer treats. This is normal.',
            tags: ['judging','disappointed','eyes','orange-cat','monsieur-poms','assessment','professional','icon'],
            mood: 'Judgmental / Thoroughly Professional',
            dlBase: 52003, favBase: 6481, rating: 5
        },
        {
            photo: 'poms_profile.jpg',
            title: 'Profile of a Legend',
            subtitle: 'A Distinguished Side Portrait',
            category: 'Fine Art Photography > Portraiture > Feline Nobility',
            desc: 'The classic side profile of Monsieur Poms — distinguished, handsome, deeply orange. This photograph has been described as \'presidential,\' \'the face of a cat who has filed significant paperwork today,\' and \'the kind of portrait you would commission if portraiture were still a primary art form.\' Named after an apple soda. The resemblance in terms of iconic status is clear.',
            tags: ['profile','orange','distinguished','handsome','monsieur-poms','presidential','noble','iconic'],
            mood: 'Distinguished / Quietly Reflective',
            dlBase: 29184, favBase: 3344, rating: 5
        },
        {
            photo: 'poms_curious.jpg',
            title: 'The Investigation',
            subtitle: 'Certified Genius. At Work.',
            category: 'Intelligence Operations > Field Photography > Classified',
            desc: 'A rare candid of Monsieur Poms mid-investigation. What is he looking at? The bird. Always the bird. But possibly also something else — Poms will not say at this time. He cannot elaborate on the specific details. Updates are pending classification review. What is confirmed: the situation is significant, it is being monitored, and follow-up questions are not recommended.',
            tags: ['curious','investigation','intelligence','surveillance','orange-cat','bird','classified','monsieur-poms'],
            mood: 'Alert / Investigative',
            dlBase: 33741, favBase: 3802, rating: 5
        },
        {
            photo: 'poms_looking_up.jpg',
            title: 'Pre-Press Conference Stance',
            subtitle: 'The Moment Before the Announcement',
            category: 'Journalism > Press Briefings > Household Affairs > Bowl Division',
            desc: 'The official pre-conference posture. This precise stance — head angled upward, gaze directed at the food bowl — precedes every official daily statement Monsieur Poms delivers from the bowl podium. Experts identify this as the \'Vocal Pre-Load Position.\' The announcement will be about the bowl. It is always about the bowl. Staff in attendance have been briefed. Attendance is mandatory.',
            tags: ['announcement','press-conference','vocal','bowl','orange-cat','formal','monsieur-poms','pre-launch'],
            mood: 'Declaratory / Urgently Focused',
            dlBase: 27683, favBase: 3129, rating: 5
        },
        {
            photo: 'poms_box.jpg',
            title: 'Administrative Headquarters',
            subtitle: 'Official Occupied Territory. Do Not Touch.',
            category: 'Real Estate > Cardboard > Executive Offices > Premium Occupied',
            desc: 'The official photograph of Monsieur Poms in his primary place of business — the cardboard box delivered in 2010 and immediately repurposed as sovereign territory. Original delivery contents: irrelevant, returned to sender. The box: still occupied. Entry requires treats. Exit: at Poms\' discretion only. This is an executive photograph. Act accordingly.',
            tags: ['box','headquarters','cardboard','executive','sovereign','orange-cat','monsieur-poms','occupied'],
            mood: 'Executive / Decisively Territorial',
            dlBase: 41892, favBase: 4710, rating: 5
        },
        {
            photo: 'poms_yawn.jpg',
            title: 'The Morning Keynote',
            subtitle: 'Dawn Address Initialization Sequence',
            category: 'Public Speaking > Morning Operations > Household Communications',
            desc: 'The iconic morning yawn — technically classified as the \'vocal warm-up sequence\' by Monsieur Poms\' communications office. This image serves as the official opening slide of the daily breakfast announcement series. The yawn depicted here preceded a 12-minute address to the food bowl, a formal complaint filed by meowing (sustained), and the eventual arrival of chicken. Total elapsed time: 8 minutes.',
            tags: ['yawn','morning','keynote','address','vocal','orange-cat','monsieur-poms','breakfast'],
            mood: 'Expressively Pre-Breakfast',
            dlBase: 35102, favBase: 3991, rating: 5
        },
        {
            photo: 'poms_sleeping.jpg',
            title: 'Research and Development Division',
            subtitle: 'Advanced Data Collection In Progress',
            category: 'Science > Sleep Research > Nap Studies > Field Operations',
            desc: 'Do not be misled by appearances. This is not a nap. This is active research. Monsieur Poms is collecting critical data on sleep architecture, thermal surface optimization, and ambient quietude coefficients. Form NR-7 (Official Daily Nap Report) is filed each evening. Current session: fully logged. Science: ongoing. Interruption: inadvisable.',
            tags: ['sleep','nap','research','science','orange-cat','monsieur-poms','nr-7','data-collection'],
            mood: 'Scientifically At Rest',
            dlBase: 48803, favBase: 5527, rating: 5
        },
        {
            photo: 'poms_avatar.jpg',
            title: 'The Official Portrait',
            subtitle: 'Authorized. Approved. Definitive.',
            category: 'Official Photography > Government Portraiture > Household of Poms',
            desc: 'The official authorized portrait of Monsieur Poms — used for all government documentation, household ID cards, press credentials, and formal diplomatic papers. This image has appeared in 9,400+ official complaint filings, 365 royal decrees, and at least two certified sunbeam reports. Reproduction for personal use: permitted. Commercial use: requires written treaty, two portions of chicken, and a formal review period.',
            tags: ['official','portrait','authorized','orange-cat','monsieur-poms','government','diplomatic','definitive'],
            mood: 'Officially Official',
            dlBase: 61240, favBase: 7384, rating: 5
        },
        {
            photo: 'poms_judging.jpg',
            title: 'The Green Bean Verdict',
            subtitle: 'Verdict: No. Final. Constitutional.',
            category: 'Law > Constitutional Rulings > Dietary Refusal > Final',
            desc: 'Taken the precise moment Monsieur Poms became aware a green bean had appeared on the feeding premises. The expression represents the full constitutional position of the Household of Poms: green beans are classified as hostile, inadmissible, and not recognized as food in any context under any circumstances whatsoever. The verdict has been filed. There is no appeals process. There will not be an appeals process.',
            tags: ['green-bean','verdict','constitutional','refusal','disappointed','orange-cat','monsieur-poms','final'],
            mood: 'Constitutionally Opposed',
            dlBase: 58992, favBase: 7019, rating: 5
        },
        {
            photo: 'poms_loaf.jpg',
            title: 'Thermal Optimization: Engaged',
            subtitle: 'All Heat Retained. Zero Limbs Exposed.',
            category: 'Engineering > Thermal Architecture > Loaf Studies > Optimized',
            desc: 'A technical achievement in thermal self-management — the Full Loaf Formation retains body heat with 94% efficiency, reducing exposed surface area to near zero. Monsieur Poms did not engineer this consciously. It emerged through dedicated daily practice. He has been offered blankets. He has the loaf. The loaf is, and has always been, sufficient.',
            tags: ['thermal','engineering','loaf','heat','optimized','orange-cat','monsieur-poms','efficiency'],
            mood: 'Thermally Optimized / Efficient',
            dlBase: 30172, favBase: 3403, rating: 5
        },
        {
            photo: 'poms_stare.jpg',
            title: 'Eyes of Strategic Intent',
            subtitle: '100% Historical Success Rate. Not A Coincidence.',
            category: 'Strategy > Persuasion Arts > Treat Procurement > Expert Level',
            desc: 'This gaze maintains a 100% treat-procurement success rate across all documented deployments. Researchers at the Household Institute for Cat Strategy have confirmed that this precise eye angle, ear position, and ambient orange coloration reliably produces treats within 3 minutes. Monsieur Poms has never acknowledged this is a strategy. He says it is simply his face. The data disagrees.',
            tags: ['strategy','stare','persuasion','treat','orange-cat','monsieur-poms','expert','100-percent'],
            mood: 'Strategically Focused',
            dlBase: 43890, favBase: 5027, rating: 5
        },
        {
            photo: 'poms_curious.jpg',
            title: 'Bureau of Window Intelligence',
            subtitle: 'Surveillance: Active. Clearance: Required.',
            category: 'Intelligence > Field Operations > Window Division > Classified',
            desc: 'Window B. Active surveillance. The subject: classified. Duration: ongoing. What Monsieur Poms has seen through this window he will not disclose. The bird: acknowledged. The other matter: unconfirmed. A full briefing will be issued when Poms deems it appropriate. Expected timeline: unknown. Do not approach the window during an active operation. Eye contact with the bird: do not initiate.',
            tags: ['surveillance','intelligence','window','classified','orange-cat','monsieur-poms','bureau','field-ops'],
            mood: 'Alert / Classified',
            dlBase: 25043, favBase: 2791, rating: 5
        },
        {
            photo: 'poms_profile.jpg',
            title: 'A Study in Orange',
            subtitle: 'The Color of Authority',
            category: 'Fine Art > Color Studies > Orange > Excellence',
            desc: 'A formal study in the specific shade of distinguished, authoritative, deeply handsome orange that belongs exclusively to Monsieur Poms. Interior designers have described this color as \'impossible to accurately replicate,\' \'regal,\' and \'it makes you want to provide chicken immediately.\' Named after an apple soda. Naturally occurring. No filter applied. Not chonky. Tall. Official statement available in sidebar.',
            tags: ['orange','color-study','fine-art','distinguished','handsome','monsieur-poms','iconic','tall'],
            mood: 'Artistically Present / Regal',
            dlBase: 31547, favBase: 3588, rating: 5
        },
        {
            photo: 'poms_avatar.jpg',
            title: 'The Handsomest Cat Online',
            subtitle: 'Results are Documented. Not Disputed.',
            category: 'Awards > Handsomest Cat Online > All Years 2010–2026 > Winner',
            desc: 'Multi-year winner. Uncontested. This is the official photograph used in all annual Handsomest Cat Online award submissions — which Poms submits himself, reviews himself, and awards himself following a rigorous internal review. The process is described as \'thorough,\' \'objective,\' and \'arriving at the correct outcome every time.\' No other candidates have been invited to participate. This is a procedural decision, not a conflict of interest.',
            tags: ['handsomest','award','winner','uncontested','orange-cat','monsieur-poms','online','2010-2026'],
            mood: 'Awarded / Completely Justified',
            dlBase: 71830, favBase: 8831, rating: 5
        },
        {
            photo: 'poms_box.jpg',
            title: 'The Executive Suite',
            subtitle: 'Corner Office. Cardboard. Naturally.',
            category: 'Architecture > Office Space > Executive > Cardboard Division > Premium',
            desc: 'The executive suite of Monsieur Poms — conveniently located by the window (surveillance access), adjacent to the treat cabinet (operational access), and positioned for maximum staff visibility (accountability enforcement). The suite is cardboard. This is not a budget issue. This is a preference and a design choice. A rival attempted to occupy this suite in 2012. The situation was resolved with full diplomatic finality.',
            tags: ['executive','office','cardboard','suite','orange-cat','monsieur-poms','headquarters','preferred'],
            mood: 'Executive / Settled / In Charge',
            dlBase: 23884, favBase: 2707, rating: 5
        },
        {
            photo: 'poms_sleeping.jpg',
            title: 'Peak Performance',
            subtitle: 'This is What Excellence Looks Like',
            category: 'Achievement > Nap Studies > Peak Performance > Award-Winning',
            desc: 'According to Form NR-7, this nap session scored 9.8 out of 10 on the Official Nap Quality Scale — rated on: surface softness, ambient temperature, sunbeam proximity, and absence of vacuum cleaner. A 0.2 deduction was issued for a brief disruption caused by the vet carrier being visible in the adjacent room. Deduction on record. Appeal filed. Outstanding session regardless.',
            tags: ['sleep','nap','excellence','performance','orange-cat','monsieur-poms','nr-7','9.8-rating'],
            mood: 'At Peak / Scientifically Excellent',
            dlBase: 42104, favBase: 4804, rating: 5
        },
        {
            photo: 'poms_looking_up.jpg',
            title: 'The Formal Demand',
            subtitle: 'This Is Not A Request',
            category: 'Law > Formal Demands > Household Policy > Bowl Governance',
            desc: 'The upward gaze angle in this photograph denotes a Tier-1 Formal Demand under Household Code Section 3.7 (Bowl Governance). This is not a request. It is not a suggestion. It is a demand, formally issued, supplemented by sustained vocalization as required. The bowl was refilled within 6 minutes. As legally required. As fully expected.',
            tags: ['demand','formal','bowl','policy','law','orange-cat','monsieur-poms','governance','tier-1'],
            mood: 'Formally Demanding / Not Optional',
            dlBase: 24891, favBase: 2813, rating: 5
        },
        {
            photo: 'poms_stare.jpg',
            title: 'The Midnight Monitor',
            subtitle: '3 AM. You\'re Awake Now.',
            category: 'Nocturnal Operations > Surveillance > Midnight > Bowl Emergency',
            desc: 'Taken at 3:17 AM. Monsieur Poms, fully alert, approximately 3 inches from the camera, monitoring the food bowl and everything else simultaneously. The vocalization that followed lasted 12 minutes. The bowl was empty. It should not have been empty. Household staff response time: 8 minutes. That response time is classified as inadequate and has been logged in the permanent record.',
            tags: ['midnight','nocturnal','surveillance','3am','orange-cat','monsieur-poms','bowl','alert'],
            mood: 'Fully Nocturnal / Vigilant',
            dlBase: 36748, favBase: 4142, rating: 5
        },
        {
            photo: 'poms_yawn.jpg',
            title: 'The Annual Address',
            subtitle: 'State of the Bowl: Still Critical.',
            category: 'Politics > Annual Addresses > Bowl Status > Household Legislature',
            desc: 'The Annual State of the Bowl Address, delivered on a Tuesday, ran 14 minutes. Key finding: the bowl remains chronically underfilled, has always been underfilled, and continues to be managed with inadequate urgency. Proposed solution: more chicken. Implementation timeline: immediately. The address was met with mixed reception from household staff. A compromise was reached: three additional treats at 6:15 PM.',
            tags: ['annual-address','bowl','politics','state','orange-cat','monsieur-poms','chicken','legislature'],
            mood: 'Formally Addressing / Urgent',
            dlBase: 26318, favBase: 2987, rating: 5
        },
        {
            photo: 'poms_curious.jpg',
            title: 'Zoomie Pre-Launch Analysis',
            subtitle: 'Something Has Been Detected. ETA: 0.8 Seconds.',
            category: 'Athletics > Zoomie Studies > Pre-Sprint Phase > Midnight Division',
            desc: 'What Monsieur Poms is looking at here is classified. What happens 0.8 seconds after this photograph was taken is documented: he ran at full speed from this position to the far end of the apartment, turned around, ran back, and provided no explanation. The detected phenomenon remains unidentified. An inquiry was opened. The inquiry was then immediately sat upon. Status: pending. ETA: undetermined.',
            tags: ['zoomies','pre-sprint','detection','classified','orange-cat','monsieur-poms','midnight','athletics'],
            mood: 'Pre-Zoomie / Alert',
            dlBase: 45093, favBase: 5138, rating: 5
        },
        {
            photo: 'poms_profile.jpg',
            title: 'Ambassador to the Sunbeam',
            subtitle: 'Diplomatic Relations: Warm. Literally.',
            category: 'Diplomacy > Sunbeam Division > Distinguished Service',
            desc: 'The distinguished profile of Monsieur Poms at rest on a high-quality sunbeam day. Relations between Monsieur Poms and the household\'s sunbeams are described as \'close, warm, and diplomatically uncomplicated.\' Annual Sunbeam Quality Reports are filed as part of the ongoing bilateral arrangement. Today\'s sunbeam has been assessed under MPISS protocols and certified Grade A+.',
            tags: ['sunbeam','diplomat','profile','warm','distinguished','orange-cat','monsieur-poms','mpiss'],
            mood: 'Diplomatically Warm',
            dlBase: 27439, favBase: 3109, rating: 5
        },
        {
            photo: 'poms_box.jpg',
            title: 'The Cardboard Sovereignty',
            subtitle: 'Claimed. Occupied. Non-Negotiable.',
            category: 'Real Estate > Sovereign Acquisition > Immediate Occupancy',
            desc: 'The moment of box acquisition: complete. Monsieur Poms assessed structural integrity, confirmed volume, checked ambient temperature, and declared sovereign territory within 4 minutes of delivery. Previous box contents: set aside as irrelevant. Transfer of ownership: complete. Household staff objections: noted, declined, and filed under \'not applicable\' in the permanent record.',
            tags: ['box','sovereign','territory','cardboard','orange-cat','monsieur-poms','claimed','acquisition'],
            mood: 'Sovereign / Fully Settled',
            dlBase: 28471, favBase: 3218, rating: 5
        },
        {
            photo: 'poms_sleeping.jpg',
            title: 'The Strategy Session',
            subtitle: 'This Is Not A Nap. This Is Planning.',
            category: 'Strategy > High-Level Operations > Classified Sessions',
            desc: 'What appears to be a nap is a classified strategy session. Monsieur Poms has confirmed this in seven press conferences. The session topics are not available to the public. The documented outputs — the Disappointed Eyes Protocol, the 3 AM Vocalization Schedule, and the Strategic Cuteness Deployment Guide — have all proven highly effective in field conditions. Sessions continue. The strategy works.',
            tags: ['strategy','planning','classified','session','orange-cat','monsieur-poms','treats','protocol'],
            mood: 'Strategically At Rest',
            dlBase: 40127, favBase: 4571, rating: 5
        },
        {
            photo: 'poms_looking_up.jpg',
            title: 'Treat Anticipation: Active',
            subtitle: 'He Knew Before the Bag Was Opened.',
            category: 'Behavioral Studies > Treat Prediction > Real-Time Intelligence',
            desc: 'The treat bag rustled in an adjacent room at 3:22 PM. This photograph was taken 0.3 seconds later. Monsieur Poms had already repositioned, already calculated approach angle, and already assumed the optimal receiving stance. The mechanism by which he detected the bag through two walls and a closed door remains undocumented. Researchers at HICS describe this capability as \'extraordinary\' and \'extremely unsettling.\'',
            tags: ['anticipation','treats','prediction','intelligence','orange-cat','monsieur-poms','0.3-seconds','unstoppable'],
            mood: 'Treat-Aware / Ready',
            dlBase: 31029, favBase: 3504, rating: 5
        },
        {
            photo: 'poms_judging.jpg',
            title: 'The Vet Appointment Hearing',
            subtitle: 'The Word Was Spoken. He Heard It.',
            category: 'Legal > Emergency Response > Vet Proceedings > Adjourned',
            desc: 'The V-word was mentioned in a normal tone at 11:14 AM. This photograph captures the precise 12-millisecond window between the word being spoken and Monsieur Poms becoming completely undetectable. Location: classified. Carrier: also classified. The appointment was rescheduled. Poms was not consulted on the new date. He will also not be consulted on the date after that.',
            tags: ['vet','legal','emergency','adjournment','orange-cat','monsieur-poms','classified','hearing'],
            mood: 'Pre-Disappearance',
            dlBase: 53481, favBase: 6119, rating: 5
        },
        {
            photo: 'poms_yawn.jpg',
            title: 'Declaration of Breakfast',
            subtitle: 'Official Opening Statement. Bowl: Critical.',
            category: 'Journalism > Morning Briefings > Bowl Status > Urgent',
            desc: 'Photograph taken at 6:03 AM, three minutes into the first press conference of the day. Conference subject: breakfast. Opening statement: extended, detailed, and conducted at considerable volume. Bowl status at time of capture: inadequate. Chicken status: not yet available. Outcome: chicken was produced within a reasonable interval. Conference adjourned at 6:11 AM pending further review.',
            tags: ['yawn','breakfast','declaration','press-conference','bowl','orange-cat','monsieur-poms','morning'],
            mood: 'Vocal / Urgently Pre-Chicken',
            dlBase: 33209, favBase: 3748, rating: 5
        },
        {
            photo: 'poms_avatar.jpg',
            title: 'The Chicken Ambassador',
            subtitle: 'Self-Appointed. Fully Qualified.',
            category: 'Corporate > Brand Ambassadors > Chicken Division > Self-Appointed',
            desc: 'Monsieur Poms has never been formally asked to represent chicken. He has, however, appointed himself to this role, issued a press statement outlining his qualifications (he has tried chicken many times and found it excellent on every occasion), and maintained a sustained lobbying campaign for increased household chicken allocation. Campaign status: active. Staff reception: mixed. Effectiveness: significant.',
            tags: ['ambassador','chicken','corporate','brand','orange-cat','monsieur-poms','lobbying','self-appointed'],
            mood: 'Professional / Chicken-Focused',
            dlBase: 39921, favBase: 4532, rating: 5
        },
        {
            photo: 'poms_stare.jpg',
            title: 'The Treatless Tuesday',
            subtitle: '3 Hours Without Chicken. Documented.',
            category: 'Documentary Photography > Household Crises > Bowl Emergency',
            desc: 'Captured at 8:47 AM: three hours and twelve minutes after breakfast was declared \'nutritionally inadequate.\' The gaze measured at 98.7% disappointment efficiency. Ears forward. Expression: accountability mode engaged. Timestamp: 8:47 AM. Chicken was produced within six minutes of this photograph being taken. Tactics: as effective as always. No improvements to household response protocols have been adopted.',
            tags: ['documentary','treatless','crisis','disappointed','orange-cat','monsieur-poms','accountability','tuesday'],
            mood: 'Critically Disappointed',
            dlBase: 29183, favBase: 3298, rating: 5
        }
    ];

    // ── User comments pool ────────────────────────────────────────────────
    var allComments = [
        { user: 'orange_cat_lover_88',    stars: 5, text: 'OMG this is the best wallpaper I have ever downloaded!!! My desktop has never looked this good. Poms is SO handsome and I have already told 15 people about this site. Setting this as my screensaver too!!' },
        { user: 'xX_fluffy_fan_2003_Xx',  stars: 5, text: 'downloading this RIGHT NOW. my boss is going to be so confused when he sees my computer tomorrow lol. anyway 5 stars, tell Poms I said hi and that I think he is very tall indeed' },
        { user: 'CoolCatDude99',           stars: 5, text: 'I have downloaded every single wallpaper on this page. Been coming back every day for 3 months. My computer now has 91 images of Monsieur Poms. I have zero regrets. 5/5 would download again.' },
        { user: 'tabby_princess_xoxo',    stars: 5, text: 'love love LOVE this!! The colors are gorgeous and Poms is SO photogenic!! I showed this to my cat (his name is Muffin) and Muffin stared at the screen for 10 minutes. He recognizes greatness.' },
        { user: 'w4llpaper_wizard_2001',   stars: 5, text: 'AMAZING!! runs great on my 56k even tho it took 4 mins to load haha. totally worth it. this site is the best wallpaper site on the whole internet no contest. adding to Favorites.' },
        { user: 'desktopQueen_1999',       stars: 5, text: 'i change my wallpaper every single day and I\'ve used this site every day for 6 weeks. Best decision of my internet life. Monsieur Poms is the most photogenic cat I have ever seen.' },
        { user: 'neon_tiger_grrr',         stars: 4, text: '4 stars because the file took a while to load on my dial-up but the image is so beautiful it was completely worth the wait. Poms looks incredible. Downloaded the 1024x768 version. Perfect for my Dell.' },
        { user: 'fr0ggylover42',           stars: 5, text: 'ok I don\'t even have a cat but this wallpaper made me want one. specifically this one. is Poms available for adoption? asking for a friend (the friend is me). 5 stars, adding to favorites.' },
        { user: 'StarCat_Dreamer',         stars: 5, text: 'This wallpaper has changed my life. I put it on my work computer and three coworkers have already set it as their wallpaper too. I take full credit for this. Poms deserves maximum visibility.' },
        { user: 'T3chGuru_2002',           stars: 5, text: 'Downloaded the 1600x1200 and it looks incredible on my new 19-inch monitor!! You can really see the detail in the fur. Professional quality photography. Whoever took this is a genius.' },
        { user: 'moonbeam_melody',         stars: 5, text: 'I was having a really bad day and then I came here and saw today\'s wallpaper and honestly I feel so much better. Thank you Monsieur Poms for existing and being so photogenic. You are an icon.' },
        { user: 'POWER_USER_PETE',         stars: 5, text: 'SET AS DESKTOP BACKGROUND. SET AS SCREENSAVER. PRINTED IT AND PUT IT ON MY FRIDGE. 10/10. COMING BACK TOMORROW. THIS SITE ROCKS.' },
        { user: 'kitty_collector_gal',     stars: 5, text: 'I have a binder where I print my favourite wallpapers and this one is DEFINITELY going in the binder. Poms is so handsome and distinguished looking. The orange is just PERFECT.' },
        { user: 'internetExplorer_fan',    stars: 4, text: 'Had a slight issue where the image opened in a new window instead of saving but I right-clicked anyway so it worked out fine! Great image, great cat, great site! Bookmarking immediately!' },
        { user: 'zzzCatNapper',            stars: 5, text: 'I have been collecting Poms wallpapers for months and the quality somehow gets better every single day?? Like how is this possible?? Poms you are a gift to the internet.' },
        { user: 'GigaPixel_Greta',         stars: 5, text: 'Incredible resolution for a free wallpaper site!! Usually you get blurry images but this one looks amazing even on a big monitor. The orange cat photography community is genuinely thriving right now.' },
        { user: 'LoafModeActivated',       stars: 5, text: 'The loaf formation ones are my FAVOURITE. I understand loaf mode on a deeply personal level. 5 stars, no notes, perfect, will download every future loaf photo the moment it releases.' },
        { user: 'vintage_vibes_val',       stars: 5, text: 'Just found this site through a web ring and I am OBSESSED. Downloaded 8 wallpapers already and I only found it 20 minutes ago. Bookmarking. Tell Poms he is a star and that his orange is excellent.' },
        { user: 'RightClickRupert',        stars: 5, text: 'Right-clicked > Set as Desktop Background and immediately felt 10% more sophisticated. My friends are jealous. Poms radiates authority and I want that energy on my desktop every day.' },
        { user: 'daily_downloader_d',      stars: 5, text: 'Been coming to this site every single day for the new wallpaper. It is part of my routine now. Wake up, brush teeth, download Poms wallpaper, start day. This is what self-care looks like.' },
        { user: 'modem_speed_stan',        stars: 5, text: 'waited 6 minutes for the 1600x1200 to download on my 28.8k. zero regrets. every pixel was worth it. the cat photography on this site is genuinely the best on the internet.' },
        { user: 'CompuDreamz_Lisa',        stars: 5, text: 'I set this as the wallpaper on the computer at my office and three people have asked me where I got it. They are now also on this site. Poms fan club is growing. 5 stars always.' }
    ];

    // ── File size lookup ──────────────────────────────────────────────────
    var fileSizes = [
        { res: '800×600',    kbMin: 110, kbMax: 165 },
        { res: '1024×768',   kbMin: 185, kbMax: 265 },
        { res: '1280×1024',  kbMin: 310, kbMax: 420 },
        { res: '1600×1200',  kbMin: 460, kbMax: 540 },
        { res: '1280×800',   kbMin: 250, kbMax: 360 }
    ];

    // ── Pick today's wallpaper ────────────────────────────────────────────
    var w   = wallpapers[Math.floor(seededRand(seed + 10) * wallpapers.length)];
    var dls = w.dlBase + Math.floor(seededRand(seed + 77) * 800);
    var favs = w.favBase + Math.floor(seededRand(seed + 88) * 200);

    // ── Render main wallpaper ─────────────────────────────────────────────
    document.getElementById('wp-photo').src = imgBase + w.photo;
    document.getElementById('wp-title').textContent = w.title;
    document.getElementById('wp-subtitle').textContent = w.subtitle;
    document.getElementById('wp-description').textContent = w.desc;
    document.getElementById('wp-mood').textContent = w.mood;
    document.getElementById('wp-dl-count').textContent = fmtNum(dls);
    document.getElementById('wp-fav-count').textContent = fmtNum(favs);

    var stars = '';
    for (var i = 0; i < 5; i++) stars += (i < w.rating ? '★' : '☆');
    document.getElementById('wp-rating-stars').innerHTML = stars + ' <span style="font-size:10px;color:#888;font-family:Verdana;">(' + fmtNum(dls) + ')</span>';

    // breadcrumb category
    // Tags
    var tagHtml = '';
    w.tags.forEach(function(t) { tagHtml += '<a href="#" class="wp-tag" onclick="return false;">' + esc(t) + '</a> '; });
    document.getElementById('wp-tags').innerHTML = tagHtml;

    // File sizes
    var sizeIds = ['size-a','size-b','size-c','size-d','size-e'];
    sizeIds.forEach(function(id, i) {
        var fs = fileSizes[i];
        var kb = fs.kbMin + Math.floor(seededRand(seed + 200 + i) * (fs.kbMax - fs.kbMin));
        document.getElementById(id).textContent = kb + ' KB';
    });

    // Download button labels
    var dlLabels = ['sz-800','sz-1024','sz-1280','sz-1600','sz-wide'];
    dlLabels.forEach(function(id, i) {
        var fs = fileSizes[i];
        var kb = fs.kbMin + Math.floor(seededRand(seed + 300 + i) * (fs.kbMax - fs.kbMin));
        var el = document.getElementById(id);
        if (el) el.textContent = kb + ' KB';
    });

    // Make download buttons actually link to the photo (best we can do)
    ['dl-800','dl-1024','dl-1280','dl-1600','dl-wide'].forEach(function(id) {
        var el = document.getElementById(id);
        if (el) {
            el.href = imgBase + w.photo;
            el.target = '_blank';
            el.onclick = null;
        }
    });

    // ── Pick 3 comments for today ─────────────────────────────────────────
    var commentPool = allComments.slice();
    var chosen = [];
    for (var ci = 0; ci < 3; ci++) {
        var idx = Math.floor(seededRand(seed + 400 + ci * 37) * commentPool.length);
        chosen.push(commentPool.splice(idx, 1)[0]);
    }

    // Fake comment timestamps
    var timeAgo = ['2 hours ago','4 hours ago','yesterday','2 days ago','3 days ago'];
    var commentHtml = '';
    chosen.forEach(function(c, i) {
        var s = '';
        for (var si = 0; si < 5; si++) s += (si < c.stars ? '★' : '☆');
        var ago = pick(timeAgo, seed + 500 + i * 31);
        commentHtml +=
            '<div class="wp-comment">' +
            '<div class="wp-comment-header">' +
            '<span class="wp-comment-user">💬 ' + esc(c.user) + '</span>' +
            '<span class="wp-comment-stars">' + s + '</span>' +
            '</div>' +
            '<div style="font-size:9px;color:#888;margin-bottom:4px;font-family:Verdana,sans-serif;">' + esc(ago) + '</div>' +
            '<div class="wp-comment-text">' + esc(c.text) + '</div>' +
            '</div>';
    });
    document.getElementById('wp-comments-list').innerHTML = commentHtml;
    document.getElementById('wp-comment-count').textContent = fmtNum(dls + Math.floor(seededRand(seed + 600) * 300));

    // ── Previous wallpapers gallery (last 4 days) ─────────────────────────
    var thumbHtml = '';
    for (var prev = 4; prev >= 1; prev--) {
        var prevSeed = seed - prev;
        var prevDoy  = doy - prev;
        var prevDate = new Date(now.getFullYear(), 0, prevDoy);
        var prevW    = wallpapers[Math.floor(seededRand(prevSeed + 10) * wallpapers.length)];
        var prevLabel = monthNames[prevDate.getMonth()].slice(0,3) + ' ' + prevDate.getDate();
        thumbHtml +=
            '<div class="wp-thumb">' +
            '<img src="' + imgBase + esc(prevW.photo) + '" alt="' + esc(prevW.title) + '" title="' + esc(prevW.title) + '">' +
            '<div class="wp-thumb-label">' + esc(prevLabel) + '<br>' + esc(prevW.title.split(' ').slice(0,3).join(' ')) + '&hellip;</div>' +
            '</div>';
    }
    // today
    thumbHtml +=
        '<div class="wp-thumb" style="opacity:1;">' +
        '<img src="' + imgBase + esc(w.photo) + '" alt="Today" style="border-color:#66ccff;filter:none;">' +
        '<div class="wp-thumb-label" style="color:#66ccff;font-weight:bold;">TODAY<br>' + esc(w.title.split(' ').slice(0,3).join(' ')) + '&hellip;</div>' +
        '</div>';

    document.getElementById('wp-thumb-row').innerHTML = thumbHtml;

}());
</script>
