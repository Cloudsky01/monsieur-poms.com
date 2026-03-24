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
<div id="random-fact-display" style="background: #FFF; border: 2px inset #999; padding: 10px; margin: 10px 0; min-height: 55px; font-weight: bold; color: #000080; font-size: 13px;">
<em>Click the button to reveal a secret fact about moi!!!</em>
</div>
<button onclick="showRandomPomsFact()" style="background: linear-gradient(to bottom, #ff9900, #ff6600); color: #fff; border: 3px outset #cc4400; padding: 8px 20px; font-family: Impact, Arial Black, sans-serif; font-size: 16px; cursor: pointer; font-weight: bold; letter-spacing: 1px;">
!!! CLICK FOR FACT !!!
</button>
<br>
<div id="fact-counter" style="font-size: 10px; margin-top: 8px; color: #555;"></div>
</div>

<script>
var _pomsLastFactIdx = -1;
var _pomsFactsSeen = 0;
var _pomsFacts = [
    "I am named after 'POMS' apple soda!! Look for the spinning bottle on this page. Very appropriate for someone of my caliber. \uD83C\uDF4E",
    "I hold regular press conferences about the state of my food bowl. The attendance is mandatory and the reviews are mostly meows.",
    "I have a genius-level IQ. I know exactly how to manipulate humans into giving me treats. I call it 'strategy'. They call it 'being annoying'. They are wrong.",
    "I am NOT fat. I am TALL. The camera adds 10 pounds and there are MANY cameras in this house. (Okay, maybe slightly chonk. But it is MUSCLE.)",
    "My hobbies include talking, being smart, and being cute. I excel at all three simultaneously.",
    "I once rejected a green bean. My human tried to give me A GREEN BEAN. I deployed the 'disappointed eyes' and walked away. I later received chicken. Victory is mine.",
    "My nicknames include Bine, Binou, Monsieur Chonk, and 'The Tall One'. I accept all of them graciously.",
    "I am an officially recognized Apple Soda Brand Ambassador. The contract was negotiated entirely in treats.",
    "My signature move is the Perfect Loaf Position. Art critics are speechless. Scientists are baffled.",
    "I have filed numerous formal complaints (meows) regarding suspicious ceiling activity. The investigation is ongoing.",
    "Every box in this house is my box. This is the law. I did not make the law, I merely enforce it.",
    "I could be asleep right now, but I choose to judge you instead. This is called work ethic.",
    "My disapproving expression has caused my human to apologise to me on multiple occasions. As it should."
];
function showRandomPomsFact() {
    var available = [];
    for (var i = 0; i < _pomsFacts.length; i++) {
        if (i !== _pomsLastFactIdx) available.push(i);
    }
    var idx = available[Math.floor(Math.random() * available.length)];
    _pomsLastFactIdx = idx;
    _pomsFactsSeen = Math.min(_pomsFactsSeen + 1, _pomsFacts.length);
    document.getElementById('random-fact-display').innerHTML =
        '\u201C' + _pomsFacts[idx] + '\u201D';
    document.getElementById('fact-counter').textContent =
        'Facts discovered: ' + _pomsFactsSeen + ' / ' + _pomsFacts.length + ' \u2014 collect them all!!!';
}
</script>
</div>
