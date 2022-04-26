<script>
    import { isActive, url, layout, meta, metatags } from "@roxi/routify";
    let routes = [
        ["./drawings", "drawings"],
        ["./digital", "digital art"],
        ["./graphic", "graphic design"],
    ];
</script>

<nav class="pt-2 self-center">
    <ul class="flex space-x-6">
        {#each routes as [path, name]}
            <li>
                <a
                    href={$url(path)}
                    class="underline hover:decoration-pink-300"
                    class:decoration-gray-400={!$isActive(path)}
                    class:decoration-pink-300={$isActive(path)}>{name}</a
                >
            </li>
        {/each}
    </ul>
</nav>
<!-- <p class="self-center mt-8">Coming soon!</p> -->
<div
    class="mt-6 flex flex-col space-y-6 md:space-y-30 justify-center place-items-center lg:grid lg:gap-y-20 lg:grid-cols-2 2xl:grid-cols-3 lg:space-y-0"
>
    <slot />
</div>
