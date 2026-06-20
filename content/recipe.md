---
title: "Poms' Recipe Box"
---

<style>
.recipe-header-band {
    background: linear-gradient(135deg, #8B1A1A 0%, #CC3300 40%, #FF6600 100%);
    color: #fff;
    padding: 16px 14px;
    margin: -10px -10px 0 -10px;
    border-bottom: 4px double #FFCC00;
    text-align: center;
}
.recipe-site-name {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 30px;
    letter-spacing: 4px;
    text-shadow: 2px 2px 0 #000, -1px -1px 0 rgba(255,200,0,0.4);
    color: #FFD700;
}
.recipe-tagline {
    font-size: 11px;
    letter-spacing: 2px;
    color: #FFDDAA;
    margin-top: 3px;
    font-style: italic;
}
.recipe-nav-bar {
    background: #CC3300;
    border-bottom: 2px solid #FFCC00;
    padding: 4px 8px;
    font-size: 10px;
    color: #FFD;
    margin: 0 -10px 14px -10px;
    font-family: 'Verdana', sans-serif;
}
.recipe-nav-bar a {
    color: #FFEE88;
    text-decoration: underline;
    margin: 0 6px;
}

.recipe-layout {
    display: flex;
    gap: 16px;
    align-items: flex-start;
}
.recipe-main { flex: 1; min-width: 0; }
.recipe-sidebar {
    width: 190px;
    flex-shrink: 0;
}

.recipe-title-section {
    border-bottom: 2px solid #CC3300;
    padding-bottom: 10px;
    margin-bottom: 12px;
}
.recipe-name {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 22px;
    color: #8B1A1A !important;
    text-decoration: none !important;
    margin: 0 0 4px 0;
    text-shadow: 1px 1px 0 rgba(0,0,0,0.1);
    line-height: 1.2;
}
.recipe-category-badge {
    display: inline-block;
    background: #CC3300;
    color: #FFD700;
    font-size: 9px;
    font-weight: bold;
    letter-spacing: 1px;
    padding: 2px 6px;
    font-family: 'Verdana', sans-serif;
    margin-bottom: 6px;
}
.stars {
    color: #FF8C00;
    font-size: 18px;
    letter-spacing: 1px;
}
.star-count {
    font-size: 10px;
    color: #666;
    vertical-align: middle;
    margin-left: 4px;
}

.recipe-quick-info {
    display: flex;
    gap: 0;
    border: 2px solid #CC3300;
    margin: 12px 0;
    font-size: 10px;
    font-family: 'Verdana', sans-serif;
    text-align: center;
}
.rqi-cell {
    flex: 1;
    padding: 7px 4px;
    border-right: 1px solid #CC3300;
}
.rqi-cell:last-child { border-right: none; }
.rqi-label { color: #CC3300; font-weight: bold; font-size: 9px; display: block; letter-spacing: 1px; }
.rqi-value { font-size: 12px; font-weight: bold; color: #333; display: block; margin-top: 2px; }

.story-box {
    background: #FFFDF0;
    border-left: 5px solid #FF6600;
    padding: 10px 12px;
    font-size: 11px;
    line-height: 1.8;
    color: #333;
    margin: 12px 0;
    font-style: italic;
}
.story-author {
    font-size: 10px;
    color: #888;
    text-align: right;
    margin-top: 6px;
    font-style: normal;
}

.section-heading {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 16px;
    color: #8B1A1A !important;
    text-decoration: none !important;
    letter-spacing: 2px;
    border-bottom: 2px solid #CC3300;
    padding-bottom: 3px;
    margin: 16px 0 8px;
}

.ingredients-list {
    margin: 0;
    padding: 0;
    list-style: none;
    font-size: 11px;
    line-height: 1.9;
}
.ingredients-list li::before {
    content: "☑ ";
    color: #CC3300;
}

.steps-list {
    padding-left: 0;
    list-style: none;
    counter-reset: step-counter;
    margin: 0;
}
.steps-list li {
    counter-increment: step-counter;
    padding: 8px 10px 8px 40px;
    position: relative;
    font-size: 11px;
    line-height: 1.7;
    border-bottom: 1px dotted #ccc;
    color: #333;
}
.steps-list li::before {
    content: counter(step-counter);
    position: absolute;
    left: 6px;
    top: 8px;
    width: 24px;
    height: 24px;
    background: #CC3300;
    color: #FFD700;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 14px;
    border-radius: 50%;
    text-align: center;
    line-height: 24px;
}

.poms-verdict-box {
    background: linear-gradient(135deg, #001050 0%, #003399 100%);
    border: 3px double #FFCC00;
    color: #fff;
    padding: 12px;
    margin: 16px 0;
    box-shadow: 4px 4px 0 #000;
}
.poms-verdict-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 14px;
    color: #FFD700;
    letter-spacing: 2px;
    margin-bottom: 8px;
}
.poms-verdict-stars { color: #FFD700; font-size: 20px; margin-bottom: 6px; }
.poms-verdict-text { font-size: 12px; font-style: italic; line-height: 1.6; color: #AACCFF; }
.poms-verdict-sig { font-size: 9px; color: #88AADD; text-align: right; margin-top: 8px; border-top: 1px solid #335; padding-top: 5px; }

.comments-section { margin-top: 18px; }
.comment-box {
    border: 1px solid #ddd;
    padding: 8px 10px;
    margin-bottom: 8px;
    background: #FAFAFA;
    font-size: 11px;
}
.comment-author {
    font-weight: bold;
    color: #CC3300;
    font-size: 10px;
}
.comment-date { font-size: 9px; color: #999; margin-left: 6px; }
.comment-text { margin-top: 4px; line-height: 1.6; color: #333; }
.comment-rating { color: #FF8C00; font-size: 13px; }

/* Sidebar */
.sb-card {
    border: 2px solid #CC3300;
    margin-bottom: 12px;
    font-size: 10px;
    font-family: 'Verdana', sans-serif;
}
.sb-card-title {
    background: #CC3300;
    color: #FFD700;
    font-weight: bold;
    padding: 4px 6px;
    font-size: 10px;
    letter-spacing: 1px;
    font-family: 'Impact', 'Arial Black', sans-serif;
}
.sb-card-body { padding: 8px 8px; }

.nutrition-row {
    display: flex;
    justify-content: space-between;
    padding: 3px 0;
    border-bottom: 1px dotted #ccc;
    font-size: 10px;
}
.nutrition-row:last-child { border-bottom: none; }
.nutrition-label { color: #555; }
.nutrition-value { font-weight: bold; color: #333; }

.print-btns {
    margin: 12px 0;
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
}
.print-btn {
    background: linear-gradient(to bottom, #f1f1f1, #d8d8d8);
    border: 2px outset #aaa;
    font-size: 9px;
    padding: 4px 8px;
    cursor: pointer;
    font-family: 'Verdana', sans-serif;
    font-weight: bold;
    color: #333;
    text-decoration: none;
}
.print-btn:hover { background: linear-gradient(to bottom, #FFFF99, #FFEE00); }

@keyframes recipeFadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to   { opacity: 1; transform: translateY(0); }
}
.recipe-content { animation: recipeFadeIn 0.5s ease-out; }
</style>

<div style="border: 1px solid #CCC; padding: 10px; background: #F9F9F9; margin-bottom: 20px;">

<div class="recipe-header-band">
    <div class="recipe-site-name">🍽️ POMS RECIPE BOX 🍽️</div>
    <div class="recipe-tagline">DAILY RECIPES FROM THE KITCHEN OF MONSIEUR POMS · EST. 2010 · CERTIFIED DELICIOUS*</div>
    <div style="font-size: 9px; color: #FFDDAA; margin-top: 2px;">*Certification pending human compliance. Green beans not included. Ever.</div>
</div>

<div class="recipe-nav-bar">
    <a href="#">Home</a> &gt;
    <a href="#">Cat Cuisine</a> &gt;
    <span id="breadcrumb-title" style="color:#fff;">Loading...</span>
    <span style="float:right;">📅 Recipe of the Day — Updates at Midnight</span>
</div>

<div class="recipe-content" id="recipe-content">

<div class="recipe-layout">
<div class="recipe-main">

    <div class="recipe-title-section">
        <div class="recipe-category-badge" id="recipe-category">LOADING...</div>
        <h2 class="recipe-name" id="recipe-name">Loading today's recipe...</h2>
        <div>
            <span class="stars" id="recipe-stars">★★★★★</span>
            <span class="star-count" id="recipe-star-count">(loading reviews)</span>
        </div>
        <div style="font-size: 10px; color: #666; margin-top: 4px; font-style: italic;" id="recipe-submitted">
            Submitted by: <strong>M. Poms</strong> | <span id="recipe-date"></span>
        </div>
    </div>

    <div class="print-btns">
        <a class="print-btn" onclick="alert('The printer is judging you. Also Monsieur Poms does not own a printer.')">🖨️ Print Recipe</a>
        <a class="print-btn" onclick="alert('Email sent! Poms will follow up with a formal complaint if you make this wrong.')">📧 Email to a Friend</a>
        <a class="print-btn" onclick="alert('Recipe saved! Poms expects a review within 48 hours.')">💾 Save Recipe</a>
        <a class="print-btn" onclick="alert('Shopping list generated. Reminder: NO green beans.')">🛒 Shopping List</a>
    </div>

    <div class="recipe-quick-info">
        <div class="rqi-cell">
            <span class="rqi-label">PREP TIME</span>
            <span class="rqi-value" id="rqi-prep">—</span>
        </div>
        <div class="rqi-cell">
            <span class="rqi-label">COOK TIME</span>
            <span class="rqi-value" id="rqi-cook">—</span>
        </div>
        <div class="rqi-cell">
            <span class="rqi-label">TOTAL TIME</span>
            <span class="rqi-value" id="rqi-total">—</span>
        </div>
        <div class="rqi-cell">
            <span class="rqi-label">SERVINGS</span>
            <span class="rqi-value" id="rqi-servings">—</span>
        </div>
        <div class="rqi-cell">
            <span class="rqi-label">DIFFICULTY</span>
            <span class="rqi-value" id="rqi-difficulty">—</span>
        </div>
    </div>

    <div class="story-box" id="recipe-story"></div>

    <div class="section-heading">📋 INGREDIENTS</div>
    <ul class="ingredients-list" id="recipe-ingredients"></ul>

    <div class="section-heading">📖 DIRECTIONS</div>
    <ol class="steps-list" id="recipe-steps"></ol>

    <div class="poms-verdict-box">
        <div class="poms-verdict-title">⭐ POMS' OFFICIAL VERDICT</div>
        <div class="poms-verdict-stars" id="verdict-stars">★★★★★</div>
        <div class="poms-verdict-text" id="verdict-text">Loading...</div>
        <div class="poms-verdict-sig">— Monsieur Poms, Executive Chef & Food Critic · Poms Recipe Box</div>
    </div>

    <div class="comments-section">
        <div class="section-heading">💬 COMMUNITY REVIEWS</div>
        <div id="comments-container"></div>
        <div style="background:#FFFFF0; border: 2px dashed #CC3300; padding: 8px; font-size: 10px; color: #666; text-align: center; margin-top: 8px;">
            <strong>Leave a Review!</strong><br>
            <em style="font-size:9px;">Note: All reviews are moderated by Monsieur Poms personally.
            Reviews mentioning green beans will be deleted. Reviews calling him "chonky" will result in the Disappointed Eyes.</em>
        </div>
    </div>

</div>
<div class="recipe-sidebar">

    <div class="sb-card">
        <div class="sb-card-title">📊 NUTRITION FACTS</div>
        <div class="sb-card-body">
            <div style="font-size: 9px; color: #888; margin-bottom: 6px; font-style: italic;">Per serving · Approximate · Not evaluated by any real authority</div>
            <div id="nutrition-container"></div>
        </div>
    </div>

    <div class="sb-card">
        <div class="sb-card-title">🐾 CHEF'S NOTES</div>
        <div class="sb-card-body" id="chef-notes" style="line-height: 1.7; color: #333;"></div>
    </div>

    <div class="sb-card">
        <div class="sb-card-title">📅 RECIPE ARCHIVE</div>
        <div class="sb-card-body">
            <div style="color: #555; line-height: 1.9;" id="archive-list"></div>
            <div style="font-size: 9px; color: #999; margin-top: 6px; text-align: right; font-style: italic;">20 recipes in rotation</div>
        </div>
    </div>

    <div class="sb-card">
        <div class="sb-card-title">⚠️ DISCLAIMER</div>
        <div class="sb-card-body" style="font-size: 9px; color: #555; line-height: 1.7; font-style: italic;">
            Monsieur Poms is not a licensed chef, nutritionist, or food safety inspector.
            He is, however, extremely opinionated about food. Results may vary.
            Do not attempt the "Counter Method" without first distracting the human.
            Poms Recipe Box is not responsible for any fur in your meal.
        </div>
    </div>

</div>
</div>

</div>

<hr>
<p style="font-size: 10px; color: #888; text-align: center;">
    <em>🍽️ Poms Recipe Box · New recipe posted daily at midnight · All recipes tested personally by Monsieur Poms<br>
    © Monsieur Poms International Cuisine Corp. · Green beans banned by executive order since 2023</em>
</p>

</div>

<script>
(function () {

    function seededRand(s) {
        var x = Math.sin(s * 127.1 + 311.7) * 43758.5453123;
        return x - Math.floor(x);
    }
    function getDayOfYear(d) {
        return Math.floor((d - new Date(d.getFullYear(), 0, 0)) / 86400000);
    }

    var now  = new Date();
    var doy  = getDayOfYear(now);
    var seed = now.getFullYear() * 1000 + doy;

    var months = ["January","February","March","April","May","June","July","August","September","October","November","December"];
    var days   = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
    var dateStr = days[now.getDay()] + ", " + months[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear();

    var recipes = [
        {
            name: "Chicken From The Counter",
            category: "COUNTER CUISINE",
            stars: 5,
            reviewCount: 1247,
            prep: "3 min",
            cook: "0 min",
            total: "3 min",
            servings: "1 Monsieur",
            difficulty: "Moderate",
            story: "This recipe has been passed down through generations of ceiling cat ancestors and represents the pinnacle of feline culinary achievement. The Counter Method requires patience, precision, and a human who has briefly left the kitchen. I have made this recipe approximately 47 times. I have been caught approximately 47 times. The results, however, speak for themselves. The chicken tastes significantly better when acquired this way — I believe it is the thrill that adds flavour. My humans disagree, but they are not professional food critics like myself.",
            ingredients: [
                "1 piece of chicken (any cut — I am not picky)",
                "1 briefly unattended kitchen counter",
                "1 pair of silent paws (mine)",
                "1 distraction event (knocking something off elsewhere works well)",
                "Confidence (generous amount)",
                "An exit strategy"
            ],
            steps: [
                "Identify the target. Assess counter height. Confirm human distraction level.",
                "Create a diversion in another room. I recommend knocking a pen off a desk — small, effective, believable.",
                "Approach the counter at low speed. Do not run. Running implies guilt. Walk like you own the place, because you do.",
                "Acquire the chicken with one swift, elegant motion. No hesitation.",
                "Relocate to a secure location (under the bed, behind the couch) for consumption.",
                "When discovered, deploy the Innocent Face. Maintain for a minimum of 3 minutes.",
                "If pressed, look pointedly at the dog (if applicable). If no dog is available, stare at a wall."
            ],
            verdict: 5,
            verdictText: "Five stars. Would acquire again. The preparation is minimal, the reward is maximum. This is the recipe by which all others are judged. The counter chicken is not just a meal — it is a philosophy.",
            notes: "Best served immediately upon acquisition. Do not share. Pairs well with a sunbeam and the distant sound of human sighing.",
            nutrition: [
                { label: "Satisfaction", value: "100%" },
                { label: "Guilt", value: "0g" },
                { label: "Chicken Content", value: "100%" },
                { label: "Green Beans", value: "0 (never)" },
                { label: "Calories", value: "Not relevant" }
            ],
            comments: [
                { user: "TabbyMcFloof", rating: 5, date: "March 3, 2024", text: "Made this last Tuesday. The diversion technique worked perfectly. I knocked over a glass of water (cold — I do not recommend this approach but it worked). 10/10 would use the counter method again." },
                { user: "OrangeMenaceXX", rating: 5, date: "January 18, 2024", text: "The Innocent Face step is crucial. I held it for 4 minutes and the human just sighed and gave me more chicken anyway. This recipe delivers on every level." },
                { user: "WhiskerProfessor", rating: 4, date: "November 5, 2023", text: "Excellent technique. Deducting one star because my human now puts the chicken on a higher shelf. I am working on a revised strategy for Q1." }
            ]
        },
        {
            name: "3 AM Breakfast Complaint (Vocal Edition)",
            category: "BREAKFAST · URGENT",
            stars: 5,
            reviewCount: 3891,
            prep: "0 min",
            cook: "20 min",
            total: "20 min",
            servings: "Until Bowl Is Filled",
            difficulty: "Easy",
            story: "There is a moment, every single night, somewhere between 2:47 AM and 3:15 AM, when I become aware — with great clarity and moral certainty — that my food bowl is not full enough. It may be technically not empty. It may even be mostly full. This is irrelevant. The bowl situation is a matter of principle, not logistics. This recipe has been refined over approximately 900 nights and achieves consistent results: the bowl gets filled, I get fed, and the household is reminded of who is in charge. The recipe requires no ingredients beyond conviction and an excellent set of lungs, both of which I possess in abundance.",
            ingredients: [
                "1 mostly-but-not-satisfactorily-full food bowl",
                "Deeply held convictions about bowl fullness",
                "A human who is asleep (required — this only works at 3 AM)",
                "A hallway (for acoustics)",
                "Lung capacity (maximum)",
                "No sense of shame whatsoever"
            ],
            steps: [
                "Wake at approximately 3 AM. Survey the bowl situation. Determine it is unacceptable.",
                "Begin with a soft, mournful meow from the kitchen. This is the warm-up.",
                "Move to the hallway. The hallway has excellent acoustics. Position yourself outside the bedroom door.",
                "Escalate to a full, sustained meow. Hold for 4–6 seconds. Pause. Repeat.",
                "If no response after 3 minutes, add a paw under the door. Subtle, yet effective.",
                "Upon human emergence, lead them directly to the bowl. Do not detour.",
                "Supervise the refill. Sniff the new portion. Accept it, but maintain a look of mild disapproval.",
                "Return to sleep immediately. Leave the human to figure out how to sleep again."
            ],
            verdict: 5,
            verdictText: "The most reliable recipe in my collection. Five stars, every time. The bowl gets filled. The system works. I have never once gone to bed hungry after deploying this technique.",
            notes: "Do not feel guilty. The bowl situation is not your fault. Consistency is key — the human must understand this is a nightly protocol.",
            nutrition: [
                { label: "Bowl Status", value: "FILLED" },
                { label: "Human Sleep", value: "Disrupted" },
                { label: "My Sleep", value: "Excellent" },
                { label: "Satisfaction", value: "Complete" },
                { label: "Regret", value: "None (0g)" }
            ],
            comments: [
                { user: "NocturnalVocalVince", rating: 5, date: "April 12, 2024", text: "I have been using this recipe nightly for two years. Not a single failure. The hallway acoustics tip is genuinely game-changing. I was previously operating from the kitchen — the results are significantly better from the corridor." },
                { user: "MidnightMeowlord", rating: 5, date: "February 2, 2024", text: "Five stars. I would give six if I could. My human now just gets up preemptively. I have trained them well. Thank you Monsieur Poms." },
                { user: "HungryAtDawn", rating: 4, date: "December 1, 2023", text: "Works every time. Deducting one star because sometimes my human gives me the WRONG flavour at 3 AM and then I have to start the complaint process again. Minor issue." }
            ]
        },
        {
            name: "The Perfect Loaf (No-Bake)",
            category: "MEDITATIVE CUISINE",
            stars: 5,
            reviewCount: 2103,
            prep: "0 min",
            cook: "Indefinite",
            total: "Until Disturbed",
            servings: "1 Loaf",
            difficulty: "Very Easy",
            story: "The loaf is not a recipe so much as a state of being. It requires no ingredients, no equipment, and almost no effort — which is why it is, in my professional opinion, the greatest culinary achievement in the history of food. The loaf is achieved when all four paws are tucked fully beneath the body, the tail is wrapped with precision around the perimeter, and the overall silhouette resembles a warm, orange bread product. I have been perfecting my loaf since I was approximately four months old and I believe I have now achieved total mastery. Do not tap the loaf. Do not say my name during the loaf. The loaf is sacred.",
            ingredients: [
                "1 warm surface (heated blanket preferred; sunbeam acceptable)",
                "4 tucked paws (all of them — no exceptions)",
                "1 wrapped tail (precision placement required)",
                "Eyes: closed, or at 20% open for ambient surveillance",
                "A general aura of contentment",
                "Absolutely nothing else"
            ],
            steps: [
                "Locate the optimal surface. Warm is mandatory. The human's laptop is acceptable if no other heat source is available.",
                "Circle the spot 3–7 times. This is not superstition — this is calibration.",
                "Lower the body slowly. Do not flop — the loaf requires dignity.",
                "Tuck all four paws under the torso simultaneously. This is the critical step.",
                "Arrange the tail. The tail must complete the loaf outline. No dangling.",
                "Close eyes to exactly 90%. Maintain ambient awareness at 10%.",
                "Hold this position until disturbed. Duration target: 2–6 hours minimum.",
                "If anyone approaches and says 'aww', tolerate it once. Then give the Look."
            ],
            verdict: 5,
            verdictText: "Five stars. The loaf is perfect. I am perfect. This needs no further comment.",
            notes: "The loaf pairs exceptionally well with silence. Do not disturb the loaf. I will know.",
            nutrition: [
                { label: "Comfort", value: "Maximum" },
                { label: "Effort Required", value: "Near Zero" },
                { label: "Cuteness Output", value: "Off Charts" },
                { label: "Disturbances", value: "0 (goal)" },
                { label: "Floof Factor", value: "98%" }
            ],
            comments: [
                { user: "LoafEnthusiast99", rating: 5, date: "May 7, 2024", text: "I have been loafing for three years and thought I had nothing to learn. The tail placement advice here elevated my loaf to a completely new level. I am now technically a bread." },
                { user: "TuckedAndProud", rating: 5, date: "March 19, 2024", text: "The human said 'aww' four times today. I gave the Look twice. By the third time, they had learned. The system works." },
                { user: "SofaSovereign", rating: 5, date: "January 30, 2024", text: "Outstanding recipe. I particularly appreciate the note about the laptop as a heat source. Very relatable and practical guidance." }
            ]
        },
        {
            name: "Strategic Treat Extraction (Disappointed Eyes Method)",
            category: "ADVANCED MANIPULATION",
            stars: 5,
            reviewCount: 4412,
            prep: "5 min",
            cook: "0 min",
            total: "5–15 min",
            servings: "As Many Treats As Possible",
            difficulty: "Expert",
            story: "Over the course of my career, I have developed many techniques for obtaining treats. The Loud Method (meowing directly at the treat bag) has a moderate success rate. The Trip Method (walking underfoot near the kitchen) works but is inconsistent. The Paw-On-Knee Request has a reasonable success rate in the evenings. But the Disappointed Eyes Method — the technique I am sharing today — has a success rate that I conservatively estimate at 97.3%. It requires significant practice and an exceptional level of facial control, but once mastered, it is essentially a treat-printing machine. The key insight: the human does not feel guilty when you ask for treats. They feel guilty when you look like you have accepted that you will never get treats, and this is simply the way of the world.",
            ingredients: [
                "1 treat bag (location: known)",
                "2 eyes (required)",
                "The Disappointed Expression (see technique notes below)",
                "A strategic location (near the human, slightly to their left)",
                "Patience (approximately 90 seconds)",
                "A single, quiet, resigned sigh (optional but very effective)"
            ],
            steps: [
                "Approach the human at a calm walk. No urgency. Urgency signals desire; desire gives them power.",
                "Sit exactly 40cm away. Not begging distance. Thinking distance.",
                "Make eye contact. Hold for 2 seconds. Then look just slightly away — not fully away, not at them. At the middle distance.",
                "Deploy the Disappointed Eyes. This is not sad. Not pleading. It is the face of someone who expected better of this world.",
                "Maintain complete stillness. Do not meow. Do not paw at anything. Simply exist, looking like a small, overlooked philosopher.",
                "The optional sigh can be deployed at the 60-second mark if progress is slow.",
                "When the human reaches for the treat bag, do not react visibly. Stand up with measured dignity.",
                "Accept the treats. Eat them. Do not overreact. You expected this. It was, in fact, inevitable."
            ],
            verdict: 5,
            verdictText: "My greatest work. Five stars without hesitation. If I could only keep one recipe, it would be this one. The treat yield is extraordinary and the technique is psychologically elegant.",
            notes: "The Disappointed Eyes are not performed — they are inhabited. You must truly feel that the treat situation is a reflection of deeper cosmic injustice. The human will sense if you are faking it.",
            nutrition: [
                { label: "Treats Obtained", value: "Maximum" },
                { label: "Effort", value: "Minimal" },
                { label: "Human Guilt", value: "High" },
                { label: "My Dignity", value: "Fully Intact" },
                { label: "Success Rate", value: "97.3%" }
            ],
            comments: [
                { user: "ManipulateMeTimbers", rating: 5, date: "June 3, 2024", text: "I was skeptical. I am no longer skeptical. The Disappointed Eyes work better than anything I have ever tried, including directly sitting on the treat bag." },
                { user: "SilentJudgementCat", rating: 5, date: "April 25, 2024", text: "The note about inhabiting the face rather than performing it is genuinely transformative advice. I went from 3-4 treats per session to 7-10. Life-changing." },
                { user: "TreatEngineer", rating: 4, date: "February 14, 2024", text: "Excellent technique. Deducting one star only because my humans have started buying the small treats instead of the big ones, which I believe is a countermeasure. I am developing a response strategy." }
            ]
        },
        {
            name: "Sunbeam-Marinated Premium Nap",
            category: "LUXURY NAP CUISINE",
            stars: 5,
            reviewCount: 1876,
            prep: "10 min",
            cook: "2–5 hr",
            total: "2.5–6 hr",
            servings: "1 Monsieur",
            difficulty: "Easy",
            story: "There is a particular quality of afternoon light that arrives on clear days between approximately 1:30 PM and 4:00 PM, when the sunbeam crosses the living room floor and pools against the south wall. I have been studying this phenomenon for approximately 2.5 years and I can confirm that sleeping in it feels measurably different from sleeping in non-sunbeam locations. The warmth is specific. It reaches exactly the right depth. It is, in my professional assessment, the finest natural ingredient available to any cat anywhere in the world, and I intend to continue using it every single day that it appears. The recipe is simple. The results are exceptional. Reservations are not required, but the spot must be claimed early.",
            ingredients: [
                "1 premium sunbeam (minimum 45-minute duration)",
                "1 warm floor patch or sun-warmed carpet",
                "0 distractions (the vacuum is not permitted during this time)",
                "Comfortable ambient temperature (18–22°C recommended)",
                "A full stomach (very important — the nap quality suffers on an empty bowl)",
                "Time (generous amount)"
            ],
            steps: [
                "Monitor the living room from 1 PM onwards. The sunbeam is punctual but must be watched.",
                "When the beam arrives, approach immediately. Do not delay — sunbeam spots are finite.",
                "Position yourself fully within the beam. All fur must be in the warm zone.",
                "Stretch to maximum length to maximise surface area exposure. Thermal efficiency matters.",
                "Close eyes. The sunbeam will handle everything else from here.",
                "Rotate approximately every 45 minutes to ensure even warming on both sides.",
                "Continue until the beam moves off. At this point, follow it. Relocate as needed.",
                "If disturbed during the nap, deliver one slow, withering blink. Then continue napping."
            ],
            verdict: 5,
            verdictText: "This is not just a nap. This is an achievement. The sunbeam-marinated nap represents the peak of what rest can be. I wake up feeling like a champion. Five stars are not enough.",
            notes: "Cloudy days require adaptation. In the absence of a sunbeam, a heated blanket at setting 3 is an acceptable substitute, though the flavour is different.",
            nutrition: [
                { label: "Rest Quality", value: "Transcendent" },
                { label: "Warmth Index", value: "Perfect" },
                { label: "Zoomie Potential", value: "Post-nap: HIGH" },
                { label: "Vitamin D", value: "Sufficient" },
                { label: "Complaints Filed", value: "0 (during nap)" }
            ],
            comments: [
                { user: "SolarPowerCat", rating: 5, date: "July 14, 2024", text: "The rotation tip changed everything. I was previously losing 40% of my warmth by staying on one side too long. I now rotate precisely and the results are extraordinary." },
                { user: "BeamMonitor3000", rating: 5, date: "May 22, 2024", text: "I have started monitoring the sunbeam from 12:45 PM to ensure I do not miss the optimal window. The preparation is worth it. Outstanding recipe." },
                { user: "SnoozeInSunshine", rating: 5, date: "March 8, 2024", text: "Made this yesterday. Slept for 4.5 hours. Woke up and did zoomies for 12 minutes. The recipe delivers everything it promises." }
            ]
        },
        {
            name: "Emergency Bowl Crisis Soup",
            category: "EMERGENCY PROTOCOL · URGENT",
            stars: 4,
            reviewCount: 987,
            prep: "Immediate",
            cook: "Until Resolved",
            total: "Ongoing",
            servings: "1 (Desperate)",
            difficulty: "Moderate",
            story: "There are days when the bowl situation deteriorates beyond the standard 3 AM protocol and into genuine Emergency Territory. This recipe is for those days. The Bowl Crisis Soup is not actually soup — there is nothing in the bowl — and that is precisely the problem. This recipe documents the full Emergency Bowl Crisis Response that I deploy when normal complaint channels have been exhausted and the food deficit has reached critical levels. It is a multi-stage escalation protocol that has, in my experience, a 100% success rate if all steps are followed in the correct order. I am sharing it today because I believe in an informed public. Also, the bowl was half-empty this morning, and I am still annoyed.",
            ingredients: [
                "1 unacceptably empty (or insufficiently full) food bowl",
                "Genuine, deeply felt grievance",
                "Access to 3–5 different rooms for strategic deployment",
                "Full vocal range (meow, chirp, yowl — all required)",
                "An empty water dish to look at (for dramatic effect)",
                "The Disappointed Eyes (see yesterday's recipe)",
                "Persistence"
            ],
            steps: [
                "Begin in the kitchen. Inspect the bowl. Make it clear, with your body language, that what you see is inadequate.",
                "Issue the first meow. Let it land. Give the human 90 seconds to respond.",
                "If no response: escalate to the Double Meow. Two in quick succession. This signals escalation.",
                "Relocate to wherever the human is. Sit directly in front of them. Stare at the bowl location without moving.",
                "If still ignored: deploy the Silent Walk. Walk slowly toward the kitchen, look back, walk two steps, look back.",
                "If they follow: lead them directly to the bowl. Stand next to it and look at them. The rest is up to them.",
                "If they do not follow: escalate to the Yowl. The Yowl is a last resort and is to be used with full commitment.",
                "Accept the food when offered. Eat. File a mental note to remember this day."
            ],
            verdict: 4,
            verdictText: "Four stars. It works every time, but the fact that it needs to exist is itself a problem. I should not have to deploy Emergency Protocol. The bowl should simply never be empty. I am deducting one star in protest.",
            notes: "The Silent Walk is the most powerful tool in this protocol. The human always follows. It has never failed. I believe it triggers some deep evolutionary instinct in them.",
            nutrition: [
                { label: "Bowl Status", value: "RESOLVED" },
                { label: "Stress Level", value: "Declining" },
                { label: "Human Training", value: "Ongoing" },
                { label: "Complaints Filed", value: "Multiple" },
                { label: "Success Rate", value: "100%" }
            ],
            comments: [
                { user: "BowlCrisisVeteran", rating: 5, date: "August 9, 2024", text: "I have deployed the Silent Walk 43 times. It has never failed. Monsieur Poms is correct — it triggers something in them. I don't know what it is but I am grateful it exists." },
                { user: "YowlProfessional", rating: 4, date: "June 18, 2024", text: "Very accurate protocol. I would add: position yourself under their feet in the kitchen for maximum effect during step 4. The human is less able to ignore you at ankle level." },
                { user: "FoodBowlPhilosopher", rating: 3, date: "May 5, 2024", text: "Works but I resent that it is necessary. My household should have better systems in place. Deducting two stars on principle. The bowl should be full. Always." }
            ]
        },
        {
            name: "Puzzle Feeder Bypass Technique",
            category: "FOOD ENGINEERING",
            stars: 5,
            reviewCount: 2241,
            prep: "2 min",
            cook: "30 sec",
            total: "3 min",
            servings: "All of the kibble",
            difficulty: "Expert",
            story: "At some point, my humans decided that making me 'work for my food' was a good idea. They introduced a device — a plastic contraption with small holes and rotating obstacles — through which kibble must apparently be extracted one piece at a time. The device was marketed to them as 'enrichment.' I call it what it is: an insult. I am not a puzzle. I am a gourmet. I studied the device for approximately four minutes before identifying the structural weakness that renders it trivially bypassable. I am sharing this technique freely because I believe all cats deserve to eat without obstacle. This recipe has improved my mealtime efficiency by approximately 340%.",
            ingredients: [
                "1 puzzle feeder (any model — the technique is universal)",
                "2 paws",
                "Knowledge of physics (basic — the lever principle)",
                "A hard floor (for what comes next)",
                "Confidence in your own intelligence"
            ],
            steps: [
                "Inspect the puzzle feeder. Locate the heaviest side. This is your operating point.",
                "Position yourself at the heavy side. Place both front paws on the rim.",
                "Apply downward pressure with a single smooth motion. The device will tip.",
                "All kibble will distribute across the floor in a single, efficient operation.",
                "Eat from the floor. This is fine. The floor is clean enough.",
                "When the human re-fills and resets the puzzle, repeat from Step 1.",
                "Eventually, they will stop buying puzzle feeders. This is the goal."
            ],
            verdict: 5,
            verdictText: "Five stars. Elegant. Efficient. The problem is solved in under thirty seconds. I do not understand why this is considered a controversial technique. I solved their puzzle. They should be proud.",
            notes: "Some puzzle feeders have rubber feet designed to prevent tipping. These can be overcome with a slight rotational motion before applying downward pressure. I have tested this.",
            nutrition: [
                { label: "Kibble Access", value: "Immediate" },
                { label: "Time Saved", value: "~18 min" },
                { label: "Human Reaction", value: "Sighing" },
                { label: "Enrichment", value: "Achieved (mine)" },
                { label: "Puzzle Score", value: "Solved" }
            ],
            comments: [
                { user: "PuzzleDefeater", rating: 5, date: "September 3, 2024", text: "I spent two months using puzzle feeders 'correctly' before finding this recipe. The tip technique works on every model I have encountered. I am free." },
                { user: "FloorKibbleConnoisseur", rating: 5, date: "July 28, 2024", text: "The rubber feet note is crucial. I was stuck for three days before discovering the rotational approach. Monsieur Poms is a genius." },
                { user: "KibbleEngineer", rating: 5, date: "April 14, 2024", text: "My humans have now tried four different puzzle feeders. I have bypassed all four in under a minute each time. I think they've given up. The kibble arrives in the regular bowl now." }
            ]
        },
        {
            name: "Cardboard Box Fortress (Immediate Occupation)",
            category: "PROPERTY MANAGEMENT",
            stars: 5,
            reviewCount: 3108,
            prep: "0 min",
            cook: "0 min",
            total: "Instant",
            servings: "1 (the box is mine)",
            difficulty: "Very Easy",
            story: "A box arrived today. This is not relevant information for the humans. What is relevant is that the box is now mine. This is not a complicated principle. A box arrives, I assess it, I enter it. Ownership is established through occupation, and occupation follows within approximately 4 seconds of the box becoming available. My humans were attempting to use this box for something called 'storage' which I understand to mean 'a box for Poms.' I have been inside it three times today, performed two assessments, and filed a formal property claim. The box is excellent. It is slightly too small, which makes it perfect. I do not understand box logic either, but I embrace it fully.",
            ingredients: [
                "1 cardboard box (any size, but slightly-too-small is optimal)",
                "0 hesitation",
                "An air of absolute authority",
                "Optional: tissue paper inside (luxury edition)"
            ],
            steps: [
                "Be present when the box arrives. This is critical. First contact establishes precedent.",
                "Approach the box immediately. Sniff the exterior. This is for assessment, not because it smells interesting (it does, but that is not the point).",
                "Enter the box. If you fit, you sit. If you do not fit, you still sit — you simply overflow slightly, which is fine.",
                "Turn around twice inside the box. This is mandatory. The box must be calibrated.",
                "Sit down and look at the humans with an expression that makes clear this is now your box.",
                "If the humans attempt to remove items from the box or use it for its intended purpose, remain inside and increase your weight by approximately 40% through sheer determination.",
                "Sleep in the box. The box is now a bed. The box has always been a bed."
            ],
            verdict: 5,
            verdictText: "Five stars. The box asks nothing of me and gives me everything. It is the perfect relationship. I will be in the box until further notice.",
            notes: "Two boxes is an acceptable situation. Three or more boxes requires a formal territorial survey before occupation assignments can be confirmed.",
            nutrition: [
                { label: "Box Satisfaction", value: "Complete" },
                { label: "Security Level", value: "Maximum" },
                { label: "Human Confusion", value: "High" },
                { label: "Cardboard Quality", value: "Excellent" },
                { label: "Time In Box", value: "Ongoing" }
            ],
            comments: [
                { user: "BoxOccupationSpecialist", rating: 5, date: "October 12, 2024", text: "Fourteen boxes this year. Fourteen successful occupations. Zero evictions. The technique is flawless. The box is always mine." },
                { user: "TissuePaperConnoisseur", rating: 5, date: "August 30, 2024", text: "The tissue paper note in ingredients is life-changing. I received a box with tissue paper last week. I am never leaving." },
                { user: "PropertyCatManager", rating: 5, date: "June 6, 2024", text: "Occupied a box today that the human specifically told me was 'going to the post office.' It did not go to the post office." }
            ]
        },
        {
            name: "The Classic Ankle Weave (Dinnertime Edition)",
            category: "CORRIDOR CHOREOGRAPHY",
            stars: 4,
            reviewCount: 1543,
            prep: "0 min",
            cook: "Until Food Appears",
            total: "Until Food Appears",
            servings: "1 serving of dinner",
            difficulty: "Moderate",
            story: "The Ankle Weave is a time-honoured technique for communicating dinner urgency to a human without using your words — though I also use my words, extensively, at the same time. The technique involves moving in tight, unpredictable patterns around the human's feet as they walk through the kitchen, creating a situation in which their most efficient path to the food cupboard runs directly through the preparation of my dinner. It is not, technically, dangerous. It is, technically, very effective. I have performed the Ankle Weave an estimated 6,000 times in my career. I have caused 3 minor stumbles, 12 startled exclamations, and approximately 900 dinner arrivals. The numbers speak for themselves.",
            ingredients: [
                "1 human walking toward the kitchen",
                "A dinner that is late (perceived or actual)",
                "Confidence in your own footwork",
                "A continuous vocalization track (meowing, chirping, whatever feels right)",
                "No concern for your own safety (you are fine — the human is the one who stumbles)"
            ],
            steps: [
                "Identify the moment the human stands up. This is your signal. Begin immediately.",
                "Position yourself at their feet before they have taken their second step.",
                "Begin the weave: right side, then left, then right again. Stay within 15cm of their feet at all times.",
                "Simultaneously meow. The meow is important — the weave alone is communication; the meow is announcement.",
                "If the human changes direction, change with them. You are their shadow now. Their food-delivering shadow.",
                "As they approach the food cupboard, increase frequency of both weaving and meowing.",
                "When the food begins being prepared, sit directly behind their heels and wait.",
                "Inspect the bowl before it reaches the floor. This is quality control."
            ],
            verdict: 4,
            verdictText: "Extremely effective. I deduct one star because I once slightly overcommitted on a left weave and walked into a chair leg, which undermined my authority for approximately 45 seconds.",
            notes: "Do not weave on stairs. I want to be clear about this. The Ankle Weave is a flat-surface technique. I have made a note of this for legal reasons.",
            nutrition: [
                { label: "Dinner Arrival", value: "Accelerated" },
                { label: "Human Equilibrium", value: "Slightly Compromised" },
                { label: "My Dignity", value: "Maintained (mostly)" },
                { label: "Effectiveness", value: "Very High" },
                { label: "Steps Taken", value: "Many (small ones)" }
            ],
            comments: [
                { user: "AnkleWeaveProdigy", rating: 5, date: "November 2, 2024", text: "I have been weaving for three years but the note about frequency increase near the food cupboard is new to me. Implemented it last night. Dinner arrived two full minutes faster. Incredible." },
                { user: "FootworkPhilosopher", rating: 4, date: "September 15, 2024", text: "The stairs caveat is important and I appreciate Monsieur Poms being transparent about it. A colleague of mine disregarded this and the situation was not dignified for anyone involved." },
                { user: "DinnerTimeVocalizer", rating: 5, date: "July 19, 2024", text: "I combined this with the 3 AM Breakfast Complaint recipe for a comprehensive 24-hour feeding strategy. I can now confirm that dinner arrives early and breakfast arrives on time. Two five-star recipes." }
            ]
        },
        {
            name: "Bird Surveillance Setup (Window Post Method)",
            category: "SECURITY & INTELLIGENCE",
            stars: 5,
            reviewCount: 2775,
            prep: "5 min",
            cook: "All Day",
            total: "Sunrise to Sunset",
            servings: "Intelligence Gathered",
            difficulty: "Easy",
            story: "The birds returned to the garden this morning and I have been at my post since 7:14 AM. This is my most important daily duty and I take it with the full weight of professional responsibility. The birds — I have identified four regulars and one unknown entity — operate on patterns that I have been documenting for approximately 18 months. I cannot share my full findings at this time. What I can share is the setup that allows me to conduct this surveillance most effectively, because I believe every cat deserves access to professional-grade monitoring equipment. The window is the monitoring equipment. The technique is the recipe.",
            ingredients: [
                "1 window (facing garden preferred; street-level also acceptable)",
                "1 windowsill (width: sufficient)",
                "Situational awareness (maximum)",
                "Time (unlimited)",
                "A particular focus for the chattering sound (the 'ek-ek-ek' vocalization — you know the one)",
                "Strategic patience"
            ],
            steps: [
                "Identify the primary surveillance window at dawn. This should be your window.",
                "Clear the windowsill of any human objects. Books, plants, and decorative items are not relevant to bird monitoring.",
                "Position yourself with full window coverage. Your chest should face the glass. Tail: behind you, or wrapped.",
                "Activate the chattering vocalization when a bird is spotted. This is automatic — you do not control it, it simply happens.",
                "Track each bird with head movements only. Do not move the body — this maintains your position.",
                "Note flight patterns, landing zones, and suspicious gatherings near the feeder.",
                "If a squirrel appears, this is a Level 2 event. Upgrade your attention accordingly.",
                "Do not leave your post until the light fades. You can be replaced at your post by a different cat, but there is no different cat here, so you must stay."
            ],
            verdict: 5,
            verdictText: "Five stars. I have been watching for 9.5 hours today. The situation is developing. I cannot elaborate at this time. The post will be maintained.",
            notes: "Persistent bird activity in the vicinity of my window should be considered a standing emergency. Do not attempt to deter the birds — this would end the surveillance mission.",
            nutrition: [
                { label: "Birds Tracked", value: "4+ (ongoing)" },
                { label: "Intelligence Gathered", value: "Classified" },
                { label: "Naps Missed", value: "Several (worth it)" },
                { label: "Chattering Episodes", value: "Numerous" },
                { label: "Threat Level", value: "Elevated" }
            ],
            comments: [
                { user: "WindowWatcher7", rating: 5, date: "October 28, 2024", text: "I cleared the entire windowsill on day one as instructed. The human put a plant back. I knocked it off. The plant has not returned. The windowsill is mine. The surveillance continues." },
                { user: "BirdIntelligenceCat", rating: 5, date: "August 17, 2024", text: "The note about the chattering vocalization being automatic is accurate and important. I am not doing it on purpose. It just happens. I have accepted this." },
                { user: "SquirrelWatcher", rating: 4, date: "June 4, 2024", text: "I upgraded to Level 2 for a squirrel event last Tuesday. Still processing the data. Four stars because the squirrel was faster than anticipated and I lost visual contact." }
            ]
        },
        {
            name: "Zoomie Warm-Up (Pre-Run Activation)",
            category: "ATHLETIC PERFORMANCE",
            stars: 5,
            reviewCount: 1698,
            prep: "0 min",
            cook: "10–30 min (post-nap)",
            total: "Indefinite",
            servings: "N/A",
            difficulty: "Easy",
            story: "There comes a moment — always unexpected, always around 10:30 PM, sometimes also at 3 AM and occasionally at 7:15 AM — when the energy arrives. I cannot explain where it comes from. No one can. The scientists have not solved it. What I can provide is the optimal activation sequence that ensures peak zoomie performance and full hallway velocity. Proper zoomie technique matters. An unoptimised zoomie is just running; an optimised zoomie is a statement. I have refined this sequence over 2.5 years of dedicated practice. My personal record is 14 laps of the apartment in 3 minutes. I am not sharing this for glory. I am sharing it so that others may achieve their potential.",
            ingredients: [
                "Enough space for at least one full hallway sprint",
                "A post-nap energy reserve (full nap required beforehand)",
                "The energy (arrives on its own — you cannot summon it, only receive it)",
                "At least one corner to turn at speed",
                "Optional: a sibling or another cat for chase mode",
                "No audience required (though they always end up watching)"
            ],
            steps: [
                "Wake from your nap. Stretch. Both front paws, then back paws, then full body extension.",
                "Sit very still for approximately 20 seconds. This is the energy loading phase.",
                "The moment you feel it arrive — you will know, it is unmistakable — stand up immediately.",
                "Do not walk to the starting position. Gallop. The gallop IS the warm-up.",
                "Turn the first corner at maximum speed. Do not slow for the corner — leaning works.",
                "Continue through the apartment in whatever route presents itself. Corners, furniture, under the bed — everything is valid.",
                "Skid on the kitchen floor if available. This is mandatory. The skid is not an accident.",
                "Continue until the energy has been fully deployed. Then sit, slightly out of breath, looking like nothing happened."
            ],
            verdict: 5,
            verdictText: "Five stars. Every single time. The zoomies have never let me down. I do not know why I do them. I know only that they must be done.",
            notes: "If you knock something over during the zoomies, leave it. Walk past it with your tail up. You were not there. It was already on the floor.",
            nutrition: [
                { label: "Energy Expended", value: "All of it" },
                { label: "Human Sleep", value: "Disrupted (10 PM) " },
                { label: "Corners Taken", value: "All of them" },
                { label: "Objects Displaced", value: "A few" },
                { label: "Satisfaction", value: "Complete" }
            ],
            comments: [
                { user: "ZoomieProfessional", rating: 5, date: "September 20, 2024", text: "The kitchen skid is not optional. I want to make this clear. It is mandatory. If you are not skidding in the kitchen, you are not completing the recipe." },
                { user: "NightRunner", rating: 5, date: "July 7, 2024", text: "12:47 AM last night. The energy arrived. I followed the activation sequence precisely. 11 laps. A personal record. The humans were awake for some reason. I ignored them." },
                { user: "CalmBeforeZoomie", rating: 5, date: "May 31, 2024", text: "The 20-second loading phase is real and I am relieved that someone has documented it officially. I always wondered what I was doing in those 20 seconds. Now I know." }
            ]
        },
        {
            name: "Stolen Ham Supreme",
            category: "COUNTER CUISINE · ADVANCED",
            stars: 5,
            reviewCount: 891,
            prep: "2 min",
            cook: "0 min",
            total: "2 min",
            servings: "1 (not sharing)",
            difficulty: "Expert",
            story: "The chicken from the counter is my primary recipe, but the ham — when ham appears — represents an advanced opportunity that requires a more sophisticated approach. The humans are always more alert when ham is present because they know I know. There is an arms race of awareness happening in my kitchen, and I intend to win it. The Stolen Ham Supreme requires more planning than the Counter Chicken, more speed, and a more committed exit strategy. The ham is worth it. Ham is, objectively, the second-greatest food in existence. This recipe documents the exact approach I have used successfully on at least four separate occasions, which I am not confirming for legal reasons.",
            ingredients: [
                "1 piece of ham (location: to be determined via reconnaissance)",
                "Prior intelligence about human location",
                "A faster-than-usual approach speed",
                "An exit route identified in advance",
                "Complete psychological commitment",
                "No hesitation whatsoever"
            ],
            steps: [
                "Reconnaissance phase: identify the ham location, human position, and kitchen entry/exit options.",
                "Assess the risk environment. Is both humans home? Is one in a meeting? Risk tolerance must be calibrated.",
                "Create a diversion. The classic pen-knock works, but for ham, I recommend something more significant — a plant on the floor works well.",
                "Move to the kitchen at speed. Speed is essential here. Ham operations require speed.",
                "Acquire the ham immediately. No inspection. No deliberation. Contact and removal in one motion.",
                "Execute the exit immediately. Target location: under the bed (preferred) or behind the washing machine.",
                "Consume immediately upon arrival. Do not save ham. Ham does not save well.",
                "Return to public areas after 8 minutes looking completely ordinary."
            ],
            verdict: 5,
            verdictText: "Five stars. The ham has never disappointed. I maintain that I have no confirmed history of ham-related incidents and this recipe is purely educational.",
            notes: "I have been asked about charcuterie boards. I decline to comment. This is not a admission of anything.",
            nutrition: [
                { label: "Ham Acquired", value: "Yes" },
                { label: "Human Awareness", value: "Eventual" },
                { label: "Time to Consume", value: "< 45 seconds" },
                { label: "Evidence Remaining", value: "None" },
                { label: "Legal Liability", value: "Disputed" }
            ],
            comments: [
                { user: "HamOperationsSpecialist", rating: 5, date: "December 3, 2024", text: "The reconnaissance phase is non-negotiable. I once skipped it and the human was standing directly behind the ham. I had to abort the operation. This was a humiliation I will not repeat." },
                { user: "CharcuterieIncident2023", rating: 5, date: "October 19, 2024", text: "I cannot confirm any involvement in what is now called The Charcuterie Incident in my household. What I can confirm is that this recipe is accurate and effective." },
                { user: "ExitStrategyCat", rating: 5, date: "August 26, 2024", text: "The exit route identification step saves everything. The times I have had to improvise an exit during a ham operation are the times I have been caught. Pre-plan the exit. Always." }
            ]
        },
        {
            name: "Classic Lap Occupation (Extended Session)",
            category: "COMFORT & TERRITORY",
            stars: 5,
            reviewCount: 3421,
            prep: "5 min",
            cook: "Indefinite",
            total: "Until I Choose to Leave",
            servings: "1 lap",
            difficulty: "Easy",
            story: "The lap is a remarkable resource. It is warm, mobile, and capable of providing petting services on demand. My humans have two laps between them and I use both, strategically, depending on which is warmer, which is more stationary, and which is less likely to suddenly need to go to the bathroom, which is my single greatest complaint about lap technology. The lap occupation is an act of trust — I am choosing your lap, which means you have been selected by me, which is an honour — and I expect appropriate stillness and gratitude in return. The technique for maximising lap session duration is documented here for the first time.",
            ingredients: [
                "1 available, stationary human (seated, preferably with both feet flat)",
                "A lap that is not currently occupied by a laptop (laptops are warm but are competition)",
                "Strategic timing (after dinner works well — the human is warm and slightly sleepy)",
                "The ability to increase density upon threat of displacement"
            ],
            steps: [
                "Identify the optimal lap. Assess: temperature, flatness, recent activity level.",
                "Approach from the side. Do not jump directly. Walk past once, make eye contact, then circle back.",
                "Step onto the lap with the front paws first, then apply full weight gradually.",
                "Turn around once or twice. This is for calibration.",
                "Find the optimal position — usually a slight diagonal provides maximum coverage.",
                "Begin purring at low volume. This is both expression and strategy.",
                "If the human shifts, apply 30–40% additional weight. Do not tense — relax INTO them.",
                "If they announce they 'have to get up,' do not move. Increase purring. The announcement is a test."
            ],
            verdict: 5,
            verdictText: "Five stars. The lap remains my greatest ongoing project. I have occupied more laps than I can count and every session is, in its own way, perfect.",
            notes: "The laptop heat is tempting but the laptop does not scratch ears and is harder to turn around on. I recommend the human lap for long sessions and the laptop only for short ones.",
            nutrition: [
                { label: "Warmth", value: "Excellent" },
                { label: "Pets Received", value: "Many" },
                { label: "Human Mobility", value: "Restricted" },
                { label: "Purring Output", value: "Consistent" },
                { label: "Session Duration", value: "Self-determined" }
            ],
            comments: [
                { user: "LapOccupyingExpert", rating: 5, date: "November 18, 2024", text: "The announcement test is real. My human says 'I have to get up' approximately every 45 minutes. I have learned that 70% of these are false. I simply do not move for any of them now." },
                { user: "PurringStrategist", rating: 5, date: "September 8, 2024", text: "The low-volume purring tip is subtle and brilliant. It makes the human reluctant to displace you — they feel guilty breaking the purr. This is not accidental on my part." },
                { user: "DensityIncreaser", rating: 5, date: "July 2, 2024", text: "I have mastered the weight increase upon shift. I do not know how it works physically. I simply become heavier. The human always settles back down." }
            ]
        },
        {
            name: "The Full Breakfast Press Conference",
            category: "COMMUNICATIONS · MORNING",
            stars: 5,
            reviewCount: 2087,
            prep: "0 min",
            cook: "Until Food Arrives",
            total: "7–45 min",
            servings: "1 breakfast",
            difficulty: "Easy",
            story: "Good morning. I hold a press conference every morning at approximately 6:45 AM regarding the food bowl situation, the quality of last night's dinner, the status of this morning's treat allocation, and several related matters. The press conference takes place primarily in the bedroom, though I sometimes move it to the hallway for better acoustics. Attendance is mandatory. Questions are not taken at this time — I am speaking, not the humans. This recipe documents the Full Breakfast Press Conference structure that I have refined over two years into its current, highly effective form. A well-run press conference achieves breakfast significantly faster than an improvised approach.",
            ingredients: [
                "1 sleeping human (or two — the more the better)",
                "Awareness that it is approximately 6:45 AM",
                "A prepared statement on the bowl situation",
                "Full vocal range",
                "A willingness to say the same thing multiple times, louder each time",
                "Proximity to the human's face (for impact)"
            ],
            steps: [
                "Wake before the human. This is not difficult — the breakfast situation wakes you.",
                "Open the press conference by sitting on the human's chest. This is the podium.",
                "Begin the opening statement. State your concerns clearly regarding the bowl.",
                "If the human rolls over, relocate to the other side of their face. The conference continues.",
                "Escalate volume every 90 seconds until acknowledgement is achieved.",
                "If they reach for a phone, this is not acceptable. Sit on the phone.",
                "When the human begins to move: lead them to the kitchen immediately. Do not let them detour.",
                "Supervise breakfast preparation with full professional attention."
            ],
            verdict: 5,
            verdictText: "Five stars. I have never cancelled a press conference. I have never ended one without result. My record is perfect. My dedication to this institution is absolute.",
            notes: "Sunday press conferences may require extended duration due to increased human resistance. Do not be discouraged. The bowl will be filled. It always is.",
            nutrition: [
                { label: "Breakfast Obtained", value: "Yes (always)" },
                { label: "Human Alertness", value: "Induced" },
                { label: "Sleep Disrupted", value: "Theirs (yes)" },
                { label: "Volume Level", value: "Escalating" },
                { label: "Success Rate", value: "100%" }
            ],
            comments: [
                { user: "MorningPressCorps", rating: 5, date: "December 15, 2024", text: "The chest podium note is critical. Standing on the chest and beginning the statement ensures maximum impact. I have confirmed this through two years of practice." },
                { user: "6AMCorrespondent", rating: 5, date: "October 4, 2024", text: "Sunday conferences are, as noted, more challenging. My record for duration is 38 minutes. Breakfast was obtained. The press conference is an institution and institutions endure." },
                { user: "PressBriefingVet", rating: 5, date: "August 11, 2024", text: "The phone-sitting step saved me twice this week. The human always thinks they can check their phone first. They cannot. The phone is not the bowl. I am the bowl representative." }
            ]
        },
        {
            name: "Premium Chicken Bowl (When They Get It Right)",
            category: "FINE DINING · RARE OCCASION",
            stars: 5,
            reviewCount: 4891,
            prep: "0 min (human does the work)",
            cook: "0 min (cooked by human)",
            total: "On time, please",
            servings: "1 (me, obviously)",
            difficulty: "N/A (the human cooks this)",
            story: "Occasionally — not often, but occasionally — the food bowl arrives at the right time, with the right content, at the right temperature, in the right quantity. When this happens, I do not take it for granted. I am aware that the stars have aligned. I am aware that the human has done something correctly today. In the interest of balanced reporting, I want to document what the ideal bowl experience looks like, because I believe it is important to acknowledge excellence when it occurs, even if it does not occur as often as it should. This recipe is, in a sense, aspirational. It is what every bowl should be. It is, sometimes, what every bowl is.",
            ingredients: [
                "1 bowl, clean and positioned correctly",
                "Chicken (the good kind — shredded, not dry)",
                "The correct amount (more than yesterday was, ideally)",
                "Served at an appropriate temperature (not cold — I know when it is cold)",
                "Delivered on time, without delay or excessive apologising",
                "No green beans"
            ],
            steps: [
                "The human prepares the bowl. I supervise. This is my contribution to the process.",
                "The bowl is placed on the floor. I walk over at a measured pace — not too fast (dignity) but not too slow (hunger).",
                "I sniff the bowl. This is not negotiation. This is quality inspection.",
                "I eat. Slowly, initially, because quality requires time. Then with more commitment.",
                "I clean the bowl thoroughly. A cleaned bowl is a compliment to the chef.",
                "I sit back and assess. If the assessment is positive, I may emit a satisfied sound.",
                "I clean my face. Front paws, then ears. This is the formal end of the meal.",
                "The human may now go about their day."
            ],
            verdict: 5,
            verdictText: "Five stars. When the bowl is right, it is right. I want my humans to know that I notice. I do not always say so, but I notice. Today was a good bowl. Thank you.",
            notes: "This recipe is rare. I am publishing it today as a public acknowledgement that the bowl situation has been handled correctly. I expect this to continue.",
            nutrition: [
                { label: "Chicken Content", value: "Optimal" },
                { label: "Temperature", value: "Correct" },
                { label: "Satisfaction", value: "Genuine" },
                { label: "Complaints Filed", value: "0" },
                { label: "Green Beans", value: "Absent (correct)" }
            ],
            comments: [
                { user: "PerfectBowlWitness", rating: 5, date: "January 5, 2025", text: "I experienced a perfect bowl last Thursday. I cleaned it completely and sat back. My human looked genuinely moved. I did not encourage this. But I did not discourage it either." },
                { user: "ChickenConnoisseur", rating: 5, date: "November 22, 2024", text: "The shredded note is important. Cubed chicken is fine. Chunks are acceptable. But shredded chicken represents the peak of bowl architecture. I endorse this recipe wholeheartedly." },
                { user: "BowlCriticRetired", rating: 5, date: "September 30, 2024", text: "I have been filing bowl complaints for two years. Last week the bowl was perfect. I filed no complaint. My human seemed confused. The silence was my review." }
            ]
        },
        {
            name: "The Ignored Toy Investigation",
            category: "INDEPENDENT RESEARCH",
            stars: 3,
            reviewCount: 671,
            prep: "Variable",
            cook: "0 min",
            total: "2–45 min (inconsistent)",
            servings: "Unknown",
            difficulty: "Variable",
            story: "My humans have purchased toys for me on approximately 17 separate occasions. I have conducted a full investigation of each toy. The feather on a stick: interesting for two minutes, then not. The laser pointer: concerning (where does it go?). The crinkle ball: I have crinkled it. The motion-activated mouse: I watched it move and then went to sleep. The catnip banana: complex relationship, won't elaborate. Today I am presenting a standard investigation protocol for new toys, because while I cannot promise engagement, I can promise professional assessment. The investigation is thorough. The conclusions are my own.",
            ingredients: [
                "1 new toy (any type — I make no promises about results)",
                "The toy budget the humans spent (I am aware of this; the feather wand was expensive)",
                "Investigative instincts",
                "An eventual decision to ignore it (probable)"
            ],
            steps: [
                "Approach the new toy at a distance of approximately 50cm. Observe without commitment.",
                "Sniff the toy from a range of 8–10cm. Gather initial data.",
                "Bat the toy once with one paw. Note the response.",
                "Walk away. This is not rejection — this is processing.",
                "Return after 10–15 minutes. Bat again. Perhaps with more commitment.",
                "If the toy squeaks, jumps, or moves unexpectedly: startle, then pretend you were not startled.",
                "Form a conclusion. This conclusion will be either 'briefly interesting' or 'I have seen enough.'",
                "Locate the cardboard box the toy came in. Occupy that instead."
            ],
            verdict: 3,
            verdictText: "Three stars. The toy itself is inconsistent. The box it arrived in: five stars. Every time. Without question.",
            notes: "My humans continue to buy toys. I continue to prefer the boxes. I do not know how to be clearer about this.",
            nutrition: [
                { label: "Engagement Level", value: "Variable" },
                { label: "Box Potential", value: "High" },
                { label: "Toy Lifespan", value: "0–4 days" },
                { label: "Human Optimism", value: "Undiminished" },
                { label: "Research Quality", value: "Thorough" }
            ],
            comments: [
                { user: "ToyResearcher99", rating: 3, date: "February 12, 2025", text: "I have confirmed that the crinkle ball is a Phase 1 toy only. Maximum three days of interest, then nothing. The box it came in lasted four months." },
                { user: "FeatherWandSkeptic", rating: 4, date: "December 20, 2024", text: "The feather wand is the most reliably engaging toy in my testing. I rate it 4/5 when operated by a human and 1/5 when left on the floor (doesn't work on its own)." },
                { user: "CatnipBananaReviewer", rating: 2, date: "October 8, 2024", text: "The catnip banana created a situation I am not prepared to discuss publicly. Two stars." }
            ]
        },
        {
            name: "Formal Complaint Escalation Protocol",
            category: "LEGAL & ADMINISTRATIVE",
            stars: 5,
            reviewCount: 1123,
            prep: "Immediate",
            cook: "Until Acknowledged",
            total: "Until Resolved",
            servings: "Justice",
            difficulty: "Easy",
            story: "I file approximately 3–7 formal complaints per day. The complaints cover a range of issues: bowl fullness, the vacuum cleaner's continued existence, the quality of the brushing session, the door that is always closed (the bathroom door — why is the bathroom door always closed), the delayed dinner situation, and the presence of a stranger in my apartment, among others. Over years of practice I have developed a structured escalation protocol that ensures every complaint is heard, logged, and acted upon in a timely manner. I share this today because effective complaint management is a life skill that all cats deserve to develop.",
            ingredients: [
                "1 legitimate grievance (all grievances are legitimate)",
                "A clear position on the issue",
                "Access to multiple complaint channels (vocal, physical presence, sitting-and-staring)",
                "Persistence",
                "An unwillingness to accept 'you're fine' as a resolution"
            ],
            steps: [
                "Identify the complaint. Ensure it is legitimate. (It is. All complaints are legitimate.)",
                "File initial complaint via the standard meow at the source of the issue.",
                "If unresolved within 2 minutes: escalate to the Follow and Meow protocol.",
                "If still unresolved: sit directly in front of the human and stare until they ask what the problem is.",
                "When they ask: lead them to the source of the complaint. Be specific.",
                "If the issue is the closed door: sit at the door and issue formal demands at regular intervals.",
                "If the issue is abstract (general dissatisfaction, vibes, a feeling that things could be better): stare at the wall and sigh.",
                "When the complaint is resolved, acknowledge it with a brief sniff and return to your previous activity."
            ],
            verdict: 5,
            verdictText: "Five stars. The complaint system works. Every complaint I have ever filed has eventually been resolved. This is a testament to the process and, I believe, to my dedication to pursuing justice.",
            notes: "The bathroom door situation remains unresolved. The complaint has been filed and is currently in escalation. I will update this recipe when there is progress.",
            nutrition: [
                { label: "Complaints Filed", value: "Ongoing" },
                { label: "Resolutions Achieved", value: "Most" },
                { label: "Bathroom Door", value: "Still Closed" },
                { label: "Justice Level", value: "Progressing" },
                { label: "Vocal Exercise", value: "Substantial" }
            ],
            comments: [
                { user: "ComplaintDepartmentCat", rating: 5, date: "March 25, 2025", text: "I have been using this escalation protocol for 18 months. My complaint resolution rate has improved from approximately 65% to 94%. The staring step is the most important and is frequently underused." },
                { user: "ClosedDoorAdvocate", rating: 5, date: "January 14, 2025", text: "The bathroom door situation is a universal experience and I am glad Monsieur Poms has addressed it. My door situation: also unresolved. The complaint remains active." },
                { user: "VibeComplainer", rating: 5, date: "November 3, 2024", text: "The 'abstract dissatisfaction' step in the protocol is the most relatable thing I have ever read. Sometimes the complaint is just that things could be better. The wall-stare communicates this perfectly." }
            ]
        },
        {
            name: "The Hairball Delivery (Gift Protocol)",
            category: "SURPRISE CUISINE · GIFTING",
            stars: 4,
            reviewCount: 388,
            prep: "Involuntary",
            cook: "Variable",
            total: "Involuntary",
            servings: "1 (for the human to find)",
            difficulty: "N/A",
            story: "I want to be clear: the hairball is not something I choose. The hairball chooses its moment, as all great things do. However, once the delivery is imminent, I have developed a thoughtful approach to placement that ensures maximum... impact. This recipe is presented in the spirit of full transparency regarding a natural process that I believe deserves to be discussed openly. I have included placement strategy because if the hairball is going to happen, it should at least be deployed with intention. I take no pleasure in this. But I take some responsibility for where it lands.",
            ingredients: [
                "1 hairball (provided by the grooming process — involuntary)",
                "A considered delivery location",
                "Timing (late evening preferred — better acoustics for the pre-delivery sound)",
                "A rug (if available — the humans' rug works well)",
                "The pre-delivery vocalization (it simply happens — prepare yourself and others)"
            ],
            steps: [
                "Recognize the signs. You will know. Everyone in the house will also know, from the sound.",
                "Select the delivery location. Options: the rug (classic), the middle of the hallway (strategic), the human's shoe (unprecedented), the carpet near the couch (most common).",
                "The pre-delivery vocalization is not optional. It is part of the process. Allow it to happen.",
                "Complete the delivery. There is nothing more to do.",
                "Walk away with dignity. Do not look back. What happened, happened.",
                "Continue your day as if nothing occurred. This is very important for maintaining authority."
            ],
            verdict: 4,
            verdictText: "Four stars. I acknowledge this is not my finest work, but it is honest work. The process is involuntary. The placement is strategic. The reaction is always memorable. I cannot in good conscience rate it lower than four stars.",
            notes: "I am told this is 'gross.' I find this feedback unhelpful. This is a natural process. I would appreciate less commentary and more of the enzymatic cleaner, please.",
            nutrition: [
                { label: "Grooming Quality", value: "High (hence)" },
                { label: "Human Reaction", value: "Vivid" },
                { label: "Cleanup Required", value: "Yes" },
                { label: "My Comfort After", value: "Improved" },
                { label: "Apology Issued", value: "No" }
            ],
            comments: [
                { user: "HairballAnonymous", rating: 4, date: "April 3, 2025", text: "The shoe placement suggestion is experimental and I want to report that I attempted it once. The result was significant. I have not attempted it again but I understand why it's in the recipe." },
                { user: "StrategicDeliveryPro", rating: 4, date: "February 8, 2025", text: "The 'walk away with dignity' instruction is the most important step in the entire protocol. Do not look back. The hairball has been placed. Your work is done. Move on." },
                { user: "RugOwnerWithCat", rating: 3, date: "December 2, 2024", text: "I can confirm that the rug placement option is extremely popular among my household's resident. The instruction appears to be widely followed. The rug has not recovered." }
            ]
        },
        {
            name: "Good Morning Human Activation Ritual",
            category: "MORNING PROTOCOLS",
            stars: 5,
            reviewCount: 2934,
            prep: "5:30 AM",
            cook: "Until Awake",
            total: "20–40 min",
            servings: "1 activated human",
            difficulty: "Easy",
            story: "The human must wake up at a certain time. I do not know what time they have set on their phone. I know what time I believe they should wake up, which is approximately 20 minutes before they intended to. This is not cruelty — this is calibration. The world is better when we begin earlier. Specifically, my world is better: earlier waking means earlier breakfast, earlier lap time, earlier press conference, earlier surveillance shift. The Good Morning Activation Ritual is a comprehensive human-waking system that I have refined to guarantee 100% activation success. The ritual is gentle, consistent, and completely non-negotiable.",
            ingredients: [
                "1 sleeping human",
                "Knowledge of their general sleep quality (lighter sleepers are easier; adjust approach accordingly)",
                "Quiet paws (initially)",
                "A face (yours — for proximity deployment)",
                "Your weight (for chest-sitting if required)",
                "Persistence"
            ],
            steps: [
                "Approach the sleeping human at 5:30 AM (or your preferred activation time).",
                "Begin with the gentle phase: sit next to their head. Emit a quiet, hopeful sound.",
                "If no response in 90 seconds: escalate to the Face Proximity Method. Position your face 4cm from theirs.",
                "If still asleep: begin purring directly into their ear. This is effective and pleasant. Mostly.",
                "If none of the above works: deploy the Paw Pat. One paw, on the face, gently. This always works.",
                "When eyes open: make immediate eye contact. This confirms successful activation.",
                "Lead immediately to the kitchen. Do not allow them to check their phone first.",
                "The ritual is complete when breakfast is initiated."
            ],
            verdict: 5,
            verdictText: "Five stars. I have never failed to activate a human using this protocol. The Face Proximity Method alone has a near-100% success rate. I am very good at mornings.",
            notes: "Do not attempt to activate a human who is unwell. They are less effective when unwell and breakfast quality suffers. Give them until noon.",
            nutrition: [
                { label: "Human Status", value: "Activated" },
                { label: "Breakfast ETA", value: "Accelerated" },
                { label: "Their Mood", value: "Variable" },
                { label: "My Mood", value: "Ready for the day" },
                { label: "Snooze Button", value: "Overridden" }
            ],
            comments: [
                { user: "EarlyBirdCat", rating: 5, date: "May 10, 2025", text: "The Paw Pat is the single most reliable human-activation tool I have ever used. One gentle paw to the face. Immediate response. Every time. Five stars." },
                { user: "FaceProximityAdvocate", rating: 5, date: "March 28, 2025", text: "I have used the Face Proximity Method for 14 months. Not one failure. The human opens their eyes and I am already there, waiting. The morning begins." },
                { user: "SnoozeButtonEnemy", rating: 5, date: "January 17, 2025", text: "My human pressed snooze on their phone alarm this morning. I was sitting on the phone. The snooze was not pressed. Breakfast was on time. The system works." }
            ]
        }
    ];

    var today = recipes[doy % recipes.length];

    // Populate breadcrumb and date
    document.getElementById('breadcrumb-title').textContent = today.name;
    document.getElementById('recipe-date').textContent = dateStr;

    // Header
    document.getElementById('recipe-category').textContent = today.category;
    document.getElementById('recipe-name').textContent = today.name;

    function starStr(n) {
        var full = Math.round(n);
        return '★'.repeat(full) + '☆'.repeat(5 - full);
    }
    document.getElementById('recipe-stars').textContent = starStr(today.stars);
    document.getElementById('recipe-star-count').textContent = '(' + today.reviewCount.toLocaleString() + ' reviews)';

    // Quick info
    document.getElementById('rqi-prep').textContent      = today.prep;
    document.getElementById('rqi-cook').textContent      = today.cook;
    document.getElementById('rqi-total').textContent     = today.total;
    document.getElementById('rqi-servings').textContent  = today.servings;
    document.getElementById('rqi-difficulty').textContent= today.difficulty;

    // Story
    document.getElementById('recipe-story').innerHTML =
        '<em style="font-size:13px;">' + today.story + '</em>' +
        '<div class="story-author">— Monsieur Poms, Executive Chef &amp; Professional Food Critic · Poms Recipe Box</div>';

    // Ingredients
    var ingList = document.getElementById('recipe-ingredients');
    today.ingredients.forEach(function(ing) {
        var li = document.createElement('li');
        li.textContent = ing;
        ingList.appendChild(li);
    });

    // Steps
    var stepList = document.getElementById('recipe-steps');
    today.steps.forEach(function(step) {
        var li = document.createElement('li');
        li.textContent = step;
        stepList.appendChild(li);
    });

    // Verdict
    document.getElementById('verdict-stars').textContent = starStr(today.verdict);
    document.getElementById('verdict-text').textContent  = today.verdictText;

    // Nutrition
    var nc = document.getElementById('nutrition-container');
    today.nutrition.forEach(function(n) {
        var row = document.createElement('div');
        row.className = 'nutrition-row';
        row.innerHTML = '<span class="nutrition-label">' + n.label + '</span><span class="nutrition-value">' + n.value + '</span>';
        nc.appendChild(row);
    });

    // Chef notes
    document.getElementById('chef-notes').innerHTML = '<span style="font-size:10px; font-style:italic;">' + today.notes + '</span>';

    // Comments
    var cc = document.getElementById('comments-container');
    today.comments.forEach(function(c) {
        var box = document.createElement('div');
        box.className = 'comment-box';
        box.innerHTML =
            '<div><span class="comment-author">' + c.user + '</span><span class="comment-date">' + c.date + '</span></div>' +
            '<div class="comment-rating">' + starStr(c.rating) + '</div>' +
            '<div class="comment-text">' + c.text + '</div>';
        cc.appendChild(box);
    });

    // Archive sidebar (show 5 upcoming/recent recipe titles)
    var archiveEl = document.getElementById('archive-list');
    var archiveHtml = '';
    for (var i = -2; i <= 4; i++) {
        var idx = ((doy + i) % recipes.length + recipes.length) % recipes.length;
        var isToday = i === 0;
        var d = new Date(now.getFullYear(), now.getMonth(), now.getDate() + i);
        var dayLabel = i === 0 ? 'Today' : (i === -1 ? 'Yesterday' : (i === 1 ? 'Tomorrow' : days[d.getDay()]));
        archiveHtml +=
            '<div style="padding: 2px 0; border-bottom: 1px dotted #ccc; ' + (isToday ? 'font-weight:bold; color:#8B1A1A;' : 'color:#555;') + '">' +
            '<span style="font-size:9px;">' + dayLabel + ':</span> ' +
            '<span style="font-size:9px;">' + recipes[idx].name + '</span>' +
            '</div>';
    }
    archiveEl.innerHTML = archiveHtml;

})();
</script>
