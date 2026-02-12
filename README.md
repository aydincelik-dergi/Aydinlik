<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aydın Çelik - E-Dergi</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Lora:ital@0;1&display=swap" rel="stylesheet">
    <style>
        :root {
            --ana-renk: #1a1a1a;
            --vurgu-renk: #c0392b;
            --altin-renk: #d4af37;
            --kagit-rengi: #fdfcf8;
        }

        * { box-sizing: border-box; }

        body {
            margin: 0;
            background-color: #222;
            font-family: 'Lora', serif;
            scroll-snap-type: y mandatory;
            overflow-y: scroll;
            height: 100vh;
        }

        .magazine {
            width: 100%;
            max-width: 900px;
            margin: 0 auto;
        }

        .page {
            height: 100vh;
            width: 100%;
            background-color: var(--kagit-rengi);
            display: flex;
            flex-direction: column;
            padding: 60px;
            scroll-snap-align: start;
            position: relative;
            box-shadow: 0 0 50px rgba(0,0,0,0.5);
            overflow: hidden;
        }

        .page-number {
            position: absolute;
            bottom: 30px;
            right: 50px;
            font-size: 0.9rem;
            color: #777;
            font-weight: bold;
        }

        /* --- 1. SAYFA: KAPAK --- */
        .cover {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1512820790803-83ca734da794?q=80&w=1000') no-repeat center;
            background-size: cover;
            color: white;
            text-align: center;
            justify-content: space-around;
        }

        .cover h1 {
            font-family: 'Playfair Display', serif;
            font-size: 5rem;
            margin: 0;
            letter-spacing: 10px;
            border-top: 3px solid white;
            border-bottom: 3px solid white;
            display: inline-block;
            padding: 15px 0;
        }

        /* --- 2. SAYFA: EDİTÖRDEN --- */
        .title { font-family: 'Playfair Display', serif; font-size: 2.8rem; margin-bottom: 20px; color: var(--ana-renk); }
        .dropcap::first-letter {
            float: left; font-size: 5rem; line-height: 1; padding-right: 12px; color: var(--vurgu-renk); font-weight: bold;
        }
        .content-body { column-count: 2; column-gap: 40px; text-align: justify; line-height: 1.8; }

        /* --- 3. SAYFA: ŞİİR KÖŞESİ --- */
        .poetry-container { border: 1px solid var(--altin-renk); padding: 40px; margin: auto; position: relative; text-align: center; }
        .poem-lines { font-style: italic; font-size: 1.3rem; line-height: 2.2; white-space: pre-line; }
        .signature { font-family: 'Playfair Display', serif; font-style: italic; font-size: 1.8rem; color: var(--vurgu-renk); margin-top: 20px; }

        /* --- 4. SAYFA: GALERİ --- */
        .gallery-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 15px; margin-top: 30px; }
        .photo-card { border: 1px solid var(--altin-renk); height: 200px; overflow: hidden; position: relative; }
        .photo-card img { width: 100%; height: 100%; object-fit: cover; transition: 0.5s; }
        .photo-card:hover img { transform: scale(1.1); }
   /* --- 5. SAYFA: SARA --- */
        .sara-box { background: rgba(255,255,255,0.9); padding: 40px; border-top: 5px solid var(--vurgu-renk); margin: auto; }

        /* --- 6. SAYFA: ARKA KAPAK --- */
        .back-cover { background-color: #2c3e50; color: white; text-align: center; justify-content: center; }
        .buy-btn { display: inline-block; padding: 12px 30px; background: var(--altin-renk); color: #1a1a1a; text-decoration: none; font-weight: bold; margin-top: 20px; }

        @media (max-width: 768px) { .content-body { column-count: 1; } .gallery-grid { grid-template-columns: 1fr 1fr; } }
    </style>
</head>
<body>

    <div class="magazine">
        <section class="page cover">
            <div>
                <p style="letter-spacing: 5px;">KÜLTÜR VE SANAT</p>
                <h1>AYDINLIK</h1>
            </div>
            <div>
                <p style="font-size: 1.5rem;">AYDIN ÇELİK</p>
                <p>ŞUBAT 2026 | SAYI 1</p>
            </div>
        </section>

        <section class="page">
            <h2 class="title">Yeni Bir Soluk</h2>
            <div class="content-body">
                <p class="dropcap">Van'ın bereketli topraklarından İstanbul'un asaletine uzanan bu yolculukta, kalemimi kağıtla buluşturmanın sevincini yaşıyorum. 1968'den bugüne süzülen hayat tecrübelerimi, emekliliğin huzuruyla birleştirerek bu dergiyi oluşturdum.</p>
                <p>Burada sadece bir yazar değil, bir dost, bir beyefendi ve bir aşık bulacaksınız. Yazılarımda geçmişin izlerini sürerken, geleceğe dair umutlarımızı yeşerteceğiz. Hoş geldiniz.</p>
            </div>
            <div class="page-number">01</div>
        </section>

        <section class="page">
            <div class="poetry-container">
                <h2 class="title" style="font-size: 2rem;">İki Gözüm</h2>
                <div class="poem-lines">
                    Van'ın soğuk yelleri eserken derinden,
                    Bir sızı yükselir kalbin en orta yerinden.
                    Gözlerim ufukta, hatıralar dökülür;
                    Sözlerin mühürlenir, ömürden ömür sökülür.
                </div>
                <div class="signature">Aydın Çelik</div>
            </div>
            <div class="page-number">02</div>
        </section>

        <section class="page" style="background-color: #1a1a1a; color: white;">
            <h2 class="title" style="color: white; text-align: center;">Anılar Galerisi</h2>
            <div class="gallery-grid">
                <div class="photo-card"><img src="https://images.unsplash.com/photo-1507679799987-c73779587ccf?w=400"><div style="position:absolute; bottom:0; background:rgba(0,0,0,0.5); width:100%; padding:5px; font-size:0.8rem; text-align:center;">Asalet</div></div>
                <div class="photo-card"><img src="https://images.unsplash.com/photo-1542332213-9b5a5a3fad35?w=400"><div style="position:absolute; bottom:0; background:rgba(0,0,0,0.5); width:100%; padding:5px; font-size:0.8rem; text-align:center;">Van Ruhu</div></div>
				
				 <div class="photo-card"><img src="https://images.unsplash.com/photo-1455390582262-044cdead277a?w=400"><div style="position:absolute; bottom:0; background:rgba(0,0,0,0.5); width:100%; padding:5px; font-size:0.8rem; text-align:center;">İlham</div></div>
            </div>
            <div class="page-number">03</div>
        </section>

        <section class="page" style="background: url('https://images.unsplash.com/photo-1516589174184-c685266d4af4?w=1000') no-repeat center; background-size: cover;">
            <div class="sara-box">
                <h2 class="title" style="text-align: center;">Sara: Olgun Bir Aşk</h2>
                <p style="font-style: italic; line-height: 1.8; text-align: justify;">
                    Bizimkisi, kelimelerin bittiği yerde başlayan bir anlayış. Sara, hayatımın en durgun ama en derin limanı. Aydın ve Sara... Birbirini tamamlayan iki ruhun hikayesi bu.
                </p>
				<p style="text-align: center; color: var(--vurgu-renk); font-weight: bold; margin-top: 20px;">"Seninle yaşlanmak değil, seninle yaşamak güzel..."</p>
            </div>
            <div class="page-number">04</div>
        </section>

        <section class="page back-cover">
            <h1>AÇ</h1>
            <p style="letter-spacing: 3px;">AYDIN ÇELİK</p>
            <div style="border: 1px solid var(--altin-renk); padding: 20px; margin: 30px 0;">
                <p>"İki Gözüm" Şiir Kitabı Yayında!</p>
                <a href="#" class="buy-btn">SATIN AL</a>
            </div>
            <p>📧 info@aydincelik.com<br>📍 İstanbul / Van</p>
            <div class="page-number" style="color: white;">05</div>
        </section>
    </div>

</body>
</html>
