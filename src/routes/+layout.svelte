<script>
    let isMenuOpen = false;

    function toggleMenu() {
        isMenuOpen = !isMenuOpen;
    }

    function closeMenu() {
        isMenuOpen = false;
    }
</script>

<header>
    <nav class="navbar">
        <div class="logo">
            <a href="/" on:click={closeMenu}>Game Lambs</a>
        </div>

        <!-- Hamburger icon per dispositivi mobili -->
        <div class="hamburger" on:click={toggleMenu}>
            <div class="line"></div>
            <div class="line"></div>
            <div class="line"></div>
        </div>

        <!-- Menu navigazione -->
        <ul class="nav-links {isMenuOpen ? 'open' : ''}">
            <li><a href="/" on:click={closeMenu}>Home</a></li>
            <li><a href="/games" on:click={closeMenu}>Giochi</a></li>
            <li><a href="/about" on:click={closeMenu}>About</a></li>
        </ul>
    </nav>
</header>

<main>
    <div class="top">
        <slot />
    </div>
</main>

<style>
    /* Assicurarsi che body e html occupino l'intera finestra */
    body,
    html {
        margin: 0;
        padding: 0;
        height: 100%;
        overflow: hidden;
        /* font-family: "Poppins", sans-serif; */
        /* font-family: "Baloo 2", cursive; */
    }

    /* Aggiungere l'immagine di sfondo con overlay e blur */
    main::before {
        content: "";
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: url("/images/game_lambs_04.webp");
        background-size: cover;
        background-position: center;
        filter: blur(7px);
        z-index: -2;
    }

    /* Aggiungere un overlay semi-trasparente */
    main::after {
        content: "";
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.6);
        z-index: -1;
    }

    .top {
        position: fixed;
        top: 90px;
        left: 0;
        z-index: 3;
        border: 2px solid yellow;
        width: 100%;
        margin-top: 10px;
        height: 85vh;
    }

    /* Assicurarsi che il contenuto principale sia leggibile e visibile sopra tutto */
    main {
        position: relative;
        z-index: 1;
        padding: 5rem;
        color: white;
        height: calc(100vh - 20rem);
        /* display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center; */
        /* overflow: hidden; */
        font-family: "Baloo 2", cursive;
    }

    /* Stili per l'header */
    header {
        background-color: #e45a33; /* Arancione dalla palette */
        padding: 1rem;
        color: white;
        width: calc(100vw - 2rem); /* L'header occupa tutta la larghezza */
        position: absolute;
        top: 0;
        left: 0;
        z-index: 2; /* Assicurarsi che l'header sia sopra l'overlay */
    }

    .navbar {
        display: flex;
        justify-content: space-between;
        align-items: center;
        font-weight: bolder;
    }

    .logo a {
        font-size: 1.8rem;
        font-family: "Baloo 2", cursive;
        color: white;
        text-decoration: none;
    }

    /* Menu navigazione */
    .nav-links {
        display: flex;
        list-style: none;
        gap: 1.5rem;
        margin-right: 1rem;
        font-family: "Baloo 2", cursive;
    }

    .nav-links li a {
        color: white;
        text-decoration: none;
        font-size: 1.2rem;
        font-weight: bold;
    }

    .nav-links li a:hover {
        color: #2f5597; /* Giallo per hover */
    }

    /* Hamburger icon */
    .hamburger {
        display: none;
        flex-direction: column;
        cursor: pointer;
        gap: 5px;
    }

    .hamburger .line {
        width: 25px;
        height: 3px;
        background-color: white;
    }

    /* Menu aperto per mobile */
    .nav-links.open {
        display: block;
        position: absolute;
        top: 62px;
        right: 0;
        background-color: rgba(0, 0, 0, 0.8);
        width: 100%;
        padding: 1rem 2rem;
        text-align: right;
    }

    .nav-links.open li {
        margin-bottom: 1rem;
    }

    /* Responsività */
    @media (max-width: 768px) {
        .nav-links {
            display: none;
            flex-direction: column;
        }

        .hamburger {
            display: flex;
        }
    }
</style>
