<template>
  <div
    class="mx-auto flex h-16 flex-nowrap border-b border-solid border-brand-gray-1 px-8"
  >
    <div class="flex items-center">
      <span>
        <img :src="searchIcon" class="w-5 h-5 mr-3" />
      </span>
      <span>
        <span class="text-lime-700 font-semibold">1536</span>
        jobs matched
      </span>
    </div>
  </div>
</template>

<script>
import searchIcon from "../assets/loupe.png";
export default {
  name: "TheSubNav",
  data() {
    return {
      searchIcon,
    };
  },
};
</script>
