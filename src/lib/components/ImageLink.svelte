<script lang="ts">
    import type { Snippet } from "svelte";

    let { imageSource, css, href, children }: {
        imageSource: string,
        css: string,
        href: string,
        children?: Snippet
    } = $props();
</script>

<a href="{href}" class="relative group overflow-hidden {css}">
     <div
         class="absolute min-w-full min-h-full bg-cover bg-center group-hover:brightness-50 transition"
         style="background-image: url('{imageSource}');"
     ></div>
     <div class="relative text-white text-2xl text-center min-w-full min-h-full overflow-hidden drop-shadow-black drop-shadow-md font-[P+PLUS+M] cursor-pointer">
         {@render children?.()}
     </div>
 </a>
