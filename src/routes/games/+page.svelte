<script>
    // Dati dei giochi. In un'applicazione reale potresti caricarli dinamicamente
    const games = [
        {
            id: "tris",
            title: "Tris",
            description: "Il classico gioco del tris.",
            image: "/images/tris.png",
            url: "https://tris.mancusoa.it",
            github: "",
        },
        {
            id: "tetris",
            title: "Tetris",
            description: "Il classico gioco del tetris.",
            image: "/images/tetris.png",
            url: "https://tetris.mancusoa.it",
            github: "",
        },
        {
            id: "parole",
            title: "pArole",
            description: "Il classico gioco Wordle.",
            image: "/images/parole.png",
            url: "https://parole.mancusoa.it",
            github: "https://github.com/profmancusoa/pArole",
        },
        {
            id: "bitfinder",
            title: "Bit Finder",
            description: "Sfida i tuoi amici in binario",
            image: "/images/bitfinder.png",
            url: "https://bitfinder.mancusoa.it",
            github: "https://github.com/profmancusoa/BitFinder",
        },
        {
            id: "colorclash",
            title: "Color Clash",
            description: "Divertente Tile Game",
            image: "/images/colorclash.png",
            url: "https://colorclash.mancusoa.it",
            github: "https://github.com/profmancusoa/ColorClash",
        },
        {
            id: "labirinto",
            title: "Labirinto",
            description: "Trova la via giusta per l'uscita",
            image: "/images/labirinto.png",
            url: "https://labirinto.mancusoa.it",
            github: "https://github.com/profmancusoa/labirinto",
        },
        {
            id: "2048",
            title: "2048s",
            description: "Realizza 2048 punti",
            image: "/images/2048.png",
            url: "https://2048.mancusoa.it",
            github: "https://github.com/profmancusoa/2048s",
        },
        {
            id: "sudoko",
            title: "Sudoko Solver",
            description: "Risolvi qualsiasi Sudoko",
            image: "/images/sudoko.png",
            url: "https://sudoko.mancusoa.it",
            github: "https://github.com/profmancusoa/Sudoko_Solver",
        },
    ];
</script>

<section class="games-grid">
    {#each games as game}
        <div class="game-card">
            <a href={game.url} target="_blank">
                <img src={game.image} alt={game.title} class="game-image" />
            </a>
            <h3>
                <a href={game.github} target="_blank">GitHub</a>
            </h3>

            <p>{game.description}</p>
        </div>
    {/each}
</section>

<style>
    /* Sezione per la griglia dei giochi */
    .games-grid {
        display: grid;
        grid-template-columns: repeat(4, 1fr); /* Griglia 3 colonne */
        gap: 5rem;
        padding: 2rem;
        margin: auto;
        height: 80vh;
        width: 80%;
    }

    .game-card {
        background-color: #f39c12;
        padding: 1rem;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
        text-align: center;
        transition: transform 0.3s;
    }

    .game-card:hover {
        transform: scale(1.05);
    }

    .game-image {
        width: 200px;
        height: 200px;
        object-fit: cover;
        border-radius: 8px;
    }

    .game-card h3 {
        margin: 1rem 0;
        font-size: 1.5rem;
    }

    .game-card h3 a {
        color: white;
    }

    .game-card p {
        font-size: 1.1rem;
        color: #444;
    }

    /* Responsività: Regola la griglia su schermi più piccoli */
    @media (max-width: 1024px) {
        .games-grid {
            grid-template-columns: repeat(2, 1fr);
        }
    }

    @media (max-width: 768px) {
        .games-grid {
            grid-template-columns: 1fr;
        }

        .game-card {
            background-color: #f39c12;
            padding: 1rem;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
            text-align: center;
            transition: transform 0.3s;
            margin: auto;
            width: 50vw;
        }

        .game-image {
            width: 150px;
            height: 150px;
            object-fit: cover;
            border-radius: 8px;
        }
    }
</style>
