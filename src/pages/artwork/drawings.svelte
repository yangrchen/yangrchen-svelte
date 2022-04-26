<script>
    import drawings from "../../lib/data/drawings.json";
    import IntersectionObserverArtImage from "../../_components/IntersectionObserverArtImage.svelte";
</script>

{#each drawings as img_props}
    <IntersectionObserverArtImage>
        <img {...img_props} decoding="sync" />
    </IntersectionObserverArtImage>
{/each}

<style>
    img {
        min-height: 30vh;
        width: auto;
        height: 100%;
        opacity: 0;
        transition: opacity 1200ms ease-out;
    }
    img.loaded {
        opacity: 1;
    }
</style>
