---
title: "Poms Cable TV Guide"
---

<style>
.tvg-wrap {
    border: 1px solid #999;
    overflow: hidden;
    background: #EAEAEA;
    margin-bottom: 20px;
}

.tvg-masthead {
    background: linear-gradient(to bottom, #003399 0%, #001166 100%);
    color: #FFD700;
    text-align: center;
    padding: 16px 10px 10px;
    border-bottom: 4px solid #CC0000;
}

.tvg-masthead-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 30px;
    letter-spacing: 6px;
    text-shadow: 2px 2px 0 #000;
    margin: 0;
}

.tvg-masthead-sub {
    font-size: 10px;
    letter-spacing: 3px;
    color: #AACCFF;
    margin-top: 4px;
    text-transform: uppercase;
}

.tvg-datebar {
    background: #CC0000;
    color: #FFFF00;
    text-align: center;
    padding: 4px 10px;
    font-family: 'Courier New', monospace;
    font-size: 13px;
    font-weight: bold;
    letter-spacing: 2px;
    border-bottom: 2px solid #880000;
}

.tvg-picks-box {
    background: #FFF9E0;
    border-bottom: 2px solid #CCC;
    padding: 10px 14px;
}

.tvg-picks-title {
    font-family: 'Impact', sans-serif;
    font-size: 15px;
    color: #CC0000;
    letter-spacing: 2px;
    border-bottom: 1px solid #CCC;
    margin-bottom: 8px;
    padding-bottom: 3px;
}

.tvg-picks-grid {
    display: flex;
    gap: 10px;
}

.tvg-pick-item {
    flex: 1;
    background: #FFF;
    border: 1px solid #DDD;
    border-left: 4px solid #003399;
    padding: 6px 8px;
    font-size: 10px;
}

.tvg-pick-ch {
    font-size: 9px;
    color: #888;
    text-transform: uppercase;
    letter-spacing: 1px;
}

.tvg-pick-show {
    font-weight: bold;
    color: #003399;
    font-size: 11px;
    margin: 2px 0;
}

.tvg-pick-desc { color: #444; line-height: 1.4; }

/* ON NOW */
.tvg-onnow-box {
    background: #1A1A2E;
    padding: 10px 14px;
    border-bottom: 3px solid #CC0000;
}

.tvg-onnow-title {
    color: #FF3333;
    font-family: 'Impact', sans-serif;
    font-size: 14px;
    letter-spacing: 3px;
    margin-bottom: 8px;
    display: flex;
    align-items: center;
    gap: 8px;
}

.tvg-onnow-pulse {
    width: 10px;
    height: 10px;
    background: #FF3333;
    border-radius: 50%;
    animation: tvgPulse 1s ease-in-out infinite;
    flex-shrink: 0;
}

@keyframes tvgPulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.3; transform: scale(0.7); }
}

.tvg-onnow-row {
    display: flex;
    align-items: flex-start;
    gap: 8px;
    margin-bottom: 5px;
    background: rgba(255,255,255,0.05);
    padding: 4px 6px;
    border-radius: 2px;
}

.tvg-onnow-chbadge {
    background: #003399;
    color: #FFD700;
    font-family: 'Courier New', monospace;
    font-weight: bold;
    font-size: 10px;
    padding: 2px 5px;
    flex-shrink: 0;
    min-width: 30px;
    text-align: center;
}

.tvg-onnow-info { flex: 1; min-width: 0; }

.tvg-onnow-show {
    color: #FFFF99;
    font-weight: bold;
    font-size: 11px;
}

.tvg-onnow-showdesc {
    color: #AAAACC;
    font-size: 9px;
    margin-top: 1px;
    line-height: 1.3;
}

/* Schedule Table */
.tvg-schedule-wrap {
    padding: 12px 12px 4px;
    background: #F0F0F0;
}

.tvg-sched-label {
    font-family: 'Impact', sans-serif;
    font-size: 13px;
    color: #003399;
    letter-spacing: 2px;
    margin-bottom: 6px;
    text-transform: uppercase;
}

.tvg-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 10px;
    background: #FFF;
}

.tvg-table th {
    background: #003366;
    color: #FFD700;
    padding: 6px 4px;
    text-align: center;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 12px;
    letter-spacing: 1px;
    border: 1px solid #001133;
}

.tvg-table th.tvg-current-col {
    background: #880000;
    color: #FFFF00;
}

.tvg-ch-cell {
    text-align: center;
    padding: 6px 4px;
    border: 1px solid #CCC;
    vertical-align: middle;
    width: 65px;
}

.tvg-ch-num {
    display: inline-block;
    font-family: 'Courier New', monospace;
    font-weight: bold;
    font-size: 13px;
    color: #FFF;
    padding: 2px 5px;
    margin-bottom: 2px;
}

.tvg-ch-name {
    font-weight: bold;
    font-size: 9px;
    line-height: 1.2;
    color: #000;
}

.tvg-show-cell {
    padding: 5px 6px;
    border: 1px solid #DDD;
    vertical-align: top;
    background: #FFF;
    min-width: 120px;
}

.tvg-show-cell.tvg-current-col {
    background: #FFFCE0;
    border-left: 3px solid #CC0000;
    border-right: 3px solid #CC0000;
}

.tvg-show-time {
    font-size: 9px;
    color: #888;
    margin-bottom: 2px;
    font-family: 'Courier New', monospace;
}

.tvg-show-title {
    font-weight: bold;
    color: #003399;
    font-size: 10px;
    line-height: 1.3;
    margin-bottom: 2px;
}

.tvg-show-desc {
    font-size: 9px;
    color: #444;
    line-height: 1.35;
}

.tvg-show-meta {
    margin-top: 3px;
    display: flex;
    align-items: center;
    gap: 4px;
    flex-wrap: wrap;
}

.tvg-badge {
    font-size: 8px;
    font-weight: bold;
    padding: 1px 4px;
    border-radius: 2px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    flex-shrink: 0;
}

.tvg-badge-live     { background: #CC0000; color: #FFF; }
.tvg-badge-new      { background: #006600; color: #FFF; }
.tvg-badge-breaking { background: #FF6600; color: #FFF; }
.tvg-badge-rerun    { background: #666666; color: #FFF; }
.tvg-badge-special  { background: #6600CC; color: #FFF; }

.tvg-stars { color: #CC9900; font-size: 9px; }

.tvg-footer {
    background: #003366;
    color: #AAAACC;
    font-size: 9px;
    padding: 6px 14px;
    text-align: center;
    letter-spacing: 1px;
}

.tvg-disclaimer {
    background: #111;
    color: #555;
    font-size: 9px;
    padding: 5px 14px;
    text-align: center;
    font-family: 'Courier New', monospace;
}
</style>

<div style="border: 1px solid #CCC; overflow: hidden; margin-bottom: 20px;">

<div style="background: linear-gradient(to right, #001166, #003399, #001166); color: #FFD700; text-align: center; padding: 18px 10px; border-bottom: 4px solid #CC0000;">
    <div style="font-family: 'Impact','Arial Black',sans-serif; font-size: 32px; letter-spacing: 7px; text-shadow: 3px 3px 0 #000; margin: 0;">
        📺 POMS CABLE GUIDE
    </div>
    <div style="font-size: 10px; color: #AACCFF; margin-top: 6px; letter-spacing: 3px; text-transform: uppercase;">
        Daily Programming Schedule &nbsp;|&nbsp; All Channels &nbsp;|&nbsp; Updated at Midnight
    </div>
    <div style="margin-top: 8px; font-size: 14px; letter-spacing: 5px; color: #5577BB;">✦ ✦ ✦ ✦ ✦</div>
</div>

<div style="background: #CC0000; color: #FFFF00; text-align: center; padding: 5px 10px; font-family: 'Courier New', monospace; font-size: 13px; font-weight: bold; letter-spacing: 2px; border-bottom: 2px solid #880000;">
    <span id="tvg-dateline">Loading date...</span>
</div>

<!-- ON NOW -->
<div style="background: #0D0D2B; padding: 12px 14px; border-bottom: 3px solid #CC0000;">
    <div style="color: #FF4444; font-family: 'Impact', sans-serif; font-size: 15px; letter-spacing: 3px; margin-bottom: 10px; display: flex; align-items: center; gap: 8px;">
        <div style="width: 10px; height: 10px; background: #FF4444; border-radius: 50%; animation: tvgPulse 1s ease-in-out infinite; flex-shrink: 0;"></div>
        ON NOW &nbsp;<span style="font-size:11px; color:#AAAACC; letter-spacing:1px; font-family: Verdana, sans-serif; font-style: italic;">— currently airing on all channels</span>
    </div>
    <div id="tvg-onnow-container" style="display: grid; grid-template-columns: 1fr 1fr; gap: 6px;">
        <div style="color: #666; font-size: 10px; font-style: italic;">Loading live schedule...</div>
    </div>
</div>

<!-- EDITOR'S PICKS -->
<div style="background: #FFF9E0; border-bottom: 2px solid #CCC; padding: 10px 14px;">
    <div style="font-family: 'Impact', sans-serif; font-size: 14px; color: #CC0000; letter-spacing: 2px; border-bottom: 1px solid #CCC; margin-bottom: 8px; padding-bottom: 4px;">
        ⭐ TONIGHT'S PICKS — EDITOR'S CHOICE
    </div>
    <div id="tvg-picks-grid" style="display: flex; gap: 8px; flex-wrap: wrap;">
        <div style="color: #666; font-size: 10px; font-style: italic;">Loading picks...</div>
    </div>
</div>

<!-- FULL SCHEDULE -->
<div style="padding: 12px 12px 4px; background: #EEEEEE;">
    <div style="font-family: 'Impact', sans-serif; font-size: 13px; color: #003399; letter-spacing: 2px; margin-bottom: 8px;">
        TODAY'S COMPLETE SCHEDULE
    </div>
    <div style="overflow-x: auto;">
        <table class="tvg-table" id="tvg-schedule-table">
            <thead>
                <tr>
                    <th style="width: 70px;">CHANNEL</th>
                    <th id="tvg-th-morning">☀️ MORNING<br><span style="font-size:9px; font-weight:normal; letter-spacing:0;">6 AM – 12 PM</span></th>
                    <th id="tvg-th-afternoon">🌤️ AFTERNOON<br><span style="font-size:9px; font-weight:normal; letter-spacing:0;">12 PM – 6 PM</span></th>
                    <th id="tvg-th-evening">🌙 EVENING<br><span style="font-size:9px; font-weight:normal; letter-spacing:0;">6 PM – 10 PM</span></th>
                    <th id="tvg-th-latenight">🌑 LATE NIGHT<br><span style="font-size:9px; font-weight:normal; letter-spacing:0;">10 PM – 6 AM</span></th>
                </tr>
            </thead>
            <tbody id="tvg-schedule-body">
                <tr><td colspan="5" style="text-align:center; padding: 20px; color: #888; font-style:italic;">Loading schedule...</td></tr>
            </tbody>
        </table>
    </div>
</div>

<div style="background: #003366; color: #AAAACC; font-size: 9px; padding: 7px 14px; text-align: center; letter-spacing: 1px; border-top: 2px solid #001133;">
    POMS CABLE &nbsp;|&nbsp; 6 CHANNELS &nbsp;|&nbsp; PROGRAMMING SUBJECT TO CHANGE WITHOUT NOTICE &nbsp;|&nbsp; CHICKEN CONTENT PROTECTED BY LAW
</div>
<div style="background: #111; color: #555; font-size: 9px; padding: 5px 14px; text-align: center; font-family: 'Courier New', monospace;">
    Schedule generated fresh daily at midnight. All shows verified by Poms. Green beans are permanently banned from this network. Complaints about programming may be filed via the Complaint Department.
</div>

</div>

<script>
(function () {

// ── Seeded RNG ──────────────────────────────────────────────────────────────
function seededRand(s) {
    var x = Math.sin(s * 127.1 + 311.7) * 43758.5453123;
    return x - Math.floor(x);
}
function pick(arr, s) { return arr[Math.floor(seededRand(s) * arr.length)]; }

// ── Date setup ───────────────────────────────────────────────────────────────
var now  = new Date();
var doy  = Math.floor((now - new Date(now.getFullYear(), 0, 0)) / 86400000);
var seed = now.getFullYear() * 1000 + doy;
var hour = now.getHours();

var dayNames   = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
var monthNames = ["January","February","March","April","May","June","July","August","September","October","November","December"];

document.getElementById('tvg-dateline').textContent =
    dayNames[now.getDay()] + ', ' + monthNames[now.getMonth()] + ' ' + now.getDate() + ', ' + now.getFullYear();

// ── Current slot ─────────────────────────────────────────────────────────────
// morning: 6–11, afternoon: 12–17, evening: 18–21, latenight: 22-23 + 0-5
var currentSlot = (hour >= 6 && hour < 12) ? 'morning'
                : (hour >= 12 && hour < 18) ? 'afternoon'
                : (hour >= 18 && hour < 22) ? 'evening'
                : 'latenight';

var slotDisplayTime = {
    morning:   '6:00 AM',
    afternoon: '12:00 PM',
    evening:   '6:00 PM',
    latenight: '10:00 PM'
};

// ── Channel data ──────────────────────────────────────────────────────────────
var channels = [
    {
        num: '2',
        name: 'MEOW-TV',
        tagline: 'For the Discerning Cat',
        color: '#003399',
        shows: {
            morning: [
                {time:'7:00 AM', title:'Good Morning Kibble!', desc:'Live bowl coverage and the day\'s top stories. Today\'s headline: Fill Level Dispute, Day 847.', badge:'live', stars:4},
                {time:'8:00 AM', title:'The Poms Report', desc:'Daily press conference, live from the food area. Opening statement: The Chicken Situation.', badge:'live', stars:5},
                {time:'6:30 AM', title:'Sunrise Vocalization Hour', desc:'Three hours of recorded demand meows. Therapeutic. For the cat. Not for you.', badge:'', stars:3},
                {time:'9:00 AM', title:'Morning Window Watch', desc:'Extended bird surveillance from the primary observation post. Today\'s count: disputed.', badge:'', stars:3},
                {time:'8:30 AM', title:'Grooming with Poms', desc:'Advanced technique masterclass. Season 3, Episode 12: The Face Wash. Very detailed.', badge:'new', stars:3},
                {time:'7:30 AM', title:'Breakfast News at Seven', desc:'Today\'s bowl situation, warm patch locations, and human movement pattern analysis.', badge:'', stars:4}
            ],
            afternoon: [
                {time:'2:00 PM', title:'Talk Paws with Poms', desc:'Today\'s topic: The Green Bean Agenda (rejected unanimously). No guests. Only complaints.', badge:'', stars:3},
                {time:'1:00 PM', title:'The Nap Block', desc:'Uninterrupted 4-hour nap coverage. Narrated in hushed tones. Please do not call.', badge:'', stars:4},
                {time:'3:00 PM', title:'Judge Whiskers', desc:'Today\'s case: Human ate the last piece of chicken. Verdict: Guilty. Sentence: Treat.', badge:'new', stars:3},
                {time:'2:30 PM', title:'Sunbeam Migration Live', desc:'Real-time tracking of the afternoon beam shift from living room to kitchen window.', badge:'live', stars:4},
                {time:'4:00 PM', title:'World of Boxes', desc:'Travel show. Today\'s destination: The New Amazon Box (Large). Occupation: immediate.', badge:'', stars:3},
                {time:'1:30 PM', title:'Treat Watch Live', desc:'Hour 6 of stationed surveillance near the treat bag. Expert commentary by Poms.', badge:'live', stars:4}
            ],
            evening: [
                {time:'6:00 PM', title:'The Evening Bowl Report', desc:'TONIGHT: Did they remember dinner? Live updates. Crisis response team on standby.', badge:'live', stars:5},
                {time:'7:00 PM', title:'Who Wants to Win Chicken?', desc:'Game show. Poms always wins. Prize: chicken. Consolation prize: disappointment.', badge:'', stars:4},
                {time:'8:00 PM', title:'The Bachelorcat', desc:'TONIGHT: Two treat flavors compete for Poms\' approval. Rose ceremony at 9 PM.', badge:'new', stars:3},
                {time:'9:00 PM', title:'CSI: Cardboard Box', desc:'TONIGHT: Someone touched the box. Poms leads the investigation. Suspect: the vacuum.', badge:'', stars:4},
                {time:'7:30 PM', title:'Dancing with the Cats', desc:'Judges award points exclusively for napping form and treat acquisition technique.', badge:'', stars:3},
                {time:'8:30 PM', title:'The Great Cat Bake Off', desc:'Contestants must produce edible chicken. Standard: Poms\'s standards. Historical pass rate: 0%.', badge:'', stars:3}
            ],
            latenight: [
                {time:'10:00 PM', title:'Zoomie Coverage', desc:'BREAKING: The 10 PM zoomie event. Full uncut footage. Duration: unknown. Reason: unknown.', badge:'live', stars:5},
                {time:'11:00 PM', title:'The Late Show with Poms', desc:'Monologue about today\'s grievances. Musical guest: also Poms. Performing: meowing.', badge:'', stars:4},
                {time:'12:00 AM', title:'Late Night Negotiations', desc:'Rerun of today\'s treat bag summit. Spoiler: Poms wins. Runtime: 48 minutes.', badge:'rerun', stars:3},
                {time:'3:00 AM', title:'3 AM Emergency Coverage', desc:'LIVE: Bowl crisis. Coverage continues until resolution. Estimated time: 3:02 AM.', badge:'live', stars:4},
                {time:'2:00 AM', title:'Overnight Wall Staring', desc:'Poms examines a specific point on the wall. 4-hour block. Classified. Educational.', badge:'', stars:3},
                {time:'1:00 AM', title:'Insomniac Paws', desc:'Call-in show for cats who can\'t sleep. Nobody calls. Poms is fine with this.', badge:'', stars:2}
            ]
        }
    },
    {
        num: '5',
        name: 'BIRB-TV',
        tagline: 'All Birds. All Day.',
        color: '#006633',
        shows: {
            morning: [
                {time:'6:00 AM', title:'LIVE: Morning Feeder Report', desc:'Today\'s birds at the feeder. Count: updating. Status: deeply concerning.', badge:'live', stars:5},
                {time:'7:30 AM', title:'Sparrow Special', desc:'Extended 3-hour block on sparrow activity. Poms is extremely invested. Commentary nonstop.', badge:'', stars:4},
                {time:'8:00 AM', title:'The Bird Brief', desc:'Overnight bird event summary. A lot happened. Some of it was frankly upsetting.', badge:'', stars:3},
                {time:'9:00 AM', title:'Field Guide: Backyard Edition', desc:'Poms\' annotated bird ID guide. Primary section: \'Birds Currently at Window B\'.', badge:'', stars:4},
                {time:'6:30 AM', title:'Breakfast Birds', desc:'What\'s at the feeder while YOU eat breakfast? More important than your breakfast.', badge:'', stars:4},
                {time:'8:30 AM', title:'Bird Behavior Studies', desc:'Why do they just sit there? Why won\'t they come closer? 4-hour investigation.', badge:'', stars:3}
            ],
            afternoon: [
                {time:'2:00 PM', title:'Window B Live', desc:'Uncut, unedited surveillance footage from the primary bird observation post. LIVE.', badge:'live', stars:5},
                {time:'1:00 PM', title:'Feeder Cam Classics', desc:'Greatest feeder moments, 2022 to present. Contains emotional content. Viewer discretion.', badge:'rerun', stars:4},
                {time:'3:00 PM', title:'The Great Sparrow Count', desc:'Annual census. Today\'s number: disputed. Poms insists it is more than yesterday.', badge:'', stars:4},
                {time:'2:30 PM', title:'Afternoon Bird Summit', desc:'Peak bird activity: 3 PM. Coverage begins 90 minutes early. Preparedness: mandatory.', badge:'', stars:4},
                {time:'4:00 PM', title:'New Bird Alert', desc:'BREAKING: Unknown species spotted at the feeder. Full response underway. Classified.', badge:'breaking', stars:5},
                {time:'1:30 PM', title:'The Chirp Files: Decoded', desc:'What are the birds saying? 3-part investigation. Part 1: Possibly about food.', badge:'', stars:3}
            ],
            evening: [
                {time:'6:30 PM', title:'Evening Bird News', desc:'End-of-day feeder report. Final count. Analysis. Assessment: still not enough.', badge:'', stars:4},
                {time:'7:00 PM', title:'Bird Watch: After Dark', desc:'Do birds have feelings? An extended documentary. Poms has opinions. Many opinions.', badge:'', stars:3},
                {time:'8:00 PM', title:'Prime Time: The Cardinal', desc:'SPECIAL: A 2-hour documentary about that one very red bird. Poms: extremely interested.', badge:'special', stars:4},
                {time:'9:00 PM', title:'Bird Confidential', desc:'What are they really chirping about? 90-minute investigation. Conclusions: classified.', badge:'', stars:3},
                {time:'7:30 PM', title:'Best Bird Moments of the Week', desc:'Top feeder cam clips. Some contain three sparrows at once. Historic.', badge:'', stars:4},
                {time:'8:30 PM', title:'The Cardinal Files', desc:'Tuesday: A large red bird appeared. Then it left. Why? Case status: open.', badge:'', stars:4}
            ],
            latenight: [
                {time:'11:00 PM', title:'Overnight Feeder Watch', desc:'Monitoring the feeder in case a nocturnal bird appears. Vigilant. Committed. Awake.', badge:'live', stars:4},
                {time:'12:00 AM', title:'Bird Dreams', desc:'Animated feature depicting what Poms dreams about. Mostly birds. Some chicken.', badge:'', stars:4},
                {time:'2:00 AM', title:'Classic Chirp Archives', desc:'Vintage bird calls from the 2019-2023 collection. Very calming. Poms: disagrees.', badge:'', stars:3},
                {time:'3:00 AM', title:'Pre-Dawn Bird Alert', desc:'First birds of morning: ETA 5:47 AM. Poms is already at Window B. This is normal.', badge:'live', stars:4},
                {time:'1:00 AM', title:'The Night Feeder', desc:'Low-light feeder cam. Update: no birds. Poms is watching anyway. Standards matter.', badge:'live', stars:3},
                {time:'10:30 PM', title:'Planning Tomorrow\'s Surveillance', desc:'Strategic session: Window B rotation, secondary sightlines, contingency perches.', badge:'', stars:3}
            ]
        }
    },
    {
        num: '8',
        name: 'PPN',
        tagline: 'Poms Personal Network',
        color: '#660099',
        shows: {
            morning: [
                {time:'8:00 AM', title:'The Morning Statement', desc:'Opening remarks for the day. Topic: still hungry. Continuation of yesterday\'s topic.', badge:'', stars:4},
                {time:'7:00 AM', title:'My Sunbeam, My Rules', desc:'Documenting this morning\'s beam claim. Includes legal commentary and territorial decree.', badge:'', stars:3},
                {time:'9:30 AM', title:'The Cardboard Chronicles', desc:'S4 E2: The Arrival of the New Amazon Box. Reaction: immediate occupation. Runtime: 47 min.', badge:'new', stars:4},
                {time:'6:00 AM', title:'Poms: Uncensored', desc:'Unedited footage of the 6 AM breakfast demand. Runtime: 37 minutes. Resolved at 6:38 AM.', badge:'', stars:4},
                {time:'10:00 AM', title:'A Day in My Life', desc:'Documentary. Today: the usual. But make it art. Director\'s cut available now.', badge:'', stars:3},
                {time:'8:30 AM', title:'I Was Not Chubby: A Memoir', desc:'Poms reads from his memoir. Chapter 7: The Vet\'s Incorrect Opinion on Body Composition.', badge:'', stars:4}
            ],
            afternoon: [
                {time:'2:00 PM', title:'The Complaint Files', desc:'Poms reviews today\'s formal filings. Current severity range: Moderate to Catastrophic.', badge:'', stars:4},
                {time:'1:00 PM', title:'Poms Reviews Things', desc:'Today: the new water fountain. Rating: 2/10. Bowl water superior. Complaint: filed.', badge:'new', stars:3},
                {time:'3:00 PM', title:'Strategic Napping with Poms', desc:'Lesson 4: Occupying the single most inconvenient position in any given room.', badge:'', stars:4},
                {time:'4:00 PM', title:'My Life: The Highlight Reel', desc:'Best moments from 12-4 PM. Featuring: excellent nap, one bug identified (released).', badge:'', stars:3},
                {time:'2:30 PM', title:'Poms Addresses the Nation', desc:'Public statement regarding the treat situation. Duration: however long it requires.', badge:'live', stars:4},
                {time:'1:30 PM', title:'Inside Cardboard Box HQ', desc:'Exclusive tour of headquarters. Note: camera crew not permitted inside. Tour: exterior.', badge:'', stars:3}
            ],
            evening: [
                {time:'7:00 PM', title:'The Evening Press Conference', desc:'Today\'s issues: dinner timing, treat quality, green bean situation (rejected with prejudice).', badge:'live', stars:5},
                {time:'8:00 PM', title:'Poms: Behind the Scenes', desc:'Rare footage of Poms when not performing. Findings: same as when performing.', badge:'', stars:3},
                {time:'9:00 PM', title:'My Terms: A Documentary', desc:'2-hour examination of why everything must be on Poms\' terms. Compelling. Binding.', badge:'', stars:4},
                {time:'6:30 PM', title:'Dinner Watch Live', desc:'Poms supervises dinner preparation from floor level. Position: directly underfoot.', badge:'live', stars:5},
                {time:'8:30 PM', title:'Poms v. Everyone: The Legal Series', desc:'Tonight: The Green Bean Lawsuit. Plaintiff: Poms. Defendant: The Refrigerator.', badge:'new', stars:4},
                {time:'7:30 PM', title:'I Am Tall: A Film by Poms', desc:'Definitive documentary addressing the height storage controversy. 90 minutes. Conclusive.', badge:'', stars:5}
            ],
            latenight: [
                {time:'11:00 PM', title:'The Midnight Reflection', desc:'Poms reflects on the day. Assessment: adequate. Could have had more chicken.', badge:'', stars:3},
                {time:'10:30 PM', title:'Zoomies: The Live Event', desc:'TONIGHT\'S 10:30 PM ZOOMIE. Unscripted. Unexplained. Required viewing.', badge:'live', stars:5},
                {time:'12:00 AM', title:'The 12 AM Address', desc:'Poms\' late-night remarks. Topic: bowl fill levels. Tone: concerned but composed.', badge:'', stars:4},
                {time:'2:00 AM', title:'Night Vision Chronicles', desc:'Poms conducts apartment patrol. Security assessment: thorough. Professional. Meow.', badge:'', stars:3},
                {time:'3:00 AM', title:'3 AM: Crisis Coverage', desc:'LIVE: Emergency bowl situation. Human: asleep. Poms: undeterred. Resolution: 3:04 AM.', badge:'live', stars:5},
                {time:'1:00 AM', title:'Overnight Planning Session', desc:'Tomorrow\'s agenda finalized. Priorities: eat, sun, eat, judge, complain, eat.', badge:'', stars:3}
            ]
        }
    },
    {
        num: '13',
        name: 'CHICKEN CH.',
        tagline: 'Chicken 24/7. No Exceptions.',
        color: '#884400',
        shows: {
            morning: [
                {time:'6:00 AM', title:'Chicken This Morning', desc:'Today\'s chicken news. Breaking: chicken is still good. This has been the report every day.', badge:'live', stars:4},
                {time:'8:00 AM', title:'The Daily Chicken', desc:'Hourly roundup of global chicken events. Poms has opinions on every single one.', badge:'', stars:4},
                {time:'9:00 AM', title:'Chicken: A Love Story', desc:'Documentary. No plot arc necessary. Just chicken. Runtime: ongoing. Rating: perfect.', badge:'', stars:5},
                {time:'7:30 AM', title:'Cooking Chicken (Do Not Cook It Wrong)', desc:'Mandatory instructional content for all household members. Final exam: Poms. No retakes.', badge:'', stars:4},
                {time:'10:00 AM', title:'World Chicken Report', desc:'International chicken news. Update: more chicken exists globally. Assessment: good.', badge:'', stars:3},
                {time:'8:30 AM', title:'Chicken History', desc:'Where did chicken come from? Poms endorses all historical decisions regarding chicken.', badge:'', stars:3}
            ],
            afternoon: [
                {time:'1:00 PM', title:'The Chicken Hour', desc:'60 solid minutes of chicken. No other topics. No vegetables. Certainly no green beans.', badge:'', stars:5},
                {time:'2:00 PM', title:'Chicken Connoisseur', desc:'Poms evaluates today\'s offering. Scoring criteria: temperature, portion, presentation.', badge:'', stars:4},
                {time:'3:00 PM', title:'Chicken: Now and Later', desc:'Today\'s chicken situation and projections for tonight\'s dinner. Forecast: cautiously hopeful.', badge:'', stars:4},
                {time:'4:00 PM', title:'Advanced Chicken Studies', desc:'Academic deep-dive. Faculty: Poms. All sections. Prerequisites: appreciation of chicken.', badge:'', stars:3},
                {time:'1:30 PM', title:'Chicken World Tour', desc:'Chicken across cultures, all rated by Poms. All ratings: high. One: transcendent.', badge:'', stars:4},
                {time:'2:30 PM', title:'Great Moments in Chicken', desc:'Archive footage of memorable chicken events. Contains emotional content. Tissues recommended.', badge:'rerun', stars:4}
            ],
            evening: [
                {time:'5:30 PM', title:'Dinner Preview: Chicken Edition', desc:'Will there be chicken at dinner? Live analysis begins at 5:30. Stakes: very high.', badge:'live', stars:5},
                {time:'7:00 PM', title:'Chicken Report: Prime Time', desc:'In-depth post-dinner chicken coverage. Was it satisfactory? Analysis: ongoing.', badge:'', stars:4},
                {time:'8:00 PM', title:'The Chicken Files: Unsolved', desc:'Cases where the chicken did not appear at dinner. Cold cases. Literally cold.', badge:'', stars:4},
                {time:'9:00 PM', title:'Chicken After Dark', desc:'Is there enough chicken in the world? Philosophical inquiry. Poms: probably not.', badge:'', stars:3},
                {time:'6:00 PM', title:'BREAKING: Dinner Chicken Confirmed', desc:'LIVE updates from the food bowl. Chicken verified. Quality analysis: ongoing.', badge:'breaking', stars:5},
                {time:'7:30 PM', title:'Tomorrow\'s Chicken: A Preview', desc:'What chicken will tomorrow bring? Predictions. Hope: high. Demands: already drafted.', badge:'', stars:3}
            ],
            latenight: [
                {time:'11:00 PM', title:'Late Night Chicken Thoughts', desc:'Reflections on today\'s chicken. Assessment: good. Could always be more. Next steps: demand.', badge:'', stars:4},
                {time:'12:00 AM', title:'Chicken at Midnight', desc:'Is there chicken right now? Surveillance: no. Complaint MP-MIDNIGHT: filed at 12:01 AM.', badge:'live', stars:3},
                {time:'2:00 AM', title:'Dream Chicken', desc:'Animated. Depicts what Poms dreams about. Primary subject: chicken. Runtime: 6 hours.', badge:'', stars:4},
                {time:'3:00 AM', title:'Pre-Dawn Chicken Anticipation', desc:'Coverage begins 3 hours before breakfast. Stakes: maximum. Enthusiasm: yes.', badge:'', stars:4},
                {time:'1:00 AM', title:'Chicken: The Night Shift', desc:'Monitoring overnight chicken developments. Status: insufficient. Complaint: filed.', badge:'', stars:3},
                {time:'10:30 PM', title:'Chicken Confidential: After Hours', desc:'What happened to the rest of the dinner chicken? Investigation ongoing. Classified.', badge:'', stars:3}
            ]
        }
    },
    {
        num: '22',
        name: 'NAP NETWORK',
        tagline: 'Professional Rest Since 2023',
        color: '#336699',
        shows: {
            morning: [
                {time:'9:00 AM', title:'The Morning Nap', desc:'Post-breakfast nap. First of the scheduled daily naps. Duration: 2-4 hours. Narrated softly.', badge:'live', stars:4},
                {time:'7:00 AM', title:'Pre-Breakfast Nap', desc:'Essential rest before the demanding task of breakfast. Recommended for all cats.', badge:'', stars:3},
                {time:'10:00 AM', title:'Nap Science Today', desc:'Peer-reviewed nap position research. Lead researcher: Poms. Funding: chicken.', badge:'', stars:4},
                {time:'8:30 AM', title:'The Art of the Loaf', desc:'Instructional. How to achieve peak loaf formation. All limbs: fully tucked. Eyes: half-open.', badge:'', stars:4},
                {time:'11:00 AM', title:'Sunbeam Nap Special', desc:'Enhanced napping in direct sunlight. Warmth index: maximum. Quality: transcendent.', badge:'special', stars:5},
                {time:'9:30 AM', title:'Morning Rest Report', desc:'Assessment of last night\'s sleep. Rating: 7.4/10. Notes: doorbell at 11 PM. Unacceptable.', badge:'', stars:3}
            ],
            afternoon: [
                {time:'1:00 PM', title:'The Grand Nap: Afternoon Edition', desc:'4-hour premium nap block. All other household activity: please coordinate accordingly.', badge:'', stars:5},
                {time:'2:30 PM', title:'Strategic Rest Planning', desc:'Expert guidance on optimal nap placement for maximum warmth and human inconvenience.', badge:'', stars:4},
                {time:'3:00 PM', title:'Competitive Napping', desc:'Can anyone nap longer than Poms? Historical record: 9 hours, 14 minutes. Unchallenged.', badge:'', stars:4},
                {time:'12:00 PM', title:'Lunchtime Nap Block', desc:'Post-lunch rest. Duration: until the dinner alarm activates (the meow). Standard protocol.', badge:'', stars:4},
                {time:'4:00 PM', title:'The Pre-Dinner Nap', desc:'Critical energy conservation before evening food demands. Physiologically necessary.', badge:'', stars:4},
                {time:'1:30 PM', title:'Nap Position Masterclass', desc:'Today: the impossible pretzel. Attempt only if professionally trained. This means Poms.', badge:'new', stars:3}
            ],
            evening: [
                {time:'7:00 PM', title:'Post-Dinner Rest Hour', desc:'Recovery from the physical effort of eating dinner. Important. Standard duration: 2-3 hours.', badge:'', stars:4},
                {time:'8:30 PM', title:'Evening Loaf Mode', desc:'LIVE: Poms in full loaf formation. All limbs confirmed tucked. Warmth level: optimal.', badge:'live', stars:5},
                {time:'9:00 PM', title:'The Bedtime Nap', desc:'Pre-sleep nap. Distinct from actual sleep. Both essential. Do not confuse them.', badge:'', stars:3},
                {time:'6:30 PM', title:'Naptime Theater', desc:'Dramatic readings of official nap reports. Tonight: Form NR-7, this morning\'s filing.', badge:'', stars:3},
                {time:'8:00 PM', title:'World\'s Greatest Naps', desc:'Historical highlights reel. Featuring: the legendary 2024 9-hour record. Narrated with reverence.', badge:'', stars:4},
                {time:'7:30 PM', title:'Nap Review: Today\'s Assessment', desc:'Professional evaluation of today\'s naps. Overall: 8.7/10. Notes: vacuum at 10 AM. Complaint filed.', badge:'', stars:4}
            ],
            latenight: [
                {time:'10:00 PM', title:'Overnight Rest Coverage', desc:'Primary sleep block begins. Estimated duration: 8-10 hours. Quality: weather permitting.', badge:'live', stars:4},
                {time:'11:00 PM', title:'Sleep Science: Late Edition', desc:'Research on overnight nap efficacy. Preliminary findings: more sleep needed. Always more sleep.', badge:'', stars:3},
                {time:'2:00 AM', title:'The 3 AM Pre-Crisis Nap', desc:'Brief rest before the 3 AM bowl emergency. Preparation is professional. Poms is professional.', badge:'', stars:3},
                {time:'12:00 AM', title:'Midnight Nap Certification', desc:'Documenting nap #3 of the evening. All quality checkboxes: checked. Certified excellent.', badge:'', stars:4},
                {time:'4:00 AM', title:'Pre-Dawn Nap', desc:'Final nap before the 6 AM breakfast demand. This one always ends abruptly.', badge:'', stars:3},
                {time:'1:00 AM', title:'The Long Nap', desc:'Uninterrupted rest. Do not ring the doorbell. A formal warning has been preemptively filed.', badge:'', stars:4}
            ]
        }
    },
    {
        num: '47',
        name: 'COMPLAINT TV',
        tagline: 'Grievances 24/7. Filed Fresh Daily.',
        color: '#880000',
        shows: {
            morning: [
                {time:'6:02 AM', title:'First Complaint of the Day', desc:'LIVE: Bowl situation, day 847. Status: insufficient. Vocalization count: 3 and rising rapidly.', badge:'live', stars:5},
                {time:'7:30 AM', title:'Complaint Roundup: Overnight Edition', desc:'Summary of complaints filed midnight to 7 AM. Total: 14. Breakdown: all food-related.', badge:'', stars:4},
                {time:'9:00 AM', title:'Filing Live with Poms', desc:'Watch in real time as formal complaints are drafted, numbered, and officially logged.', badge:'live', stars:4},
                {time:'8:00 AM', title:'Historical Grievances', desc:'Classic complaints from 2022-2024. The Great Green Bean Incident. Never forgotten.', badge:'rerun', stars:4},
                {time:'10:00 AM', title:'The Complaint Department Opens', desc:'Official office hours. Today\'s docket: 9 items. 7 food-related. 2 vacuum-related. All valid.', badge:'', stars:3},
                {time:'7:00 AM', title:'Morning Severity Report', desc:'Classification of overnight filings. Tier 1: 3 critical. Tier 2: 7 serious. None: dismissed.', badge:'', stars:4}
            ],
            afternoon: [
                {time:'2:00 PM', title:'Afternoon Complaint Block', desc:'3-hour grievance coverage. Current topic: nap interrupted by doorbell. Inexcusable.', badge:'', stars:4},
                {time:'1:00 PM', title:'The Complaint Files: Unsolved', desc:'Cases filed but not resolved. The Green Bean Case: still open. Expected resolution: never.', badge:'', stars:4},
                {time:'3:30 PM', title:'Complaints vs. Formal Demands', desc:'What is the difference? Expert: Poms. Curriculum: 3 hours. All answers: yes, both valid.', badge:'', stars:3},
                {time:'4:00 PM', title:'Pre-Dinner Grievance Summary', desc:'All complaints must be filed before 6 PM. Today\'s count: 17. Resolution status: pending.', badge:'', stars:4},
                {time:'2:30 PM', title:'Best of Complaints: This Week', desc:'Top 10 complaints of the week, ranked by severity and dramatic impact of delivery.', badge:'rerun', stars:4},
                {time:'1:30 PM', title:'Formal vs. Informal Complaints', desc:'Formal: meowed at specific volume. Informal: the look. The look is legally recognized.', badge:'', stars:3}
            ],
            evening: [
                {time:'5:45 PM', title:'Dinner Delay Alert', desc:'BREAKING: Dinner not yet prepared. Complaint MP-DN filed at 5:45 PM. Severity: Tier 1.', badge:'breaking', stars:5},
                {time:'7:00 PM', title:'The Evening Grievance Report', desc:'Comprehensive review of today\'s complaints. Total filed: 23. All: valid. None: dismissed.', badge:'', stars:4},
                {time:'8:00 PM', title:'Prime Time Complaints', desc:'Tonight\'s top filings: 15-minute dinner delay, insufficient treats, the doorbell at 2 PM.', badge:'', stars:4},
                {time:'9:00 PM', title:'Complaint Resolution Watch', desc:'LIVE monitoring: how many complaints were resolved today? Update: some. Most: pending.', badge:'live', stars:4},
                {time:'6:30 PM', title:'Open Forum: Active Grievances', desc:'Community discussion of outstanding issues. Community size: 1. Forum location: kitchen floor.', badge:'', stars:3},
                {time:'8:30 PM', title:'Closing Arguments', desc:'Final complaints of the day. Tonight\'s closer: \'the bowl, again, still, always, forever\'.', badge:'', stars:4}
            ],
            latenight: [
                {time:'11:00 PM', title:'Midnight Filing Deadline', desc:'All complaints must be formally lodged by 11 PM. Current queue: 6. Processing now.', badge:'live', stars:4},
                {time:'12:00 AM', title:'Overnight Complaint Archive', desc:'System update: all complaints logged. Storage medium: the permanent memory of Poms.', badge:'', stars:3},
                {time:'2:00 AM', title:'3 AM Pre-Filing Preparation', desc:'Drafting tomorrow\'s 3 AM bowl complaint in advance. Professional. Efficient. Inevitable.', badge:'', stars:4},
                {time:'3:00 AM', title:'LIVE: 3 AM Bowl Emergency Filing', desc:'Complaint MP-3AM filed at 3:02 AM. Severity: Tier 1. Response time: 0-4 minutes.', badge:'live', stars:5},
                {time:'1:00 AM', title:'Overnight Grievances', desc:'Low-key complaint period. Mainly about the quiet. Too quiet. Suspicious quiet. Documented.', badge:'', stars:3},
                {time:'10:00 PM', title:'Daily Statistics Summary', desc:'Today\'s numbers: 31 filed, 3 resolved, 28 pending. Trend: upward. Poms: satisfied.', badge:'', stars:4}
            ]
        }
    }
];

// ── Build "On Now" section ─────────────────────────────────────────────────
var onnowContainer = document.getElementById('tvg-onnow-container');
onnowContainer.innerHTML = '';

channels.forEach(function (ch, i) {
    var slotShows = ch.shows[currentSlot];
    var show = pick(slotShows, seed * 7 + i * 13 + 99);

    var row = document.createElement('div');
    row.style.cssText = 'display:flex;align-items:flex-start;gap:8px;background:rgba(255,255,255,0.06);padding:5px 7px;border-radius:2px;';

    var chBadge = '<div style="background:' + ch.color + ';color:#FFD700;font-family:\'Courier New\',monospace;font-weight:bold;font-size:10px;padding:3px 5px;flex-shrink:0;min-width:32px;text-align:center;border-radius:2px;">CH ' + ch.num + '</div>';

    var badgeHtml = '';
    if (show.badge) {
        var badgeColors = {live:'#CC0000',new:'#006600',breaking:'#FF6600',rerun:'#666',special:'#6600CC'};
        var bc = badgeColors[show.badge] || '#333';
        badgeHtml = ' <span style="background:' + bc + ';color:#FFF;font-size:8px;font-weight:bold;padding:1px 4px;border-radius:2px;text-transform:uppercase;vertical-align:middle;">' + show.badge.toUpperCase() + '</span>';
    }

    row.innerHTML = chBadge +
        '<div style="flex:1;min-width:0;">' +
            '<div style="color:#FFFF99;font-weight:bold;font-size:11px;line-height:1.3;">' + show.title + badgeHtml + '</div>' +
            '<div style="color:#888AAA;font-size:9px;margin-top:1px;line-height:1.3;">' + ch.name + ' &nbsp;|&nbsp; ' + show.time + ' &nbsp;|&nbsp; ' + show.desc.substring(0, 80) + (show.desc.length > 80 ? '…' : '') + '</div>' +
        '</div>';

    onnowContainer.appendChild(row);
});

// ── Editor's Picks (random prime-time shows from 3 channels) ──────────────
var pickChannelIdxs = [];
var usedIdxs = {};
while (pickChannelIdxs.length < 3) {
    var ri = Math.floor(seededRand(seed * 3 + pickChannelIdxs.length * 77) * channels.length);
    if (!usedIdxs[ri]) { usedIdxs[ri] = true; pickChannelIdxs.push(ri); }
}

var picksGrid = document.getElementById('tvg-picks-grid');
picksGrid.innerHTML = '';

pickChannelIdxs.forEach(function (ci, pi) {
    var ch = channels[ci];
    var evShows = ch.shows.evening;
    var show = pick(evShows, seed * 5 + ci * 31 + pi * 17);

    var badgeHtml = '';
    if (show.badge) {
        var badgeColors = {live:'#CC0000',new:'#006600',breaking:'#FF6600',rerun:'#666',special:'#6600CC'};
        var bc = badgeColors[show.badge] || '#333';
        badgeHtml = '<span style="background:' + bc + ';color:#FFF;font-size:8px;font-weight:bold;padding:1px 4px;border-radius:2px;text-transform:uppercase;margin-right:4px;">' + show.badge.toUpperCase() + '</span>';
    }

    var stars = '';
    for (var s = 0; s < show.stars; s++) stars += '★';

    var div = document.createElement('div');
    div.style.cssText = 'flex:1;min-width:140px;background:#FFF;border:1px solid #DDD;border-left:4px solid ' + ch.color + ';padding:6px 8px;';
    div.innerHTML =
        '<div style="font-size:9px;color:#888;text-transform:uppercase;letter-spacing:1px;margin-bottom:2px;">CH ' + ch.num + ' ' + ch.name + ' &nbsp;|&nbsp; Tonight</div>' +
        '<div style="font-weight:bold;color:#003399;font-size:11px;margin-bottom:3px;">' + badgeHtml + show.title + '</div>' +
        '<div style="font-size:9px;color:#444;line-height:1.4;margin-bottom:4px;">' + show.desc + '</div>' +
        '<div style="color:#CC9900;font-size:10px;">' + stars + '</div>';

    picksGrid.appendChild(div);
});

// ── Render Schedule Table ─────────────────────────────────────────────────
var slotKeys   = ['morning', 'afternoon', 'evening', 'latenight'];
var slotThIds  = ['tvg-th-morning', 'tvg-th-afternoon', 'tvg-th-evening', 'tvg-th-latenight'];

// Highlight current column header
slotThIds.forEach(function (id, i) {
    if (slotKeys[i] === currentSlot) {
        var th = document.getElementById(id);
        if (th) { th.style.background = '#880000'; th.style.color = '#FFFF00'; }
    }
});

var tbody = document.getElementById('tvg-schedule-body');
tbody.innerHTML = '';

channels.forEach(function (ch, ci) {
    var tr = document.createElement('tr');

    // Channel cell
    var chTd = document.createElement('td');
    chTd.className = 'tvg-ch-cell';
    chTd.style.cssText = 'text-align:center;padding:6px 4px;border:1px solid #CCC;vertical-align:middle;width:65px;background:#F8F8F8;';
    chTd.innerHTML =
        '<div style="display:inline-block;background:' + ch.color + ';color:#FFD700;font-family:\'Courier New\',monospace;font-weight:bold;font-size:13px;padding:2px 5px;margin-bottom:3px;">' + ch.num + '</div>' +
        '<div style="font-weight:bold;font-size:9px;line-height:1.2;color:#000;">' + ch.name + '</div>' +
        '<div style="font-size:8px;color:#666;line-height:1.2;margin-top:2px;">' + ch.tagline + '</div>';
    tr.appendChild(chTd);

    slotKeys.forEach(function (slot, si) {
        var slotShows = ch.shows[slot];
        var show = pick(slotShows, seed * 7 + ci * 13 + si * 43);

        var isCurrent = (slot === currentSlot);
        var td = document.createElement('td');
        td.style.cssText = 'padding:6px 7px;border:1px solid #DDD;vertical-align:top;background:' + (isCurrent ? '#FFFCE0' : '#FFF') + ';' + (isCurrent ? 'border-left:3px solid #CC0000;border-right:3px solid #CC0000;' : '');

        var badgeHtml = '';
        if (show.badge) {
            var badgeColors = {live:'#CC0000',new:'#006600',breaking:'#FF6600',rerun:'#666666',special:'#6600CC'};
            var bc = badgeColors[show.badge] || '#333';
            badgeHtml = '<span style="background:' + bc + ';color:#FFF;font-size:8px;font-weight:bold;padding:1px 4px;border-radius:2px;text-transform:uppercase;margin-right:3px;">' + show.badge.toUpperCase() + '</span>';
        }

        var stars = '';
        for (var s = 0; s < show.stars; s++) stars += '★';

        td.innerHTML =
            '<div style="font-size:9px;color:#888;margin-bottom:2px;font-family:\'Courier New\',monospace;">' + show.time + (isCurrent ? ' &nbsp;<strong style="color:#CC0000;font-size:8px;">▶ ON NOW</strong>' : '') + '</div>' +
            '<div style="font-weight:bold;color:#003399;font-size:10px;line-height:1.3;margin-bottom:2px;">' + badgeHtml + show.title + '</div>' +
            '<div style="font-size:9px;color:#444;line-height:1.35;">' + show.desc + '</div>' +
            '<div style="margin-top:4px;color:#CC9900;font-size:9px;">' + stars + '</div>';

        tr.appendChild(td);
    });

    tbody.appendChild(tr);
});

}());
</script>
