
<html lang="id">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<meta name="description" content="Another Visual - Photography & Videography">
<meta name="theme-color" content="#0a0a0a">

<title>Another Visual — Photography & Videography</title>

<style>

    :root {
        --bg: #080808;
        --bg-soft: #111111;
        --card: #151515;
        --card-hover: #1b1b1b;
        --text: #ffffff;
        --text-muted: #a4a4a4;
        --border: rgba(255,255,255,.10);
        --accent: #ffffff;
        --radius: 18px;
        --max-width: 1200px;
    }

    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    html {
        scroll-behavior: smooth;
        scroll-padding-top: 90px;
    }

    body {
        font-family: Arial, Helvetica, sans-serif;
        background: var(--bg);
        color: var(--text);
        line-height: 1.7;
        overflow-x: hidden;
    }

    body.no-scroll {
        overflow: hidden;
    }

    img {
        max-width: 100%;
        display: block;
    }

    a {
        color: inherit;
        text-decoration: none;
    }

    button {
        font: inherit;
    }

    /* =========================
       DEVICE INFO
    ========================= */

    #deviceInfo {
        display: none;
    }

    /* =========================
       HEADER
    ========================= */

    .navbar {
        position: sticky;
        top: 0;
        z-index: 1000;
        width: 100%;
        background: rgba(8, 8, 8, .88);
        backdrop-filter: blur(18px);
        -webkit-backdrop-filter: blur(18px);
        border-bottom: 1px solid var(--border);
    }

    .nav-container {
        max-width: var(--max-width);
        min-height: 72px;
        margin: auto;
        padding: 0 24px;

        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 30px;
    }

    .logo {
        font-size: 20px;
        font-weight: 800;
        letter-spacing: -.5px;
        white-space: nowrap;
    }

    .logo span {
        color: var(--text-muted);
    }

    .nav-menu {
        display: flex;
        align-items: center;
        gap: 8px;
        list-style: none;
    }

    .nav-menu a {
        display: block;
        padding: 9px 13px;
        border-radius: 10px;
        color: var(--text-muted);
        font-size: 14px;
        transition: .25s ease;
    }

    .nav-menu a:hover,
    .nav-menu a.active {
        color: #fff;
        background: rgba(255,255,255,.08);
    }

    .menu-toggle {
        display: none;
        width: 42px;
        height: 42px;
        border: 1px solid var(--border);
        border-radius: 10px;
        background: #111;
        color: #fff;
        cursor: pointer;
    }

    /* =========================
       HERO - JAKARTA
    ========================= */

    .hero {
        position: relative;
        min-height: 82vh;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        padding: 90px 24px;

        background:
            linear-gradient(
                rgba(0,0,0,.68),
                rgba(0,0,0,.82)
            ),
            url("https://images.unsplash.com/photo-1555899434-94d1368aa7af?auto=format&fit=crop&w=2200&q=85")
            center center / cover no-repeat;

        overflow: hidden;
    }

    .hero::before {
        content: "";
        position: absolute;
        inset: 0;
        background:
            linear-gradient(
                to bottom,
                rgba(0,0,0,.15),
                rgba(0,0,0,.65)
            );
        pointer-events: none;
    }

    .hero-content {
        position: relative;
        z-index: 1;
        max-width: 900px;
    }

    .hero-tag {
        display: inline-block;
        margin-bottom: 20px;
        padding: 7px 13px;
        border: 1px solid rgba(255,255,255,.25);
        border-radius: 100px;
        color: #ddd;
        font-size: 12px;
        text-transform: uppercase;
        letter-spacing: 1.5px;
        background: rgba(0,0,0,.25);
        backdrop-filter: blur(8px);
    }

    .hero h1 {
        font-size: clamp(42px, 8vw, 92px);
        line-height: .95;
        letter-spacing: -4px;
        margin-bottom: 28px;
        text-shadow: 0 10px 35px rgba(0,0,0,.5);
    }

    .hero h1 span {
        color: #aaa;
    }

    .hero p {
        max-width: 680px;
        margin: auto;
        color: #ddd;
        font-size: 17px;
        text-shadow: 0 3px 15px rgba(0,0,0,.7);
    }

    .hero-buttons {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 12px;
        margin-top: 32px;
    }

    .btn {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        min-height: 46px;
        padding: 0 20px;
        border-radius: 10px;
        border: 1px solid var(--border);
        transition: .25s ease;
        cursor: pointer;
    }

    .btn-white {
        color: #000;
        background: #fff;
    }

    .btn-dark {
        color: #fff;
        background: #151515;
    }

    .btn:hover {
        transform: translateY(-2px);
    }

    /* =========================
       GENERAL SECTION
    ========================= */

    section {
        max-width: var(--max-width);
        margin: auto;
        padding: 90px 24px;
    }

    .section-header {
        margin-bottom: 35px;
    }

    .section-tag {
        display: inline-block;
        margin-bottom: 12px;
        color: var(--text-muted);
        font-size: 12px;
        font-weight: 700;
        letter-spacing: 1.5px;
        text-transform: uppercase;
    }

    .section-header h2 {
        font-size: clamp(32px, 5vw, 55px);
        line-height: 1.05;
        letter-spacing: -2px;
    }

    .section-header p {
        max-width: 650px;
        margin-top: 15px;
        color: var(--text-muted);
    }

    /* =========================
       BENTO
    ========================= */

    .bento-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 18px;
    }

    .bento-card {
        padding: 30px;
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--radius);
        transition: .3s ease;
    }

    .bento-card:hover {
        background: var(--card-hover);
        transform: translateY(-3px);
    }

    .bento-card h3 {
        font-size: 26px;
        margin-bottom: 15px;
    }

    .bento-card p {
        color: var(--text-muted);
    }

    /* =========================
       PORTFOLIO
    ========================= */

    .folder-nav {
        display: flex;
        gap: 8px;
        flex-wrap: wrap;
        margin-bottom: 25px;
    }

    .folder-btn {
        padding: 10px 16px;
        border-radius: 100px;
        border: 1px solid var(--border);
        background: #111;
        color: var(--text-muted);
        cursor: pointer;
        transition: .25s ease;
    }

    .folder-btn:hover,
    .folder-btn.active {
        background: #fff;
        color: #000;
        border-color: #fff;
    }

    .masonry-grid {
        columns: 3 280px;
        column-gap: 18px;
    }

    .port-item {
        position: relative;
        overflow: hidden;
        margin-bottom: 18px;
        border-radius: var(--radius);
        background: #111;
        cursor: pointer;
        break-inside: avoid;
        border: 1px solid var(--border);
    }

    .port-item img {
        width: 100%;
        height: auto;
        transition: transform .5s ease;
        user-select: none;
        -webkit-user-drag: none;
    }

    .port-item:hover img {
        transform: scale(1.04);
    }

    .port-overlay {
        position: absolute;
        inset: auto 0 0;
        padding: 50px 20px 20px;
        background: linear-gradient(
            transparent,
            rgba(0,0,0,.9)
        );
    }

    .port-cat {
        color: #bbb;
        font-size: 11px;
        text-transform: uppercase;
        letter-spacing: 1px;
    }

    .port-title {
        margin-top: 4px;
        font-size: 20px;
        font-weight: 700;
    }

    .port-item.hidden {
        display: none;
    }

    /* =========================
       PRICE
    ========================= */

    #pricelist {
        background: #050505;
    }

    #pricelist .price-card {
        background: linear-gradient(145deg, #181818 0%, #0d0d0d 100%);
        border: 1px solid #2a2a2a;
        border-radius: 8px;
        box-shadow: 0 12px 35px rgba(0,0,0,.35);
        position: relative;
        overflow: hidden;
        transition: transform .25s ease, border-color .25s ease, box-shadow .25s ease;
    }

    #pricelist .price-card::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        height: 4px;
        background: #e50914;
    }

    #pricelist .price-card:hover {
        transform: translateY(-5px);
        border-color: #e50914;
        box-shadow: 0 18px 45px rgba(229,9,20,.18);
    }

    #pricelist .price-card h3 {
        color: #fff;
    }

    #pricelist .price-amount {
        color: #fff;
    }

    #pricelist .price-features {
        color: #b3b3b3;
    }

    #pricelist .price-features li::marker {
        color: #e50914;
    }

    #pricelist .btn-outline {
        color: #fff;
        border-color: #555;
        background: #181818;
    }

    #pricelist .btn-outline:hover {
        background: #e50914;
        border-color: #e50914;
        color: #fff;
    }

    #pricelist .btn-solid {
        background: #e50914;
        border-color: #e50914;
        color: #fff;
    }

    #pricelist .btn-solid:hover {
        background: #f40612;
        border-color: #f40612;
    }

    #pricelist .price-card.premium {
        background: linear-gradient(145deg, #202020 0%, #0d0d0d 100%);
        color: #fff;
        border-color: #e50914;
    }

    #pricelist .price-card.premium .price-features {
        color: #d0d0d0;
    }

    #pricelist .price-card.premium .btn-solid {
        background: #e50914;
    }

    .price-section-title {
        display: block;
        margin: 55px 0 20px;
        color: #fff;
    }

    .price-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 18px;
    }

    .price-card {
        display: flex;
        flex-direction: column;
        padding: 30px;
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--radius);
    }

    .price-card.premium {
        background: #f4f4f4;
        color: #000;
    }

    .price-card h3 {
        font-size: 24px;
        margin-bottom: 10px;
    }

    .price-amount {
        margin-bottom: 25px;
        font-size: 29px;
        font-weight: 800;
    }

    .price-features {
        flex: 1;
        padding-left: 20px;
        color: var(--text-muted);
    }

    .premium .price-features {
        color: #555;
    }

    .price-features li {
        margin-bottom: 10px;
    }

    .btn-outline,
    .btn-solid {
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 45px;
        margin-top: 25px;
        border-radius: 9px;
        border: 1px solid var(--border);
        transition: .25s ease;
    }

    .btn-outline:hover {
        background: #fff;
        color: #000;
    }

    .btn-solid {
        background: #000;
        color: #fff;
        border-color: #000;
    }

    /* =========================
       ABOUT
    ========================= */

    .about-layout {
        display: grid;
        grid-template-columns: minmax(0, 1.1fr) minmax(300px, .9fr);
        gap: 35px;
        align-items: stretch;
    }

    .founder-text h3 {
        font-size: 35px;
        margin-bottom: 12px;
    }

    .founder-text h4 {
        margin-bottom: 12px;
    }

    .founder-text p {
        margin-bottom: 17px;
        color: var(--text-muted);
    }

    .founder-text .signature {
        margin-top: 30px;
        color: #fff;
        font-weight: 600;
    }

    .signature span {
        color: var(--text-muted);
        font-weight: 400;
    }

    .card-image {
        min-height: 450px;
        border-radius: var(--radius);
        background-size: cover;
        background-position: center;
    }

    /* =========================
       CONTACT
    ========================= */

    .contact-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 18px;
    }

    .contact-card {
        min-height: 210px;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .contact-card h4 {
        font-size: 24px;
        margin-bottom: 8px;
    }

    .contact-card a {
        color: var(--text-muted);
        word-break: break-word;
        transition: .2s ease;
    }

    .contact-card a:hover {
        color: #fff;
    }

    /* =========================
       SOCIAL MEDIA
    ========================= */

    .social-links {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 14px;
        margin: 28px 0 22px;
    }

    .social-link {
        width: 48px;
        height: 48px;
        display: flex;
        align-items: center;
        justify-content: center;

        border: 1px solid var(--border);
        border-radius: 50%;
        background: #111;
        color: #fff;

        transition: .25s ease;
    }

    .social-link:hover {
        background: #fff;
        color: #000;
        transform: translateY(-3px);
    }

    .social-link svg {
        width: 21px;
        height: 21px;
        fill: currentColor;
    }

    /* =========================
       FOOTER
    ========================= */

    footer {
        padding: 50px 24px;
        border-top: 1px solid var(--border);
        text-align: center;
        color: var(--text-muted);
        font-size: 13px;
    }

    /* =========================
       SLIDER
    ========================= */

    .slider-modal {
        position: fixed;
        inset: 0;
        z-index: 9999;
        display: none;
        align-items: center;
        justify-content: center;
        padding: 25px;
        background: rgba(0,0,0,.96);
    }

    .slider-modal.active {
        display: flex;
    }

    .slider-content {
        position: relative;
        width: min(1100px, 100%);
        height: min(90vh, 800px);
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .slider-image {
        max-width: calc(100% - 120px);
        max-height: 85vh;
        width: auto;
        height: auto;
        object-fit: contain;
        border-radius: 10px;
        user-select: none;
        -webkit-user-drag: none;
    }

    .slider-close,
    .slider-prev,
    .slider-next {
        position: absolute;
        z-index: 2;
        display: flex;
        align-items: center;
        justify-content: center;
        width: 48px;
        height: 48px;
        border: 1px solid rgba(255,255,255,.2);
        border-radius: 50%;
        background: rgba(255,255,255,.08);
        color: #fff;
        cursor: pointer;
        transition: .2s ease;
    }

    .slider-close:hover,
    .slider-prev:hover,
    .slider-next:hover {
        background: #fff;
        color: #000;
    }

    .slider-close {
        top: 10px;
        right: 10px;
    }

    .slider-prev {
        left: 10px;
    }

    .slider-next {
        right: 10px;
    }

    .slider-counter {
        position: absolute;
        bottom: 10px;
        left: 50%;
        transform: translateX(-50%);
        padding: 7px 12px;
        border-radius: 100px;
        background: rgba(0,0,0,.6);
        color: #fff;
        font-size: 12px;
    }

    .slider-title {
        position: absolute;
        top: 10px;
        left: 50%;
        transform: translateX(-50%);
        width: 70%;
        text-align: center;
        color: #fff;
        font-size: 14px;
    }

    /* =========================
       MOBILE
    ========================= */

    @media (max-width: 900px) {

        .nav-container {
            min-height: 64px;
        }

        .menu-toggle {
            display: block;
        }

        .nav-menu {
            position: absolute;
            top: 64px;
            left: 12px;
            right: 12px;

            display: none;
            flex-direction: column;
            align-items: stretch;

            padding: 10px;
            background: rgba(15,15,15,.98);
            border: 1px solid var(--border);
            border-radius: 14px;
        }

        .nav-menu.show {
            display: flex;
        }

        .nav-menu a {
            padding: 13px;
        }

        .hero {
            min-height: 75vh;
            padding: 70px 20px;
        }

        .hero h1 {
            letter-spacing: -2.5px;
        }

        .bento-grid,
        .price-grid,
        .contact-grid {
            grid-template-columns: 1fr;
        }

        .about-layout {
            grid-template-columns: 1fr;
        }

        .card-image {
            min-height: 350px;
            order: 2;
        }

        .founder-text {
            order: 1;
        }

        section {
            padding: 65px 18px;
        }
    }

    @media (max-width: 600px) {

        .nav-container {
            padding: 0 16px;
        }

        .logo {
            font-size: 17px;
        }

        .hero {
            padding: 60px 18px;
        }

        .hero h1 {
            font-size: clamp(42px, 15vw, 70px);
        }

        .hero p {
            font-size: 15px;
        }

        .hero-buttons {
            flex-direction: column;
        }

        .hero-buttons .btn {
            width: 100%;
        }

        .bento-card {
            padding: 23px;
        }

        .bento-card h3 {
            font-size: 23px;
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

        .masonry-grid {
            columns: 1;
        }

        .price-card {
            padding: 24px;
        }

        .founder-text h3 {
            font-size: 29px;
        }

        .card-image {
            min-height: 300px;
        }

        .contact-card {
            min-height: 170px;
        }

        .slider-modal {
            padding: 10px;
        }

        .slider-content {
            height: 90vh;
        }

        .slider-image {
            max-width: 100%;
            max-height: 75vh;
        }

        .slider-prev,
        .slider-next {
            width: 42px;
            height: 42px;
        }

        .slider-prev {
            left: 5px;
        }

        .slider-next {
            right: 5px;
        }

        .slider-close {
            top: 0;
            right: 0;
        }

        .slider-title {
            top: 5px;
            width: 60%;
            font-size: 12px;
        }
    }

    /* =========================
       REDUCE MOTION
    ========================= */

    @media (prefers-reduced-motion: reduce) {
        *,
        *::before,
        *::after {
            scroll-behavior: auto !important;
            transition: none !important;
            animation: none !important;
        }
    }

</style>

</head>

<body>

<!-- =========================
     NAVBAR
========================= -->

<header class="navbar">

    <div class="nav-container">

        <a href="#home" class="logo">
            Another <span>Visual</span>
        </a>

        <button
            class="menu-toggle"
            id="menuToggle"
            aria-label="Buka menu"
            aria-expanded="false">
            ☰
        </button>

        <nav>

            <ul class="nav-menu" id="navMenu">

                <li>
                    <a href="#home" class="active">
                        Home
                    </a>
                </li>

                <li>
                    <a href="#filosofi">
                        Filosofi
                    </a>
                </li>

                <li>
                    <a href="#portfolio">
                        Portfolio
                    </a>
                </li>

                <li>
                    <a href="#pricelist">
                        Pricelist
                    </a>
                </li>

                <li>
                    <a href="#tentang">
                        Tentang Kami
                    </a>
                </li>

                <li>
                    <a href="#kontak">
                        Kontak
                    </a>
                </li>

            </ul>

        </nav>

    </div>

</header>


<!-- =========================
     HOME
========================= -->

<main>

    <section id="home" class="hero">

        <div class="hero-content">

            <span class="hero-tag">
                Photography • Videography • Visual Production
            </span>

            <h1>
                Another<br>
                <span>Visual.</span>
            </h1>

            <p>
                Mengabadikan cerita, emosi, dan momen melalui
                karya visual yang memiliki karakter.
            </p>

            <div class="hero-buttons">

                <a
                    href="#portfolio"
                    class="btn btn-white">
                    Lihat Portfolio
                </a>

                <a
                    href="#kontak"
                    class="btn btn-dark">
                    Hubungi Kami
                </a>

            </div>

        </div>

    </section>


    <!-- =========================
         FILOSOFI
    ========================= -->

    <section id="filosofi">

        <div class="section-header">

            <span class="section-tag">
                01. Filosofi
            </span>

            <h2>
                Visual yang<br>
                punya cerita.
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
                    Kami percaya bahwa mahakarya visual tidak ditentukan
                    seberapa mahal alat yang digenggam, melainkan bagaimana
                    ketajaman mata seorang kreator dalam merangkai cerita,
                    komposisi, dan emosi di setiap jepretan.
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
                    Visi utama kami adalah menghadirkan standar visual
                    tertinggi yang menyentuh hati. Melalui teknik
                    pencahayaan matang, sudut pandang sinematik, dan
                    sentuhan emosional, setiap momen diabadikan bukan
                    sekadar gambar, melainkan sebuah mahakarya abadi.
                </p>

            </div>

        </div>

    </section>


    <!-- =========================
         PORTFOLIO
    ========================= -->

    <section id="portfolio">

        <div class="section-header">

            <span class="section-tag">
                02. Portfolio
            </span>

            <h2>
                Selected Works.
            </h2>

            <p>
                Beberapa karya yang telah kami abadikan.
                Klik foto untuk melihat seluruh dokumentasi.
            </p>

        </div>

        <div class="folder-nav">

            <button
                class="folder-btn active"
                data-filter="all">
                Semua Folder
            </button>

            <button
                class="folder-btn"
                data-filter="wedding">
                Wedding
            </button>

            <button
                class="folder-btn"
                data-filter="engagement">
                Engagement
            </button>

            <button
                class="folder-btn"
                data-filter="wisuda">
                Wisuda
            </button>

            <button
                class="folder-btn"
                data-filter="event">
                Event
            </button>

        </div>


        <div class="masonry-grid">

            <!-- =========================
                 WEDDING
            ========================= -->

            <div
                class="port-item wedding"
                data-title="Wedding Falaq & Cindy"
                data-images='[
                    "https://lh3.googleusercontent.com/d/1K5JYuw4FpqSI9NEduRvZNm_8eJRS_Mr2",
                    "https://lh3.googleusercontent.com/d/1sJJIfzNtLeDnY69v5W9it6EMWJzScWO",
                    "https://lh3.googleusercontent.com/d/18V0VTAzCCy9rw8Pkyy3jwVr06jbwqXjE",
                    "https://lh3.googleusercontent.com/d/18AiExWPI4x61GapsGDVEBAq6v3mhiUvw",
                    "https://lh3.googleusercontent.com/d/1jKrtiykv5AEAyyIixWZJIblm4kwSbvj3",
                    "https://lh3.googleusercontent.com/d/1VikQ2MtDl94PstxWeOPGFGZZBA76wRAJ",
                    "https://lh3.googleusercontent.com/d/18UYnUMDsVlxNF5CD3oRa7ShpY560WHPY",
                    "https://lh3.googleusercontent.com/d/12_urvrE4195fyQmf1RhEv3-ToTvxv6l5",
                    "https://lh3.googleusercontent.com/d/1ffcvFRZDPaoMzVLIgqm3GgDp83qRak6v"
                ]'>

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


            <!-- =========================
                 ENGAGEMENT
            ========================= -->

            <div
                class="port-item engagement"
                data-title="Engagement Fikry & Reny"
                data-images='[
                    "https://lh3.googleusercontent.com/d/1CSJdaeY-POpOhoytFeI4PyPvCc6_43Jk",
                    "https://lh3.googleusercontent.com/d/1RZIXo9bAFTMbIv327LqCBZZys3No0Jop",
                    "https://lh3.googleusercontent.com/d/16RB0mGvb4YMqixSaT5ugndThBWce_IP4",
                    "https://lh3.googleusercontent.com/d/1pgDLZcUJxZ5fiGv4EadaWnQyigXkrLmc",
                    "https://lh3.googleusercontent.com/d/1ul39oBgor5kz0XAVGsM0vEPVOcfrKVv9",
                    "https://lh3.googleusercontent.com/d/1JLmj7thqafLvTXMTqGZXCLMx5mo1gtpm",
                    "https://lh3.googleusercontent.com/d/1aVgL_GPfg2adk_RN1UYLaL1vM1wkZ8iw",
                    "https://lh3.googleusercontent.com/d/1bl36KWAmRwiRCaqQicr1xZhBOc86RcwO",
                    "https://lh3.googleusercontent.com/d/17yN3ucaM5EtI46O7e8fGwdWyKxfylyCW",
                    "https://lh3.googleusercontent.com/d/1boUj5TLrYIWDkrcgW8AQsTghgnke36rk",
                    "https://lh3.googleusercontent.com/d/1UmCat8QQcEtkDr2KyzhM0yWys7l7LDkc",
                    "https://lh3.googleusercontent.com/d/19I127-vR7AFi6OKdj2vFYBLA6DJofGMU",
                    "https://lh3.googleusercontent.com/d/1Ui7W4zjre4TtivvXq2NDbsyw3gTqqIhC"
                ]'>

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


            <!-- =========================
                 WISUDA
            ========================= -->

            <div
                class="port-item wisuda"
                data-title="Wisuda Reny Riani"
                data-images='[
                    "https://lh3.googleusercontent.com/d/1tdANeaA_DLSrfHtAXZQQEDzNckCwCl_u",
                    "https://lh3.googleusercontent.com/d/1ANX4TlyLrA2rg4es-1twvUenPk2xD8ha",
                    "https://lh3.googleusercontent.com/d/1L9HRUY0fNw6iAVpeb3TofmZWORZY82so",
                    "https://lh3.googleusercontent.com/d/1X4687Zb8Zos-tGLzKB44nmIBlZeBrR9_",
                    "https://lh3.googleusercontent.com/d/1CTqP6v3eLVrPBklcaRW7sttGg4_QwgCx",
                    "https://lh3.googleusercontent.com/d/1sPew-WXRoUgqJr-7rJXoqHli882oFJi1"
                ]'>

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


            <!-- =========================
                 EVENT - JALAN SANTAI
            ========================= -->

            <div
                class="port-item event"
                data-title="Jalan Santai Kemerdekaan 2025"
                data-images='[
                    "https://lh3.googleusercontent.com/d/1_axQ1oATs8QwUrEDC56LEWqSs5cwa5LA",
                    "https://lh3.googleusercontent.com/d/1rLXnbHyq6fo_bcscrBcXqjiXNjQ9dcYN",
                    "https://lh3.googleusercontent.com/d/1zkjFPSBp0x4keMEPfFJv0tGuRjHae2GL",
                    "https://lh3.googleusercontent.com/d/1cWtB847VpSlCIG_KqRce9I6_5ql_TU5O",
                    "https://lh3.googleusercontent.com/d/1fT-R800YeD44qZNZnl-KKq6qPQkgs39p"
                ]'>

                <img
                    src="https://lh3.googleusercontent.com/d/1_axQ1oATs8QwUrEDC56LEWqSs5cwa5LA"
                    alt="Jalan Santai Kemerdekaan 2025"
                    loading="lazy">

                <div class="port-overlay">

                    <div class="port-cat">
                        Event (5 Foto)
                    </div>

                    <div class="port-title">
                        Jalan Santai 2025
                    </div>

                </div>

            </div>


            <!-- =========================
                 EVENT - BIRTHDAY SHIFA
            ========================= -->

            <div
                class="port-item event"
                data-title="Birthday Party Shifa Derma Hapsari"
                data-images='[
                    "https://lh3.googleusercontent.com/d/1N8-sIvxr8eRICT9wMClRGXyJ9yg-WUTP",
                    "https://lh3.googleusercontent.com/d/1Kr6qz8GT-HVv82WTRv-MY71KsoZGnJnl",
                    "https://lh3.googleusercontent.com/d/10YXaft2ZExYEacVuol2zFp_AOas-eRo1",
                    "https://lh3.googleusercontent.com/d/1H_a6sd6MgSwJsi9hijA9-ZF00pHgbk4T",
                    "https://lh3.googleusercontent.com/d/1QCaSzkwp1ajyZdrr5GWoSbTnPV_Hfz-D",
                    "https://lh3.googleusercontent.com/d/1UWt9F8kFj4MZYh_nR-25vWI8q3fzWQAs",
                    "https://lh3.googleusercontent.com/d/1xytZeJttsAUARa5dX12eKjmsAtWKLRxs",
                    "https://lh3.googleusercontent.com/d/1K-2JFojdFZ3PBlmVrWztzKs3J5Vj-4_A",
                    "https://lh3.googleusercontent.com/d/1_uFxx6Oj8mXfE6BdA_D7tbKw80gFSy-B",
                    "https://lh3.googleusercontent.com/d/1Efld3NKoTzX8sK7VCZlcl7cbS3oKROqH",
                    "https://lh3.googleusercontent.com/d/1XhC7QPcsF1-64OegG1WNJryA2ODnBlKg",
                    "https://lh3.googleusercontent.com/d/11qDcFJ33eFJuvilWnYXDlvhHMPdhpIyD",
                    "https://lh3.googleusercontent.com/d/1rRxSq32KlKwQ6Y5tioCCaazpPtu3Klae",
                    "https://lh3.googleusercontent.com/d/1PderuDJmq8xsbk5KGGMb2py8fI9In3hh",
                    "https://lh3.googleusercontent.com/d/1Dzu4O2B-zh0_cyMr6Pot89eJ0zsdD22A"
                ]'>

                <img
                    src="https://lh3.googleusercontent.com/d/1N8-sIvxr8eRICT9wMClRGXyJ9yg-WUTP"
                    alt="Birthday Party Shifa Derma Hapsari"
                    loading="lazy">

                <div class="port-overlay">

                    <div class="port-cat">
                        Event (15 Foto)
                    </div>

                    <div class="port-title">
                        Birthday Party Shifa Derma Hapsari
                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         PRICELIST
    ========================= -->

    <section id="pricelist">

        <div class="section-header">

            <span class="section-tag">
                05. Pricelist
            </span>

            <h2>
                Pilih paket<br>
                yang sesuai.
            </h2>

        </div>


        <span class="section-tag price-section-title">
            01. Paket Wedding
        </span>

        <div class="price-grid">

            <div class="price-card">

                <h3>
                    Basic
                </h3>

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
                    class="btn-outline">
                    Pilih Paket
                </a>

            </div>


            <div class="price-card premium">

                <h3>
                    Premium
                </h3>

                <div class="price-amount">
                    Rp 1.500.000
                </div>

                <ul class="price-features">

                    <li>
                        1 Fotografer & 1 Videografer
                    </li>

                    <li>
                        Edit Foto + Video Sinematik (Max 5 Menit)
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
                    class="btn-solid">
                    Pilih Paket
                </a>

            </div>

        </div>


        <span class="section-tag price-section-title">
            02. Paket Engagement
        </span>

        <div class="price-grid">

            <div class="price-card">

                <h3>
                    Foto Saja
                </h3>

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
                    class="btn-outline">
                    Pilih Paket
                </a>

            </div>


            <div class="price-card">

                <h3>
                    Video Saja
                </h3>

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
                    class="btn-outline">
                    Pilih Paket
                </a>

            </div>


            <div class="price-card premium">

                <h3>
                    Komplit
                </h3>

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
                    class="btn-solid">
                    Pilih Paket
                </a>

            </div>

        </div>


        <span class="section-tag price-section-title">
            03. Paket Wisuda
        </span>

        <div class="price-grid">

            <div class="price-card">

                <h3>
                    Basic
                </h3>

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
                    class="btn-outline">
                    Pilih Paket
                </a>

            </div>


            <div class="price-card">

                <h3>
                    Premium
                </h3>

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
                    class="btn-outline">
                    Pilih Paket
                </a>

            </div>


            <div class="price-card premium">

                <h3>
                    Pro
                </h3>

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
                    class="btn-solid">
                    Pilih Paket
                </a>

            </div>

        </div>
        

        <span class="section-tag price-section-title">
            01. Paket Event
        </span>

        <div class="price-grid">

            <div class="price-card">

                <h3>
                    Basic
                </h3>

                <div class="price-amount">
                    Rp 900.000
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
                    class="btn-outline">
                    Pilih Paket
                </a>

            </div>


            <div class="price-card premium">

                <h3>
                    Premium
                </h3>

                <div class="price-amount">
                    Rp 2.000.000
                </div>

                <ul class="price-features">

                    <li>
                        1 Fotografer & 1 Videografer
                    </li>

                    <li>
                        Edit Foto + Video Sinematik (Max 5 Menit)
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
                    class="btn-solid">
                    Pilih Paket
                </a>

            </div>

        </div>


    </section>


    <!-- =========================
         TENTANG KAMI
    ========================= -->

    <section id="tentang">

        <div class="section-header">

            <span class="section-tag">
                06. Tentang Kami
            </span>

            <h2>
                Mengenal<br>
                Another Visual.
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
                    Perkenalkan saya Alif Nur Hidayat
                    selaku Founder dari PT Another Visual
                </h4>

                <p>
                    Saya mewakili tim dan pendiri PT Another Visual
                    ingin mengucapkan terima kasih sebesar-besarnya
                    kepada seluruh klien, mitra, kru, dan semua pihak
                    yang telah mempercayakan momen berharganya kepada kami.
                </p>

                <p>
                    Bagi kami, PT Another Visual bukan hanya tentang
                    foto, video, atau produksi visual. Kami percaya
                    setiap event punya cerita, setiap momen punya makna,
                    dan tugas kami adalah mengabadikannya dengan cara
                    terbaik agar bisa terus dikenang.
                </p>

                <p>
                    Perjalanan kami sampai hari ini tentunya tidak mudah.
                    Namun berkat dukungan dan kepercayaan dari kalian semua,
                    PT Another Visual terus berkembang menjadi tim kreatif
                    yang selalu ingin memberikan hasil terbaik, profesional,
                    dan penuh dedikasi.
                </p>

                <p>
                    Dari tahap pra-produksi hingga hasil akhir yang dapat
                    dinikmati bersama, setiap proses dikerjakan dengan
                    dedikasi penuh. Tanpa kerja sama, konsistensi, dan
                    semangat solid dari tim, pencapaian ini mustahil terwujud.
                </p>

                <p>
                    Semoga ke depannya PT Another Visual bisa terus hadir,
                    berkarya, dan menjadi bagian dari lebih banyak cerita
                    luar biasa lainnya. Terima kasih sudah menjadi bagian
                    dari perjalanan kami.
                </p>

                <p class="signature">
                    Salam hangat,<br>
                    <span>
                        Alif Nur Hidayat — Founder PT Another Visual
                    </span>
                </p>

            </div>


            <div
                class="card-image"
                style="
                    background-image:
                    url('https://lh3.googleusercontent.com/d/1XCVRVaa9RkMXH04tVXUSDGJZN92wRSL9');
                "
                role="img"
                aria-label="Founder PT Another Visual">
            </div>

        </div>

    </section>


    <!-- =========================
         KONTAK
    ========================= -->

    <section id="kontak">

        <div class="section-header">

            <span class="section-tag">
                07. Kontak
            </span>

            <h2>
                Mari buat<br>
                sesuatu bersama.
            </h2>

        </div>


        <div class="contact-grid">

            <a
                href="https://wa.me/6287765829615"
                target="_blank"
                rel="noopener noreferrer"
                class="bento-card contact-card">

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


            <a
                href="mailto:anothervisualjakarta@gmail.com"
                class="bento-card contact-card">

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


            <a
                href="https://instagram.com/another_visual.id"
                target="_blank"
                rel="noopener noreferrer"
                class="bento-card contact-card">

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

    </section>

</main>


<!-- =========================
     FOOTER
========================= -->

<footer>

    <p>
        Ikuti Another Visual
    </p>


    <!-- SOCIAL MEDIA ICONS -->

    <div class="social-links">

        <!-- INSTAGRAM -->

        <a
            href="https://instagram.com/another_visual.id"
            target="_blank"
            rel="noopener noreferrer"
            class="social-link"
            aria-label="Instagram Another Visual">

            <svg
                viewBox="0 0 24 24"
                aria-hidden="true">

                <path d="M7.5 2h9A5.5 5.5 0 0 1 22 7.5v9a5.5 5.5 0 0 1-5.5 5.5h-9A5.5 5.5 0 0 1 2 16.5v-9A5.5 5.5 0 0 1 7.5 2Zm0 2A3.5 3.5 0 0 0 4 7.5v9A3.5 3.5 0 0 0 7.5 20h9a3.5 3.5 0 0 0 3.5-3.5v-9A3.5 3.5 0 0 0 16.5 4h-9ZM12 7a5 5 0 1 1 0 10 5 5 0 0 1 0-10Zm0 2a3 3 0 1 0 0 6 3 3 0 0 0 0-6Zm5.25-3.25a1.25 1.25 0 1 1 0 2.5 1.25 1.25 0 0 1 0-2.5Z"/>

            </svg>

        </a>


        <!-- WHATSAPP -->

        <a
            href="https://wa.me/6287765829615"
            target="_blank"
            rel="noopener noreferrer"
            class="social-link"
            aria-label="WhatsApp Another Visual">

            <svg
                viewBox="0 0 24 24"
                aria-hidden="true">

                <path d="M12 2a9.9 9.9 0 0 0-8.55 14.9L2 22l5.27-1.38A10 10 0 1 0 12 2Zm0 2a8 8 0 0 1 6.93 12L18.1 17.3l-3.12.82-.18.03a8 8 0 0 1-4.03-1.08l-.27-.16-2.95.77.79-2.82-.18-.28A8 8 0 1 1 12 4Zm-3.3 3.7c-.2 0-.5.08-.7.32-.2.23-.76.75-.76 1.82s.78 2.11.89 2.26c.11.14 1.53 2.46 3.75 3.34.52.2.93.32 1.25.41.53.17 1.01.14 1.39.08.42-.06 1.3-.53 1.48-1.04.18-.51.18-.95.13-1.04-.05-.09-.2-.14-.42-.25-.22-.11-1.3-.64-1.5-.71-.2-.08-.35-.11-.5.11-.15.23-.58.71-.71.86-.13.15-.26.17-.48.06-.22-.11-.93-.34-1.77-1.09-.65-.58-1.09-1.3-1.22-1.52-.13-.23-.01-.35.1-.46.1-.1.22-.26.33-.39.11-.13.15-.23.22-.38.07-.15.04-.28-.02-.39-.06-.11-.5-1.2-.69-1.64-.18-.43-.36-.37-.5-.38Z"/>

            </svg>

        </a>

    </div>


    <p>
        © <span id="currentYear"></span>
        PT Another Visual. All rights reserved.
    </p>

    <span id="deviceInfo"></span>

</footer>


<!-- =========================
     SLIDER MODAL
========================= -->

<div
    class="slider-modal"
    id="sliderModal"
    aria-hidden="true">

    <div class="slider-content">

        <div
            class="slider-title"
            id="sliderTitle">
        </div>

        <button
            class="slider-close"
            id="sliderClose"
            aria-label="Tutup">
            ×
        </button>

        <button
            class="slider-prev"
            id="sliderPrev"
            aria-label="Foto sebelumnya">
            ‹
        </button>

        <img
            id="sliderImage"
            class="slider-image"
            src=""
            alt="Portfolio">

        <button
            class="slider-next"
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


<!-- =========================
     JAVASCRIPT
========================= -->

<script>

    /* =========================
       CURRENT YEAR
    ========================= */

    document.getElementById("currentYear").textContent =
        new Date().getFullYear();


    /* =========================
       DEVICE DETECTION
    ========================= */

    function detectDevice() {

        const width = window.innerWidth;

        let device = "Desktop";

        if (width <= 600) {
            device = "Mobile";
        } else if (width <= 1024) {
            device = "Tablet";
        }

        document.body.dataset.device =
            device.toLowerCase();

        return device;
    }

    detectDevice();

    window.addEventListener(
        "resize",
        detectDevice
    );


    /* =========================
       MOBILE MENU
    ========================= */

    const menuToggle =
        document.getElementById("menuToggle");

    const navMenu =
        document.getElementById("navMenu");

    menuToggle.addEventListener(
        "click",
        function () {

            const isOpen =
                navMenu.classList.toggle("show");

            menuToggle.setAttribute(
                "aria-expanded",
                isOpen
            );

        }
    );


    /* Tutup menu setelah klik */

    document.querySelectorAll(".nav-menu a")
        .forEach(function(link) {

            link.addEventListener(
                "click",
                function() {

                    navMenu.classList.remove(
                        "show"
                    );

                    menuToggle.setAttribute(
                        "aria-expanded",
                        "false"
                    );

                }
            );

        });


    /* =========================
       ACTIVE NAVIGATION
    ========================= */

    const sections =
        document.querySelectorAll(
            "main section"
        );

    const navLinks =
        document.querySelectorAll(
            ".nav-menu a"
        );

    const observer =
        new IntersectionObserver(
            function(entries) {

                entries.forEach(
                    function(entry) {

                        if (
                            entry.isIntersecting
                        ) {

                            navLinks.forEach(
                                function(link) {

                                    link.classList.remove(
                                        "active"
                                    );

                                }
                            );

                            const activeLink =
                                document.querySelector(
                                    '.nav-menu a[href="#' +
                                    entry.target.id +
                                    '"]'
                                );

                            if (activeLink) {

                                activeLink.classList.add(
                                    "active"
                                );

                            }

                        }

                    }
                );

            },
            {
                rootMargin:
                    "-35% 0px -55% 0px"
            }
        );

    sections.forEach(
        function(section) {
            observer.observe(section);
        }
    );


    /* =========================
       PORTFOLIO FILTER
    ========================= */

    const filterButtons =
        document.querySelectorAll(
            ".folder-btn"
        );

    const portfolioItems =
        document.querySelectorAll(
            ".port-item"
        );


    filterButtons.forEach(
        function(button) {

            button.addEventListener(
                "click",
                function() {

                    const filter =
                        button.dataset.filter;

                    filterButtons.forEach(
                        function(btn) {

                            btn.classList.remove(
                                "active"
                            );

                        }
                    );

                    button.classList.add(
                        "active"
                    );

                    portfolioItems.forEach(
                        function(item) {

                            if (
                                filter === "all" ||
                                item.classList.contains(
                                    filter
                                )
                            ) {

                                item.classList.remove(
                                    "hidden"
                                );

                            } else {

                                item.classList.add(
                                    "hidden"
                                );

                            }

                        }
                    );

                }
            );

        }
    );


    /* =========================
       SLIDER
    ========================= */

    const sliderModal =
        document.getElementById(
            "sliderModal"
        );

    const sliderImage =
        document.getElementById(
            "sliderImage"
        );

    const sliderTitle =
        document.getElementById(
            "sliderTitle"
        );

    const sliderCounter =
        document.getElementById(
            "sliderCounter"
        );

    const sliderClose =
        document.getElementById(
            "sliderClose"
        );

    const sliderPrev =
        document.getElementById(
            "sliderPrev"
        );

    const sliderNext =
        document.getElementById(
            "sliderNext"
        );


    let currentImages = [];
    let currentIndex = 0;


    function openSlider(
        images,
        title
    ) {

        if (
            !Array.isArray(images) ||
            images.length === 0
        ) {
            return;
        }

        currentImages = images;
        currentIndex = 0;

        sliderTitle.textContent =
            title || "";

        sliderModal.classList.add(
            "active"
        );

        sliderModal.setAttribute(
            "aria-hidden",
            "false"
        );

        document.body.classList.add(
            "no-scroll"
        );

        updateSlider();

    }


    function updateSlider() {

        if (!currentImages.length) {
            return;
        }

        sliderImage.src =
            currentImages[currentIndex];

        sliderCounter.textContent =
            (currentIndex + 1) +
            " / " +
            currentImages.length;

    }


    function nextSlide() {

        if (!currentImages.length) {
            return;
        }

        currentIndex =
            (currentIndex + 1) %
            currentImages.length;

        updateSlider();

    }


    function prevSlide() {

        if (!currentImages.length) {
            return;
        }

        currentIndex =
            (currentIndex - 1 +
            currentImages.length) %
            currentImages.length;

        updateSlider();

    }


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

        currentImages = [];
        currentIndex = 0;

    }


    sliderNext.addEventListener(
        "click",
        nextSlide
    );

    sliderPrev.addEventListener(
        "click",
        prevSlide
    );

    sliderClose.addEventListener(
        "click",
        closeSlider
    );


    /* Klik area gelap untuk menutup */

    sliderModal.addEventListener(
        "click",
        function(event) {

            if (
                event.target === sliderModal
            ) {

                closeSlider();

            }

        }
    );


    /* =========================
       PORTFOLIO CLICK
    ========================= */

    portfolioItems.forEach(
        function(item) {

            item.addEventListener(
                "click",
                function() {

                    try {

                        const images =
                            JSON.parse(
                                item.dataset.images
                            );

                        openSlider(
                            images,
                            item.dataset.title
                        );

                    } catch (error) {

                        console.error(
                            "Portfolio error:",
                            error
                        );

                    }

                }
            );

        }
    );


    /* =========================
       KEYBOARD SLIDER
    ========================= */

    document.addEventListener(
        "keydown",
        function(event) {

            if (
                !sliderModal.classList.contains(
                    "active"
                )
            ) {
                return;
            }

            if (
                event.key === "ArrowRight"
            ) {

                nextSlide();

            }

            if (
                event.key === "ArrowLeft"
            ) {

                prevSlide();

            }

            if (
                event.key === "Escape"
            ) {

                closeSlider();

            }

        }
    );


    /* =========================
       SWIPE SLIDER MOBILE
    ========================= */

    let touchStartX = 0;
    let touchEndX = 0;


    sliderModal.addEventListener(
        "touchstart",
        function(event) {

            touchStartX =
                event.changedTouches[0]
                .screenX;

        },
        {
            passive: true
        }
    );


    sliderModal.addEventListener(
        "touchend",
        function(event) {

            touchEndX =
                event.changedTouches[0]
                .screenX;

            handleSwipe();

        },
        {
            passive: true
        }
    );


    function handleSwipe() {

        const difference =
            touchEndX - touchStartX;

        if (
            Math.abs(difference) < 50
        ) {
            return;
        }

        if (difference < 0) {

            nextSlide();

        } else {

            prevSlide();

        }

    }


    /* =========================
       IMAGE PROTECTION
    ========================= */

    document.addEventListener(
        "contextmenu",
        function(event) {

            if (
                event.target.tagName === "IMG" ||
                event.target.classList.contains(
                    "card-image"
                )
            ) {

                event.preventDefault();

            }

        }
    );


    document.addEventListener(
        "dragstart",
        function(event) {

            if (
                event.target.tagName === "IMG"
            ) {

                event.preventDefault();

            }

        }
    );


    document.addEventListener(
        "keydown",
        function(event) {

            const key =
                event.key.toLowerCase();

            if (
                (event.ctrlKey ||
                 event.metaKey) &&
                ["s", "u", "c"].includes(key)
            ) {

                event.preventDefault();

            }

        }
    );

</script>

</body>
</html>
```
