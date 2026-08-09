<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Another Visual | JKT Creative Agency</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css?family=Outfit:wght@300;500;700;900&family=Plus+Jakarta+Sans:wght@400;500;600&display=swap" rel="stylesheet">
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
nav a:hover { 
    color: var(--text-main); 
}
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
.page.active { 
    display: block; 
}
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
.bento-card h3 { 
    font-size: 32px; 
    font-weight: 500; 
    margin-bottom: 15px; 
}
.bento-card p { 
    color: var(--text-muted); 
    font-size: 16px; 
    line-height: 1.7; 
}

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
.hero h1 span { 
    color: var(--text-muted); 
    font-weight: 300; 
}
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
.port-item:hover img { 
    transform: scale(1.05); 
}
.port-item:hover .port-overlay { 
    opacity: 1; 
}
.port-cat { 
    color: var(--text-muted); 
    font-size: 13px; 
    text-transform: uppercase; 
    letter-spacing: 1px; 
}
.port-title { 
    font-family: 'Outfit', sans-serif; 
    font-size: 28px; 
    font-weight: 500; 
}

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
.slide-btn:hover { 
    background: var(--accent); 
    color: var(--bg-base); 
}
.prev-btn { left: -70px; }
.next-btn { right: -70px; }
.close-modal { 
    position: absolute; 
    top: -60px; 
    right: 0; 
    color: #fff; 
    font-size: 40px; 
    cursor: pointer; 
    font-family: 'Outfit'; 
}

/* PRICELIST */
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
.price-card h3 { 
    font-size: 2
    
