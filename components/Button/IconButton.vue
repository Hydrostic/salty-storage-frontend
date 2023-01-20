<template>
  <div
    class="w-8 h-8 grid mx-1 hover:bg-gray-200 rounded-lg items-center justify-center"
    ref="btn"
  >
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "IconButton",
  data() {
    return {
      className: "text-slate-800 m-auto",
      size: "18",
    };
  },
  mounted() {
    if (this.$refs.btn.children.length === 1) {
      this.$refs.btn.children[0].classList.add("text-slate-800");
    }
  },
  props: {
    disabled: {
      type: Boolean,
    },
    selected: {
      type: Boolean,
    },
  },
};
</script>

<style scoped></style>
