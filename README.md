<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <meta name="description" content="PT Another Visual - Photography, Videography, Wedding, Engagement, Wisuda dan Event">
    <meta name="theme-color" content="#0a0a0a">

    <title>PT Another Visual</title>

    <style>
        /* =========================================================
           RESET & DASAR
        ========================================================= */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            -webkit-text-size-adjust: 100%;
        }

        body {
            margin: 0;
            padding: 0;
            background: #080808;
            color: #fff;
            font-family: Arial, Helvetica, sans-serif;
            line-height: 1.6;
            overflow-x: hidden;
        }

        img {
            display: block;
            max-width: 100%;
        }

        button,
        a {
            font: inherit;
        }

        button {
            border: 0;
            cursor: pointer;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        :root {
            --bg: #080808;
            --bg-soft: #101010;
            --card: #141414;
            --card-hover: #1a1a1a;
            --border: rgba(255, 255, 255, 0.10);
            --border-hover: rgba(255, 255, 255, 0.22);
            --text: #ffffff;
            --text-muted: #a7a7a7;
            --accent: #ffffff;
            --radius: 20px;
            --radius-md: 14px;
            --max-width: 1200px;
        }

        .container {
            width: min(100% - 40px, var(--max-width));
            margin: 0 auto;
        }

        /* =========================================================
           HEADER
        ========================================================= */

        header {
            position: sticky;
            top: 0;
            z-index: 1000;
            width: 100%;
            background: rgba(8, 8, 8, 0.88);
            border-bottom: 1px solid var(--border);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
        }

        .navbar {
            min-height: 74px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 25px;
        }

        .logo {
            font-size: 20px;
            font-weight: 800;
            letter-spacing: 1px;
            white-space: nowrap;
        }

        .logo span {
            color: #888;
        }

        .nav-menu {
            display: flex;
            align-items: center;
            gap: 28px;
            list-style: none;
        }

        .nav-menu a {
            color: #aaa;
            font-size: 14px;
            transition: color 0.25s ease;
        }

        .nav-menu a:hover {
            color: #fff;
        }

        /* =========================================================
           HERO
        ========================================================= */

        .hero {
            min-height: 85vh;
            display: flex;
            align-items: center;
            padding: 100px 0;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;
            width: 500px;
            height: 500px;
            right: -180px;
            top: -180px;
            background: rgba(255,255,255,0.04);
            border-radius: 50%;
            filter: blur(20px);
            pointer-events: none;
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 850px;
        }

        .hero-tag {
            display: inline-block;
            margin-bottom: 22px;
            color: #999;
            font-size: 12px;
            font-weight: 700;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        .hero h1 {
            font-size: clamp(42px, 7vw, 92px);
            line-height: 0.98;
            letter-spacing: -4px;
            margin-bottom: 30px;
        }

        .hero h1 span {
            color: #777;
        }

        .hero p {
            max-width: 680px;
            color: var(--text-muted);
            font-size: clamp(15px, 2vw, 18px);
            line-height: 1.8;
        }

        .hero-actions {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 32px;
        }

        .btn-solid,
        .btn-outline {
            display: inline-flex;
            justify-content: center;
            align-items: center;
            min-height: 48px;
            padding: 12px 22px;
            border-radius: 999px;
            transition: all 0.25s ease;
            font-weight: 700;
            font-size: 14px;
        }

        .btn-solid {
            color: #000;
            background: #fff;
        }

        .btn-solid:hover {
            background: #ddd;
            transform: translateY(-2px);
        }

        .btn-outline {
            color: #fff;
            border: 1px solid var(--border-hover);
            background: transparent;
        }

        .btn-outline:hover {
            background: #fff;
            color: #000;
        }

        /* =========================================================
           SECTION
        ========================================================= */

        section {
            padding: 90px 0;
            scroll-margin-top: 80px;
        }

        .section-head {
            margin-bottom: 35px;
        }

        .section-tag {
            display: inline-block;
            margin-bottom: 12px;
            color: #999;
            font-size: 11px;
            font-weight: 800;
            letter-spacing: 1.8px;
            text-transform: uppercase;
        }

        .section-head h2 {
            font-size: clamp(30px, 5vw, 54px);
            line-height: 1.1;
            letter-spacing: -2px;
        }

        .section-head p {
            max-width: 650px;
            margin-top: 15px;
            color: var(--text-muted);
        }

        /* =========================================================
           BENTO
        ========================================================= */

        .bento-grid {
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            gap: 18px;
        }

        .bento-card {
            padding: 32px;
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: var(--radius);
            transition: transform 0.25s ease, border-color 0.25s ease;
        }

        .bento-card:hover {
            transform: translateY(-3px);
            border-color: var(--border-hover);
        }

        .bento-card h3 {
            margin-bottom: 14px;
            font-size: clamp(24px, 3vw, 34px);
        }

        .bento-card p {
            color: var(--text-muted);
            line-height: 1.8;
        }

        /* =========================================================
           PORTFOLIO FILTER
        ========================================================= */

        .folder-nav {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-bottom: 28px;
        }

        .folder-btn {
            padding: 11px 18px;
            color: #999;
            background: #111;
            border: 1px solid var(--border);
            border-radius: 999px;
            transition: all 0.25s ease;
        }

        .folder-btn:hover,
        .folder-btn.active {
            color: #000;
            background: #fff;
            border-color: #fff;
        }

        /* =========================================================
           MASONRY PORTFOLIO
        ========================================================= */

        .masonry-grid {
            columns: 4 260px;
            column-gap: 16px;
        }

        .port-item {
            position: relative;
            display: inline-block;
            width: 100%;
            margin-bottom: 16px;
            overflow: hidden;
            border-radius: 16px;
            background: #111;
            cursor: pointer;
            break-inside: avoid;
            -webkit-column-break-inside: avoid;
        }

        .port-item img {
            width: 100%;
            height: auto;
            min-height: 220px;
            object-fit: cover;
            transition: transform 0.45s ease;
        }

        .port-item:hover img {
            transform: scale(1.04);
        }

        .port-overlay {
            position: absolute;
            inset: auto 0 0 0;
            padding: 60px 18px 18px;
            background: linear-gradient(
                to top,
                rgba(0,0,0,0.88),
                rgba(0,0,0,0)
            );
            pointer-events: none;
        }

        .port-cat {
            color: #aaa;
            font-size: 11px;
            font-weight: 700;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        .port-title {
            margin-top: 4px;
            color: #fff;
            font-size: 18px;
            font-weight: 700;
        }

        .port-item.hidden {
            display: none;
        }

        /* =========================================================
           PRICELIST
        ========================================================= */

        .price-section {
            background: #0d0d0d;
        }

        .price-title {
            color: #fff !important;
            margin-top: 35px;
            margin-bottom: 20px;
        }

        .price-grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(0, 1fr));
            gap: 18px;
            margin-bottom: 40px;
        }

        .price-card {
            display: flex;
            flex-direction: column;
            padding: 30px;
            min-height: 100%;
            background: #121212;
            border: 1px solid var(--border);
            border-radius: var(--radius);
        }

        .price-card.premium {
            border-color: rgba(255,255,255,0.35);
            background: linear-gradient(
                145deg,
                #191919,
                #101010
            );
        }

        .price-card h3 {
            font-size: 23px;
            margin-bottom: 10px;
        }

        .price-amount {
            margin-bottom: 24px;
            font-size: 30px;
            font-weight: 800;
            letter-spacing: -1px;
        }

        .price-features {
            flex: 1;
            padding-left: 20px;
            margin-bottom: 28px;
            color: var(--text-muted);
        }

        .price-features li {
            margin-bottom: 10px;
        }

        .price-card .btn-solid,
        .price-card .btn-outline {
            width: 100%;
        }

        /* =========================================================
           ABOUT
        ========================================================= */

        .about-layout {
            display: grid;
            grid-template-columns: 1.3fr 0.7fr;
            gap: 30px;
            align-items: stretch;
        }

        .founder-text h3 {
            margin-bottom: 18px;
            font-size: clamp(28px, 4vw, 42px);
        }

        .founder-text h4 {
            margin-bottom: 10px;
            font-size: 18px;
        }

        .founder-text p {
            margin-bottom: 16px;
            color: var(--text-muted);
        }

        .card-image {
            min-height: 400px;
            border-radius: var(--radius-md);
            background-size: cover;
            background-position: center;
        }

        /* =========================================================
           CONTACT
        ========================================================= */

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(0, 1fr));
            gap: 18px;
        }

        .contact-card h4 {
            margin-bottom: 10px;
            font-size: 22px;
        }

        .contact-card a {
            display: inline-block;
            color: #aaa;
            word-break: break-word;
            transition: color 0.2s ease;
        }

        .contact-card a:hover {
            color: #fff;
        }

        /* =========================================================
           FOOTER
        ========================================================= */

        footer {
            padding: 35px 0;
            border-top: 1px solid var(--border);
            color: #666;
            text-align: center;
            font-size: 13px;
        }

        /* =========================================================
           SLIDER / LIGHTBOX
        ========================================================= */

        .slider-modal {
            position: fixed;
            inset: 0;
            z-index: 9999;
            display: none;
            align-items: center;
            justify-content: center;
            padding: 20px;
            background: rgba(0,0,0,0.96);
            touch-action: none;
        }

        .slider-modal.active {
            display: flex;
        }

        .slider-content {
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            height: 100%;
        }

        .slider-image {
            max-width: calc(100vw - 150px);
            max-height: calc(100vh - 100px);
            width: auto;
            height: auto;
            object-fit: contain;
            border-radius: 8px;
            user-select: none;
            -webkit-user-drag: none;
            transition: opacity 0.2s ease;
        }

        .slider-btn {
            position: absolute;
            top: 50%;
            z-index: 2;
            display: flex;
            align-items: center;
            justify-content: center;
            width: 52px;
            height: 52px;
            border-radius: 50%;
            color: #fff;
            background: rgba(255,255,255,0.12);
            border: 1px solid rgba(255,255,255,0.18);
            transform: translateY(-50%);
            font-size: 25px;
            transition: all 0.2s ease;
        }

        .slider-btn:hover {
            background: #fff;
            color: #000;
        }

        .slider-prev {
            left: 25px;
        }

        .slider-next {
            right: 25px;
        }

        .slider-close {
            position: absolute;
            top: 20px;
            right: 25px;
            z-index: 3;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            color: #fff;
            background: rgba(255,255,255,0.12);
            border: 1px solid rgba(255,255,255,0.18);
            font-size: 25px;
        }

        .slider-counter {
            position: absolute;
            left: 50%;
            bottom: 22px;
            transform: translateX(-50%);
            color: #aaa;
            background: rgba(0,0,0,0.5);
            padding: 6px 13px;
            border-radius: 999px;
            font-size: 13px;
        }

        .slider-title {
            position: absolute;
            left: 50%;
            top: 25px;
            transform: translateX(-50%);
            max-width: 70%;
            color: #fff;
            text-align: center;
            font-size: 14px;
            font-weight: 700;
        }

        /* =========================================================
           RESPONSIVE TABLET
        ========================================================= */

        @media (max-width: 900px) {

            .nav-menu {
                gap: 15px;
            }

            .hero {
                min-height: 75vh;
                padding: 80px 0;
            }

            .bento-grid {
                grid-template-columns: 1fr;
            }

            .price-grid {
                grid-template-columns: repeat(2, minmax(0, 1fr));
            }

            .about-layout {
                grid-template-columns: 1fr;
            }

            .card-image {
                min-height: 350px;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }

            .masonry-grid {
                columns: 3 220px;
            }
        }

        /* =========================================================
           RESPONSIVE HP
        ========================================================= */

        @media (max-width: 600px) {

            .container {
                width: min(100% - 24px, var(--max-width));
            }

            header {
                position: sticky;
            }

            .navbar {
                min-height: 64px;
            }

            .logo {
                font-size: 16px;
            }

            .nav-menu {
                gap: 12px;
            }

            .nav-menu a {
                font-size: 11px;
            }

            .nav-menu li:nth-child(n+4) {
                display: none;
            }

            .hero {
                min-height: auto;
                padding: 80px 0 70px;
            }

            .hero h1 {
                letter-spacing: -2px;
                font-size: clamp(40px, 13vw, 64px);
            }

            .hero p {
                font-size: 14px;
                line-height: 1.7;
            }

            .hero-actions {
                display: grid;
                grid-template-columns: 1fr;
            }

            .hero-actions a {
                width: 100%;
            }

            section {
                padding: 65px 0;
            }

            .section-head {
                margin-bottom: 25px;
            }

            .section-head h2 {
                letter-spacing: -1px;
            }

            .bento-card {
                padding: 23px;
                border-radius: 16px;
            }

            .bento-card h3 {
                font-size: 25px;
            }

            .folder-nav {
                gap: 7px;
                overflow-x: auto;
                flex-wrap: nowrap;
                padding-bottom: 7px;
                scrollbar-width: none;
            }

            .folder-nav::-webkit-scrollbar {
                display: none;
            }

            .folder-btn {
                flex: 0 0 auto;
                padding: 9px 14px;
                font-size: 12px;
            }

            .masonry-grid {
                columns: 2 150px;
                column-gap: 9px;
            }

            .port-item {
                margin-bottom: 9px;
                border-radius: 11px;
            }

            .port-item img {
                min-height: 150px;
            }

            .port-overlay {
                padding: 45px 10px 10px;
            }

            .port-cat {
                font-size: 8px;
            }

            .port-title {
                font-size: 13px;
            }

            .price-grid {
                grid-template-columns: 1fr;
                gap: 13px;
            }

            .price-card {
                padding: 23px;
            }

            .price-amount {
                font-size: 26px;
            }

            .about-layout {
                gap: 18px;
            }

            .card-image {
                min-height: 280px;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }

            .contact-card {
                padding: 22px;
            }

            /* Slider HP */
            .slider-modal {
                padding: 10px;
            }

            .slider-image {
                max-width: calc(100vw - 20px);
                max-height: calc(100vh - 120px);
            }

            .slider-btn {
                width: 42px;
                height: 42px;
                font-size: 20px;
                background: rgba(255,255,255,0.15);
            }

            .slider-prev {
                left: 8px;
            }

            .slider-next {
                right: 8px;
            }

            .slider-close {
                top: 10px;
                right: 10px;
                width: 40px;
                height: 40px;
                font-size: 20px;
            }

            .slider-title {
                top: 15px;
                max-width: 55%;
                font-size: 12px;
            }

            .slider-counter {
                bottom: 12px;
                font-size: 11px;
            }
        }

        /* =========================================================
           HP SANGAT KECIL
        ========================================================= */

        @media (max-width: 380px) {

            .nav-menu a {
                font-size: 10px;
            }

            .masonry-grid {
                columns: 1;
            }

            .port-item img {
                min-height: 240px;
            }
        }

        /* =========================================================
           AKSESIBILITAS
        ========================================================= */

        @media (prefers-reduced-motion: reduce) {
            html {
                scroll-behavior: auto;
            }

            *,
            *::before,
            *::after {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
            }
        }
    </style>
</head>

<body>

    <!-- =========================================================
         HEADER
    ========================================================== -->

    <header>
        <div class="container navbar">

            <a href="#home" class="logo">
                ANOTHER<span>VISUAL</span>
            </a>

            <ul class="nav-menu">
                <li><a href="#about">Tentang</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#pricing">Pricelist</a></li>
                <li><a href="#contact">Kontak</a></li>
            </ul>

        </div>
    </header>


    <!-- =========================================================
         HERO
    ========================================================== -->

    <main>

        <section class="hero" id="home">
            <div class="container">
                <div class="hero-content">

                    <span class="hero-tag">
                        PT Another Visual
                    </span>

                    <h1>
                        Visual yang<br>
                        <span>bercerita.</span>
                    </h1>

                    <p>
                        Kami mengabadikan setiap momen melalui foto,
                        video, dan produksi visual dengan pendekatan
                        kreatif, sinematik, dan penuh emosi.
                    </p>

                    <div class="hero-actions">
                        <a href="#portfolio" class="btn-solid">
                            Lihat Portfolio
                        </a>

                        <a href="#contact" class="btn-outline">
                            Hubungi Kami
                        </a>
                    </div>

                </div>
            </div>
        </section>


        <!-- =====================================================
             FILOSOFI & VISI
        ====================================================== -->

        <section>
            <div class="container">

                <div class="section-head">
                    <span class="section-tag">01. Filosofi</span>
                    <h2>Identitas visual kami.</h2>
                </div>

                <div class="bento-grid">

                    <div class="bento-card">
                        <span class="section-tag">Filosofi Kami</span>

                        <h3>
                            Estetika Tanpa Batas
                        </h3>

                        <p>
                            Kami percaya bahwa mahakarya visual tidak ditentukan seberapa mahal alat yang digenggam, melainkan bagaimana ketajaman mata seorang kreator dalam merangkai cerita, komposisi, dan emosi di setiap jepretan.
                        </p>
                    </div>

                    <div class="bento-card">
                        <span class="section-tag">Visi Kami</span>

                        <h3>
                            Karya yang Berbicara
                        </h3>

                        <p>
                            Visi utama kami adalah menghadirkan standar visual tertinggi yang menyentuh hati. Melalui teknik pencahayaan matang, sudut pandang sinematik, dan sentuhan emosional, setiap momen diabadikan bukan sekadar gambar, melainkan sebuah mahakarya abadi.
                        </p>
                    </div>

                </div>

            </div>
        </section>


        <!-- =====================================================
             PORTFOLIO
        ====================================================== -->

        <section id="portfolio">

            <div class="container">

                <div class="section-head">
                    <span class="section-tag">02. Portfolio</span>
                    <h2>Beberapa karya kami.</h2>
                </div>

                <div class="folder-nav">

                    <button
                        class="folder-btn active"
                        onclick="filterItems('all')">
                        Semua Folder
                    </button>

                    <button
                        class="folder-btn"
                        onclick="filterItems('wedding')">
                        Wedding
                    </button>

                    <button
                        class="folder-btn"
                        onclick="filterItems('engagement')">
                        Engagement
                    </button>

                    <button
                        class="folder-btn"
                        onclick="filterItems('wisuda')">
                        Wisuda
                    </button>

                    <button
                        class="folder-btn"
                        onclick="filterItems('event')">
                        Event
                    </button>

                </div>


                <div class="masonry-grid">

                    <!-- WEDDING -->

                    <div
                        class="port-item wedding"
                        onclick="openSlider([
                            'https://lh3.googleusercontent.com/d/1K5JYuw4FpqSI9NEduRvZNm_8eJRS_Mr2',
                            'https://lh3.googleusercontent.com/d/1sJJIfzNtLeDnY69v5Vw9it6EMWJzScWO',
                            'https://lh3.googleusercontent.com/d/18V0VTAzCCy9rw8Pkyy3jwVr06jbwqXjE',
                            'https://lh3.googleusercontent.com/d/18AiExWPI4x61GapsGDVEBAq6v3mhiUvw',
                            'https://lh3.googleusercontent.com/d/1jKrtiykv5AEAyyIixWZJIblm4kwSbvj3',
                            'https://lh3.googleusercontent.com/d/1VikQ2MtDl94PstxWeOPGFGZZBA76wRAJ',
                            'https://lh3.googleusercontent.com/d/18UYnUMDsVlxNF5CD3oRa7ShpY560WHPY',
                            'https://lh3.googleusercontent.com/d/12_urvrE4195fyQmf1RhEv3-ToTvxv6l5',
                            'https://lh3.googleusercontent.com/d/1ffcvFRZDPaoMzVLIgqm3GgDp83qRak6v'
                        ], 'Wedding Falaq & Cindy')">

                        <img
                            src="https://lh3.googleusercontent.com/d/1K5JYuw4FpqSI9NEduRvZNm_8eJRS_Mr2"
                            alt="Wedding Falaq & Cindy"
                            loading="lazy">

                        <div class="port-overlay">
                            <div class="port-cat">
                                Wedding (9 Foto)
                            </div>

                            <div class="port-title">
                                Falaq & Cindy
                            </div>
                        </div>
                    </div>


                    <!-- ENGAGEMENT -->

                    <div
                        class="port-item engagement"
                        onclick="openSlider([
                            'https://lh3.googleusercontent.com/d/1CSJdaeY-POpOhoytFeI4PyPvCc6_43Jk',
                            'https://lh3.googleusercontent.com/d/1RZIXo9bAFTMbIv327LqCBZZys3No0Jop',
                            'https://lh3.googleusercontent.com/d/16RB0mGvb4YMqixSaT5ugndThBWce_IP4',
                            'https://lh3.googleusercontent.com/d/1pgDLZcUJxZ5fiGv4EadaWnQyigXkrLmc',
                            'https://lh3.googleusercontent.com/d/1ul39oBgor5kz0XAVGsM0vEPVOcfrKVv9',
                            'https://lh3.googleusercontent.com/d/1JLmj7thqafLvTXMTqGZXCLMx5mo1gtpm',
                            'https://lh3.googleusercontent.com/d/1aVgL_GPfg2adk_RN1UYLaL1vM1wkZ8iw',
                            'https://lh3.googleusercontent.com/d/1bl36KWAmRwiRCaqQicr1xZhBOc86RcwO',
                            'https://lh3.googleusercontent.com/d/17yN3ucaM5EtI46O7e8fGwdWyKxfylyCW',
                            'https://lh3.googleusercontent.com/d/1boUj5TLrYIWDkrcgW8AQsTghgnke36rk',
                            'https://lh3.googleusercontent.com/d/1UmCat8QQcEtkDr2KyzhM0yWys7l7LDkc',
                            'https://lh3.googleusercontent.com/d/19I127-vR7AFi6OKdj2vFYBLA6DJofGMU',
                            'https://lh3.googleusercontent.com/d/1Ui7W4zjre4TtivvXq2NDbsyw3gTqqIhC'
                        ], 'Engagement Fikry & Reny')">

                        <img
                            src="https://lh3.googleusercontent.com/d/1CSJdaeY-POpOhoytFeI4PyPvCc6_43Jk"
                            alt="Engagement Fikry & Reny"
                            loading="lazy">

                        <div class="port-overlay">
                            <div class="port-cat">
                                Engagement (13 Foto)
                            </div>

                            <div class="port-title">
                                Fikry & Reny
                            </div>
                        </div>
                    </div>


                    <!-- WISUDA -->

                    <div
                        class="port-item wisuda"
                        onclick="openSlider([
                            'https://lh3.googleusercontent.com/d/1tdANeaA_DLSrfHtAXZQQEDzNckCwCl_u',
                            'https://lh3.googleusercontent.com/d/1ANX4TlyLrA2rg4es-1twvUenPk2xD8ha',
                            'https://lh3.googleusercontent.com/d/1L9HRUY0fNw6iAVpeb3TofmZWORZY82so',
                            'https://lh3.googleusercontent.com/d/1X4687Zb8Zos-tGLzKB44nmIBlZeBrR9_',
                            'https://lh3.googleusercontent.com/d/1CTqP6v3eLVrPBklcaRW7sttGg4_QwgCx',
                            'https://lh3.googleusercontent.com/d/1sPew-WXRoUgqJr-7rJXoqHli882oFJi1'
                        ], 'Wisuda Reny Riani')">

                        <img
                            src="https://lh3.googleusercontent.com/d/1tdANeaA_DLSrfHtAXZQQEDzNckCwCl_u"
                            alt="Wisuda Reny Riani"
                            loading="lazy">

                        <div class="port-overlay">
                            <div class="port-cat">
                                Wisuda (6 Foto)
                            </div>

                            <div class="port-title">
                                Reny Riani
                            </div>
                        </div>
                    </div>


                    <!-- EVENT -->

                    <div
                        class="port-item event"
                        onclick="openSlider([
                            'https://lh3.googleusercontent.com/d/1_axQ1oATs8QwUrEDC56LEWqSs5cwa5LA',
                            'https://lh3.googleusercontent.com/d/1rLXnbHyq6fo_bcscrBcXqjiXNjQ9dcYN',
                            'https://lh3.googleusercontent.com/d/1zkjFPSBp0x4keMEPfFJv0tGuRjHae2GL',
                            'https://lh3.googleusercontent.com/d/1cWtB847VpSlCIG_KqRce9I6_5ql_TU5O',
                            'https://lh3.googleusercontent.com/d/1fT-R800YeD44qZNZnl-KKq6qPQkgs39p'
                        ], 'Corporate - Jalan Santai Kemerdekaan 2025')">

                        <img
                            src="https://lh3.googleusercontent.com/d/1_axQ1oATs8QwUrEDC56LEWqSs5cwa5LA"
                            alt="Corporate Event"
                            loading="lazy">

                        <div class="port-overlay">
                            <div class="port-cat">
                                Corporate Event (5 Foto)
                            </div>

                            <div class="port-title">
                                Jalan Santai 2025
                            </div>
                        </div>
                    </div>

                </div>

            </div>

        </section>


        <!-- =====================================================
             PRICELIST
        ====================================================== -->

        <section id="pricing" class="price-section">

            <div class="container">

                <div class="section-head">
                    <span class="section-tag">03. Pricelist</span>
                    <h2>Paket layanan.</h2>
                </div>


                <span class="section-tag price-title">
                    01. Paket Wedding
                </span>

                <div class="price-grid">

                    <div class="price-card">

                        <h3>Basic</h3>

                        <div class="price-amount">
                            Rp 850.000
                        </div>

                        <ul class="price-features">
                            <li>1-2 Fotografer Profesional</li>
                            <li>Full Color Grading & Editing</li>
                            <li>Durasi Fleksibel (Mengikuti Klien)</li>
                            <li>Pengiriman via Google Drive</li>
                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-outline">
                            Pilih Paket
                        </a>

                    </div>


                    <div class="price-card premium">

                        <h3>Premium</h3>

                        <div class="price-amount">
                            Rp 1.500.000
                        </div>

                        <ul class="price-features">
                            <li>1 Fotografer & 1 Videografer</li>
                            <li>Edit Foto + Video Sinematik (Max 5 Menit)</li>
                            <li>Durasi Fleksibel (Mengikuti Klien)</li>
                            <li>Pengiriman via Google Drive</li>
                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-solid">
                            Pilih Paket
                        </a>

                    </div>

                </div>


                <span class="section-tag price-title">
                    02. Paket Engagement
                </span>

                <div class="price-grid">

                    <div class="price-card">

                        <h3>Foto Saja</h3>

                        <div class="price-amount">
                            Rp 350.000
                        </div>

                        <ul class="price-features">
                            <li>1-2 Fotografer</li>
                            <li>Full Editing Foto</li>
                            <li>Durasi Fleksibel</li>
                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-outline">
                            Pilih Paket
                        </a>

                    </div>


                    <div class="price-card">

                        <h3>Video Saja</h3>

                        <div class="price-amount">
                            Rp 500.000
                        </div>

                        <ul class="price-features">
                            <li>1 Videografer</li>
                            <li>Video Sinematik (Max 5 Menit)</li>
                            <li>Durasi Fleksibel</li>
                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-outline">
                            Pilih Paket
                        </a>

                    </div>


                    <div class="price-card premium">

                        <h3>Komplit</h3>

                        <div class="price-amount">
                            Rp 850.000
                        </div>

                        <ul class="price-features">
                            <li>1 Fotografer & 1 Videografer</li>
                            <li>Full Edit Foto + Video Sinematik</li>
                            <li>Durasi Fleksibel</li>
                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-solid">
                            Pilih Paket
                        </a>

                    </div>

                </div>


                <span class="section-tag price-title">
                    03. Paket Wisuda
                </span>

                <div class="price-grid">

                    <div class="price-card">

                        <h3>Basic</h3>

                        <div class="price-amount">
                            Rp 300.000
                        </div>

                        <ul class="price-features">
                            <li>1 Fotografer (Max 2 Jam)</li>
                            <li>Free Editing Semua Foto</li>
                            <li>Waktu ditentukan klien</li>
                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-outline">
                            Pilih Paket
                        </a>

                    </div>


                    <div class="price-card">

                        <h3>Premium</h3>

                        <div class="price-amount">
                            Rp 500.000
                        </div>

                        <ul class="price-features">
                            <li>1-3 Fotografer (Max 5 Jam)</li>
                            <li>Free Editing Semua Foto</li>
                            <li>Waktu ditentukan klien</li>
                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-outline">
                            Pilih Paket
                        </a>

                    </div>


                    <div class="price-card premium">

                        <h3>Pro</h3>

                        <div class="price-amount">
                            Rp 1.000.000
                        </div>

                        <ul class="price-features">
                            <li>Tim Foto & Video (Max 10 Jam)</li>
                            <li>Full Edit + Video Sinematik</li>
                            <li>Waktu ditentukan klien</li>
                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-solid">
                            Pilih Paket
                        </a>

                    </div>

                </div>

            </div>

        </section>


        <!-- =====================================================
             ABOUT
        ====================================================== -->

        <section id="about">

            <div class="container">

                <div class="section-head">
                    <span class="section-tag">04. Tentang Kami</span>
                    <h2>Mengenal Another Visual.</h2>
                </div>


                <div class="bento-card about-layout">

                    <div class="founder-text">

                        <h3>
                            PT Another Visual
                        </h3>

                        <h4>
                            Halo semuanya
                        </h4>

                        <h4>
                            Perkenalkan saya Alif Nur Hidayat selaku Founder dari PT Another Visual
                        </h4>

                        <p>
                            Saya mewakili tim dan pendiri PT Another Visual ingin mengucapkan terima kasih sebesar-besarnya kepada seluruh klien, mitra, kru, dan semua pihak yang telah mempercayakan momen berharganya kepada kami.
                        </p>

                        <p>
                            Bagi kami, PT Another Visual bukan hanya tentang foto, video, atau produksi visual. Kami percaya setiap event punya cerita, setiap momen punya makna, dan tugas kami adalah mengabadikannya dengan cara terbaik agar bisa terus dikenang.
                        </p>

                        <p>
                            Perjalanan kami sampai hari ini tentunya tidak mudah. Namun berkat dukungan dan kepercayaan dari kalian semua, PT Another Visual terus berkembang menjadi tim kreatif yang selalu ingin memberikan hasil terbaik, profesional, dan penuh dedikasi.
                        </p>

                        <p>
                            Dari tahap pra-produksi hingga hasil akhir yang dapat dinikmati bersama, setiap proses dikerjakan dengan dedikasi penuh. Tanpa kerja sama, konsistensi, dan semangat solid dari tim, pencapaian ini mustahil terwujud.
                        </p>

                        <p>
                            Semoga ke depannya PT Another Visual bisa terus hadir, berkarya, dan menjadi bagian dari lebih banyak cerita luar biasa lainnya. Terima kasih sudah menjadi bagian dari perjalanan kami.
                        </p>

                        <p style="margin-top: 30px; font-weight: 600; color: #fff;">
                            Salam hangat,<br>
                            <span style="color: var(--text-muted); font-weight: 400;">
                                Alif Nur Hidayat — Founder PT Another Visual
                            </span>
                        </p>

                    </div>


                    <div
                        class="card-image"
                        style="
                            background-image: url('https://lh3.googleusercontent.com/d/1XCVRVaa9RkMXH04tVXUSDGJZN92wRSL9');
                        ">
                    </div>

                </div>

            </div>

        </section>


        <!-- =====================================================
             CONTACT
        ====================================================== -->

        <section id="contact">

            <div class="container">

                <div class="section-head">
                    <span class="section-tag">05. Kontak</span>
                    <h2>Mari buat sesuatu.</h2>
                </div>


                <div class="contact-grid">

                    <div class="bento-card contact-card">

                        <span class="section-tag">
                            Pesan Langsung
                        </span>

                        <h4>
                            WhatsApp
                        </h4>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer">
                            +62 877 6582 9615
                        </a>

                    </div>


                    <div class="bento-card contact-card">

                        <span class="section-tag">
                            Keperluan Bisnis
                        </span>

                        <h4>
                            Email
                        </h4>

                        <a href="mailto:anothervisualjakarta@gmail.com">
                            anothervisualjakarta@gmail.com
                        </a>

                    </div>


                    <div class="bento-card contact-card">

                        <span class="section-tag">
                            Sosial Media
                        </span>

                        <h4>
                            Instagram
                        </h4>

                        <a
                            href="https://instagram.com/another_visual.id"
                            target="_blank"
                            rel="noopener noreferrer">
                            @another_visual.id
                        </a>

                    </div>

                </div>

            </div>

        </section>

    </main>


    <!-- =========================================================
         FOOTER
    ========================================================== -->

    <footer>
        <div class="container">
            © <span id="currentYear"></span> PT Another Visual. All rights reserved.
        </div>
    </footer>


    <!-- =========================================================
         SLIDER
    ========================================================== -->

    <div
        class="slider-modal"
        id="sliderModal"
        aria-hidden="true">

        <div class="slider-content">

            <button
                class="slider-close"
                id="sliderClose"
                aria-label="Tutup">
                ×
            </button>

            <div
                class="slider-title"
                id="sliderTitle">
            </div>

            <button
                class="slider-btn slider-prev"
                id="sliderPrev"
                aria-label="Foto sebelumnya">
                ‹
            </button>

            <img
                class="slider-image"
                id="sliderImage"
                src=""
                alt="Portfolio">

            <button
                class="slider-btn slider-next"
                id="sliderNext"
                aria-label="Foto berikutnya">
                ›
            </button>

            <div
                class="slider-counter"
                id="sliderCounter">
                1 / 1
            </div>

        </div>

    </div>


    <!-- =========================================================
         JAVASCRIPT
    ========================================================== -->

    <script>

        /* =====================================================
           FILTER PORTFOLIO
        ====================================================== */

        function filterItems(category) {

            const items = document.querySelectorAll(".port-item");
            const buttons = document.querySelectorAll(".folder-btn");

            buttons.forEach(function(button) {
                button.classList.remove("active");
            });

            const clickedButton = Array.from(buttons).find(function(button) {
                return button.getAttribute("onclick") === "filterItems('" + category + "')";
            });

            if (clickedButton) {
                clickedButton.classList.add("active");
            }

            items.forEach(function(item) {

                if (category === "all") {
                    item.classList.remove("hidden");
                    return;
                }

                if (item.classList.contains(category)) {
                    item.classList.remove("hidden");
                } else {
                    item.classList.add("hidden");
                }

            });
        }


        /* =====================================================
           SLIDER
        ====================================================== */

        const sliderModal = document.getElementById("sliderModal");
        const sliderImage = document.getElementById("sliderImage");
        const sliderTitle = document.getElementById("sliderTitle");
        const sliderCounter = document.getElementById("sliderCounter");

        const sliderPrev = document.getElementById("sliderPrev");
        const sliderNext = document.getElementById("sliderNext");
        const sliderClose = document.getElementById("sliderClose");

        let sliderImages = [];
        let currentSlide = 0;

        let touchStartX = 0;
        let touchStartY = 0;
        let touchEndX = 0;
        let touchEndY = 0;


        function openSlider(images, title) {

            if (!Array.isArray(images) || images.length === 0) {
                return;
            }

            sliderImages = images;
            currentSlide = 0;

            sliderTitle.textContent = title || "";

            sliderModal.classList.add("active");
            sliderModal.setAttribute("aria-hidden", "false");

            document.body.style.overflow = "hidden";

            updateSlider();

        }


        function updateSlider() {

            if (!sliderImages.length) {
                return;
            }

            sliderImage.style.opacity = "0";

            const newImage = new Image();

            newImage.onload = function() {

                sliderImage.src = sliderImages[currentSlide];

                sliderImage.style.opacity = "1";

                sliderCounter.textContent =
                    (currentSlide + 1) + " / " + sliderImages.length;

            };

            newImage.onerror = function() {

                sliderImage.style.opacity = "1";

                sliderCounter.textContent =
                    "Gagal memuat foto " +
                    (currentSlide + 1) +
                    " / " +
                    sliderImages.length;

            };

            newImage.src = sliderImages[currentSlide];

            preloadNearbyImages();

        }


        function preloadNearbyImages() {

            if (!sliderImages.length) {
                return;
            }

            const nextIndex =
                (currentSlide + 1) % sliderImages.length;

            const previousIndex =
                (currentSlide - 1 + sliderImages.length) %
                sliderImages.length;

            const nextImage = new Image();
            nextImage.src = sliderImages[nextIndex];

            const previousImage = new Image();
            previousImage.src = sliderImages[previousIndex];

        }


        function nextSlide() {

            if (!sliderImages.length) {
                return;
            }

            currentSlide =
                (currentSlide + 1) % sliderImages.length;

            updateSlider();

        }


        function previousSlide() {

            if (!sliderImages.length) {
                return;
            }

            currentSlide =
                (currentSlide - 1 + sliderImages.length) %
                sliderImages.length;

            updateSlider();

        }


        function closeSlider() {

            sliderModal.classList.remove("active");
            sliderModal.setAttribute("aria-hidden", "true");

            sliderImage.src = "";

            document.body.style.overflow = "";

            sliderImages = [];
            currentSlide = 0;

        }


        /* =====================================================
           TOMBOL SLIDER
        ====================================================== */

        sliderNext.addEventListener("click", function(event) {

            event.stopPropagation();

            nextSlide();

        });


        sliderPrev.addEventListener("click", function(event) {

            event.stopPropagation();

            previousSlide();

        });


        sliderClose.addEventListener("click", function(event) {

            event.stopPropagation();

            closeSlider();

        });


        /* =====================================================
           KLIK AREA GELAP UNTUK MENUTUP
        ====================================================== */

        sliderModal.addEventListener("click", function(event) {

            if (event.target === sliderModal) {
                closeSlider();
            }

        });


        /* =====================================================
           KEYBOARD LAPTOP / DESKTOP
        ====================================================== */

        document.addEventListener("keydown", function(event) {

            if (!sliderModal.classList.contains("active")) {
                return;
            }

            if (event.key === "Escape") {
                closeSlider();
            }

            if (event.key === "ArrowRight") {
                nextSlide();
            }

            if (event.key === "ArrowLeft") {
                previousSlide();
            }

        });


        /* =====================================================
           SWIPE HP / TABLET
        ====================================================== */

        sliderModal.addEventListener("touchstart", function(event) {

            if (!event.changedTouches.length) {
                return;
            }

            touchStartX =
                event.changedTouches[0].screenX;

            touchStartY =
                event.changedTouches[0].screenY;

        }, {
            passive: true
        });


        sliderModal.addEventListener("touchend", function(event) {

            if (!event.changedTouches.length) {
                return;
            }

            touchEndX =
                event.changedTouches[0].screenX;

            touchEndY =
                event.changedTouches[0].screenY;

            handleSwipe();

        }, {
            passive: true
        });


        function handleSwipe() {

            const differenceX =
                touchEndX - touchStartX;

            const differenceY =
                touchEndY - touchStartY;

            const minimumSwipeDistance = 45;

            /*
             * Kalau gerakan vertikal lebih besar,
             * jangan dianggap sebagai swipe foto.
             */

            if (
                Math.abs(differenceY) >
                Math.abs(differenceX)
            ) {
                return;
            }

            if (
                Math.abs(differenceX) <
                minimumSwipeDistance
            ) {
                return;
            }

            if (differenceX < 0) {
                nextSlide();
            } else {
                previousSlide();
            }

        }


        /* =====================================================
           DOUBLE CLICK / ZOOM TIDAK MENGGANGGU SLIDER
        ====================================================== */

        sliderImage.addEventListener("dragstart", function(event) {
            event.preventDefault();
        });


        /* =====================================================
           TAHUN FOOTER
        ====================================================== */

        document.getElementById("currentYear").textContent =
            new Date().getFullYear();

    </script>

</body>
</html>
