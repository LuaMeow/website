<script>
    import BottomMenu from "$lib/components/BottomMenu.svelte";
    import TopMenu from "$lib/components/TopMenu.svelte";

    import backgroundImage from "$lib/assets/images/CloverDrop.webp";

    import PixelfedLogo from "$lib/components/PixelfedLogo.svelte";
    import InstagramLogo from "$lib/components/InstagramLogo.svelte";
</script>

<title>
    Contact
</title>

<div class="min-h-screen relative justify-center items-center">
    <div
        class="absolute top-0 min-h-screen min-w-screen bg-cover bg-center bg-no-repeat"
        style="background-image: url('{backgroundImage}');"
    >
        <TopMenu currentPage={"contact"} />
    
        <div class="relative flex rounded-md bg-gray-700 opacity-90 w-[80%] h-180 justify-center m-auto">
            <h1 class="text-4xl underline drop-shadow-md drop-shadow-black text-gray-300 mt-10">
                Contact
            </h1>
            <div class="absolute text-2xl text-gray-300 drop-shadow-md drop-shadow-black left-90 top-30">
                <span class="underline">
                    Find me on:
                </span>
                <a href="https://www.instagram.com/olivia.lua.photography/" class="flex items-center gap-3 fill-gray-300 drop-shadow-md drop-shadow-black group mt-10">
                    <InstagramLogo class="h-20 w-20 group-hover:fill-green-700 group-hover:h-23 group-hover:w-23 transition-all" />
                    <div class="text-2xl text-gray-300 whitespace-nowrap group-hover:text-green-700 group-hover:text-3xl transition-all">
                        Instagram
                    </div>
                </a>
            </div>
            <div class="absolute text-2xl text-gray-300 drop-shadow-md drop-shadow-black right-90 top-30">
                <span class="underline">
                    Or send me a Mail:
                </span>
                <form 
                    class="absolute flex flex-col gap-4 mt-10 text-black w-100"
                    action="mailto:photography-web@olivialua.de" method="POST" enctype="text/plain"
                >
                    <input type="text" name="Name" placeholder="Your name" />
                    <input type="email" name="Email" placeholder="Your email" />
                    <textarea class="h-75" name="Message" placeholder="Your message"></textarea>
                    <button class="drop-shadow-md drop-shadow-black hover:text-green-700 text-gray-300 hover:text-3xl transition-all" type="submit">Send!</button>
                </form>
            </div>
        </div>
    </div>
</div>
<BottomMenu currentPage={"contact"} /> 