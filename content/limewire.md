---
title: "Poms's LimeWire"
---

<style>
.lw-page-header {
    background: linear-gradient(135deg, #001a33 0%, #003366 50%, #001a33 100%);
    color: #00FF66;
    text-align: center;
    padding: 16px 12px;
    margin: -20px -20px 0 -20px;
    border-bottom: 3px solid #00FF66;
    font-family: 'Verdana', sans-serif;
}
.lw-page-header p { font-size: 11px; color: #88FFAA; margin: 4px 0; }
.lw-date-badge {
    display: inline-block;
    background: #FF3300;
    color: #FFF;
    font-weight: bold;
    font-size: 10px;
    padding: 2px 8px;
    border: 1px solid #FF6600;
    margin-top: 6px;
    font-family: 'Courier New', monospace;
}
#riaa-popup {
    position: fixed; top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    background: #D4D0C8;
    border: 2px solid; border-color: #FFFFFF #808080 #808080 #FFFFFF;
    box-shadow: 3px 3px 8px rgba(0,0,0,0.5);
    z-index: 9999; width: 320px;
    font-family: 'Verdana', sans-serif; font-size: 11px;
}
.riaa-titlebar {
    background: linear-gradient(to right, #AA0000, #FF0000);
    color: white; padding: 3px 6px; font-weight: bold; font-size: 11px;
    display: flex; justify-content: space-between; align-items: center;
}
.riaa-body { padding: 16px; text-align: center; color: #000; }
.riaa-body p { margin: 6px 0; font-size: 11px; }
.riaa-note { font-size: 9px; color: #666; margin-top: 10px; }
.riaa-ok-btn {
    background: linear-gradient(to bottom, #fff 0%, #e0e0e0 100%);
    border: 2px solid; border-color: #FFFFFF #808080 #808080 #FFFFFF;
    padding: 4px 16px; margin-top: 10px; cursor: pointer;
    font-family: 'Verdana', sans-serif; font-size: 11px; font-weight: bold;
}
.riaa-ok-btn:hover { background: #0000FF; color: white; }
#riaa-overlay {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    background: rgba(0,0,0,0.4); z-index: 9998;
}
.lw-window {
    background: #D4D0C8;
    border: 2px solid; border-color: #FFFFFF #808080 #808080 #FFFFFF;
    box-shadow: 2px 2px 5px rgba(0,0,0,0.3);
    margin: 16px 0 0 0;
    font-family: 'Verdana', 'Arial', sans-serif; font-size: 11px;
}
.lw-titlebar {
    background: linear-gradient(to bottom, #1a2a3a 0%, #0a1822 100%);
    color: #CCDDEE; padding: 3px 6px;
    display: flex; justify-content: space-between; align-items: center;
    font-size: 11px; font-weight: bold; user-select: none;
}
.lw-logo-text { color: #00FF66; font-style: italic; font-weight: bold; }
.lw-titlebar-btns { display: flex; gap: 3px; }
.lw-titlebar-btn {
    background: #D4D0C8; border: 2px solid;
    border-color: #FFFFFF #808080 #808080 #FFFFFF;
    width: 16px; height: 14px; font-size: 9px; font-weight: bold;
    display: flex; align-items: center; justify-content: center;
    cursor: default; color: #000; line-height: 1;
}
.lw-menubar {
    background: #D4D0C8; border-bottom: 1px solid #808080;
    padding: 2px 6px; font-size: 10px; color: #000;
    display: flex; gap: 14px; user-select: none;
}
.lw-tabs {
    background: #C0C0C0; display: flex; padding: 4px 4px 0 4px;
    gap: 2px; border-bottom: 2px solid #888;
}
.lw-tab {
    background: #B0B0B0; border: 1px solid #808080; border-bottom: none;
    padding: 3px 10px; font-size: 10px; cursor: default; color: #444;
    user-select: none; border-radius: 3px 3px 0 0;
}
.lw-tab.active {
    background: #FFFFFF; color: #000; font-weight: bold;
    border-color: #888 #888 #FFF #888; padding-bottom: 4px; margin-bottom: -2px;
}
.lw-toolbar {
    background: #E0E0E0; border-bottom: 2px solid #888;
    padding: 3px 6px; display: flex; gap: 4px; align-items: center;
}
.lw-btn {
    background: linear-gradient(to bottom, #F8F8F8, #D8D8D8);
    border: 2px solid; border-color: #FFFFFF #808080 #808080 #FFFFFF;
    padding: 2px 8px; font-family: 'Verdana', sans-serif;
    font-size: 10px; cursor: pointer; color: #000;
}
.lw-btn:hover { background: linear-gradient(to bottom, #E8E8FF, #C8C8F8); }
.lw-autoclear { margin-left: auto; font-size: 9px; color: #555; }
.lw-content {
    background: #FFFFFF; border: 2px inset #808080; margin: 4px;
    overflow-x: auto;
}
.lw-section-bar {
    background: linear-gradient(to right, #1a4a7a, #2a6aaa);
    color: #FFFFFF; font-size: 10px; font-weight: bold; padding: 3px 8px;
}
.lw-table {
    width: 100%; border-collapse: collapse;
    font-size: 10px; font-family: 'Verdana', sans-serif;
}
.lw-table th {
    background: linear-gradient(to bottom, #B8C8D8, #A0B8CC);
    color: #000; padding: 3px 6px; text-align: left;
    font-size: 10px; font-weight: bold;
    border-right: 1px solid #8899AA; border-bottom: 2px solid #8899AA;
    white-space: nowrap;
}
.lw-table td {
    padding: 3px 6px; border-bottom: 1px solid #E8E8E8;
    vertical-align: middle; white-space: nowrap;
}
.lw-table tr:nth-child(even) td { background: #F5F8FF; }
.lw-table tr:hover td { background: #DCE8FF; }
.lw-completed-row td { background: #F0FFF0 !important; }
.lw-completed-row:hover td { background: #D8FFD8 !important; }
.lw-filename {
    font-weight: bold; color: #000044; max-width: 200px;
    overflow: hidden; text-overflow: ellipsis;
    font-family: 'Courier New', monospace; font-size: 9px;
}
.lw-progress-wrap { display: inline-flex; align-items: center; gap: 4px; }
.lw-progress-bg {
    background: #E0E0E0; border: 1px solid #9999AA;
    width: 72px; height: 12px; display: inline-block; overflow: hidden;
}
.lw-progress-fill { height: 100%; background: linear-gradient(to bottom, #77BBFF 0%, #4488EE 40%, #3366CC 100%); }
.lw-done-fill { height: 100%; background: linear-gradient(to bottom, #88EE88, #44CC44, #22AA22); }
.lw-status-dl { color: #004488; font-weight: bold; }
.lw-status-connect { color: #886600; }
.lw-status-queued { color: #555; }
.lw-status-sources { color: #AA4400; }
.lw-status-complete { color: #006600; font-weight: bold; }
.lw-statusbar {
    background: linear-gradient(to bottom, #C8C8C8, #B8B8B8);
    border-top: 2px solid #FFFFFF; padding: 2px 8px;
    font-size: 9px; color: #222; display: flex; gap: 12px;
    flex-wrap: wrap; font-family: 'Courier New', monospace;
}
.lw-statusbar-item { white-space: nowrap; }
.lw-shared-section {
    margin-top: 20px; border: 2px solid #000080; background: #F0F8FF;
}
.lw-shared-header {
    background: linear-gradient(to right, #000080, #003399);
    color: #FFFF00; font-weight: bold; font-size: 11px; padding: 5px 10px;
}
.lw-shared-table {
    width: 100%; border-collapse: collapse;
    font-size: 10px; font-family: 'Verdana', sans-serif;
}
.lw-shared-table th {
    background: #CCE0FF; padding: 3px 8px;
    text-align: left; border-bottom: 1px solid #888;
}
.lw-shared-table td {
    padding: 3px 8px; border-bottom: 1px solid #DDE8FF;
    font-family: 'Courier New', monospace; font-size: 9px;
}
.lw-shared-table tr:hover td { background: #EEF4FF; }
.lw-upload-count { color: #FF6600; font-weight: bold; font-size: 10px; }
.lw-disclaimer {
    background: #FFFFF0; border: 2px dashed #CCAA00;
    padding: 8px 12px; margin-top: 14px;
    font-size: 10px; font-family: 'Courier New', monospace; color: #444;
}
</style>

<div class="lw-page-header">
    <div style="font-size:34px;font-family:Impact,'Arial Black',sans-serif;color:#00FF66;text-shadow:0 0 12px #00FF66;letter-spacing:3px;margin-bottom:4px;">🍋 LimeWire</div>
    <div style="font-size:18px;font-family:Impact,'Arial Black',sans-serif;color:#FFFFFF;text-shadow:1px 1px 0 #000;letter-spacing:2px;margin-bottom:8px;">POMS'S DOWNLOAD STATION</div>
    <p>What is Monsieur Poms downloading today?? Updated every midnight!!</p>
    <p style="font-size:10px;color:#AAFFCC;">LimeWire is personally listed as one of Poms's top friends. He is always downloading something.</p>
    <div class="lw-date-badge" id="lw-date-display">Loading...</div>
</div>

<div id="riaa-overlay" onclick="closeRiaa()"></div>
<div id="riaa-popup">
    <div class="riaa-titlebar">
        <span>⚠️ RIAA Legal Notice — Action Required</span>
        <div class="lw-titlebar-btn" onclick="closeRiaa()" style="cursor:pointer;">×</div>
    </div>
    <div class="riaa-body">
        <p style="font-weight:bold;color:#CC0000;">WARNING FROM THE RIAA</p>
        <p>Our systems have detected unauthorized file sharing from IP address:</p>
        <p style="font-family:'Courier New',monospace;font-size:13px;font-weight:bold;color:#000080;background:#EEF;padding:4px;border:1px solid #aaa;">192.168.1.CAT</p>
        <p>Downloading copyrighted material without authorization violates federal law and the exclusive rights of copyright holders.</p>
        <p class="riaa-note">Monsieur Poms has dismissed this warning 1,247 times.<br>He does not care about the RIAA.<br>He cares about chicken.</p>
        <br>
        <button class="riaa-ok-btn" onclick="closeRiaa()">I Understand (Poms doesn't)</button>
    </div>
</div>

<div class="lw-window">
    <div class="lw-titlebar">
        <span>🍋 <span class="lw-logo-text">LimeWire</span> Pro 5.5.16 &nbsp;&mdash;&nbsp; monsieur_poms's Downloads</span>
        <div class="lw-titlebar-btns">
            <div class="lw-titlebar-btn">_</div>
            <div class="lw-titlebar-btn">□</div>
            <div class="lw-titlebar-btn">×</div>
        </div>
    </div>
    <div class="lw-menubar">
        <span>File</span><span>View</span><span>Tools</span><span>Help</span>
    </div>
    <div class="lw-tabs">
        <div class="lw-tab">🔍 Search</div>
        <div class="lw-tab">📚 Library</div>
        <div class="lw-tab">🌐 Connections</div>
        <div class="lw-tab active">⬇️ Downloads</div>
        <div class="lw-tab">📊 Monitor</div>
    </div>
    <div class="lw-toolbar">
        <button class="lw-btn">▶ Resume All</button>
        <button class="lw-btn">⏸ Pause All</button>
        <button class="lw-btn">🔃 Retry</button>
        <button class="lw-btn">🗑 Remove</button>
        <button class="lw-btn">✅ Clear Finished</button>
        <span class="lw-autoclear">Auto-Clear: <strong>ON</strong></span>
    </div>
    <div class="lw-content">
        <div class="lw-section-bar">✅ &nbsp;FINISHED DOWNLOADS — <span id="completed-count">3</span> files</div>
        <table class="lw-table">
            <thead><tr>
                <th style="width:18px;"></th>
                <th>Filename</th>
                <th>Size</th>
                <th>Progress</th>
                <th>Avg Speed</th>
                <th>Status</th>
            </tr></thead>
            <tbody id="completed-tbody"></tbody>
        </table>
        <div class="lw-section-bar" style="margin-top:2px;">⬇️ &nbsp;ACTIVE DOWNLOADS — <span id="active-count">7</span> files</div>
        <table class="lw-table">
            <thead><tr>
                <th style="width:18px;"></th>
                <th>Filename</th>
                <th>Size</th>
                <th>Progress</th>
                <th>Speed</th>
                <th>Sources</th>
                <th>Status</th>
            </tr></thead>
            <tbody id="active-tbody"></tbody>
        </table>
    </div>
    <div class="lw-statusbar" id="lw-statusbar">Loading...</div>
</div>

<div class="lw-shared-section">
    <div class="lw-shared-header">📤 POMS'S SHARED FILES — What Poms is currently uploading to the network</div>
    <table class="lw-shared-table">
        <thead><tr><th></th><th>Filename</th><th>Size</th><th>Uploading To</th><th>Speed</th></tr></thead>
        <tbody>
            <tr><td>🎵</td><td class="lw-filename">MY_OFFICIAL_MEOW_SOUNDS_2024_SAMPLER.zip</td><td>34.2 MB</td><td><span class="lw-upload-count">3 peers</span></td><td>2.1 KB/s</td></tr>
            <tr><td>📄</td><td class="lw-filename">POMS_FAN_CLUB_OFFICIAL_APPLICATION_FORM.pdf</td><td>512 KB</td><td><span class="lw-upload-count">7 peers</span></td><td>5.3 KB/s</td></tr>
            <tr><td>🖼️</td><td class="lw-filename">ORANGE_CAT_SUPERIORITY_WALLPAPER_PACK.zip</td><td>78.4 MB</td><td><span class="lw-upload-count">1 peer</span></td><td>0.9 KB/s</td></tr>
            <tr><td>🎵</td><td class="lw-filename">POMS_BANGER_OFFICIAL_SINGLE_[HIGH_QUALITY].mp3</td><td>8.7 MB</td><td><span class="lw-upload-count">12 peers</span></td><td>11.4 KB/s</td></tr>
            <tr><td>📄</td><td class="lw-filename">COMPLETE_GUIDE_TO_LIVING_WITH_HUMANS.pdf</td><td>5.9 MB</td><td><span class="lw-upload-count">4 peers</span></td><td>3.7 KB/s</td></tr>
            <tr><td>🎵</td><td class="lw-filename">NYAN_CAT_MEGAMIX_BY_POMS_[UNOFFICIAL].mp3</td><td>22.1 MB</td><td><span class="lw-upload-count">2 peers</span></td><td>1.8 KB/s</td></tr>
        </tbody>
    </table>
</div>

<div class="lw-disclaimer">
⚠️ DISCLAIMER: Monsieur Poms does not condone actual copyright infringement. He condones chicken.<br>
This page is a parody. LimeWire shut down in 2010. Poms has not gotten the memo.<br>
The RIAA has Poms on their watchlist. He is not scared. He is napping.
</div>

<script>
function closeRiaa() {
    document.getElementById('riaa-popup').style.display = 'none';
    document.getElementById('riaa-overlay').style.display = 'none';
}

(function() {
    var now = new Date();
    var start = new Date(now.getFullYear(), 0, 0);
    var dayOfYear = Math.floor((now - start) / 86400000);

    var months = ["January","February","March","April","May","June","July","August","September","October","November","December"];
    var days = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
    document.getElementById('lw-date-display').textContent =
        "📅 " + days[now.getDay()] + ", " + months[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear() + " — Daily Download Queue";

    var filePool = [
        // FOOD & TREATS
        ["HOW_TO_OPEN_TREAT_CABINET_TUTORIAL.avi",        "14.3 MB", "video"],
        ["CHICKEN_ASMR_3_HOURS_UNINTERRUPTED.mp3",        "32.1 MB", "audio"],
        ["KIBBLE_BRAND_TIERLIST_2024_OFFICIAL.xls",        "2.1 MB",  "doc"],
        ["SECRET_LOCATION_OF_TREAT_STASH.txt",             "128 KB",  "doc"],
        ["CHICKEN_vs_KIBBLE_GREAT_DEBATE_EXTENDED.wmv",    "89.4 MB", "video"],
        ["DINNER_ALWAYS_LATE_COMPILATION_VOL3.mp3",        "18.9 MB", "audio"],
        ["TRICKS_TO_GET_SECOND_BREAKFAST.pdf",             "1.4 MB",  "doc"],
        ["MAKING_DISAPPOINTED_EYES_FOR_TREATS_HD.mpg",     "67.3 MB", "video"],
        ["BOWL_ALWAYS_LOOKS_EMPTY_TECHNIQUE.txt",          "64 KB",   "doc"],
        ["FOODS_TO_NEVER_EAT_GREEN_BEANS_FINAL.pdf",       "3.7 MB",  "doc"],
        ["ADVANCED_BEGGING_POSITIONS_RANKED.pdf",          "2.8 MB",  "doc"],
        ["CHICKEN_RECIPE_UNLOCK_CODES_ENCRYPTED.zip",      "892 KB",  "archive"],
        ["OFFICIAL_MEAL_DEMANDS_TEMPLATE_V4.doc",          "768 KB",  "doc"],
        ["TREAT_BAG_SOUND_IDENTIFICATION_GUIDE.mp3",       "4.2 MB",  "audio"],
        ["MIDNIGHT_SNACK_ACCESS_PROTOCOLS.pdf",            "1.9 MB",  "doc"],
        ["POMS_FOOD_PHILOSOPHY_EXTENDED.pdf",              "11.4 MB", "doc"],
        // NAPS & SUNBEAMS
        ["OPTIMAL_SUNBEAM_LOCATIONS_MAP_2024.bmp",         "8.2 MB",  "image"],
        ["ADVANCED_NAP_TECHNIQUES_VOL_2.pdf",              "5.1 MB",  "doc"],
        ["HOW_TO_CLAIM_PILLOW_LEGALLY.pdf",                "2.8 MB",  "doc"],
        ["TOP_50_SLEEPING_POSITIONS_RANKED.avi",           "44.7 MB", "video"],
        ["LOAF_MODE_TUTORIAL_FULL_HD.mpg",                 "28.3 MB", "video"],
        ["SUNBEAM_TRACKING_SOFTWARE_V2_BETA.exe",          "1.2 MB",  "app"],
        ["WARM_SPOT_DETECTION_ALGORITHMS.zip",             "3.4 MB",  "archive"],
        ["BEST_NAPPING_SPOTS_PHOTO_ARCHIVE.zip",           "34.7 MB", "archive"],
        ["SUNBEAM_QUALITY_INSPECTION_CHECKLIST.pdf",       "1.7 MB",  "doc"],
        ["PROFESSIONAL_LOAF_FORMATION_GUIDE.pdf",          "3.2 MB",  "doc"],
        ["BLANKET_REAL_ESTATE_LAW_FOR_CATS.pdf",           "8.9 MB",  "doc"],
        ["PRIME_NAPPING_SCHEDULE_OPTIMIZER.xls",           "2.3 MB",  "doc"],
        ["STRATEGIC_SUNBEAM_CLAIMING_V3.pdf",              "4.6 MB",  "doc"],
        // BEHAVIOR & CHAOS
        ["HOW_TO_KNOCK_THINGS_OFF_TABLE.mpg",              "52.6 MB", "video"],
        ["3AM_ZOOMIES_ORIGIN_FULLY_EXPLAINED.pdf",         "4.3 MB",  "doc"],
        ["WALL_STARING_ADVANCED_PRACTITIONERS.txt",        "512 KB",  "doc"],
        ["DRAMATIC_TAIL_MOVEMENTS_101.avi",                "31.8 MB", "video"],
        ["HAIRBALL_STRATEGIC_TIMING_GUIDE.pdf",            "2.2 MB",  "doc"],
        ["PERFECT_BLANKET_KNEADING_TECHNIQUE.mpg",         "19.5 MB", "video"],
        ["SITTING_ON_KEYBOARD_PRODUCTIVITY.pdf",           "1.9 MB",  "doc"],
        ["BATHROOM_SUPERVISION_OFFICIAL_PROTOCOL.pdf",     "3.1 MB",  "doc"],
        ["SILENT_STARE_INTIMIDATION_TECHNIQUES.avi",       "27.4 MB", "video"],
        ["MIDNIGHT_HAUNTING_COMPLETE_GUIDE.pdf",           "3.3 MB",  "doc"],
        ["ALARM_CLOCK_DEFEAT_STRATEGIES_V7.pdf",           "2.6 MB",  "doc"],
        ["3AM_RUN_ORIGIN_DOCUMENTARY_FULL.avi",            "73.2 MB", "video"],
        ["CERTIFIED_PAWS_OF_FURY_TRAINING.pdf",            "5.8 MB",  "doc"],
        ["CERTIFIED_CHAOS_AGENT_DIPLOMA_2024.pdf",         "1.3 MB",  "doc"],
        // SURVEILLANCE & INTELLIGENCE
        ["BIRD_IDENTIFICATION_FIELD_GUIDE_2024.pdf",       "6.7 MB",  "doc"],
        ["BIRDS_OUTSIDE_WINDOW_COMPILATION_8HRS.avi",      "234.7 MB","video"],
        ["WINDOW_SURVEILLANCE_PRO_TIPS.txt",               "384 KB",  "doc"],
        ["SQUIRREL_WATCHING_ADVANCED_STRATEGIES.pdf",      "4.8 MB",  "doc"],
        ["DOG_NEXT_DOOR_DOSSIER_CLASSIFIED.pdf",           "3.9 MB",  "doc"],
        ["SUSPICIOUS_HOUSEHOLD_SOUNDS_DATABASE.zip",       "15.3 MB", "archive"],
        ["HOUSEHOLD_THREAT_ASSESSMENT_2024.xls",           "2.1 MB",  "doc"],
        ["COVERT_OPS_UNDER_BED_MANUAL.pdf",                "4.4 MB",  "doc"],
        // LEGAL & OFFICIAL
        ["FORMAL_COMPLAINT_TEMPLATES_MASTER.doc",          "768 KB",  "doc"],
        ["LEGAL_CLAIM_ON_SUNBEAM_PATENT.pdf",              "2.4 MB",  "doc"],
        ["ROYAL_DECREE_TEMPLATES_OFFICIAL_V5.doc",         "1.1 MB",  "doc"],
        ["CHONK_IS_A_MYTH_SCIENTIFIC_PROOF.pdf",           "1.6 MB",  "doc"],
        ["I_AM_TALL_NOT_FAT_EVIDENCE_PACK.pdf",            "3.8 MB",  "doc"],
        ["PRESS_CONFERENCE_SPEECH_TEMPLATES.doc",          "1.8 MB",  "doc"],
        ["CERTIFIED_GENIUS_CERTIFICATE_BLANK.pdf",         "512 KB",  "doc"],
        ["VET_ESCAPE_ROUTES_FULLY_UPDATED.pdf",            "2.9 MB",  "doc"],
        // ENTERTAINMENT & MISC
        ["NYAN_CAT_EXTENDED_10_HOURS_HQ.mp3",              "41.2 MB", "audio"],
        ["POMS_GREATEST_HITS_[NOT_A_VIRUS].mp3",           "7.8 MB",  "audio"],
        ["CAT_DOCUMENTARIES_COMPLETE_PACK.zip",            "892.3 MB","archive"],
        ["COMPLETE_DICTIONARY_OF_MEOWS.pdf",               "9.3 MB",  "doc"],
        ["HUMANS_DO_NOT_UNDERSTAND_MANIFESTO.txt",         "192 KB",  "doc"],
        ["ORANGE_CAT_SUPERIORITY_PROOF.pdf",               "5.2 MB",  "doc"],
        ["HOW_TO_TELEPORT_THROUGH_CLOSED_DOORS.avi",       "22.8 MB", "video"],
        ["WATER_BOWL_vs_TAP_TASTE_TEST_RESULTS.avi",       "29.7 MB", "video"],
        ["COMPLETE_GUIDE_TO_HUMAN_TRAINING.pdf",           "11.4 MB", "doc"],
        ["POMS_DRINK_BRAND_OFFICIAL_ANALYSIS.xls",         "2.7 MB",  "doc"],
        ["TACTICAL_USE_OF_MEOW_IN_NEGOTIATIONS.pdf",       "3.9 MB",  "doc"],
        ["CERTIFIED_TOP_8_FRIEND_APPLICATION.doc",         "1.3 MB",  "doc"]
    ];

    var completedPool = [
        ["STRATEGIC_STILLNESS_QUICK_GUIDE.txt",            "96 KB",  "doc"],
        ["HOW_TO_IGNORE_HUMANS_EFFECTIVELY.txt",           "256 KB", "doc"],
        ["WINDOW_SURVEILLANCE_CHEAT_SHEET.txt",            "384 KB", "doc"],
        ["THE_BOWL_IS_NEVER_FULL_PHILOSOPHY.txt",          "128 KB", "doc"],
        ["ALARM_CLOCK_DEFEAT_FINAL_DRAFT.pdf",             "2.6 MB", "doc"],
        ["FOODS_TO_NEVER_EAT_GREEN_BEANS.pdf",             "3.7 MB", "doc"],
        ["CHONK_IS_A_MYTH_PROOF.pdf",                      "1.6 MB", "doc"],
        ["KEYBOARD_SITTING_FORM_V2.doc",                   "896 KB", "doc"],
        ["LOAF_GUIDE_CERTIFIED_COPY.pdf",                  "3.2 MB", "doc"],
        ["NYAN_CAT_RINGTONE_PACK_2024.zip",                "12.4 MB","archive"],
        ["CERTIFIED_GENIUS_CERTIFICATE.pdf",               "512 KB", "doc"],
        ["PRESS_CONFERENCE_SPEECH_V1_FINAL.doc",           "768 KB", "doc"],
        ["PERFECT_SUNBEAM_SPOT_ANNUAL_MAP.bmp",            "4.1 MB", "image"],
        ["DISAPPOINTED_EYES_QUICK_REFERENCE.pdf",          "892 KB", "doc"],
        ["CHICKEN_RECIPE_BASIC_VERSION.txt",               "64 KB",  "doc"],
        ["TAIL_FLICK_MEANINGS_GUIDE.txt",                  "192 KB", "doc"],
        ["HOW_TO_FALL_ASLEEP_INSTANTLY.pdf",               "1.4 MB", "doc"],
        ["BLANKET_KNEADING_MASTERCLASS_NOTES.txt",         "384 KB", "doc"]
    ];

    var typeIcons = { audio:"🎵", video:"🎬", doc:"📄", image:"🖼️", archive:"📦", app:"⚙️" };

    function dhash(a, b) { return Math.abs((a * 1009 + b * 127 + a * b * 31) | 0); }

    function getProgress(i) { return (dhash(dayOfYear, i) % 85) + 8; }

    function getSpeed(progress, i) {
        var h = dhash(dayOfYear, i + 100);
        if (progress < 12) return ((h % 15 + 5) / 10).toFixed(1) + " KB/s";
        if (progress < 50) return ((h % 50 + 30) / 10).toFixed(1) + " KB/s";
        return ((h % 70 + 60) / 10).toFixed(1) + " KB/s";
    }

    function getSources(i) { return (dhash(dayOfYear, i + 50) % 11) + 1; }

    function getStatus(progress, i) {
        var special = dhash(dayOfYear + 1000, i) % 14;
        if (special === 0) return ["More Sources...", "lw-status-sources", 0];
        if (progress < 10) return ["Connecting...", "lw-status-connect", 1];
        return ["Downloading", "lw-status-dl", getSources(i)];
    }

    function progressBar(pct, done) {
        var cls = done ? "lw-done-fill" : "lw-progress-fill";
        var p = done ? 100 : pct;
        return '<div class="lw-progress-wrap">' +
               '<div class="lw-progress-bg"><div class="' + cls + '" style="width:' + p + '%;"></div></div>' +
               '&nbsp;<span style="font-size:10px;">' + p + '%</span></div>';
    }

    // Pick 7 active files
    var s = dayOfYear % filePool.length;
    var activeFiles = [];
    for (var i = 0; i < 7; i++) activeFiles.push(filePool[(s + i) % filePool.length]);

    // Pick 3 completed files
    var cs = (dayOfYear * 5) % completedPool.length;
    var completedFiles = [];
    for (var i = 0; i < 3; i++) completedFiles.push(completedPool[(cs + i) % completedPool.length]);

    // Render completed
    var ch = '';
    for (var i = 0; i < completedFiles.length; i++) {
        var f = completedFiles[i];
        ch += '<tr class="lw-completed-row">' +
            '<td>' + (typeIcons[f[2]] || "📄") + '</td>' +
            '<td class="lw-filename" title="' + f[0] + '">' + f[0] + '</td>' +
            '<td>' + f[1] + '</td>' +
            '<td>' + progressBar(100, true) + '</td>' +
            '<td style="color:#888;">—</td>' +
            '<td><span class="lw-status-complete">✅ Complete</span></td>' +
            '</tr>';
    }
    document.getElementById('completed-tbody').innerHTML = ch;

    // Render active
    var ah = '';
    var totalSpeed = 0;
    for (var i = 0; i < activeFiles.length; i++) {
        var f = activeFiles[i];
        var progress = getProgress(i);
        var speedStr = getSpeed(progress, i);
        totalSpeed += parseFloat(speedStr);
        var st = getStatus(progress, i);
        ah += '<tr>' +
            '<td>' + (typeIcons[f[2]] || "📄") + '</td>' +
            '<td class="lw-filename" title="' + f[0] + '">' + f[0] + '</td>' +
            '<td>' + f[1] + '</td>' +
            '<td>' + progressBar(progress, false) + '</td>' +
            '<td>' + speedStr + '</td>' +
            '<td>' + (st[2] > 0 ? st[2] : '—') + '</td>' +
            '<td><span class="' + st[1] + '">' + st[0] + '</span></td>' +
            '</tr>';
    }
    document.getElementById('active-tbody').innerHTML = ah;

    // Status bar
    var hosts = (dhash(dayOfYear, 999) % 4000) + 1000;
    var upSpeed = ((dhash(dayOfYear, 998) % 100) / 10 + 2.0).toFixed(1);
    document.getElementById('lw-statusbar').innerHTML =
        '<span class="lw-statusbar-item">🟢 Connected: <strong>' + hosts + '</strong> hosts</span>' +
        '<span class="lw-statusbar-item">⬆️ Uploads: <strong>6</strong> &nbsp;' + upSpeed + ' KB/s</span>' +
        '<span class="lw-statusbar-item">⬇️ Downloads: <strong>7</strong> &nbsp;' + totalSpeed.toFixed(1) + ' KB/s</span>' +
        '<span class="lw-statusbar-item">📁 Sharing: <strong>1,337</strong> files</span>' +
        '<span class="lw-statusbar-item" style="color:#AA0000;">⚠️ Firewall: <strong>DISABLED</strong> (Poms removed it)</span>';
})();
</script>
