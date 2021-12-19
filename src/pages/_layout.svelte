<script>
    import Navbar from "../_components/Navbar.svelte";
</script>

<!-- routify:options preload="proximity" -->
<div class="flex flex-col mt-10">
    <Navbar />
    <slot />
    <footer class="px-5 text-center text-sm md:text-base mt-24 mb-4">
        Built with love by Yang Chen using <span class="underline">Svelte</span>
        and <span class="underline">Tailwind CSS</span>.
    </footer>
</div>

<style>
    :global(body) {
        background-color: #f2f2f2;
    }
</style>
