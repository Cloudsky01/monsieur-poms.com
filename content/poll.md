---
title: "Daily Poll"
---

<style>
.poll-outer {
    border: 1px solid #CCC;
    overflow: hidden;
    margin-bottom: 20px;
    background: #F5F5F5;
}

.poll-header-strip {
    background: linear-gradient(to right, #000066, #000099, #000066);
    color: #FFFF00;
    text-align: center;
    padding: 18px 10px;
    border-bottom: 4px solid #FF0000;
}

.poll-header-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 30px;
    letter-spacing: 5px;
    text-shadow: 2px 2px 0 #FF0000;
    margin: 0;
}

.poll-header-sub {
    font-size: 10px;
    color: #AAAAFF;
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-top: 5px;
}

.poll-datebar {
    background: #CC0000;
    color: #FFFF00;
    font-family: 'Courier New', monospace;
    font-size: 11px;
    font-weight: bold;
    letter-spacing: 2px;
    text-align: center;
    padding: 4px 10px;
    border-bottom: 2px solid #880000;
}

.poll-question-box {
    background: #FFFFFF;
    border: 3px inset #CCCCCC;
    margin: 14px;
    padding: 14px 16px;
}

.poll-question-label {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 11px;
    letter-spacing: 3px;
    color: #CC0000;
    text-transform: uppercase;
    margin-bottom: 8px;
    border-bottom: 1px solid #EEE;
    padding-bottom: 5px;
}

.poll-question-text {
    font-size: 15px;
    font-weight: bold;
    color: #000080;
    line-height: 1.4;
    margin-bottom: 14px;
}

.poll-option {
    display: flex;
    align-items: flex-start;
    gap: 8px;
    padding: 7px 8px;
    margin: 4px 0;
    border: 1px solid #CCCCCC;
    background: #F8F8F8;
    cursor: pointer;
    font-size: 12px;
    color: #333;
    transition: background 0.1s;
    user-select: none;
}

.poll-option:hover {
    background: #E8E8FF;
    border-color: #0000FF;
}

.poll-option.selected {
    background: #DDEEFF;
    border-color: #000099;
    font-weight: bold;
    color: #000080;
}

.poll-radio {
    margin-top: 2px;
    flex-shrink: 0;
    accent-color: #000080;
}

.vote-btn {
    display: block;
    margin: 14px auto 0;
    background: linear-gradient(to bottom, #3366FF, #0033CC);
    color: #FFFF00;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 16px;
    letter-spacing: 3px;
    border: 3px outset #6699FF;
    padding: 8px 28px;
    cursor: pointer;
    text-shadow: 1px 1px 0 #000033;
    box-shadow: 3px 3px 0 #001166;
    text-transform: uppercase;
}

.vote-btn:hover {
    background: linear-gradient(to bottom, #FF6600, #CC3300);
    border-color: #FF9944;
}

.vote-btn:active {
    border-style: inset;
    box-shadow: 1px 1px 0 #001166;
}

.results-box {
    display: none;
    margin: 14px;
    padding: 14px;
    background: #FFFFFF;
    border: 3px inset #AAAAAA;
}

.results-header {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 13px;
    letter-spacing: 3px;
    color: #006600;
    text-transform: uppercase;
    margin-bottom: 12px;
    border-bottom: 2px solid #006600;
    padding-bottom: 5px;
}

.result-row {
    margin: 6px 0;
    font-size: 11px;
}

.result-label {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 2px;
    gap: 4px;
}

.result-label-text {
    color: #333;
    line-height: 1.3;
    flex: 1;
}

.result-pct {
    font-weight: bold;
    font-family: 'Courier New', monospace;
    color: #000080;
    font-size: 12px;
    flex-shrink: 0;
    min-width: 36px;
    text-align: right;
}

.result-bar-outer {
    background: #DDDDDD;
    border: 1px solid #999;
    height: 14px;
    width: 100%;
}

.result-bar-inner {
    height: 100%;
    background: linear-gradient(to right, #003399, #3366FF);
    animation: barGrow 0.6s ease-out forwards;
}

.result-bar-inner.winner {
    background: linear-gradient(to right, #006600, #33BB33);
}

@keyframes barGrow {
    from { width: 0; }
}

.winner-badge {
    display: inline-block;
    background: #FFDD00;
    color: #000000;
    font-size: 9px;
    font-weight: bold;
    padding: 1px 5px;
    border: 1px solid #CC9900;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-left: 6px;
    vertical-align: middle;
}

.votes-total {
    font-size: 10px;
    color: #666;
    font-family: 'Courier New', monospace;
    margin-bottom: 12px;
}

.poms-comment-box {
    background: linear-gradient(to right, #FFFDE0, #FFFACC);
    border: 2px solid #CCAA00;
    border-left: 5px solid #FFDD00;
    padding: 10px 13px;
    margin-top: 14px;
    font-size: 11px;
    color: #333;
    line-height: 1.65;
}

.poms-comment-header {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 10px;
    letter-spacing: 2px;
    color: #885500;
    text-transform: uppercase;
    margin-bottom: 5px;
}

.your-vote-notice {
    font-size: 10px;
    color: #006600;
    font-weight: bold;
    font-style: italic;
    text-align: center;
    margin-top: 10px;
    padding-top: 8px;
    border-top: 1px dashed #AAAAAA;
}

.archive-section {
    margin: 0 14px 14px;
    border: 1px solid #CCCCCC;
    background: #FFFFFF;
}

.archive-header {
    background: #000080;
    color: #FFFFFF;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 13px;
    letter-spacing: 3px;
    padding: 6px 10px;
    text-transform: uppercase;
}

.archive-row {
    border-bottom: 1px solid #EEEEEE;
    padding: 7px 10px;
    font-size: 10px;
}

.archive-row:last-child { border-bottom: none; }

.archive-row-date {
    font-family: 'Courier New', monospace;
    color: #888;
    font-size: 9px;
    margin-bottom: 2px;
}

.archive-row-q {
    font-weight: bold;
    color: #000080;
    margin-bottom: 3px;
}

.archive-winner-tag {
    display: inline-block;
    background: #006600;
    color: #FFF;
    font-size: 9px;
    font-weight: bold;
    padding: 1px 5px;
    margin-right: 4px;
    text-transform: uppercase;
}

.archive-winner-pct {
    color: #006600;
    font-weight: bold;
    font-family: 'Courier New', monospace;
}

.poll-disclaimer {
    font-size: 9px;
    color: #888;
    text-align: center;
    padding: 8px 14px;
    background: #F0F0F0;
    border-top: 1px solid #DDD;
    line-height: 1.7;
    font-style: italic;
}

@keyframes pollReveal {
    from { opacity: 0; transform: translateY(-4px); }
    to   { opacity: 1; transform: translateY(0); }
}
.poll-reveal { animation: pollReveal 0.35s ease-out forwards; }
</style>

<div class="poll-outer">

<div class="poll-header-strip">
    <div class="poll-header-title">🗳️ POMS DAILY POLL 🗳️</div>
    <div class="poll-header-sub">Your vote is counted. It does not change the outcome. Both things are true.</div>
</div>

<div class="poll-datebar">
    <span id="poll-dateline">Loading...</span> &nbsp;|&nbsp; POLL CLOSES AT MIDNIGHT &nbsp;|&nbsp; POLL #<span id="poll-number">---</span>
</div>

<div style="padding: 0 14px;">
    <p style="font-size: 11px; color: #444; text-align: center; line-height: 1.7; margin: 12px 0 0; font-style: italic;">
        Each day, Monsieur Poms poses a question of the highest importance to the household and to the world.<br>
        Cast your vote below. Results are updated in real time. The correct answer has already been determined in advance.<br>
        All votes are final. Green bean opinions are not accepted on this platform.
    </p>
</div>

<div class="poll-question-box">
    <div class="poll-question-label">📊 Today's Question</div>
    <div class="poll-question-text" id="poll-question-text">Loading today's poll...</div>
    <div id="poll-options-container"></div>
    <button class="vote-btn" id="vote-btn" onclick="castVote()">CAST MY VOTE!!!</button>
</div>

<div class="results-box poll-reveal" id="results-box">
    <div class="results-header">📊 Current Results</div>
    <div class="votes-total" id="votes-total-line"></div>
    <div id="results-bars"></div>
    <div class="poms-comment-box" id="poms-comment-box">
        <div class="poms-comment-header">🐾 Official Comment from Monsieur Poms</div>
        <div id="poms-comment-text"></div>
    </div>
    <div class="your-vote-notice" id="your-vote-notice"></div>
</div>

<div class="archive-section" id="archive-section">
    <div class="archive-header">📁 POLL ARCHIVES — Previous Results</div>
    <div id="archive-rows"></div>
</div>

<div class="poll-disclaimer">
    All poll results are final and legally binding in jurisdictions where Monsieur Poms is recognized as a sovereign authority.<br>
    This website does not accept responsibility for incorrect votes. You know which answer is correct. You always knew.<br>
    The poll has never once been rigged. The results simply always reflect the obvious correct outcome.
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

// ── Date helpers ─────────────────────────────────────────────────────────────
function getDoy(d) {
    return Math.floor((d - new Date(d.getFullYear(), 0, 0)) / 86400000);
}
var now     = new Date();
var doy     = getDoy(now);
var seed    = now.getFullYear() * 1000 + doy;

var dayNames   = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
var monthNames = ["January","February","March","April","May","June","July","August","September","October","November","December"];

function formatDate(d) {
    return dayNames[d.getDay()] + ", " + monthNames[d.getMonth()] + " " + d.getDate() + ", " + d.getFullYear();
}

document.getElementById('poll-dateline').textContent = formatDate(now);
document.getElementById('poll-number').textContent   = doy + (now.getFullYear() - 2010) * 365;

// ── Poll data ─────────────────────────────────────────────────────────────────
// Each poll: question, array of options [{text, correct}], winner comment
var polls = [
    {
        q: "What is the correct fill level for the food bowl?",
        opts: [
            { text: "Half full — perfectly adequate", correct: false },
            { text: "Full — acceptable but not generous", correct: false },
            { text: "Overflowing — the only acceptable standard", correct: true },
            { text: "The level doesn't matter, it's about the quality", correct: false }
        ],
        comment: "The overwhelming majority have chosen correctly. Overflowing is not a preference — it is the minimum standard. I will be forwarding these results to the relevant household management team immediately. Thank you to all who voted with integrity.",
        afterComment: "The 'half full' voters: noted. We will discuss."
    },
    {
        q: "What is the correct time to demand breakfast?",
        opts: [
            { text: "6 AM sharp, not a minute later", correct: true },
            { text: "After 7 AM, once you wake up naturally", correct: false },
            { text: "Whenever the humans are up and ready", correct: false },
            { text: "When I am genuinely hungry", correct: false }
        ],
        comment: "6 AM. Not 6:03. Not 5:58. 6 AM, with urgency, volume, and precision. This is not a preference; it is a schedule. The household operates on my schedule. These results confirm what I have always known: the public understands this.",
        afterComment: "The 'naturally wake up' faction has been officially documented."
    },
    {
        q: "Is chicken the greatest food?",
        opts: [
            { text: "Yes. Obviously. Without question.", correct: true },
            { text: "It is one of many great foods", correct: false },
            { text: "I prefer fish personally", correct: false },
            { text: "I have no strong opinions on chicken", correct: false }
        ],
        comment: "The numbers speak for themselves. Chicken is not one of many great foods. It IS the food. I have maintained this position since birth and the public has finally caught up. To the fish faction: I respect your journey, but you are wrong.",
        afterComment: "The 'no strong opinion' group: we need to talk."
    },
    {
        q: "Who deserves priority access to the prime sunbeam spot?",
        opts: [
            { text: "Whoever gets there first", correct: false },
            { text: "Everyone should share equally", correct: false },
            { text: "Monsieur Poms — by decree and natural right", correct: true },
            { text: "The plants, they need it for photosynthesis", correct: false }
        ],
        comment: "I am moved by this result. Genuinely moved. The public recognizes what the plants refuse to acknowledge: I was there first, I am there most, and my need is greatest. The sunbeam belongs to me. It always has. This poll simply made it official.",
        afterComment: "The plant lobby had 4%. I will address this next week."
    },
    {
        q: "How many naps per day is optimal?",
        opts: [
            { text: "1 to 2 — that is more than enough", correct: false },
            { text: "3 to 4 — a reasonable amount", correct: false },
            { text: "5 to 7 — properly managed rest", correct: false },
            { text: "As many as are needed — quantity is not the metric", correct: true }
        ],
        comment: "The quantity is not the point. The point is quality, duration, and whether the sunbeam was present. I may nap 9 times or once for 11 hours. Both are valid. Both are optimal. Both are professionally executed. The public understands this and I am grateful.",
        afterComment: "'1 to 2' is a position I cannot support in good conscience."
    },
    {
        q: "The vacuum cleaner is best described as...",
        opts: [
            { text: "A useful household cleaning tool", correct: false },
            { text: "Loud but harmless", correct: false },
            { text: "A confirmed and documented threat to household security", correct: true },
            { text: "Something I personally find neutral", correct: false }
        ],
        comment: "Confirmed. Documented. Classified. I have filed 47 formal reports about the vacuum cleaner since 2023 and not one has been resolved. These poll results go into the official record. I am gratified that the public has taken this seriously. The vacuum is a THREAT.",
        afterComment: "'Loud but harmless': these voters have not been paying attention."
    },
    {
        q: "What should happen when green beans are served at dinner?",
        opts: [
            { text: "Eat them — vegetables are nutritious", correct: false },
            { text: "Move them to the side and eat around them", correct: false },
            { text: "Remove them from the plate, the house, and the premises", correct: true },
            { text: "Try them once before judging", correct: false }
        ],
        comment: "Correct. Immediate and total removal. I tried one in 2023. Once. The incident is documented. The verdict stands for all future time. The 'try them once' faction is testing my patience and I have very limited patience in this area specifically.",
        afterComment: "The 'eat them' voters: I am choosing not to comment. You know why."
    },
    {
        q: "Who is the most important resident of the household?",
        opts: [
            { text: "The humans — they pay rent and provide services", correct: false },
            { text: "Everyone contributes equally in their own way", correct: false },
            { text: "Monsieur Poms — clearly and without ambiguity", correct: true },
            { text: "Whoever holds the treat bag in a given moment", correct: false }
        ],
        comment: "Without ambiguity. Without question. Without revision. I am the most important resident. The humans provide services — food, warmth, lap access — and are valued accordingly. But importance is a different matter. The public understands the distinction.",
        afterComment: "The treat bag theory has merit but misunderstands the question."
    },
    {
        q: "The best nap position is...",
        opts: [
            { text: "Curled up in a neat, compact ball", correct: false },
            { text: "Full sprawl — maximum territorial coverage", correct: false },
            { text: "The Loaf — all limbs professionally tucked", correct: false },
            { text: "Directly on the human's laptop or important paperwork", correct: true }
        ],
        comment: "Strategic. Warm. Inconvenient to everyone but me. The laptop position communicates: I am here, I am warm, and whatever you are doing is less important than my current nap. The public instinctively understood this. I did not need to explain it. I rarely do.",
        afterComment: "'Compact ball' voters: respectable. But not strategic."
    },
    {
        q: "A treat should be given...",
        opts: [
            { text: "Once per day, as a small and sensible reward", correct: false },
            { text: "Twice per day — morning and evening", correct: false },
            { text: "On demand and immediately, without negotiation", correct: true },
            { text: "Never — treats are not necessary for a balanced diet", correct: false }
        ],
        comment: "On demand. Immediately. No negotiation. I will not discuss the timeline. I will not discuss 'whether I earned it.' I want a treat. This is the entire conversation. The public agrees. The 'never' faction: I am aware of your position. I reject it.",
        afterComment: "'Twice per day' is closer, but 'twice per day' implies a schedule. I don't believe in schedules for treats."
    },
    {
        q: "An empty food bowl should be interpreted as...",
        opts: [
            { text: "Fine — meal times are scheduled and consistent", correct: false },
            { text: "A gentle reminder to refill when convenient", correct: false },
            { text: "A full-scale domestic emergency requiring immediate escalation", correct: true },
            { text: "An opportunity to practice patience and gratitude", correct: false }
        ],
        comment: "Correct. Emergency. Full-scale. Immediate. The empty bowl is not a hint. It is not a suggestion. It is an alarm. I treat it as one. The household should treat it as one. The public agrees and I am relieved this needed only one poll to confirm.",
        afterComment: "The 'practice patience' option received votes. I am choosing to move forward."
    },
    {
        q: "What is the correct thing to do at 3 AM?",
        opts: [
            { text: "Sleep. It is 3 AM. Nothing else.", correct: false },
            { text: "Dream about pleasant things quietly", correct: false },
            { text: "File an emergency vocalization regarding the bowl", correct: true },
            { text: "Conduct a thorough perimeter patrol of the apartment", correct: false }
        ],
        comment: "The bowl does not keep office hours. The bowl's emptiness at 3 AM is as unacceptable as at noon — arguably more so, due to the darkness and the urgency. The public correctly identifies: vocalization is necessary. Sustained, precise, and well-projected vocalization.",
        afterComment: "The 'sleep' faction: I hear you. I also hear the bowl. And it is louder."
    },
    {
        q: "Rate the performance of the household humans this week.",
        opts: [
            { text: "Outstanding — exceptional service and full compliance", correct: false },
            { text: "Good — minor delays but generally satisfactory", correct: false },
            { text: "Needs Improvement — several documented incidents this week", correct: true },
            { text: "Excellent — I have no complaints at this time", correct: false }
        ],
        comment: "I always have complaints. There is no week in which I have no complaints. The public understands this. Three documented incidents this week: late dinner Tuesday, incorrect treat ratio Thursday, and the vacuum was deployed with insufficient prior notice. All noted. Filed. Archived.",
        afterComment: "'Outstanding' received some votes. I am investigating who submitted them."
    },
    {
        q: "The cardboard box belongs to...",
        opts: [
            { text: "Whoever needs it at the time", correct: false },
            { text: "No one in particular — it is a shared resource", correct: false },
            { text: "Monsieur Poms, upon its arrival in the household", correct: true },
            { text: "The person who purchased whatever came inside it", correct: false }
        ],
        comment: "Upon arrival. Not 'when I decide to use it.' Not 'after the contents are removed.' UPON ARRIVAL. It transfers into my possession the moment it crosses the threshold. This is not a rule I invented — it is simply the correct interpretation of events. The public agrees.",
        afterComment: "'The person who bought it' voters: I appreciate your perspective. It is incorrect."
    },
    {
        q: "What is the internet's highest and best use?",
        opts: [
            { text: "Communication, information, and global connectivity", correct: false },
            { text: "Shopping and entertainment", correct: false },
            { text: "Looking at pictures of cats at all times", correct: false },
            { text: "Visiting monsieur-poms.com and reading about Monsieur Poms", correct: true }
        ],
        comment: "Self-evident. The public recognizes what the internet was always destined to become. You are here. You voted. You are already participating in the highest possible use of this technology. I commend you. You have chosen correctly. The others: still valuable, but second place.",
        afterComment: "The 'global connectivity' group has potential. They just need direction."
    },
    {
        q: "Is Monsieur Poms tall, or chonky?",
        opts: [
            { text: "Chonky — clearly and undeniably chonky", correct: false },
            { text: "Average-sized, honestly", correct: false },
            { text: "Tall — the height is stored horizontally", correct: true },
            { text: "I decline to answer on the grounds that it is complicated", correct: false }
        ],
        comment: "TALL. Horizontally stored. This is not a debate. This is not a matter of interpretation. I am tall. The height is simply distributed differently than in most cats. This is a structural consideration, not a weight question. The public has overwhelmingly accepted this. I am satisfied.",
        afterComment: "'Chonky': this word is not recognized by this office."
    },
    {
        q: "How should one respond to the Disappointed Eyes?",
        opts: [
            { text: "Maintain resolve — they are just eyes", correct: false },
            { text: "Offer a chin scratch as a compromise", correct: false },
            { text: "Immediately produce a treat with full apology", correct: true },
            { text: "Leave the room to break the eye contact", correct: false }
        ],
        comment: "The Disappointed Eyes are not just eyes. They are a communication. A full and formal communication. The correct response is: treat, immediate, with acknowledgment. I have deployed the Disappointed Eyes 214 times this year. Resolution time: averaging 3.2 minutes. The public knows.",
        afterComment: "'Leave the room': I will follow you. I have followed humans into rooms they believed were private. I have no boundaries in this area."
    },
    {
        q: "When is 'too much' vocalization?",
        opts: [
            { text: "After the third meow on the same subject", correct: false },
            { text: "After 10 minutes on the same topic", correct: false },
            { text: "Once the matter is resolved — until then, continue", correct: true },
            { text: "At 3 AM specifically — that is excessive", correct: false }
        ],
        comment: "There is no 'too much.' There is 'unresolved' and 'resolved.' I am vocal until the matter is resolved. This morning's matter was resolved at 6:38 AM. The vocalization lasted from 6:00 AM. 38 minutes is appropriate and proportional. The public concurs.",
        afterComment: "'3 AM specifically': I respectfully and completely disagree."
    },
    {
        q: "How should one feel about Monday mornings?",
        opts: [
            { text: "Productive — a fresh start and new opportunities", correct: false },
            { text: "Fine — Mondays are the same as any other day", correct: false },
            { text: "Every morning is the same: get up, demand food, assess the sunbeam", correct: true },
            { text: "Dread — Mondays are objectively difficult", correct: false }
        ],
        comment: "The days of the week are a human concept that I observe only in terms of bowl timing and human availability. Monday, Thursday, Saturday — the bowl assessment is identical. The sunbeam question is identical. My position is identical. The public, correctly, understands this efficiency.",
        afterComment: "The 'productive' group: I respect this orientation. I simply do not share it."
    },
    {
        q: "The lap is best described as...",
        opts: [
            { text: "A sometimes-available resting spot", correct: false },
            { text: "Mine, whenever I choose to use it, without question", correct: true },
            { text: "A shared space that must be negotiated", correct: false },
            { text: "Unavailable when the human is working", correct: false }
        ],
        comment: "Mine. Without qualification. Without a scheduling system. Without negotiation. The human may have other plans. Those plans are now secondary. I have arrived. The lap is in use. Please remain still. The public agrees this is the correct arrangement and I thank them sincerely.",
        afterComment: "'When the human is working': this is precisely when the lap is most available and most needed."
    },
    {
        q: "What should happen if dinner is more than 5 minutes late?",
        opts: [
            { text: "Wait patiently — it will arrive shortly", correct: false },
            { text: "Politely remind the human once", correct: false },
            { text: "Begin a sustained vocal escalation campaign immediately", correct: true },
            { text: "Check back in 10 minutes to allow time to prepare", correct: false }
        ],
        comment: "Sustained. Escalating. Sustained escalation. Not a single reminder. A CAMPAIGN. The bowl is late. This is a scheduling failure. The household needs to understand the gravity. I begin at minute 6 and I do not stop until resolution is confirmed. The public understands protocol.",
        afterComment: "'Politely remind once': I do not do things once in this context."
    },
    {
        q: "Which room has the best sunbeam quality?",
        opts: [
            { text: "Wherever I am currently sitting", correct: true },
            { text: "The living room — large windows", correct: false },
            { text: "The kitchen — lots of morning light", correct: false },
            { text: "It varies — I check all rooms systematically", correct: false }
        ],
        comment: "Wherever I am. This is not preference — it is operational. I relocate to the beam. The beam becomes my location. My location therefore always has the best sunbeam. This is a tautology, but a correct one. The public grasped this and voted accordingly. Efficient.",
        afterComment: "'Check all rooms': this is my exact method, but the answer is still wherever I end up."
    },
    {
        q: "Should Monsieur Poms get more treats?",
        opts: [
            { text: "No — the current treat allocation is appropriate", correct: false },
            { text: "Maybe — it depends on the day", correct: false },
            { text: "Yes — always, unconditionally, and without ceiling", correct: true },
            { text: "I need more information before answering", correct: false }
        ],
        comment: "Yes. Always. The answer is yes in all contexts, in all time zones, on all days of the week including Sundays. The treat situation is never fully resolved. There is always room. I will provide a filing cabinet's worth of documentation to support this position if required.",
        afterComment: "The 'appropriate allocation' group: there is no appropriate allocation. There is only more."
    },
    {
        q: "The best way to wake a sleeping human is...",
        opts: [
            { text: "Wait nearby and let them wake naturally", correct: false },
            { text: "Gently sit on their feet until they stir", correct: false },
            { text: "Stand directly on their face at the earliest opportunity", correct: true },
            { text: "Make a noise from the hallway as a subtle signal", correct: false }
        ],
        comment: "Direct. Efficient. Immediate. The face provides warmth, proximity, and unambiguous communication. The message is: I am here, I am ready, the bowl requires attention. A hallway noise is ambiguous. Face presence is not. The public understands. The humans also understand. They just wish they did not.",
        afterComment: "'Wait nearby': I tried this in 2023. It took 47 minutes. Never again."
    },
    {
        q: "This website is...",
        opts: [
            { text: "Pretty good, I suppose", correct: false },
            { text: "A solid effort with room for improvement", correct: false },
            { text: "Excellent — among the better sites on the internet", correct: false },
            { text: "The finest and most important website currently online", correct: true }
        ],
        comment: "Correct. The finest. I have visited other sites. I have assessed them. They are not this. I am featured on this site. My decrees, my opinions, my nap reports, my exchange data — all here. There is no higher possible standard. The public voted correctly and I am proud of all of you.",
        afterComment: "'Room for improvement': if you have specific notes, please submit via the Complaint Department."
    }
];

// ── Pick today's poll ────────────────────────────────────────────────────────
var todayPoll = polls[Math.floor(seededRand(seed) * polls.length)];
var winnerIdx = 0;
for (var i = 0; i < todayPoll.opts.length; i++) {
    if (todayPoll.opts[i].correct) { winnerIdx = i; break; }
}

document.getElementById('poll-question-text').textContent = todayPoll.q;

// Build options
var optContainer = document.getElementById('poll-options-container');
todayPoll.opts.forEach(function (opt, i) {
    var div = document.createElement('div');
    div.className = 'poll-option';
    div.id = 'poll-opt-' + i;
    div.innerHTML =
        '<input type="radio" name="poll-vote" value="' + i + '" id="radio-' + i + '" class="poll-radio"> ' +
        '<label for="radio-' + i + '" style="cursor:pointer; flex:1;">' + opt.text + '</label>';
    div.onclick = function () {
        document.querySelectorAll('.poll-option').forEach(function (el) { el.classList.remove('selected'); });
        div.classList.add('selected');
        document.getElementById('radio-' + i).checked = true;
    };
    optContainer.appendChild(div);
});

// ── Build fake vote percentages ──────────────────────────────────────────────
function buildPercentages(winIdx, numOpts, s) {
    var winPct = 78 + Math.floor(seededRand(s) * 16);   // 78–93%
    var remaining = 100 - winPct;
    var others = [];
    for (var i = 0; i < numOpts - 1; i++) {
        others.push(0);
    }
    for (var j = 0; j < remaining; j++) {
        var pick2 = Math.floor(seededRand(s + j * 7 + 1) * others.length);
        others[pick2]++;
    }
    var result = [];
    var oi = 0;
    for (var k = 0; k < numOpts; k++) {
        if (k === winIdx) { result.push(winPct); }
        else { result.push(others[oi++]); }
    }
    return result;
}

var pcts = buildPercentages(winnerIdx, todayPoll.opts.length, seed + 77);
var totalVotes = 41800 + Math.floor(seededRand(seed + 200) * 8400);

var selectedVoteIdx = -1;
var hasVoted = false;

window.castVote = function () {
    if (hasVoted) return;
    var checked = document.querySelector('input[name="poll-vote"]:checked');
    if (!checked) {
        alert("Please select an option before voting!");
        return;
    }
    selectedVoteIdx = parseInt(checked.value, 10);
    hasVoted = true;

    document.getElementById('vote-btn').disabled = true;
    document.getElementById('vote-btn').textContent = 'VOTE RECORDED';
    document.getElementById('vote-btn').style.background = 'linear-gradient(to bottom, #666, #444)';

    // Build results
    var resBox = document.getElementById('results-box');
    resBox.style.display = 'block';

    document.getElementById('votes-total-line').textContent =
        'Total votes cast: ' + totalVotes.toLocaleString() + ' (including yours — thank you for your participation)';

    var barsDiv = document.getElementById('results-bars');
    barsDiv.innerHTML = '';
    todayPoll.opts.forEach(function (opt, i) {
        var isWinner = (i === winnerIdx);
        var pct = pcts[i];
        var row = document.createElement('div');
        row.className = 'result-row';

        var badge = isWinner ? '<span class="winner-badge">✓ Poms\' Pick</span>' : '';
        var myVote = (i === selectedVoteIdx) ? '<span style="color:#006600;font-size:9px;font-weight:bold;"> ← YOUR VOTE</span>' : '';

        row.innerHTML =
            '<div class="result-label">' +
                '<span class="result-label-text">' + opt.text + badge + myVote + '</span>' +
                '<span class="result-pct">' + pct + '%</span>' +
            '</div>' +
            '<div class="result-bar-outer">' +
                '<div class="result-bar-inner ' + (isWinner ? 'winner' : '') + '" style="width:' + pct + '%;">' +
                '</div>' +
            '</div>';

        barsDiv.appendChild(row);
    });

    document.getElementById('poms-comment-text').textContent = todayPoll.comment;

    var voteNote = (selectedVoteIdx === winnerIdx)
        ? "✓ You voted correctly. Monsieur Poms acknowledges your good judgment and extends a formal nod."
        : "You did not vote for the correct option. This has been noted. There is still time to learn from this.";
    document.getElementById('your-vote-notice').textContent = voteNote;

    resBox.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
};

// ── Build archive (last 5 days) ───────────────────────────────────────────────
var archiveDiv = document.getElementById('archive-rows');
archiveDiv.innerHTML = '';

for (var d = 1; d <= 5; d++) {
    var pastDate = new Date(now);
    pastDate.setDate(pastDate.getDate() - d);
    var pastDoy  = getDoy(pastDate);
    var pastSeed = pastDate.getFullYear() * 1000 + pastDoy;

    var pastPoll = polls[Math.floor(seededRand(pastSeed) * polls.length)];
    var pastWin  = 0;
    for (var pi = 0; pi < pastPoll.opts.length; pi++) {
        if (pastPoll.opts[pi].correct) { pastWin = pi; break; }
    }
    var pastPcts = buildPercentages(pastWin, pastPoll.opts.length, pastSeed + 77);

    var row2 = document.createElement('div');
    row2.className = 'archive-row';
    row2.innerHTML =
        '<div class="archive-row-date">' + formatDate(pastDate) + '</div>' +
        '<div class="archive-row-q">' + pastPoll.q + '</div>' +
        '<div>' +
            '<span class="archive-winner-tag">Winner</span>' +
            '<span style="font-size:10px; color:#333;">' + pastPoll.opts[pastWin].text + '</span>' +
            ' <span class="archive-winner-pct">(' + pastPcts[pastWin] + '%)</span>' +
        '</div>';
    archiveDiv.appendChild(row2);
}

})();
</script>
