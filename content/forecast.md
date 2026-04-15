---
title: "Poms Weather Station"
---

<style>
.forecast-condition {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 20px;
    color: #FFD700;
    letter-spacing: 2px;
    text-shadow: 2px 2px 0 #000044;
    margin: 8px 0;
    line-height: 1.2;
}

.metric-bar-outer {
    background: #c0c0c0;
    border: 2px inset #888;
    height: 20px;
    width: 100%;
    margin-bottom: 2px;
    position: relative;
    overflow: hidden;
}
.metric-bar-inner {
    height: 100%;
    position: absolute;
    left: 0;
    top: 0;
    animation: barFill 0.6s ease-out forwards;
}
@keyframes barFill {
    from { width: 0%; }
}

.metric-row {
    margin-bottom: 12px;
}
.metric-label-row {
    font-size: 10px;
    font-family: 'Courier New', monospace;
    color: #000;
    font-weight: bold;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 2px;
}

.forecast-day-card {
    border: 2px solid #0000AA;
    background: linear-gradient(to bottom, #d8e8ff, #b0c8ff);
    padding: 6px 3px;
    text-align: center;
    font-size: 10px;
    font-family: 'Verdana', sans-serif;
    flex: 1;
    min-width: 0;
}
.forecast-day-card.today-card {
    background: linear-gradient(to bottom, #ffe880, #ffcc00);
    border-color: #cc6600;
    border-width: 3px;
}

@keyframes weatherFloat {
    0%   { transform: translateY(0px); }
    50%  { transform: translateY(-7px); }
    100% { transform: translateY(0px); }
}
.weather-icon-big {
    animation: weatherFloat 3s ease-in-out infinite;
    display: inline-block;
}

.retro-weather-box {
    background: linear-gradient(135deg, #001050 0%, #003399 55%, #0055bb 100%);
    border: 4px double #88bbff;
    color: #ffffff;
    padding: 16px;
    margin: 15px 0;
    box-shadow: 5px 5px 0 #000;
}

.advisory-box {
    background: #FFFFAA;
    border: 3px solid #FF0000;
    border-left: 8px solid #FF0000;
    padding: 12px;
    margin: 15px 0;
}

.ticker-container {
    background: #000;
    color: #00FF00;
    font-family: 'Courier New', monospace;
    font-size: 11px;
    font-weight: bold;
    padding: 4px 6px;
    border: 2px inset #333;
    margin-bottom: 15px;
}
</style>

<div style="border: 1px solid #CCC; padding: 10px; background: #F9F9F9; margin-bottom: 20px;">

<div style="text-align: center; background: linear-gradient(to right, #000080, #003399, #000080); color: #FFFF00; padding: 14px 10px; margin: -10px -10px 10px -10px; border-bottom: 3px solid #FF00FF;">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 28px; letter-spacing: 4px; text-shadow: 2px 2px 0 #000;">
        📡 POMS WEATHER STATION 📡
    </div>
    <div style="font-size: 11px; margin-top: 4px; color: #aaccff; letter-spacing: 2px;">
        OFFICIAL DAILY CAT-METEOROLOGICAL FORECAST
    </div>
</div>

<div style="text-align: center; font-size: 10px; color: #666; padding: 6px 0 4px;">
    CATEGORY: Meteorological Services &nbsp;|&nbsp; Certified by the Monsieur Poms Academy of Science &nbsp;|&nbsp; Est. 2010
</div>
<hr>

<p style="font-size: 11px; text-align: center; color: #444;">
    <em>The most accurate cat-based weather forecast on the internet.<br>
    All readings taken directly from the food bowl observation post. Forecast updates daily at midnight.</em>
</p>

<div class="ticker-container">
    <marquee scrollamount="4" id="weather-ticker">⚡ LOADING FORECAST DATA... please stand by ⚡</marquee>
</div>

<!-- Main current conditions card -->
<div class="retro-weather-box">
    <div style="display: flex; align-items: center; gap: 15px; flex-wrap: wrap;">
        <div style="text-align: center; flex-shrink: 0;">
            <div class="weather-icon-big" id="weather-icon" style="font-size: 72px; line-height: 1;">⏳</div>
            <div style="font-size: 50px; font-weight: bold; color: #FFD700; font-family: 'Courier New', monospace; margin-top: 4px; text-shadow: 0 0 10px #FFD700;" id="weather-temp">--°P</div>
            <div style="font-size: 9px; color: #99bbdd; letter-spacing: 1px;">Pom Degrees (°P)</div>
        </div>
        <div style="flex: 1; min-width: 180px;">
            <div id="weather-date" style="font-size: 10px; color: #99bbdd; letter-spacing: 1px; margin-bottom: 6px; text-transform: uppercase;"></div>
            <div class="forecast-condition" id="weather-condition">LOADING CONDITIONS...</div>
            <div id="weather-desc" style="font-size: 11px; color: #cce0ff; margin: 10px 0; line-height: 1.6;"></div>
            <div style="display: flex; flex-wrap: wrap; gap: 10px; font-size: 10px; color: #aaccff; margin-top: 8px; border-top: 1px solid #335588; padding-top: 8px;">
                <span>💧 Fluffiness: <strong id="weather-humidity" style="color: #fff;"></strong></span>
                <span>🌬️ Zoomie Wind: <strong id="weather-wind" style="color: #fff;"></strong></span>
                <span>✨ Vibe Index: <strong id="weather-vibe" style="color: #FFD700;"></strong></span>
            </div>
        </div>
    </div>
</div>

<!-- Daily metrics -->
<div style="background: #F0F0F0; border: 3px double #666; padding: 12px; margin: 15px 0;">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 15px; color: #000080; margin-bottom: 12px; letter-spacing: 1px; border-bottom: 2px solid #000080; padding-bottom: 4px;">
        📊 TODAY'S CONDITIONS REPORT
    </div>
    <div id="metrics-container"></div>
</div>

<!-- 7-day outlook -->
<div style="margin: 15px 0;">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 15px; color: #000080; margin-bottom: 8px; letter-spacing: 1px; border-bottom: 2px solid #000080; padding-bottom: 4px;">
        🗓️ 7-DAY POMS OUTLOOK
    </div>
    <div id="seven-day-container" style="display: flex; gap: 4px;"></div>
    <div style="font-size: 9px; color: #999; margin-top: 4px; text-align: right;">
        Temperatures in °P (Pom Degrees). Subject to food bowl influence.
    </div>
</div>

<!-- Advisory -->
<div class="advisory-box" id="advisory-box">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 14px; color: #CC0000; margin-bottom: 8px; letter-spacing: 1px;">
        ⚠️ OFFICIAL WEATHER ADVISORY FROM MONSIEUR POMS
    </div>
    <div id="advisory-text" style="font-size: 12px; font-style: italic; color: #000080; line-height: 1.7;"></div>
    <div style="font-size: 9px; color: #888; margin-top: 10px; text-align: right; border-top: 1px dotted #ccc; padding-top: 6px;">
        — Chief Meteorologist M. Poms &nbsp;|&nbsp; Poms Weather Station, Food Bowl Division
    </div>
</div>

<hr>
<p style="font-size: 10px; color: #888; text-align: center; line-height: 1.6;">
    <em>Poms Weather Station accepts no liability for inaccurate forecasts.<br>
    In the event of bowl-empty conditions, contact your nearest food dispenser immediately.<br>
    Green bean conditions will not be forecast. Not now. Not ever. This is final.</em>
</p>

</div>

<script>
(function () {

    // --- Seeded deterministic random ---
    function seededRand(s) {
        var x = Math.sin(s * 127.1 + 311.7) * 43758.5453123;
        return x - Math.floor(x);
    }

    function getDayOfYear(date) {
        var start = new Date(date.getFullYear(), 0, 0);
        return Math.floor((date - start) / 86400000);
    }

    var now  = new Date();
    var doy  = getDayOfYear(now);
    var seed = now.getFullYear() * 1000 + doy;

    // --- Weather conditions ---
    var conditions = [
        {
            icon: "☀️",
            name: "SUNNY WITH SCATTERED NAPS",
            desc: "Ideal conditions for premium sunbeam occupation. High nap productivity expected throughout the day. Treat probability is elevated.",
            tempHigh: 88, tempLow: 72,
            humidity: "92% floof", wind: "2 mph (imperceptible)", vibe: "Transcendent",
            chicken: 85, nap: 94, complaint: 18, surveillance: 52, judgment: 35,
            advisory: "Excellent day for sunbeam claiming. I recommend securing the prime living room spot no later than 9 AM before the afternoon shift moves in. Chicken forecast is very promising. Green beans remain categorically refused."
        },
        {
            icon: "⛅",
            name: "PARTLY CLOUDY, CHANCE OF ZOOMIES",
            desc: "Partly overcast with unpredictable bursts of high-velocity hallway activity. Zoomie episodes may occur with little to no warning, particularly after 10 PM.",
            tempHigh: 79, tempLow: 65,
            humidity: "74% floof", wind: "18 mph (ZOOMIE GUSTS)", vibe: "Unpredictable",
            chicken: 70, nap: 65, complaint: 45, surveillance: 68, judgment: 55,
            advisory: "Residents should be aware of sudden zoomie events tonight. No explanation will be provided. The cause is known only to me and I am not sharing it at this time. Do not follow me."
        },
        {
            icon: "☁️",
            name: "HEAVY FOOD BOWL OVERCAST",
            desc: "Dense cloud cover driven by an ongoing bowl shortage situation. Visibility critically low near the kitchen. Formal complaints expected throughout the afternoon.",
            tempHigh: 65, tempLow: 55,
            humidity: "88% floof", wind: "6 mph (sighing)", vibe: "Disgruntled",
            chicken: 22, nap: 48, complaint: 91, surveillance: 40, judgment: 78,
            advisory: "The bowl situation is critical. I have filed three complaints this morning and will be issuing more throughout the day. Today is not the day to offer green beans. This is your official warning."
        },
        {
            icon: "⛈️",
            name: "THUNDERSTORM OF COMPLAINTS",
            desc: "Severe complaint activity developing overnight. Multiple meow fronts converging near the food bowl. 3 AM vocalization alert is in full effect.",
            tempHigh: 61, tempLow: 50,
            humidity: "96% floof", wind: "22 mph (COMPLAINT WINDS)", vibe: "Formal Grievance",
            chicken: 10, nap: 30, complaint: 99, surveillance: 35, judgment: 95,
            advisory: "SEVERE COMPLAINT ADVISORY. Food bowl conditions have deteriorated to critical levels. I will be meowing at 3 AM. This is not a threat — this is a forecast. Prepare accordingly."
        },
        {
            icon: "🟫",
            name: "PERFECT LOAF CONDITIONS",
            desc: "Optimum loaf formation weather. All limbs fully tuckable. Ambient warmth sufficient for extended loaf maintenance. Do not tap the loaf.",
            tempHigh: 76, tempLow: 64,
            humidity: "68% floof", wind: "1 mph (loaf-safe)", vibe: "Fully Tucked",
            chicken: 72, nap: 98, complaint: 25, surveillance: 20, judgment: 42,
            advisory: "Today I have achieved the loaf. I am bread. Do not tap me. Do not say my name. I am in a deep loaf meditation. Unless there is chicken — in which case I can be interrupted."
        },
        {
            icon: "❄️",
            name: "CRISP AND JUDGEMENTAL",
            desc: "Cool, clear conditions ideal for peak judgemental activity. Side-eye probability elevated. Humans advised to act normally and avoid suspicious behaviour.",
            tempHigh: 58, tempLow: 44,
            humidity: "52% floof", wind: "10 mph (dismissive)", vibe: "Withering",
            chicken: 60, nap: 75, complaint: 52, surveillance: 88, judgment: 99,
            advisory: "I have been watching. I am aware of everything. The 3 PM couch incident will not be forgotten. Chicken delivery at this time is the only known path to diplomatic restoration."
        },
        {
            icon: "🌫️",
            name: "FOGGY WITH DINNER DEPRESSION",
            desc: "Low-visibility conditions caused by prolonged dinner delay. Morale at a post-food-puzzle low. Outlook improving only if immediate action is taken.",
            tempHigh: 66, tempLow: 57,
            humidity: "82% floof", wind: "4 mph (mournful)", vibe: "Gloomy",
            chicken: 15, nap: 55, complaint: 82, surveillance: 30, judgment: 65,
            advisory: "Dinner was supposed to happen. It did not happen. We are now operating in a dinner deficit situation. I have issued a formal statement and will be staring at the food cupboard until conditions improve."
        },
        {
            icon: "🌈",
            name: "CLEARING WITH CHICKEN EXPECTED",
            desc: "Morning overcast giving way to positive chicken developments. Outlook dramatically improving as of the afternoon. Sunbeam quality above average.",
            tempHigh: 80, tempLow: 66,
            humidity: "58% floof", wind: "7 mph (hopeful)", vibe: "Cautiously Optimistic",
            chicken: 91, nap: 80, complaint: 28, surveillance: 55, judgment: 40,
            advisory: "I have detected early signs of chicken in the kitchen area. This is very promising and I will be supervising from my food bowl vantage point. This is, potentially, a good day. I am cautiously optimistic."
        },
        {
            icon: "🌲",
            name: "EXTREME SURVEILLANCE CONDITIONS",
            desc: "Exceptionally high bird activity detected outside the window. Full surveillance deployment activated. Updates will be provided when the situation develops.",
            tempHigh: 74, tempLow: 60,
            humidity: "63% floof", wind: "9 mph (irrelevant)", vibe: "Hyper-Focused",
            chicken: 65, nap: 30, complaint: 40, surveillance: 99, judgment: 70,
            advisory: "There is a bird. I have been tracking it for three hours. I cannot share my full findings at this time, but the situation is developing. Do not move me from the window. This is my post."
        },
        {
            icon: "🌪️",
            name: "HIGH ZOOMIE WINDS OVERNIGHT",
            desc: "Strong zoomie systems developing throughout the evening. High-velocity hallway activity forecast between 10 PM and 1 AM. Source remains classified.",
            tempHigh: 77, tempLow: 62,
            humidity: "71% floof", wind: "35 mph (FULL ZOOMIE)", vibe: "Chaotic",
            chicken: 68, nap: 45, complaint: 58, surveillance: 75, judgment: 50,
            advisory: "ZOOMIE WARNING ISSUED. I will be running at full speed tonight for reasons I cannot disclose. This is normal. This is fine. If you hear a loud thump, it was nothing. Go back to sleep."
        },
        {
            icon: "🌦️",
            name: "MODERATE TREAT SHOWER",
            desc: "Periodic treat delivery expected throughout the day. Conditions ideal for strategic manipulation of humans into producing snacks.",
            tempHigh: 82, tempLow: 68,
            humidity: "60% floof", wind: "5 mph (gentle)", vibe: "Strategically Pleased",
            chicken: 78, nap: 82, complaint: 22, surveillance: 48, judgment: 38,
            advisory: "Today's treat probability is HIGH. I have deployed my most effective strategy: being extremely cute for short bursts followed by judgemental pauses. Results: excellent. Operation continues."
        },
        {
            icon: "👁️",
            name: "PROLONGED WALL-STARING EVENT",
            desc: "A significant wall-staring event is underway. Duration unknown. What I see cannot be explained to humans at this time or any future time.",
            tempHigh: 71, tempLow: 59,
            humidity: "67% floof", wind: "3 mph (existential)", vibe: "Cryptic",
            chicken: 55, nap: 60, complaint: 35, surveillance: 62, judgment: 60,
            advisory: "I have been staring at the wall for 14 minutes. I cannot explain what I see. I cannot explain why. What I can tell you is that it is very important and you should probably leave the room."
        },
        {
            icon: "🌙",
            name: "3 AM COMPLAINT SYSTEM ACTIVE",
            desc: "Overnight meow front moving through the hallway. Complaint system fully operational. Bowl conditions: not ideal. Humans: advised.",
            tempHigh: 63, tempLow: 50,
            humidity: "77% floof", wind: "12 mph (nocturnal)", vibe: "Relentlessly Awake",
            chicken: 30, nap: 20, complaint: 95, surveillance: 55, judgment: 80,
            advisory: "I was awake at 3 AM, 3:15 AM, 3:32 AM, and 4:01 AM. Each time, the bowl situation had not improved. I issued appropriate vocal statements. This is not a complaint. This is a public record."
        },
        {
            icon: "🌸",
            name: "EXCEPTIONAL CHICKEN CONDITIONS",
            desc: "Rare high-pressure chicken system bringing the best atmospheric conditions in recent memory. Historic nap quality anticipated. This is a special day.",
            tempHigh: 95, tempLow: 78,
            humidity: "55% floof", wind: "4 mph (satisfied)", vibe: "Peak Monsieur",
            chicken: 99, nap: 97, complaint: 5, surveillance: 45, judgment: 20,
            advisory: "Today is exceptional. The chicken was on time. The sunbeam is optimal. My nap last night was a masterclass in rest. I am, at this moment, at peak Monsieur. Do not ruin it. Do not mention the vet."
        }
    ];

    // --- Get today's condition ---
    var cond = conditions[doy % conditions.length];

    // --- Small daily variance in metrics via seeded random ---
    function metricVal(base, variance, offset) {
        return Math.max(1, Math.min(99, base + Math.floor((seededRand(seed + offset) - 0.5) * variance)));
    }
    var metrics = {
        chicken:     metricVal(cond.chicken,     14, 1),
        nap:         metricVal(cond.nap,         12, 2),
        complaint:   metricVal(cond.complaint,   18, 3),
        surveillance:metricVal(cond.surveillance,14, 4),
        judgment:    metricVal(cond.judgment,    16, 5)
    };

    // --- Current temperature ---
    var currentTemp = cond.tempLow + Math.floor(seededRand(seed + 99) * (cond.tempHigh - cond.tempLow + 1));

    // --- Date string ---
    var dayNames  = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
    var monthNames= ["January","February","March","April","May","June","July","August","September","October","November","December"];
    var dateStr   = dayNames[now.getDay()] + ", " + monthNames[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear();

    // --- Populate main card ---
    document.getElementById('weather-icon').textContent      = cond.icon;
    document.getElementById('weather-condition').textContent = cond.name;
    document.getElementById('weather-desc').textContent      = cond.desc;
    document.getElementById('weather-temp').textContent      = currentTemp + "°P";
    document.getElementById('weather-humidity').textContent  = cond.humidity;
    document.getElementById('weather-wind').textContent      = cond.wind;
    document.getElementById('weather-vibe').textContent      = cond.vibe;
    document.getElementById('weather-date').textContent      = dateStr;
    document.getElementById('advisory-text').textContent     = cond.advisory;

    // --- Ticker ---
    document.getElementById('weather-ticker').textContent =
        "⚡ " + dateStr.toUpperCase() + " ⚡ CONDITIONS: " + cond.name +
        " ⚡ TEMP: " + currentTemp + "°P ⚡ VIBE: " + cond.vibe.toUpperCase() +
        " ⚡ ZOOMIE WIND: " + cond.wind.toUpperCase() + " ⚡ CHICKEN OUTLOOK: " +
        (metrics.chicken >= 70 ? "PROMISING" : metrics.chicken >= 40 ? "UNCERTAIN" : "CRITICAL") + " ⚡";

    // --- Metrics bars ---
    var metricDefs = [
        { key: "chicken",      label: "🍗 CHICKEN SATISFACTION INDEX", color: "#DD5500", hi: "Fully Satisfied",    lo: "Critically Depleted" },
        { key: "nap",          label: "💤 NAP QUALITY RATING",         color: "#5533CC", hi: "Championship Nap",  lo: "Restless & Displeased" },
        { key: "complaint",    label: "😤 COMPLAINT VOLUME",           color: "#CC0000", hi: "Maximum Grievance", lo: "Unusually Quiet" },
        { key: "surveillance", label: "🔭 SURVEILLANCE ACTIVITY",      color: "#005500", hi: "Full Monitor Mode", lo: "Off Duty" },
        { key: "judgment",     label: "😾 JUDGMENT CAPACITY",          color: "#770077", hi: "Peak Judgement",    lo: "Briefly Forgiving" }
    ];
    var mc = document.getElementById('metrics-container');
    metricDefs.forEach(function (m) {
        var v   = metrics[m.key];
        var row = document.createElement('div');
        row.className = 'metric-row';
        var status = v >= 70 ? m.hi : (v <= 30 ? m.lo : "Moderate");
        row.innerHTML =
            '<div class="metric-label-row">' +
                '<span>' + m.label + '</span>' +
                '<span style="color:' + m.color + '; font-size:11px;">' + v + '% &mdash; ' + status + '</span>' +
            '</div>' +
            '<div class="metric-bar-outer">' +
                '<div class="metric-bar-inner" style="width:' + v + '%; background: linear-gradient(to right, ' + m.color + 'aa, ' + m.color + ');"></div>' +
            '</div>';
        mc.appendChild(row);
    });

    // --- 7-day forecast ---
    var sdc = document.getElementById('seven-day-container');
    for (var i = 0; i < 7; i++) {
        var d     = new Date(now.getFullYear(), now.getMonth(), now.getDate() + i);
        var dDoy  = getDayOfYear(d);
        var dSeed = d.getFullYear() * 1000 + dDoy;
        var dCond = conditions[dDoy % conditions.length];
        var dTemp = dCond.tempLow + Math.floor(seededRand(dSeed + 99) * (dCond.tempHigh - dCond.tempLow + 1));
        var label = i === 0 ? "TODAY" : dayNames[d.getDay()].substring(0, 3).toUpperCase();

        var words = dCond.name.split(' ');
        var short = words.slice(0, 3).join(' ') + (words.length > 3 ? '…' : '');

        var card = document.createElement('div');
        card.className = 'forecast-day-card' + (i === 0 ? ' today-card' : '');
        card.innerHTML =
            '<div style="font-weight:bold; font-size:10px; border-bottom:1px solid #6688bb; padding-bottom:3px; margin-bottom:4px;">' + label + '</div>' +
            '<div style="font-size:22px; line-height:1.3;">' + dCond.icon + '</div>' +
            '<div style="font-size:9px; margin:3px 0; line-height:1.4; color:#000066;">' + short + '</div>' +
            '<div style="font-size:12px; font-weight:bold; color:#000080;">' + dTemp + '°P</div>';
        sdc.appendChild(card);
    }

})();
</script>
