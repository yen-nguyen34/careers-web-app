<template>
  <header class="w-full text-sm">
    <div class="fixed left-0 top-0 h-16 w-full bg-white">
      <div
        class="mx-auto flex h-full flex-nowrap border-b border-solid border-brand-gray-1 px-8"
      >
        <a :href="url" class="flex h-full items-center text-xl">{{
          company
        }}</a>

        <nav class="ml-12 h-full">
          <ul class="flex h-full list-none">
            <li
              v-for="menuItem in menuItems"
              :key="menuItem"
              class="ml-9 h-full first:ml-0"
            >
              <a href="" class="flex h-full items-center py-2.5">{{
                menuItem
              }}</a>
            </li>
          </ul>
        </nav>

        <div class="ml-auto flex h-full items-center">
          <ProfileImage v-if="isLogined" />
          <ActionButton text="Sign In" v-else @click="logInUser" />
        </div>
      </div>
      <TheSubNav />
    </div>
  </header>

  <main class="mt-36">
    <TheHero />
  </main>
</template>

<script>
import ActionButton from "../Shared/ActionButton.vue";
import ProfileImage from "./ProfileImage.vue";
import TheSubNav from "./TheSubNav.vue";
import TheHero from "../SearchJob/TheHero.vue";
export default {
  name: "MainNav",
  components: {
    ActionButton,
    ProfileImage,
    TheSubNav,
    TheHero,
  },
  data() {
    return {
      company: "Bobo Careers",
      url: "https://careers.google.com",
      menuItems: [
        "Teams",
        "Locations",
        "Life at Bobo Corp",
        "How we hire",
        "Students",
        "Jobs",
      ],
      isLogined: false,
    };
  },
  methods: {
    logInUser() {
      this.isLogined = true;
    },
  },
};
</script>
