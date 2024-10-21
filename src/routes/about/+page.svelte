<section class="about">
    <h1>About Game Lambs</h1>
    <p>
        Game Lambs è un progetto dedicato all'insegnamento di JavaScript
        attraverso lo sviluppo di giochi interattivi. Il nostro obiettivo è
        rendere l'apprendimento del codice divertente e coinvolgente per tutti
        gli studenti.
    </p>
</section>

<style>
    .about {
        width: 60%;
        height: 80vh;
        margin: auto;
        text-align: center;
        padding: 2rem;
        font-size: 3rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .about h1 {
        color: #f39c12;
    }

    .about p {
        font-size: 2rem;
        line-height: 1.6;
        color: white;
    }

    /* Responsività */
    @media (max-width: 768px) {
        .about {
            padding: 0.5rem;
            font-size: 1.9rem;
        }

        .about p {
            font-size: 1.5rem;
            line-height: 1.6;
        }
    }
</style>
