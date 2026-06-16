---
title: "PawBay Daily Auction"
---

<style>
.pb-header {
    background: linear-gradient(to bottom, #0064d2, #003087);
    padding: 10px 15px 0;
    margin: -20px -20px 0 -20px;
}
.pb-logo {
    font-family: Arial Black, sans-serif;
    font-size: 30px;
    font-weight: 900;
    letter-spacing: -1px;
    line-height: 1;
}
.pb-logo .l-p { color: #e53238; }
.pb-logo .l-a1 { color: #f5af02; }
.pb-logo .l-w { color: #86b817; }
.pb-logo .l-b { color: #ffffff; }
.pb-logo .l-a2 { color: #f5af02; }
.pb-logo .l-y { color: #86b817; }
.pb-topbar {
    display: flex; justify-content: space-between; align-items: center;
    padding-bottom: 6px;
}
.pb-topbar-right { color: #aac8ff; font-size: 11px; font-family: Arial, sans-serif; }
.pb-topbar-right span { color: #fff; text-decoration: underline; cursor: pointer; margin-left: 8px; }
.pb-subnav {
    background: #f0f4ff;
    border-top: 2px solid #e53238;
    padding: 4px 0 4px 15px;
    font-size: 11px;
    color: #333;
    font-family: Arial, sans-serif;
    margin: 0 -20px;
}
.pb-breadcrumb { color: #555; }
.pb-breadcrumb a { color: #0064d2; text-decoration: none; }
.pb-section-hdr {
    background: #f0f0f0;
    border-top: 2px solid #ccc;
    border-bottom: 1px solid #ccc;
    padding: 6px 10px;
    font-weight: bold;
    font-size: 13px;
    color: #333;
    font-family: Arial, sans-serif;
    margin: 16px -20px 0 -20px;
}
.pb-price {
    font-size: 28px;
    font-weight: bold;
    color: #117a00;
    font-family: 'Courier New', monospace;
}
.pb-bid-btn {
    background: linear-gradient(to bottom, #3b9ddd, #0064d2);
    color: #fff;
    border: 1px solid #003087;
    padding: 8px 0;
    font-size: 14px;
    font-weight: bold;
    cursor: pointer;
    width: 100%;
    border-radius: 4px;
    margin-bottom: 6px;
    font-family: Arial, sans-serif;
}
.pb-bid-btn:hover { background: linear-gradient(to bottom, #5ab4f0, #1a7ddb); }
.pb-buynow-btn {
    background: linear-gradient(to bottom, #ffd700, #e8b800);
    color: #333;
    border: 1px solid #c8a000;
    padding: 7px 0;
    font-size: 13px;
    font-weight: bold;
    cursor: pointer;
    width: 100%;
    border-radius: 4px;
    font-family: Arial, sans-serif;
}
.pb-buynow-btn:hover { background: linear-gradient(to bottom, #ffe033, #f5c400); }
.pb-countdown {
    font-family: 'Courier New', monospace;
    font-size: 24px;
    color: #cc0000;
    font-weight: bold;
    letter-spacing: 3px;
}
.pb-seller-box {
    background: #fffbe6;
    border: 1px solid #e0c800;
    padding: 8px;
    font-size: 11px;
    font-family: Arial, sans-serif;
    margin-top: 8px;
    border-radius: 3px;
}
.pb-specs-table td {
    padding: 5px 8px;
    font-size: 12px;
    border-bottom: 1px solid #eee;
    vertical-align: top;
    font-family: Arial, sans-serif;
}
.pb-specs-table tr:nth-child(odd) td { background: #f9f9f9; }
.pb-specs-table td:first-child { font-weight: bold; color: #555; width: 40%; }
.pb-hist-table { border-collapse: collapse; width: 100%; font-size: 12px; font-family: Arial, sans-serif; }
.pb-hist-table th { background: #e0e8f8; padding: 5px 8px; border: 1px solid #bcd; font-weight: bold; color: #333; }
.pb-hist-table td { padding: 5px 8px; border-bottom: 1px solid #eee; color: #333; }
.pb-hist-table tr:nth-child(even) td { background: #f5f8ff; }
.pb-qa-item { margin-bottom: 12px; font-size: 13px; font-family: Arial, sans-serif; }
.pb-qa-q { font-weight: bold; color: #0064d2; margin-bottom: 3px; }
.pb-qa-q::before { content: "Q: "; }
.pb-qa-a { color: #333; padding-left: 12px; border-left: 3px solid #e53238; line-height: 1.6; }
.pb-qa-a::before { content: "A: "; font-weight: bold; color: #555; }
.pb-more-grid { display: flex; flex-wrap: wrap; gap: 8px; padding: 10px 0; }
.pb-more-item {
    width: 80px; text-align: center; font-size: 10px; font-family: Arial, sans-serif;
    border: 1px solid #ddd; padding: 4px; cursor: pointer; color: #0064d2;
    text-decoration: underline;
}
.pb-more-item img { width: 72px; height: 55px; object-fit: cover; display: block; margin-bottom: 3px; }
.pb-condition-badge {
    display: inline-block;
    background: #e8f4e8;
    border: 1px solid #aaddaa;
    color: #226622;
    font-size: 11px;
    padding: 2px 7px;
    border-radius: 10px;
    font-family: Arial, sans-serif;
    font-weight: bold;
}
.pb-condition-badge.used { background: #fff4e0; border-color: #ddcc88; color: #886600; }
.pb-condition-badge.rare { background: #f0e0ff; border-color: #cc88ff; color: #660099; }
#pb-modal-overlay {
    display: none; position: fixed; top: 0; left: 0; right: 0; bottom: 0;
    background: rgba(0,0,0,0.55); z-index: 9998;
}
#pb-modal {
    display: none; position: fixed; top: 50%; left: 50%;
    transform: translate(-50%,-50%);
    background: #fff; border: 3px solid #cc0000;
    padding: 20px 24px; width: 300px; z-index: 9999;
    box-shadow: 6px 6px 20px rgba(0,0,0,0.5);
    text-align: center; font-family: Arial, sans-serif;
}
#pb-modal-title { font-weight: bold; color: #cc0000; font-size: 14px; margin-bottom: 10px; }
#pb-modal-text { font-size: 13px; color: #333; line-height: 1.65; font-style: italic; }
#pb-modal-close {
    margin-top: 14px; padding: 6px 22px;
    background: #0064d2; color: #fff;
    border: none; cursor: pointer; border-radius: 3px;
    font-size: 13px; font-weight: bold;
}
</style>

<!-- PawBay Header -->
<div class="pb-header">
    <div class="pb-topbar">
        <div class="pb-logo">
            <span class="l-p">P</span><span class="l-a1">a</span><span class="l-w">w</span><span class="l-b">B</span><span class="l-a2">a</span><span class="l-y">y</span>
            <span style="color:#aac8ff; font-size:13px; font-weight:normal; font-family:Arial; vertical-align:middle;">&nbsp;Daily Auction</span>
        </div>
        <div class="pb-topbar-right">
            Daily since 2010
            <span>Sign In</span>
            <span>Register</span>
            <span>Help</span>
        </div>
    </div>
</div>
<div class="pb-subnav">
    <span class="pb-breadcrumb">
        🐾 PawBay &rsaquo; Cats &rsaquo; Monsieur Poms &rsaquo; <span id="pb-category">Loading…</span>
    </span>
</div>

<!-- Item Title -->
<div style="padding: 12px 0 6px; font-family: Arial, sans-serif;">
    <div style="font-size: 10px; color: #999;">Item # <span id="pb-item-num">—</span></div>
    <h2 id="pb-title" style="margin: 4px 0 3px; font-size: 18px; color: #222; font-family: Arial, sans-serif; text-decoration: none; font-weight: bold;">Loading…</h2>
    <div id="pb-subtitle" style="font-size: 12px; color: #666; line-height: 1.4;"></div>
</div>

<!-- Main 2-column layout -->
<table width="100%" cellpadding="0" cellspacing="8" style="font-family: Arial, sans-serif; margin-bottom: 4px;">
<tr valign="top">
    <td width="210">
        <!-- Photo -->
        <div style="border: 2px solid #bbb; padding: 3px; background: #fff; text-align: center;">
            <img id="pb-photo" src="" alt="Item" style="width: 200px; height: 165px; object-fit: cover; display: block;">
        </div>
        <div style="font-size: 10px; color: #999; text-align: center; margin-top: 2px;">📷 Official Poms Archive Photo</div>

        <!-- Shipping -->
        <div style="margin-top: 8px; background: #f5fbff; border: 1px solid #aaccee; padding: 7px; font-size: 11px; border-radius: 3px;">
            <strong>📦 Shipping:</strong><br>
            <span id="pb-ship-short" style="color: #333; line-height: 1.5;"></span>
        </div>

        <!-- Returns -->
        <div style="margin-top: 5px; background: #fff5f5; border: 1px solid #ffaaaa; padding: 6px; font-size: 10px; border-radius: 3px;">
            <strong style="color: #aa0000;">⚠ Returns:</strong><br>
            <span id="pb-returns-short" style="color: #660000;"></span>
        </div>
    </td>

    <td>
        <!-- Bid box -->
        <table width="100%" cellpadding="0" cellspacing="0" style="border: 2px solid #ccc; border-radius: 4px; overflow: hidden;">
            <tr>
                <td style="background: #f0f0f0; padding: 6px 10px; border-bottom: 1px solid #ccc;">
                    <span id="pb-cond-badge" class="pb-condition-badge">New</span>
                    &nbsp;<span id="pb-cond-note" style="font-size: 11px; color: #666;"></span>
                </td>
            </tr>
            <tr>
                <td style="padding: 10px;">
                    <div style="font-size: 12px; color: #555;">Current Bid:</div>
                    <div id="pb-current-bid" class="pb-price">$0.00</div>
                    <div style="font-size: 11px; color: #0064d2; margin-top: 2px;">
                        [<span id="pb-num-bids">0</span> bid<span id="pb-bids-s">s</span>]
                        &nbsp;—&nbsp; <span style="color: #888;">Starts at <span id="pb-start-bid">$0.00</span></span>
                    </div>
                </td>
            </tr>
            <tr>
                <td style="padding: 4px 10px 10px;">
                    <button class="pb-bid-btn" onclick="pbPlaceBid()">🔨 Place Bid</button>
                    <button class="pb-buynow-btn" onclick="pbBuyNow()">⚡ Buy It Now — <span id="pb-buynow-price">$0.00</span></button>
                </td>
            </tr>
            <tr>
                <td style="padding: 0 10px 10px; border-top: 1px solid #e8e8e8; padding-top: 8px;">
                    <div style="font-size: 12px; color: #555;">⏱ Auction Ends In:</div>
                    <div id="pb-countdown" class="pb-countdown">00:00:00</div>
                    <div style="font-size: 10px; color: #999; margin-top: 2px;">Midnight tonight — bid while you can!</div>
                </td>
            </tr>
            <tr>
                <td class="pb-seller-box" style="margin: 0; border-radius: 0; border-left: none; border-right: none; border-bottom: none;">
                    <strong>Seller:</strong> <span style="color: #0064d2; font-weight: bold;">monsieur_poms_official</span><br>
                    <span style="color: #f5af02; font-size: 13px;">★★★★★</span>
                    <span style="font-size: 11px;"> 99.8% positive (2,847 ratings)</span><br>
                    <span style="font-size: 10px; color: #777;">Member since: 2010 &nbsp;|&nbsp; 🐾 PawBay Top Seller</span>
                </td>
            </tr>
        </table>
    </td>
</tr>
</table>

<!-- Description -->
<div class="pb-section-hdr">📋 Item Description</div>
<div id="pb-desc" style="padding: 12px 4px; font-size: 13px; line-height: 1.8; color: #333; font-family: Arial, sans-serif;"></div>

<!-- Specs -->
<div class="pb-section-hdr">📊 Item Specifics</div>
<div style="padding: 8px 0;">
    <table class="pb-specs-table" id="pb-specs" width="100%"></table>
</div>

<!-- Shipping full -->
<div class="pb-section-hdr">📦 Shipping &amp; Returns</div>
<div id="pb-ship-full" style="padding: 10px 4px; font-size: 13px; color: #333; font-family: Arial, sans-serif; line-height: 1.7;"></div>

<!-- Bid history -->
<div class="pb-section-hdr">📈 Bid History (<span id="pb-bid-count-hdr">0</span> bids)</div>
<div style="padding: 8px 0;" id="pb-bid-history-wrap">
    <table class="pb-hist-table" id="pb-bid-history">
        <thead><tr><th>Bidder</th><th>Bid Amount</th><th>Time</th></tr></thead>
        <tbody id="pb-bid-tbody"></tbody>
    </table>
    <div id="pb-no-bids" style="display:none; font-size:13px; color:#888; padding:10px 4px; font-family:Arial,sans-serif; font-style:italic;">No bids yet. Be the first! (Your bid will be rejected, but still.)</div>
</div>

<!-- Q&A -->
<div class="pb-section-hdr">❓ Questions &amp; Answers from the Community</div>
<div id="pb-qa" style="padding: 12px 4px;"></div>

<!-- More from seller -->
<div class="pb-section-hdr">🏪 More From This Seller</div>
<div class="pb-more-grid" id="pb-more"></div>

<!-- Footnote -->
<div style="margin-top: 16px; padding-top: 10px; border-top: 1px dashed #ccc; text-align: center; font-size: 10px; color: #999; font-family: Arial, sans-serif; line-height: 1.7;">
    * PawBay is a Monsieur Poms personal trading platform and is not affiliated with any actual marketplace.
    All listings are real in the sense that Poms endorses them. All bids are final and also meaningless.
    Poms is not responsible for emotional outcomes. PawBay reserves the right to reject all bids for any reason or no reason.
    This is consistent with his general policy on everything.
</div>

<!-- Modal -->
<div id="pb-modal-overlay" onclick="pbCloseModal()"></div>
<div id="pb-modal">
    <div id="pb-modal-title">⚠ Official Response from Monsieur Poms</div>
    <div id="pb-modal-text"></div>
    <br>
    <button id="pb-modal-close" onclick="pbCloseModal()">OK (Accepted Under Protest)</button>
</div>

<script>
(function() {
    var BASE = 'https://cloudsky01.github.io/monsieur-poms.com/images/';

    // --- Day seed ---
    var now = new Date();
    var doy = Math.floor((now - new Date(now.getFullYear(), 0, 0)) / 86400000);

    function sr(s) { var x = Math.sin(s + 1) * 10000; return x - Math.floor(x); }
    function pick(arr, s) { return arr[Math.floor(sr(s) * arr.length)]; }
    function fmt(n) { return '$' + n.toFixed(2); }

    // --- Auction data ---
    var A = [
        {
            title: "One (1) Sanctioned Lap Session — Duration: 10 Minutes (Non-Negotiable)",
            sub: "Premium physical experience. Certificate of attendance not guaranteed.",
            cat: "Premium Services > Physical Experiences > Lap Access",
            cond: "New", condNote: "Never previously offered at a public price point.",
            img: "poms_loaf.jpg", start: 24.99, buy: 89.99, num: "230958475821",
            specs: [
                ["Duration","Up to 10 minutes (or until something better happens)"],
                ["Lap Requirements","Standard human lap, warmth level 7/10 minimum"],
                ["Early Exit Policy","Poms may leave without warning at any moment. No refund."],
                ["Treat Deposit","Required. Chicken preferred. Green beans not accepted."],
                ["Transferability","Non-transferable, non-tradeable, non-negotiable"]
            ],
            desc: "Extremely rare opportunity. Monsieur Poms will sit on your lap for up to ten (10) minutes, provided: (1) the lap is warm, (2) no sudden movements occur, (3) the word 'vet' is not spoken, and (4) a treat is provided as a deposit upon arrival.<br><br>Duration is ten minutes, or until something more interesting presents itself, whichever comes first. Poms reserves the right to exit at any moment — including immediately upon landing — should circumstances not meet his exact standards. These terms are non-negotiable.<br><br><em>Please note: bidding on this item does not guarantee a pleasant experience. It merely guarantees <b>an</b> experience.</em>",
            ship: "Buyer must travel to the designated sunbeam location. Coordinates provided after auction close. Poms will not ship. He does not recognize the postal system as relevant to his lifestyle.",
            ret: "No returns. I am not a product. I am Monsieur Poms.",
            qa: [
                ["Can the session be extended for an additional fee?","No. Ten minutes is already an enormous concession on my part."],
                ["Is a treat deposit really required?","Yes. Do not arrive without treats. Ideally chicken. I will know if you are lying."],
                ["What if you leave before 10 minutes are up?","That is not a defect. That is a feature. You received exactly what was advertised: a possible lap session."]
            ]
        },
        {
            title: "RESERVED: Prime Kitchen Window Sunbeam Slot — Morning Hours (Licensed, Not Sold)",
            sub: "You are purchasing a license to observe, not to occupy. I will still be sitting here.",
            cat: "Real Estate > Temporary Licenses > Sunbeam Access",
            cond: "Used", condNote: "Poms has occupied this sunbeam since 2010. Warmth pre-verified.",
            img: "poms_stare.jpg", start: 34.99, buy: 119.99, num: "172836495071",
            specs: [
                ["License Type","Observational only. No physical access to sunbeam."],
                ["Hours","9:00 AM — 11:30 AM (sunbeam moves after that)"],
                ["Occupant","Monsieur Poms (present at all times)"],
                ["Sublicensing","Strictly prohibited"],
                ["Renewal","Must be rebid each day"]
            ],
            desc: "This listing grants the winning bidder the exclusive right to <em>observe</em> Monsieur Poms occupying the kitchen window sunbeam between approximately 9:00 AM and 11:30 AM.<br><br>Please note: you are NOT purchasing the sunbeam. You are NOT purchasing the window sill. You are NOT receiving physical access to the area. Monsieur Poms will be there, taking up the full space, and he will not move. This is a premium observational license.<br><br>The sunbeam moves on its own schedule. Poms moves with it. This is not included in the license.",
            ship: "You must come here. Poms will not bring the sunbeam to you. That is not how sunbeams work.",
            ret: "The sunbeam is non-returnable. It is the sun.",
            qa: [
                ["Can I sit near the sunbeam?","No. The floor in front of the window is also mine."],
                ["What if it's cloudy?","I still sit here, out of habit. You still get to observe me. The contract holds."],
                ["Can I take photos?","I allow exactly three (3) photos. After that I will look away deliberately."]
            ]
        },
        {
            title: "Certificate of Authentic Judgment — Gold Paw Seal, Dated Today",
            sub: "Official documentation that Monsieur Poms has judged you. Formal and legally significant (to him).",
            cat: "Official Documents > Certificates > Judgment Records",
            cond: "New", condNote: "Freshly issued. Ink dry within 2-3 business naps.",
            img: "poms_judging.jpg", start: 14.99, buy: 44.99, num: "398472016583",
            specs: [
                ["Seal Type","Gold Paw (embossed, unofficial, but very real to me)"],
                ["Judgment Type","General assessment. Findings: classified."],
                ["Validity","Indefinite, or until I issue a revised judgment"],
                ["Frame","Not included. That is your problem."],
                ["Authenticity","Signed by Monsieur Poms. He cannot hold a pen but the sentiment is there."]
            ],
            desc: "Receive official dated documentation that Monsieur Poms has judged you. This certificate includes the Gold Paw Seal of the House of Poms, the judgment date, and a formal findings section left intentionally vague for maximum unease.<br><br>The judgment itself is non-negotiable. The outcome is not revealed until the certificate is delivered, at which point it is also not fully revealed. You simply receive the certificate and carry the uncertainty with you.<br><br>This is considered by many to be the most valuable certificate Monsieur Poms issues. 'Many' in this case means Monsieur Poms.",
            ship: "Certificate will be issued at the window sill at Poms' earliest convenience. Physical mailing not available. He has no stamps.",
            ret: "Once judged, always judged. No refunds.",
            qa: [
                ["Can I request a positive judgment?","You may request it. The request will be considered and then set aside."],
                ["Is the judgment legally binding?","In the household of Monsieur Poms, all judgments are binding."],
                ["What if I disagree with the judgment?","File a complaint with the Complaint Department. It will be reviewed and dismissed. These are the procedures."]
            ]
        },
        {
            title: "LIVE EVENT TICKET: Watch Monsieur Poms Eat Breakfast — One-Time Viewing",
            sub: "Non-reproducible. Begins when Poms decides it begins. Runtime: variable.",
            cat: "Event Tickets > Dining Experiences > Live Food Events",
            cond: "New", condNote: "Event occurs daily whether or not this listing sells.",
            img: "poms_curious.jpg", start: 19.99, buy: 59.99, num: "546172839401",
            specs: [
                ["Start Time","When Poms decides. Usually when he starts yelling."],
                ["Duration","Until bowl is empty, then judgment time"],
                ["Seating","Standing room only. Do not sit closer than 1.5 feet."],
                ["Talking","Absolutely not during the meal"],
                ["Re-entry","No. One viewing per ticket."]
            ],
            desc: "Witness history. Monsieur Poms will eat breakfast, and you will be there to see it.<br><br>The event begins when Poms has finished announcing that the bowl is empty and a human has refilled it. You will be given a 30-second warning (Poms running toward the kitchen at full speed). Please keep up.<br><br>Ticket holders are expected to observe respectfully. No commentary on portion sizes. No offering of green beans. No saying 'good boy' in a high-pitched voice during the meal. All of these constitute grounds for ejection.",
            ship: "You must be present in person. Poms is considering a streaming service but has not yet decided.",
            ret: "Breakfast, once eaten, cannot be uneaten. No returns on consumed meals.",
            qa: [
                ["How much does he eat?","Enough. Never enough. The bowl is always both too full and too empty depending on the moment."],
                ["Can I bring a camera?","You may attempt to photograph. He will look away at the exact wrong moment. This is intentional."],
                ["What if he's not hungry?","He is always hungry. He has been hungry since birth. The question is not relevant."]
            ]
        },
        {
            title: "One (1) Royal Complaint Filed On Your Behalf — Official Case Number Included",
            sub: "Let Monsieur Poms lodge your grievance. He is very experienced in this area.",
            cat: "Services > Legal & Administrative > Complaint Filing",
            cond: "New", condNote: "Every complaint handled personally. Do not expect resolution.",
            img: "poms_profile.jpg", start: 9.99, buy: 29.99, num: "718293046152",
            specs: [
                ["Complaint Type","Any grievance accepted. Green bean complaints expedited."],
                ["Processing Time","Immediately, loudly, at 3 AM if necessary"],
                ["Resolution Guarantee","None. Poms files complaints. He does not resolve them."],
                ["Case Number","Assigned upon submission. Format: POMS-YYYY-XXXXX"],
                ["Follow-up","Poms will continue complaining until satisfied or asleep"]
            ],
            desc: "Do you have a complaint? Something that simply isn't right? Monsieur Poms will file it.<br><br>Since 2010 he has filed over 12,000 formal complaints — primarily regarding bowl fill levels, treat delays, the presence of green beans, and suboptimal lap conditions. Your complaint will be added to his active caseload and prosecuted with the same tenacity he applies to all things.<br><br>He will meow about your issue loudly and persistently until (a) something changes, (b) he gets a treat, or (c) he falls asleep. All three outcomes are possible.",
            ship: "Complaints are delivered vocally, in person, to whoever is present. Remote complaint filing available for an additional $5.",
            ret: "Complaints filed are complaints filed. There is no un-complaining.",
            qa: [
                ["Can I file a complaint about another cat?","Yes. Inter-cat complaints are handled with particular enthusiasm."],
                ["What language will the complaint be filed in?","Meow. A very specific meow. The energy will be understood even if not the words."],
                ["Can I file multiple complaints?","Each complaint requires a separate bid. Poms has standards."]
            ]
        },
        {
            title: "FRONT ROW TICKET: The Morning Press Conference — Standing Room Only",
            sub: "The daily food bowl briefing. Doors open when Poms wakes up.",
            cat: "Event Tickets > Press Events > Daily Briefings",
            cond: "New", condNote: "Press conference occurs daily regardless of ticket sales.",
            img: "poms_avatar.jpg", start: 17.99, buy: 49.99, num: "623081947562",
            specs: [
                ["Location","The food bowl. Or wherever Poms currently is."],
                ["Start Time","6:00 AM – 9:00 AM (when Poms declares it time)"],
                ["Format","Sustained meowing with Q&A (no actual Q&A)"],
                ["Media Credentials","Not accepted. Poms is his own media."],
                ["Dress Code","Smart casual. No pajamas. Poms finds them disrespectful."]
            ],
            desc: "Every morning, Monsieur Poms convenes the press corps (the household) to deliver his official statement on the food bowl situation, the treat situation, the sunbeam situation, and the general state of affairs.<br><br>Today's front row ticket grants you access to witness this historic daily event from the closest available position — approximately 3 feet from Monsieur Poms, receiving his complete statement at full volume directly to your face.<br><br>Duration: approximately 30 minutes. Sometimes 45. Sometimes the whole morning. Duration is at Poms' discretion.",
            ship: "You must attend in person. There is no remote access. Poms requires a live audience.",
            ret: "The information delivered at the press conference cannot be un-heard.",
            qa: [
                ["Are questions accepted?","There are no questions. There is only the statement. You are there to receive it."],
                ["Can I bring notes?","You may bring notes. He will sit on them."],
                ["What if he has nothing to say?","He always has something to say. This has never been a problem."]
            ]
        },
        {
            title: "THE SLOW BLINK — Exclusively Issued to Winning Bidder, Valid 24 Hours",
            sub: "The highest honor Monsieur Poms can bestow. Reserve immediately.",
            cat: "Collectibles > Emotional Milestones > Rare Gestures",
            cond: "Rare", condNote: "Slow blinks are the cat equivalent of 'I trust you.' This is being sold for money. Poms is aware.",
            img: "poms_looking_up.jpg", start: 74.99, buy: 299.99, num: "891047362510",
            specs: [
                ["Duration","One (1) slow blink. Both eyes. Simultaneously."],
                ["Exclusivity","Only one winner per day. Non-transferable."],
                ["Emotional Value","Incalculable. That is why it is being sold for money instead."],
                ["Certificate","Included. 'The Slow Blink was given. You were there.'"],
                ["Conditions","Poms must be in the right mood. Mood: not guaranteed."]
            ],
            desc: "This is the most personal item currently listed on PawBay.<br><br>The Slow Blink is recognized among cat communication scholars as the highest form of feline affection — the cat equivalent of saying 'I trust you, I like you, you are okay.' Monsieur Poms bestows two to three of these per day, to people he chooses, at times he chooses.<br><br>This listing makes one available to the winning bidder. Poms will look at you and blink slowly, on purpose, for you. That is the item. That is, honestly, more than most people get.<br><br><em>Poms was informed this was being sold. He stared at the screen for a long time. Then he walked away. We are interpreting this as consent.</em>",
            ship: "You must be present. The slow blink cannot be mailed. It will not work through a screen.",
            ret: "The emotional experience of receiving a slow blink cannot be returned. Once felt, it stays with you.",
            qa: [
                ["What if he doesn't blink?","You will receive a certificate stating that Poms considered it, which is arguably the same thing."],
                ["Can I video it?","You can try. He tends to blink when you're not looking. This is intentional."],
                ["Is $299.99 the correct Buy It Now price?","$299.99 is simply the floor. The slow blink is beyond currency."]
            ]
        },
        {
            title: "RARE LISTING: One (1) Voluntary Cuddle Session — Mood-Dependent, No Guarantees",
            sub: "He has to want to. We cannot make him. That is the product.",
            cat: "Premium Services > High Risk Experiences > Voluntary Contact",
            cond: "Rare", condNote: "He doesn't just do this for anyone. Rarity status: genuine.",
            img: "poms_sleeping.jpg", start: 49.99, buy: 199.99, num: "734829105647",
            specs: [
                ["Voluntariness","100% voluntary. On his end. You must be completely stationary."],
                ["Duration","Unknown. Until he decides to leave."],
                ["Body Part Access","Head only. Do not touch the belly. This is serious."],
                ["Initiation","Poms initiates. You do not initiate. Ever."],
                ["Cancellation Risk","High. Any sudden sound resets the session."]
            ],
            desc: "The rarest listing currently available on PawBay.<br><br>This item represents Monsieur Poms voluntarily sitting close to you, possibly pressing his head against you, and staying there for an indeterminate period. He will do this because he <em>wants</em> to. You cannot ask him. You can only create favorable conditions and hope.<br><br>Favorable conditions: warmth, stillness, presence of a blanket, absence of sudden sounds, complete suppression of the urge to say 'aww' at full volume when it happens. The winning bidder will be briefed. Beyond that, the universe decides.",
            ship: "Poms will not travel to you. You create the conditions; he provides the outcome (maybe).",
            ret: "The hope of a cuddle session cannot be refunded even if no cuddle occurs. The possibility was genuine.",
            qa: [
                ["What is the probability of success?","Unknown. He could also just stare at you for 20 minutes and walk away. Both are valid outcomes."],
                ["Should I try to pet him?","Wait. Let him lead. Any premature movement resets everything. You have been warned."],
                ["Can I tell people this happened?","You may tell people. He will deny everything."]
            ]
        },
        {
            title: "Professional Nap Location Advisory Report — Personalized Consulting Service",
            sub: "Where should you nap? Monsieur Poms has strong opinions about this.",
            cat: "Services > Professional Consulting > Sleep Architecture",
            cond: "New", condNote: "16+ hours of daily field experience. He is the foremost expert.",
            img: "poms_loaf.jpg", start: 12.99, buy: 34.99, num: "281647039812",
            specs: [
                ["Deliverable","One (1) personalized nap location report"],
                ["Nap Types Covered","Sun nap, couch nap, floor nap, box nap, loaf nap"],
                ["Rating Scale","1-10 based on warmth, softness, sunbeam access"],
                ["Format","Oral presentation (meowing) + demonstration if warranted"],
                ["Revision Policy","No revisions. The first location is the correct location."]
            ],
            desc: "Monsieur Poms has been conducting nap location research since 2010. He has tested every surface: the couch (7/10), the bed (varies), the sunbeam spot (10/10, reserved for personal use), the cardboard box (surprisingly good, 8/10), and the floor directly in the way of foot traffic (strategic, 9/10).<br><br>Your advisory report will draw on this extensive database. Poms will review your sleeping situation and issue a formal recommendation. He cannot be held responsible for the quality of your implementation. The location is correct. What you do with it is your business.",
            ship: "Consultation conducted remotely via vibes. No travel required on your part.",
            ret: "If you disagree with the nap location recommendation, you are wrong. No refunds.",
            qa: [
                ["Can he advise on outdoor nap spots?","He has no outdoor nap experience. He is an indoor cat. The outside is not his jurisdiction."],
                ["What if my best spot is a couch he hasn't tested?","He will trust his instincts. His instincts are very good."],
                ["How long is the report?","The length of a single authoritative meow."]
            ]
        },
        {
            title: "AUTHENTIC Poms Fur Sample — Certificate of Provenance, Dated Today",
            sub: "One of the most collectible items in the Poms catalog. Naturally sourced.",
            cat: "Collectibles > Physical Artifacts > Genuine Materials",
            cond: "Used", condNote: "All fur shed voluntarily (via grooming, couch sitting, or general existence).",
            img: "poms_yawn.jpg", start: 8.99, buy: 24.99, num: "490123765842",
            specs: [
                ["Color","Orange. Unmistakably orange."],
                ["Quantity","Approximately several strands"],
                ["Source","Couch, mainly. Also sweater. Also everywhere."],
                ["Certificate","Signed by the person who found the fur"],
                ["Storage","Small envelope. Handle with care."]
            ],
            desc: "An item of genuine provenance. This fur sample comes from Monsieur Poms — specifically from whatever surface he sat on most recently — and is accompanied by a certificate stating that yes, this is in fact his fur, because the orange color and sheer volume leave no other plausible explanation.<br><br>Collect it. Frame it. Keep it in a small envelope. This is the experience of being a Poms fan: soft, orange, and inexplicably present on every garment you own within 48 hours of arrival.",
            ship: "Shipped in a small envelope. Do not let it blow away.",
            ret: "The fur has been shed. The process is irreversible. No returns.",
            qa: [
                ["Is this sanitary?","It is from a very clean cat. He grooms extensively. Multiple times per day."],
                ["Can you send more?","More fur will be shed tomorrow. Please rebid."],
                ["Does he know this is being sold?","We told him. He groomed himself and walked away. We're counting that as consent."]
            ]
        },
        {
            title: "Midnight Serenade Package — One (1) 3 AM Vocal Performance, Front Row",
            sub: "Poms performs nightly. Tonight, you have the best seat in the house.",
            cat: "Entertainment > Live Music > Nocturnal Performances",
            cond: "New", condNote: "Performance occurs whether or not this listing sells.",
            img: "poms_stare.jpg", start: 0.99, buy: 4.99, num: "567890123456",
            specs: [
                ["Start Time","Approximately 3:00 AM. He is consistent."],
                ["Setlist","Complaints about the bowl, occasional freestyle meow"],
                ["Duration","Until someone gets up. Or 4 AM. Whichever first."],
                ["Volume","Loud. Remarkably loud for a cat."],
                ["Ticket Type","Standing room (standing in the hallway at 3 AM)"]
            ],
            desc: "Every night, Monsieur Poms delivers his Midnight Serenade: a full vocal repertoire of meows, trills, and sustained yowls at full volume directly into the hallway, directed at no one in particular and everyone specifically.<br><br>The content is always the same in theme — something is wrong with the bowl, or the house in general — but the execution varies. Some nights operatic. Some staccato. Some a single note held for an alarming duration.<br><br>Tonight's front row ticket means you have consented to be present. You were going to be anyway. Now you have documentation.",
            ship: "You will receive this whether you want it or not.",
            ret: "The performance occurred. No refunds.",
            qa: [
                ["Can I ask him to stop?","Yes. He will stop for 4-7 seconds and then resume."],
                ["Is the bowl actually empty?","Unclear. He begins the serenade regardless of current bowl status."],
                ["Can I turn the lights off?","Yes. He will perform in the dark."]
            ]
        },
        {
            title: "ZOOMIES VIEWING EXPERIENCE — Live Event, Unpredictable Runtime",
            sub: "He starts running. No one knows why. Front row seats available.",
            cat: "Entertainment > Live Events > Unexplained Athletics",
            cond: "New", condNote: "Event may begin with no warning. Spectators must be agile.",
            img: "poms_curious.jpg", start: 7.99, buy: 19.99, num: "678901234567",
            specs: [
                ["Duration","30 seconds to 8 minutes. Completely unpredictable."],
                ["Path","All rooms. Possibly all rooms twice."],
                ["Maximum Speed","Extremely fast for a cat of his build. Do not underestimate."],
                ["Reason","Unknown. Has always been unknown. Will remain unknown."],
                ["Eye Contact","He will not make eye contact. He is busy."]
            ],
            desc: "Something happens. Something always happens. And then Monsieur Poms runs.<br><br>The ZOOMIES VIEWING EXPERIENCE is front row access to one of nature's most baffling phenomena: a large orange cat running at full speed from one end of the house to the other, for reasons never established, at times never predicted, for a duration never consistent.<br><br>You cannot predict when it will happen. Neither can anyone else. That is the experience. That is what you're paying for.",
            ship: "You must be on-site. Zoomies cannot be streamed without losing something essential.",
            ret: "The zoomies happened. The kinetic energy was real. No refunds.",
            qa: [
                ["Why does he do this?","We don't know. He doesn't know. The universe doesn't know. It simply happens."],
                ["Is it scary?","Slightly. He comes around corners very fast."],
                ["Can I try to catch him?","Please do not try to catch him. He is in a state. Let him run."]
            ]
        },
        {
            title: "Royal Pardon Certificate — 24-Hour Immunity from Today's Complaints",
            sub: "Poms will not complain about you specifically, for exactly one day.",
            cat: "Official Documents > Legal Pardons > Temporary Immunity",
            cond: "New", condNote: "Does not stop general complaints. Only personal complaints. Read carefully.",
            img: "poms_judging.jpg", start: 21.99, buy: 64.99, num: "789012345678",
            specs: [
                ["Validity","24 hours. Midnight to midnight."],
                ["Scope","Personal complaints only. General grievances continue."],
                ["Exclusions","Belly touching, saying 'fat' or 'chonky'"],
                ["Transferability","Non-transferable. You specifically are pardoned."],
                ["Renewal","Must be repurchased. No bulk discounts."]
            ],
            desc: "Every day, Monsieur Poms files a roster of complaints. Most are general. But some are personal.<br><br>This Royal Pardon grants the winning bidder temporary immunity from the personal complaint category. For 24 hours, Poms will direct his grievances elsewhere. He will not meow specifically at you. He will not produce that particular stare. He will look generally disappointed at the room rather than specifically at you.<br><br>This is, by most accounts, a significant quality of life improvement.",
            ship: "Pardon issued in the form of Poms sitting somewhere other than directly in front of you.",
            ret: "The pardon cannot be un-issued. However, it expires at midnight. No refund for unused time.",
            qa: [
                ["Does this guarantee positive treatment?","Absolutely not. You are simply exempt from active complaints. Neutral indifference is the maximum."],
                ["Can I get pardoned for touching the belly?","No. This is specifically excluded. That was a separate incident."],
                ["What happens after 24 hours?","Complaints resume. He has been keeping a list."]
            ]
        },
        {
            title: "Personal Chicken Quality Assessment — Certified Non-Green-Bean Rating",
            sub: "Poms evaluates your chicken. His opinion is the only one that matters.",
            cat: "Services > Food & Beverage Consulting > Quality Assessment",
            cond: "New", condNote: "Poms has been assessing chicken quality since 2010.",
            img: "poms_profile.jpg", start: 16.99, buy: 44.99, num: "890123456789",
            specs: [
                ["Assessment Criteria","Smell, texture, portion, overall adequacy"],
                ["Green Bean Check","Included at no extra charge. Finding: NOT ACCEPTABLE."],
                ["Rating Scale","Acceptable / Not Acceptable / Chicken (Chicken = perfect)"],
                ["Sample Required","Minimum one piece. Recommended: more."],
                ["Deliverable","Verbal assessment (meowing) + facial expression report"]
            ],
            desc: "Monsieur Poms is the foremost chicken quality assessor in this household and possibly beyond. Since 2010, he has evaluated thousands of chicken portions and developed a proprietary methodology: (1) initial smell evaluation, (2) first bite quality, (3) portion adequacy review, (4) follow-up thoughts on whether more is warranted (always yes).<br><br>All assessments include an automatic green bean scan. Any detected green beans trigger an immediate negative ruling and a formal complaint. Please ensure your chicken is green bean-free before submission.",
            ship: "Chicken must be presented in person. It must arrive warm.",
            ret: "If the chicken was wrong, please bring better chicken. That is the only acceptable resolution.",
            qa: [
                ["What if I bring the wrong kind of chicken?","He will let you know. Loudly. At length."],
                ["Is the green bean ban absolute?","The ban has been absolute since 2010. It has never wavered."],
                ["Can I get a second opinion?","There is no second opinion. There is only Poms' opinion. The assessment is final."]
            ]
        },
        {
            title: "Formal Certificate of Adequacy — 'You Are Acceptable' — Bronze Level",
            sub: "The lowest tier of Poms approval. Still more than most people receive.",
            cat: "Collectibles > Certificates of Achievement > Approval Documentation",
            cond: "New", condNote: "Bronze is entry level. Gold and Platinum exist but have never been issued.",
            img: "poms_avatar.jpg", start: 6.99, buy: 17.99, num: "901234567890",
            specs: [
                ["Tier","Bronze (lowest of three. The other two remain theoretical.)"],
                ["Statement","'You are acceptable. This is not nothing.'"],
                ["Permanence","Valid until Poms revises his opinion"],
                ["Higher Tiers","Silver (rare), Gold (theoretical), Platinum (not real yet)"],
                ["Frame","Not included. Recommended."]
            ],
            desc: "This certificate formally states that Monsieur Poms finds you acceptable. Not remarkable. Not impressive. Not even particularly notable. But acceptable.<br><br>To be clear: this is more than most people get. The Bronze Certificate represents Poms acknowledging your presence without complaint. He is not actively avoiding you. That is a form of recognition.<br><br>The certificate is suitable for framing. Poms recommends a modest frame. Nothing too ornate. You haven't earned that yet.",
            ship: "Issued in the form of Poms not actively avoiding you for one (1) day.",
            ret: "You cannot return adequacy once granted. It exists now.",
            qa: [
                ["Can I upgrade to Silver?","Silver is very rare. You would need to do something exceptional. Examples are not provided."],
                ["What disqualifies me for Bronze?","The presence of green beans on your person. Or saying 'chonky' within earshot."],
                ["Is this frameable?","Highly recommended. The concept is frameable; the physical document you must source yourself."]
            ]
        },
        {
            title: "One (1) Keyboard Occupation Service — 30+ Minutes Guaranteed",
            sub: "Poms will sit on your keyboard. Productivity: yours. Timeline: his.",
            cat: "Services > Productivity Enhancement > Keyboard Management",
            cond: "New", condNote: "The service will be performed. Your work situation is your own concern.",
            img: "poms_box.jpg", start: 11.99, buy: 29.99, num: "012345678901",
            specs: [
                ["Duration","30 minutes minimum. Often considerably more."],
                ["Keyboard Types","Laptop, external mechanical, extended format"],
                ["Work Impact","Significant. Multiple autocorrect events likely."],
                ["Removal Attempts","Discouraged. He will return immediately."],
                ["Additional Services","Monitor occupation may occur at no extra cost"]
            ],
            desc: "Your work can wait. Monsieur Poms has determined it is time to sit on the keyboard. This service, which Poms has been providing since 2010, ensures your keyboard is warm, fully occupied, and completely inaccessible for no less than 30 minutes.<br><br>During this time, Poms may walk across several keys, accidentally open additional browser windows, type several paragraphs of random characters, and look at you with an expression suggesting he is helping. He is helping. You may not feel that way in the moment.",
            ship: "Poms will deploy himself at the optimal moment. You will not see it coming.",
            ret: "The keyboard will be returned when Poms decides he is done. Not before.",
            qa: [
                ["What if I have an important meeting?","Poms does not recognize meetings as reasons to leave the keyboard."],
                ["Can I work around him?","You can try. He will slide closer."],
                ["Does he do standing desks?","He has assessed all surfaces. He adapts."]
            ]
        },
        {
            title: "LIVE DEMONSTRATION: Watch Monsieur Poms Fit Into A Box",
            sub: "The box is too small. He will fit. He always fits. No one knows how.",
            cat: "Entertainment > Physical Demonstrations > Advanced Spatial Relations",
            cond: "New", condNote: "The fitting cannot be explained. It can only be witnessed.",
            img: "poms_box.jpg", start: 13.99, buy: 39.99, num: "123456789012",
            specs: [
                ["Box Type","Medium — too small. This is intentional."],
                ["Fitting Method","Unknown. This is the demonstration."],
                ["Time to Complete","Variable. He takes his time. The suspense is part of it."],
                ["Post-Fitting Duration","He stays in the box until he decides otherwise."],
                ["Explanation","None will be provided. It simply happens."]
            ],
            desc: "A box arrives. The box is too small. This is obvious to everyone present. The dimensions are wrong. The math does not work. And yet.<br><br>Monsieur Poms approaches the box. He sniffs it. He walks around it. He sits next to it, thinking. And then he gets in. All of him. Somehow. The box accepts him in a way that defies spatial logic.<br><br>This is the demonstration. You will watch. You will have questions. The questions will not be answered.",
            ship: "You must be present. The box demonstration cannot be adequately described after the fact.",
            ret: "Once you have seen Poms in the box, you cannot unsee it. No refunds.",
            qa: [
                ["How does he do it?","We've watched hundreds of times. We still don't know."],
                ["Is the box safe?","He assessed it and declared it acceptable. It is safe."],
                ["Can I keep the box after?","No. The box is Poms'. It has always been Poms'."]
            ]
        },
        {
            title: "3AM Yelling Session — VIP Position Directly Outside Bedroom Door",
            sub: "Maximum volume. First to receive the statement.",
            cat: "Entertainment > Nocturnal Events > Acoustic Experiences",
            cond: "New", condNote: "The yelling occurs whether or not this listing sells.",
            img: "poms_yawn.jpg", start: 1.99, buy: 7.99, num: "234567890123",
            specs: [
                ["Start Time","Approximately 3 AM. Very consistent."],
                ["VIP Position","Directly outside the bedroom door"],
                ["Volume Level","Full. No indoor voice."],
                ["Content","Food bowl update, general grievances, mysterious statement"],
                ["Duration","Until someone opens the door. Or 4 AM."]
            ],
            desc: "Every night at approximately 3 AM, Monsieur Poms delivers his statement. The VIP position places you directly on the other side of the bedroom door — the primary delivery location. You will hear it first. You will hear it loudest. You will receive the full audio experience with no acoustic dampening.<br><br>The content varies nightly: sometimes about the bowl. Sometimes something he saw in the hallway. Sometimes one specific meow repeated at 4-second intervals for 20 minutes. This is the experience.",
            ship: "You are already there. You don't have a choice.",
            ret: "The sound waves have traveled. They cannot be unsent.",
            qa: [
                ["Can I close the door?","You can. He will continue. Slightly louder."],
                ["Is there any way to stop it?","Opening the door stops it immediately. He just wanted to know you were listening."],
                ["What does he want?","The bowl. Always the bowl. Sometimes also just confirmation of your existence."]
            ]
        },
        {
            title: "One (1) Official Head Bump — Issued Under the Poms Royal Seal",
            sub: "Also known as a 'bunt.' He means it. It is formal.",
            cat: "Premium Services > Physical Contact > Formal Greetings",
            cond: "New", condNote: "The head bump is simultaneously territorial and affectionate. You will be both marked and honored.",
            img: "poms_sleeping.jpg", start: 29.99, buy: 89.99, num: "345678901234",
            specs: [
                ["Action","Monsieur Poms presses his head against yours. Once."],
                ["Territorial Mark","You will be lightly scented. This is an honor."],
                ["Recipient Position","Lower yourself to his level. Do not make him jump."],
                ["Second Bump","May occur spontaneously. Cannot be requested."],
                ["Certificate","Certificate of Head Bump Issuance included."]
            ],
            desc: "When Monsieur Poms presses his head against you, he is saying several things simultaneously: I acknowledge you. I am marking you. You are, within the context of this household and this moment, acceptable to me.<br><br>The Official Head Bump is one of the most intimate items in the Poms catalog. The moment lasts seconds. The meaning, as documented by the included Certificate of Head Bump Issuance, lasts indefinitely.<br><br>Please lower yourself to his level to receive the bump. He will not jump. He will simply not do it if the geometry is wrong.",
            ship: "You must be present. The bump cannot be mailed.",
            ret: "You have been bumped. It cannot be reversed. It cannot be returned.",
            qa: [
                ["Will it definitely happen?","The conditions will be correct. Beyond that: Poms decides."],
                ["What if he headbutts me too hard?","Then he was very enthusiastic. Accept it with grace."],
                ["Can I headbutt back?","Please do not headbutt Monsieur Poms."]
            ]
        },
        {
            title: "Professional Treat Negotiation Services — Poms as Your Personal Advocate",
            sub: "He has been negotiating for treats since 2010. Persistence rate: 100%.",
            cat: "Services > Legal & Advocacy > Treat Procurement",
            cond: "New", condNote: "Same intensity applied to your treats as to his own.",
            img: "poms_loaf.jpg", start: 15.99, buy: 44.99, num: "456789012345",
            specs: [
                ["Negotiation Style","Persistent. Vocal. Unrelenting. But charming."],
                ["Success Guarantee","None. Persistence guaranteed."],
                ["Phases","The Look → The Meow → The Persistence → The Escalation"],
                ["Chicken Modifier","+50% effectiveness on chicken-related requests"],
                ["Duration","Until treats are produced or he falls asleep (can be hours)"]
            ],
            desc: "Monsieur Poms has developed a comprehensive multi-phase treat negotiation methodology: (Phase 1) Extended eye contact with the treat cabinet. (Phase 2) Meowing directed at the treat cabinet. (Phase 3) Meowing directed at the human nearest the treats. (Phase 4) Sitting on the human. (Phase 5) Escalated meowing.<br><br>The success rate is high. The treats are usually produced. Poms knows what he's doing. For one negotiation cycle, he will direct this full methodology toward your treat situation.",
            ship: "Services conducted in person. Remote advocacy is available but less effective.",
            ret: "If treats were not obtained: Poms tried. He really tried. That has to count for something. No refunds.",
            qa: [
                ["What if the treats are on a high shelf?","This is an acknowledged limitation. Poms advocates; he does not climb shelves. He has principles."],
                ["Can he negotiate for things other than treats?","His methods are treat-optimized. Results for non-treat items may be inconsistent."],
                ["Has he ever failed?","Once. In 2014. He has not spoken of it since."]
            ]
        },
        {
            title: "EXTREMELY RARE: I Will Move When Asked — This Day, One (1) Time Only",
            sub: "He will move. You ask. He moves. This has never happened before at market price.",
            cat: "Limited Edition > Physical Compliance > Voluntary Movement",
            cond: "Rare", condNote: "Rarity level: Historical. Poms does not move when asked as a general rule.",
            img: "poms_stare.jpg", start: 89.99, buy: 499.99, num: "567890123450",
            specs: [
                ["Action","Poms will move when asked. Once. Today only."],
                ["Activation","Say 'Poms, please move.' He will move."],
                ["Distance","At least 6 inches. Possibly more if feeling generous."],
                ["Attitude","Mild dissatisfaction expressed. The move will still occur."],
                ["Repeat Usage","One (1) use. He remembers."]
            ],
            desc: "This is the single most extraordinary item currently listed on PawBay. Monsieur Poms, who has moved voluntarily when asked approximately zero times since 2010, is offering — for one day, one time — to move when asked.<br><br>You say the words. He will hear them. He will look at you with an expression suggesting great personal sacrifice. And then he will move. At least six inches.<br><br>A certificate will document this moment. <em>The Buy It Now price reflects the genuine rarity of this event. $499.99 may seem high. Consider the alternative: he never moves. That is free. The value proposition is clear.</em>",
            ship: "You must be present to witness and utilize this item.",
            ret: "Once used, the moment is spent. The movement was real. You saw it.",
            qa: [
                ["Is this verified?","It will happen in real time. There are no simulations."],
                ["What if he ignores the request?","He won't. This listing carries an obligation. He understands this."],
                ["What's his expression when he moves?","Resigned but dignified. He maintains his dignity in all circumstances."]
            ]
        },
        {
            title: "Custom AIM Away Message — Personally Written and Endorsed by Poms",
            sub: "Your profile. His words. Maximum early-2000s energy.",
            cat: "Creative Services > Digital Content > AIM Profile Enhancement",
            cond: "New", condNote: "Messages written in Poms' authentic voice: lyrical, dramatic, about chicken or napping.",
            img: "poms_looking_up.jpg", start: 18.99, buy: 49.99, num: "678901234560",
            specs: [
                ["Format","One (1) AIM-style away message, 50–150 characters"],
                ["Style","Formal. Resigned. Unexpectedly philosophical."],
                ["Topics","Napping, food, judgment, window surveillance, philosophical malaise"],
                ["Customization","Submit context; Poms will incorporate or ignore it"],
                ["Delivery","Within 3–5 business naps"]
            ],
            desc: "It is the early 2000s. You are on AIM. Your away message needs to communicate something essential. You need Monsieur Poms' help.<br><br>Your message will be written in his voice — formal, resigned, unexpectedly philosophical: <em>'currently unavailable. much like the treats, which are also unavailable. this is not unrelated.'</em><br><br>The message will suit your AIM profile, your under-construction page, or your general life philosophy. Poms writes well. He has been composing his thoughts since 2010.",
            ship: "Message will be delivered via the medium of having been written.",
            ret: "If you don't like the message, please consider that Poms knows what you need better than you do.",
            qa: [
                ["Can I request a specific topic?","You may suggest. He will consider. He will write what he writes."],
                ["What if it's about chicken?","It will probably be about chicken. They usually are."],
                ["Can it be longer?","AIM had character limits. These are constraints Poms respects."]
            ]
        },
        {
            title: "THE DAILY STARE EXPERIENCE — Duration Indeterminate, Intensity: Maximum",
            sub: "He stares. You are there. That is the experience.",
            cat: "Premium Experiences > Psychological Services > Sustained Observation",
            cond: "New", condNote: "The stare is not hostile. It is not friendly. It simply is.",
            img: "poms_judging.jpg", start: 5.99, buy: 14.99, num: "789012345601",
            specs: [
                ["Duration","Until he looks away. Unpredictable."],
                ["Intensity","Maximum. He does not do partial stares."],
                ["Distance","Approximately 2–4 feet. Close enough to matter."],
                ["Emotional Content","Unknown. That is the experience. The not-knowing."],
                ["Blinking","Occasional. Does not break the stare."]
            ],
            desc: "Monsieur Poms sits. He looks at you. Directly at you. His eyes are steady. His expression is unreadable. He blinks slowly, once, and then continues looking.<br><br>You do not know what he is thinking. You will never know what he is thinking. This ambiguity is the experience. Is this warmth? Judgment? A question about the treat situation? You will not arrive at certainty.<br><br>The stare lasts until it doesn't. He will eventually look away. You will feel, briefly, like something has ended. Then he may look at you again.",
            ship: "You must be physically present to be stared at. Remote staring is not the same.",
            ret: "You have been looked at. The experience is complete.",
            qa: [
                ["Should I stare back?","You may. He will win. He always wins. But try if you want."],
                ["Is this evaluation?","Probably. Everything with Poms is evaluation."],
                ["What if it's unsettling?","It is a little unsettling. That is part of it."]
            ]
        },
        {
            title: "Window Surveillance Exclusive Viewer Access — Bird Situation Briefing Included",
            sub: "Stand-up briefing on current avian activity. Poms is the only source.",
            cat: "Entertainment > Live Surveillance > Bird Intelligence",
            cond: "New", condNote: "Intelligence accuracy: varies. Enthusiasm: constant.",
            img: "poms_curious.jpg", start: 9.99, buy: 27.99, num: "890123456701",
            specs: [
                ["Briefing Format","Chattering, tail movement, occasional meow"],
                ["Intelligence Gathered","Bird species (estimated), quantity, location, threat level"],
                ["Threat Assessment","Always high. The birds are always doing something."],
                ["Window Access","Viewing from behind Poms. He has the primary position."],
                ["Confidentiality","None. He announces everything."]
            ],
            desc: "Monsieur Poms has been monitoring the window situation since 2010. He is the household's leading expert on bird behavior and general outdoor activity within visual range of the kitchen window.<br><br>As an exclusive viewer, you will stand behind Poms and receive a live briefing on current conditions. The briefing is delivered through chattering — a specific sound cats make when they see birds that can only be described as extreme, contained excitement — and through tail movements that Poms assures are informative.<br><br>The bird situation is ongoing and serious. You will leave more informed.",
            ship: "On-site only. The birds are at this specific window.",
            ret: "Bird intelligence briefings are time-sensitive. Once the birds leave, the briefing is over. No refunds.",
            qa: [
                ["What if there are no birds?","There are always birds. Poms will wait. The birds always come back."],
                ["Can I point at a bird?","He already knows. He's been watching it for 20 minutes."],
                ["Does he ever catch them?","He has not had the opportunity. He considers this a technicality, not a limitation."]
            ]
        },
        {
            title: "One (1) Guaranteed Loaf Formation Observation — Weather Permitting",
            sub: "He tucks his paws. He becomes bread. You are there. You see it.",
            cat: "Premium Experiences > Rare Formations > Loaf Category",
            cond: "New", condNote: "Loaf formation requires paw-tuck, full body settle, and ambient warmth.",
            img: "poms_loaf.jpg", start: 12.99, buy: 34.99, num: "901234567801",
            specs: [
                ["Loaf Type","Classic Full Loaf (all paws tucked, none visible)"],
                ["Duration","Until something disturbs him. Hopefully: long."],
                ["Location","The couch, primarily. Sometimes counter. He knows."],
                ["Paw Visibility","Zero. That is the point of the loaf."],
                ["Dignity Level","Maximum. The loaf is his most dignified form."]
            ],
            desc: "At some point today, Monsieur Poms will become a loaf. He will settle onto a flat surface, tuck every paw completely out of sight beneath his body, and transform into an approximately bread-shaped object with a face.<br><br>When Poms loafs, he is at peace. He is warm. He is also, technically, a loaf.<br><br>Your observation ticket grants you the right to witness this moment. You may look. You may photograph from a respectful distance. You may not disturb. The loaf is sacred.",
            ship: "On-site viewing only. The loaf cannot be shipped.",
            ret: "The loaf was real. You saw it. Experience complete.",
            qa: [
                ["Can I pet him in loaf form?","He will endure it for ~3 seconds before exiting loaf formation. Consider whether it's worth it."],
                ["Why is it called a loaf?","Because he looks exactly like bread. Observe and you will understand immediately."],
                ["Does weather affect it?","'Weather permitting' refers to indoor warmth. He loafs more when it is warm."]
            ]
        },
        {
            title: "Founding Charter Membership: The Official Poms Fan Club",
            sub: "He has not asked for a fan club. This is happening anyway.",
            cat: "Collectibles > Memberships > Fan Organizations",
            cond: "New", condNote: "Poms has been informed and had no comment.",
            img: "poms_profile.jpg", start: 10.99, buy: 27.99, num: "012345678910",
            specs: [
                ["Membership Type","Founding Charter Member"],
                ["Benefits","A certificate. The knowledge that you are in the fan club."],
                ["Newsletter","Published irregularly at Poms' discretion (this website)"],
                ["Annual Dues","Bid price, annually. Implied by the word 'membership.'"],
                ["Poms Involvement","He is aware. He is not involved."]
            ],
            desc: "The Official Poms Fan Club is now accepting founding charter members. Poms was not consulted. He was informed. He stared at the notification for approximately 8 seconds and then went to check his food bowl.<br><br>We are interpreting this as acceptance.<br><br>As a founding charter member, you receive: (1) a certificate stating your membership, (2) the knowledge that you are now officially in the fan club, and (3) access to any future fan club communications, which could theoretically never be issued.",
            ship: "Membership issued digitally in your heart and also on a certificate.",
            ret: "Once you have joined the fan club, you have joined the fan club. Membership may be revoked by Poms at any time.",
            qa: [
                ["Does Poms know my name?","He knows you're a fan. Specifics are not guaranteed."],
                ["Will there be merchandise?","Discussions are ongoing. By which we mean: undiscussed. But potentially yes."],
                ["Can I meet Poms?","Poms does not do meet and greets on demand. That is a separate listing."]
            ]
        },
        {
            title: "USED: Warmth-Infused Sunbeam Spot — Residual Warmth Fades After 5 Minutes",
            sub: "The sunbeam has moved. The warmth remains, briefly. Act now.",
            cat: "Collectibles > Physical Artifacts > Used Warmth",
            cond: "Used", condNote: "Poms has vacated. His warmth lingers. Time is critical.",
            img: "poms_stare.jpg", start: 3.99, buy: 9.99, num: "123456789023",
            specs: [
                ["Location","Wherever Poms was sitting most recently"],
                ["Temperature","Warm. Fading."],
                ["Time Window","5 minutes from listing. Act quickly."],
                ["Fur Content","Some fur included at no extra charge"],
                ["Sunbeam","The beam itself has moved. Residual warmth only."]
            ],
            desc: "Monsieur Poms has vacated his sunbeam spot. In his absence, the spot retains thermal energy: a warm patch, soft, slightly furry, carrying the ambient warmth of a cat who was very comfortable there moments ago.<br><br>This is your chance. The warmth window is approximately five minutes. Poms is elsewhere, monitoring the situation.<br><br>This is an extremely time-sensitive listing. By the time you are reading this, the clock has already started.",
            ship: "On-site only. The warmth cannot travel.",
            ret: "The warmth may have dissipated before you arrived. This is not a defect. This is entropy.",
            qa: [
                ["What if the spot is cold when I get there?","You have received the authentic used sunbeam spot experience. Warmth moves faster than expected."],
                ["Is there fur in it?","Almost certainly."],
                ["Can I keep this spot now?","No. Poms will return. He always returns to his spots."]
            ]
        },
        {
            title: "Certified Non-Green-Bean Treat Pre-Approval — Valid for One (1) Treat",
            sub: "Poms has reviewed your proposed treat. It is not a green bean. It is approved.",
            cat: "Food & Beverage > Certified Items > Treat Clearance",
            cond: "New", condNote: "Green beans permanently banned since 2010. This confirms your treat is not one.",
            img: "poms_avatar.jpg", start: 4.99, buy: 12.99, num: "234567890134",
            specs: [
                ["Covers","Any treat that is not a green bean"],
                ["Green Bean Status","Banned. Permanently. Since 2010. Non-negotiable."],
                ["Approval Process","Poms will smell it. He will decide. Usually yes, if not a green bean."],
                ["Validity","Single use. For one (1) treat presentation."],
                ["Chicken","Always pre-approved. Doesn't even need this certificate."]
            ],
            desc: "In 2010, Monsieur Poms issued a permanent, irrevocable ban on green beans. The circumstances of the original incident are not fully documented, but the stance has never wavered.<br><br>This certification confirms that your proposed treat contains no green beans. It is approved for presentation. He will likely eat it.<br><br>Certificate does not apply to broccoli, Brussels sprouts, or vegetables disguised in food. Poms has a very accurate nose.",
            ship: "Certificate issued upon treat review. You must present the treat in person.",
            ret: "If the treat contained a hidden green bean despite certification, the certification process was compromised at the source.",
            qa: [
                ["What about carrots?","Carrots are not green beans, which is in their favor. They are also not chicken, which is not."],
                ["Why does he hate green beans so much?","The incident of 2010 is not discussed. Moving forward."],
                ["Can I get a certification for a whole bag?","Per-treat only. He assesses each one individually."]
            ]
        },
        {
            title: "Emergency Treat Request Priority Processing — Skip the Line",
            sub: "Your urgent treat need, elevated to the top of the queue. Poms still decides.",
            cat: "Services > Emergency Response > Treat Procurement Priority",
            cond: "New", condNote: "Priority means considered first. 'First' still means Poms considers it. He may still say no.",
            img: "poms_curious.jpg", start: 8.99, buy: 24.99, num: "345678901245",
            specs: [
                ["Response Time","Within 2–3 meows of submission"],
                ["Queue Priority","Elevated above standard treat requests"],
                ["Outcome Guarantee","None. This is priority processing, not priority approval."],
                ["Escalation Path","Meow → Louder meow → Sitting on treat cabinet"],
                ["Best For","Time-sensitive treat situations. Also: all treat situations."]
            ],
            desc: "Standard treat requests take time. The process involves eye contact with the treat cabinet, meowing in a specific register, waiting, meowing again, sitting on the nearest person, waiting more. It works, but not quickly.<br><br>Emergency Treat Priority Processing moves your request to the front. Poms will begin advocating immediately. The outcome is still not guaranteed — Poms cannot unilaterally produce treats, he can only advocate — but the timeline is significantly compressed.",
            ship: "Services rendered in person. Remote advocacy is available but less effective.",
            ret: "Processing fee non-refundable regardless of outcome. Poms tried. Earnestly.",
            qa: [
                ["What counts as a 'treat emergency'?","Anything Poms classifies as urgent. He classifies most treat situations as urgent."],
                ["Can I use this for food, not just treats?","Food has a separate process. This is treats only."],
                ["What is his success rate?","He has never stopped trying. That is the metric he uses."]
            ]
        },
        {
            title: "VIP BEHIND THE BOWL Documentary Access — Meal Prep Surveillance, Live",
            sub: "You're in the kitchen. Poms is underfoot. You are officially crew.",
            cat: "Entertainment > Documentaries > Food Production > Live Access",
            cond: "New", condNote: "Poms is always there. He is always watching. Your ticket makes it official.",
            img: "poms_profile.jpg", start: 22.99, buy: 69.99, num: "456789012356",
            specs: [
                ["Format","Live, in-person documentary observation"],
                ["Subject","Monsieur Poms supervising his meal preparation"],
                ["Subject Cooperation","Poms will be present regardless. His presence is your access."],
                ["Runtime","Duration of meal prep + 5-10 minutes post-meal assessment"],
                ["Tripping Hazard","High. He will be underfoot. This is non-negotiable."]
            ],
            desc: "Every meal starts the same way. Poms hears something — a cabinet opening, a bag rustling, bowl-adjacent activity — and he arrives. Immediately underfoot. Vocalizing. Supervising.<br><br>This documentary access places you in the kitchen during this moment. You will observe Poms in his natural, purposeful state: weaving between feet, meowing with increasing urgency, maintaining constant surveillance until the bowl is filled.<br><br>The moment the bowl is placed down, he goes silent. The transition from agitated to consumed. This is the documentary.",
            ship: "You must be in the kitchen. This is non-negotiable. The kitchen is where it happens.",
            ret: "The documentary was filmed. The meal was consumed. No refunds.",
            qa: [
                ["Is he always underfoot?","Always. It has resulted in several near-falls. He considers these unrelated to his presence."],
                ["Can I hold him during prep?","He will resist. He cannot supervise from your arms."],
                ["Does he ever help?","He is helping. His definition of help differs from the human perspective. Both are valid."]
            ]
        }
    ];

    // "More from seller" shortcuts
    var MORE_ITEMS = [
        { label: "Daily Card", href: "card/", img: "poms_stare.jpg" },
        { label: "Forecast", href: "forecast/", img: "poms_loaf.jpg" },
        { label: "Horoscope", href: "horoscope/", img: "poms_looking_up.jpg" },
        { label: "Decree", href: "decree/", img: "poms_judging.jpg" },
        { label: "Complaints", href: "complaint/", img: "poms_stare.jpg" },
        { label: "Nap Report", href: "naplog/", img: "poms_sleeping.jpg" }
    ];

    var BID_REJECTIONS = [
        "Your bid has been received and immediately rejected. I simply wanted to see what numbers you would offer.",
        "After careful consideration lasting approximately 0.3 seconds, I have declined your bid. The reason is classified.",
        "Thank you for your interest. I have reviewed your offer and found it insulting. Please bid again with more dignity.",
        "Your bid was reviewed by a panel of one (me). The decision was unanimous: no.",
        "I have temporarily suspended bidding to take a nap. Timeline: unknown.",
        "Bid rejected. You moved the mouse too fast. This is not the energy I need from a potential buyer.",
        "I don't know you. You could be anyone. You could be a dog person. I cannot take that risk.",
        "The bid amount is noted. It is not enough. Everything I own is worth more. This is just a fact.",
        "Your bid has been forwarded to my legal team (also me). They will review it at their earliest convenience (never).",
        "I appreciate the enthusiasm. However, I was just about to take a nap. Bid denied."
    ];

    var BUYNOW_REJECTIONS = [
        "Buy It Now has been disabled. I reconsidered. You cannot buy me.",
        "The Buy It Now feature is available only to buyers I personally approve. I have not personally approved you.",
        "Buy It Now requires a 15-treat minimum deposit, paid in advance, non-refundable. Contact my office (the sunbeam spot) to arrange.",
        "Error: Buy It Now unavailable for items of this rarity. Please place a standard bid that I will also reject.",
        "Buy It Now has been removed from this listing because I decided I don't want to part with it after all."
    ];

    var BIDDERS = [
        'whisker_hoarder99','treats4life_xoxo','catmom2001','kibble_king_real',
        'orange_cat_fan88','meow_investor_pro','purrfect_collector','fluffmaster5000',
        'sunbeam_seeker77','mousepad_guy2001','pawprint_patricia','tabby_fan_official',
        'cardboard_box_fanXO','loaf_formation_stan','3am_survivor_99',
        'chicken_tender_luv','treat_bag_rustler','snuggles4ever2001',
        'catnip_connoisseur','zoomies_witness_x'
    ];

    // --- Pick today's auction ---
    var a = A[doy % A.length];

    // --- Generate bids ---
    var numBids = Math.floor(sr(doy * 7 + 3) * 6); // 0–5
    var bids = [];
    var price = a.start;
    for (var i = 0; i < numBids; i++) {
        price += 0.50 + Math.floor(sr(doy * 13 + i * 7) * 12) * 0.50;
        var bidderIdx = Math.floor(sr(doy * 17 + i * 11) * BIDDERS.length);
        var hour = 6 + Math.floor(sr(doy * 19 + i * 5) * 12);
        var min = Math.floor(sr(doy * 23 + i * 3) * 60);
        var pad = function(n) { return n < 10 ? '0' + n : '' + n; };
        bids.push({
            bidder: BIDDERS[bidderIdx],
            amount: price,
            time: pad(hour) + ':' + pad(min)
        });
    }

    // --- Populate page ---
    document.getElementById('pb-category').textContent = a.cat;
    document.getElementById('pb-item-num').textContent = a.num;
    document.getElementById('pb-title').textContent = a.title;
    document.getElementById('pb-subtitle').textContent = a.sub;
    document.getElementById('pb-photo').src = BASE + a.img;
    document.getElementById('pb-photo').alt = a.title;
    document.getElementById('pb-start-bid').textContent = fmt(a.start);

    var condBadge = document.getElementById('pb-cond-badge');
    condBadge.textContent = a.cond;
    if (a.cond === 'Used') { condBadge.className = 'pb-condition-badge used'; }
    else if (a.cond === 'Rare' || a.cond === 'Extremely Rare') { condBadge.className = 'pb-condition-badge rare'; }
    document.getElementById('pb-cond-note').textContent = a.condNote;

    var currentBid = numBids > 0 ? bids[bids.length - 1].amount : a.start;
    document.getElementById('pb-current-bid').textContent = fmt(currentBid);
    document.getElementById('pb-num-bids').textContent = numBids;
    document.getElementById('pb-bids-s').textContent = numBids === 1 ? '' : 's';
    document.getElementById('pb-buynow-price').textContent = fmt(a.buy);

    document.getElementById('pb-ship-short').textContent = a.ship;
    document.getElementById('pb-returns-short').textContent = a.ret;

    document.getElementById('pb-desc').innerHTML = a.desc;

    // Specs
    var specsHtml = '';
    for (var j = 0; j < a.specs.length; j++) {
        specsHtml += '<tr><td>' + a.specs[j][0] + '</td><td>' + a.specs[j][1] + '</td></tr>';
    }
    document.getElementById('pb-specs').innerHTML = specsHtml;

    // Shipping full
    document.getElementById('pb-ship-full').innerHTML =
        '<strong>Shipping:</strong> ' + a.ship + '<br><br>' +
        '<strong>Returns:</strong> ' + a.ret;

    // Bid history
    document.getElementById('pb-bid-count-hdr').textContent = numBids;
    if (numBids === 0) {
        document.getElementById('pb-bid-history-wrap').querySelector('table').style.display = 'none';
        document.getElementById('pb-no-bids').style.display = 'block';
    } else {
        var tbodyHtml = '';
        for (var k = bids.length - 1; k >= 0; k--) {
            tbodyHtml += '<tr>' +
                '<td style="color:#0064d2;">' + bids[k].bidder + '</td>' +
                '<td style="font-weight:bold;">' + fmt(bids[k].amount) + '</td>' +
                '<td style="color:#888;">Today, ' + bids[k].time + '</td>' +
                '</tr>';
        }
        document.getElementById('pb-bid-tbody').innerHTML = tbodyHtml;
    }

    // Q&A
    var qaHtml = '';
    for (var q = 0; q < a.qa.length; q++) {
        qaHtml += '<div class="pb-qa-item">' +
            '<div class="pb-qa-q">' + a.qa[q][0] + '</div>' +
            '<div class="pb-qa-a">' + a.qa[q][1] + '</div>' +
            '</div>';
    }
    document.getElementById('pb-qa').innerHTML = qaHtml;

    // More from seller
    var baseUrl = 'https://cloudsky01.github.io/monsieur-poms.com/';
    var moreHtml = '';
    for (var m = 0; m < MORE_ITEMS.length; m++) {
        moreHtml += '<a href="' + baseUrl + MORE_ITEMS[m].href + '" class="pb-more-item" style="text-decoration:none;">' +
            '<img src="' + BASE + MORE_ITEMS[m].img + '" alt="' + MORE_ITEMS[m].label + '">' +
            MORE_ITEMS[m].label +
            '</a>';
    }
    document.getElementById('pb-more').innerHTML = moreHtml;

    // --- Countdown ---
    function updateCountdown() {
        var n = new Date();
        var midnight = new Date(n); midnight.setHours(24, 0, 0, 0);
        var diff = midnight - n;
        var h = Math.floor(diff / 3600000);
        var mi = Math.floor((diff % 3600000) / 60000);
        var s = Math.floor((diff % 60000) / 1000);
        var p = function(x) { return x < 10 ? '0' + x : '' + x; };
        document.getElementById('pb-countdown').textContent = p(h) + ':' + p(mi) + ':' + p(s);
    }
    updateCountdown();
    setInterval(updateCountdown, 1000);

    // --- Modal helpers ---
    window.pbCloseModal = function() {
        document.getElementById('pb-modal').style.display = 'none';
        document.getElementById('pb-modal-overlay').style.display = 'none';
    };
    function showModal(text) {
        document.getElementById('pb-modal-text').innerHTML = text;
        document.getElementById('pb-modal').style.display = 'block';
        document.getElementById('pb-modal-overlay').style.display = 'block';
    }

    // --- Bid / Buy Now ---
    window.pbPlaceBid = function() {
        var msg = pick(BID_REJECTIONS, doy * 31 + Math.floor(Math.random() * 100));
        showModal('&ldquo;' + msg + '&rdquo;<br><br><span style="font-size:11px;color:#999;">— Monsieur Poms, Official Response</span>');
    };
    window.pbBuyNow = function() {
        var msg = pick(BUYNOW_REJECTIONS, doy * 37 + Math.floor(Math.random() * 100));
        showModal('&ldquo;' + msg + '&rdquo;<br><br><span style="font-size:11px;color:#999;">— Monsieur Poms, Official Response</span>');
    };
})();
</script>
