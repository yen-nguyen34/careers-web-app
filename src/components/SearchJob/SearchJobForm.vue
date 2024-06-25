<template>
  <form
    class="flex h-12 items-center rounded-3xl border border-solid border-brand-gray-3"
  >
    <img :src="searchIcon" class="w-5 h-5 mr-3" />
    <div class="flex h-full flex-1 flex-nowrap text-base font-light">
      <div class="relative flex h-full flex-1 items-center pl-3">
        <label class="absolute -top-10 left-0">Role</label>
        <text-input v-model="role" placeholder="Software Engineer" />
      </div>

      <span
        class="flex h-full items-center border-l border-r border-brand-gray-1"
      >
        in
      </span>

      <img :src="locationIcon" class="w-5 h-5 mr-3" />
      <div class="relative flex h-full flex-1 items-center pl-3">
        <label class="absolute -top-10 left-0">Where?</label>
        <text-input v-model="location" placeholder="Los Angeles" />
      </div>
    </div>

    <ActionButton text="Search" type="secondary" class="rounded-r-3xl" />
  </form>
</template>

<script>
import searchIcon from "../assets/loupe.png";
import locationIcon from "../assets/location.png";
import ActionButton from "../Shared/ActionButton.vue";
export default {
  name: "SearchJobForm",
  components: {
    ActionButton,
  },
  data() {
    return {
      searchIcon,
      locationIcon,
      role: "",
      location: "",
    };
  },
};
</script>
