<script lang="ts">
  import { Label, Select } from 'flowbite-svelte';
  let selected;

  let selection = [
    { value: 'inorganic', name: 'Incorganic' },
    { value: 'organic', name: 'Organic' },
    { value: undefined, name: 'All' }
  ];

  import {
    Table,
    TableBody,
    TableBodyCell,
    TableBodyRow,
    TableHead,
    TableHeadCell,
    TableSearch
  } from 'flowbite-svelte';
  let searchTerm = '';
  let items = [
    { id: 1, maker: 'Toyota', type: 'ABC', make: 2017 },
    { id: 2, maker: 'Ford', type: 'CDE', make: 2018 },
    { id: 3, maker: 'Volvo', type: 'FGH', make: 2019 },
    { id: 4, maker: 'Saab', type: 'IJK', make: 2020 }
  ];
  $: filteredItems = items.filter((item) => item.maker.toLowerCase().indexOf(searchTerm.toLowerCase()) !== -1);
</script>

<Label
  >Select an option
  <Select class="mt-2" items={selection} bind:value={selected} />
</Label>

{#if selected == null || selected === 'inorganic'}
  <hr class="my-5" />
  <h1 class="text-3xl text-white">Inorganic</h1>
  <TableSearch placeholder="Search by maker name" hoverable={true} bind:inputValue={searchTerm}>
    <TableHead>
      <TableHeadCell>ID</TableHeadCell>
      <TableHeadCell>Maker</TableHeadCell>
      <TableHeadCell>Type</TableHeadCell>
      <TableHeadCell>Make</TableHeadCell>
    </TableHead>
    <TableBody class="divide-y">
      {#each filteredItems as item}
        <TableBodyRow>
          <TableBodyCell>{item.id}</TableBodyCell>
          <TableBodyCell>{item.maker}</TableBodyCell>
          <TableBodyCell>{item.type}</TableBodyCell>
          <TableBodyCell>{item.make}</TableBodyCell>
        </TableBodyRow>
      {/each}
    </TableBody>
  </TableSearch>
{/if}

{#if selected == null || selected === 'organic'}
  <hr class="my-5" />
  <h1 class="text-3xl text-white">Organic</h1>
  <TableSearch placeholder="Search by maker name" hoverable={true} bind:inputValue={searchTerm}>
    <TableHead>
      <TableHeadCell>ID</TableHeadCell>
      <TableHeadCell>Maker</TableHeadCell>
      <TableHeadCell>Type</TableHeadCell>
      <TableHeadCell>Make</TableHeadCell>
    </TableHead>
    <TableBody class="divide-y">
      {#each filteredItems as item}
        <TableBodyRow>
          <TableBodyCell>{item.id}</TableBodyCell>
          <TableBodyCell>{item.maker}</TableBodyCell>
          <TableBodyCell>{item.type}</TableBodyCell>
          <TableBodyCell>{item.make}</TableBodyCell>
        </TableBodyRow>
      {/each}
    </TableBody>
  </TableSearch>
{/if}

<style lang="css">
</style>
