<script>
    // Dati dei giochi. In un'applicazione reale potresti caricarli dinamicamente
    const games = [
        {
            id: "snake",
            title: "Snake Game",
            description: "Il classico gioco Snake.",
            image: "/images/snake.png",
        },
        {
            id: "tic-tac-toe",
            title: "Tic Tac Toe",
            description: "Sfida i tuoi amici a Tic Tac Toe!",
            image: "/images/snake.png",
        },
        {
            id: "memory",
            title: "Memory Game",
            description: "Allenati con il gioco del memory.",
            image: "/images/snake.png",
        },
        {
            id: "asteroids",
            title: "Asteroids",
            description: "Distruggi gli asteroidi nello spazio.",
            image: "/images/snake.png",
        },
        {
            id: "pong",
            title: "Pong",
            description: "Gioca a Ping Pong classico!",
            image: "/images/snake.png",
        },
        {
            id: "breakout",
            title: "Breakout",
            description: "Distruggi i mattoni con la pallina.",
            image: "/images/snake.png",
        },
    ];
</script>

<section class="games-grid">
    {#each games as game}
        <div class="game-card">
            <a href={`/games/${game.id}`}>
                <img src={game.image} alt={game.title} class="game-image" />
            </a>
            <h3><a href={`/games/${game.id}`}>{game.title}</a></h3>
            <p>{game.description}</p>
        </div>
    {/each}
</section>

<style>
    /* Sezione per la griglia dei giochi */
    .games-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr); /* Griglia 3 colonne */
        gap: 2rem;
        padding: 2rem;
    }

    .game-card {
        background-color: white;
        padding: 1rem;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        text-align: center;
        transition: transform 0.3s;
    }

    .game-card:hover {
        transform: scale(1.05); /* Effetto di zoom sul hover */
    }

    .game-image {
        width: 100%;
        height: 200px;
        object-fit: cover;
        border-radius: 8px;
    }

    .game-card h3 {
        margin: 1rem 0;
        font-size: 1.5rem;
        color: #e45a33; /* Arancione dalla palette */
    }

    .game-card p {
        font-size: 1rem;
        color: #555;
    }

    /* Responsività: Regola la griglia su schermi più piccoli */
    @media (max-width: 1024px) {
        .games-grid {
            grid-template-columns: repeat(2, 1fr); /* 2 colonne su tablet */
        }
    }

    @media (max-width: 768px) {
        .games-grid {
            grid-template-columns: 1fr; /* 1 colonna su smartphone */
        }
    }
</style>
