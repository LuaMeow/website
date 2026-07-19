<script>
    import ArrowUp from "./ArrowUp.svelte";

    let { currentPage } = $props();

    function gotoTop() {
        window.scrollTo({ top: 0, behavior: "smooth" });
    }
</script>

<div class="flex justify-center items-center w-full">
    <div class="relative flex bg-[#1E1E1E] w-full h-[40vh] mb-0">
        <nav>
            <a class="flex font-[M+PLUS+U] text-gray-300 drop-shadow-md drop-shadow-black text-md ml-[30vw] mt-15" style="{currentPage === "home" ? "text-decoration: underline;" : ""}" href="/">Home</a>
            <a class="flex font-[M+PLUS+U] text-gray-300 drop-shadow-md drop-shadow-black text-md ml-[30vw] mt-8" style="{currentPage === "portfolio" ? "text-decoration: underline;" : ""}" href="/Portfolio">Portfolio</a>
            <a class="flex font-[M+PLUS+U] text-gray-300 drop-shadow-md drop-shadow-black text-md ml-[30vw] mt-8" style="{currentPage === "about" ? "text-decoration: underline;" : ""}" href="/About">About</a>
            <a class="flex font-[M+PLUS+U] text-gray-300 drop-shadow-md drop-shadow-black text-md ml-[30vw] mt-8" style="{currentPage === "contact" ? "text-decoration: underline;" : ""}" href="/Contact">Contact</a>    
            <button type="button" class="absolute top-15 right-[30vw] cursor-pointer" onclick={gotoTop}>
                <ArrowUp class="flex fill-gray-300 drop-shadow-md drop-shadow-black h-6 w-6 "/>
            </button>
        </nav>
    </div>
</div>