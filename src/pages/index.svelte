<script>
    import { metatags, url } from "@roxi/routify";
    import ImageLoader from "../_components/Image/ImageLoader.svelte";

    metatags.title = "Yang Chen";
    metatags.description = "Description coming soon...";
    let src = "images/yang-profile.png";
</script>

<div
    class="flex flex-col space-y-10 lg:space-x-0 md:space-y-0 lg:flex-row lg:mx-24 xl:mx-72 mt-12 items-center"
>
    <ImageLoader
        {src}
        alt="Portrait of author with boxing gloves on"
        className="h-96 md:h-[40rem] xl:h-[30rem]"
    />
    <p
        class="w-4/6 text-l break-words leading-loose md:leading-loose md:text-xl lg:leading-loose lg:text-2xl xl:leading-loose xl:text-xl md:pt-16 xl:pt-0"
    >
        Hiya! I'm Yang, a software consultant and artist based in Chapel Hill. I
        love to design awesome projects for end users at <a
            href={$url("/")}
            class="underline decoration-sky-500">Macedon Technologies</a
        >. Outside of work, I'm an avid
        <a href={$url("/resume")} class="underline decoration-pink"
            >representational artist</a
        >
        and a curious student of the online program at
        <a href={$url("/artwork")} class="underline decoration-sky-500"
            >Watts Atelier</a
        >
    </p>
</div>
