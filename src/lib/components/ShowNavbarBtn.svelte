<script>
    let isUnfolded = false;
    let button;

    const unfold = () => {
        isUnfolded = !isUnfolded;
        console.log(isUnfolded);
    };
</script>

<button class="{isUnfolded ? 'bar-unfolded' : 'side-button'}" bind:this={ button } on:click={ unfold }>
    <div class="bar" id="bar1"></div>
    <div class="bar" id="bar2"></div>
    <div class="bar" id="bar3"></div>
</button>