<template>
  <div>
    <div class="search-container p-2 w-[890px] flex justify-start">
      <div class="space-x-8 flex border-r p-3 border-[#E6E6E6]">
        <div>All</div>
        <img src="/icons/arrow-down-brown.svg" alt="" />
      </div>
      <div class="py-3 px-4">
        <input
          type="text"
          class="bg-transparent focus:outline-none"
          id="search-input"
          placeholder="Search for anything here"
        />
      </div>
      <div class="p-3 flex justify-end">
        <img src="/icons/Search.svg" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.search-container {
  border: 2px solid #fff;
  background: #f1f1f1;
  color: #999;
}

#search-input {
  width: 700px;
}
</style>
