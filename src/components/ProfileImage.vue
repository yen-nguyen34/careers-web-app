<template>
  <img
    id="avatarButton"
    type="button"
    data-dropdown-toggle="userDropdown"
    data-dropdown-placement="bottom-start"
    class="w-11 h-11 rounded-full cursor-pointer"
    :src="profileImg"
    alt="User dropdown"
  />
  <ProfileInfo />
</template>

<script>
import profileImg from "../assets/human.png";
import ProfileInfo from "./ProfileInfo.vue";
export default {
  name: "ProfileImage",
  components: {
    ProfileInfo,
  },
  data() {
    return {
      profileImg,
    };
  },
  //   methods: {
  //     toggleDropDown() {
  //       this.showDropDown = true;
  //     },
  //   },
};
</script>
