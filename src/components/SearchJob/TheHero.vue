<template>
  <section class="flex h-screen flex-col bg-white pb-20 pt-10">
    <div class="grid grid-cols-12">
      <div class="col-span-5 col-start-2">
        <TheHeadLine />
      </div>
    </div>
  </section>
</template>

<script>
import TheHeadLine from "./TheHeadLine.vue";

export default {
  name: "TheHero",
  components: {
    TheHeadLine,
  },
};
</script>
