<script>
    import drawings from "../../lib/data/drawings.json";
    import IntersectionObserverArtImage from "../../_components/IntersectionObserverArtImage.svelte";
    import Image from "../../_components/Image.svelte";

    let imgLoad = () => {};
</script>

{#each drawings as imgProps}
    <IntersectionObserverArtImage>
        <Image {imgProps} />
    </IntersectionObserverArtImage>
{/each}
