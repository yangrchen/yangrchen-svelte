<script>
    import { isActive, url, layout } from "@roxi/routify";
    let routes = [
        ["/index", "about"],
        ["/artwork", "artwork"],
        ["/resume", "resume"],
    ];
</script>

<nav class="flex flex-col items-center sticky top-0 p-2">
    <a href={$url("/")} class="text-3xl md:text-5xl">YANG CHEN</a>
    <ul class="flex space-x-4 md:text-2xl">
        {#each routes as [path, name]}
            <li
                class:underline={$isActive(path)}
                class="hover:underline decoration-pink-300"
            >
                {#if path == "/artwork"}
                    <a href={$url(path + "/drawings")}>{name}</a>
                {:else}
                    <a href={$url(path)}>{name}</a>
                {/if}
            </li>
        {/each}
    </ul>
</nav>

<style>
    @import url("https://fonts.googleapis.com/css2?family=Martel+Sans:wght@200&display=swap");
    nav {
        background-color: #f2f2f2;
    }
    nav > a {
        font-family: "Martel Sans", sans-serif;
    }
</style>
