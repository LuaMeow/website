<script>
    import ArrowUp from "./ArrowUp.svelte";

    let { currentPage } = $props();

    function gotoTop() {
        window.scrollTo({ top: 0, behavior: "smooth" });
    }
</script>

<div class="flex justify-center items-center w-full">
    <div class="relative flex justify-center bg-[#1E1E1E] w-full h-[45vh] mb-0">
        <hr class="absolute h-[1px] w-[70%] my-10 mx-auto bg-gray-300 border-0">
        <nav class="absolute left-150 top-20 drop-shadow-md drop-shadow-black">
            <a class="flex font-[M+PLUS+U] text-gray-300 drop-shadow-md drop-shadow-black text-md" 
                style="{currentPage === "home" ? "text-decoration: underline;" : ""}" 
                href="/">
                Home
            </a>
            <a class="flex font-[M+PLUS+U] text-gray-300 drop-shadow-md drop-shadow-black text-md mt-8" 
                style="{currentPage === "portfolio" ? "text-decoration: underline;" : ""}" 
                href="/Portfolio">
                Portfolio
            </a>
            <a class="flex font-[M+PLUS+U] text-gray-300 drop-shadow-md drop-shadow-black text-md mt-8" 
                style="{currentPage === "about" ? "text-decoration: underline;" : ""}" 
                href="/About">
            About
        </a>
            <a class="flex font-[M+PLUS+U] text-gray-300 drop-shadow-md drop-shadow-black text-md mt-8" 
                style="{currentPage === "contact" ? "text-decoration: underline;" : ""}" 
                href="/Contact">
                Contact
            </a>    
        </nav>

        <button type="button" class="absolute top-20 right-150 cursor-pointer" onclick={gotoTop}>
            <ArrowUp class="flex fill-gray-300 drop-shadow-md drop-shadow-black h-6 w-6 "/>
        </button>
        <hr class="absolute h-[1px] w-[70%] my-80 mx-auto bg-gray-300 border-0 drop-shadow-md drop-shadow-black">
    </div>
</div>