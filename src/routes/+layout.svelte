<header>
    <nav class="navbar">
        <div class="logo">
            <a href="/">Game Lambs</a>
        </div>

        <ul class="nav-links">
            <li><a href="/">Home</a></li>
            <li><a href="/games">Giochi</a></li>
            <li><a href="/about">About</a></li>
        </ul>
    </nav>
</header>

<main>
    <slot />
</main>

<style>
    :global(body) {
        background-image: url("/images/game_lambs_04.webp");
        background-size: cover;
    }

    main {
        height: calc(100vh - 60px - 20px - 20px);
    }

    header {
        background-color: #e45a33;
        padding: 10px;
        color: white;
        height: 60px;
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
        color: #2f5597;
    }

    @media (max-width: 768px) {
        .nav-links {
            display: none;
        }
    }
</style>
