<script>
    import WorkTile from "../../_components/WorkTile/WorkTile.svelte";
    import jobs from "../../lib/data/jobs.json";
</script>

<div class="mt-6 md:mt-10">
    <h1 class="text-center text-4xl font-bold">Work</h1>
    <div class="mt-8 space-y-8">
        {#each jobs as job}
            <WorkTile {...job} />
        {/each}
    </div>
</div>
