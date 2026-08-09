<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">

    <meta name="viewport"
          content="width=device-width, initial-scale=1.0, viewport-fit=cover">

    <meta name="theme-color" content="#0a0a0a">
    <meta name="description"
          content="PT Another Visual - Photography, Videography & Visual Production">

    <title>PT Another Visual</title>

    <style>
        /* =========================================================
           RESET
        ========================================================= */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            scroll-padding-top: 80px;
        }

        body {
            font-family:
                Inter,
                -apple-system,
                BlinkMacSystemFont,
                "Segoe UI",
                sans-serif;

            background: #080808;
            color: #fff;
            line-height: 1.6;
            overflow-x: hidden;

            -webkit-user-select: none;
            user-select: none;
        }

        body.no-scroll {
            overflow: hidden;
        }

        img {
            max-width: 100%;
            display: block;

            -webkit-user-drag: none;
            user-drag: none;

            user-select: none;
            -webkit-user-select: none;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        button {
            font: inherit;
        }

        /* =========================================================
           VARIABLES
        ========================================================= */

        :root {
            --bg: #080808;
            --bg-soft: #101010;
            --card: #121212;
            --card-hover: #181818;

            --white: #ffffff;
            --text: #f5f5f5;
            --text-muted: #929292;

            --border: rgba(255, 255, 255, 0.10);
            --border-hover: rgba(255, 255, 255, 0.25);

            --accent: #ffffff;

            --radius-sm: 12px;
            --radius-md: 20px;
            --radius-lg: 28px;

            --container: 1180px;

            --shadow:
                0 20px 60px rgba(0, 0, 0, 0.35);
        }

        /* =========================================================
           DEVICE INDICATOR
        ========================================================= */

        body::before {
            content: "";
            display: none;
        }

        body.device-mobile::before {
            content: "Mobile";
        }

        body.device-tablet::before {
            content: "Tablet";
        }

        body.device-desktop::before {
            content: "Desktop";
        }

        /* =========================================================
           CONTAINER
        ========================================================= */

        .container {
            width: min(var(--container), calc(100% - 40px));
            margin: 0 auto;
        }

        /* =========================================================
           NAVBAR
        ========================================================= */

        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 72px;

            display: flex;
            align-items: center;

            z-index: 1000;

            background: rgba(8, 8, 8, 0.78);
            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);

            border-bottom: 1px solid var(--border);
        }

        .nav-inner {
            width: min(var(--container), calc(100% - 40px));
            margin: auto;

            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 30px;
        }

        .logo {
            font-size: 18px;
            font-weight: 800;
            letter-spacing: -0.5px;
            white-space: nowrap;
        }

        .logo span {
            color: var(--text-muted);
            font-weight: 400;
        }

        .nav-menu {
            display: flex;
            align-items: center;
            gap: 8px;
            list-style: none;
        }

        .nav-menu a {
            display: block;
            padding: 9px 14px;

            color: #aaa;
            font-size: 13px;
            font-weight: 600;

            border-radius: 999px;

            transition:
                color 0.2s ease,
                background 0.2s ease;
        }

        .nav-menu a:hover,
        .nav-menu a.active {
            color: #fff;
            background: rgba(255, 255, 255, 0.08);
        }

        .menu-toggle {
            display: none;

            width: 42px;
            height: 42px;

            border: 1px solid var(--border);
            border-radius: 12px;

            background: #111;
            color: #fff;

            cursor: pointer;
        }

        /* =========================================================
           HERO
        ========================================================= */

        .hero {
            min-height: 100vh;

            display: flex;
            align-items: center;

            padding:
                120px 0
                80px;

            position: relative;

            background:
                radial-gradient(
                    circle at 80% 20%,
                    rgba(255,255,255,0.08),
                    transparent 30%
                ),
                var(--bg);
        }

        .hero-content {
            max-width: 850px;
        }

        .hero-tag {
            display: inline-flex;
            align-items: center;

            padding: 7px 12px;

            border: 1px solid var(--border);
            border-radius: 999px;

            color: #aaa;

            font-size: 11px;
            font-weight: 700;
            letter-spacing: 1px;
            text-transform: uppercase;

            margin-bottom: 22px;
        }

        .hero h1 {
            font-size: clamp(48px, 8vw, 100px);
            line-height: 0.95;
            letter-spacing: -5px;

            margin-bottom: 28px;
        }

        .hero h1 span {
            color: #777;
        }

        .hero-description {
            max-width: 680px;

            color: var(--text-muted);
            font-size: 17px;
            line-height: 1.8;

            margin-bottom: 32px;
        }

        .hero-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;

            min-height: 48px;
            padding: 0 20px;

            border-radius: 999px;

            font-size: 13px;
            font-weight: 700;

            transition:
                transform 0.2s ease,
                background 0.2s ease;
        }

        .btn:hover {
            transform: translateY(-2px);
        }

        .btn-solid {
            background: #fff;
            color: #000;
        }

        .btn-outline {
            background: transparent;
            border: 1px solid var(--border);
            color: #fff;
        }

        /* =========================================================
           SECTION
        ========================================================= */

        section {
            padding: 100px 0;
        }

        .section-header {
            margin-bottom: 45px;
        }

        .section-tag {
            display: inline-block;

            color: #888;

            font-size: 11px;
            font-weight: 800;
            letter-spacing: 1.5px;
            text-transform: uppercase;

            margin-bottom: 12px;
        }

        .section-title {
            font-size: clamp(34px, 5vw, 58px);
            line-height: 1;
            letter-spacing: -2.5px;

            margin-bottom: 18px;
        }

        .section-description {
            max-width: 680px;

            color: var(--text-muted);
            font-size: 15px;
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
            background:
                linear-gradient(
                    145deg,
                    rgba(255,255,255,0.055),
                    rgba(255,255,255,0.018)
                );

            border: 1px solid var(--border);
            border-radius: var(--radius-md);

            padding: 32px;

            box-shadow: var(--shadow);

            transition:
                transform 0.3s ease,
                border-color 0.3s ease,
                background 0.3s ease;
        }

        .bento-card:hover {
            transform: translateY(-4px);
            border-color: var(--border-hover);
            background: var(--card-hover);
        }

        .bento-card h3 {
            font-size: 28px;
            line-height: 1.1;
            margin-bottom: 15px;
        }

        .bento-card p {
            color: var(--text-muted);
            font-size: 14px;
            line-height: 1.8;
        }

        /* =========================================================
           PORTFOLIO FILTER
        ========================================================= */

        .folder-nav {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;

            margin-bottom: 25px;
        }

        .folder-btn {
            padding: 10px 16px;

            border: 1px solid var(--border);
            border-radius: 999px;

            background: transparent;
            color: #888;

            cursor: pointer;

            font-size: 12px;
            font-weight: 700;

            transition:
                color 0.2s ease,
                background 0.2s ease,
                border-color 0.2s ease;
        }

        .folder-btn:hover,
        .folder-btn.active {
            background: #fff;
            border-color: #fff;
            color: #000;
        }

        /* =========================================================
           PORTFOLIO GRID
        ========================================================= */

        .masonry-grid {
            columns: 2 300px;
            column-gap: 18px;
        }

        .port-item {
            position: relative;

            width: 100%;

            margin-bottom: 18px;

            break-inside: avoid;

            overflow: hidden;

            border-radius: var(--radius-md);

            background: #111;

            border: 1px solid var(--border);

            cursor: pointer;

            transition:
                transform 0.3s ease,
                opacity 0.3s ease;
        }

        .port-item:hover {
            transform: translateY(-4px);
        }

        .port-item.hidden {
            display: none;
        }

        .port-item img {
            width: 100%;
            height: auto;

            object-fit: cover;

            transition:
                transform 0.5s ease,
                filter 0.5s ease;
        }

        .port-item:hover img {
            transform: scale(1.04);
            filter: brightness(0.72);
        }

        .port-overlay {
            position: absolute;
            left: 0;
            right: 0;
            bottom: 0;

            padding: 24px;

            background:
                linear-gradient(
                    transparent,
                    rgba(0,0,0,0.9)
                );

            pointer-events: none;
        }

        .port-cat {
            color: #aaa;

            font-size: 10px;
            font-weight: 800;
            letter-spacing: 1px;
            text-transform: uppercase;

            margin-bottom: 4px;
        }

        .port-title {
            color: #fff;

            font-size: 20px;
            font-weight: 700;
        }

        /* =========================================================
           PRICE LIST
        ========================================================= */

        .price-section-title {
            display: block;

            color: #fff;

            margin:
                50px 0 20px;

            font-size: 12px;
            font-weight: 800;
            letter-spacing: 1.5px;
            text-transform: uppercase;
        }

        .price-section-title:first-child {
            margin-top: 0;
        }

        .price-grid {
            display: grid;
            grid-template-columns:
                repeat(3, minmax(0, 1fr));

            gap: 18px;

            margin-bottom: 20px;
        }

        .price-card {
            position: relative;

            display: flex;
            flex-direction: column;

            min-height: 390px;

            padding: 30px;

            background: var(--card);

            border: 1px solid var(--border);
            border-radius: var(--radius-md);

            transition:
                transform 0.3s ease,
                border-color 0.3s ease;
        }

        .price-card:hover {
            transform: translateY(-5px);
            border-color: var(--border-hover);
        }

        .price-card.premium {
            background:
                linear-gradient(
                    145deg,
                    #202020,
                    #101010
                );

            border-color: rgba(255,255,255,0.3);
        }

        .price-card h3 {
            font-size: 22px;
            margin-bottom: 12px;
        }

        .price-amount {
            font-size: 30px;
            font-weight: 800;
            letter-spacing: -1px;

            margin-bottom: 25px;
        }

        .price-features {
            list-style: none;

            display: flex;
            flex-direction: column;

            gap: 12px;

            margin-bottom: 30px;
        }

        .price-features li {
            color: #aaa;

            font-size: 13px;

            padding-left: 20px;

            position: relative;
        }

        .price-features li::before {
            content: "✓";

            position: absolute;
            left: 0;

            color: #fff;
            font-weight: 800;
        }

        .price-card .btn-outline,
        .price-card .btn-solid {
            margin-top: auto;
            width: 100%;
        }

        /* =========================================================
           ABOUT
        ========================================================= */

        .about-layout {
            display: grid;

            grid-template-columns:
                minmax(0, 1.15fr)
                minmax(300px, 0.85fr);

            gap: 40px;

            align-items: stretch;
        }

        .founder-text h3 {
            font-size: 34px;
            line-height: 1.1;

            margin-bottom: 20px;
        }

        .founder-text h4 {
            color: #fff;

            font-size: 17px;
            line-height: 1.5;

            margin-bottom: 12px;
        }

        .founder-text p {
            color: var(--text-muted);

            font-size: 14px;
            line-height: 1.85;

            margin-bottom: 15px;
        }

        .card-image {
            width: 100%;
            min-height: 450px;

            border-radius: var(--radius-md);

            background-image:
                url('https://lh3.googleusercontent.com/d/1XCVRVaa9RkMXH04tVXUSDGJZN92wRSL9');

            background-size: cover;
            background-position: center;

            border: 1px solid var(--border);
        }

        /* =========================================================
           CONTACT
        ========================================================= */

        .contact-grid {
            display: grid;

            grid-template-columns:
                repeat(3, minmax(0, 1fr));

            gap: 18px;
        }

        .contact-card {
            display: block;

            cursor: pointer;

            min-height: 190px;

            transition:
                transform 0.25s ease,
                border-color 0.25s ease;
        }

        .contact-card:hover {
            transform: translateY(-5px);
            border-color: rgba(255,255,255,0.3);
        }

        .contact-card h4 {
            font-size: 22px;
            margin-bottom: 10px;
        }

        .contact-card a {
            display: inline-block;

            color: #aaa;

            font-size: 14px;

            word-break: break-word;

            transition: color 0.2s ease;
        }

        .contact-card:hover a {
            color: #fff;
        }

        /* =========================================================
           FOOTER
        ========================================================= */

        footer {
            padding: 45px 0;

            border-top: 1px solid var(--border);

            color: #666;

            font-size: 12px;
        }

        .footer-inner {
            display: flex;
            align-items: center;
            justify-content: space-between;

            gap: 20px;
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

            width: 100%;
            height: 100%;

            display: flex;
            align-items: center;
            justify-content: center;
        }

        .slider-image {
            max-width: min(90vw, 1200px);
            max-height: 84vh;

            width: auto;
            height: auto;

            object-fit: contain;

            border-radius: 8px;

            box-shadow:
                0 30px 100px rgba(0,0,0,0.7);

            pointer-events: none;

            -webkit-user-drag: none;
            user-select: none;
        }

        .slider-close,
        .slider-prev,
        .slider-next {
            position: fixed;

            z-index: 10;

            display: flex;
            align-items: center;
            justify-content: center;

            border: 1px solid rgba(255,255,255,0.18);

            background: rgba(20,20,20,0.75);
            color: #fff;

            cursor: pointer;

            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);

            transition:
                background 0.2s ease,
                transform 0.2s ease;
        }

        .slider-close:hover,
        .slider-prev:hover,
        .slider-next:hover {
            background: #fff;
            color: #000;
        }

        .slider-close {
            top: 20px;
            right: 20px;

            width: 46px;
            height: 46px;

            border-radius: 50%;

            font-size: 25px;
        }

        .slider-prev,
        .slider-next {
            top: 50%;
            transform: translateY(-50%);

            width: 50px;
            height: 50px;

            border-radius: 50%;

            font-size: 22px;
        }

        .slider-prev {
            left: 25px;
        }

        .slider-next {
            right: 25px;
        }

        .slider-counter {
            position: fixed;

            left: 50%;
            bottom: 25px;

            transform: translateX(-50%);

            color: #aaa;

            padding: 7px 13px;

            background: rgba(20,20,20,0.8);

            border: 1px solid rgba(255,255,255,0.1);

            border-radius: 999px;

            font-size: 12px;
        }

        .slider-title {
            position: fixed;

            top: 25px;
            left: 50%;

            transform: translateX(-50%);

            max-width: 60%;

            color: #aaa;

            font-size: 12px;
            font-weight: 700;

            text-align: center;

            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        /* =========================================================
           MOBILE
        ========================================================= */

        @media (max-width: 900px) {

            .container,
            .nav-inner {
                width: min(
                    var(--container),
                    calc(100% - 30px)
                );
            }

            .nav-menu {
                position: fixed;

                top: 72px;
                left: 15px;
                right: 15px;

                display: none;
                flex-direction: column;

                padding: 10px;

                background: rgba(15,15,15,0.97);

                border: 1px solid var(--border);
                border-radius: 18px;

                box-shadow: var(--shadow);
            }

            .nav-menu.open {
                display: flex;
            }

            .nav-menu li,
            .nav-menu a {
                width: 100%;
            }

            .nav-menu a {
                padding: 13px 15px;
            }

            .menu-toggle {
                display: block;
            }

            .bento-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .price-grid {
                grid-template-columns:
                    repeat(2, minmax(0, 1fr));
            }

            .about-layout {
                grid-template-columns: 1fr;
            }

            .card-image {
                min-height: 420px;
                order: 2;
            }
        }

        @media (max-width: 600px) {

            html {
                scroll-padding-top: 70px;
            }

            .navbar {
                height: 64px;
            }

            .nav-menu {
                top: 64px;
            }

            .container,
            .nav-inner {
                width: calc(100% - 24px);
            }

            section {
                padding: 70px 0;
            }

            .hero {
                min-height: 90vh;

                padding:
                    100px 0
                    60px;
            }

            .hero h1 {
                font-size: clamp(46px, 15vw, 72px);
                letter-spacing: -3px;
            }

            .hero-description {
                font-size: 14px;
                line-height: 1.75;
            }

            .hero-buttons {
                display: grid;
                grid-template-columns: 1fr;
            }

            .btn {
                width: 100%;
            }

            .bento-card {
                padding: 24px;
            }

            .bento-card h3 {
                font-size: 24px;
            }

            .masonry-grid {
                columns: 1;
            }

            .folder-nav {
                flex-wrap: nowrap;

                overflow-x: auto;

                padding-bottom: 5px;

                scrollbar-width: none;
            }

            .folder-nav::-webkit-scrollbar {
                display: none;
            }

            .folder-btn {
                flex: 0 0 auto;
            }

            .price-grid {
                grid-template-columns: 1fr;
            }

            .price-card {
                min-height: auto;
            }

            .about-layout {
                gap: 25px;
            }

            .card-image {
                min-height: 330px;
            }

            .founder-text h3 {
                font-size: 29px;
            }

            .contact-grid {
                gap: 12px;
            }

            .contact-card {
                min-height: 160px;
            }

            .footer-inner {
                flex-direction: column;
                align-items: flex-start;
            }

            .slider-prev,
            .slider-next {
                width: 42px;
                height: 42px;

                top: auto;
                bottom: 20px;

                transform: none;
            }

            .slider-prev {
                left: 20px;
            }

            .slider-next {
                right: 20px;
            }

            .slider-close {
                top: 15px;
                right: 15px;

                width: 42px;
                height: 42px;
            }

            .slider-image {
                max-width: 94vw;
                max-height: 76vh;
            }

            .slider-title {
                top: 20px;
                left: 75px;
                right: 75px;

                transform: none;

                max-width: none;
            }

            .slider-counter {
                bottom: 76px;
            }
        }

        /* =========================================================
           SMALL PHONE
        ========================================================= */

        @media (max-width: 380px) {

            .hero h1 {
                font-size: 43px;
            }

            .section-title {
                font-size: 32px;
            }

            .bento-card,
            .price-card {
                padding: 20px;
            }
        }

        /* =========================================================
           REDUCE MOTION
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
         NAVIGATION
    ========================================================= -->

    <header class="navbar">
        <div class="nav-inner">

            <a href="#home" class="logo">
                Another <span>Visual</span>
            </a>

            <button
                class="menu-toggle"
                id="menuToggle"
                type="button"
                aria-label="Buka menu"
                aria-expanded="false">
                ☰
            </button>

            <ul class="nav-menu" id="navMenu">
                <li>
                    <a href="#home" class="nav-link active">
                        Home
                    </a>
                </li>

                <li>
                    <a href="#portfolio" class="nav-link">
                        Portfolio
                    </a>
                </li>

                <li>
                    <a href="#harga" class="nav-link">
                        Pricelist
                    </a>
                </li>

                <li>
                    <a href="#tentang" class="nav-link">
                        Tentang Kami
                    </a>
                </li>

                <li>
                    <a href="#kontak" class="nav-link">
                        Kontak
                    </a>
                </li>
            </ul>

        </div>
    </header>


    <!-- =========================================================
         HOME
    ========================================================= -->

    <main>

        <section id="home" class="hero">

            <div class="container">

                <div class="hero-content">

                    <div class="hero-tag">
                        PT Another Visual
                    </div>

                    <h1>
                        Visual yang
                        <span>bercerita.</span>
                    </h1>

                    <p class="hero-description">
                        Kami mengabadikan momen melalui fotografi,
                        videografi, dan produksi visual dengan pendekatan
                        kreatif, sinematik, dan penuh emosi.
                    </p>

                    <div class="hero-buttons">

                        <a
                            href="#portfolio"
                            class="btn btn-solid">
                            Lihat Portfolio
                        </a>

                        <a
                            href="#kontak"
                            class="btn btn-outline">
                            Hubungi Kami
                        </a>

                    </div>

                </div>

            </div>

        </section>


        <!-- =====================================================
             FILOSOFI
        ===================================================== -->

        <section id="filosofi">

            <div class="container">

                <div class="section-header">

                    <span class="section-tag">
                        Filosofi
                    </span>

                    <h2 class="section-title">
                        Cerita di balik<br>
                        setiap karya.
                    </h2>

                </div>

                <div class="bento-grid">

                    <div class="bento-card">

                        <span class="section-tag">
                            Filosofi Kami
                        </span>

                        <h3>
                            Estetika Tanpa Batas
                        </h3>

                        <p>
                            Kami percaya bahwa mahakarya visual tidak
                            ditentukan seberapa mahal alat yang digenggam,
                            melainkan bagaimana ketajaman mata seorang
                            kreator dalam merangkai cerita, komposisi,
                            dan emosi di setiap jepretan.
                        </p>

                    </div>


                    <div class="bento-card">

                        <span class="section-tag">
                            Visi Kami
                        </span>

                        <h3>
                            Karya yang Berbicara
                        </h3>

                        <p>
                            Visi utama kami adalah menghadirkan standar
                            visual tertinggi yang menyentuh hati. Melalui
                            teknik pencahayaan matang, sudut pandang
                            sinematik, dan sentuhan emosional, setiap momen
                            diabadikan bukan sekadar gambar, melainkan
                            sebuah mahakarya abadi.
                        </p>

                    </div>

                </div>

            </div>

        </section>


        <!-- =====================================================
             PORTFOLIO
        ===================================================== -->

        <section id="portfolio">

            <div class="container">

                <div class="section-header">

                    <span class="section-tag">
                        Portfolio
                    </span>

                    <h2 class="section-title">
                        Karya kami.
                    </h2>

                    <p class="section-description">
                        Pilih kategori untuk melihat dokumentasi
                        fotografi dan visual PT Another Visual.
                    </p>

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
                        onclick="openSlider(
                            [
                                'https://lh3.googleusercontent.com/d/1K5JYuw4FpqSI9NEduRvZNm_8eJRS_Mr2',
                                'https://lh3.googleusercontent.com/d/1sJJIfzNtLeDnY69v5Vw9it6EMWJzScWO',
                                'https://lh3.googleusercontent.com/d/18V0VTAzCCy9rw8Pkyy3jwVr06jbwqXjE',
                                'https://lh3.googleusercontent.com/d/18AiExWPI4x61GapsGDVEBAq6v3mhiUvw',
                                'https://lh3.googleusercontent.com/d/1jKrtiykv5AEAyyIixWZJIblm4kwSbvj3',
                                'https://lh3.googleusercontent.com/d/1VikQ2MtDl94PstxWeOPGFGZZBA76wRAJ',
                                'https://lh3.googleusercontent.com/d/18UYnUMDsVlxNF5CD3oRa7ShpY560WHPY',
                                'https://lh3.googleusercontent.com/d/12_urvrE4195fyQmf1RhEv3-ToTvxv6l5',
                                'https://lh3.googleusercontent.com/d/1ffcvFRZDPaoMzVLIgqm3GgDp83qRak6v'
                            ],
                            'Wedding Falaq & Cindy'
                        )">

                        <img
                            src="https://lh3.googleusercontent.com/d/1K5JYuw4FpqSI9NEduRvZNm_8eJRS_Mr2"
                            alt="Wedding Falaq & Cindy"
                            draggable="false">

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
                        onclick="openSlider(
                            [
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
                            ],
                            'Engagement Fikry & Reny'
                        )">

                        <img
                            src="https://lh3.googleusercontent.com/d/1CSJdaeY-POpOhoytFeI4PyPvCc6_43Jk"
                            alt="Engagement Fikry & Reny"
                            draggable="false">

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
                        onclick="openSlider(
                            [
                                'https://lh3.googleusercontent.com/d/1tdANeaA_DLSrfHtAXZQQEDzNckCwCl_u',
                                'https://lh3.googleusercontent.com/d/1ANX4TlyLrA2rg4es-1twvUenPk2xD8ha',
                                'https://lh3.googleusercontent.com/d/1L9HRUY0fNw6iAVpeb3TofmZWORZY82so',
                                'https://lh3.googleusercontent.com/d/1X4687Zb8Zos-tGLzKB44nmIBlZeBrR9_',
                                'https://lh3.googleusercontent.com/d/1CTqP6v3eLVrPBklcaRW7sttGg4_QwgCx',
                                'https://lh3.googleusercontent.com/d/1sPew-WXRoUgqJr-7rJXoqHli882oFJi1'
                            ],
                            'Wisuda Reny Riani'
                        )">

                        <img
                            src="https://lh3.googleusercontent.com/d/1tdANeaA_DLSrfHtAXZQQEDzNckCwCl_u"
                            alt="Wisuda Reny Riani"
                            draggable="false">

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
                        onclick="openSlider(
                            [
                                'https://lh3.googleusercontent.com/d/1_axQ1oATs8QwUrEDC56LEWqSs5cwa5LA',
                                'https://lh3.googleusercontent.com/d/1rLXnbHyq6fo_bcscrBcXqjiXNjQ9dcYN',
                                'https://lh3.googleusercontent.com/d/1zkjFPSBp0x4keMEPfFJv0tGuRjHae2GL',
                                'https://lh3.googleusercontent.com/d/1cWtB847VpSlCIG_KqRce9I6_5ql_TU5O',
                                'https://lh3.googleusercontent.com/d/1fT-R800YeD44qZNZnl-KKq6qPQkgs39p'
                            ],
                            'Corporate - Jalan Santai Kemerdekaan 2025'
                        )">

                        <img
                            src="https://lh3.googleusercontent.com/d/1_axQ1oATs8QwUrEDC56LEWqSs5cwa5LA"
                            alt="Corporate Event"
                            draggable="false">

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
        ===================================================== -->

        <section id="harga">

            <div class="container">

                <div class="section-header">

                    <span class="section-tag">
                        Pricelist
                    </span>

                    <h2 class="section-title">
                        Pilih paketmu.
                    </h2>

                </div>


                <!-- WEDDING -->

                <span class="section-tag price-section-title">
                    01. Paket Wedding
                </span>

                <div class="price-grid">

                    <div class="price-card">

                        <h3>Basic</h3>

                        <div class="price-amount">
                            Rp 850.000
                        </div>

                        <ul class="price-features">

                            <li>
                                1-2 Fotografer Profesional
                            </li>

                            <li>
                                Full Color Grading & Editing
                            </li>

                            <li>
                                Durasi Fleksibel (Mengikuti Klien)
                            </li>

                            <li>
                                Pengiriman via Google Drive
                            </li>

                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-outline btn">
                            Pilih Paket
                        </a>

                    </div>


                    <div class="price-card premium">

                        <h3>Premium</h3>

                        <div class="price-amount">
                            Rp 1.500.000
                        </div>

                        <ul class="price-features">

                            <li>
                                1 Fotografer & 1 Videografer
                            </li>

                            <li>
                                Edit Foto + Video Sinematik
                                (Max 5 Menit)
                            </li>

                            <li>
                                Durasi Fleksibel (Mengikuti Klien)
                            </li>

                            <li>
                                Pengiriman via Google Drive
                            </li>

                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-solid btn">
                            Pilih Paket
                        </a>

                    </div>

                </div>


                <!-- ENGAGEMENT -->

                <span class="section-tag price-section-title">
                    02. Paket Engagement
                </span>

                <div class="price-grid">

                    <div class="price-card">

                        <h3>Foto Saja</h3>

                        <div class="price-amount">
                            Rp 350.000
                        </div>

                        <ul class="price-features">

                            <li>
                                1-2 Fotografer
                            </li>

                            <li>
                                Full Editing Foto
                            </li>

                            <li>
                                Durasi Fleksibel
                            </li>

                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-outline btn">
                            Pilih Paket
                        </a>

                    </div>


                    <div class="price-card">

                        <h3>Video Saja</h3>

                        <div class="price-amount">
                            Rp 500.000
                        </div>

                        <ul class="price-features">

                            <li>
                                1 Videografer
                            </li>

                            <li>
                                Video Sinematik (Max 5 Menit)
                            </li>

                            <li>
                                Durasi Fleksibel
                            </li>

                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-outline btn">
                            Pilih Paket
                        </a>

                    </div>


                    <div class="price-card premium">

                        <h3>Komplit</h3>

                        <div class="price-amount">
                            Rp 850.000
                        </div>

                        <ul class="price-features">

                            <li>
                                1 Fotografer & 1 Videografer
                            </li>

                            <li>
                                Full Edit Foto + Video Sinematik
                            </li>

                            <li>
                                Durasi Fleksibel
                            </li>

                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-solid btn">
                            Pilih Paket
                        </a>

                    </div>

                </div>


                <!-- WISUDA -->

                <span class="section-tag price-section-title">
                    03. Paket Wisuda
                </span>

                <div class="price-grid">

                    <div class="price-card">

                        <h3>Basic</h3>

                        <div class="price-amount">
                            Rp 300.000
                        </div>

                        <ul class="price-features">

                            <li>
                                1 Fotografer (Max 2 Jam)
                            </li>

                            <li>
                                Free Editing Semua Foto
                            </li>

                            <li>
                                Waktu ditentukan klien
                            </li>

                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-outline btn">
                            Pilih Paket
                        </a>

                    </div>


                    <div class="price-card">

                        <h3>Premium</h3>

                        <div class="price-amount">
                            Rp 500.000
                        </div>

                        <ul class="price-features">

                            <li>
                                1-3 Fotografer (Max 5 Jam)
                            </li>

                            <li>
                                Free Editing Semua Foto
                            </li>

                            <li>
                                Waktu ditentukan klien
                            </li>

                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-outline btn">
                            Pilih Paket
                        </a>

                    </div>


                    <div class="price-card premium">

                        <h3>Pro</h3>

                        <div class="price-amount">
                            Rp 1.000.000
                        </div>

                        <ul class="price-features">

                            <li>
                                Tim Foto & Video (Max 10 Jam)
                            </li>

                            <li>
                                Full Edit + Video Sinematik
                            </li>

                            <li>
                                Waktu ditentukan klien
                            </li>

                        </ul>

                        <a
                            href="https://wa.me/6287765829615"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="btn-solid btn">
                            Pilih Paket
                        </a>

                    </div>

                </div>

            </div>

        </section>


        <!-- =====================================================
             TENTANG KAMI
        ===================================================== -->

        <section id="tentang">

            <div class="container">

                <div class="section-header">

                    <span class="section-tag">
                        Tentang Kami
                    </span>

                    <h2 class="section-title">
                        Di balik Another Visual.
                    </h2>

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
                            Perkenalkan saya Alif Nur Hidayat selaku
                            Founder dari PT Another Visual
                        </h4>

                        <p>
                            Saya mewakili tim dan pendiri PT Another Visual
                            ingin mengucapkan terima kasih sebesar-besarnya
                            kepada seluruh klien, mitra, kru, dan semua pihak
                            yang telah mempercayakan momen berharganya kepada
                            kami.
                        </p>

                        <p>
                            Bagi kami, PT Another Visual bukan hanya tentang
                            foto, video, atau produksi visual. Kami percaya
                            setiap event punya cerita, setiap momen punya
                            makna, dan tugas kami adalah mengabadikannya
                            dengan cara terbaik agar bisa terus dikenang.
                        </p>

                        <p>
                            Perjalanan kami sampai hari ini tentunya tidak
                            mudah. Namun berkat dukungan dan kepercayaan dari
                            kalian semua, PT Another Visual terus berkembang
                            menjadi tim kreatif yang selalu ingin memberikan
                            hasil terbaik, profesional, dan penuh dedikasi.
                        </p>

                        <p>
                            Dari tahap pra-produksi hingga hasil akhir yang
                            dapat dinikmati bersama, setiap proses dikerjakan
                            dengan dedikasi penuh. Tanpa kerja sama,
                            konsistensi, dan semangat solid dari tim,
                            pencapaian ini mustahil terwujud.
                        </p>

                        <p>
                            Semoga ke depannya PT Another Visual bisa terus
                            hadir, berkarya, dan menjadi bagian dari lebih
                            banyak cerita luar biasa lainnya. Terima kasih
                            sudah menjadi bagian dari perjalanan kami.
                        </p>

                        <p style="
                            margin-top: 30px;
                            font-weight: 600;
                            color: #fff;
                        ">
                            Salam hangat,<br>

                            <span style="
                                color: var(--text-muted);
                                font-weight: 400;
                            ">
                                Alif Nur Hidayat —
                                Founder PT Another Visual
                            </span>
                        </p>

                    </div>


                    <div
                        class="card-image"
                        aria-label="Foto Founder PT Another Visual">
                    </div>

                </div>

            </div>

        </section>


        <!-- =====================================================
             KONTAK
        ===================================================== -->

        <section id="kontak">

            <div class="container">

                <div class="section-header">

                    <span class="section-tag">
                        Kontak
                    </span>

                    <h2 class="section-title">
                        Mari bekerja sama.
                    </h2>

                    <p class="section-description">
                        Klik salah satu kontak di bawah untuk langsung
                        terhubung dengan PT Another Visual.
                    </p>

                </div>


                <div class="contact-grid">


                    <!-- WHATSAPP -->

                    <a
                        class="bento-card contact-card"
                        href="https://wa.me/6287765829615"
                        target="_blank"
                        rel="noopener noreferrer">

                        <span class="section-tag">
                            Pesan Langsung
                        </span>

                        <h4>
                            WhatsApp
                        </h4>

                        <span>
                            +62 877 6582 9615
                        </span>

                    </a>


                    <!-- EMAIL -->

                    <a
                        class="bento-card contact-card"
                        href="mailto:anothervisualjakarta@gmail.com">

                        <span class="section-tag">
                            Keperluan Bisnis
                        </span>

                        <h4>
                            Email
                        </h4>

                        <span>
                            anothervisualjakarta@gmail.com
                        </span>

                    </a>


                    <!-- INSTAGRAM -->

                    <a
                        class="bento-card contact-card"
                        href="https://instagram.com/another_visual.id"
                        target="_blank"
                        rel="noopener noreferrer">

                        <span class="section-tag">
                            Sosial Media
                        </span>

                        <h4>
                            Instagram
                        </h4>

                        <span>
                            @another_visual.id
                        </span>

                    </a>

                </div>

            </div>

        </section>

    </main>


    <!-- =========================================================
         FOOTER
    ========================================================= -->

    <footer>

        <div class="container">

            <div class="footer-inner">

                <div>
                    © <span id="year"></span>
                    PT Another Visual
                </div>

                <div>
                    Photography • Videography • Visual Production
                </div>

            </div>

        </div>

    </footer>


    <!-- =========================================================
         SLIDER
    ========================================================= -->

    <div
        class="slider-modal"
        id="sliderModal"
        aria-hidden="true">

        <div class="slider-content">

            <button
                class="slider-close"
                type="button"
                onclick="closeSlider()"
                aria-label="Tutup">
                ×
            </button>

            <div
                class="slider-title"
                id="sliderTitle">
            </div>

            <button
                class="slider-prev"
                type="button"
                onclick="previousSlide()"
                aria-label="Foto sebelumnya">
                ‹
            </button>

            <img
                id="sliderImage"
                class="slider-image"
                src=""
                alt=""
                draggable="false">

            <button
                class="slider-next"
                type="button"
                onclick="nextSlide()"
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
    ========================================================= -->

    <script>

        /* =====================================================
           YEAR
        ===================================================== */

        document.getElementById("year").textContent =
            new Date().getFullYear();


        /* =====================================================
           DEVICE DETECTION
        ===================================================== */

        function detectDevice() {

            const width = window.innerWidth;

            document.body.classList.remove(
                "device-mobile",
                "device-tablet",
                "device-desktop"
            );

            if (width <= 600) {

                document.body.classList.add(
                    "device-mobile"
                );

            } else if (width <= 1024) {

                document.body.classList.add(
                    "device-tablet"
                );

            } else {

                document.body.classList.add(
                    "device-desktop"
                );

            }
        }

        detectDevice();

        window.addEventListener(
            "resize",
            detectDevice
        );


        /* =====================================================
           MOBILE MENU
        ===================================================== */

        const menuToggle =
            document.getElementById("menuToggle");

        const navMenu =
            document.getElementById("navMenu");

        menuToggle.addEventListener(
            "click",
            function () {

                const isOpen =
                    navMenu.classList.toggle("open");

                menuToggle.setAttribute(
                    "aria-expanded",
                    isOpen ? "true" : "false"
                );

            }
        );


        document.querySelectorAll(".nav-link")
            .forEach(function (link) {

                link.addEventListener(
                    "click",
                    function () {

                        navMenu.classList.remove("open");

                        menuToggle.setAttribute(
                            "aria-expanded",
                            "false"
                        );

                    }
                );

            });


        /* =====================================================
           ACTIVE NAVIGATION
        ===================================================== */

        const sections =
            document.querySelectorAll("main section");

        const navLinks =
            document.querySelectorAll(".nav-link");

        const observer =
            new IntersectionObserver(
                function (entries) {

                    entries.forEach(
                        function (entry) {

                            if (entry.isIntersecting) {

                                navLinks.forEach(
                                    function (link) {

                                        link.classList.remove(
                                            "active"
                                        );

                                        if (
                                            link.getAttribute(
                                                "href"
                                            ) ===
                                            "#" + entry.target.id
                                        ) {

                                            link.classList.add(
                                                "active"
                                            );

                                        }

                                    }
                                );

                            }

                        }
                    );

                },
                {
                    rootMargin:
                        "-30% 0px -60% 0px"
                }
            );

        sections.forEach(
            function (section) {
                observer.observe(section);
            }
        );


        /* =====================================================
           PORTFOLIO FILTER
        ===================================================== */

        function filterItems(category) {

            const buttons =
                document.querySelectorAll(".folder-btn");

            const items =
                document.querySelectorAll(".port-item");

            buttons.forEach(
                function (button) {

                    button.classList.remove("active");

                    const buttonCategory =
                        button
                            .getAttribute("onclick")
                            .match(
                                /filterItems\('([^']+)'\)/
                            );

                    if (
                        buttonCategory &&
                        buttonCategory[1] === category
                    ) {

                        button.classList.add("active");

                    }

                }
            );


            items.forEach(
                function (item) {

                    if (
                        category === "all" ||
                        item.classList.contains(category)
                    ) {

                        item.classList.remove("hidden");

                    } else {

                        item.classList.add("hidden");

                    }

                }
            );

        }


        /* =====================================================
           SLIDER VARIABLES
        ===================================================== */

        let sliderImages = [];

        let sliderIndex = 0;

        let sliderName = "";

        const sliderModal =
            document.getElementById("sliderModal");

        const sliderImage =
            document.getElementById("sliderImage");

        const sliderTitle =
            document.getElementById("sliderTitle");

        const sliderCounter =
            document.getElementById("sliderCounter");


        /* =====================================================
           OPEN SLIDER
        ===================================================== */

        function openSlider(images, title) {

            if (
                !Array.isArray(images) ||
                images.length === 0
            ) {
                return;
            }

            sliderImages = images;

            sliderIndex = 0;

            sliderName = title || "";

            sliderModal.classList.add("active");

            sliderModal.setAttribute(
                "aria-hidden",
                "false"
            );

            document.body.classList.add(
                "no-scroll"
            );

            updateSlider();

        }


        /* =====================================================
           UPDATE SLIDER
        ===================================================== */

        function updateSlider() {

            if (!sliderImages.length) {
                return;
            }

            sliderImage.src =
                sliderImages[sliderIndex];

            sliderImage.alt =
                sliderName +
                " - Foto " +
                (sliderIndex + 1);

            sliderTitle.textContent =
                sliderName;

            sliderCounter.textContent =
                (sliderIndex + 1) +
                " / " +
                sliderImages.length;

        }


        /* =====================================================
           NEXT
        ===================================================== */

        function nextSlide() {

            if (!sliderImages.length) {
                return;
            }

            sliderIndex =
                (sliderIndex + 1) %
                sliderImages.length;

            updateSlider();

        }


        /* =====================================================
           PREVIOUS
        ===================================================== */

        function previousSlide() {

            if (!sliderImages.length) {
                return;
            }

            sliderIndex =
                (
                    sliderIndex -
                    1 +
                    sliderImages.length
                ) %
                sliderImages.length;

            updateSlider();

        }


        /* =====================================================
           CLOSE
        ===================================================== */

        function closeSlider() {

            sliderModal.classList.remove(
                "active"
            );

            sliderModal.setAttribute(
                "aria-hidden",
                "true"
            );

            document.body.classList.remove(
                "no-scroll"
            );

            sliderImage.src = "";

        }


        /* =====================================================
           KEYBOARD CONTROL
        ===================================================== */

        document.addEventListener(
            "keydown",
            function (event) {

                if (
                    !sliderModal.classList.contains(
                        "active"
                    )
                ) {
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

            }
        );


        /* =====================================================
           CLICK BACKDROP TO CLOSE
        ===================================================== */

        sliderModal.addEventListener(
            "click",
            function (event) {

                if (
                    event.target === sliderModal ||
                    event.target.classList.contains(
                        "slider-content"
                    )
                ) {

                    closeSlider();

                }

            }
        );


        /* =====================================================
           SWIPE SUPPORT - HP
        ===================================================== */

        let touchStartX = 0;
        let touchStartY = 0;

        sliderModal.addEventListener(
            "touchstart",
            function (event) {

                if (!event.touches.length) {
                    return;
                }

                touchStartX =
                    event.touches[0].clientX;

                touchStartY =
                    event.touches[0].clientY;

            },
            {
                passive: true
            }
        );


        sliderModal.addEventListener(
            "touchend",
            function (event) {

                if (!event.changedTouches.length) {
                    return;
                }

                const touchEndX =
                    event.changedTouches[0].clientX;

                const touchEndY =
                    event.changedTouches[0].clientY;

                const diffX =
                    touchEndX - touchStartX;

                const diffY =
                    touchEndY - touchStartY;


                /* Hanya dianggap swipe
                   kalau gerakan horizontal
                   lebih besar dari vertikal */

                if (
                    Math.abs(diffX) > 50 &&
                    Math.abs(diffX) >
                    Math.abs(diffY)
                ) {

                    if (diffX < 0) {

                        nextSlide();

                    } else {

                        previousSlide();

                    }

                }

            },
            {
                passive: true
            }
        );


        /* =====================================================
           PREVENT IMAGE DRAG
        ===================================================== */

        document.addEventListener(
            "dragstart",
            function (event) {

                if (
                    event.target.tagName === "IMG"
                ) {

                    event.preventDefault();

                }

            }
        );


        /* =====================================================
           PREVENT RIGHT CLICK
        ===================================================== */

        document.addEventListener(
            "contextmenu",
            function (event) {

                if (
                    event.target.tagName === "IMG" ||
                    event.target.closest(".card-image") ||
                    event.target.closest(".port-item")
                ) {

                    event.preventDefault();

                }

            }
        );


        /* =====================================================
           PREVENT COPY ON IMAGES
        ===================================================== */

        document.addEventListener(
            "copy",
            function (event) {

                if (
                    window.getSelection &&
                    window.getSelection().anchorNode
                ) {

                    const node =
                        window.getSelection().anchorNode;

                    if (
                        node &&
                        node.parentElement &&
                        (
                            node.parentElement.closest(
                                ".port-item"
                            ) ||
                            node.parentElement.closest(
                                ".card-image"
                            )
                        )
                    ) {

                        event.preventDefault();

                    }

                }

            }
        );


        /* =====================================================
           PREVENT LONG PRESS IMAGE
        ===================================================== */

        document.querySelectorAll("img")
            .forEach(
                function (image) {

                    image.setAttribute(
                        "draggable",
                        "false"
                    );

                    image.addEventListener(
                        "mousedown",
                        function (event) {

                            if (event.button === 2) {
                                event.preventDefault();
                            }

                        }
                    );

                }
            );

    </script>

</body>
</html>
