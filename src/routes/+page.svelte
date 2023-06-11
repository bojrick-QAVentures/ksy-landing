<script>
  import { Carousel } from 'flowbite-svelte'

  // ./imageData/+server.js has the following
   const images = [
    {
      id: 0,
      name: "Cosmic timetraveler",
      imgurl: "https://placehold.co/1600x1900",
      attribution: "cosmic-timetraveler-pYyOZ8q7AII-unsplash.com",
    },
    {
      id: 1,
      name: "Cristina Gottardi",
      imgurl: "https://placehold.co/1600x1900",
      attribution: "cristina-gottardi-CSpjU6hYo_0-unsplash.com",
    }
  ];
</script>

<slot>
  <h1>Welcome to SvelteKit</h1>

  <div class="max-w-4xl">
    <Carousel {images} />
  </div>
</slot>
