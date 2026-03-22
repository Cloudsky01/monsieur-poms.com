---
title: "Home"
---

<!-- POST 1 -->
<div style="border: 1px solid #CCC; padding: 10px; background: #F9F9F9; margin-bottom: 20px;">
<h2 style="margin-top: 0;">✨ WELCOME TO MY DOMAIN ✨</h2>
<div style="font-size: 10px; color: #666;">Posted on: January 22, 2010 @ 4:20 PM | Mood: Excited</div>
<hr>
<p>Hi everyone!!!! Welcome to my <strong>BRAND NEW</strong> website. My human decided to make this for me because I am so famous and cute.</p>

<p>Here you will find:</p>
<ul>
<li>Cute pics of me (obviously)</li>
<li>Facts about why I am the best</li>
<li>A guestbook for you to tell me I am pretty</li>
</ul>

<div style="text-align: center; border: 3px dashed #FF00FF; padding: 10px; background: #FFF0F5; margin: 10px;">
<h3>PICTURE OF THE DAY</h3>
<img id="potd-img" src="" alt="Poms" style="width: 100%; max-width: 400px; border: 2px solid #000; display: block; margin: 0 auto;">
<p><em id="potd-caption"></em></p>
<div style="font-size: 10px; color: #888;" id="potd-date"></div>
</div>

<script>
(function() {
    var images = [
        {src: 'poms_sleeping.jpg',    caption: "Me 'working' hard lol!!! xD"},
        {src: 'poms_loaf.jpg',        caption: 'Perfect Orange Loaf mode activated'},
        {src: 'poms_yawn.jpg',        caption: 'RAAAWR!! (Big yawn)'},
        {src: 'poms_stare.jpg',       caption: 'Staring into your soul... do you feel it?'},
        {src: 'poms_box.jpg',         caption: 'If I fits, I sits. This is science.'},
        {src: 'poms_judging.jpg',     caption: 'Judging your life choices (and finding them lacking)'},
        {src: 'poms_profile.jpg',     caption: 'Distinguished Gentleman Profile Shot'},
        {src: 'poms_curious.jpg',     caption: 'Investigating suspicious activity in the vicinity'},
        {src: 'poms_looking_up.jpg',  caption: 'Looking up the ceiling bug situation'},
        {src: 'poms_avatar.jpg',      caption: 'My official portrait. Hang it in the Louvre.'},
        {src: 'poms_drink.jpg',       caption: 'Official POMS Apple Soda Brand Ambassador photo!!!'}
    ];
    var baseURL = 'https://cloudsky01.github.io/monsieur-poms.com/images/';
    var now = new Date();
    var start = new Date(now.getFullYear(), 0, 0);
    var dayOfYear = Math.floor((now - start) / 86400000);
    var pic = images[dayOfYear % images.length];
    document.getElementById('potd-img').src = baseURL + pic.src;
    document.getElementById('potd-caption').textContent = pic.caption;
    var months = ['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec'];
    document.getElementById('potd-date').textContent =
        'Photo of the Day for ' + months[now.getMonth()] + ' ' + now.getDate() + ', ' + now.getFullYear();
})();
</script>

<p>Don't forget to add me to your top 8!!!</p>
<p>xoxo,<br>Monsieur Poms 🐾</p>
</div>

<!-- POST 2 -->
<div style="border: 1px solid #CCC; padding: 10px; background: #F9F9F9; margin-bottom: 20px;">
<h2 style="margin-top: 0;">😡 WHY ARE VEGETABLES?? 😡</h2>
<div style="font-size: 10px; color: #666;">Posted on: January 20, 2010 @ 10:00 AM | Mood: Angry</div>
<hr>
<p>Today my human tried to give me a green bean. A GREEN BEAN. Can you believe it???</p>
<p>I looked at them with my "disappointed eyes" and walked away. I deserve <strong>CHICKEN</strong>. Only chicken.</p>
<p><u>Update:</u> I got chicken later. Victory is mine.</p>
</div>
