---
title: "Name Analyzer"
---

<style>
.na-header {
    background: linear-gradient(to right, #000066, #000099, #000066);
    color: #FFFF00;
    text-align: center;
    padding: 22px 10px 16px;
    margin: -20px -20px 0 -20px;
    border-bottom: 4px solid #FF00FF;
}
.na-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 34px;
    letter-spacing: 6px;
    text-shadow: 2px 2px 0 #FF0000, 4px 4px 0 #880000;
    margin: 0 0 6px 0;
}
.na-subtitle {
    font-size: 10px;
    color: #AAAAFF;
    letter-spacing: 3px;
    text-transform: uppercase;
}
.na-datebar {
    background: #CC0000;
    color: #FFFF00;
    font-family: 'Courier New', monospace;
    font-size: 11px;
    font-weight: bold;
    letter-spacing: 2px;
    text-align: center;
    padding: 5px 10px;
    margin: 0 -20px;
    border-bottom: 2px solid #880000;
}
.featured-block {
    border: 3px solid #FF00FF;
    background: #FFFAFC;
    margin: 20px 0;
    padding: 0;
    overflow: hidden;
}
.featured-block-title {
    background: #FF00FF;
    color: #FFFFFF;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 14px;
    letter-spacing: 3px;
    padding: 6px 10px;
    text-align: center;
}
.featured-block-body {
    padding: 12px 15px;
}
.analyze-box {
    border: 3px inset #888888;
    background: #F0F0F0;
    padding: 15px;
    margin: 20px 0;
    text-align: center;
}
.analyze-box-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 20px;
    color: #000080;
    letter-spacing: 3px;
    margin: 0 0 10px 0;
    text-shadow: 1px 1px 0 #888888;
}
.name-input {
    font-family: 'Courier New', monospace;
    font-size: 16px;
    padding: 7px 10px;
    border: 3px inset #888888;
    background: #FFFFFF;
    color: #000080;
    width: 200px;
    text-transform: uppercase;
}
.analyze-btn {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 15px;
    letter-spacing: 2px;
    background: linear-gradient(to bottom, #FFFF00, #CCCC00);
    color: #000080;
    border: 3px outset #888888;
    padding: 8px 18px;
    cursor: pointer;
    margin-left: 8px;
    vertical-align: middle;
}
.analyze-btn:hover {
    background: linear-gradient(to bottom, #FFE800, #AAAA00);
    border-style: inset;
}
.certificate {
    border: 3px dashed #000080;
    background: #FFFFF8;
    padding: 14px 18px;
    margin: 10px 0 0 0;
    position: relative;
}
.cert-header {
    text-align: center;
    border-bottom: 2px solid #000080;
    padding-bottom: 10px;
    margin-bottom: 14px;
}
.cert-stamp {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 13px;
    color: #000080;
    letter-spacing: 4px;
    text-transform: uppercase;
}
.cert-meta {
    font-family: 'Courier New', monospace;
    font-size: 10px;
    color: #555;
    margin: 4px 0 0;
}
.score-row {
    display: flex;
    align-items: center;
    margin: 7px 0;
}
.score-label {
    width: 200px;
    flex-shrink: 0;
    font-weight: bold;
    color: #000080;
    font-size: 11px;
    font-family: 'Verdana', sans-serif;
}
.score-bar-bg {
    flex: 1;
    height: 14px;
    background: #CCCCCC;
    border: 1px inset #999999;
    overflow: hidden;
}
.score-bar-fill {
    height: 100%;
    background: linear-gradient(to right, #000099, #3333FF);
}
.score-num {
    width: 34px;
    text-align: right;
    font-family: 'Courier New', monospace;
    font-size: 11px;
    font-weight: bold;
    color: #000080;
    flex-shrink: 0;
    margin-left: 6px;
}
.total-score-line {
    border-top: 2px solid #000080;
    margin-top: 14px;
    padding-top: 12px;
    text-align: center;
    font-family: 'Courier New', monospace;
    font-size: 13px;
    font-weight: bold;
    color: #000080;
}
.verdict-box {
    margin-top: 12px;
    padding: 10px 14px;
    border: 2px solid;
    text-align: center;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 17px;
    letter-spacing: 2px;
}
.poms-note {
    margin-top: 12px;
    font-style: italic;
    font-size: 11px;
    color: #333;
    border-top: 1px dotted #888;
    padding-top: 8px;
    font-family: 'Courier New', monospace;
    line-height: 1.5;
}
.cert-fine-print {
    margin-top: 10px;
    font-size: 9px;
    color: #888;
    text-align: center;
    border-top: 1px dotted #888;
    padding-top: 6px;
    font-family: 'Verdana', sans-serif;
}
.how-it-works {
    border: 2px solid #888888;
    background: #F0F0F0;
    padding: 10px 14px;
    margin: 20px 0;
    font-size: 11px;
    font-family: 'Courier New', monospace;
    color: #333;
    line-height: 1.6;
}
</style>

<div class="na-header">
    <div class="na-title">&#10022; POMS NAME ANALYZER &#10022;</div>
    <div class="na-subtitle">Official Household Staff Evaluation System &mdash; ANALY-PAWS&trade; v2.0</div>
</div>

<div class="na-datebar" id="na-datebar">Loading...</div>

<div class="featured-block">
    <div class="featured-block-title">&#11088; TODAY'S FEATURED ANALYSIS &#11088;</div>
    <div class="featured-block-body" id="featured-body">Loading evaluation...</div>
</div>

<div class="analyze-box">
    <div class="analyze-box-title">ANALYZE YOUR NAME</div>
    <p style="font-size:11px; color:#444; margin:0 0 12px 0; font-family:'Verdana',sans-serif;">
        Monsieur Poms will personally evaluate your name and issue<br>
        an Official Staff Competency Rating. Results are binding.
    </p>
    <input type="text" id="name-input" class="name-input" placeholder="ENTER YOUR NAME" maxlength="30">
    <button class="analyze-btn" id="analyze-btn">ANALYZE</button>
    <div style="font-size:9px; color:#666; margin-top:9px; font-family:'Courier New',monospace;">
        &#9888; DISCLAIMER: Poms is not responsible for hurt feelings. All scores are final and non-negotiable.
    </div>
</div>

<div id="results" style="display:none; margin: 0 0 20px 0;"></div>

<div class="how-it-works">
    <strong style="color:#000080;">HOW IT WORKS:</strong><br>
    Monsieur Poms' proprietary ANALY-PAWS&trade; engine cross-references your name against six
    core household staff competency metrics developed over three years of rigorous feline observation.
    Each metric is scored 0&ndash;100. The Overall Poms Score is the average. A formal verdict is
    then issued. All evaluations are permanent. Poms has your file.
</div>

<script>
(function() {

    // xorshift32 seeded RNG — consistent results for same name
    function Rng(seed) {
        this.s = (seed >>> 0) || 1;
    }
    Rng.prototype.next = function(max) {
        var x = this.s;
        x ^= x << 13;
        x ^= x >>> 17;
        x ^= x << 5;
        this.s = x >>> 0;
        return this.s % (max >>> 0);
    };

    function nameToSeed(name) {
        name = name.toUpperCase().replace(/[^A-Z0-9]/g, '');
        if (!name) return 12345;
        var h = 5381;
        for (var i = 0; i < name.length; i++) {
            h = (((h << 5) >>> 0) + h + name.charCodeAt(i)) >>> 0;
        }
        return h || 1;
    }

    var CATEGORIES = [
        { key: 'canopener', label: '🥫 Can Opener Proficiency' },
        { key: 'lap',       label: '🛋 Lap Cushion Quality' },
        { key: 'chicken',   label: '🍗 Chicken Procurement' },
        { key: 'treats',    label: '🎁 Treat Delivery Speed' },
        { key: 'overnight', label: '🌙 3AM Responsiveness' },
        { key: 'bird',      label: '🐦 Bird Surveillance Aid' }
    ];

    var VERDICTS = [
        { min: 85, text: 'EXEMPLARY STAFF',           color: '#005500', bg: '#EEFFEE',
          summary: 'Poms has reviewed your file and found it acceptable. Do not let this go to your head.' },
        { min: 70, text: 'CONDITIONALLY ACCEPTABLE',  color: '#336600', bg: '#F5FFF0',
          summary: 'You have been cleared for household duties. Probationary period: indefinitely.' },
        { min: 55, text: 'ON PROBATION',               color: '#886600', bg: '#FFFFF0',
          summary: 'A performance improvement plan has been issued. More chicken is the first line item.' },
        { min: 40, text: 'BELOW EXPECTATIONS',         color: '#884400', bg: '#FFF8EE',
          summary: 'Poms has been briefed on this evaluation. He is currently staring at the wall about it.' },
        { min: 25, text: 'UNSATISFACTORY',             color: '#CC0000', bg: '#FFF2F2',
          summary: 'The Disappointed Eyes have been deployed. This is a Level 2 situation. Act accordingly.' },
        { min:  0, text: 'REJECTED',                   color: '#880000', bg: '#FFE8E8',
          summary: 'This file has been forwarded to the Formal Complaints Department. Do not call us. We will not call you either.' }
    ];

    var POMS_NOTES = [
        "The can opener technique was evaluated and found marginally passable. Barely.",
        "I have reviewed this individual's treat delivery record. Response times are unacceptable.",
        "There is potential here. I am choosing not to acknowledge it at this time.",
        "Sources confirm this person has never once woken up at 3 AM without prompting. Disgraceful.",
        "The chicken procurement history suggests adequate effort. More effort is still expected.",
        "I sat on this file for several hours. The lap quality assessment is, unfortunately, accurate.",
        "I am issuing this evaluation under protest. The numbers are what they are.",
        "This individual's bird surveillance assistance has been noted. Noted, not praised.",
        "I have been informed that this person sometimes delivers food before 7 AM. This is the only positive in the file.",
        "Their enthusiasm is not in question. Their competence, however, is very much in question.",
        "The green bean incident has not been forgotten. It factors into the overall score.",
        "I consulted with my legal team (myself) and confirmed: these scores are final.",
        "This evaluation was conducted under strict scientific protocols that I developed and am not sharing.",
        "The overnight complaint response record is abysmal. Three missed meow events in one week.",
        "I note with mild approval that this individual knows where the treat bag is kept.",
        "The sunbeam was not preserved on three separate occasions. This is reflected in the score.",
        "I reviewed this file during my morning loaf session. My conclusions are irrefutable.",
        "A formal letter of concern has been issued. This individual has 24 hours to respond with chicken.",
        "I have factored in the time they laughed at the word 'chonky'. Scores reflect this.",
        "Overall assessment: could be worse. Is still pretty bad. Room for improvement: yes. Will they improve: unclear.",
        "I chose to sit beside this individual rather than on them last Tuesday. This was strategic, not affectionate.",
        "The keyboard was sat on twice in protest during this evaluation period. The subject did not respond appropriately.",
        "An incident involving the vacuum cleaner was reviewed. Poms was not warned. A formal complaint was filed.",
        "This individual has been observed petting other cats on social media. The file is marked accordingly.",
        "The treat bag rustling response time has improved by 0.2 seconds. This does not offset the chicken shortfall.",
        "I headbutted this individual at 5 AM on three occasions. Their response was, at best, medium.",
        "The quality of the morning chin scratch has been reviewed. Technique: adequate. Duration: insufficient.",
        "This person attempted to pick me up without consent on two documented occasions. Unacceptable.",
        "They called me 'little guy'. I am not a little guy. I am horizontally tall. File noted.",
        "Assessment complete. I am going to go sit in a box now and think about this."
    ];

    var FEATURED_NAMES = [
        'Alex','Alice','Bob','Charlie','Chris','Claire','Daniel','David','Emma','Emily',
        'Frank','Grace','Hannah','Henry','Jack','Jake','James','Jane','Jessica','Julia',
        'Kevin','Laura','Liam','Lisa','Mark','Mary','Michael','Olivia','Patrick','Rachel',
        'Ryan','Sarah','Sophie','Steve','Thomas','Tyler','Victoria','William','Zoe','Natalie'
    ];

    function generateAnalysis(name) {
        var seed = nameToSeed(name);
        var rng = new Rng(seed);
        var scores = {};
        var total = 0;
        for (var i = 0; i < CATEGORIES.length; i++) {
            var s = 20 + rng.next(71); // 20–90
            scores[CATEGORIES[i].key] = s;
            total += s;
        }
        var overall = Math.round(total / CATEGORIES.length);

        var verdict = VERDICTS[VERDICTS.length - 1];
        for (var j = 0; j < VERDICTS.length; j++) {
            if (overall >= VERDICTS[j].min) { verdict = VERDICTS[j]; break; }
        }

        var note = POMS_NOTES[rng.next(POMS_NOTES.length)];
        return { name: name, scores: scores, overall: overall, verdict: verdict, note: note };
    }

    function renderCertificate(data, into, isCustom) {
        var now = new Date();
        var MONTHS = ['JAN','FEB','MAR','APR','MAY','JUN','JUL','AUG','SEP','OCT','NOV','DEC'];
        var dateStr = MONTHS[now.getMonth()] + ' ' + now.getDate() + ', ' + now.getFullYear();

        var rows = '';
        for (var i = 0; i < CATEGORIES.length; i++) {
            var cat = CATEGORIES[i];
            var sc = data.scores[cat.key];
            rows +=
                '<div class="score-row">' +
                  '<div class="score-label">' + cat.label + '</div>' +
                  '<div class="score-bar-bg"><div class="score-bar-fill" style="width:' + sc + '%"></div></div>' +
                  '<div class="score-num">' + sc + '</div>' +
                '</div>';
        }

        var customBadge = isCustom
            ? '<div style="color:#CC0000;font-size:9px;letter-spacing:2px;margin-bottom:5px;font-family:\'Verdana\',sans-serif;">' +
              '&#9888; CUSTOM EVALUATION &mdash; RESULTS ARE BINDING &#9888;</div>'
            : '';

        into.innerHTML =
            '<div class="certificate">' +
              '<div class="cert-header">' +
                customBadge +
                '<div class="cert-stamp">Official Staff Evaluation Certificate</div>' +
                '<div class="cert-meta">ISSUED BY: MONSIEUR POMS &nbsp;|&nbsp; DATE: ' + dateStr + '</div>' +
                '<div class="cert-meta" style="margin-top:3px;">RE: <strong style="font-size:13px;">' +
                    escHtml(data.name.toUpperCase()) + '</strong></div>' +
              '</div>' +
              rows +
              '<div class="total-score-line">' +
                'OVERALL POMS SCORE: <span style="font-size:20px; color:#000080;">' + data.overall + '</span> / 100' +
              '</div>' +
              '<div class="verdict-box" style="color:' + data.verdict.color + ';border-color:' + data.verdict.color + ';background:' + data.verdict.bg + ';">' +
                'VERDICT: ' + data.verdict.text +
              '</div>' +
              '<div style="font-size:10px;color:#555;font-family:\'Verdana\',sans-serif;font-style:italic;text-align:center;margin-top:6px;">' +
                data.verdict.summary +
              '</div>' +
              '<div class="poms-note">' +
                '&#x1F4DD; PERSONAL NOTE FROM POMS: &ldquo;' + escHtml(data.note) + '&rdquo;' +
              '</div>' +
              '<div class="cert-fine-print">' +
                'Certified by ANALY-PAWS&trade; v2.0 &bull; Non-transferable &bull; May be revoked without notice &bull; Poms is not liable for emotional distress' +
              '</div>' +
            '</div>';
    }

    function escHtml(s) {
        return s.replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(/"/g,'&quot;');
    }

    // Date bar
    var now = new Date();
    var DAYS = ['SUNDAY','MONDAY','TUESDAY','WEDNESDAY','THURSDAY','FRIDAY','SATURDAY'];
    var MONTHS_LONG = ['JANUARY','FEBRUARY','MARCH','APRIL','MAY','JUNE','JULY','AUGUST','SEPTEMBER','OCTOBER','NOVEMBER','DECEMBER'];
    document.getElementById('na-datebar').textContent =
        '[ ' + DAYS[now.getDay()] + ', ' + MONTHS_LONG[now.getMonth()] + ' ' + now.getDate() + ', ' + now.getFullYear() + ' ]  —  DAILY FEATURED ANALYSIS ACTIVE';

    // Daily featured name
    var dayOfYear = Math.floor((now - new Date(now.getFullYear(), 0, 0)) / 86400000);
    var featuredName = FEATURED_NAMES[dayOfYear % FEATURED_NAMES.length];
    var featuredData = generateAnalysis(featuredName);
    var featuredBody = document.getElementById('featured-body');
    featuredBody.innerHTML =
        '<p style="font-size:11px;color:#660066;font-family:\'Courier New\',monospace;margin:0 0 10px;font-style:italic;">' +
        'Monsieur Poms has personally selected <strong>' + featuredName.toUpperCase() + '</strong> for today\'s ' +
        'featured evaluation. All relevant personnel are advised to review this assessment carefully.' +
        '</p>';
    var featuredCert = document.createElement('div');
    featuredBody.appendChild(featuredCert);
    renderCertificate(featuredData, featuredCert, false);

    // User analysis
    function runAnalysis() {
        var raw = document.getElementById('name-input').value.trim();
        if (!raw) { alert('Please enter a name. Poms is waiting.'); return; }
        var safe = raw.replace(/[^a-zA-Z0-9\s\-]/g, '').trim().substring(0, 30);
        if (!safe) { alert('Poms only accepts standard names. Please try again.'); return; }

        var resultsDiv = document.getElementById('results');
        resultsDiv.style.display = 'block';
        var certDiv = document.createElement('div');
        resultsDiv.innerHTML = '';
        resultsDiv.appendChild(certDiv);
        renderCertificate(generateAnalysis(safe), certDiv, true);
        resultsDiv.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }

    document.getElementById('analyze-btn').addEventListener('click', runAnalysis);
    document.getElementById('name-input').addEventListener('keydown', function(e) {
        if (e.key === 'Enter') runAnalysis();
    });

})();
</script>
