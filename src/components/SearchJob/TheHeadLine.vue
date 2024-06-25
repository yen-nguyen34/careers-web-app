<template>
  <section>
    <h1 class="mb-14 text-8xl font-bold tracking-tighter">
      <span :class="actionClasses">{{ action }}</span>
      <br />
      for everyone
    </h1>
    <h2 class="text-3xl font-light">Find your next job at Bobo Corp.</h2>
    <div class="mb-4">
      <SearchJobForm />
    </div>
  </section>
</template>

<script>
import SearchJobForm from "./SearchJobForm.vue";
export default {
  name: "TheHeadLine",
  components: {
    SearchJobForm,
  },
  data() {
    return {
      action: "Build",
      interval: null,
    };
  },
  computed: {
    actionClasses() {
      return {
        build: this.action.toLowerCase() === "build",
        create: this.action.toLowerCase() === "create",
        design: this.action.toLowerCase() === "design",
        code: this.action.toLowerCase() === "code",
      };
    },
  },
  created() {
    this.changeTitle();
  },
  beforeUnmount() {
    clearInterval(this.interval);
  },
  methods: {
    changeTitle() {
      let index = 0;
      const actions = ["Build", "Create", "Design", "Code"];
      this.interval = setInterval(() => {
        this.action = actions[index];
        console.log(index, this.action);
        index = (index + 1) % actions.length;
      }, 3000);
    },
  },
};
</script>

<style scoped>
.build {
  color: #1a73e8;
}

.create {
  color: #34a853;
}

.design {
  color: #f9ab00;
}

.code {
  color: #d93025;
}
</style>
