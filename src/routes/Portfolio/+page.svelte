<script>
    import BottomMenu from "$lib/components/BottomMenu.svelte";
    import TopMenu from "$lib/components/TopMenu.svelte";
    import backgroundImage2 from "$lib/assets/images/coot1.webp";
    import natureButton from "$lib/assets/images/naturebutton.webp";
    import otherButton from "$lib/assets/images/otherbutton.webp";
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
    <a href="/Portfolio/Nature" class="relative group w-100 h-100 mr-50">
        <div
            class="absolute min-w-100 min-h-100 bg-cover bg-center rounded-xl group-hover:brightness-50 transition"
            style="background-image: url('{natureButton}');"
        ></div>
        <div class="absolute top-30 left-25 text-white text-2xl text-center drop-shadow-black drop-shadow-md font-[P+PLUS+M] cursor-pointer">
            <span class="group-hover:underline">
                Nature<br>
                & <br>
                Wildlife <br>
            </span>
            ⟶
        </div>
    </a>

    <a href="/Portfolio/Other" class="relative group w-100 h-100">
        <div
            class="absolute min-w-100 min-h-100 bg-cover bg-center rounded-xl group-hover:brightness-50"
            style="background-image: url('{otherButton}');">
        </div>
        <div class="absolute top-35 left-60 text-white text-2xl text-center drop-shadow-black drop-shadow-md font-[P+PLUS+M] cursor-pointer">
            <span class="group-hover:underline">
                Other <br>
            </span>
            ⟶
        </div>
    </a>
</div>

<BottomMenu currentPage={"portfolio"} />
