<script>
    import BottomMenu from "$lib/components/BottomMenu.svelte";
    import TopMenu from "$lib/components/TopMenu.svelte";
    import backgroundImage2 from "$lib/assets/images/coot.webp";
    import natureButton from "$lib/assets/images/GreatTit.webp";
    import otherButton from "$lib/assets/images/Vespa.webp";
    import ImageLink from "$lib/components/ImageLink.svelte";
</script>

<title> Portfolio </title>

<div class="relative min-h-[60vh] justify-center items-top">
    <div
        class="absolute min-w-screen min-h-[60vh] bg-cover bg-center mb-0"
        style="background-image: url('{backgroundImage2}');">

        <TopMenu currentPage={"Portfolio"} />

        <div class="text-5xl underline text-center text-gray-300 font-custom drop-shadow-black drop-shadow-md pt-40">
            My Portfolio
        </div>
    </div>
</div>

<div class="flex bg-white min-h-150 items-center justify-center">
    <ImageLink href="/Portfolio/Nature" imageSource={natureButton} css="w-100 h-100 mr-50 rounded-xl">
        <span class="absolute top-30 left-25">
            <span class="group-hover:underline">
                Nature <br>
                & <br>
                Wildlife <br>
            </span>
            ⟶
        </span>
    </ImageLink>

    <ImageLink href="/Portfolio/Other" imageSource={otherButton} css="w-100 h-100 rounded-xl">
        <span class="absolute top-35 left-60">
            <span class="group-hover:underline">
                Other <br>
            </span>
            ⟶
        </span>
    </ImageLink>
</div>

<BottomMenu currentPage={"portfolio"} />
