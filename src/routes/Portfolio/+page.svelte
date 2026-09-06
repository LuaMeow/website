<script>
    import BottomMenu from "$lib/components/BottomMenu.svelte";
    import TopMenu from "$lib/components/TopMenu.svelte";
    import backgroundImage2 from "$lib/assets/images/coot1.webp";
    import natureButton from "$lib/assets/images/naturebutton.webp";
    import otherButton from "$lib/assets/images/otherbutton.webp";

</script>
<title>
    Portfolio
</title>
<div class = "relative min-h-[60vh] justify-center items-top">
    <div
        class ="absolute min-w-screen min-h-[70vh] bg-cover bg-center mb-0"
        style ="background-image: url('{backgroundImage2}');">
        <TopMenu currentPage={"portfolio"}/>
        <div class ="text-5xl underline text-center text-gray-300 font-custom drop-shadow-black drop-shadow-md pt-16">
            My Portfolio
        </div>
    </div>
</div>
<div class = "relative flex-row bg-white min-h-150 mt-0">
    <div
        class = "absolute min-w-100 min-h-100 bg-cover bg-center mt-25 ml-100 left-10 rounded-xl"
        style = "background-image: url('{natureButton}');">
        <button
            type = "button"
            class= "absolute inset-0 right-30 text-white text-2xl text-center drop-shadow-black drop-shadow-md font-[P+PLUS+M]">
            Nature <br>
            & <br>
            Wildlife <br>
            ⟶
        </button>
    </div>
    <div
        class = "absolute min-w-100 min-h-100 bg-cover bg-center mt-25 mr-100 right-10 rounded-xl"
        style = "background-image: url('{otherButton}');">
        <button
            type = "button"
            class = "absolute inset-0 left-30 text-white text-2xl text-center drop-shadow-black drop-shadow-md font-[P+PLUS+M]">
            Other <br>
            ⟶
        </button>
    </div>
</div>
<BottomMenu currentPage={"portfolio"}/>
