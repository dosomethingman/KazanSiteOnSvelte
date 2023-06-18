<script>
    export let data;
</script>

<svelte:head>
    <title>{data.post.mainTitle}</title>
</svelte:head>

<article class="main-article">
    {#each data.post.paragraphs as par}
        {#if par.imgSrc}
            <img src="{ par.imgSrc }" class="par-img">
        {/if}
        {#if par.title}
            <h1>{ par.title }</h1>
        {/if}
        {#if par.text}
            <p>{ par.text }</p>
        {/if}
        <hr>
    {/each}
</article>