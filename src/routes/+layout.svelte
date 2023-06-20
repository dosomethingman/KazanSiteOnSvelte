<script>
    import "../styles/css/main.css"
    import Navbar from "$lib/components/Navbar.svelte";
    import MediaQuery from 'svelte-media-queries';
    import ShowNavbarBtn from '$lib/components/ShowNavbarBtn.svelte';

    export let data;
    const lowResMaxWidth = "520px";
    let navbarUnfolded = false;
</script>

<svelte:head>
    <title>Cайт о Казани</title>
</svelte:head>

<header class="main-header">
    <h1 id="main-h1">Сайт о Казани</h1>
    <MediaQuery query="(max-width: { lowResMaxWidth })" let:matches>
        {#if !matches}
            <Navbar navbarClass="header-navbar" linkClass="header-nav-link" homepageLinkClass="homepage-link" {data} />
        {:else}
            <div class="button-container" on:click={ () => {navbarUnfolded = !navbarUnfolded;}}>
                <ShowNavbarBtn/>
            </div>
        {/if}
    </MediaQuery>
</header>

<MediaQuery query="(max-width: { lowResMaxWidth })" let:matches>
    {#if matches}
        <Navbar navbarClass="{navbarUnfolded ? "navbar-low-res-unfolded" : "navbar-low-res"}" linkClass="nav-link-low-res" homepageLinkClass="homepage-link-low-res" {data} />
    {/if}
</MediaQuery>

<main>
    <slot />
</main>

<footer>
    <p>Егор Юртаев 2023. Источники: Интернет, Википедия</p>
</footer>