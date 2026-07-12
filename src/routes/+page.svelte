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

    let slideInterval = setInterval(slideRight, 5000);

    function slide(direction) {
        if(direction === "left")
            slideLeft();
        else if(direction === "right")
            slideRight();

        clearInterval(slideInterval);
        slideInterval = setInterval(slideRight, 5000);
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

<div style= "height: 100vh; width: 100vw; position: relative; display: flex; justify-content: top; align-items: center; flex-direction: column;">
    {#each sliderImages as image, index}
        <img src="{image}" alt="Ant Background" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; z-index: -1; opacity: {index === currentImageIndex ? 1 : 0}; transition: opacity 1s ease-in-out;">
    {/each}

    <button onclick={() => slide("left")} class="absolute top-0 left-0 h-full w-50 flex items-center justify-center group">
        <div class="absolute h-full w-1 left-0 bg-linear-to-l from-transparent to-gray-200 group-hover:w-full transition-all opacity-25"></div>
        <LeftArrow class="absolute mt-[50vh] mr-10 top-2.5 left-2.5 z-1 h-12.5 w-12.5 fill-gray-300 group-hover:fill-gray-400 drop-shadow-md drop-shadow-black"/>
    </button>

    <button onclick={() => slide("right")} class="absolute top-0 right-0 h-full w-50 flex items-center justify-center group">
        <div class="absolute h-full w-1 right-0 bg-linear-to-r from-transparent to-gray-200 group-hover:w-full transition-all opacity-25"></div>
        <RightArrow class="absolute mt-[50vh] ml-10 top-2.5 right-2.5 z-1 h-12.5 w-12.5 fill-gray-300 group-hover:fill-gray-400 drop-shadow-md drop-shadow-black"/>
    </button>

    <TopMenu/>

    <ArrowsDown class="absolute bottom-0 h-20 w-20 fill-gray-300 drop-shadow-md drop-shadow-black animate-bounce"/>

    
</div>


<div class="bg-white" style="min-height: 50vh;">
</div>
<div style="background-image: url('{backgroundImage2}'); background-size: cover; background-position: center; min-height: 60vh; position: relative; display: flex; justify-content: top; align-items: center; flex-direction: column;"></div>
<div class="bg-white" style="min-height: 50vh;">
</div>
<div style=" background-color: rgb(30,30,30); min-height: 40vh;">
</div>