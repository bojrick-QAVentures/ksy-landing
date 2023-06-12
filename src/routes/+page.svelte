<script>
  import {
    Card,
    Button,
    Heading,
    P,
    Img,
    Tabs,
    TabItem,
    TextPlaceholder,
    Toggle,
    Skeleton,
    ImagePlaceholder, Timeline, TimelineItem
  } from 'flowbite-svelte';

  // <script>
  // import { CardPlaceholder, ImagePlaceholder, ListPlaceholder, Skeleton, TestimonialPlaceholder, TextPlaceholder, VideoPlaceholder, WidgetPlaceholder } from 'flowbite-svelte'

  let vCard = false;
  import { Carousel } from 'flowbite-svelte';
  let showThumbs = false;
  let showCaptions = false;
  let hCard = false;

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
    <Carousel class="w-full h-auto" {images} loop {showCaptions} {showThumbs} duration="3000" />
  </div>

  <div class="flex flex-wrap bg-[#1da1f2] mb-5 w-full h-auto">
    <div class="w-full md:w-1/2">
      <Img
        class="w-full h-auto"
        src="/images/Fragrance Sample.jpg"
        alt="sample 1"
        size="max-w-lg"
        alignment="mx-auto"
      />
    </div>
    <div class="w-full md:w-1/2">
      <Heading class="p-8" tag="h2">Who We Are</Heading>

      <P class="px-8 py-4">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
        magna aliqua. Amet cursus sit amet dictum sit. Quis enim lobortis scelerisque fermentum dui faucibus in. Mattis
        vulputate enim nulla aliquet porttitor lacus luctus accumsan. Ipsum dolor sit amet consectetur adipiscing elit.
        Euismod nisi porta lorem mollis aliquam ut porttitor. Tortor consequat id porta nibh. Tortor condimentum lacinia
        quis vel eros donec ac odio. Elementum sagittis vitae et leo duis ut diam quam nulla. Vel turpis nunc eget
        lorem.
      </P>
    </div>
  </div>
  <Heading tag="h2" class="mb-4 text-center">Chemical Products Offered across Industries</Heading>

  <div class="flex flex-wrap justify-center gap-5">
    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4">
      <Card img="/images/researching-laboratory.jpg" reverse={vCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Noteworthy technology acquisitions 2021</h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
        </p>
        <Button>
          Read more <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 ml-2"><path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" /></svg>
        </Button>
      </Card>
      <!--    <Toggle bind:checked={vCard} class="mt-4 italic dark:text-gray-500">Reverse</Toggle>-->
    </div>

    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4">
      <Card img="/images/researching-laboratory.jpg" reverse={vCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Noteworthy technology acquisitions 2021</h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
        </p>
        <Button>
          Read more <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 ml-2"><path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" /></svg>
        </Button>
      </Card>
      <!--    <Toggle bind:checked={vCard} class="mt-4 italic dark:text-gray-500">Reverse</Toggle>-->
    </div>


    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4">
      <Card img="/images/researching-laboratory.jpg" reverse={vCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Noteworthy technology acquisitions 2021</h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
        </p>
        <Button>
          Read more <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 ml-2"><path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" /></svg>
        </Button>
      </Card>
      <!--    <Toggle bind:checked={vCard} class="mt-4 italic dark:text-gray-500">Reverse</Toggle>-->
    </div>


    <Heading tag="h2" class="mb-4 text-center">Our Strengths</Heading>
    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4">
      <Card img="/images/F100014962.jpg" href="/" horizontal reverse={hCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
          Noteworthy technology acquisitions 2021
        </h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
        </p>
      </Card>
      <!--        <Toggle bind:checked={hCard} class="mt-4 italic dark:text-gray-500">Reverse</Toggle>-->
    </div>
    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4">
      <Card img="/images/F100014962.jpg" href="/" horizontal reverse={hCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
          Noteworthy technology acquisitions 2021
        </h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
        </p>
      </Card>
      <!--        <Toggle bind:checked={hCard} class="mt-4 italic dark:text-gray-500">Reverse</Toggle>-->
    </div>
    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4">
      <Card img="/images/F100014962.jpg" href="/" horizontal reverse={hCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
          Noteworthy technology acquisitions 2021
        </h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
        </p>
      </Card>
      <!--        <Toggle bind:checked={hCard} class="mt-4 italic dark:text-gray-500">Reverse</Toggle>-->
    </div>
  </div>

  <Tabs class = "flex mt-10 justify-center">
    <TabItem open>
      <span slot="title">Profile</span>
      <Timeline>
        <TimelineItem title="Application UI code in Tailwind CSS" date="February 2022">
          <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">
            Get access to over 20+ pages including a dashboard layout, charts, kanban board, calendar,
            and pre-order E-commerce & Marketing pages.
          </p>
          <Button color="alternative">Learn more
            <svg class="ml-2 w-3 h-3" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M12.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-2.293-2.293a1 1 0 010-1.414z" clip-rule="evenodd" /></svg>
          </Button>
        </TimelineItem>
        <TimelineItem title="Application UI code in Tailwind CSS" date="March 2022">
          <p class="text-base font-normal text-gray-500 dark:text-gray-400">All of the pages and components are first designed in Figma and we keep a parity between the two versions even as we update the project.</p>
        </TimelineItem>
        <TimelineItem title="Application UI code in Tailwind CSS" date="April 2022">
          <p class="text-base font-normal text-gray-500 dark:text-gray-400">Get started with dozens of web components and interactive elements built on top of Tailwind CSS.</p>
        </TimelineItem>
      </Timeline>
    </TabItem>
    <TabItem>
      <span slot="title">Dashboard</span>
      <p class="text-sm text-gray-500 dark:text-gray-400"><b>Dashboard:</b> Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
      <div class="flex flex-wrap bg-[#1da1f2] mb-5 w-full h-auto">
        <div class="w-full md:w-1/2">
          <Img
                  class="w-full h-auto"
                  src="/images/Fragrance Sample.jpg"
                  alt="sample 1"
                  size="max-w-lg"
                  alignment="mx-auto"
          />
        </div>
        <div class="w-full md:w-1/2">
          <Heading class="p-8" tag="h2">Who We Are</Heading>

          <P class="px-8 py-4">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
            magna aliqua. Amet cursus sit amet dictum sit. Quis enim lobortis scelerisque fermentum dui faucibus in. Mattis
            vulputate enim nulla aliquet porttitor lacus luctus accumsan. Ipsum dolor sit amet consectetur adipiscing elit.
            Euismod nisi porta lorem mollis aliquam ut porttitor. Tortor consequat id porta nibh. Tortor condimentum lacinia
            quis vel eros donec ac odio. Elementum sagittis vitae et leo duis ut diam quam nulla. Vel turpis nunc eget
            lorem.
          </P>
        </div>
      </div>
    </TabItem>
    <TabItem>
      <span slot="title">Settings</span>
      <p class="text-sm text-gray-500 dark:text-gray-400"><b>Settings:</b> Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
      <Timeline>
        <TimelineItem title="Application UI code in Tailwind CSS" date="February 2022">
          <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">
            Get access to over 20+ pages including a dashboard layout, charts, kanban board, calendar,
            and pre-order E-commerce & Marketing pages.
          </p>
          <Button color="alternative">Learn more
            <svg class="ml-2 w-3 h-3" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M12.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-2.293-2.293a1 1 0 010-1.414z" clip-rule="evenodd" /></svg>
          </Button>
        </TimelineItem>
        <TimelineItem title="Application UI code in Tailwind CSS" date="March 2022">
          <p class="text-base font-normal text-gray-500 dark:text-gray-400">All of the pages and components are first designed in Figma and we keep a parity between the two versions even as we update the project.</p>
        </TimelineItem>
        <TimelineItem title="Application UI code in Tailwind CSS" date="April 2022">
          <p class="text-base font-normal text-gray-500 dark:text-gray-400">Get started with dozens of web components and interactive elements built on top of Tailwind CSS.</p>
        </TimelineItem>
      </Timeline>
    </TabItem>
    <TabItem>
      <span slot="title">Users</span>
      <p class="text-sm text-gray-500 dark:text-gray-400"><b>Users:</b> Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
      <Timeline>
        <TimelineItem title="Application UI code in Tailwind CSS" date="February 2022">
          <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">
            Get access to over 20+ pages including a dashboard layout, charts, kanban board, calendar,
            and pre-order E-commerce & Marketing pages.
          </p>
          <Button color="alternative">Learn more
            <svg class="ml-2 w-3 h-3" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M12.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-2.293-2.293a1 1 0 010-1.414z" clip-rule="evenodd" /></svg>
          </Button>
        </TimelineItem>
        <TimelineItem title="Application UI code in Tailwind CSS" date="March 2022">
          <p class="text-base font-normal text-gray-500 dark:text-gray-400">All of the pages and components are first designed in Figma and we keep a parity between the two versions even as we update the project.</p>
        </TimelineItem>
        <TimelineItem title="Application UI code in Tailwind CSS" date="April 2022">
          <p class="text-base font-normal text-gray-500 dark:text-gray-400">Get started with dozens of web components and interactive elements built on top of Tailwind CSS.</p>
        </TimelineItem>
      </Timeline>
    </TabItem>
  </Tabs>

  <Heading tag="h2" class="mb-4 text-center">Chemical Products Offered across Industries</Heading>

  <div class="flex flex-wrap justify-center gap-5">
    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4">
      <Card img="/images/pexels-pixabay-356040.jpg" reverse={vCard} size="md">
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

    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4">
      <Card img="/images/pexels-pixabay-356040.jpg" reverse={vCard} size="auto">
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

    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4">
      <Card img="/images/pexels-pixabay-356040.jpg" reverse={vCard} size="auto">
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

    <Heading tag="h2" class="mb-4 text-center">Our Strengths</Heading>
    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4">
      <Card img="/images/pexels-pixabay-356040.jpg" href="/" horizontal reverse={hCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
          Noteworthy technology acquisitions 2021
        </h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
        </p>
      </Card>
      <!--        <Toggle bind:checked={hCard} class="mt-4 italic dark:text-gray-500">Reverse</Toggle>-->
    </div>
    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4">
      <Card img="/images/pexels-pixabay-356040.jpg" href="/" horizontal reverse={hCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
          Noteworthy technology acquisitions 2021
        </h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
        </p>
      </Card>
      <!--        <Toggle bind:checked={hCard} class="mt-4 italic dark:text-gray-500">Reverse</Toggle>-->
    </div>
    <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/4">
      <Card img="/images/pexels-pixabay-356040.jpg" href="/" horizontal reverse={hCard}>
        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
          Noteworthy technology acquisitions 2021
        </h5>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
          Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
        </p>
      </Card>
      <!--        <Toggle bind:checked={hCard} class="mt-4 italic dark:text-gray-500">Reverse</Toggle>-->
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
