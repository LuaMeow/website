<script>
    import TopMenu from '$lib/components/TopMenu.svelte';
    import backgroundImage1 from '$lib/assets/images/AntBackground.webp';
    import backgroundImage2 from '$lib/assets/images/coot1.webp';
    import backgroundImage3 from '$lib/assets/images/BlueTitSpring.webp';
    import backgroundImage4 from '$lib/assets/images/Swans.webp';
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

    function slideRight() {
        console.log('Sliding right');
        if (currentImageIndex < sliderImages.length - 1) {
            currentImageIndex++;
        } else {
            currentImageIndex = 0; // Loop back to the first image
        }
    }

    function slideLeft() {
        console.log('Sliding left');
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
    <img src="{sliderImages[currentImageIndex]}" alt="Ant Background" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; z-index: -1;">
    <button onclick={slideLeft} style="position: absolute; top: 10px; left: 10px; z-index: 1;">
        Previous
    </button>
    <button onclick={slideRight} style="position: absolute; top: 10px; right: 10px; z-index: 1;">
        Next
    </button>
    <TopMenu/>

    <h1 class="centered">Welcome to my Home Page</h1>
    
</div>


<div class="bg-white" style="min-height: 50vh;">
</div>
<div style="background-image: url('{backgroundImage2}'); background-size: cover; background-position: center; min-height: 60vh; position: relative; display: flex; justify-content: top; align-items: center; flex-direction: column;"></div>
<div class="bg-white" style="min-height: 50vh;">
</div>
<div style=" background-color: rgb(30,30,30); min-height: 40vh;">
</div>