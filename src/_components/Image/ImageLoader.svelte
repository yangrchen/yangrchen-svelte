<script>
    export let img_props;
    export let className = "";
    import IntersectionObserver from "./IntersectionObserver.svelte";
    import Image from "./Image.svelte";
    import { onMount } from "svelte";

    let nativeLoading = false;

    onMount(() => {
        if ("loading" in HTMLImageElement.prototype) {
            nativeLoading = true;
        }
    });
</script>

<IntersectionObserver once={true} let:intersecting>
    {#if intersecting || nativeLoading}
        <Image {img_props} {className} />
    {/if}
</IntersectionObserver>
