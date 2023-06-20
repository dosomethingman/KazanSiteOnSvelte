<script>
    import "../styles/css/main.css"
    import Navbar from "$lib/components/Navbar.svelte";
    export let data;
</script>

<svelte:head>
    <title>Cайт о Казани</title>
</svelte:head>

<header class="main-header">
    <h1 id="main-h1">Сайт о Казани</h1>
    <Navbar navbarClass="header-navbar" linkClass="header-nav-link" {data} />
</header>

<main>
    <slot />
</main>

<footer>
    <p>Егор Юртаев 2023</p>
</footer>