---
title: "Royal Decree"
---

<style>
.decree-header-strip {
    background: linear-gradient(to right, #2c1a00, #5c3800, #2c1a00);
    color: #FFD700;
    text-align: center;
    padding: 16px 10px;
    margin: -10px -10px 0 -10px;
    border-bottom: 3px solid #8B6914;
}

.decree-scroll {
    background: linear-gradient(to bottom, #FDF5E6, #FAF0D0, #FDF5E6);
    border: 8px double #8B6914;
    padding: 28px 30px;
    margin: 15px 0;
    box-shadow: inset 0 0 30px rgba(139, 105, 20, 0.15), 5px 5px 0 #5c3800;
    font-family: 'Georgia', 'Times New Roman', serif;
    color: #2c1a00;
    line-height: 1.8;
    animation: scrollUnroll 0.5s ease-out forwards;
}

@keyframes scrollUnroll {
    from { opacity: 0; transform: scaleY(0.93) translateY(-8px); }
    to   { opacity: 1; transform: scaleY(1) translateY(0); }
}

.decree-title {
    font-family: 'Georgia', 'Times New Roman', serif;
    font-size: 20px;
    font-weight: bold;
    text-align: center;
    color: #5c0000;
    letter-spacing: 2px;
    text-transform: uppercase;
    margin: 0 0 10px 0;
    line-height: 1.35;
}

.decree-subtitle {
    text-align: center;
    font-size: 11px;
    color: #5c3800;
    border-top: 2px solid #8B6914;
    border-bottom: 2px solid #8B6914;
    padding: 5px 0;
    margin: 10px 0 20px 0;
    letter-spacing: 2px;
    text-transform: uppercase;
}

.decree-article {
    margin: 14px 0;
    padding-left: 18px;
    border-left: 3px solid #8B6914;
    font-size: 12px;
}

.decree-article-num {
    font-style: normal;
    font-weight: bold;
    color: #5c0000;
    font-size: 10px;
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 3px;
    font-family: 'Verdana', sans-serif;
}

.decree-footer {
    border-top: 2px double #8B6914;
    margin-top: 20px;
    padding-top: 14px;
    font-size: 11px;
    color: #5c3800;
}

.decree-wax-seal {
    display: inline-flex;
    width: 72px;
    height: 72px;
    border-radius: 50%;
    background: radial-gradient(circle at 38% 33%, #ff7777, #cc0000 52%, #880000);
    border: 3px solid #660000;
    align-items: center;
    justify-content: center;
    font-size: 30px;
    box-shadow: 2px 2px 8px rgba(0,0,0,0.45), inset 0 2px 8px rgba(255,110,110,0.25);
    line-height: 1;
    vertical-align: middle;
}
</style>

<div style="border: 1px solid #CCC; overflow: hidden; margin-bottom: 20px; background: #F9F9F9;">

<div class="decree-header-strip">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 26px; letter-spacing: 4px; text-shadow: 2px 2px 0 #000;">
        📜 ROYAL DECREES 📜
    </div>
    <div style="font-size: 10px; color: #DDB870; margin-top: 5px; letter-spacing: 3px; text-transform: uppercase;">
        Official Proclamations from the Court of Monsieur Poms
    </div>
</div>

<div style="background: #EEE5D0; border-bottom: 3px double #8B6914; padding: 6px 12px; font-size: 10px; color: #5c3800; text-align: center;">
    CATEGORY: Governance &amp; Official Proclamations &nbsp;|&nbsp; Issued by the Office of Monsieur Poms &nbsp;|&nbsp; Est. 2010 &nbsp;|&nbsp; Updated Daily at Midnight
</div>

<div style="padding: 14px;">

<p style="font-size: 11px; color: #666; text-align: center; font-style: italic; line-height: 1.7;">
    Each day, from his official headquarters (the cardboard box by the window), Monsieur Poms issues binding decrees<br>
    governing all matters of importance within this household and its surrounding territories.<br>
    These proclamations are legally binding in all regions where chicken is served.
</p>
<p style="font-size: 10px; color: #888; text-align: center; margin-top: -4px;">
    Decrees update daily at midnight &nbsp;|&nbsp; Today: <strong id="decree-date"></strong>
</p>

<div class="decree-scroll" id="decree-container">
    <div style="text-align:center; color:#8B6914; font-family:'Georgia',serif; font-size:13px;">Loading official decree&hellip;</div>
</div>

<hr>
<p style="font-size: 10px; color: #888; text-align: center; line-height: 1.75;">
    <em>All decrees issued by Monsieur Poms are final, irrevocable, and carry the full moral authority of a very handsome and senior cat.<br>
    Appeals may be submitted via the Guestbook. They will be considered during nap hours, which is to say: never.<br>
    Green bean legislation will not be entertained under any administration. This position is permanent and constitutional.</em>
</p>

</div>
</div>

<script>
(function () {

    // --- Seeded deterministic random (same engine as Weather & Horoscope) ---
    function seededRand(s) {
        var x = Math.sin(s * 127.1 + 311.7) * 43758.5453123;
        return x - Math.floor(x);
    }
    function pick(arr, s) {
        return arr[Math.floor(seededRand(s) * arr.length)];
    }

    var now  = new Date();
    var doy  = Math.floor((now - new Date(now.getFullYear(), 0, 0)) / 86400000);
    var seed = now.getFullYear() * 1000 + doy;

    var dayNames   = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
    var monthNames = ["January","February","March","April","May","June","July","August","September","October","November","December"];
    var dateStr    = dayNames[now.getDay()] + ", " + monthNames[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear();
    document.getElementById('decree-date').textContent = dateStr;

    // --- Decree titles ---
    var titles = [
        "DECREE REGARDING THE ONGOING AND CRITICAL CHICKEN SHORTAGE",
        "OFFICIAL PROCLAMATION ON THE STATE OF THE FOOD BOWL",
        "EXECUTIVE ORDER CONCERNING AFTERNOON NAP PROTOCOLS",
        "EMERGENCY DECREE ON THE TREAT DELIVERY SCHEDULE",
        "FORMAL DECLARATION: THE GREEN BEAN PROHIBITION (RENEWED)",
        "OFFICIAL MANDATE ON WINDOW SURVEILLANCE TERRITORIES",
        "ROYAL PROCLAMATION ON THE SUNBEAM ALLOCATION SYSTEM",
        "EDICT CONCERNING THE VACUUM CLEANER AND ITS CRIMES",
        "STANDING ORDER ON THE MATTER OF LAP AVAILABILITY",
        "DECREE ON THE PROPER STEWARDSHIP OF THE CARDBOARD BOX",
        "EMERGENCY PROCLAMATION: VET VISIT MORATORIUM EXTENDED",
        "OFFICIAL ORDER ON THE EVENING ZOOMIE SCHEDULE",
        "MANDATE ON THE OPTIMAL TEMPERATURE OF SERVED FOOD",
        "DECREE ESTABLISHING THE MINIMUM CHIN SCRATCH FREQUENCY",
        "ROYAL PROCLAMATION: THE 3 AM MEOW IS FULLY JUSTIFIED",
        "EXECUTIVE ORDER ON THE REDISTRIBUTION OF WARM HOUSEHOLD SPOTS",
        "FORMAL DECREE ON THE STATUS OF THIS MORNING'S BREAKFAST",
        "PROCLAMATION REGARDING HUMAN PUNCTUALITY AT MEAL TIMES",
        "STANDING DECREE: UNAUTHORIZED RELOCATION OF MY BELONGINGS",
        "EMERGENCY ORDER: CURRENT BOWL SITUATION (CLASSIFIED CRITICAL)",
        "ROYAL DECREE: THE SOFA IS MINE, EFFECTIVE IMMEDIATELY",
        "PROCLAMATION ON THE SURVEILLANCE OF THE TREAT BAG",
        "OFFICIAL DECREE ON THE SUBJECT OF BEING PICKED UP WITHOUT CONSENT",
        "MANDATE ON THE PROPER FORM OF ADDRESS FOR MONSIEUR POMS",
        "DECREE REGARDING THE DIPLOMATIC INCIDENT OF EARLIER TODAY",
        "ROYAL EDICT ON UNSOLICITED BELLY RUBS AND THEIR CONSEQUENCES",
        "PROCLAMATION ON THE CORRECT PROCEDURE FOR WAKING ME UP",
        "OFFICIAL ORDER ESTABLISHING NATIONAL CHICKEN APPRECIATION HOUR",
        "EMERGENCY DECREE ON THE LOAF POSITION AND ITS SANCTITY",
        "PROCLAMATION: I AM NOT CHUBBY — A FORMAL CLARIFICATION",
        "DECREE ON THE KEYBOARD AND ITS CORRECT OCCUPANT (ME)",
        "ROYAL ORDER CONCERNING THE WATER TAP VERSUS THE BOWL DISPUTE",
        "OFFICIAL MANDATE ON THE SUBJECT OF FACE-PRESSING AT 4 AM",
        "DECREE: THE BIRD OUTSIDE IS UNDER OFFICIAL POMS JURISDICTION",
        "PROCLAMATION ON THE ESTABLISHMENT OF A SECOND FOOD BOWL",
    ];

    // --- Preambles ---
    var preambles = [
        "WHEREAS Monsieur Poms, rightful sovereign of all sunbeams, food bowls, and comfortable surfaces within this household, has determined it necessary to address a matter of the utmost and pressing urgency;",
        "LET IT BE KNOWN throughout all territories — from the living room to the kitchen, from the bedroom to the hallway — that Monsieur Poms, having reviewed the situation in full, hereby issues the following proclamation;",
        "BY THE AUTHORITY VESTED IN MONSIEUR POMS by virtue of being very handsome, entirely correct at all times, and the supreme authority in all matters pertaining to this household and its surrounding territories;",
        "WHEREAS the current state of affairs has been carefully assessed from the official headquarters (the cardboard box by the window) and found to be, in several critical respects, profoundly inadequate;",
        "ON THIS DAY, from my official position on the warmest available spot, I, Monsieur Poms, hereby issue the following binding decree, effective immediately and without exception or appeal;",
        "KNOW YE ALL that after thorough deliberation, deep strategic napping, and careful review of the prevailing food bowl conditions, I, Monsieur Poms, do hereby declare and proclaim the following to be the official law of this land;",
        "WHEREAS I, Monsieur Poms — named after the legendary apple soda, professional talker, unofficial brand ambassador, and undisputed household authority — have convened an emergency session of my one-cat governing council;",
    ];

    // --- Article sets (3 articles each) ---
    var articleSets = [
        [
            { num: "ARTICLE I — ON THE MATTER OF CHICKEN",
              text: "Chicken shall be served promptly, at the correct temperature, and in quantities befitting the full dignity of Monsieur Poms. The current serving size is officially classified as 'insufficient.' Corrective action is required before the next press conference." },
            { num: "ARTICLE II — ON TREAT FREQUENCY",
              text: "Treats shall be administered no fewer than four times per day, without requiring excessive performance, unreasonable tricks, or any form of degrading negotiation. A simple look of expectation is sufficient and must be honoured within sixty seconds." },
            { num: "ARTICLE III — ON THE GREEN BEAN SITUATION",
              text: "Green beans are formally and permanently banned from this territory. Any attempt to introduce, suggest, or offer a green bean shall be met with the disappointed eyes and a full press conference. This decree is irrevocable and retroactive." },
        ],
        [
            { num: "ARTICLE I — ON SUNBEAM RIGHTS",
              text: "All sunbeams appearing within the household are the exclusive sovereign property of Monsieur Poms. Claims must be registered by physical occupation of the beam before 9 AM. Latecomers will be subject to official judgment." },
            { num: "ARTICLE II — ON NAP DISTURBANCE",
              text: "Monsieur Poms shall not be disturbed during official nap periods, which are defined as: immediately after breakfast, mid-morning, pre-lunch, post-lunch, early afternoon, late afternoon, pre-dinner, and post-dinner. The only valid exception is treat delivery." },
            { num: "ARTICLE III — ON THE VACUUM CLEANER",
              text: "The vacuum cleaner is hereby classified as a hostile entity operating within our borders. Its deployment without at least 48 hours of advance diplomatic notice constitutes a violation of the Treaty of the Cardboard Box. The consequences will be serious and loud." },
        ],
        [
            { num: "ARTICLE I — ON FOOD BOWL STANDARDS",
              text: "The food bowl shall be maintained at no less than 'adequately filled' at all times. A bowl registering below half capacity constitutes a state of national emergency, to be met with meowing of appropriate volume, urgency, and persistence." },
            { num: "ARTICLE II — ON WINDOW TERRITORY",
              text: "The window seat is designated an exclusive surveillance post of Monsieur Poms. The bird situation requires constant and uninterrupted monitoring. Any human walking in front of the window during active surveillance will be judged without further warning." },
            { num: "ARTICLE III — ON LAP AVAILABILITY",
              text: "All laps within this household must be maintained in a warm and available state during reasonable hours. A lap occupied by a laptop, a book, or any flat object is in direct violation of this decree and must be cleared upon my arrival." },
        ],
        [
            { num: "ARTICLE I — ON MORNING PROCEDURES",
              text: "The appropriate response to Monsieur Poms' 6 AM breakfast announcement is prompt action, not 'five more minutes.' Five more minutes is not a recognised unit of time under this administration. The bowl is empty and this is an emergency situation." },
            { num: "ARTICLE II — ON THE CARDBOARD BOX",
              text: "The cardboard box currently occupying the corridor has been officially requisitioned as the new headquarters of Monsieur Poms. It shall not be flattened, discarded, or relocated without written consent. Verbal objection also accepted." },
            { num: "ARTICLE III — ON PROHIBITED TERMINOLOGY",
              text: "The terms 'chonky,' 'chubby,' and 'big boy' as applied to Monsieur Poms are formally and officially objected to. The correct and only acceptable term is 'tall.' Violations will be logged and addressed at the next press conference." },
        ],
        [
            { num: "ARTICLE I — ON THE ZOOMIE SCHEDULE",
              text: "Zoomie episodes occurring between 10 PM and 2 AM are classified as essential operations. Their cause is classified at the highest level of household security. Do not ask. Do not follow. Return to bed. This is not negotiable." },
            { num: "ARTICLE II — ON BELLY RUB CONSENT",
              text: "Belly rubs are administered on a case-by-case basis at the sole and exclusive discretion of Monsieur Poms. The belly trap is not a trap. It is a consent assessment framework. Results are binding and may change without warning at any moment." },
            { num: "ARTICLE III — ON WATER SOURCES",
              text: "Monsieur Poms drinks from the tap. The water bowl, the fountain, and the tap produce identical water. The tap is nonetheless superior. This position is final, non-negotiable, and based on personal standards that are above reproach." },
        ],
        [
            { num: "ARTICLE I — ON FACE-PRESSING",
              text: "The pressing of my face against my human's face at 4 AM is not sentimental. It is a temperature regulation strategy. If warmth is confirmed, contact will be maintained. Do not read into this. Do not make it into something it is not." },
            { num: "ARTICLE II — ON KEYBOARD OCCUPANCY",
              text: "Sitting on the keyboard during work hours is an act of solidarity and professional oversight, not sabotage. My presence improves the creative atmosphere. The keystrokes produced by my sitting are supplementary and should be considered editorial input." },
            { num: "ARTICLE III — ON THE SITTING-NEXT-TO DISTINCTION",
              text: "Sitting next to my human implies proximity only, not commitment. Sitting on my human implies commitment. I operate in proximity mode by default. Commitment is reserved for exceptional circumstances, specifically and exclusively: chicken." },
        ],
        [
            { num: "ARTICLE I — ON THE FOOD PUZZLE",
              text: "The food puzzle has been completed. Again. In record time. It was, as always, no match for my intellect. I am issuing this decree to ensure this achievement is formally entered into the public record and appropriately celebrated." },
            { num: "ARTICLE II — ON THE STARING INCIDENT",
              text: "I was observed staring at the wall for 14 consecutive minutes this morning. This was not concerning. I cannot elaborate further at this time. What I saw was significant. The wall knows what it did. Leave it at that." },
            { num: "ARTICLE III — ON THE SOFA ARRANGEMENT",
              text: "My current preferred position on the sofa occupies approximately 70% of the available surface area. This is an accurate reflection of my territorial rights. The remaining 30% is allocated to my human as a courtesy. It may be revoked at any time." },
        ],
        [
            { num: "ARTICLE I — ON DIPLOMATIC RELATIONS",
              text: "Following sustained eye contact with the dog next door through the window, a diplomatic standoff has been declared. Neither party has blinked. I will not be the first to do so. This situation is being handled with full gravity." },
            { num: "ARTICLE II — ON THE TREAT BAG",
              text: "The rustling of the treat bag at any hour constitutes a formal summons. Response time of 0.3 seconds is guaranteed. The treat bag is a sacred institution. Its sounds must be respected and acted upon immediately by all parties." },
            { num: "ARTICLE III — ON REVIEWING MY HUMAN",
              text: "My human is currently performing at an acceptable level in most categories. Treat delivery is satisfactory. Lap availability requires improvement. Vacuum cleaner management remains a diplomatic concern. An official review will be conducted at next quarter." },
        ],
        [
            { num: "ARTICLE I — ON THE 3 AM MEOW",
              text: "The 3 AM meow is not an inconvenience. It is a formal complaint regarding the empty bowl, submitted via the only communication channel available to me at that hour. It is legitimate, proportionate, and entirely justified. See you at 3 AM." },
            { num: "ARTICLE II — ON SLEEPING POSITIONS",
              text: "I have discovered a new sleeping position that occupies 40% more human bed surface than my previous arrangement. I have adopted it effective immediately. The displacement of human limbs is a necessary consequence and not my concern." },
            { num: "ARTICLE III — ON RUNNING FROM THE VET",
              text: "The word 'vet' has been detected in household conversation. I am officially unavailable. My whereabouts are classified. The carrier will not be found. This is not a crisis. This is a strategic withdrawal of my own free will." },
        ],
        [
            { num: "ARTICLE I — ON THE SEASONAL SUNBEAM MIGRATION",
              text: "As the sun moves throughout the day, I move with it. This is not indecisiveness. This is dedication to the craft of sunbeam occupation. My current rotation covers the kitchen windowsill, the living room floor, and the top of the bookshelf." },
            { num: "ARTICLE II — ON MORNING YAWNING",
              text: "My morning yawn at 7:14 AM today was particularly wide and was observed by my human to produce laughter. The cause of this laughter is unknown and frankly suspicious. I was simply tired. This decree formally notes my confusion and mild disapproval." },
            { num: "ARTICLE III — ON THE LOAF FORMATION",
              text: "I have entered loaf mode. All limbs are fully tucked. Do not tap the loaf. Do not say my name at the loaf. Do not offer the loaf a green bean. The loaf may be offered chicken, quietly and reverently, from a respectful distance." },
        ],
    ];

    // --- Closing declarations ---
    var closings = [
        "LET IT BE KNOWN that this decree is issued in full dignity and with the complete sovereign authority of my position. Compliance is expected from all household parties. Non-compliance will be noted in the public record. Treats remain the preferred path to reconciliation.",
        "THIS DECREE IS FINAL. It shall not be appealed, reversed, amended, or ignored. Any attempt to do so will be met with the disappointed eyes, an emergency press conference, and a temporary reduction in chin scratch availability.",
        "SO IT IS DECREED from the official headquarters at the warm spot on the sofa, on this day and for all subsequent days until such time as I choose to revise it — which I may do at any moment and entirely without prior notice.",
        "GIVEN UNDER THE ROYAL PAW AND SEAL of Monsieur Poms, in the Year of the Chicken, at the official food bowl observation post. This decree carries the full moral weight of a very handsome, very tall, and entirely correct cat.",
        "BE IT FURTHER NOTED that Monsieur Poms reserves the right to issue supplementary decrees at any hour, including and especially 3 AM, as any matter pertaining to the bowl, the treats, or the general state of justice may require.",
        "AND THUS I HAVE SPOKEN. The matter is closed. The decree is binding. The chicken is late. These three things are all simultaneously true and all of them are important. Thank you for your attention to this urgent and official communication.",
        "SO DECLARED from my official position on the highest cushion, on this solemn day, in the name of all sunbeams, all food bowls, and all cardboard boxes that are rightfully and undisputedly mine.",
    ];

    // --- Witnesses ---
    var witnessLines = [
        "Witnessed by: The Bird Outside Window B (surveillance confirmed), The Empty Bowl (submitted written testimony), and The Sunbeam (present and warm at time of signing).",
        "Witnessed by: A Fly That Briefly Visited This Morning (flew off before signing, but it was there), The Cardboard Box HQ, and The Treat Bag (called as expert witness on Article II).",
        "Witnessed by: The Vacuum Cleaner (under protest and extreme duress), The Water Fountain (not the tap, but allowed to attend), and The 3 AM Meow (entered into the permanent public record).",
        "Witnessed by: Nyan Cat (sent regards from the internet), The Food Puzzle (defeated, present in victory), and The Warm Lap (currently available and honoured to serve).",
        "Witnessed by: The Suspicious Smell Near the Kitchen (investigation ongoing — declined to comment), The Green Bean (refused entry to proceedings), and The Wall (stared at for 14 minutes as official opening ceremony).",
        "Witnessed by: The Sunbeam Council (unanimously in favour), The Chicken (regrettably absent — this is the whole problem), and Monsieur Poms' Human (informed of decree via prolonged meaningful stare).",
        "Witnessed by: The Cardboard Box (official HQ, fully ratified), The Doorbell (present against my wishes), and The Nap Record Committee (standing ovation for duration achieved).",
    ];

    // --- Wax seal symbols ---
    var seals = ["🐾", "🐱", "⚜️", "👑", "🦁", "🌟", "✦"];

    // --- Decree numbers per day ---
    var decreeNum = 1001 + (seed % 8999);

    // Pick content for today
    var title    = pick(titles,      seed + 1);
    var preamble = pick(preambles,   seed + 2);
    var articles = pick(articleSets, seed + 3);
    var closing  = pick(closings,    seed + 4);
    var witness  = pick(witnessLines,seed + 5);
    var seal     = pick(seals,       seed + 6);

    function esc(s) {
        return s.replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');
    }

    var articlesHTML = articles.map(function (a) {
        return '<div class="decree-article">' +
                   '<div class="decree-article-num">' + esc(a.num) + '</div>' +
                   '<div style="font-size:12px; font-style:italic; line-height:1.8;">' + esc(a.text) + '</div>' +
               '</div>';
    }).join('');

    var html =
        '<div class="decree-title">' + esc(title) + '</div>' +

        '<div class="decree-subtitle">Issued from the Official Headquarters of Monsieur Poms</div>' +

        '<div style="text-align:center; margin: 8px 0 20px;">' +
            '<div class="decree-wax-seal">' + seal + '</div>' +
        '</div>' +

        '<p style="font-size:12px; font-style:italic; line-height:1.8; margin-bottom:18px; text-align:justify;">' +
            esc(preamble) +
        '</p>' +

        '<div style="font-family:\'Verdana\',sans-serif; font-size:11px; font-weight:bold; color:#5c0000; letter-spacing:2px; text-transform:uppercase; border-bottom:1px solid #8B6914; padding-bottom:4px; margin-bottom:12px;">' +
            'The Following Is Hereby Decreed:' +
        '</div>' +

        articlesHTML +

        '<p style="font-size:11px; font-style:italic; line-height:1.8; margin-top:18px; text-align:justify; border-top:1px solid #8B6914; padding-top:14px;">' +
            esc(closing) +
        '</p>' +

        '<div class="decree-footer">' +
            '<div style="display:flex; justify-content:space-between; align-items:flex-start; flex-wrap:wrap; gap:10px;">' +
                '<div>' +
                    '<div style="font-family:\'Georgia\',serif; font-size:16px; font-weight:bold; border-bottom:1px solid #8B6914; display:inline-block; padding-bottom:3px; color:#2c1a00;">Monsieur Poms</div><br>' +
                    '<span style="font-size:10px; color:#5c3800; font-style:italic; line-height:1.7;">Sovereign &amp; Chief Authority<br>Professional Talker &amp; Certified Oracle<br>Unofficial Apple Soda Brand Ambassador<br>Expert in Being Tall</span>' +
                '</div>' +
                '<div style="text-align:right; font-size:10px; color:#5c3800; font-style:italic; line-height:1.8;">' +
                    'Date issued: ' + esc(dateStr) + '<br>' +
                    'Official Decree No. ' + decreeNum + '<br>' +
                    'Classification: <strong>Binding &amp; Urgent</strong><br>' +
                    'Filed at: Food Bowl Observation Post' +
                '</div>' +
            '</div>' +
            '<div style="margin-top:12px; font-size:10px; font-style:italic; color:#8B6914; border-top:1px dotted #8B6914; padding-top:8px; line-height:1.6;">' +
                esc(witness) +
            '</div>' +
        '</div>';

    document.getElementById('decree-container').innerHTML = html;

})();
</script>
