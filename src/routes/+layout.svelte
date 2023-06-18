<script>
    import "../styles/css/main.css"
    export let data;
</script>

<svelte:head>
    <title>Главная страница</title>
</svelte:head>

<header class="main-header">
    <h1 id="main-h1">Сайт о Казани</h1>
    <nav class="header-navbar">
        <!--<a href="#" class="header-nav-link">история</a>
        <a href="#" class="header-nav-link">достопримечательности</a>
        <a href="#" class="header-nav-link">учебные заведения</a>
        <a href="#" class="header-nav-link">отдых</a>-->
        {#each data.summaries as { slug, title }}
            <a href="./{ slug }" class="header-nav-link">{ title }</a>
        {/each}
    </nav>
</header>

<main>
    <slot />
</main>

<footer>
    <p>Егор Юртаев 2023</p>
</footer>