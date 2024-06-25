<template>
  <input
    type="text"
    :value="modelValue"
    class="w-full text-lg font-normal focus:outline-nones"
    @input="handleInput"
    required
  />
</template>

<script>
export default {
  name: "TextInput",
  data() {
    return {
      modelName: "",
    };
  },
};
</script>
