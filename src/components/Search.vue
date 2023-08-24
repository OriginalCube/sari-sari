<script lang="ts">
import SearchIcons from "./search/SearchIcons.vue";
export default { name: "Search", components: { SearchIcons } };
</script>

<template>
  <div class="w-full h-auto flex flex-col gap-2">
    <div class="w-full flex items-center justify-center gap-4">
      <input
        type="text"
        class="w-4/6 p-2 text-xl outline-none border-2 border-black"
        placeholder="Enter product name"
      />
      <button class="text-md">Search</button>
    </div>
    <div class="w-full flex items-center justify-evenly">
      <SearchIcons name="Veggies" image="vegetable" />
      <SearchIcons name="Bread" image="bread" />
      <SearchIcons name="Fruits" image="fruits" />
      <SearchIcons name="Poultry" image="poultry" />
      <SearchIcons name="Grain" image="wheat" />
      <SearchIcons name="Meat" image="meat" />
    </div>
  </div>
</template>

<style></style>
