<script setup>
import { onMounted } from "vue";
import { Carousel } from "flowbite";
onMounted(() => {
  const items = [
    {
      position: 0,
      el: document.getElementById("carousel-item-1"),
    },
    {
      position: 1,
      el: document.getElementById("carousel-item-2"),
    },
    {
      position: 2,
      el: document.getElementById("carousel-item-3"),
    },
    {
      position: 3,
      el: document.getElementById("carousel-item-4"),
    },
  ];
  const options = {
    defaultPosition: 1,
    interval: 5000,

    indicators: {
      activeClasses: "bg-white dark:bg-gray-800",
      inactiveClasses:
        "bg-white/50 dark:bg-gray-800/50 hover:bg-white dark:hover:bg-gray-800",
      items: [
        {
          position: 0,
          el: document.getElementById("carousel-indicator-1"),
        },
        {
          position: 1,
          el: document.getElementById("carousel-indicator-2"),
        },
        {
          position: 2,
          el: document.getElementById("carousel-indicator-3"),
        },
        {
          position: 3,
          el: document.getElementById("carousel-indicator-4"),
        },
      ],
    },

    // callback functions
    // onNext: () => {
    //     console.log('next slider item is shown');
    // },
    // onPrev: ( ) => {
    //     console.log('previous slider item is shown');
    // },
    // onChange: ( ) => {
    //     console.log('new slider item has been shown');
    // }
  };
  if (document.getElementById("carousel-item-1")) {
    const carousel = new Carousel(items, options);
    carousel.cycle();
    // set event listeners for prev and next buttons
    const prevButton = document.getElementById("data-carousel-prev");
    const nextButton = document.getElementById("data-carousel-next");
    prevButton.addEventListener("click", () => {
      carousel.prev();
    });
    nextButton.addEventListener("click", () => {
      carousel.next();
    });
  }
});
</script>

<template>
    <div class="max-w-[1400px] py-16 px-4 mx-auto">
  
          <div class="relative">
              <!-- Carousel wrapper -->
              <div class="relative h-screen overflow-hidden rounded-lg max-h-screen">
                   <!-- Item 1 -->
                  <div id="carousel-item-1" class="hidden duration-3000 ease-in-out">
                    <img src="~assets/images/shopping-15.jpg" class="absolute block w-full h-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">
                    <figcaption class="absolute">
                        <h1>Elevate Your Style</h1>
                        <p>Discover Amazing Deals</p>
                      </figcaption>
                    <NuxtLink to="/products" class="btn rounded-full absolute px-6 py-3.5 font-medium text-md text-center bottom-20 left-1/2 transform -translate-x-1/2 transition ease-in-out">Shop Now</NuxtLink>
                  </div>
                  <!-- Item 2 -->
                  <div id="carousel-item-2" class="hidden duration-3000 ease-in-out">
                      <img src="~assets/images/shopping-33.jpg" class="absolute block w-full h-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="..." >
                      <figcaption class="absolute">
                        <h1>Fashion Finds Awaits</h1>
                        <p>50% Discounts</p>
                      </figcaption>
                      <NuxtLink to="/products" class="btn rounded-full absolute px-6 py-3.5 text-md font-medium text-center bottom-20 left-1/2 transform -translate-x-1/2 transition ease-in-out">Shop Now</NuxtLink>
                  </div>
                  <!-- Item 3 -->
                  <div id="carousel-item-3" class="hidden duration-3000 ease-in-out">
                      <img src="~assets/images/shopping-17.jpg" class="absolute block w-full h-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">
                      <figcaption class="absolute">
                        <h1>Trendy, Chic, and Affordable</h1>
                        <p>Discover Amazing Deals</p>
                      </figcaption>
                      <NuxtLink to="/products" class="btn rounded-full absolute px-6 py-3.5 text-md font-medium text-center bottom-20 left-1/2 transform -translate-x-1/2 transition ease-in-out">Shop Now</NuxtLink>
                  </div>
                  <!-- Item 4 -->
                  <div id="carousel-item-4" class="hidden duration-3000 ease-in-out">
                      <img src="~assets/images/shopping-16.jpg" class="absolute block w-full h-full -translate-x-1/2 -translate-y-1/2 top-1/2 left-1/2" alt="...">
                      <figcaption class="absolute">
                        <h1>Savings That Sparkle</h1>
                        <p>50% Discount</p>
                      </figcaption>
                      <NuxtLink to="/products" class="btn rounded-full absolute px-6 py-3.5 text-md font-medium text-center bottom-20 left-1/2 transform -translate-x-1/2 transition ease-in-out">Shop Now</NuxtLink>
                  </div>
              </div>
              <!-- Slider indicators -->
              <div class="absolute z-30 flex space-x-3 -translate-x-1/2 bottom-5 left-1/2">
                  <button id="carousel-indicator-1" type="button" class="w-3 h-3 rounded-full" aria-current="true" aria-label="Slide 1"></button>
                  <button id="carousel-indicator-2" type="button" class="w-3 h-3 rounded-full" aria-current="false" aria-label="Slide 2"></button>
                  <button id="carousel-indicator-3" type="button" class="w-3 h-3 rounded-full" aria-current="false" aria-label="Slide 3"></button>
                  <button id="carousel-indicator-4" type="button" class="w-3 h-3 rounded-full" aria-current="false" aria-label="Slide 4"></button>
              </div>
    <!-- Slider indicators -->
            <div class="absolute z-30 flex space-x-3 -translate-x-1/2 bottom-5 left-1/2">
                <button id="carousel-indicator-1" type="button" class="w-3 h-3 rounded-full" aria-current="true" aria-label="Slide 1"></button>
                <button id="carousel-indicator-2" type="button" class="w-3 h-3 rounded-full" aria-current="false" aria-label="Slide 2"></button>
                <button id="carousel-indicator-3" type="button" class="w-3 h-3 rounded-full" aria-current="false" aria-label="Slide 3"></button>
                <button id="carousel-indicator-4" type="button" class="w-3 h-3 rounded-full" aria-current="false" aria-label="Slide 4"></button>
            </div>
            <!-- Slider controls -->
            <button id="data-carousel-prev" type="button" class="absolute top-0 left-0 z-30 flex items-center justify-center h-full px-4 cursor-pointer group focus:outline-none">
                <span class="inline-flex items-center justify-center w-8 h-8 rounded-full sm:w-10 sm:h-10 bg-white/30 dark:bg-gray-800/30 group-hover:bg-white/50 dark:group-hover:bg-gray-800/60 group-focus:ring-4 group-focus:ring-white dark:group-focus:ring-gray-800/70 group-focus:outline-none">
                    <svg class="w-5 h-5 text-white sm:w-6 sm:h-6 dark:text-gray-800" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path></svg>
                    <span class="hidden">Previous</span>
                </span>
            </button>
            <button id="data-carousel-next" type="button" class="absolute top-0 right-0 z-30 flex items-center justify-center h-full px-4 cursor-pointer group focus:outline-none">
                <span class="inline-flex items-center justify-center w-8 h-8 rounded-full sm:w-10 sm:h-10 bg-white/30 dark:bg-gray-800/30 group-hover:bg-white/50 dark:group-hover:bg-gray-800/60 group-focus:ring-4 group-focus:ring-white dark:group-focus:ring-gray-800/70 group-focus:outline-none">
                    <svg class="w-5 h-5 text-white sm:w-6 sm:h-6 dark:text-gray-800" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
                    <span class="hidden">Next</span>
                </span>
            </button>
        </div>
    </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,400;1,600&display=swap');

  figcaption {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
  }

  h1 {
    font-family: 'Playfair Display', sans-serif;
    font-size: 4rem;
    font-weight: 600;
    color: #fff;
  }

  p {
    color: #12b488;
    font-size: 1.25rem;
  }



</style>
