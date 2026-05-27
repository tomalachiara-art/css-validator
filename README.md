/* Semplice stile per i pulsanti lingua */
@import url('https://fonts.googleapis.com/css2?family=Lora:wght@400;600;700&display=swap');
.lang-switcher {
    display: flex;
    gap: 10px;
    margin-left: 20px;
}
.lang-btn {
    background: none;
    border: 1px solid #fff;
    color: white;
    cursor: pointer;
    padding: 2px 5px;
    font-size: 0.8rem;
}
.lang-btn:hover { background: rgba(255,255,255,0.2); }

/* Layout Strutturale */
:root { --pale: #E4EAE4; --soft: #C3D3C2; --leaf: #B7C9B6; --deep: #33403a; --dark: #33403a; }
* { margin: 0; padding: 0; box-sizing: border-box; }
body { font-family: 'Lora', serif; line-height: 1.6; color: var(--deep); background: var(--pale); }

.navbar { display: flex; align-items: center; padding: 20px 5% 20px 3%; background: var(--soft); border-bottom: 1px solid var(--leaf); position: sticky; top: 0; z-index: 1000; }
.logo { margin-right: 20px; }
.logo img { display: block; max-height: 58px; width: auto; }
.nav-toggle { display: none; border: 1px solid var(--deep); background: none; color: var(--deep); padding: 8px 12px; border-radius: 4px; cursor: pointer; font-size: 1rem; }
.nav-links { display: flex; list-style: none; position: relative; flex: 1; justify-content: space-around; }
.nav-links a { text-decoration: none; color: var(--deep); font-weight: bold; }

/* Dropdown menu */
.dropdown { position: relative; }
.dropbtn { background: none; border: 1px solid var(--deep); color: var(--deep); padding: 8px 12px; cursor: pointer; border-radius: 4px; display: inline-flex; align-items: center; gap: 6px; }
.dropbtn::before { content: "☰"; font-size: 1rem; }
.dropdown-content { display: none; position: absolute; right: 0; top: 100%; background: white; min-width: 240px; box-shadow: 0 8px 16px rgba(0,0,0,0.2); padding: 12px; z-index: 1001; border: 1px solid var(--leaf); border-radius: 8px; opacity: 0; transform: translateY(-6px); transition: opacity .25s ease, transform .25s ease; }
.dropdown-content.show { display: block; opacity: 1; transform: translateY(0); }
.dropdown-content a { display: block; padding: 8px 10px; text-decoration: none; color: var(--deep); border-radius: 4px; margin-bottom: 6px; }
.dropdown-content a:hover { background: var(--pale); }
.dropdown-divider { border-top: 1px solid var(--leaf); margin: 8px 0; }
.dropdown-lang { display: flex; justify-content: space-around; gap: 6px; padding-top: 6px; }
.dropdown:hover .dropdown-content, .dropdown:focus-within .dropdown-content { display: block; }
.lang-btn { background: none; border: 1px solid #fff; color: white; cursor: pointer; padding: 2px 5px; font-size: 0.8rem; }
.lang-btn:hover { background: rgba(255,255,255,0.2); }

/* Override dropdown language button colors */
.dropdown-lang .lang-btn { border-color: var(--deep); color: var(--deep); }
.dropdown-lang .lang-btn:hover { background: rgba(51,64,58,0.1); }

/* overlay mobile */
.mobile-overlay { display: none; position: fixed; inset: 0; background: rgba(0,0,0,0.35); z-index: 900; opacity: 0; transition: opacity .25s ease; pointer-events: none; }
.mobile-overlay.show { display: block; opacity: 1; pointer-events: auto; }

/* Responsive navbar */
@media (max-width: 768px) {
    .navbar { padding: 15px 5%; }
    .nav-toggle { display: block; }
    .nav-links { position: fixed; top: 0; left: 0; right: 0; z-index: 1002; width: 100%; background: var(--soft); flex-direction: column; display: none; border-bottom: 1px solid var(--leaf); padding: 70px 10px 20px; max-height: calc(100vh - 70px); overflow-y: auto; }
    .nav-links.show { display: flex; }
    .nav-links li { margin: 10px 0; }
    .dropbtn { width: 100%; justify-content: flex-start; }
    .dropdown-content { position: static; width: 100%; box-shadow: none; border: none; background: transparent; padding: 0; }
    .dropdown-content a { background: var(--soft); margin-bottom: 6px; }
    .dropdown-divider { display: none; }
    .dropdown-lang { flex-wrap: wrap; background: var(--soft); margin-top: 6px; }
}


.hero {
    height: 80vh;
   background-image: linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.45)),
   url('DSC6169.png');
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: white;
}


.hero-content {
    max-width: 600px;
}

.btn {
    display: inline-block;
    padding: 12px 30px;
    background: var(--deep);
    color: white;
    text-decoration: none;
    margin-top: 20px;
    border-radius: 5px;
    cursor: pointer;
    transition: background 0.3s ease;
}

.btn:hover {
    background: var(--leaf);
}

.menu, #storia, #prenota, #contatti {
    padding: 60px 5%;
}
.menu-container, .reservation-container, .contact-container, .menu-container {
    max-width: 1200px;
    margin: 0 auto;
}
.menu-items { display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 25px; }
.reservation-container, .contact-container { text-align: left; }
.reservation-container h2, .contact-container h2, #storia h2 { text-align: left; }
.reservation-container p, .contact-container p { margin-bottom: 12px; line-height: 1.7; }

.menu-section-title { width: 100%; grid-column: 1 / -1; margin: 40px 0 20px; text-align: center; color: var(--dark); font-size: 2em; text-transform: uppercase; letter-spacing: 2px; border-bottom: 2px solid var(--leaf); }

.menu-item { background: var(--soft); padding: 20px; border-radius: 8px; border: 1px solid var(--leaf); box-shadow: 0 2px 8px rgba(0,0,0,0.05); }

/* Stili specifici per la sezione storia */
#storia .menu-item {
    background: var(--soft);
    padding: 30px;
    border-radius: 12px;
    border: 1px solid var(--leaf);
    box-shadow: 0 2px 8px rgba(0,0,0,0.08);
}

#storia h3 {
    margin-top: 24px;
    margin-bottom: 8px;
    font-size: 1.4rem;
    color: var(--dark);
}

#storia p {
    line-height: 1.8;
    margin-bottom: 8px;
}

/* FORM PRENOTA – versione elegante */
.reservation {
    background: var(--soft);
    padding: 60px 5%;
    border-top: 1px solid var(--leaf);
    border-bottom: 1px solid var(--leaf);
}

.reservation-container {
    max-width: 700px;
    margin: 0 auto;
    background: white;
    padding: 40px;
    border-radius: 12px;
    box-shadow: 0 4px 14px rgba(0,0,0,0.08);
    border: 1px solid var(--leaf);
}

.reservation-container h2 {
    text-align: center;
    margin-bottom: 20px;
    color: var(--dark);
}

.reservation-container p {
    margin-bottom: 10px;
    line-height: 1.7;
}

#reservationForm {
    margin-top: 25px;
    display: flex;
    flex-direction: column;
    gap: 18px;
}

#reservationForm label {
    font-weight: bold;
    color: var(--dark);
}

#reservationForm input,
#reservationForm textarea {
    padding: 12px;
    border-radius: 6px;
    border: 1px solid var(--leaf);
    background: var(--pale);
    font-size: 1rem;
}

#reservationForm button {
    margin-top: 10px;
    width: 100%;
}

/* Contenitori prenotazione e contatti */
.reservation-container,
.contact-container {
    max-width: 1200px;
    margin: 0 auto;
}

/* Griglia informativa per orari/indirizzo/contatti */
.info-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 30px;
    margin-top: 30px;
}

.info-box {
    background: var(--soft);
    padding: 20px;
    border-radius: 10px;
    border: 1px solid var(--leaf);
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
}

.info-box h3 {
    margin-bottom: 10px;
    color: var(--dark);
}

.info-box p {
    margin-bottom: 6px;
    line-height: 1.7;
}

.menu-item h3 { color: var(--dark); margin-bottom: 15px; border-bottom: 1px solid var(--deep); font-size: 1.4em; }

.dish { display: flex; justify-content: space-between; padding: 8px 0; border-bottom: 1px solid rgba(87,105,87,0.2); align-items: center; }
.dish:last-child { border-bottom: none; }
.dish-name { font-size: 0.95em; flex: 1; padding-right: 15px; }
.price { font-weight: bold; color: var(--dark); min-width: 50px; text-align: right; }

footer { text-align: center; padding: 40px; background: var(--soft); margin-top: 50px; }

/* Bottoni tondi */
.circle-btn {
    width: 50px;
    height: 50px;
    background: var(--deep);
    color: white;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 22px;
    text-decoration: none;
    border: 2px solid var(--leaf);
    transition: background 0.2s ease, transform 0.2s ease;
}

.circle-btn:hover {
    background: var(--leaf);
    transform: scale(1.1);
}

/* Sticky orizzontale (visibile solo in alto) */
.sticky-top {
    position: sticky;
    top: 10px;
    display: flex;
    gap: 10px;
    justify-content: center;
    z-index: 3000;
    padding-top: 10px;
    opacity: 1;
    transition: opacity 0.3s ease;
}

/* Sticky verticale (inizialmente nascosto) */
.sticky-side {
    position: fixed;
    right: 30px;
    bottom: 90px;
    display: flex;
    flex-direction: column;
    gap: 12px;
    z-index: 3000;
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.3s ease;
}

/* Quando scrolli */
body.scrolled .sticky-top {
    opacity: 0;
    pointer-events: none;
}

body.scrolled .sticky-side {
    opacity: 1;
    pointer-events: auto;
}


/* MOBILE */
@media (max-width: 768px) {

    /* Nascondi dropdown desktop */
    .dropdown {
        display: none !important;
    }

    /* Mostra hamburger */
    .nav-toggle {
        display: block !important;
        margin-left: auto;
        font-size: 1.8rem;
        background: none;
        border: none;
        cursor: pointer;
    }

    /* Menu mobile */
    .nav-links {
        position: fixed;
        top: 0;
        right: 0;
        width: 70%;
        height: 100vh;
        background: var(--soft);
        flex-direction: column;
        padding: 80px 20px 20px;
        gap: 20px;
        display: none;
        z-index: 2000;
        border-left: 1px solid var(--leaf);
    }

    .nav-links.show {
        display: flex;
    }

    /* Lingue in fondo */
    .lang-row {
        margin-top: auto;
        padding-top: 15px;
        border-top: 1px solid var(--leaf);
        display: flex;
        gap: 10px;
    }

    /* Mostra lingue solo su mobile */
    .mobile-only {
        display: flex !important;
    }
}

/* Desktop: nascondi lingue mobile */
@media (min-width: 769px) {
    .mobile-only {
        display: none !important;
    }
}


    


/* Scroll to Top Button */
#scrollToTopBtn {
    display: none;
    position: fixed;
    bottom: 20px;
    right: 30px;
    z-index: 99;
    font-size: 18px;
    border: none;
    outline: none;
    background-color: var(--deep);
    color: white;
    cursor: pointer;
    padding: 0;
    border-radius: 50%;
    width: 50px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
}

#scrollToTopBtn:hover {
    background-color: var(--leaf);
}
