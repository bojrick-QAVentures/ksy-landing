<script lang="ts">
  import type { PageData } from './$types';
  import {
    TableBody,
    TableBodyCell,
    TableBodyRow,
    TableHead,
    TableHeadCell,
    TableSearch
  } from 'flowbite-svelte';

  export let data: PageData;
  export let items = data.items ?? [];
  let searchTerm = '';
  $: filteredItems = items.filter((item) => item.maker.toLowerCase().indexOf(searchTerm.toLowerCase()) !== -1);
</script>

<TableSearch placeholder="Search by maker name" hoverable={true} bind:inputValue={searchTerm} shadow divClass='products'>
    <TableHead theadClass="m-4">
      <TableHeadCell>ID</TableHeadCell>
      <TableHeadCell>Maker</TableHeadCell>
      <TableHeadCell>Type</TableHeadCell>
      <TableHeadCell>Make</TableHeadCell>
    </TableHead>
    <TableBody>
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

<style lang="css">
</style>
