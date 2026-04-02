---
title: "Fun Facts"
---

<div style="border: 1px solid #CCC; padding: 10px; background: #F9F9F9;">
<h2 style="margin-top: 0;">💡 FUN FACTS 💡</h2>
<hr>

<ul>
<li>
<font color="red"><strong>DID YOU KNOW?</strong></font>
I am named after a delicious apple soda called "Poms". Look for the spinning bottle on this page!!!
</li>
<br>
<li>
<font color="blue"><strong>DID YOU KNOW?</strong></font>
I am very vocal. I don't just "meow", I hold press conferences about the state of my food bowl.
</li>
<br>
<li>
<font color="green"><strong>DID YOU KNOW?</strong></font>
I am actually a genius. I know exactly how to manipulate humans into giving me treats. It's called "strategy".
</li>
<br>
<li>
<font color="purple"><strong>DID YOU KNOW?</strong></font>
I am NOT fat. I am <strong>tall</strong>. The camera adds 10 pounds, and there are many cameras in this house.<br>
<span style="font-size: 9px;">(Okay, maybe I'm a little bit chonk, but it's muscle!)</span>
</li>
</ul>

<br>
<div style="background-color: #FFFF00; border: 2px dashed red; padding: 10px; text-align: center;">
<blink><strong>!!! RANDOM FACT GENERATOR !!!</strong></blink><br>
<br>
<div style="background-color: #000; color: #00FF00; font-family: 'Courier New', monospace; font-size: 13px; padding: 12px; border: 2px inset #555; min-height: 60px; text-align: left; margin-bottom: 10px; line-height: 1.6;" id="fact-display">
&gt; Click the button to load a FACT about Monsieur Poms!<span class="blink" style="color:#00FF00;">_</span>
</div>
<div style="font-size: 10px; color: #555; margin-bottom: 8px;" id="fact-counter">&nbsp;</div>
<button onclick="showFact()" style="
    background: linear-gradient(to bottom, #FF6600, #CC3300);
    color: #FFFF00;
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 18px;
    letter-spacing: 2px;
    border: 3px outset #FF9900;
    padding: 8px 20px;
    cursor: pointer;
    text-shadow: 1px 1px 0 #000;
    box-shadow: 3px 3px 0 #000;
    margin-bottom: 4px;
" onmouseover="this.style.background='linear-gradient(to bottom, #FF9900, #FF6600)'"
   onmouseout="this.style.background='linear-gradient(to bottom, #FF6600, #CC3300)'">
★ GIMME A FACT ★
</button>
<div style="font-size: 9px; color: #888; margin-top: 4px;">(click multiple times for more facts!)</div>
</div>

<script>
(function() {
    var facts = [
        "I am named after a delicious apple soda called POMS. You can see the spinning bottle right on this very website. You're welcome.",
        "I am NOT fat. I am TALL. The camera adds 10 pounds, and there are many cameras in this house. (Okay, maybe I'm a little bit chonk. But it's muscle!)",
        "I am a professional talker. I don't just 'meow' — I hold full press conferences about the state of my food bowl. Daily.",
        "I am actually a genius. I know exactly how to manipulate humans into giving me treats. It's called 'strategy'. Very advanced stuff.",
        "My official nicknames are: Bine, Binou, Monsieur Chonk, and The Tall One. I prefer Monsieur Poms. I have standards.",
        "I am almost 3 years old. This is relevant because I have almost 3 years of experience in being cute, demanding, and correct.",
        "I hold daily press conferences from my food bowl. The topic is always the same: more food. I am consistent. This is leadership.",
        "I am an unofficial Apple Soda brand ambassador. POMS soda shares my name. I consider this a tremendous honour and I take no royalties.",
        "One of my greatest hobbies is solving puzzles. Another is talking. Another is being cute. I am very accomplished.",
        "My life story is mostly classified. What I can tell you is that it has involved a lot of chicken, several naps, and minimal vegetables.",
        "I have been known to issue formal complaints via meowing at 3 AM. The bowl was half-empty. It was an emergency situation.",
        "I have reviewed the green bean situation multiple times. My verdict remains: no. Never. Not now, not ever. This is final.",
        "The spinning POMS bottle on this website represents my personal brand. I approved this design. It took me 45 minutes of staring at it.",
    ];

    var usedIndices = [];

    window.showFact = function() {
        if (usedIndices.length === facts.length) {
            usedIndices = [];
        }

        var available = facts.map(function(_, i) { return i; }).filter(function(i) {
            return usedIndices.indexOf(i) === -1;
        });
        var pick = available[Math.floor(Math.random() * available.length)];
        usedIndices.push(pick);

        var display = document.getElementById('fact-display');
        var counter = document.getElementById('fact-counter');
        var text = '> ' + facts[pick];
        counter.textContent = 'Fact ' + usedIndices.length + ' of ' + facts.length + ' — collect them all!!';

        // typewriter effect
        display.innerHTML = '';
        var i = 0;
        var cursor = '<span class="blink" style="color:#00FF00;">_</span>';

        function type() {
            if (i < text.length) {
                display.innerHTML = text.slice(0, i + 1) + cursor;
                i++;
                setTimeout(type, 22);
            } else {
                display.innerHTML = text + cursor;
            }
        }
        type();
    };
})();
</script>
</div>
