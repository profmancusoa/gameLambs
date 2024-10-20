<script>
    // Logica per la Home Page
</script>

<section class="hero">
    <h1>Benvenuti su Game Lambs!</h1>
    <p>
        Imparare JavaScript divertendosi, attraverso lo sviluppo di giochi
        interattivi.
    </p>
    <!-- Pulsante per accedere alla pagina Giochi -->
    <a href="/games" class="cta-button">Vai ai Giochi</a>
</section>

<style>
    /* Sezione Hero */
    .hero {
        border: 12px solid green;
        text-align: center;
        padding: 2rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 80vh; /* Occupa tutta la finestra */
        position: relative;
        z-index: 1; /* Contenuto sopra lo sfondo */
    }

    .hero h1 {
        font-size: 6rem;
        color: #f39c12; /* Giallo brillante della palette */
        margin-bottom: 1rem;
    }

    .hero p {
        font-size: 2rem;
        color: white;
        max-width: 800px;
    }

    /* Stile del pulsante */
    .cta-button {
        margin-top: 2rem;
        padding: 1rem 2rem;
        background-color: #f39c12; /* Giallo dalla palette */
        color: white;
        font-size: 1.5rem;
        font-weight: bold;
        text-decoration: none;
        border-radius: 5px;
        transition: background-color 0.3s ease;
    }

    .cta-button:hover {
        background-color: #e45a33; /* Arancione per hover */
    }

    /* Responsività per schermi più piccoli */
    @media (max-width: 768px) {
        .hero h1 {
            font-size: 3.5rem; /* Riduce la dimensione del titolo su mobile */
        }
        .hero p {
            font-size: 1.5rem;
        }
        .cta-button {
            font-size: 1.2rem; /* Riduce la dimensione del pulsante su mobile */
        }
    }

    /* Sfondo */
    body,
    html {
        margin: 0;
        padding: 0;
        height: 100%;
        overflow: hidden;
        font-family: "Poppins", sans-serif;
    }

    /* Immagine di sfondo con effetto blur */
    body::before {
        content: "";
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: url("/images/game_lambs_04.webp"); /* Usa l'immagine di sfondo */
        background-size: cover;
        background-position: center;
        filter: blur(15px); /* Applicare l'effetto blur */
        z-index: -2; /* Mettere l'immagine dietro tutto */
    }

    /* Overlay per migliorare la leggibilità */
    body::after {
        content: "";
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5); /* Overlay semi-trasparente */
        z-index: -1; /* Overlay sopra l'immagine di sfondo */
    }
</style>
