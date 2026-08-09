<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Another Visual | JKT Creative Agency</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;500;700;900&family=Plus+Jakarta+Sans:wght@400;500;600&display=swap" rel="stylesheet">

    <style>
        :root {
            --bg-base: #09090b;
            --bg-surface: rgba(24, 24, 27, 0.4);
            --bg-surface-hover: rgba(39, 39, 42, 0.6);
            --text-main: #ffffff;
            --text-muted: #a1a1aa;
            --accent: #ffffff;
            --border-color: rgba(255, 255, 255, 0.06);
            --radius-lg: 32px;
            --radius-md: 20px;
            --transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-font-smoothing: antialiased;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            color: var(--text-main);
            background-color: var(--bg-base);
            overflow-x: hidden;
            line-height: 1.6;
        }

        h1, h2, h3, h4, .brand-text {
            font-family: 'Outfit', sans-serif;
        }

        /* BACKGROUND JAKARTA */
        .jakarta-bg {
            position: fixed;
            inset: 0;
            width: 100vw;
            height: 100vh;
            background: url('https://images.unsplash.com/photo-1555899434-94d1368aa7af?q=80&w=2000') center/cover no-repeat;
            filter: grayscale(100%) opacity(12%) blur(2px);
            z-index: -2;
        }

        .grain-overlay {
            position: fixed;
            inset: 0;
            background: radial-gradient(circle at center, transparent 0%, #09090b 100%);
            z-index: -1;
            pointer-events: none;
        }

        /* FLOATING NAVBAR */
        header {
            position: fixed;
            top: 25px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            align-items: center;
            justify-content: space-between;
            background: rgba(9, 9, 11, 0.6);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid var(--border-color);
            padding: 8px 12px 8px 24px;
            border-radius: 100px;
            width: 90%;
            max-width: 1000px;
            z-index: 1000;
        }

        .brand {
            display: flex;
            align-items: center;
            gap: 12px;
            cursor: pointer;
        }

        .brand-text {
            font-size: 18px;
            font-weight: 700;
            letter-spacing: -0.5px;
        }

        nav {
            display: flex;
            gap: 5px;
            background: rgba(255, 255, 255, 0.03);
            padding: 5px;
            border-radius: 100px;
        }

        nav a {
            color: var(--text-muted);
            text-decoration: none;
            font-size: 14px;
            font-weight: 500;
            padding: 10px 24px;
            border-radius: 100px;
            cursor: pointer;
            transition: var(--transition);
        }

        nav a:hover { color: var(--text-main); }
        nav a.active {
            background: var(--accent);
            color: var(--bg-base);
            font-weight: 600;
        }

        /* PAGE SECTIONS */
        .page {
            display: none;
            padding: 160px 5% 100px 5%;
            min-height: 100vh;
            max-width: 1300px;
            margin: 0 auto;
            animation: elegantFade 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
        }

        .page.active { display: block; }

        @keyframes elegantFade {
            0% { opacity: 0; transform: translateY(30px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        .section-tag {
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: var(--text-muted);
            margin-bottom: 12px;
            display: block;
        }

        .section-title {
            font-size: 48px;
            font-weight: 700;
            letter-spacing: -1px;
            margin-bottom: 60px;
            line-height: 1.1;
        }

        /* BENTO CARDS */
        .bento-card {
            background: var(--bg-surface);
            border: 1px solid var(--border-color);
            border-radius: var(--radius-lg);
            padding: 45px;
            backdrop-filter: blur(10px);
            transition: var(--transition);
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
        }

        .bento-card:hover {
            background: var(--bg-surface-hover);
            transform: translateY(-5px);
        }

        .bento-card h3 { font-size: 32px; font-weight: 500; margin-bottom: 15px; }
        .bento-card p { color: var(--text-muted); font-size: 16px; line-height: 1.7; }

        /* HERO SECTION */
        .hero {
            text-align: center;
            max-width: 900px;
            margin: 60px auto 100px auto;
        }

        .hero h1 {
            font-size: 72px;
            font-weight: 900;
            letter-spacing: -3px;
            line-height: 1.05;
            margin-bottom: 30px;
        }

        .hero h1 span { color: var(--text-muted); font-weight: 300; }

        .hero p {
            font-size: 20px;
            color: var(--text-muted);
            margin-bottom: 50px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .btn-primary {
            display: inline-block;
            padding: 18px 40px;
            background: var(--accent);
            color: var(--bg-base);
            text-decoration: none;
            font-family: 'Outfit', sans-serif;
            font-weight: 600;
            font-size: 16px;
            border-radius: 100px;
            transition: var(--transition);
            cursor: pointer;
        }

        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 0 40px rgba(255,255,255,0.2);
        }

        .bento-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 24px;
            margin-bottom: 100px;
        }

        /* FOLDER PORTOFOLIO */
        .folder-nav {
            display: flex;
            gap: 10px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .folder-btn {
            background: transparent;
            color: var(--text-muted);
            border: 1px solid var(--border-color);
            padding: 12px 28px;
            border-radius: 100px;
            cursor: pointer;
            font-family: 'Outfit', sans-serif;
            font-weight: 500;
            font-size: 15px;
            transition: var(--transition);
        }

        .folder-btn:hover, .folder-btn.active {
            background: var(--accent);
            color: var(--bg-base);
            border-color: var(--accent);
        }

        .masonry-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 20px;
        }

        .port-item {
            position: relative;
            border-radius: var(--radius-md);
            overflow: hidden;
            aspect-ratio: 4/5;
            cursor: pointer;
            border: 1px solid var(--border-color);
        }

        .port-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .port-overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(to top, rgba(9,9,11,0.9) 0%, rgba(9,9,11,0) 60%);
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            padding: 30px;
            opacity: 0;
            transition: var(--transition);
        }

        .port-item:hover img { transform: scale(1.05); }
        .port-item:hover .port-overlay { opacity: 1; }
        
        .port-cat { color: var(--text-muted); font-size: 13px; text-transform: uppercase; letter-spacing: 1px; }
        .port-title { font-family: 'Outfit', sans-serif; font-size: 28px; font-weight: 500; }

        /* SLIDER MODAL PORTFOLIO */
        .modal-glass {
            display: none; 
            position: fixed; 
            inset: 0; 
            background: rgba(9, 9, 11, 0.95);
            backdrop-filter: blur(12px); 
            z-index: 2000; 
            justify-content: center; 
            align-items: center;
        }
        
        .modal-box {
            position: relative;
            max-width: 800px;
            width: 90%;
            text-align: center;
        }

        .modal-box img {
            width: 100%;
            max-height: 70vh;
            object-fit: contain;
            border-radius: 16px;
            border: 1px solid var(--border-color);
        }

        .client-info {
            margin-top: 20px;
            font-family: 'Outfit', sans-serif;
            font-size: 22px;
            font-weight: 500;
            color: #fff;
        }

        .slide-btn {
            position: absolute;
            top: 45%;
            transform: translateY(-50%);
            background: rgba(255,255,255,0.1);
            color: #fff;
            border: none;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            cursor: pointer;
            font-size: 20px;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .slide-btn:hover { background: var(--accent); color: var(--bg-base); }
        .prev-btn { left: -70px; }
        .next-btn { right: -70px; }
        .close-modal { position: absolute; top: -60px; right: 0; color: #fff; font-size: 40px; cursor: pointer; font-family: 'Outfit'; }

        /* PRICELIST (PERBESAR & CENTER) */
        .price-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 24px;
            margin-bottom: 80px;
        }

        .price-card {
            background: var(--bg-surface);
            border: 1px solid var(--border-color);
            border-radius: var(--radius-lg);
            padding: 50px 40px;
            display: flex;
            flex-direction: column;
            text-align: center;
            align-items: center;
            transition: var(--transition);
        }

        .price-card.premium {
            background: rgba(255, 255, 255, 0.04);
            border-color: rgba(255, 255, 255, 0.25);
        }

        .price-card h3 { font-size: 26px; color: var(--text-muted); font-weight: 500; }
        
        .price-amount { 
            font-family: 'Outfit', sans-serif; 
            font-size: 52px; 
            font-weight: 900; 
            margin: 15px 0 35px 0; 
            letter-spacing: -2px;
            color: #ffffff;
        }
        
        .price-features { 
            list-style: none; 
            flex-grow: 1; 
            margin-bottom: 40px; 
            width: 100%;
        }
        
        .price-features li {
            padding: 16px 0; 
            border-bottom: 1px solid var(--border-color); 
            font-size: 16px; 
            color: #d4d4d8;
        }

        .btn-outline {
            display: block; width: 100%; text-align: center; padding: 18px; border: 1px solid var(--text-muted);
            color: var(--text-main); text-decoration: none; border-radius: 100px; font-weight: 600; font-family: 'Outfit', sans-serif; transition: var(--transition);
        }
        .btn-outline:hover { background: var(--text-main); color: var(--bg-base); }
        
        .btn-solid {
            display: block; width: 100%; text-align: center; padding: 18px; background: var(--accent);
            color: var(--bg-base); text-decoration: none; border-radius: 100px; font-weight: 700; font-family: 'Outfit', sans-serif; transition: var(--transition);
        }
        .btn-solid:hover { transform: translateY(-3px); box-shadow: 0 10px 30px rgba(255,255,255,0.2); }

        /* ABOUT & CONTACT */
        .about-layout { display: grid; grid-template-columns: 1fr 1fr; gap: 40px; }
        .founder-text h3 { font-size: 40px; letter-spacing: -1px; margin-bottom: 10px; }
        .founder-text h4 { color: var(--text-muted); font-size: 18px; margin-bottom: 30px; font-weight: 400; }
        .founder-text p { font-size: 16px; color: #d4d4d8; margin-bottom: 20px; }

        .contact-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
        .contact-card { text-align: center; padding: 50px 30px; }
        .contact-card h4 { font-size: 24px; margin-bottom: 15px; }
        .contact-card a { color: var(--text-muted); text-decoration: none; font-size: 18px; transition: var(--transition); }
        .contact-card a:hover { color: var(--text-main); }

        /* FOOTER (IKON SOSMED DI BAWAH) */
        footer {
            padding: 80px 5% 50px 5%;
            text-align: center;
            border-top: 1px solid var(--border-color);
            margin-top: 50px;
            background: rgba(9, 9, 11, 0.5);
        }
        
        .footer-quote { font-family: 'Outfit', sans-serif; font-size: 28px; font-weight: 300; max-width: 800px; margin: 0 auto 30px auto; color: var(--text-muted); }
        
        .footer-socials {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .social-icon-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: var(--bg-surface);
            border: 1px solid var(--border-color);
            border-radius: 50%;
            color: var(--text-main);
            transition: var(--transition);
            text-decoration: none;
        }

        .social-icon-btn:hover {
            background: var(--accent);
            color: var(--bg-base);
            border-color: var(--accent);
            transform: translateY(-4px);
        }

        .social-icon-btn svg {
            width: 20px;
            height: 20px;
            fill: currentColor;
        }

        .copyright { color: #52525b; font-size: 14px; }

        @media (max-width: 900px) {
            header { flex-direction: column; border-radius: var(--radius-md); padding: 15px; gap: 20px; width: 95%; top: 15px;}
            nav { flex-wrap: wrap; justify-content: center; }
            .hero h1 { font-size: 48px; }
            .bento-grid { grid-template-columns: 1fr; }
            .about-layout { grid-template-columns: 1fr; }
            .page { padding-top: 220px; }
            .slide-btn { display: none; }
        }
    </style>
</head>
<body>

    <div class="jakarta-bg"></div>
    <div class="grain-overlay"></div>

    <header>
        <div class="brand" onclick="navTo('home')">
            <span class="brand-text">ANOTHER VISUAL.</span>
        </div>
        <nav>
            <a onclick="navTo('home')" id="nav-home" class="active">Beranda</a>
            <a onclick="navTo('portfolio')" id="nav-portfolio">Portofolio</a>
            <a onclick="navTo('pricelist')" id="nav-pricelist">Paket Harga</a>
            <a onclick="navTo('about')" id="nav-about">Tentang Kami</a>
            <a onclick="navTo('contact')" id="nav-contact">Kontak</a>
        </nav>
    </header>

    <section id="page-home" class="page active">
        <div class="hero">
            <h1>Visual Storytelling <br><span>Untuk Brand Modern.</span></h1>
            <p>Agensi kreatif berbasis di Jakarta. Kami siap menerjemahkan momen spesial Anda menjadi karya visual komersial yang berkelas dan timeless.</p>
            <a onclick="navTo('portfolio')" class="btn-primary">Lihat Karya Kami</a>
        </div>

        <div class="bento-grid">
            <div class="bento-card">
                <span class="section-tag">Filosofi Kami</span>
                <h3>Estetika Tanpa Batas</h3>
                <p>Kami percaya bahwa mahakarya visual tidak ditentukan seberapa mahal alat yang digenggam, melainkan bagaimana ketajaman mata seorang kreator dalam merangkai cerita, komposisi, dan emosi di setiap jepretan.</p>
            </div>
            
            <div class="bento-card">
                <span class="section-tag">Visi Kami</span>
                <h3>Karya yang Berbicara</h3>
                <p>Visi utama kami adalah menghadirkan standar visual tertinggi yang menyentuh hati. Melalui teknik pencahayaan matang, sudut pandang sinematik, dan sentuhan emosional, setiap momen diabadikan bukan sekadar gambar, melainkan sebuah mahakarya abadi.</p>
            </div>
        </div>
    </section>

    <section id="page-portfolio" class="page">
        <span class="section-tag">Galeri Pilihan</span>
        <h2 class="section-title">Portofolio</h2>

        <div class="folder-nav">
            <button class="folder-btn active" onclick="filterItems('all')">Semua Folder</button>
            <button class="folder-btn" onclick="filterItems('wedding')">Wedding</button>
            <button class="folder-btn" onclick="filterItems('engagement')">Engagement</button>
            <button class="folder-btn" onclick="filterItems('wisuda')">Wisuda</button>
            <button class="folder-btn" onclick="filterItems('event')">Event</button>
        </div>

        <div class="masonry-grid">
            <div class="port-item wedding" onclick="openSlider([
                'https://lh3.googleusercontent.com/d/1K5JYuw4FpqSI9NEduRvZNm_8eJRS_Mr2',
                'https://lh3.googleusercontent.com/d/1sJJIfzNtLeDnY69v5Vw9it6EMWJzScWO',
                'https://lh3.googleusercontent.com/d/18V0VTAzCCy9rw8Pkyy3jwVr06jbwqXjE',
                'https://lh3.googleusercontent.com/d/18AiExWPI4x61GapsGDVEBAq6v3mhiUvw',
                'https://lh3.googleusercontent.com/d/1jKrtiykv5AEAyyIixWZJIblm4kwSbvj3',
                'https://lh3.googleusercontent.com/d/1AG35QW1gkHG_ysKrIjzmgwSdZ-WDJE_W',
                'https://lh3.googleusercontent.com/d/1VikQ2MtDl94PstxWeOPGFGZZBA76wRAJ',
                'https://lh3.googleusercontent.com/d/18UYnUMDsVlxNF5CD3oRa7ShpY560WHPY',
                'https://lh3.googleusercontent.com/d/12_urvrE4195fyQmf1RhEv3-ToTvxv6l5',
                'https://lh3.googleusercontent.com/d/1ffcvFRZDPaoMzVLIgqm3GgDp83qRak6v'
            ], 'Wedding Falaq & Cindy')">
                <img src="https://lh3.googleusercontent.com/d/1K5JYuw4FpqSI9NEduRvZNm_8eJRS_Mr2" alt="Wedding Falaq & Cindy">
                <div class="port-overlay">
                    <div class="port-cat">Wedding (10 Foto)</div>
                    <div class="port-title">Falaq & Cindy</div>
                </div>
            </div>

            <div class="port-item engagement" onclick="openSlider([
                'https://lh3.googleusercontent.com/d/1CSJdaeY-POpOhoytFeI4PyPvCc6_43Jk',
                'https://lh3.googleusercontent.com/d/1RZIXo9bAFTMbIv327LqCBZZys3No0Jop',
                'https://lh3.googleusercontent.com/d/16RB0mGvb4YMqixSaT5ugndThBWce_IP4',
                'https://lh3.googleusercontent.com/d/1pgDLZcUJxZ5fiGv4EadaWnQyigXkrLmc',
                'https://lh3.googleusercontent.com/d/1ul39oBgor5kz0XAVGsM0vEPVOcfrKVv9',
                'https://lh3.googleusercontent.com/d/1N-vITNSioYPnd2WtIzGNU8BDtiHVtGz7',
                'https://lh3.googleusercontent.com/d/1JLmj7thqafLvTXMTqGZXCLMx5mo1gtpm',
                'https://lh3.googleusercontent.com/d/1aVgL_GPfg2adk_RN1UYLaL1vM1wkZ8iw',
                'https://lh3.googleusercontent.com/d/1bl36KWAmRwiRCaqQicr1xZhBOc86RcwO',
                'https://lh3.googleusercontent.com/d/17yN3ucaM5EtI46O7e8fGwdWyKxfylyCW',
                'https://lh3.googleusercontent.com/d/1boUj5TLrYIWDkrcgW8AQsTghgnke36rk',
                'https://lh3.googleusercontent.com/d/1UmCat8QQcEtkDr2KyzhM0yWys7l7LDkc',
                'https://lh3.googleusercontent.com/d/19I127-vR7AFi6OKdj2vFYBLA6DJofGMU',
                'https://lh3.googleusercontent.com/d/1V6GRE0pDTMDO0aAtyE6vj7r2w-FJXHes',
                'https://lh3.googleusercontent.com/d/1Ui7W4zjre4TtivvXq2NDbsyw3gTqqIhC'
            ], 'Engagement Fikry & Reny')">
                <img src="https://lh3.googleusercontent.com/d/1CSJdaeY-POpOhoytFeI4PyPvCc6_43Jk" alt="Engagement Fikry & Reny">
                <div class="port-overlay">
                    <div class="port-cat">Engagement (15 Foto)</div>
                    <div class="port-title">Fikry & Reny</div>
                </div>
            </div>

            <div class="port-item wisuda" onclick="openSlider([
                'https://lh3.googleusercontent.com/d/1tdANeaA_DLSrfHtAXZQQEDzNckCwCl_u',
                'https://lh3.googleusercontent.com/d/1ANX4TlyLrA2rg4es-1twvUenPk2xD8ha',
                'https://lh3.googleusercontent.com/d/1L9HRUY0fNw6iAVpeb3TofmZWORZY82so',
                'https://lh3.googleusercontent.com/d/1qNz-6khAoXYFkU-cQZjn8pYdT9MIRfPM',
                'https://lh3.googleusercontent.com/d/1X4687Zb8Zos-tGLzKB44nmIBlZeBrR9_',
                'https://lh3.googleusercontent.com/d/1CTqP6v3eLVrPBklcaRW7sttGg4_QwgCx',
                'https://lh3.googleusercontent.com/d/1sPew-WXRoUgqJr-7rJXoqHli882oFJi1'
            ], 'Wisuda Reny Riani')">
                <img src="https://lh3.googleusercontent.com/d/1tdANeaA_DLSrfHtAXZQQEDzNckCwCl_u" alt="Wisuda Reny Riani">
                <div class="port-overlay">
                    <div class="port-cat">Wisuda (7 Foto)</div>
                    <div class="port-title">Reny Riani</div>
                </div>
            </div>

            <div class="port-item event" onclick="openSlider([
                'https://lh3.googleusercontent.com/d/1zm6ILIXa8mNLJ5z2Y-J-zN1JUZzmON6w',
                'https://lh3.googleusercontent.com/d/1_axQ1oATs8QwUrEDC56LEWqSs5cwa5LA',
                'https://lh3.googleusercontent.com/d/1k5xQXFot-YZCUz8_3JCm_UTj2gaaFd_Y',
                'https://lh3.googleusercontent.com/d/1rLXnbHyq6fo_bcscrBcXqjiXNjQ9dcYN',
                'https://lh3.googleusercontent.com/d/1zkjFPSBp0x4keMEPfFJv0tGuRjHae2GL',
                'https://lh3.googleusercontent.com/d/1cWtB847VpSlCIG_KqRce9I6_5ql_TU5O',
                'https://lh3.googleusercontent.com/d/1fT-R800YeD44qZNZnl-KKq6qPQkgs39p'
            ], 'Corporate - Jalan Santai Kemerdekaan 2025')">
                <img src="https://lh3.googleusercontent.com/d/1zm6ILIXa8mNLJ5z2Y-J-zN1JUZzmON6w" alt="Corporate Event">
                <div class="port-overlay">
                    <div class="port-cat">Corporate Event (7 Foto)</div>
                    <div class="port-title">Jalan Santai 2025</div>
                </div>
            </div>
        </div>
    </section>

    <div class="modal-glass" id="imageModal">
        <div class="modal-box">
            <span class="close-modal" onclick="closeModal()">×</span>
            <button class="slide-btn prev-btn" onclick="changeSlide(-1)">❮</button>
            <img id="modalImgSrc" src="">
            <button class="slide-btn next-btn" onclick="changeSlide(1)">❯</button>
            <div class="client-info" id="clientNameText">Nama Klien</div>
        </div>
    </div>

    <section id="page-pricelist" class="page">
        <span class="section-tag">Investasi</span>
        <h2 class="section-title">Daftar Paket Harga</h2>

        <span class="section-tag" style="color: #fff; margin-bottom: 20px;">01. Paket Wedding</span>
        <div class="price-grid">
            <div class="price-card">
                <h3>Basic</h3>
                <div class="price-amount">Rp 850.000</div>
                <ul class="price-features">
                    <li>1-2 Fotografer Profesional</li>
                    <li>Full Color Grading & Editing</li>
                    <li>Durasi Fleksibel (Mengikuti Klien)</li>
                    <li>Pengiriman via Google Drive</li>
                </ul>
                <a href="https://wa.me/6287765829615" target="_blank" class="btn-outline">Pilih Paket</a>
            </div>
            <div class="price-card premium">
                <h3>Premium</h3>
                <div class="price-amount">Rp 1.500.000</div>
                <ul class="price-features">
                    <li>1 Fotografer & 1 Videografer</li>
                    <li>Edit Foto + Video Sinematik (Max 5 Menit)</li>
                    <li>Durasi Fleksibel (Mengikuti Klien)</li>
                    <li>Pengiriman via Google Drive</li>
                </ul>
                <a href="https://wa.me/6287765829615" target="_blank" class="btn-solid">Pilih Paket</a>
            </div>
        </div>

        <span class="section-tag" style="color: #fff; margin-bottom: 20px;">02. Paket Engagement</span>
        <div class="price-grid">
            <div class="price-card">
                <h3>Foto Saja</h3>
                <div class="price-amount">Rp 350.000</div>
                <ul class="price-features">
                    <li>1-2 Fotografer</li>
                    <li>Full Editing Foto</li>
                    <li>Durasi Fleksibel</li>
                </ul>
                <a href="https://wa.me/6287765829615" target="_blank" class="btn-outline">Pilih Paket</a>
            </div>
            <div class="price-card">
                <h3>Video Saja</h3>
                <div class="price-amount">Rp 500.000</div>
                <ul class="price-features">
                    <li>1 Videografer</li>
                    <li>Video Sinematik (Max 5 Menit)</li>
                    <li>Durasi Fleksibel</li>
                </ul>
                <a href="https://wa.me/6287765829615" target="_blank" class="btn-outline">Pilih Paket</a>
            </div>
            <div class="price-card premium">
                <h3>Komplit</h3>
                <div class="price-amount">Rp 850.000</div>
                <ul class="price-features">
                    <li>1 Fotografer & 1 Videografer</li>
                    <li>Full Edit Foto + Video Sinematik</li>
                    <li>Durasi Fleksibel</li>
                </ul>
                <a href="https://wa.me/6287765829615" target="_blank" class="btn-solid">Pilih Paket</a>
            </div>
        </div>

        <span class="section-tag" style="color: #fff; margin-bottom: 20px;">03. Paket Wisuda</span>
        <div class="price-grid">
            <div class="price-card">
                <h3>Basic</h3>
                <div class="price-amount">Rp 300.000</div>
                <ul class="price-features">
                    <li>1 Fotografer (Max 2 Jam)</li>
                    <li>Free Editing Semua Foto</li>
                    <li>Waktu ditentukan klien</li>
                </ul>
                <a href="https://wa.me/6287765829615" target="_blank" class="btn-outline">Pilih Paket</a>
            </div>
            <div class="price-card">
                <h3>Premium</h3>
                <div class="price-amount">Rp 500.000</div>
                <ul class="price-features">
                    <li>1-3 Fotografer (Max 5 Jam)</li>
                    <li>Free Editing Semua Foto</li>
                    <li>Waktu ditentukan klien</li>
                </ul>
                <a href="https://wa.me/6287765829615" target="_blank" class="btn-outline">Pilih Paket</a>
            </div>
            <div class="price-card premium">
                <h3>Pro</h3>
                <div class="price-amount">Rp 1.000.000</div>
                <ul class="price-features">
                    <li>Tim Foto & Video (Max 10 Jam)</li>
                    <li>Full Edit + Video Sinematik</li>
                    <li>Waktu ditentukan klien</li>
                </ul>
                <a href="https://wa.me/6287765829615" target="_blank" class="btn-solid">Pilih Paket</a>
            </div>
        </div>
    </section>

    <section id="page-about" class="page">
        <span class="section-tag">Studio Kami</span>
        <h2 class="section-title">Tentang Kami</h2>

        <div class="bento-card about-layout">
            <div class="founder-text">
                <h3>PT Another Visual</h3>
                <h4>Halo semua nya</h4>
                     <h4>Perkenal kan saya  Alif Nur Hidayat saya selaku Founder dari PT Another Visual</h4>
<p>Saya mewakili tim dan pendiri PT Another Visual ingin mengucapkan terima kasih sebesar-besarnya kepada seluruh klien, mitra, kru, dan semua pihak yang telah mempercayakan momen berharganya kepada kami.</p>
<p>Bagi kami, PT Another Visual bukan hanya tentang foto, video, atau produksi visual. Kami percaya setiap event punya cerita, setiap momen punya makna, dan tugas kami adalah mengabadikannya dengan cara terbaik agar bisa terus dikenang.</p>
<p>Perjalanan kami sampai hari ini tentunya tidak mudah. Namun berkat dukungan dan kepercayaan dari kalian semua, PT Another Visual terus berkembang menjadi tim kreatif yang selalu ingin memberikan hasil terbaik, profesional, dan penuh dedikasi.</p>
<p>Dari tahap pra-produksi hingga hasil akhir yang dapat dinikmati bersama, setiap proses dikerjakan dengan dedikasi penuh. Tanpa kerja sama, konsistensi, dan semangat solid dari tim, pencapaian ini mustahil terwujud.</p>
<p>Semoga ke depannya PT Another Visual bisa terus hadir, berkarya, dan menjadi bagian dari lebih banyak cerita luar biasa lainnya. Terima kasih sudah menjadi bagian dari perjalanan kami.</p>
<p>Salam hangat,<br><strong>Alif Nur Hidayat</strong><br>Pendiri PT Another Visual</p>
                <p style="margin-top: 30px; font-weight: 600; color: #fff;">Salam hangat,<br><span style="color: var(--text-muted); font-weight: 400;">Alif Nur Hidayat — Founder PT Another Visual</span></p>
            </div>
            <div class="card-image" style="background-image: url('https://lh3.googleusercontent.com/d/1XCVRVaa9RkMXH04tVXUSDGJZN92wRSL9'); border-radius: var(--radius-md); background-size: cover; background-position: center; min-height: 300px;"></div>
    </section>

    <section id="page-contact" class="page">
        <span class="section-tag">Hubungi Kami</span>
        <h2 class="section-title">Mari Berkolaborasi.</h2>

        <div class="contact-grid">
            <div class="bento-card contact-card">
                <span class="section-tag">Pesan Langsung</span>
                <h4>WhatsApp</h4>
                <a href="https://wa.me/6287765829615" target="_blank">+62 877 6582 9615</a>
            </div>
            <div class="bento-card contact-card">
                <span class="section-tag">Keperluan Bisnis</span>
                <h4>Email</h4>
                <a href="mailto:anothervisualjakarta@gmail.com">anothervisualjakarta@gmail.com</a>
            </div>
            <div class="bento-card contact-card">
                <span class="section-tag">Sosial Media</span>
                <h4>Instagram</h4>
                <a href="https://instagram.com/another_visual.id" target="_blank">@another_visual.id</a>
            </div>
        </div>
    </section>

    <footer>
        <div class="footer-quote">"Kami tidak sekadar mengabadikan momen, kami merangkai memori abadi."</div>
        
        <div class="footer-socials">
            <a href="https://instagram.com/another_visual.id" class="social-icon-btn" target="_blank" aria-label="Instagram">
                <svg viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
            </a>
            <a href="https://wa.me/6287765829615" class="social-icon-btn" target="_blank" aria-label="WhatsApp">
                <svg viewBox="0 0 24 24"><path d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.245 2.248 3.481 5.236 3.48 8.414-.003 6.557-5.338 11.892-11.893 11.892-1.99-.001-3.951-.5-5.688-1.448l-6.305 1.654zm6.597-3.807c1.676.995 3.276 1.591 5.392 1.592 5.448 0 9.886-4.434 9.889-9.885.002-5.462-4.415-9.89-9.881-9.892-5.452 0-9.887 4.434-9.889 9.884-.001 2.225.651 3.891 1.746 5.634l-.999 3.648 3.742-.981zm11.387-5.464c-.074-.124-.272-.198-.57-.347-.297-.149-1.758-.868-2.031-.967-.272-.099-.47-.149-.669.149-.198.297-.768.967-.941 1.165-.173.198-.347.223-.644.074-.297-.149-1.255-.462-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.297-.347.446-.521.151-.172.2-.296.3-.495.099-.198.05-.372-.025-.521-.075-.148-.669-1.611-.916-2.206-.242-.579-.487-.501-.669-.51l-.57-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.065 2.876 1.213 3.074c.149.198 2.095 3.2 5.076 4.487.709.306 1.263.489 1.694.626.712.226 1.36.194 1.872.118.571-.085 1.758-.719 2.006-1.413.248-.695.248-1.29.173-1.414z"/></svg>
            </a>
            <a href="mailto:anothervisualjakarta@gmail.com" class="social-icon-btn" target="_blank" aria-label="Email">
                <svg viewBox="0 0 24 24"><path d="M12 12.713l-11.985-9.713h23.97l-11.985 9.713zm0 2.574l-12-9.728v15.441h24v-15.441l-12 9.728z"/></svg>
            </a>
        </div>

        <div class="copyright">© 2026 PT Another Visual. Berbasis di Jakarta.</div>
    </footer>

    <script>
        function navTo(pageId) {
            document.querySelectorAll('.page').forEach(sec => sec.classList.remove('active'));
            document.getElementById('page-' + pageId).classList.add('active');
            
            document.querySelectorAll('nav a').forEach(link => link.classList.remove('active'));
            document.getElementById('nav-' + pageId).classList.add('active');
            
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function filterItems(category) {
            document.querySelectorAll('.folder-btn').forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
            
            document.querySelectorAll('.port-item').forEach(item => {
                if (category === 'all' || item.classList.contains(category)) {
                    item.style.display = 'block';
                } else {
                    item.style.display = 'none';
                }
            });
        }

        let currentImages = [];
        let currentIndex = 0;
        let currentClientName = "";

        function openSlider(imagesArray, clientName) {
            currentImages = imagesArray;
            currentIndex = 0;
            currentClientName = clientName;
            
            updateModalContent();
            document.getElementById('imageModal').style.display = "flex";
        }

        function closeModal() {
            document.getElementById('imageModal').style.display = "none";
        }

        function changeSlide(direction) {
            currentIndex += direction;
            if (currentIndex >= currentImages.length) currentIndex = 0;
            if (currentIndex < 0) currentIndex = currentImages.length - 1;
            updateModalContent();
        }

        function updateModalContent() {
            document.getElementById('modalImgSrc').src = currentImages[currentIndex];
            document.getElementById('clientNameText').innerText = currentClientName + ` (${currentIndex + 1} dari ${currentImages.length})`;
        }

        document.getElementById('imageModal').addEventListener('click', function(e) {
            if (e.target === this) closeModal();
        });
    </script>
</body>
</html>
