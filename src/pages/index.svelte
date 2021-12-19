<script>
    import { metatags, url } from "@roxi/routify";
    import ImageLoader from "../_components/Image/ImageLoader.svelte";

    metatags.description = "Description coming soon...";
    let src = "images/yang-profile.png";
</script>

<div
    class="flex flex-col space-y-10 lg:space-x-8 md:space-y-0 lg:flex-row mt-12 justify-center items-center"
>
    <ImageLoader
        {src}
        alt="Portrait of author with boxing gloves on"
        className="h-96 md:h-[40rem] xl:h-[30rem]"
    />
    <div
        class="w-3/6 text-l break-words leading-loose md:leading-loose md:text-xl lg:leading-loose lg:text-2xl xl:leading-loose xl:text-xl md:pt-16 lg:pt-0 xl:pt-0 space-y-2"
    >
        <p
            class="text-l break-words leading-loose md:leading-loose md:text-xl lg:leading-loose lg:text-2xl xl:leading-loose xl:text-xl md:pt-16 lg:pt-0 xl:pt-0"
        >
            Hiya! I'm Yang, a software consultant and artist based in Chapel
            Hill. I love to design awesome projects for end users at <a
                href={$url("/")}
                class="underline decoration-emerald-500">Macedon Technologies</a
            >. Outside of work, I'm an avid
            <a href={$url("/resume")} class="underline decoration-cyan-500"
                >representational artist</a
            >
            and a curious student of the online program at
            <a href={$url("/artwork")} class="underline decoration-pink-500"
                >Watts Atelier</a
            >
            Check out my work in the
            <a href={$url("/artwork")} class="underline decoration-cyan-500"
                >gallery</a
            >!
        </p>
        <p>Feel free to ping me by email or social media!</p>
    </div>
</div>
