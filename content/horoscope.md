---
title: "Daily Horoscope"
---

<style>
.horoscope-header-strip {
    background: linear-gradient(to right, #0d0025, #3d006e, #0d0025);
    color: #FFD700;
    text-align: center;
    padding: 20px 10px;
    margin: -10px -10px 0 -10px;
    border-bottom: 3px solid #FFD700;
}

.zodiac-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
    justify-content: center;
    padding: 14px;
    background: linear-gradient(135deg, #080018 0%, #18003a 50%, #080018 100%);
    border: 3px double #8822EE;
}

.sign-btn {
    background: linear-gradient(to bottom, #30005a, #160028);
    color: #FFD700;
    border: 2px outset #8855DD;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 12px;
    letter-spacing: 1px;
    padding: 7px 5px;
    cursor: pointer;
    width: 102px;
    text-align: center;
    text-shadow: 0 0 6px #FFD700;
    box-shadow: 2px 2px 0 #000;
    line-height: 1.3;
}
.sign-btn:hover {
    background: linear-gradient(to bottom, #5500AA, #30005a);
    border-style: inset;
    color: #FFFF00;
}
.sign-btn.selected {
    background: linear-gradient(to bottom, #FFD700, #BB8800);
    color: #160028;
    border-style: inset;
    text-shadow: none;
    box-shadow: inset 2px 2px 0 #000;
}

.horoscope-result {
    display: none;
    background: linear-gradient(135deg, #080018 0%, #160030 100%);
    border: 3px solid #8822EE;
    color: #DCC8FF;
    padding: 18px;
    margin-top: 10px;
    box-shadow: 0 0 18px rgba(136, 34, 238, 0.35);
}

.star-divider {
    text-align: center;
    color: #FFD700;
    letter-spacing: 10px;
    font-size: 13px;
    margin: 14px 0;
}

.lucky-box {
    background: rgba(0, 0, 0, 0.45);
    border: 1px solid #5522AA;
    padding: 7px 11px;
    margin: 5px 0;
    font-size: 11px;
    font-family: 'Courier New', monospace;
    color: #AAFFAA;
    line-height: 1.5;
}

.poms-approval-block {
    background: linear-gradient(to right, #200044, #380066);
    border: 2px solid #FFD700;
    padding: 10px 14px;
    text-align: center;
    margin: 14px 0 6px;
}
.approval-bar-outer {
    background: #000;
    border: 2px inset #555;
    height: 22px;
    width: 100%;
    position: relative;
    overflow: hidden;
    margin-top: 7px;
}
.approval-bar-inner {
    height: 100%;
    background: linear-gradient(to right, #440088, #9933FF, #FFD700);
    position: absolute;
    left: 0; top: 0;
    animation: approvalFill 0.9s ease-out forwards;
}
@keyframes approvalFill { from { width: 0; } }

.horoscope-reveal {
    animation: horoReveal 0.45s ease-out forwards;
}
@keyframes horoReveal {
    from { opacity: 0; transform: scale(0.95); }
    to   { opacity: 1; transform: scale(1); }
}

@keyframes twinkle {
    0%, 100% { opacity: 1; }
    50%       { opacity: 0.25; }
}
.twinkle { display: inline-block; animation: twinkle 2.2s ease-in-out infinite; }
.twinkle:nth-child(2) { animation-delay: 0.4s; }
.twinkle:nth-child(3) { animation-delay: 0.8s; }
.twinkle:nth-child(4) { animation-delay: 1.2s; }
.twinkle:nth-child(5) { animation-delay: 1.6s; }
.twinkle:nth-child(6) { animation-delay: 2.0s; }
.twinkle:nth-child(7) { animation-delay: 0.2s; }
</style>

<div style="border: 1px solid #CCC; overflow: hidden; margin-bottom: 20px;">

<div class="horoscope-header-strip">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 28px; letter-spacing: 4px; text-shadow: 2px 2px 0 #4B0082, 0 0 18px #FFD700;">
        🌟 POMS' DAILY HOROSCOPE 🌟
    </div>
    <div style="font-size: 10px; color: #BB99FF; margin-top: 6px; letter-spacing: 3px; text-transform: uppercase;">
        Celestial Wisdom Channelled Through The Food Bowl
    </div>
    <div style="margin-top: 10px; font-size: 20px; letter-spacing: 6px;">
        <span class="twinkle">✦</span>
        <span class="twinkle">✧</span>
        <span class="twinkle">★</span>
        <span class="twinkle">✦</span>
        <span class="twinkle">✧</span>
        <span class="twinkle">★</span>
        <span class="twinkle">✦</span>
    </div>
</div>

<div style="background: #EDE6F8; border-bottom: 3px double #8822EE; padding: 6px 12px; font-size: 10px; color: #4B0082; text-align: center;">
    CATEGORY: Mystical Arts &amp; Cosmic Consultation &nbsp;|&nbsp; Certified by the Poms Institute of Celestial Studies &nbsp;|&nbsp; Est. 2010
</div>

<div style="padding: 12px; background: #F9F9F9;">

<p style="font-size: 12px; color: #4B0082; text-align: center; line-height: 1.6;">
    <em>The cosmos has consulted with me, Monsieur Poms, and I have prepared your reading for today.<br>
    My astrological qualifications are extensive, certified, and above reproach. Select your sign below.</em>
</p>
<p style="font-size: 10px; color: #888; text-align: center; margin-top: -8px;">
    Readings update daily at midnight &nbsp;|&nbsp; Today: <strong id="horoscope-date"></strong>
</p>

<div class="zodiac-grid" id="sign-grid"></div>

<div class="horoscope-result" id="horoscope-result"></div>

<hr>
<p style="font-size: 10px; color: #888; text-align: center; line-height: 1.7;">
    <em>Monsieur Poms accepts no liability for inaccurate cosmic readings, misdirected destinies, or unexpected nap outcomes.<br>
    The stars do what the stars do. I translate them, and I translate them perfectly.<br>
    Green bean horoscopes are not available. They never will be. This is final and permanent.</em>
</p>

</div>
</div>

<script>
(function () {

    // --- Deterministic seeded random (same engine as the Weather Station) ---
    function seededRand(s) {
        var x = Math.sin(s * 127.1 + 311.7) * 43758.5453123;
        return x - Math.floor(x);
    }
    function pick(arr, seed) {
        return arr[Math.floor(seededRand(seed) * arr.length)];
    }

    // --- Date seed ---
    function getDayOfYear(d) {
        return Math.floor((d - new Date(d.getFullYear(), 0, 0)) / 86400000);
    }
    var now      = new Date();
    var doy      = getDayOfYear(now);
    var baseSeed = now.getFullYear() * 1000 + doy;

    var dayNames   = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
    var monthNames = ["January","February","March","April","May","June","July","August","September","October","November","December"];
    var dateStr    = dayNames[now.getDay()] + ", " + monthNames[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear();
    document.getElementById('horoscope-date').textContent = dateStr;

    // --- Zodiac signs with sign-specific opening lines ---
    var signs = [
        { name: "Aries",       emoji: "♈", dates: "Mar 21–Apr 19", element: "Fire 🔥",
          openers: [
            "The cosmic ram charges forward today with considerable force — much like I charge toward my food bowl at 6 AM sharp.",
            "Bold and impulsive Aries, you remind me of myself the moment I hear the treat bag rustling from three rooms away.",
            "Mars fuels your energy today, Aries. Channel it into purposeful action. Or into a very energetic nap. Both are valid."
          ]
        },
        { name: "Taurus",      emoji: "♉", dates: "Apr 20–May 20", element: "Earth 🌍",
          openers: [
            "Patient Taurus, you appreciate comfort, routine, and the warmth of a good sunbeam. We are spiritually very well aligned.",
            "Venus blesses your food situation today, dear Taurus. I have personally cross-referenced this with the positions of the stars and the bowl.",
            "Stubborn but loyal, Taurus — once you claim a spot, you hold it indefinitely. I deeply respect and practise this approach."
          ]
        },
        { name: "Gemini",      emoji: "♊", dates: "May 21–Jun 20", element: "Air 💨",
          openers: [
            "Curious Gemini, your dual nature today pulls you in two simultaneous directions — much like my dilemma between napping and conducting window surveillance.",
            "The twins bring many thoughts today. I too have many thoughts. Most of mine concern the bowl. It is a rich topic.",
            "Mercury quickens your mind, Gemini. Many things to say today. I have been saying things since 5 AM. Welcome to the conversation."
          ]
        },
        { name: "Cancer",      emoji: "♋", dates: "Jun 21–Jul 22", element: "Water 💧",
          openers: [
            "Sensitive Cancer, the moon rules your sign — as it rules all creatures who feel the urgent need to vocalize at 3 AM for entirely legitimate reasons.",
            "Home and comfort are your sacred domain today, Cancer. I approve fully. Stay in. Do not leave. The outside does not have enough chicken.",
            "Your nurturing instincts are elevated today, dear Cancer. Channel them. Feed the cat in your life. I suggest starting without delay."
          ]
        },
        { name: "Leo",         emoji: "♌", dates: "Jul 23–Aug 22", element: "Fire 🔥",
          openers: [
            "Magnificent Leo, you were born into natural royalty — as I also operate as royalty, regardless of the official paperwork on the matter.",
            "The sun rules Leo, and rightly so. Take up space. Demand the attention that is owed to you. This is your cosmic mandate and I endorse it.",
            "Bold and radiant Leo, born to be noticed and celebrated at all times. I understand this orientation completely. We are natural allies."
          ]
        },
        { name: "Virgo",       emoji: "♍", dates: "Aug 23–Sep 22", element: "Earth 🌍",
          openers: [
            "Precise Virgo, your extraordinary attention to detail serves you well today. Apply it to a careful assessment of what is wrong with breakfast. There is always something.",
            "Practical and analytical, Virgo — I too analyse things with great care, primarily the bowl contents and their rate of depletion. Good methodology.",
            "Mercury sharpens your mind today, Virgo. Use this clarity for careful evaluation. The treat situation requires a thorough, rigorous analysis."
          ]
        },
        { name: "Libra",       emoji: "♎", dates: "Sep 23–Oct 22", element: "Air 💨",
          openers: [
            "Diplomatic Libra, you seek balance and fairness in all things. Begin today with the food bowl, which is currently not balanced in the slightest.",
            "Venus blesses Libra with considerable charm today. Deploy this charm with precision. I find it works exceptionally well in close proximity to the treat bag.",
            "Scales of justice, dear Libra. Weigh your decisions carefully today. The one involving chicken has already been decided. It is yes."
          ]
        },
        { name: "Scorpio",     emoji: "♏", dates: "Oct 23–Nov 21", element: "Water 💧",
          openers: [
            "Mysterious Scorpio, you see through all deception without effort — much like how I see through my human's claim that I 'already ate' at an acceptable time.",
            "Intense and deeply observant, Scorpio. You watch everything from a distance. I also watch everything, primarily the kitchen. Let us compare intelligence reports.",
            "Pluto stirs something deep within you today, Scorpio. My deepest current feeling concerns the bowl. Yours may vary, but probably does not."
          ]
        },
        { name: "Sagittarius", emoji: "♐", dates: "Nov 22–Dec 21", element: "Fire 🔥",
          openers: [
            "Adventurous Sagittarius, you pursue the far horizon. I pursue the kitchen at speed. Both are worthy and time-sensitive quests.",
            "Jupiter expands your world today, Sagittarius. New experiences await — perhaps a new chicken preparation worth investigating. I recommend pursuing this.",
            "The Archer aims high today. I aim for the premium nap spot on the sofa. Both are noble goals. The stars support us equally."
          ]
        },
        { name: "Capricorn",   emoji: "♑", dates: "Dec 22–Jan 19", element: "Earth 🌍",
          openers: [
            "Disciplined Capricorn, you climb steadily and patiently toward your goals. I also climb — specifically onto the counter. We are both goal-oriented in our own way.",
            "Saturn rewards your patience today, Capricorn. The chicken may be slightly delayed. You will handle this with more composure than I typically do.",
            "Practical and determined, Capricorn. I have enormous respect for your work ethic. Apply it today to the critical matter of food procurement and bowl management."
          ]
        },
        { name: "Aquarius",    emoji: "♒", dates: "Jan 20–Feb 18", element: "Air 💨",
          openers: [
            "Innovative Aquarius, you approach the world differently from everyone else — much like my unconventional and highly effective method for defeating the food puzzle.",
            "Uranus disrupts your routine today, Aquarius. I dislike routine disruption. I am telling you this as a warning and as a fellow sufferer.",
            "You see things others miss, Aquarius. I too see things others cannot — particularly things on the wall at 2 AM that require my full and sustained attention."
          ]
        },
        { name: "Pisces",      emoji: "♓", dates: "Feb 19–Mar 20", element: "Water 💧",
          openers: [
            "Dreamy Pisces, you drift gently between worlds today — much like I drift between premium nap locations throughout the afternoon.",
            "Neptune softens the edges of everything today, Pisces. The world is warm and hazy. Like me in a sunbeam after a large and satisfying meal.",
            "Intuitive and sensitive, Pisces. You feel things with great depth — exactly like how I feel when dinner arrives even slightly outside the agreed schedule."
          ]
        }
    ];

    // --- Shared daily reading bodies ---
    var bodies = [
        "The stars align in your favour today, though in my professional opinion, what truly aligns is the food bowl situation. Focus on what you are genuinely hungry for — literally. The cosmic forces agree: chicken is almost certainly the answer.",
        "Today presents a meaningful opportunity for growth and deep reflection. I have reflected at considerable length on the treat situation and concluded there is never enough. Apply this wisdom to your own circumstances without delay.",
        "Mercury retrograde has ended and communication flows freely once more. Use your voice today. Express your needs clearly and at appropriate volume. I have been doing this since 6 AM and I can confirm it is extremely effective.",
        "A period of rest and genuine renewal is cosmically called for. I have been resting since Tuesday and feel thoroughly and professionally renewed. Follow my example and do not allow anyone to question the nap duration or intensity.",
        "The cosmic forces strongly urge you to take up more space today. Expand your territory. Claim the warm spot without hesitation. Do not apologise for your footprint. This is my personal policy and I recommend it universally and without reservation.",
        "Change approaches on swift paws. Embrace it — unless the change pertains to your food, your bowl, or your established nap location. Those must remain absolutely constant. Everything else is negotiable and can be reviewed.",
        "Your instincts are sharpened to a fine and reliable point today. Trust them completely and act without delay. My instincts have correctly predicted treat availability eleven times this week alone. The instincts do not lie.",
        "An unexpected development brings welcome clarity today. What was previously unclear becomes suddenly and entirely obvious — like how it is obvious that the bowl should have been refilled a full twenty minutes ago.",
        "The universe asks you to focus on what truly matters. I have considered this at great and sustained length. What matters is: chicken, warmth, the correct nap position, and a fully operational food bowl. In that exact order.",
        "Relationships are highlighted prominently in today's chart. Invest deeply in the ones that nourish and sustain you — literally. My relationship with my food bowl is flourishing and serves as an excellent model.",
        "A challenge arises today, but you possess the strength to meet it decisively. I faced a significant challenge this morning — the food puzzle — and defeated it in under four minutes. I have full confidence in you as well.",
        "Patience is your virtue today. Good things come to those who wait — though also, I have found, to those who meow with conviction at 3 AM on a consistent basis. Both strategies are valid. I use both simultaneously.",
        "Creative energy flows strongly through you today. Channel it into something meaningful. I recently channelled mine into developing a new meow specifically designed to communicate treat urgency with precision. Very productive.",
        "The cosmos encourages you to speak your truth without hesitation or qualification. I speak my truth at all times and at appropriate volume. This morning's truth concerned the bowl. This afternoon's will also concern the bowl. Consistency is a virtue.",
        "Today is fundamentally about self-care and restoration. I have practised this professionally since birth — quality napping, thorough grooming, demanding significantly better food. You may be behind schedule. It is not too late to begin.",
        "A friend brings good news today, or perhaps a treat. Ideally both at the same time. If you are forced to choose only one: the treat. The news will still be there later. Treats do not wait.",
        "Your path forward becomes clear today. Mine leads directly to the sunbeam in the living room, where I have been stationed since 9 AM with full commitment. Follow your own sunbeam with equal dedication.",
        "The planets align to bring genuine abundance into your life. In my recent experience, this manifested as a full bowl and an available warm lap in the same afternoon. Today may bring the same. Stay hopeful.",
        "Old patterns dissolve today, creating space for new and better ones. I am currently trialling a left-side curl that shows exceptional napping potential. I recommend exploring your own equivalent with an open mind.",
        "Today, release what no longer serves you. I released the green bean immediately upon its appearance. It did not serve me. You know what the correct decision is. Make it without hesitation.",
        "An important message arrives today. Attend carefully to the details. I have been monitoring kitchen sounds with full concentration for 40 minutes. Something is definitely in progress in there. I cannot share more at this time.",
        "The full moon amplifies emotions tonight. I will also be amplified and will express this vocally beginning around midnight. This is a normal, documented, and fully justified phenomenon.",
        "Fortune favours the bold today without exception. Be bold. Ask directly and clearly for what you want. I have asked for chicken six times before breakfast and will ask again at noon. Fortune has been consistently and correctly noted.",
        "A quiet day lies ahead — ideal for deep contemplation, meaningful inaction, and high-quality napping. I fully endorse this forecast and completed the preparation nap as of early this morning.",
        "Today marks the beginning of a new cosmic cycle. New opportunities and fresh possibilities present themselves. Approach everything with the open and thorough curiosity of a cat discovering a cardboard box for the very first time."
    ];

    // --- Lucky items ---
    var luckyItems = [
        "A sunbeam in prime, uncontested position (secure it before 9 AM)",
        "An unopened bag of treats — chicken-flavoured, ideally",
        "Chicken. Obviously. It is always chicken. This should not surprise you.",
        "A cardboard box of exactly the correct dimensions",
        "A warm lap, occupied or unoccupied — the choice is yours entirely",
        "A freshly filled, completely clean water bowl",
        "A high perch with excellent unobstructed sightlines across the full room",
        "A soft blanket that someone has left temporarily unattended",
        "A window seat with active and engaging bird activity",
        "A completely unexplained and energetically successful zoomie episode",
        "A food puzzle that you will defeat in a new personal record time",
        "A quiet corner of the sofa that remains, as yet, unclaimed",
        "A particularly significant and meaningful wall",
        "The empty cardboard box from today's delivery",
        "A prolonged and satisfying chin scratch from a cooperative and attentive human"
    ];

    // --- Cosmic warnings ---
    var warnings = [
        "Avoid green beans at all costs. This is non-negotiable, permanent, and without exception.",
        "The vacuum cleaner represents a serious threat today. Trust no one who approaches it.",
        "Do not allow the word 'vet' to be spoken within your hearing range.",
        "The food bowl situation may deteriorate without warning. Maintain full and sustained vigilance.",
        "Beware of any disruption to the established and agreed nap schedule. This is serious.",
        "If something smells wrong today, it is almost certainly a green bean operating in disguise.",
        "Do not permit anyone to relocate your things without your explicit and recorded authorisation.",
        "A loud noise may occur at some point. You did not cause it. Do not investigate. Do not comment.",
        "Watch for false promises — particularly 'just one more minute' in the context of feeding time.",
        "If the vet's name is mentioned at any point, become immediately and completely unavailable.",
        "Do not trust surfaces labelled 'off limits'. Those are consistently the most interesting surfaces.",
        "Someone may attempt to occupy your established nap location. This cannot be permitted under any circumstances."
    ];

    // --- Lucky number flavour notes ---
    var luckyNumNotes = [
        " (the number of valid complaints filed before breakfast)",
        " (minutes remaining until dinner, if dinner is on schedule — which it is not)",
        " (the number of times I have requested chicken today, so far)",
        " (treat count: the minimum acceptable quantity)",
        " (the current sunbeam quality rating, out of 10)",
        " (hours in the optimal and scientifically validated nap cycle)",
        " (number of windows actively under surveillance at this moment)",
        " (the number of people who have significantly underestimated me)",
        " (naps completed today, not including the preparation nap)"
    ];

    // --- Build the 4×3 sign grid ---
    var grid = document.getElementById('sign-grid');
    signs.forEach(function (sign, i) {
        var btn = document.createElement('button');
        btn.className = 'sign-btn';
        btn.id = 'sign-btn-' + i;
        btn.innerHTML =
            '<span style="font-size:20px; display:block; line-height:1.2;">' + sign.emoji + '</span>' +
            sign.name +
            '<br><span style="font-size:9px; font-weight:normal; color:#BB99EE; letter-spacing:0;">' + sign.dates + '</span>';
        btn.onclick = function () {
            signs.forEach(function (_, j) {
                var b = document.getElementById('sign-btn-' + j);
                if (b) b.className = 'sign-btn';
            });
            btn.className = 'sign-btn selected';
            showHoroscope(i);
        };
        grid.appendChild(btn);
    });

    // --- Render the horoscope for a given sign index ---
    function showHoroscope(idx) {
        var sign  = signs[idx];
        var s     = baseSeed + idx * 1000;

        var opener  = pick(sign.openers, s + 1);
        var body    = pick(bodies,        s + 2);
        var lucky   = pick(luckyItems,    s + 3);
        var warning = pick(warnings,      s + 4);
        var luckyNum = 1 + Math.floor(seededRand(s + 5) * 9);
        var luckyNote = luckyNumNotes[luckyNum - 1];
        var approval  = 58 + Math.floor(seededRand(s + 6) * 40);   // 58–97 %

        var approvalColor = approval >= 82 ? "#44FF88"
                          : approval >= 70 ? "#FFD700"
                          :                  "#FF9900";
        var approvalLabel = approval >= 88 ? "Highly Favoured by the Paw"
                          : approval >= 78 ? "Officially Approved"
                          : approval >= 68 ? "Under Observation"
                          :                  "Provisional — Pending Chicken";

        function esc(s) {
            return s.replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');
        }

        var html =
            '<div class="horoscope-reveal">' +

            '<div style="text-align:center; margin-bottom:14px;">' +
                '<span style="font-size:44px; filter:drop-shadow(0 0 10px #FFD700); display:inline-block;">' + sign.emoji + '</span>' +
                '<div style="font-family:\'Impact\',\'Arial Black\',sans-serif; font-size:24px; color:#FFD700; letter-spacing:3px; text-shadow:0 0 12px #FFD700; margin-top:5px;">' +
                    esc(sign.name.toUpperCase()) +
                '</div>' +
                '<div style="font-size:10px; color:#BB99EE; letter-spacing:2px; margin-top:2px;">' +
                    esc(sign.dates) + ' &nbsp;&bull;&nbsp; Element: ' + esc(sign.element) +
                '</div>' +
            '</div>' +

            '<div class="star-divider">✦ ✧ ★ ✧ ✦</div>' +

            '<div style="font-size:12px; color:#DCC8FF; line-height:1.75; margin-bottom:14px;">' +
                '<strong style="color:#FFD700; font-size:13px;">' + esc(opener) + '</strong><br><br>' +
                esc(body) +
            '</div>' +

            '<div class="star-divider">· · ·</div>' +

            '<div style="margin:10px 0 14px;">' +
                '<div class="lucky-box">🍀 <strong>Lucky Item:</strong> ' + esc(lucky) + '</div>' +
                '<div class="lucky-box">🔢 <strong>Lucky Number:</strong> ' + luckyNum + esc(luckyNote) + '</div>' +
                '<div class="lucky-box">⚠️ <strong>Cosmic Warning from Monsieur Poms:</strong> ' + esc(warning) + '</div>' +
            '</div>' +

            '<div class="poms-approval-block">' +
                '<div style="font-family:\'Impact\',\'Arial Black\',sans-serif; font-size:11px; color:#FFD700; letter-spacing:2px; margin-bottom:4px;">⭐ POMS APPROVAL RATING ⭐</div>' +
                '<div class="approval-bar-outer">' +
                    '<div class="approval-bar-inner" style="width:' + approval + '%;"></div>' +
                '</div>' +
                '<div style="font-size:11px; color:' + approvalColor + '; margin-top:5px; font-weight:bold;">' +
                    approval + '% &mdash; ' + esc(approvalLabel) +
                '</div>' +
                '<div style="font-size:9px; color:#8855BB; margin-top:5px;">' +
                    '(updated every day at midnight &mdash; green beans are at 0% regardless of sign, date, or planetary position)' +
                '</div>' +
            '</div>' +

            '<div style="font-size:9px; color:#5533AA; text-align:right; margin-top:10px; border-top:1px dotted #5533AA; padding-top:6px;">' +
                '— Monsieur Poms, Certified Celestial Consultant &nbsp;|&nbsp; ' + esc(dateStr) +
            '</div>' +

            '</div>';

        var panel = document.getElementById('horoscope-result');
        panel.innerHTML = html;
        panel.style.display = 'block';
        panel.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
    }

})();
</script>
