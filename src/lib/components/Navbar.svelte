<script>
    export let navbarClass;
    export let linkClass;
    export let data;
</script>

<nav class="{ navbarClass }">
    <a href="/" class="homepage-link">&#127968;</a>
    <!--<a href="#" class="header-nav-link">история</a>
    <a href="#" class="header-nav-link">достопримечательности</a>
    <a href="#" class="header-nav-link">учебные заведения</a>
    <a href="#" class="header-nav-link">отдых</a>-->
    {#each data.summaries as { slug, title }}
        <a href="./{ slug }" class="{ linkClass }">{ title }</a>
    {/each}
</nav>