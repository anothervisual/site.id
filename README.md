<!DOCTYPE html>

<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

```
<meta
    name="description"
    content="PT Another Visual - Photography, Videography, Wedding, Engagement, Wisuda dan Event."
>

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
    }

    body {
        font-family: Arial, Helvetica, sans-serif;
        background: #080808;
        color: #fff;
        line-height: 1.7;
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
    }

    a {
        color: inherit;
        text-decoration: none;
    }

    :root {
        --bg: #080808;
        --bg-soft: #111111;
        --card: #151515;
        --card-hover: #1c1c1c;
        --border: rgba(255, 255, 255, 0.09);
        --text: #ffffff;
        --text-muted: #a6a6a6;
        --accent: #ffffff;
        --radius: 22px;
        --radius-md: 16px;
        --max-width: 1200px;
    }


    /* =========================================================
       GENERAL
    ========================================================= */

    .container {
        width: min(100% - 40px, var(--max-width));
        margin: 0 auto;
    }

    .section {
        padding: 80px 0;
    }

    .section-title {
        margin-bottom: 35px;
    }

    .section-title h2 {
        font-size: clamp(30px, 5vw, 52px);
        line-height: 1.1;
        margin-bottom: 12px;
    }

    .section-title p {
        color: var(--text-muted);
        max-width: 700px;
    }

    .section-tag {
        display: inline-block;
        margin-bottom: 14px;
        color: var(--text-muted);
        font-size: 12px;
        font-weight: 700;
        letter-spacing: 2px;
        text-transform: uppercase;
    }


    /* =========================================================
       BENTO
    ========================================================= */

    .bento-grid {
        display: grid;
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 20px;
    }

    .bento-card {
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--radius);
        padding: 30px;
        transition:
            transform 0.3s ease,
            background 0.3s ease,
            border-color 0.3s ease;
    }

    .bento-card:hover {
        transform: translateY(-4px);
        background: var(--card-hover);
        border-color: rgba(255, 255, 255, 0.16);
    }

    .bento-card h3 {
        font-size: clamp(23px, 3vw, 32px);
        line-height: 1.2;
        margin-bottom: 15px;
    }

    .bento-card p {
        color: var(--text-muted);
        font-size: 15px;
    }


    /* =========================================================
       PORTFOLIO FILTER
    ========================================================= */

    .folder-nav {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        margin-bottom: 30px;
    }

    .folder-btn {
        cursor: pointer;
        color: #aaa;
        background: #151515;
        border: 1px solid var(--border);
        border-radius: 999px;
        padding: 10px 18px;
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
        columns: 3 280px;
        column-gap: 18px;
    }

    .port-item {
        position: relative;
        display: inline-block;
        width: 100%;
        margin: 0 0 18px;
        overflow: hidden;
        border-radius: var(--radius-md);
        background: #111;
        cursor: pointer;
        break-inside: avoid;
        -webkit-column-break-inside: avoid;
    }

    .port-item.hidden {
        display: none;
    }

    .port-item img {
        width: 100%;
        height: auto;
        min-height: 180px;
        object-fit: cover;
        transition: transform 0.5s ease;
    }

    .port-item:hover img {
        transform: scale(1.05);
    }

    .port-overlay {
        position: absolute;
        inset: auto 0 0 0;
        padding: 60px 20px 20px;
        background: linear-gradient(
            transparent,
            rgba(0, 0, 0, 0.88)
        );
        pointer-events: none;
    }

    .port-cat {
        color: #ccc;
        font-size: 11px;
        letter-spacing: 1.5px;
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

    .price-grid {
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 20px;
        margin-bottom: 45px;
    }

    .price-card {
        display: flex;
        flex-direction: column;
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: var(--radius);
        padding: 28px;
        min-height: 100%;
    }

    .price-card.premium {
        border-color: rgba(255, 255, 255, 0.35);
        background: linear-gradient(
            145deg,
            #1b1b1b,
            #101010
        );
    }

    .price-card h3 {
        font-size: 24px;
        margin-bottom: 10px;
    }

    .price-amount {
        font-size: clamp(25px, 4vw, 34px);
        font-weight: 800;
        margin-bottom: 20px;
    }

    .price-features {
        list-style: none;
        color: var(--text-muted);
        margin-bottom: 25px;
    }

    .price-features li {
        position: relative;
        padding-left: 20px;
        margin-bottom: 9px;
        font-size: 14px;
    }

    .price-features li::before {
        content: "✓";
        position: absolute;
        left: 0;
        color: #fff;
    }

    .btn-outline,
    .btn-solid {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        width: 100%;
        min-height: 48px;
        padding: 12px 18px;
        border-radius: 12px;
        font-weight: 700;
        cursor: pointer;
        transition: all 0.25s ease;
        margin-top: auto;
    }

    .btn-outline {
        color: #fff;
        border: 1px solid rgba(255, 255, 255, 0.25);
        background: transparent;
    }

    .btn-outline:hover {
        color: #000;
        background: #fff;
    }

    .btn-solid {
        color: #000;
        background: #fff;
    }

    .btn-solid:hover {
        background: #ddd;
        transform: translateY(-2px);
    }


    /* =========================================================
       ABOUT
    ========================================================= */

    .about-layout {
        display: grid;
        grid-template-columns: 1.15fr 0.85fr;
        gap: 30px;
        align-items: stretch;
    }

    .founder-text h4 {
        margin-bottom: 12px;
        font-size: 18px;
    }

    .founder-text p {
        margin-bottom: 17px;
    }

    .card-image {
        width: 100%;
        min-height: 400px;
    }


    /* =========================================================
       CONTACT
    ========================================================= */

    .contact-grid {
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 20px;
    }

    .contact-card h4 {
        font-size: 21px;
        margin-bottom: 5px;
    }

    .contact-card a {
        color: var(--text-muted);
        word-break: break-word;
        transition: color 0.2s ease;
    }

    .contact-card a:hover {
        color: #fff;
    }


    /* =========================================================
       SLIDER / LIGHTBOX
    ========================================================= */

    .slider-modal {
        position: fixed;
        inset: 0;
        z-index: 99999;
        display: none;
        align-items: center;
        justify-content: center;
        padding: 20px;
        background: rgba(0, 0, 0, 0.96);
        opacity: 0;
        transition: opacity 0.25s ease;
    }

    .slider-modal.active {
        display: flex;
        opacity: 1;
    }

    .slider-content {
        position: relative;
        width: 100%;
        height: 100%;
        max-width: 1400px;
        display: flex;
        align-items: center;
        justify-content: center;
        user-select: none;
        touch-action: pan-y;
    }

    .slider-image {
        display: block;
        width: auto;
        height: auto;
        max-width: calc(100vw - 120px);
        max-height: calc(100vh - 150px);
        object-fit: contain;
        border-radius: 8px;
        box-shadow: 0 20px 80px rgba(0, 0, 0, 0.6);
        user-select: none;
        -webkit-user-drag: none;
    }

    .slider-close,
    .slider-prev,
    .slider-next {
        position: fixed;
        z-index: 100001;
        display: flex;
        align-items: center;
        justify-content: center;
        width: 48px;
        height: 48px;
        border-radius: 50%;
        color: #fff;
        background: rgba(255, 255, 255, 0.1);
        border: 1px solid rgba(255, 255, 255, 0.18);
        cursor: pointer;
        transition: all 0.2s ease;
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
        font-size: 28px;
    }

    .slider-prev {
        left: 20px;
        top: 50%;
        transform: translateY(-50%);
        font-size: 25px;
    }

    .slider-next {
        right: 20px;
        top: 50%;
        transform: translateY(-50%);
        font-size: 25px;
    }

    .slider-info {
        position: fixed;
        z-index: 100001;
        left: 50%;
        bottom: 22px;
        transform: translateX(-50%);
        padding: 8px 15px;
        color: #ddd;
        background: rgba(0, 0, 0, 0.65);
        border: 1px solid rgba(255, 255, 255, 0.12);
        border-radius: 999px;
        font-size: 13px;
        white-space: nowrap;
    }

    .slider-loading {
        position: absolute;
        color: #aaa;
        font-size: 13px;
    }


    /* =========================================================
       MOBILE
    ========================================================= */

    @media (max-width: 900px) {

        .container {
            width: min(100% - 28px, var(--max-width));
        }

        .section {
            padding: 55px 0;
        }

        .bento-grid,
        .about-layout,
        .contact-grid {
            grid-template-columns: 1fr;
        }

        .price-grid {
            grid-template-columns: repeat(2, minmax(0, 1fr));
        }

        .masonry-grid {
            columns: 2 220px;
        }

        .about-layout {
            gap: 20px;
        }

        .card-image {
            min-height: 300px;
        }
    }


    @media (max-width: 600px) {

        body {
            font-size: 14px;
        }

        .container {
            width: calc(100% - 24px);
        }

        .section {
            padding: 45px 0;
        }

        .bento-grid {
            gap: 14px;
        }

        .bento-card {
            padding: 22px;
            border-radius: 17px;
        }

        .bento-card h3 {
            font-size: 24px;
        }

        .bento-card p {
            font-size: 14px;
        }

        .folder-nav {
            gap: 8px;
            overflow-x: auto;
            flex-wrap: nowrap;
            padding-bottom: 5px;
            scrollbar-width: none;
        }

        .folder-nav::-webkit-scrollbar {
            display: none;
        }

        .folder-btn {
            flex: 0 0 auto;
            padding: 9px 15px;
            font-size: 13px;
        }

        .masonry-grid {
            columns: 1;
        }

        .port-item {
            margin-bottom: 14px;
            border-radius: 15px;
        }

        .port-overlay {
            padding: 70px 15px 15px;
        }

        .port-title {
            font-size: 17px;
        }

        .port-cat {
            font-size: 10px;
        }

        .price-grid {
            grid-template-columns: 1fr;
            gap: 14px;
            margin-bottom: 35px;
        }

        .price-card {
            padding: 22px;
            border-radius: 17px;
        }

        .price-amount {
            font-size: 29px;
        }

        .about-layout {
            grid-template-columns: 1fr;
        }

        .card-image {
            min-height: 280px;
            order: -1;
        }

        .contact-grid {
            gap: 14px;
        }

        .contact-card {
            padding: 22px;
        }


        /* MOBILE SLIDER */

        .slider-modal {
            padding: 10px;
        }

        .slider-image {
            width: 100%;
            max-width: calc(100vw - 20px);
            max-height: calc(100vh - 120px);
            border-radius: 5px;
        }

        .slider-close {
            top: 12px;
            right: 12px;
            width: 42px;
            height: 42px;
            font-size: 24px;
        }

        .slider-prev,
        .slider-next {
            width: 42px;
            height: 42px;
            top: auto;
            bottom: 55px;
            transform: none;
            font-size: 20px;
        }

        .slider-prev {
            left: 15px;
        }

        .slider-next {
            right: 15px;
        }

        .slider-info {
            bottom: 16px;
            font-size: 11px;
            padding: 6px 11px;
        }
    }
</style>
```

</head>

<body>

```
<main>

    <!-- =====================================================
         FILOSOFI & VISI
    ====================================================== -->

    <section class="section">
        <div class="container">

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
                        tertinggi yang menyentuh hati. Melalui teknik pencahayaan
                        matang, sudut pandang sinematik, dan sentuhan emosional,
                        setiap momen diabadikan bukan sekadar gambar, melainkan
                        sebuah mahakarya abadi.
                    </p>
                </div>

            </div>

        </div>
    </section>


    <!-- =====================================================
         PORTFOLIO
    ====================================================== -->

    <section class="section">
        <div class="container">

            <div class="section-title">
                <span class="section-tag">
                    Portfolio
                </span>

                <h2>
                    Karya Kami
                </h2>

                <p>
                    Dokumentasi berbagai momen yang telah kami abadikan.
                </p>
            </div>


            <div class="folder-nav">

                <button
                    type="button"
                    class="folder-btn active"
                    onclick="filterItems('all')"
                >
                    Semua Folder
                </button>

                <button
                    type="button"
                    class="folder-btn"
                    onclick="filterItems('wedding')"
                >
                    Wedding
                </button>

                <button
                    type="button"
                    class="folder-btn"
                    onclick="filterItems('engagement')"
                >
                    Engagement
                </button>

                <button
                    type="button"
                    class="folder-btn"
                    onclick="filterItems('wisuda')"
                >
                    Wisuda
                </button>

                <button
                    type="button"
                    class="folder-btn"
                    onclick="filterItems('event')"
                >
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
                    ], 'Wedding Falaq & Cindy')"
                >

                    <img
                        src="https://lh3.googleusercontent.com/d/1K5JYuw4FpqSI9NEduRvZNm_8eJRS_Mr2"
                        alt="Wedding Falaq & Cindy"
                        loading="lazy"
                    >

                    <div class="port-overlay">
                        <div class="port-cat">
                            Wedding (9 Foto)
                        </div>

                        <div class="port-title">
                            Falaq &amp; Cindy
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
                    ], 'Engagement Fikry & Reny')"
                >

                    <img
                        src="https://lh3.googleusercontent.com/d/1CSJdaeY-POpOhoytFeI4PyPvCc6_43Jk"
                        alt="Engagement Fikry & Reny"
                        loading="lazy"
                    >

                    <div class="port-overlay">
                        <div class="port-cat">
                            Engagement (13 Foto)
                        </div>

                        <div class="port-title">
                            Fikry &amp; Reny
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
                    ], 'Wisuda Reny Riani')"
                >

                    <img
                        src="https://lh3.googleusercontent.com/d/1tdANeaA_DLSrfHtAXZQQEDzNckCwCl_u"
                        alt="Wisuda Reny Riani"
                        loading="lazy"
                    >

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
                    ], 'Corporate - Jalan Santai Kemerdekaan 2025')"
                >

                    <img
                        src="https://lh3.googleusercontent.com/d/1_axQ1oATs8QwUrEDC56LEWqSs5cwa5LA"
                        alt="Corporate Event"
                        loading="lazy"
                    >

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
         PRICE LIST
    ====================================================== -->

    <section class="section">
        <div class="container">

            <span
                class="section-tag"
                style="color: #fff; margin-bottom: 20px;"
            >
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
                        <li>Full Color Grading &amp; Editing</li>
                        <li>Durasi Fleksibel (Mengikuti Klien)</li>
                        <li>Pengiriman via Google Drive</li>
                    </ul>

                    <a
                        href="https://wa.me/6287765829615"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="btn-outline"
                    >
                        Pilih Paket
                    </a>

                </div>


                <div class="price-card premium">

                    <h3>Premium</h3>

                    <div class="price-amount">
                        Rp 1.500.000
                    </div>

                    <ul class="price-features">
                        <li>1 Fotografer &amp; 1 Videografer</li>
                        <li>Edit Foto + Video Sinematik (Max 5 Menit)</li>
                        <li>Durasi Fleksibel (Mengikuti Klien)</li>
                        <li>Pengiriman via Google Drive</li>
                    </ul>

                    <a
                        href="https://wa.me/6287765829615"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="btn-solid"
                    >
                        Pilih Paket
                    </a>

                </div>

            </div>


            <span
                class="section-tag"
                style="color: #fff; margin-bottom: 20px;"
            >
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
                        class="btn-outline"
                    >
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
                        class="btn-outline"
                    >
                        Pilih Paket
                    </a>

                </div>


                <div class="price-card premium">

                    <h3>Komplit</h3>

                    <div class="price-amount">
                        Rp 850.000
                    </div>

                    <ul class="price-features">
                        <li>1 Fotografer &amp; 1 Videografer</li>
                        <li>Full Edit Foto + Video Sinematik</li>
                        <li>Durasi Fleksibel</li>
                    </ul>

                    <a
                        href="https://wa.me/6287765829615"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="btn-solid"
                    >
                        Pilih Paket
                    </a>

                </div>

            </div>


            <span
                class="section-tag"
                style="color: #fff; margin-bottom: 20px;"
            >
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
                        class="btn-outline"
                    >
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
                        class="btn-outline"
                    >
                        Pilih Paket
                    </a>

                </div>


                <div class="price-card premium">

                    <h3>Pro</h3>

                    <div class="price-amount">
                        Rp 1.000.000
                    </div>

                    <ul class="price-features">
                        <li>Tim Foto &amp; Video (Max 10 Jam)</li>
                        <li>Full Edit + Video Sinematik</li>
                        <li>Waktu ditentukan klien</li>
                    </ul>

                    <a
                        href="https://wa.me/6287765829615"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="btn-solid"
                    >
                        Pilih Paket
                    </a>

                </div>

            </div>

        </div>
    </section>


    <!-- =====================================================
         ABOUT / TENTANG KAMI
    ====================================================== -->

    <section class="section">
        <div class="container">

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
                        Saya mewakili tim dan pendiri PT Another Visual ingin
                        mengucapkan terima kasih sebesar-besarnya kepada seluruh
                        klien, mitra, kru, dan semua pihak yang telah mempercayakan
                        momen berharganya kepada kami.
                    </p>

                    <p>
                        Bagi kami, PT Another Visual bukan hanya tentang foto,
                        video, atau produksi visual. Kami percaya setiap event
                        punya cerita, setiap momen punya makna, dan tugas kami
                        adalah mengabadikannya dengan cara terbaik agar bisa
                        terus dikenang.
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

                    <p
                        style="
                            margin-top: 30px;
                            font-weight: 600;
                            color: #fff;
                        "
                    >
                        Salam hangat,<br>

                        <span
                            style="
                                color: var(--text-muted);
                                font-weight: 400;
                            "
                        >
                            Alif Nur Hidayat — Founder PT Another Visual
                        </span>
                    </p>

                </div>


                <div
                    class="card-image"
                    style="
                        background-image: url('https://lh3.googleusercontent.com/d/1XCVRVaa9RkMXH04tVXUSDGJZN92wRSL9');
                        border-radius: var(--radius-md);
                        background-size: cover;
                        background-position: center;
                        min-height: 300px;
                    "
                ></div>

            </div>

        </div>
    </section>


    <!-- =====================================================
         CONTACT
    ====================================================== -->

    <section class="section">
        <div class="container">

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
                        rel="noopener noreferrer"
                    >
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
                        rel="noopener noreferrer"
                    >
                        @another_visual.id
                    </a>

                </div>

            </div>

        </div>
    </section>

</main>


<!-- =========================================================
     SLIDER MODAL
========================================================== -->

<div
    id="sliderModal"
    class="slider-modal"
    aria-hidden="true"
>

    <div
        class="slider-content"
        id="sliderContent"
    >

        <div
            id="sliderLoading"
            class="slider-loading"
        >
            Memuat foto...
        </div>

        <img
            id="sliderImage"
            class="slider-image"
            src=""
            alt=""
            draggable="false"
        >

    </div>


    <button
        type="button"
        class="slider-close"
        id="sliderClose"
        aria-label="Tutup"
    >
        ×
    </button>


    <button
        type="button"
        class="slider-prev"
        id="sliderPrev"
        aria-label="Foto sebelumnya"
    >
        ‹
    </button>


    <button
        type="button"
        class="slider-next"
        id="sliderNext"
        aria-label="Foto berikutnya"
    >
        ›
    </button>


    <div
        id="sliderInfo"
        class="slider-info"
    >
        1 / 1
    </div>

</div>


<script>
    /* =========================================================
       PORTFOLIO FILTER
    ========================================================= */

    function filterItems(category) {

        const items = document.querySelectorAll(".port-item");
        const buttons = document.querySelectorAll(".folder-btn");

        buttons.forEach(button => {
            button.classList.remove("active");
        });

        const activeButton = Array.from(buttons).find(button => {
            const text = button.textContent.trim().toLowerCase();

            if (category === "all") {
                return text === "semua folder";
            }

            return text === category.toLowerCase();
        });

        if (activeButton) {
            activeButton.classList.add("active");
        }

        items.forEach(item => {

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


    /* =========================================================
       SLIDER VARIABLES
    ========================================================= */

    let sliderImages = [];
    let sliderIndex = 0;
    let sliderTitle = "";

    const sliderModal = document.getElementById("sliderModal");
    const sliderImage = document.getElementById("sliderImage");
    const sliderInfo = document.getElementById("sliderInfo");
    const sliderLoading = document.getElementById("sliderLoading");
    const sliderContent = document.getElementById("sliderContent");

    const sliderClose = document.getElementById("sliderClose");
    const sliderPrev = document.getElementById("sliderPrev");
    const sliderNext = document.getElementById("sliderNext");


    /* =========================================================
       OPEN SLIDER
    ========================================================= */

    function openSlider(images, title = "") {

        if (!Array.isArray(images) || images.length === 0) {
            return;
        }

        sliderImages = images;
        sliderIndex = 0;
        sliderTitle = title;

        sliderModal.classList.add("active");
        sliderModal.setAttribute("aria-hidden", "false");

        document.body.style.overflow = "hidden";

        showSlide(sliderIndex);
    }


    /* =========================================================
       SHOW SLIDE
    ========================================================= */

    function showSlide(index) {

        if (!sliderImages.length) {
            return;
        }

        if (index < 0) {
            index = sliderImages.length - 1;
        }

        if (index >= sliderImages.length) {
            index = 0;
        }

        sliderIndex = index;

        const imageUrl = sliderImages[sliderIndex];

        sliderLoading.style.display = "block";
        sliderImage.style.visibility = "hidden";

        sliderImage.onload = function () {
            sliderLoading.style.display = "none";
            sliderImage.style.visibility = "visible";
        };

        sliderImage.onerror = function () {
            sliderLoading.textContent = "Foto tidak dapat dimuat.";
            sliderImage.style.visibility = "hidden";
        };

        sliderImage.src = imageUrl;

        sliderImage.alt =
            sliderTitle
                ? sliderTitle + " - Foto " + (sliderIndex + 1)
                : "Portfolio Foto " + (sliderIndex + 1);

        sliderInfo.textContent =
            (sliderIndex + 1) + " / " + sliderImages.length;
    }


    /* =========================================================
       NEXT / PREVIOUS
    ========================================================= */

    function nextSlide() {

        if (!sliderImages.length) {
            return;
        }

        showSlide(sliderIndex + 1);
    }


    function prevSlide() {

        if (!sliderImages.length) {
            return;
        }

        showSlide(sliderIndex - 1);
    }


    /* =========================================================
       CLOSE SLIDER
    ========================================================= */

    function closeSlider() {

        sliderModal.classList.remove("active");
        sliderModal.setAttribute("aria-hidden", "true");

        document.body.style.overflow = "";

        setTimeout(() => {
            sliderImage.src = "";
            sliderImages = [];
            sliderIndex = 0;
        }, 250);
    }


    /* =========================================================
       BUTTON EVENTS
    ========================================================= */

    sliderClose.addEventListener("click", function (event) {
        event.stopPropagation();
        closeSlider();
    });


    sliderPrev.addEventListener("click", function (event) {
        event.stopPropagation();
        prevSlide();
    });


    sliderNext.addEventListener("click", function (event) {
        event.stopPropagation();
        nextSlide();
    });


    sliderImage.addEventListener("click", function (event) {
        event.stopPropagation();
    });


    sliderContent.addEventListener("click", function (event) {
        event.stopPropagation();
    });


    /* =========================================================
       CLICK OUTSIDE TO CLOSE
    ========================================================= */

    sliderModal.addEventListener("click", function (event) {

        if (event.target === sliderModal) {
            closeSlider();
        }

    });


    /* =========================================================
       KEYBOARD
    ========================================================= */

    document.addEventListener("keydown", function (event) {

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
            prevSlide();
        }

    });


    /* =========================================================
       MOBILE SWIPE
    ========================================================= */

    let touchStartX = 0;
    let touchStartY = 0;
    let touchEndX = 0;
    let touchEndY = 0;


    sliderContent.addEventListener(
        "touchstart",
        function (event) {

            if (!event.touches || !event.touches.length) {
                return;
            }

            touchStartX = event.touches[0].clientX;
            touchStartY = event.touches[0].clientY;

        },
        { passive: true }
    );


    sliderContent.addEventListener(
        "touchend",
        function (event) {

            if (!event.changedTouches || !event.changedTouches.length) {
                return;
            }

            touchEndX = event.changedTouches[0].clientX;
            touchEndY = event.changedTouches[0].clientY;

            const differenceX = touchEndX - touchStartX;
            const differenceY = touchEndY - touchStartY;

            /*
             * Hanya dianggap swipe apabila gerakan horizontal
             * lebih besar daripada gerakan vertikal.
             */

            if (
                Math.abs(differenceX) > 50 &&
                Math.abs(differenceX) > Math.abs(differenceY)
            ) {

                if (differenceX < 0) {
                    nextSlide();
                } else {
                    prevSlide();
                }

            }

        },
        { passive: true }
    );


    /* =========================================================
       PRELOAD FOTO BERIKUTNYA
    ========================================================= */

    function preloadNextImage() {

        if (!sliderImages.length) {
            return;
        }

        const nextIndex =
            (sliderIndex + 1) % sliderImages.length;

        const image = new Image();
        image.src = sliderImages[nextIndex];
    }


    /* =========================================================
       PRELOAD FOTO SEBELUMNYA
    ========================================================= */

    function preloadPreviousImage() {

        if (!sliderImages.length) {
            return;
        }

        const previousIndex =
            (sliderIndex - 1 + sliderImages.length) %
            sliderImages.length;

        const image = new Image();
        image.src = sliderImages[previousIndex];
    }


    /*
     * Setelah foto selesai dimuat,
     * siapkan foto berikutnya dan sebelumnya.
     */

    sliderImage.addEventListener("load", function () {
        preloadNextImage();
        preloadPreviousImage();
    });
</script>
```

</body>
</html>
