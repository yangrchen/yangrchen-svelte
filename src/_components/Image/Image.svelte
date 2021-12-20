<script>
    export let src;
    export let alt;
    export let className = "";

    import { onMount } from "svelte";

    let loaded = false;
    let thisImage;

    onMount(() => {
        thisImage.onload = () => {
            loaded = true;
        };
    });
</script>

<img
    {src}
    {alt}
    class:loaded
    class={className}
    bind:this={thisImage}
    loading="lazy"
/>

<style>
    img {
        opacity: 0;
        transition: opacity 1000ms ease-out;
    }
    img.loaded {
        opacity: 1;
    }
</style>
