<script>
    import BottomMenu from "$lib/components/BottomMenu.svelte";
    import TopMenu from "$lib/components/TopMenu.svelte";

    import backgroundImage from "$lib/assets/images/CloverDrop.webp";
</script>

<title>Contact</title>

<div class="min-h-screen">
        <div
            class="absolute top-0 min-h-screen min-w-screen bg-cover bg-center bg-no-repeat"
            style="background-image: url('{backgroundImage}');"
        >
            <TopMenu currentPage={"contact"} />
            <div class="relative flex min-h-[60vh] items-center justify-center">
                <div class="flex rounded-md bg-gray-700 opacity-90 w-[80%] h-180 justify-center">
                    <h1 class="text-3xl underline drop-shadow-md drop-shadow-black text-gray-300 mt-10">Contact</h1>
                </div>
            </div>
        </div>
</div>
<BottomMenu currentPage={"contact"} />