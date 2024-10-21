<section class="hero">
    <h1>Benvenuti su Game Lambs!</h1>
    <p>
        Imparare JavaScript divertendosi, attraverso lo sviluppo di giochi
        interattivi.
    </p>
    <a href="/games" class="cta-button">Vai ai Giochi</a>
</section>

<style>
    .hero {
        text-align: center;
        padding: 2rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 80vh;
        position: relative;
        z-index: 1;
    }

    .hero h1 {
        font-size: 6rem;
        color: #f39c12;
        margin-bottom: 1rem;
    }

    .hero p {
        font-size: 2rem;
        color: white;
        max-width: 800px;
    }

    .cta-button {
        margin-top: 2rem;
        padding: 1rem 2rem;
        background-color: #f39c12;
        color: white;
        font-size: 1.5rem;
        font-weight: bold;
        text-decoration: none;
        border-radius: 5px;
        transition: background-color 0.3s ease;
    }

    .cta-button:hover {
        background-color: #e45a33;
    }

    @media (max-width: 768px) {
        .hero h1 {
            font-size: 3.5rem;
        }
        .hero p {
            font-size: 1.5rem;
        }
        .cta-button {
            font-size: 1.2rem;
        }
    }
</style>
