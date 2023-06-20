<script>
    export let data;
</script>

<article class="main-article">
    {#each data.post.paragraphs as par}
        {#if par.imgSrc}
            <div class="img-container">
                <img src="{ par.imgSrc }" class="par-img" alt="{ par.imgLabel }">
                {#if par.imgLabel}
                    <span class="img-label">{ par.imgLabel }</span>
                {/if}
            </div>
        {/if}
        {#if par.title}
            <h1>{ par.title }</h1>
        {/if}
        {#if par.text}
            <p>{ par.text }</p>
        {/if}
        <hr class="paragraph-hr">
    {/each}
</article>