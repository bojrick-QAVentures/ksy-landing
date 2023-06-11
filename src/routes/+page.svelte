<script>
  import { Card, Button, Heading, P, Img, TextPlaceholder,Toggle, Skeleton, ImagePlaceholder } from 'flowbite-svelte';

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
      imgurl: '/images/researching-laboratory.jpg',
      attribution: 'cosmic-timetraveler-pYyOZ8q7AII-unsplash.com'
    },
    {
      id: 1,
      name: 'Cristina Gottardi',
      imgurl: '/images/close-up-hand-holding-tube.jpg',
      attribution: 'cristina-gottardi-CSpjU6hYo_0-unsplash.com'
    }
  ];
</script>

<slot>
  <!--  <h1>Welcome to SvelteKit</h1>-->

  <div class="carousel-container mb-5">
    <Carousel class = "w-full h-auto" {images} loop {showCaptions} {showThumbs} duration="3000" />
  </div>

  <div class="flex flex-wrap bg-[#1da1f2] mb-5">
    <div class = "w-full md:w-1/2 h-auto" >
    <Img src="/images/Fragrance Sample.jpg" alt="sample 1" size="max-w-lg" alignment="mx-auto"  />
    </div>
    <div class = "w-full md:w-1/2">
    <Heading class="p-8" tag="h2">Who We Are</Heading>

    <P class="px-8 py-4">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
      labore et dolore magna aliqua. Amet cursus sit amet dictum sit. Quis enim lobortis scelerisque
      fermentum dui faucibus in. Mattis vulputate enim nulla aliquet porttitor lacus luctus accumsan.
      Ipsum dolor sit amet consectetur adipiscing elit. Euismod nisi porta lorem mollis aliquam ut
      porttitor. Tortor consequat id porta nibh. Tortor condimentum lacinia quis vel eros donec ac odio.
      Elementum sagittis vitae et leo duis ut diam quam nulla. Vel turpis nunc eget lorem.
    </P>
    </div>
  </div>
  <Heading tag="h1" class='mb-4 text-center'>Chemical Products Offered across Industries</Heading>

  <div class="grid grid-cols-3 gap-4">
    <div class="md:w-auto p-4">
      <Card img="/images/image-1.webp" reverse={vCard} size="md">
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

    <div class="w-full p-4">
      <Card img="/images/image-1.webp" reverse={vCard} size="auto">
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

    <div class="w-full p-4">
      <Card img="/images/image-1.webp" reverse={vCard} size="auto">
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

  <!--  <Skeleton size="md" class="my-8" />-->
  <!--  <Skeleton size="lg" class="my-8" />-->
  <!--  <Skeleton size="xl" class="my-8" />-->
  <!--  <Skeleton size="xxl" class="mt-8 mb-2.5" />-->
</slot>

<style>

</style>
