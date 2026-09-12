<script lang="ts">
    let { title, options, href, currentPage }: {
      title: string,
      options: { name: string, href: string }[],
      href: string,
      currentPage: string
    } = $props();

    let pages = $derived(currentPage.split("/"));
</script>

<div class="relative group">
    <a href="{href}" class="{pages[0] === title ? "underline" : ""}">
        {title}
    </a>
    <div class="absolute">
        <a href="{href}" class="text-2xl {pages[0] === title && pages[1] !== undefined ? "underline" : "hidden"}">
            {pages[1]}
        </a>
        <div class="overflow-hidden">
            <div class="flex flex-col -translate-y-full group-hover:translate-y-0 transition-all">
                {#each options as option}
                    <a href="{option.href}" class=" {pages[1] === option.name ? "hidden" : ""} text-2xl">
                        {option.name}
                    </a>
                {/each}
            </div>
        </div>
    </div>
</div>
