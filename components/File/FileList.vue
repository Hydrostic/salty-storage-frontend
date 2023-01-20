<template>
  <div
    class="grid grid-flow-row gap-1 overflow-y-auto overflow-x-hidden h-full select-none"
    v-click-outside="onClickOutside"
  >
    <div
      class="rounded-lg h-12 flex items-center justify-around"
      :class="selectedItem === i ? 'bg-indigo-100' : 'hover:bg-gray-200'"
      v-for="i in 150"
      :key="i"
      @click="selectedItem = i"
    >
      <FileIcon
        class="ml-4"
        :class="selectedItem === i ? 'text-indigo-600' : ''"
      />

      <span
        class="mx-4 grow text-sm font-medium"
        :class="selectedItem === i ? 'text-indigo-600' : ''"
        >image {{ i }}</span
      >
      <span
        class="mx-4 text-xs font-medium text-gray-500"
        :class="selectedItem === i ? 'text-indigo-600' : ''"
        >{{ i }} 天前</span
      >
      <span
        class="mx-4 text-xs font-medium text-gray-500"
        :class="selectedItem === i ? 'text-indigo-600' : ''"
        >114.514 KB</span
      >
    </div>
  </div>
  <slot name="metadata" :metadata="data.list[0]"></slot>
</template>

<script setup>
import { FileIcon } from "vue-tabler-icons";
import vClickOutside from "vue-click-outside";
let selectedItem = ref(null);
let data = reactive({
  list: [
    {
      id: "1111111",
      name: "冬之花11111111111111111111111111111111111111.jpg",
      category: "image",
      size: 10756785,
    },
  ],
});
let onClickOutside = () => {
  selectedItem.value = null;
};
</script>

<style scoped></style>
