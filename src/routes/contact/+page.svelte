<!--<script>-->
<!--  -->
<!--</script>-->

<script>
  import { Label, Input } from 'flowbite-svelte';
  import { Button } from 'flowbite-svelte';
  const btn1 = () => {
    alert('You clicked btn1.');
  };
  const btn2 = () => {
    alert('You touched btn2.');
  };
</script>

<slot>
  <div class="flex flex-wrap">
    <div class="mb-6">
      <Label for="large-input" class="block mb-2">First Name</Label>
      <Input id="large-input" size="lg" placeholder="First Name" />
    </div>
    <div class="mb-6">
      <Label for="large-input" class="block mb-2">Last Name</Label>
      <Input id="large-input" size="lg" placeholder="Last Name" />
    </div>
  </div>
  <div class="mb-6">
    <Label for="default-input" class="block mb-2">Default input</Label>
    <Input id="default-input" placeholder="Default input" />
  </div>
  <div class="mb-6">
    <Label for="large-input" class="block mb-2">Small input</Label>
    <Input size="sm" placeholder="Small input" label="Small input" />
  </div>

  <Button on:click={btn1}>Submit</Button>
  <Button on:touchstart={btn2}>Clear</Button>
</slot>
