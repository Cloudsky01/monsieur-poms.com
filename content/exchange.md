---
title: "The Kibble Exchange"
---

<style>
.kex-header-strip {
    background: linear-gradient(to right, #001400, #003300, #001400);
    color: #00FF00;
    text-align: center;
    padding: 18px 10px;
    margin: -10px -10px 0 -10px;
    border-bottom: 4px solid #00CC00;
}

.kex-ticker-bar {
    background: #000;
    color: #00FF00;
    font-family: 'Courier New', monospace;
    font-size: 12px;
    font-weight: bold;
    padding: 5px 0;
    border-top: 2px solid #005500;
    border-bottom: 2px solid #005500;
    overflow: hidden;
    white-space: nowrap;
}

.kex-main-board {
    background: #001a00;
    border: 3px double #00AA00;
    padding: 14px;
    margin: 12px 0;
    box-shadow: 5px 5px 0 #000;
    font-family: 'Courier New', monospace;
}

.kex-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 11px;
    font-family: 'Courier New', monospace;
}
.kex-table th {
    background: #003300;
    color: #00FF00;
    padding: 5px 8px;
    text-align: left;
    font-size: 10px;
    letter-spacing: 2px;
    text-transform: uppercase;
    border: 1px solid #005500;
}
.kex-table td {
    padding: 6px 8px;
    border: 1px solid #003300;
    vertical-align: middle;
}
.kex-table tr.kex-row-odd td  { background: #001800; }
.kex-table tr.kex-row-even td { background: #001200; }

.kex-up   { color: #00FF66; font-weight: bold; }
.kex-down { color: #FF4444; font-weight: bold; }
.kex-flat { color: #FFFF00; font-weight: bold; }

.kex-ticker-sym {
    font-family: 'Impact', 'Arial Black', sans-serif;
    letter-spacing: 1px;
    font-size: 13px;
    color: #FFFF00;
}

.kex-bar-outer {
    background: #003300;
    border: 1px solid #005500;
    height: 10px;
    width: 80px;
    display: inline-block;
    vertical-align: middle;
    overflow: hidden;
}
.kex-bar-inner {
    height: 100%;
    animation: kexFill 0.8s ease-out forwards;
}
@keyframes kexFill { from { width: 0%; } }

.kex-index-box {
    background: linear-gradient(to bottom, #002200, #001800);
    border: 2px solid #00AA00;
    padding: 10px 14px;
    margin: 10px 0;
    display: flex;
    gap: 14px;
    flex-wrap: wrap;
    align-items: stretch;
}

.kex-index-card {
    flex: 1;
    min-width: 140px;
    background: #001200;
    border: 1px solid #005500;
    padding: 8px 10px;
    text-align: center;
    font-family: 'Courier New', monospace;
}

.kex-index-name {
    font-size: 9px;
    color: #00AA00;
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 4px;
    border-bottom: 1px dotted #005500;
    padding-bottom: 3px;
}

.kex-index-val {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 22px;
    letter-spacing: 1px;
    line-height: 1.2;
    margin: 5px 0 3px;
}

.kex-analyst-box {
    background: #FFFFF0;
    border: 3px double #005500;
    padding: 14px 16px;
    margin: 12px 0;
    font-size: 11px;
    line-height: 1.75;
    color: #1a2a00;
}

.kex-analyst-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 14px;
    color: #003300;
    letter-spacing: 2px;
    border-bottom: 2px solid #005500;
    padding-bottom: 5px;
    margin-bottom: 10px;
}

.kex-portfolio-box {
    background: linear-gradient(to right, #001a00, #003300);
    border: 3px solid #00CC00;
    padding: 12px 16px;
    margin: 12px 0;
    font-family: 'Courier New', monospace;
    font-size: 11px;
    color: #00FF00;
}

.kex-portfolio-title {
    font-family: 'Impact', 'Arial Black', sans-serif;
    font-size: 14px;
    letter-spacing: 2px;
    color: #FFFF00;
    border-bottom: 2px solid #00CC00;
    padding-bottom: 5px;
    margin-bottom: 10px;
    text-shadow: 0 0 6px #00FF00;
}

.kex-disclaimer {
    font-size: 9px;
    color: #888;
    text-align: center;
    line-height: 1.7;
    font-style: italic;
    border-top: 1px dotted #CCC;
    padding-top: 8px;
    margin-top: 10px;
}

.kex-alert {
    background: #1a0000;
    border: 3px solid #FF4444;
    color: #FF8888;
    font-family: 'Courier New', monospace;
    font-size: 11px;
    padding: 8px 12px;
    margin: 6px 0;
    display: none;
}

@keyframes kexReveal {
    from { opacity: 0; transform: translateY(-6px); }
    to   { opacity: 1; transform: translateY(0); }
}
.kex-reveal { animation: kexReveal 0.4s ease-out forwards; }

.kex-volume-spark {
    display: inline-block;
    vertical-align: middle;
    font-size: 9px;
    color: #005500;
    letter-spacing: 0;
    font-family: 'Courier New', monospace;
}
</style>

<div style="border: 1px solid #CCC; overflow: hidden; margin-bottom: 20px; background: #001200;">

<div class="kex-header-strip">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 28px; letter-spacing: 4px; text-shadow: 0 0 16px #00FF00, 2px 2px 0 #000;">
        📈 THE KIBBLE EXCHANGE 📉
    </div>
    <div style="font-size: 10px; color: #00AA00; margin-top: 5px; letter-spacing: 3px; text-transform: uppercase;">
        Official Cat-Financial Markets &nbsp;|&nbsp; Chief Analyst: Monsieur Poms &nbsp;|&nbsp; Est. 2010
    </div>
    <div style="margin-top: 8px; font-size: 13px; letter-spacing: 3px; color: #007700;">
        ▲ ▼ ▲ ▼ ▲ ▼ ▲ ▼ ▲
    </div>
</div>

<div style="background: #001800; border-bottom: 2px solid #005500; padding: 5px 12px; font-size: 10px; color: #00AA00; text-align: center; font-family: 'Courier New', monospace;">
    MARKET SESSION: OPEN &nbsp;|&nbsp; EXCHANGE: KIBBLE &nbsp;|&nbsp; CURRENCY: TREATS (TRT) &nbsp;|&nbsp; TODAY: <strong id="kex-date" style="color:#FFFF00;"></strong>
</div>

<div class="kex-ticker-bar">
    <marquee scrollamount="5" id="kex-ticker">⚡ LOADING MARKET DATA... please stand by ⚡</marquee>
</div>

<div style="padding: 12px;">

<p style="font-size: 11px; color: #00AA00; text-align: center; line-height: 1.75; font-style: italic; font-family: 'Courier New', monospace; margin-bottom: 6px;">
    The Kibble Exchange is the world's foremost cat-financial market, founded and regulated by Monsieur Poms.<br>
    All prices update daily at midnight. Investments made in chicken are non-refundable and extremely advisable.<br>
    Green Bean Holdings (GLBN) is listed for informational purposes only. Poms does not recommend it. Ever.
</p>

<!-- ══════════════════════════════════════════ -->
<!-- MARKET INDICES                             -->
<!-- ══════════════════════════════════════════ -->
<div class="kex-index-box kex-reveal" id="kex-indices"></div>

<!-- GLBN ALERT (shown when GLBN crashes hard) -->
<div class="kex-alert" id="kex-glbn-alert">
    ⚠️ GLBN ALERT: Global Green Bean Holdings has declined for the 5,478th consecutive session.
    Analysts remain baffled. Monsieur Poms is not baffled. He has been saying this since 2010.
</div>

<!-- ══════════════════════════════════════════ -->
<!-- MAIN BOARD                                 -->
<!-- ══════════════════════════════════════════ -->
<div class="kex-main-board kex-reveal">
    <div style="font-family: 'Impact', 'Arial Black', sans-serif; font-size: 14px; color: #00FF00; letter-spacing: 2px; border-bottom: 2px solid #005500; padding-bottom: 5px; margin-bottom: 10px; text-shadow: 0 0 6px #00FF00;">
        📊 TODAY'S MARKET BOARD — KIBBLE EXCHANGE (KBX)
    </div>
    <table class="kex-table" id="kex-board"></table>
</div>

<!-- ══════════════════════════════════════════ -->
<!-- ANALYST REPORT                             -->
<!-- ══════════════════════════════════════════ -->
<div class="kex-analyst-box kex-reveal">
    <div class="kex-analyst-title">📰 DAILY ANALYST REPORT — M. POMS, CHIEF MARKET ANALYST</div>
    <div style="font-size: 10px; color: #888; font-family: 'Verdana', sans-serif; margin-bottom: 8px; letter-spacing: 1px; text-transform: uppercase;">
        Kibble Exchange Research Division &nbsp;|&nbsp; Certified by the Poms Institute of Financial Studies
    </div>
    <div id="kex-analyst-text" style="font-size: 12px; color: #2a3a00; line-height: 1.8;"></div>
    <div style="font-size: 9px; color: #888; text-align: right; margin-top: 10px; border-top: 1px dotted #CCC; padding-top: 5px; font-family: 'Courier New', monospace;">
        — M. Poms, Chief Analyst &nbsp;|&nbsp; <span id="kex-analyst-date"></span>
    </div>
</div>

<!-- ══════════════════════════════════════════ -->
<!-- PORTFOLIO OF THE DAY                       -->
<!-- ══════════════════════════════════════════ -->
<div class="kex-portfolio-box kex-reveal">
    <div class="kex-portfolio-title">💼 POMS' PORTFOLIO RECOMMENDATION OF THE DAY</div>
    <div id="kex-portfolio" style="line-height: 1.8;"></div>
    <div style="font-size: 9px; color: #007700; margin-top: 10px; border-top: 1px dotted #005500; padding-top: 6px;">
        ⚠ Past treat performance does not guarantee future chicken. Not financial advice. This IS cat advice.
        All portfolios approved by Monsieur Poms after reviewing them from directly on top of them.
    </div>
</div>

<div class="kex-disclaimer">
    The Kibble Exchange is regulated solely by Monsieur Poms and his legal team (the food bowl).<br>
    Green Bean Holdings (GLBN) has never recovered. Analysts project it never will. Monsieur Poms issues this as a public service announcement.<br>
    Market hours: always open, except during nap hours (approximately 20 hours per day). Trades executed upon waking.
</div>

</div><!-- /padding -->
</div><!-- /outer -->

<script>
(function () {

    // ── Deterministic seeded random (same engine as all other pages) ──────────
    function seededRand(s) {
        var x = Math.sin(s * 127.1 + 311.7) * 43758.5453123;
        return x - Math.floor(x);
    }
    function pick(arr, s) { return arr[Math.floor(seededRand(s) * arr.length)]; }
    function esc(s) { return String(s).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;'); }

    // ── Date seed ─────────────────────────────────────────────────────────────
    var now  = new Date();
    var doy  = Math.floor((now - new Date(now.getFullYear(), 0, 0)) / 86400000);
    var seed = now.getFullYear() * 1000 + doy;

    var dayNames   = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
    var monthNames = ["January","February","March","April","May","June","July","August","September","October","November","December"];
    var dateStr    = dayNames[now.getDay()] + ", " + monthNames[now.getMonth()] + " " + now.getDate() + ", " + now.getFullYear();

    document.getElementById('kex-date').textContent         = dateStr;
    document.getElementById('kex-analyst-date').textContent = dateStr;

    // ── Stocks ────────────────────────────────────────────────────────────────
    var stocks = [
        {
            sym: "CHKN",
            name: "Chicken Corp. International",
            desc: "The world's most essential food commodity. Sole approved diet of Monsieur Poms.",
            basePrice: 142.50,
            baseRange: [+2, +18],   // generally positive
            emoji: "🍗",
            sector: "Food & Sustenance"
        },
        {
            sym: "NAPS",
            name: "National Nap Index Fund",
            desc: "Diversified fund covering all premium sleeping positions, surfaces, and sunbeam intersections.",
            basePrice: 88.40,
            baseRange: [+1, +12],   // very stable, mostly positive
            emoji: "💤",
            sector: "Wellness & Rest"
        },
        {
            sym: "TRTS",
            name: "Premium Treats LLC",
            desc: "Leading producer of chicken-flavoured treats. Not a luxury. A necessity.",
            basePrice: 64.20,
            baseRange: [-4, +14],
            emoji: "🎁",
            sector: "Snack Markets"
        },
        {
            sym: "SUNBM",
            name: "Sunbeam Futures & Acquisition Trust",
            desc: "Specialists in prime sunbeam occupation rights and warm-spot territory claims.",
            basePrice: 55.80,
            baseRange: [-8, +15],   // volatile — weather dependent
            emoji: "☀️",
            sector: "Solar & Warmth"
        },
        {
            sym: "VCLZR",
            name: "Vocalization Industries Inc.",
            desc: "Diversified meowing and press conference solutions. Volume spikes at 3 AM.",
            basePrice: 37.90,
            baseRange: [-6, +20],   // unpredictable
            emoji: "📢",
            sector: "Communications"
        },
        {
            sym: "BWLCO",
            name: "BowlCo Fill Level Corp.",
            desc: "Critical infrastructure. Bowl fill rates are the market's most-watched indicator.",
            basePrice: 29.60,
            baseRange: [-15, +10],  // volatile, often declining
            emoji: "🥣",
            sector: "Food Infrastructure"
        },
        {
            sym: "CDBX",
            name: "CardBox Properties Ltd.",
            desc: "Premium cardboard real estate. Headquarters of Monsieur Poms. Cannot be relocated.",
            basePrice: 104.10,
            baseRange: [0, +8],     // stable, appreciated
            emoji: "📦",
            sector: "Real Estate"
        },
        {
            sym: "ZOMIE",
            name: "Zoomie Kinetics International",
            desc: "Classified operations. Source of energy: unknown. Speed: maximum. Reason: undisclosed.",
            basePrice: 22.30,
            baseRange: [-20, +35],  // extremely volatile
            emoji: "🏃",
            sector: "Energy & Kinetics"
        },
        {
            sym: "VCCN",
            name: "Vacuum Cleaner Corp.",
            desc: "A hostile entity. Listed under protest. Do not invest. Do not approach.",
            basePrice: 18.50,
            baseRange: [-18, -2],   // always declining
            emoji: "🌀",
            sector: "Hostile Entities"
        },
        {
            sym: "GLBN",
            name: "Global Green Bean Holdings",
            desc: "A prohibited commodity. Listed for educational purposes only. Has never recovered. Will not.",
            basePrice: 0.04,
            baseRange: [-0.02, -0.001], // basically zero, always falling
            emoji: "🥦",
            sector: "Prohibited Goods"
        }
    ];

    // ── Calculate today's price for each stock ─────────────────────────────
    function calcStock(stock, i) {
        var rLo = stock.baseRange[0];
        var rHi = stock.baseRange[1];
        var changePct = rLo + seededRand(seed + i * 37 + 7) * (rHi - rLo);

        var price;
        if (stock.sym === "GLBN") {
            // GLBN always near zero, always declining
            price = Math.max(0.001, stock.basePrice - seededRand(seed + i * 19) * 0.015);
        } else {
            // Add a multi-year drift based on year + doy so prices feel "accumulated"
            var driftFactor = 1 + (seed / 100000) * seededRand(seed + i * 53);
            price = stock.basePrice * driftFactor * (1 + changePct / 100);
            price = Math.max(0.01, price);
        }

        var change = price * changePct / 100;
        if (stock.sym === "GLBN") {
            change = -(seededRand(seed + i * 23) * 0.01 + 0.001);
        }

        var volume = Math.floor(seededRand(seed + i * 41) * 9500 + 500);

        return {
            price: price,
            change: change,
            changePct: stock.sym === "GLBN" ? -(seededRand(seed + i * 29) * 8 + 2) : changePct,
            volume: volume,
            open: price - change * 0.6,
            high: price + Math.abs(change) * seededRand(seed + i * 61) * 0.8,
            low:  price - Math.abs(change) * seededRand(seed + i * 67) * 0.8
        };
    }

    var computed = stocks.map(function (s, i) {
        return { stock: s, data: calcStock(s, i) };
    });

    // ── Market indices ─────────────────────────────────────────────────────
    // Kibble Composite Index (KCI) — weighted average of non-hostile stocks
    var kciRaw = 0, kciCt = 0;
    computed.forEach(function (c) {
        if (c.stock.sym !== "VCCN" && c.stock.sym !== "GLBN") {
            kciRaw += c.data.changePct;
            kciCt++;
        }
    });
    var kciChange = kciRaw / kciCt;
    var kciVal = 4281 + kciChange * 12 + seededRand(seed + 9999) * 40;

    // Chicken Futures Index
    var chknData = computed[0].data;
    var chknIdx  = chknData.price * 2.8 + seededRand(seed + 8888) * 15;

    // Complaint Volatility Index (CVI — higher is more volatile/complaining)
    var cviVal = 30 + Math.floor(seededRand(seed + 7777) * 70);

    var indices = [
        {
            name: "KCI — Kibble Composite",
            val: kciVal.toFixed(2),
            change: kciChange,
            sub: "Main market index"
        },
        {
            name: "CHKF — Chicken Futures",
            val: chknIdx.toFixed(2) + " TRT",
            change: chknData.changePct,
            sub: "Per portion, treat-denominated"
        },
        {
            name: "CVI — Complaint Volatility",
            val: cviVal,
            change: null,
            sub: cviVal >= 70 ? "HIGH — meow front incoming" : cviVal >= 45 ? "MODERATE — manageable" : "LOW — cautiously content"
        }
    ];

    var idxEl = document.getElementById('kex-indices');
    indices.forEach(function (idx) {
        var card = document.createElement('div');
        card.className = 'kex-index-card';
        var arrow = '';
        var col = '#FFFF00';
        if (idx.change !== null) {
            arrow = idx.change >= 0 ? '▲' : '▼';
            col   = idx.change >= 0 ? '#00FF66' : '#FF4444';
        }
        card.innerHTML =
            '<div class="kex-index-name">' + esc(idx.name) + '</div>' +
            '<div class="kex-index-val" style="color:' + col + ';text-shadow:0 0 8px ' + col + ';">' +
                esc(String(idx.val)) +
            '</div>' +
            (idx.change !== null
                ? '<div style="font-size:11px;color:' + col + ';font-weight:bold;">' +
                      arrow + ' ' + Math.abs(idx.change).toFixed(2) + '%' +
                  '</div>'
                : '') +
            '<div style="font-size:9px;color:#007700;margin-top:3px;">' + esc(idx.sub) + '</div>';
        idxEl.appendChild(card);
    });

    // ── Build the market board ─────────────────────────────────────────────
    var tbody = document.getElementById('kex-board');

    var hdr = document.createElement('thead');
    hdr.innerHTML =
        '<tr>' +
        '<th style="width:60px;">Symbol</th>' +
        '<th>Company</th>' +
        '<th style="width:75px;">Price (TRT)</th>' +
        '<th style="width:70px;">Change</th>' +
        '<th style="width:60px;">% Chg</th>' +
        '<th style="width:100px;">Sentiment</th>' +
        '<th style="width:65px;">Volume</th>' +
        '</tr>';
    tbody.appendChild(hdr);

    var tbodyEl = document.createElement('tbody');

    computed.forEach(function (c, i) {
        var s    = c.stock;
        var d    = c.data;
        var up   = d.change >= 0;
        var flat = Math.abs(d.changePct) < 0.5;
        var cls  = flat ? 'kex-flat' : (up ? 'kex-up' : 'kex-down');
        var arrow = flat ? '—' : (up ? '▲' : '▼');

        // Sentiment bar (based on change relative to its typical range)
        var rng  = s.baseRange[1] - s.baseRange[0];
        var norm = rng > 0 ? (d.changePct - s.baseRange[0]) / rng : 0.5;
        norm = Math.max(0, Math.min(1, norm));
        var barColor = norm > 0.6 ? '#00CC44' : (norm < 0.35 ? '#CC2200' : '#CCAA00');

        var priceStr;
        if (s.sym === "GLBN") {
            priceStr = d.price.toFixed(4);
        } else {
            priceStr = d.price.toFixed(2);
        }

        var changeStr;
        if (s.sym === "GLBN") {
            changeStr = d.change.toFixed(4);
        } else {
            changeStr = (d.change >= 0 ? '+' : '') + d.change.toFixed(2);
        }

        var pctStr = (d.changePct >= 0 ? '+' : '') + d.changePct.toFixed(2) + '%';

        var tr = document.createElement('tr');
        tr.className = 'kex-row-' + (i % 2 === 0 ? 'odd' : 'even');
        tr.innerHTML =
            '<td>' +
                '<div class="kex-ticker-sym">' + esc(s.sym) + '</div>' +
                '<div style="font-size:14px;line-height:1;">' + s.emoji + '</div>' +
            '</td>' +
            '<td>' +
                '<div style="color:#CCFFCC;font-size:11px;font-weight:bold;">' + esc(s.name) + '</div>' +
                '<div style="color:#007700;font-size:9px;margin-top:2px;">' + esc(s.sector) + '</div>' +
            '</td>' +
            '<td style="font-size:13px;font-weight:bold;color:#FFFF00;white-space:nowrap;">' +
                esc(priceStr) +
            '</td>' +
            '<td class="' + cls + '" style="white-space:nowrap;">' +
                arrow + ' ' + esc(changeStr) +
            '</td>' +
            '<td class="' + cls + '" style="white-space:nowrap;">' +
                esc(pctStr) +
            '</td>' +
            '<td>' +
                '<div class="kex-bar-outer"><div class="kex-bar-inner" style="width:' + (norm * 100).toFixed(0) + '%;background:' + barColor + ';"></div></div>' +
                '<div style="font-size:9px;color:' + barColor + ';margin-top:2px;">' +
                    (norm > 0.7 ? 'BULLISH' : (norm < 0.3 ? 'BEARISH' : 'NEUTRAL')) +
                '</div>' +
            '</td>' +
            '<td style="color:#007700;font-size:10px;white-space:nowrap;">' +
                d.volume.toLocaleString() +
            '</td>';
        tbodyEl.appendChild(tr);
    });

    tbody.appendChild(tbodyEl);

    // ── GLBN alert (if it drops below a threshold) ─────────────────────────
    var glbnData = computed[9].data;
    if (glbnData.price < 0.03) {
        document.getElementById('kex-glbn-alert').style.display = 'block';
    }

    // ── Scrolling ticker ──────────────────────────────────────────────────
    var tickerParts = computed.map(function (c) {
        var up = c.data.change >= 0;
        var arrow = c.data.change >= 0 ? '▲' : '▼';
        var pct = (c.data.changePct >= 0 ? '+' : '') + c.data.changePct.toFixed(2) + '%';
        return c.stock.sym + ' ' + c.stock.emoji + ' ' +
               (c.stock.sym === "GLBN" ? c.data.price.toFixed(4) : c.data.price.toFixed(2)) +
               ' ' + arrow + ' ' + pct;
    });
    var tickerStr = tickerParts.join('   ///   ');
    tickerStr += '   ///   KCI: ' + kciVal.toFixed(2) + (kciChange >= 0 ? ' ▲' : ' ▼') + Math.abs(kciChange).toFixed(2) + '%';
    tickerStr += '   ///   ANALYST: ' + (kciChange >= 1.5 ? 'BULLISH — CHICKEN CONFIRMED' : kciChange >= 0 ? 'STABLE — TREATS FLOWING' : 'BEARISH — BOWL SITUATION CRITICAL');
    document.getElementById('kex-ticker').textContent = tickerStr;

    // ── Analyst report ────────────────────────────────────────────────────
    var analystReports = [
        "Markets opened in an orderly fashion this morning, which is to say the food bowl was filled at an acceptable time and I was able to take my post at the observation desk before the opening bell. CHKN remains the cornerstone of any sound portfolio. I have reviewed the data personally. The data agrees with me.",
        "It is my professional assessment that NAPS is significantly undervalued by the broader market. Nap quality remains the most reliable indicator of household wellbeing. I am heavily invested — approximately 18 hours per day — and I have no intention of divesting at current conditions.",
        "VCLZR had an exceptional session overnight. Volume was high. The press conference at 3 AM was necessary, thorough, and completely justified by the prevailing bowl conditions. I expect continued strength throughout the week, particularly if the bowl situation remains unresolved.",
        "GLBN continues its historic decline, now approaching its 5,478th consecutive losing session. I have been calling this since 2010 and I will continue to call it for as long as green beans exist and I have a functioning voice, which is to say: indefinitely.",
        "SUNBM is exhibiting classic seasonal patterns — strongly correlated with cloud cover and the location of the premium living room beam. I secured my position at 9:02 AM and intend to hold through the afternoon session. Do not move me during active holding.",
        "ZOMIE had an extraordinary overnight session. Volumes were extremely high. The cause of the kinetic event remains classified at my discretion. What I can tell you is that the hallway is clear and the situation is resolved. I will not be providing further commentary.",
        "BWLCO declined sharply this morning following a critical fill-level event at 6:14 AM. The bowl reached 32% capacity — well below the minimum threshold established in Royal Decree No. 7734. Emergency vocalizations were deployed. The situation has since been partially resolved.",
        "CDBX continues to demonstrate extraordinary stability and long-term appreciation potential. The cardboard box headquarters has been in continuous operation since Q3 of this year and shows no signs of structural deterioration. It is my primary physical asset and I will be sitting in it later.",
        "TRTS is experiencing moderate volatility this session. Treat delivery was slightly behind schedule this afternoon, creating a brief but significant anxiety spike in the broader household market. Conditions have since stabilised following a successful deployment of the disappointed eyes.",
        "Overall market conditions today reflect what I would characterise as 'manageable with appropriate chicken.' CHKN continues to outperform. VCCN remains a hostile entity and should be avoided. Green beans are not a market instrument. I do not know why I continue to have to say this.",
        "My technical analysis today identifies a strong support zone for NAPS between 11 AM and 2 PM, with a secondary peak anticipated in the late afternoon. I entered a position at 10:45 AM and intend to hold it until dinner. Volume: high. Strategy: immaculate.",
        "VCCN — the Vacuum Cleaner — staged an unwanted incursion this morning without the required 48 hours of advance diplomatic notice. I evacuated the premises immediately. My official position on VCCN remains: short. It will always remain: short. This is constitutional."
    ];

    var report = pick(analystReports, seed + 404);
    document.getElementById('kex-analyst-text').innerHTML =
        '<p style="margin:0 0 10px;">' +
        '&ldquo;' + esc(report) + '&rdquo;' +
        '</p>' +
        '<p style="margin:0; font-size:10px; color:#5c7a00; font-style:italic;">' +
        'Credentials: Chief Analyst since 2010. Certified by the Poms Institute of Financial Studies. ' +
        'Methodology: staring at the market board from the food bowl observation post. ' +
        'Conflicts of interest: I am invested in CHKN emotionally, physically, and gastrointestinally.' +
        '</p>';

    // ── Portfolio of the day ──────────────────────────────────────────────
    var portfolios = [
        {
            alloc: [
                { sym: "CHKN", pct: 45, note: "Core holding. Non-negotiable. The entire strategy depends on this." },
                { sym: "NAPS", pct: 30, note: "Defensive position. Resilient in all market conditions." },
                { sym: "CDBX", pct: 15, note: "Stable real estate. Headquarters-grade. Hold indefinitely." },
                { sym: "TRTS", pct: 10, note: "Treat exposure. Maintain at all times for tactical flexibility." }
            ],
            name: "THE CLASSIC POMS",
            summary: "The all-weather portfolio. Maximum chicken exposure. Zero green beans. Never fails. I have never lost money on this allocation and I intend to maintain this track record."
        },
        {
            alloc: [
                { sym: "CHKN", pct: 35, note: "Core. Always." },
                { sym: "SUNBM", pct: 25, note: "Seasonal strength expected. Position secured as of 9 AM." },
                { sym: "VCLZR", pct: 20, note: "High-conviction call. Volume elevated today. Press conferences imminent." },
                { sym: "NAPS", pct: 20, note: "Defensive floor. Will not move below this allocation." }
            ],
            name: "THE VOCAL GROWTH FUND",
            summary: "Aggressive positioning across chicken and communications. For investors who believe in direct, high-volume advocacy and are not afraid of 3 AM volatility. I believe in this."
        },
        {
            alloc: [
                { sym: "NAPS", pct: 40, note: "Maximum defensive position. I am currently executing this strategy." },
                { sym: "CHKN", pct: 35, note: "Essential sustenance allocation. Cannot be reduced." },
                { sym: "CDBX", pct: 25, note: "Headquarters REIT. The box is operational. The box is mine." }
            ],
            name: "THE LOAF PRESERVATION STRATEGY",
            summary: "Conservative allocation focused on stability, warmth, and minimal disruption. Ideal for days when I am in loaf mode and cannot be moved. Do not tap the portfolio."
        },
        {
            alloc: [
                { sym: "ZOMIE", pct: 30, note: "High-risk, high-reward. Source classified. Performance: maximum." },
                { sym: "CHKN", pct: 35, note: "Risk mitigation via chicken. Standard practice." },
                { sym: "VCLZR", pct: 20, note: "Elevated today. Multiple press conferences scheduled." },
                { sym: "TRTS", pct: 15, note: "Tactical treat reserve for negotiation purposes." }
            ],
            name: "THE MIDNIGHT PORTFOLIO",
            summary: "High-conviction, high-volatility strategy. Results: excellent, but unpredictable. Best entered at 10 PM. Sources of outperformance: classified. Do not follow me into this trade. Just trust me."
        },
        {
            alloc: [
                { sym: "CHKN", pct: 50, note: "50% is the minimum I will accept in any portfolio. This is also the maximum. I am open to negotiating upward." },
                { sym: "BWLCO", pct: 20, note: "Bowl infrastructure. Currently underweight. Requires urgent attention." },
                { sym: "TRTS", pct: 20, note: "Essential snack market exposure. Non-discretionary." },
                { sym: "CDBX", pct: 10, note: "Stable anchor. The box has been appraised. I sat in it during the appraisal." }
            ],
            name: "THE BOWL RECOVERY FUND",
            summary: "Constructed following this morning's bowl-level incident. Overweight CHKN as a direct corrective measure. The situation has been assessed from the food bowl observation post and this portfolio is the appropriate response."
        }
    ];

    var todayPortfolio = pick(portfolios, seed + 808);
    var portHtml = '<div style="font-size:13px;color:#FFFF00;font-family:\'Impact\',\'Arial Black\',sans-serif;letter-spacing:1px;margin-bottom:8px;text-shadow:0 0 6px #00FF00;">' +
        '&ldquo;' + esc(todayPortfolio.name) + '&rdquo;' +
        '</div>';
    portHtml += '<div style="font-size:10px;color:#00AA00;font-style:italic;margin-bottom:10px;">' + esc(todayPortfolio.summary) + '</div>';

    todayPortfolio.alloc.forEach(function (a) {
        var barW = a.pct;
        portHtml +=
            '<div style="margin-bottom:7px;">' +
            '<div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:2px;">' +
                '<span style="font-size:12px;color:#FFFF00;font-weight:bold;">' + esc(a.sym) + '</span>' +
                '<span style="font-size:12px;color:#00FF00;">' + a.pct + '%</span>' +
            '</div>' +
            '<div style="background:#003300;border:1px solid #005500;height:14px;overflow:hidden;margin-bottom:2px;">' +
                '<div style="height:100%;width:' + barW + '%;background:linear-gradient(to right,#005500,#00AA00);animation:kexFill 0.8s ease-out forwards;"></div>' +
            '</div>' +
            '<div style="font-size:9px;color:#007700;font-style:italic;">' + esc(a.note) + '</div>' +
            '</div>';
    });

    document.getElementById('kex-portfolio').innerHTML = portHtml;

}());
</script>
