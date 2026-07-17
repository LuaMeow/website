<script>
    import TopMenu from '$lib/components/TopMenu.svelte';
    import RightArrow from '$lib/components/RightArrow.svelte';
    import LeftArrow from '$lib/components/LeftArrow.svelte';
    import ArrowsDown from '$lib/components/ArrowsDown.svelte';
    import backgroundImage4 from '$lib/assets/images/AntBackground.webp';
    import backgroundImage2 from '$lib/assets/images/coot1.webp';
    import backgroundImage3 from '$lib/assets/images/BlueTitSpring.webp';
    import backgroundImage1 from '$lib/assets/images/Swans.webp';
    import backgroundImage5 from '$lib/assets/images/TawnyOwlClose.webp';
    import backgroundImage6 from '$lib/assets/images/Efferia.webp';

    let currentImageIndex = $state(0);
    let sliderImages = [
        backgroundImage1,
        backgroundImage3,
        backgroundImage4,
        backgroundImage5,
        backgroundImage6
    ];  

    let slideInterval = setInterval(slideRight, 6000);

    function clearSlideInterval() {
        clearInterval(slideInterval);
        slideInterval = setInterval(slideRight, 6000);
    }

    function slideRight() {
        if (currentImageIndex < sliderImages.length - 1) {
            currentImageIndex++;
        } else {
            currentImageIndex = 0; // Loop back to the first image
        }
    }

    function slideLeft() {
        if (currentImageIndex > 0) {
            currentImageIndex--;
        } else {
            currentImageIndex = sliderImages.length - 1; // Loop back to the last image
        }
    }

</script>

<head>
    <title>Olivia Lua Photography</title>
    
</head>

<div style= "height: 100vh; min-width: 100%; position: relative; display: flex; justify-content: top; align-items: center; flex-direction: column;">
    {#each sliderImages as image, index}
        <img src="{image}" alt="Ant Background" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; z-index: -1; opacity: {index === currentImageIndex ? 1 : 0}; transition: opacity 1s ease-in-out;">
    {/each}

    <button onclick={() => {clearSlideInterval(); slideLeft()}} class="absolute top-0 left-0 h-full w-50 flex items-center justify-center group">
        <div class="absolute h-full w-1 left-0 bg-linear-to-l from-transparent to-gray-200 group-hover:w-full transition-all opacity-25"></div>
        <LeftArrow class="absolute mt-[50vh] mr-10 top-2.5 left-2.5 z-1 h-12.5 w-12.5 fill-gray-300 group-hover:fill-gray-400 drop-shadow-md drop-shadow-black"/>
    </button>

    <button onclick={() => {clearSlideInterval(); slideRight()}} class="absolute top-0 right-0 h-full w-50 flex items-center justify-center group">
        <div class="absolute h-full w-1 right-0 bg-linear-to-r from-transparent to-gray-200 group-hover:w-full transition-all opacity-25"></div>
        <RightArrow class="absolute mt-[50vh] ml-10 top-2.5 right-2.5 z-1 h-12.5 w-12.5 fill-gray-300 group-hover:fill-gray-400 drop-shadow-md drop-shadow-black"/>
    </button>

    <TopMenu/>

    <div class="absolute bottom-10 inline-flex items-center">
        {#each sliderImages as image, index}
            <label class="relative flex items-center cursor-pointer" for="imageRadio{index}">
                <input
                    name="sliderSelector"
                    type="radio"
                    class="peer h-5 w-5 m-3 cursor-pointer appearance-none bg-gray-300 rounded-full border border-slate-300 checked:border-slate-400 transition-all shadow-md shadow-black checked:h-7 checked:w-7 focus:outline-none focus:bg-opacity-0 focus:ring-offset-0 focus:ring-0"
                    id="imageRadio{index}"
                    onclick={() => {clearSlideInterval(); currentImageIndex = index }}
                    checked="{currentImageIndex === index ? "checked" : ""}"
                />
                <span class="absolute bg-slate-800 w-4.5 h-4.5 rounded-full opacity-0 peer-checked:opacity-100 transition-opacity duration-200 top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2"></span>
            </label>
        {/each}
    </div>

    <div class="absolute bottom-0 right-10 animate-bounce">
        <div class="bottom-25 right-8 font-[M+PLUS+U] text-2xl text-gray-300 drop-shadow-black drop-shadow-md text-center">
            Scroll <br> 
            for <br>
            More!
        </div>
        <ArrowsDown class="bottom-0 right-5 h-20 w-20 fill-gray-300 drop-shadow-md drop-shadow-black"/>
    </div>
    
</div>


<div class="bg-white" style="min-height: 50vh;">
</div>
<div style="background-image: url('{backgroundImage2}'); background-size: cover; background-position: center; min-height: 60vh; position: relative; display: flex; justify-content: top; align-items: center; flex-direction: column;"></div>
<div class="bg-white" style="min-height: 50vh;">
</div>
<div style=" background-color: rgb(30,30,30); min-height: 40vh;">
</div>