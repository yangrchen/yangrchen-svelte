<script>
    import { isActive, url, layout } from "@roxi/routify";
</script>

<nav class="flex flex-col items-center sticky top-0 p-2">
    <a href={$url("/")} class="text-3xl md:text-5xl">YANG CHEN</a>
    <ul class="flex space-x-4 md:text-2xl">
        <li
            class:underline={$isActive("/index")}
            class="hover:underline decoration-pink-300"
        >
            <a href={$url("/")}>about</a>
        </li>
        {#each $layout.children as { path, title }}
            <li class:underline={$isActive(path)}>
                <a href={$url(path)} class="hover:underline decoration-pink-300"
                    >{title}</a
                >
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
