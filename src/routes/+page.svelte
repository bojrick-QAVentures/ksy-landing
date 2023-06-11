<script>
  import { Card, Button, Toggle, Skeleton, ImagePlaceholder } from 'flowbite-svelte';

  // <script>
  // import { CardPlaceholder, ImagePlaceholder, ListPlaceholder, Skeleton, TestimonialPlaceholder, TextPlaceholder, VideoPlaceholder, WidgetPlaceholder } from 'flowbite-svelte'

  let vCard = false;
  import { Carousel } from 'flowbite-svelte';
  let showThumbs = false;
  let showCaptions = false;

  // ./imageData/+server.js has the following
  const images = [
    {
      id: 0,
      name: 'Cosmic timetraveler',
      imgurl: 'src/images/researching-laboratory.jpg',
      attribution: 'cosmic-timetraveler-pYyOZ8q7AII-unsplash.com'
    },
    {
      id: 1,
      name: 'Cristina Gottardi',
      imgurl: 'src/images/close-up-hand-holding-tube.jpg',
      attribution: 'cristina-gottardi-CSpjU6hYo_0-unsplash.com'
    }
  ];
</script>

<slot>
  <!--  <h1>Welcome to SvelteKit</h1>-->

  <div class="carousel-container">
    <Carousel {images} loop {showCaptions} {showThumbs} duration="3000" />
  </div>

  <div class="flex flex-wrap justify-center items-center">
    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/3 xl:w-1/3">
      <Card img="/images/image-1.webp" reverse={vCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
          Noteworthy technology acquisitions 2021
        </h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
        </p>
        <Button color="blue">
          Read more <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-5 h-5 ml-2"
            ><path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" /></svg
          >
        </Button>
      </Card>
      <!--    <Toggle bind:checked={vCard} class="mt-4 italic dark:text-gray-500">Reverse</Toggle>-->
    </div>

    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/3 xl:w-1/3">
      <Card img="/images/image-1.webp" reverse={vCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
          Noteworthy technology acquisitions 2021
        </h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
        </p>
        <Button color="blue">
          Read more <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-5 h-5 ml-2"
            ><path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" /></svg
          >
        </Button>
      </Card>
      <!--    <Toggle bind:checked={vCard} class="mt-4 italic dark:text-gray-500">Reverse</Toggle>-->
    </div>

    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/3 xl:w-1/3">
      <Card img="/images/image-1.webp" reverse={vCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
          Noteworthy technology acquisitions 2021
        </h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
        </p>
        <Button color="blue">
          Read more <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-5 h-5 ml-2"
            ><path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" /></svg
          >
        </Button>
      </Card>
      <!--    <Toggle bind:checked={vCard} class="mt-4 italic dark:text-gray-500">Reverse</Toggle>-->
    </div>
  </div>

  <!--  <ImagePlaceholder />-->
  <!--  <ImagePlaceholder imgHeight={60} class='mt-8'/>-->
  <!--  <Skeleton size="sm" class="my-8" />-->
  <!--  <Skeleton size="md" class="my-8" />-->
  <!--  <Skeleton size="lg" class="my-8" />-->
  <!--  <Skeleton size="xl" class="my-8" />-->
  <!--  <Skeleton size="xxl" class="mt-8 mb-2.5" />-->
</slot>

<style>
  .carousel-container {
    height: 500px; /* Adjust the height as needed */
  }
</style>
