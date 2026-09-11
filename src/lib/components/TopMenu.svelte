<script lang="ts">
    import DropDownMenu from "./DropDownMenu.svelte";
    let { currentPage } = $props();
</script>

<div class="flex flex-nowrap justify-center items-center p-1 m-2 mt-10 mb-[10vh] text-3xl text-gray-300 text-shadow-black text-shadow-md">
    <nav class="flex flex-nowrap">
        <a style="margin-right: 2vw; font-[M+PLUS+U]; {currentPage === "home" ? "text-decoration: underline;" : ""}" href="/">Home</a>
        <DropDownMenu title="Portfolio" options={[ { name: "Nature", href: "/Portfolio/Nature"}, {name: "Other", href: "/Portfolio/Other"} ]} href="/Portfolio" currentPage={currentPage}/>
    </nav>
    <div class="text-center text-6xl ml-[3vw] mr-[3vw]">
        <h1 class="font-custom">Olivia Lua Photography</h1>
    </div>
    <nav>
        <a style="font-[M+PLUS+U]; {currentPage === "about" ? "text-decoration: underline;" : ""}" href="/About">About</a>
        <a style="margin-left: 2vw; font-[M+PLUS+U]; {currentPage === "contact" ? "text-decoration: underline" : ""}" href="/Contact">Contact</a>
    </nav>
</div>
