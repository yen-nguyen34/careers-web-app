<template>
  <form
    class="flex h-12 w-full items-center rounded-3xl border border-solid border-brand-gray-3"
  >
    <div class="flex h-full flex-1 flex-wrap text-base font-light">
      <label class="absolute left-0 -top-10">Role</label>
      <span>
        <input class="w-full text-lg font-normal focus:outline-none" />
      </span>
      <span>
        <img :src="searchIcon" class="w-5 h-5 mr-3" />
      </span>
    </div>
  </form>
</template>

<script>
import searchIcon from "../assets/loupe.png";
export default {
  name: "SearchJobForm",
  data() {
    return {
      searchIcon,
    };
  },
};
</script>
