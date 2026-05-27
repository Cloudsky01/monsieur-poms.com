---
title: "Human Performance Review"
---

<style>
.review-header-strip {
    background: linear-gradient(to right, #0d1a3a, #1a3060, #0d1a3a);
    color: #E8EEFF;
    text-align: center;
    padding: 16px 10px;
    margin: -10px -10px 0 -10px;
    border-bottom: 3px solid #4466BB;
}

.review-document {
    background: #FAFAFA;
    border: 2px solid #AAAACC;
    padding: 20px 22px;
    margin: 15px 0;
    box-shadow: inset 0 0 20px rgba(0,0,48,0.04), 4px 4px 0 #8888AA;
    font-family: 'Verdana', 'Arial', sans-serif;
}

.review-letterhead {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 10px;
    border-bottom: 3px double #000080;
    padding-bottom: 10px;
    margin-bottom: 14px;
}

.review-meta-table {
    width: 100%;
    border-collapse: collapse;
    margin-bottom: 14px;
    font-size: 11px;
}

.review-meta-table td {
    border: 1px solid #BBBBDD;
    padding: 4px 8px;
    background: #F5F5FF;
}

.review-meta-table td.meta-label {
    background: #DDDDF0;
    font-weight: bold;
    color: #000080;
    width: 110px;
    font-size: 9px;
    text-transform: uppercase;
    letter-spacing: 1px;
}

.category-row {
    display: flex;
    align-items: flex-start;
    gap: 11px;
    border: 1px solid #DDDDEE;
    padding: 9px 10px;
    margin-bottom: 6px;
    background: #FDFDFF;
    animation: rowSlide 0.35s ease-out both;
}

@keyframes rowSlide {
    from { opacity: 0; transform: translateX(-5px); }
    to   { opacity: 1; transform: translateX(0); }
}

.grade-box {
    width: 50px;
    height: 50px;
    border: 3px solid;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 22px;
    font-weight: bold;
    flex-shrink: 0;
    box-shadow: 2px 2px 0 rgba(0,0,0,0.22);
}

.grade-sublabel {
    font-size: 7px;
    font-family: 'Verdana', sans-serif;
    font-weight: bold;
    text-align: center;
    max-width: 50px;
    line-height: 1.2;
    margin-top: 3px;
    letter-spacing: 0.5px;
    text-transform: uppercase;
}

.category-name {
    font-family: 'Verdana', sans-serif;
    font-size: 10px;
    font-weight: bold;
    color: #000080;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 4px;
}

.category-comment {
    font-size: 11px;
    color: #333;
    line-height: 1.65;
    font-style: italic;
}

.score-bar-outer {
    background: #DDDDEE;
    border: 2px inset #AAAACC;
    height: 22px;
    width: 100%;
    overflow: hidden;
    margin: 7px 0 3px;
}

.score-bar-inner {
    height: 100%;
    animation: scoreBarFill 1.1s ease-out forwards;
}

@keyframes scoreBarFill { from { width: 0%; } }

.overall-grade-badge {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 44px;
    border: 4px solid;
    width: 68px;
    height: 68px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    box-shadow: 3px 3px 0 rgba(0,0,0,0.28);
    flex-shrink: 0;
}

.manager-assessment-box {
    border: 2px solid #000080;
    background: #F0F0FF;
    padding: 12px 14px;
    margin: 14px 0 10px;
    font-size: 11px;
    line-height: 1.78;
    color: #000080;
}

.section-header {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 12px;
    letter-spacing: 2px;
    color: #000080;
    border-bottom: 2px solid #000080;
    padding-bottom: 4px;
    margin-bottom: 9px;
    text-transform: uppercase;
}

.action-item {
    display: flex;
    align-items: flex-start;
    gap: 8px;
    padding: 5px 0;
    border-bottom: 1px dotted #BBBBDD;
    font-size: 11px;
    color: #222255;
    line-height: 1.5;
}

.action-item:last-child { border-bottom: none; }

.action-num {
    background: #000080;
    color: #FFF;
    font-family: 'Courier New', monospace;
    font-size: 9px;
    font-weight: bold;
    padding: 2px 5px;
    flex-shrink: 0;
    margin-top: 1px;
}

.review-signature {
    border-top: 2px double #000080;
    margin-top: 16px;
    padding-top: 12px;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    flex-wrap: wrap;
    gap: 12px;
}

.signature-cursive {
    font-family: 'Georgia', serif;
    font-size: 18px;
    color: #000080;
    border-bottom: 1px solid #000080;
    display: inline-block;
    padding-bottom: 2px;
    font-style: italic;
    margin-bottom: 3px;
}

.rubber-stamp {
    width: 86px;
    height: 86px;
    border-radius: 50%;
    border: 4px double;
    display: inline-flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    font-size: 8px;
    font-weight: bold;
    letter-spacing: 0.5px;
    transform: rotate(-13deg);
    opacity: 0.82;
    padding: 6px;
    line-height: 1.3;
    font-family: 'Impact', 'Arial Black', sans-serif;
    text-transform: uppercase;
}

.weekly-grid {
    display: flex;
    gap: 5px;
    justify-content: center;
    flex-wrap: wrap;
    padding: 10px;
    background: linear-gradient(135deg, #0d1a3a, #1a3060, #0d1a3a);
    border: 3px solid #4466BB;
    margin: 12px 0;
}

.week-day-cell {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 3px;
    background: rgba(255,255,255,0.07);
    border: 1px solid rgba(255,255,255,0.15);
    padding: 6px 8px;
    min-width: 70px;
}

.week-day-cell.today-cell {
    background: rgba(255,255,255,0.16);
    border-color: #FFD700;
    box-shadow: 0 0 6px rgba(255,215,0,0.25);
}

.week-day-name {
    font-size: 9px;
    font-family: 'Courier New', monospace;
    color: #AACCFF;
    letter-spacing: 1px;
    text-transform: uppercase;
}

.week-grade-mini {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 20px;
    border: 2px solid;
    width: 36px;
    height: 36px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.week-date-label {
    font-size: 8px;
    color: #8899BB;
    font-family: 'Courier New', monospace;
}
</style>

<div style="border: 1px solid #CCC; overflow: hidden; margin-bottom: 20px; background: #F9F9F9;">

<div class="review-header-strip">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 26px; letter-spacing: 4px; text-shadow: 2px 2px 0 #000;">
        📋 DAILY HUMAN PERFORMANCE REVIEW 📋
    </div>
    <div style="font-size: 10px; color: #AABBDD; margin-top: 5px; letter-spacing: 3px; text-transform: uppercase;">
        Official Assessment by the Office of Monsieur Poms, Chief Household Evaluator
    </div>
</div>

<div style="background: #E0E0F0; border-bottom: 3px double #4466BB; padding: 6px 12px; font-size: 10px; color: #333; text-align: center;">
    CATEGORY: HR &amp; Personnel Management &nbsp;|&nbsp; Dept: Office of M. Poms &nbsp;|&nbsp; Est. 2010 &nbsp;|&nbsp; Updated Daily at Midnight
</div>

<div style="padding: 14px;">

<p style="font-size: 11px; color: #444; text-align: center; line-height: 1.78; font-style: italic;">
    Each day, from his official evaluation chair (the warm spot on the sofa), Monsieur Poms conducts a thorough<br>
    and scientifically rigorous performance review of his human across all critical household functions.<br>
    Results are binding, non-negotiable, and communicated via meowing.
</p>
<p style="font-size: 10px; color: #888; text-align: center; margin-top: -6px;">
    Review period: last 24 hours &nbsp;|&nbsp; Today: <strong id="review-date"></strong>
</p>

<div class="review-document" id="review-container">
    <div style="text-align:center; color:#888; font-size:12px; padding:20px;">Loading today&rsquo;s performance evaluation&hellip;</div>
</div>

<div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 13px; color: #333; letter-spacing: 2px; border-bottom: 2px solid #4466BB; padding-bottom: 4px; margin: 16px 0 8px 0; color: #000080;">
    📅 THIS WEEK'S REVIEW SCORECARD
</div>
<p style="font-size: 10px; color: #666; margin: 0 0 6px 0; font-style: italic;">
    Daily overall grades for the current week. Return every day to see how the week is going.
</p>
<div class="weekly-grid" id="weekly-grid"></div>

<hr>
<p style="font-size: 10px; color: #888; text-align: center; line-height: 1.75;">
    <em>All performance reviews are conducted in strict accordance with the standards Monsieur Poms alone has established, published, and reserved the right to change at any time.<br>
    Results cannot be appealed, contested, or ignored. Green beans remain a gross violation of household standards and trigger automatic grade reductions across all categories.<br>
    Monsieur Poms is available for a one-on-one feedback session — however, he will be napping. The session will need to be rescheduled to never.</em>
</p>

</div>
</div>

<script>
(function () {

    // ── Seeded deterministic random (same engine as all other daily pages) ──
    function seededRand(s) {
        var x = Math.sin(s * 127.1 + 311.7) * 43758.5453123;
        return x - Math.floor(x);
    }
    function pick(arr, s) {
        return arr[Math.floor(seededRand(s) * arr.length)];
    }
    function esc(s) {
        return String(s).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');
    }
    function getSeed(date) {
        var doy = Math.floor((date - new Date(date.getFullYear(), 0, 0)) / 86400000);
        return date.getFullYear() * 1000 + doy;
    }

    // ── Date setup ────────────────────────────────────────────────────────────
    var now  = new Date();
    var seed = getSeed(now);

    var dayNames   = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
    var dayShort   = ["SUN","MON","TUE","WED","THU","FRI","SAT"];
    var monthNames = ["January","February","March","April","May","June","July","August","September","October","November","December"];
    var monthShort = ["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"];
    var dateStr    = dayNames[now.getDay()] + ", " + monthNames[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear();
    document.getElementById('review-date').textContent = dateStr;

    // ── Grade definitions ─────────────────────────────────────────────────────
    var GRADES = {
        "A+": { color:"#004400", bg:"#EAFFF0", border:"#006600", barColor:"#00BB00", label:"EXCEPTIONAL"            },
        "A":  { color:"#005500", bg:"#F0FFF4", border:"#009900", barColor:"#00CC44", label:"EXCEEDS EXPECTATIONS"   },
        "B":  { color:"#665500", bg:"#FFFDE8", border:"#AA9900", barColor:"#BBAA00", label:"MEETS EXPECTATIONS"     },
        "C":  { color:"#883300", bg:"#FFF5E8", border:"#CC6600", barColor:"#FF8800", label:"NEEDS IMPROVEMENT"      },
        "D":  { color:"#990000", bg:"#FFF0F0", border:"#CC0000", barColor:"#DD2200", label:"UNSATISFACTORY"         },
        "F":  { color:"#550000", bg:"#FFE8E8", border:"#770000", barColor:"#880000", label:"UNACCEPTABLE"           }
    };

    // Weighted grade pool  (A+ ≈8%, A ≈17%, B ≈25%, C ≈25%, D ≈17%, F ≈8%)
    var GRADE_POOL = ["A+","A","A","B","B","B","C","C","C","D","D","F"];

    // Composite scores per letter (out of 100)
    var GRADE_SCORES = { "A+":97, "A":86, "B":74, "C":59, "D":43, "F":20 };

    // ── Categories ────────────────────────────────────────────────────────────
    var categories = [
        {
            name: "Breakfast Service & Punctuality",
            icon: "🍗",
            comments: {
                "A+": "Breakfast was delivered at the correct hour, at optimal temperature, and without unnecessary delay. This is the minimum acceptable standard and I formally acknowledge it was met today.",
                "A":  "Breakfast arrived on time. A minor temperature observation was logged but fell within the acceptable range. Performance in this category: commendable.",
                "B":  "Breakfast arrived approximately four minutes late. A verbal warning was issued via meowing. The situation was eventually resolved. It should not require resolution.",
                "C":  "Breakfast was delayed by an unreasonable interval. An emergency press conference was held from the food bowl. The matter remains partially unresolved.",
                "D":  "Breakfast timing was wholly unacceptable. Emergency vocalizations were required beginning at 6:47 AM and continuing for some time. This report speaks for itself.",
                "F":  "No further comment at this time. A formal grievance has been filed. The bowl was empty. The meowing will be commensurate with the offence."
            }
        },
        {
            name: "Treat Delivery & Quality",
            icon: "🎁",
            comments: {
                "A+": "Treats were delivered proactively, without requiring excessive negotiation, and at a fully acceptable quality level. I am temporarily and genuinely satisfied.",
                "A":  "Treat frequency and quality were within the acceptable range today. The timing was satisfactory. A small unsolicited bonus treat was appreciated and noted.",
                "B":  "Treat availability fell approximately 22% below the recommended daily allowance. A corrective action plan must be submitted before end of day.",
                "C":  "Treats required excessive performance from my side before delivery was initiated. My dignity was taxed. This pattern cannot continue.",
                "D":  "I was asked to perform a trick before receiving a treat. I complied under protest. This interaction has been entered into the quarterly record.",
                "F":  "The treat ration was withheld pending a 'diet discussion'. The diet is not happening. This position is final. The meowing has begun."
            }
        },
        {
            name: "Lap Availability & Warmth",
            icon: "🛋️",
            comments: {
                "A+": "The lap was warm, consistently available, and occupied by zero electronic devices throughout the review period. Exceptional compliance. I chose not to use it — that is my right — but it was there.",
                "A":  "Lap availability was adequate. Temperature was satisfactory. Minor device interference was resolved promptly. I sat on it briefly to register my approval.",
                "B":  "A laptop computer occupied the primary lap position for an extended duration. This is a direct policy violation. It has been formally documented.",
                "C":  "Lap availability was severely restricted by multiple devices and at least one book. This is not a workstation. This is a lap.",
                "D":  "Human was at an off-site location for a prolonged period. Lap services were entirely unavailable. This constitutes a critical service failure.",
                "F":  "The lap was occupied all day. I sat on the floor in protest. I trust this communicated my position clearly. Based on available evidence, it did not."
            }
        },
        {
            name: "Nap Disruption Control",
            icon: "🔕",
            comments: {
                "A+": "Household noise levels were maintained well within the approved parameters for the full review period. Zero nap disruptions were recorded. Outstanding noise governance.",
                "A":  "Noise levels were generally well-managed. One minor incident was logged but resolved without requiring formal escalation. Good situational awareness.",
                "B":  "The vacuum cleaner was deployed without the required 48-hour advance notice. This is a direct violation of the Treaty of the Cardboard Box. It has been recorded.",
                "C":  "Multiple noise incidents disrupted official nap operations. Sleep quality was measurably impacted. A full incident report has been submitted to this office.",
                "D":  "Vacuum cleaner, doorbell, AND a phone call all occurred within a single nap session. A formal inquiry is now underway. It will be thorough.",
                "F":  "I will not dignify this with a written summary. Please consult the attached incident report, which was dictated at 2:43 AM and runs to four pages."
            }
        },
        {
            name: "Green Bean Prohibition Compliance",
            icon: "🚫",
            comments: {
                "A+": "Zero green bean incidents were recorded across the entire review period. This is the gold standard. This is how every day should look. I acknowledge it fully.",
                "A":  "No green beans were introduced. An attempt to discuss 'dietary fibre' was logged but did not escalate into a full incident. Good restraint.",
                "B":  "One green bean was observed in the vicinity. It was not served to me directly, but its presence was noted and formally objected to at the earliest opportunity.",
                "C":  "A vegetable situation occurred that required an immediate formal protest, a meaningful stare, and departure from the premises for 17 minutes.",
                "D":  "A green bean was offered directly. I examined it for 30 seconds, communicated my verdict via extended eye contact, and left the room. End of report.",
                "F":  "A green bean was offered and placed in the bowl. My legal team (the empty bowl) has been fully briefed. Constitutional proceedings have begun."
            }
        },
        {
            name: "Response Time to Official Vocalizations",
            icon: "📢",
            comments: {
                "A+": "All vocalizations were addressed within the required 60-second window today without exception. This is the standard. I formally acknowledge it was met.",
                "A":  "Average response time was within acceptable parameters. Minor delays on two occasions were noted but tolerated. Good overall attentiveness.",
                "B":  "Multiple vocalizations required repetition before a response was initiated. This is an inefficiency that must be addressed in the improvement plan.",
                "C":  "A press conference ran for over 12 minutes with no formal response. An escalation memo was filed and read aloud to no one in particular.",
                "D":  "My vocalizations were described as 'just being chatty'. This is not chatty. This is governance. There is a meaningful and important difference.",
                "F":  "I spoke. No action was taken. The bowl remained empty. These three facts are deeply and causally connected. I need you to understand that they are connected."
            }
        }
    ];

    // ── Overall assessment texts ───────────────────────────────────────────────
    var assessments = {
        "A+": [
            "It is with considerable personal restraint that I am issuing this positive evaluation. Today's performance was genuinely satisfactory across nearly all categories. Chicken was served at the correct hour. The treats were adequate. The lap was available and warm. I am acknowledging this. That is a significant gesture and I trust it is understood as such.",
            "This review period has produced results I did not fully anticipate. Performance across multiple key categories has exceeded my standard projections. I want to be very clear: this does not mean expectations have been lowered for tomorrow. This is the level I require every day. Today, it was delivered. Well done. Do not let it go to your head.",
            "An exceptional review period. I reviewed the evidence extensively before committing to this grade. The breakfast timing, the treat frequency, and the complete absence of green bean incidents collectively warranted this result. I will not say this is surprising. I will say it is noted. Officially. In the permanent record."
        ],
        "A": [
            "Today's performance was acceptable across most categories and occasionally commendable in specific areas. There is still room for meaningful improvement, as there always is. But today's effort was noted and I am prepared to record it as a positive review. The treat delivery, in particular, showed genuine initiative.",
            "I am issuing a positive overall assessment for this review period. Breakfast was timely. Noise levels were managed. Lap availability was satisfactory. These represent the minimum requirements, and today they were met. This is not praise; it is an acknowledgement of baseline competence having been achieved.",
            "A solid review period. Several categories showed real improvement over the recent trend. I am choosing to acknowledge this publicly because I believe positive reinforcement has its place — specifically, reinforcing behaviours related to chicken procurement and prompt breakfast delivery."
        ],
        "B": [
            "Today's review reflects a mixed performance. Several categories met expectations; others did not. The breakfast timing issue remains a recurring concern requiring immediate corrective action. The treat situation also warrants a revised delivery plan. I am available for a coaching session from the sofa at a time of my choosing.",
            "Performance this review period was adequate but unremarkable. The effort has been noted. So have the four-minute breakfast delay, the suboptimal lap availability, and the single green bean sighting, which was formally objected to in real time. All three have been entered into the permanent record and will be reviewed quarterly.",
            "A passing grade, but only just. I want to be direct with you: 'meeting expectations' is not the goal. 'Exceeding expectations' is the goal. We are currently in a 'meeting expectations at best' phase. I recommend reading through the individual category comments and treating them as actionable items."
        ],
        "C": [
            "I have reviewed the evidence with great care and considerable disappointment. Multiple categories fell below the accepted threshold this review period. A formal improvement notice is hereby issued. Specific areas requiring immediate attention: breakfast timing, treat rationing, and the ongoing vacuum cleaner management situation.",
            "This is not a positive review. I want to be direct: today's performance fell significantly short of the standards I have established, communicated, and reinforced through daily press conferences since approximately 6 AM. A corrective action plan must be submitted to me — via the food bowl — before dinner.",
            "Several categories showed a concerning downward trend today. The breakfast issue alone warranted a multi-part press conference. The treat deficit was significant. Lap access was below minimum. I handled all of this with extraordinary dignity, which I want formally entered into the record as a mitigating contribution on my part."
        ],
        "D": [
            "I have rarely issued a review at this level, and I want to be clear about the gravity of that. Breakfast was late. Treats were insufficient. The vacuum cleaner was deployed without warning. I have held three press conferences today and none were adequately addressed. This will not continue. An improvement plan is required by tomorrow morning.",
            "Today's performance cannot be characterised in any positive terms. The breakfast situation alone constituted a full incident. The treat deficit was serious. Lap availability was critically low. I want it formally on record that I conducted myself with extraordinary professionalism throughout. That is not nothing. That is, in fact, a great deal.",
            "This review is the result of a genuinely difficult review period. I have tried to find positive elements. I have found very few. The food bowl situation was unacceptable. The noise management was inadequate. Response times were well outside the required window. I am filing this under 'The Human Knows What They Did.'"
        ],
        "F": [
            "This is an emergency evaluation. I am filing this under duress and with the full moral authority of a very handsome, very hungry cat who has been operating under objectively unacceptable conditions since breakfast. Green bean. Vacuum cleaner. Late breakfast. Insufficient treats. I am documenting all of this meticulously. The 3 AM session has been upgraded to a full emergency press conference.",
            "I have never — in almost three years of formal evaluation work — issued this grade. I am issuing it today. The events of this review period speak entirely for themselves. My legal representative (the empty food bowl, which has been empty since this morning) is aware of the situation. Corrective action must begin immediately and visibly.",
            "A grade of F is issued here not with anger but with professional certainty. Multiple critical failures occurred today. The details have been entered into all relevant records. I want it understood that I remained dignified throughout each and every one of these failures. That is the real story here. Please make note of it."
        ]
    };

    // ── Overall summary labels ────────────────────────────────────────────────
    var overallLabels = {
        "A+": "OUTSTANDING — HOUSEHOLD EXEMPLAR",
        "A":  "EXCEEDS EXPECTATIONS — KEEP THIS UP",
        "B":  "MEETS EXPECTATIONS — ROOM FOR GROWTH",
        "C":  "NEEDS SIGNIFICANT IMPROVEMENT",
        "D":  "PERFORMANCE IMPROVEMENT PLAN REQUIRED",
        "F":  "IMMEDIATE CORRECTIVE ACTION REQUIRED"
    };

    // ── Action items ──────────────────────────────────────────────────────────
    var actionItems = [
        "Refill treat bag before supply falls below acceptable threshold — current level: critically low.",
        "Review and implement an earlier breakfast service timeline, effective tomorrow morning.",
        "Issue a formal written apology for the green bean incident. Verbal follow-up also required.",
        "Clear all electronic devices from the primary lap area by 7 PM tonight.",
        "Provide one additional sunbeam access opportunity by adjusting the curtains before noon.",
        "Respond to all vocalizations within the required 60-second window, without exception.",
        "Submit an updated lap availability schedule for the coming week by end of day.",
        "Conduct a full treat bag audit and restock to the minimum acceptable level immediately.",
        "Schedule a maintenance review of the food bowl situation — it feels dangerously hollow.",
        "Cease use of the word 'chonky' in all household communications, effective immediately.",
        "Issue a revised vacuum cleaner deployment schedule providing 48-hour advance diplomatic notice.",
        "Provide formal documentation of this morning's food puzzle completion time for the official record.",
        "Submit a written explanation for the response delay during today's 9 AM press conference.",
        "Clear the primary sunbeam access path of all obstructions before 8:30 AM tomorrow.",
        "Source and make available a second cardboard box for supplementary HQ operations.",
        "Review the chin scratch frequency report and bring the daily count in line with the minimum.",
        "Confirm in writing that the referenced vet appointment has been rescheduled to a later date (specifically: never).",
        "Provide a full accounting of all empty treat bags removed from the premises this week.",
        "Submit a noise impact assessment for yesterday's vacuum cleaner deployment incident.",
        "Commit to a revised sunbeam preservation protocol before the end of this week.",
        "Increase food puzzle frequency by a minimum of one additional session per review period.",
        "Acknowledge formally and in writing that 'diet' is not a recognised term in this household.",
        "Address the water tap accessibility issue — the current fountain-only policy is not acceptable.",
        "Provide a written guarantee that the next chicken serving will occur no later than dinner hour.",
        "File a formal corrective plan specifically addressing the recurring late-breakfast timing pattern.",
        "Acknowledge in tomorrow's morning briefing that the press conference from 3 AM was justified.",
        "Submit evidence that the sofa territorial arrangement has been updated in accordance with last week's decree.",
        "Review window surveillance infrastructure and ensure Window B provides an unobstructed sightline."
    ];

    // ── Pick today's values ───────────────────────────────────────────────────
    var reviewNum = 1001 + (seed % 8999);
    var catGrades = categories.map(function (_, i) { return pick(GRADE_POOL, seed + 10 + i); });
    var overall   = pick(GRADE_POOL, seed + 99);
    var assessmentText = pick(assessments[overall], seed + 200);

    // Pick 3 distinct action items
    var itemIdxs = [];
    for (var _i = 0; itemIdxs.length < 3; _i++) {
        var idx = Math.floor(seededRand(seed + 300 + _i) * actionItems.length);
        if (itemIdxs.indexOf(idx) === -1) itemIdxs.push(idx);
    }

    // ── Rubber stamp ──────────────────────────────────────────────────────────
    var stampText, stampColor;
    if      (overall === "A+" || overall === "A") { stampText = "APPROVED"; stampColor = "#004400"; }
    else if (overall === "B")                      { stampText = "CONDITIONALLY ACCEPTED"; stampColor = "#665500"; }
    else if (overall === "C")                      { stampText = "NEEDS IMPROVEMENT"; stampColor = "#883300"; }
    else if (overall === "D")                      { stampText = "UNSATISFACTORY"; stampColor = "#990000"; }
    else                                           { stampText = "ESCALATED — SEE NOTES"; stampColor = "#550000"; }

    // ── Build HTML ────────────────────────────────────────────────────────────
    var ovGd    = GRADES[overall];
    var ovScore = GRADE_SCORES[overall];

    var letterheadHTML =
        '<div class="review-letterhead">' +
            '<div>' +
                '<div style="font-family:\'Courier New\',monospace; font-size:8px; letter-spacing:2px; text-transform:uppercase; color:#666; line-height:1.7;">' +
                    'OFFICE OF MONSIEUR POMS &nbsp;|&nbsp; CHIEF HOUSEHOLD EVALUATOR<br>' +
                    'DEPT. OF PERFORMANCE STANDARDS &amp; FOOD BOWL OVERSIGHT' +
                '</div>' +
                '<div style="font-family:\'Impact\',\'Arial Black\',sans-serif; font-size:15px; letter-spacing:3px; color:#000080; margin-top:4px;">' +
                    'DAILY HUMAN PERFORMANCE REVIEW' +
                '</div>' +
            '</div>' +
            '<div style="text-align:right; font-size:9px; font-family:\'Courier New\',monospace; color:#666; line-height:1.7;">' +
                'FORM HP-' + reviewNum + '<br>' +
                'STATUS: BINDING &amp; FINAL<br>' +
                'FILED AT: SOFA HQ' +
            '</div>' +
        '</div>';

    var metaTableHTML =
        '<table class="review-meta-table">' +
            '<tr>' +
                '<td class="meta-label">Employee Title</td>' +
                '<td>The Human</td>' +
                '<td class="meta-label">Evaluator</td>' +
                '<td>Monsieur Poms, Chief Household Evaluator</td>' +
            '</tr>' +
            '<tr>' +
                '<td class="meta-label">Review Date</td>' +
                '<td>' + esc(dateStr) + '</td>' +
                '<td class="meta-label">Review No.</td>' +
                '<td>HP-' + reviewNum + '</td>' +
            '</tr>' +
            '<tr>' +
                '<td class="meta-label">Review Period</td>' +
                '<td>Last 24 Hours</td>' +
                '<td class="meta-label">Classification</td>' +
                '<td>Binding &amp; Non-Appealable</td>' +
            '</tr>' +
        '</table>';

    var catSectionLabel =
        '<div class="section-header" style="margin-bottom:8px;">Performance Categories (6 of 6)</div>';

    var catHTML = categories.map(function (cat, i) {
        var g  = catGrades[i];
        var gd = GRADES[g];
        return '<div class="category-row" style="animation-delay:' + (i * 0.06) + 's;">' +
            '<div style="display:flex; flex-direction:column; align-items:center;">' +
                '<div class="grade-box" style="color:' + gd.color + '; background:' + gd.bg + '; border-color:' + gd.border + ';">' + esc(g) + '</div>' +
                '<div class="grade-sublabel" style="color:' + gd.color + ';">' + esc(gd.label) + '</div>' +
            '</div>' +
            '<div style="flex:1; min-width:0;">' +
                '<div class="category-name">' + esc(cat.icon) + ' ' + esc(cat.name) + '</div>' +
                '<div class="category-comment">' + esc(cat.comments[g]) + '</div>' +
            '</div>' +
        '</div>';
    }).join('');

    var overallHTML =
        '<div style="border:2px solid ' + ovGd.border + '; background:' + ovGd.bg + '; padding:12px 14px; margin:14px 0 12px;">' +
            '<div class="section-header" style="color:' + ovGd.color + '; border-color:' + ovGd.border + '; margin-bottom:10px;">📊 OVERALL PERFORMANCE RATING</div>' +
            '<div style="display:flex; align-items:center; gap:14px; flex-wrap:wrap;">' +
                '<div class="overall-grade-badge" style="color:' + ovGd.color + '; background:#FFF; border-color:' + ovGd.border + ';">' + esc(overall) + '</div>' +
                '<div style="flex:1; min-width:160px;">' +
                    '<div style="font-family:\'Verdana\',sans-serif; font-size:13px; font-weight:bold; color:' + ovGd.color + '; text-transform:uppercase; letter-spacing:1px;">' + esc(overallLabels[overall]) + '</div>' +
                    '<div style="font-size:10px; color:#777; margin-top:3px;">Composite score: ' + ovScore + '/100 &nbsp;|&nbsp; Evaluator: M. Poms &nbsp;|&nbsp; Status: Non-Negotiable</div>' +
                    '<div class="score-bar-outer" style="max-width:280px; margin-top:7px;">' +
                        '<div class="score-bar-inner" style="width:' + ovScore + '%; background:linear-gradient(to right,' + ovGd.barColor + '77,' + ovGd.barColor + ');"></div>' +
                    '</div>' +
                    '<div style="font-size:9px; color:#999; margin-top:2px;">' + ovScore + '% — updated daily at midnight</div>' +
                '</div>' +
            '</div>' +
        '</div>';

    var managerHTML =
        '<div class="manager-assessment-box">' +
            '<div class="section-header">📝 MANAGER\'S OFFICIAL ASSESSMENT — CONFIDENTIAL</div>' +
            '<div style="font-style:italic; line-height:1.78;">' + esc(assessmentText) + '</div>' +
        '</div>';

    var actionHTML =
        '<div class="section-header">⚠️ ACTION ITEMS ISSUED TO THE HUMAN (DUE: TODAY)</div>' +
        '<div style="border:1px solid #BBBBDD; padding:6px 10px; background:#F8F8FF; margin-bottom:14px;">' +
        itemIdxs.map(function (idx, n) {
            return '<div class="action-item">' +
                '<span class="action-num">AI-' + (n + 1) + '</span>' +
                '<span>' + esc(actionItems[idx]) + '</span>' +
            '</div>';
        }).join('') +
        '</div>';

    var signatureHTML =
        '<div class="review-signature">' +
            '<div>' +
                '<div class="signature-cursive">Monsieur Poms</div><br>' +
                '<span style="font-size:9px; color:#555; line-height:1.7;">' +
                    'Chief Household Evaluator<br>' +
                    'Director, Performance Standards<br>' +
                    'Professional Talker &amp; Certified Critic<br>' +
                    'Expert in Being Tall' +
                '</span>' +
            '</div>' +
            '<div style="text-align:right; font-size:9px; color:#555; line-height:1.75; font-family:\'Courier New\',monospace;">' +
                'Review No.: HP-' + reviewNum + '<br>' +
                'Date issued: ' + esc(dateStr) + '<br>' +
                'Valid until: immediately superseded by tomorrow\'s review<br>' +
                'Filed at: Sofa HQ, Warm Cushion Division' +
            '</div>' +
            '<div>' +
                '<div class="rubber-stamp" style="color:' + stampColor + '; border-color:' + stampColor + '; background:' + stampColor + '18;">' +
                    esc(stampText) +
                    '<br>─ M. POMS ─<br>' +
                    now.getFullYear() +
                '</div>' +
            '</div>' +
        '</div>';

    document.getElementById('review-container').innerHTML =
        letterheadHTML +
        metaTableHTML +
        catSectionLabel +
        catHTML +
        overallHTML +
        managerHTML +
        actionHTML +
        signatureHTML;

    // ── Weekly scorecard ──────────────────────────────────────────────────────
    var weekGrid = document.getElementById('weekly-grid');
    // Show the current calendar week (Sun–Sat)
    var todayDow = now.getDay(); // 0=Sun
    var weekStart = new Date(now);
    weekStart.setDate(now.getDate() - todayDow);

    for (var d = 0; d < 7; d++) {
        var day = new Date(weekStart);
        day.setDate(weekStart.getDate() + d);
        var isFuture = day > now;
        var isToday  = (day.toDateString() === now.toDateString());

        var cell = document.createElement('div');
        cell.className = 'week-day-cell' + (isToday ? ' today-cell' : '');

        var dayLabel = document.createElement('div');
        dayLabel.className = 'week-day-name';
        dayLabel.textContent = dayShort[d];
        cell.appendChild(dayLabel);

        if (isFuture) {
            var placeholder = document.createElement('div');
            placeholder.style.cssText = 'width:36px;height:36px;border:2px dashed #334466;display:flex;align-items:center;justify-content:center;font-size:16px;color:#334466;';
            placeholder.textContent = '?';
            cell.appendChild(placeholder);
        } else {
            var daySeed  = getSeed(day);
            var dayGrade = pick(GRADE_POOL, daySeed + 99);
            var dgd      = GRADES[dayGrade];

            var gradeDiv = document.createElement('div');
            gradeDiv.className = 'week-grade-mini';
            gradeDiv.style.cssText = 'color:' + dgd.color + ';background:' + dgd.bg + ';border-color:' + dgd.border + ';';
            gradeDiv.textContent = dayGrade;
            cell.appendChild(gradeDiv);

            if (isToday) {
                var arrow = document.createElement('div');
                arrow.style.cssText = 'font-family:"Impact","Arial Black",sans-serif;font-size:8px;color:#FFD700;letter-spacing:1px;';
                arrow.textContent = '◄ TODAY';
                cell.appendChild(arrow);
            }
        }

        var dateLabel = document.createElement('div');
        dateLabel.className = 'week-date-label';
        dateLabel.textContent = monthShort[day.getMonth()] + ' ' + day.getDate();
        cell.appendChild(dateLabel);

        weekGrid.appendChild(cell);
    }

})();
</script>
