<template>
  <div
    class="absolute top-16 right-0 h-full w-80 p-4 flex flex-col items-center px-8 select-none"
  >
    <img src="http://localhost:1145/IMG_0532.png" class="rounded-lg shadow" />
    <div class="my-5 grid grid-rows-2 grid-flow-col w-full">
      <PhotoIcon size="22" class="text-indigo-600 row-span-2 mt-2 mr-2" />
      <span
        class="text-sm font-medium col-span-2 select-text text-ellipsis overflow-hidden whitespace-nowrap"
        >{{ data.name.split(".")[0] }}</span
      >
      <span
        class="text-xs text-gray-400 row-span-1 col-span-1 text-ellipsis overflow-hidden whitespace-nowrap"
        >{{
          data.name.split(".").length > 1 ? data.name.split(".")[1] : "未知类型"
        }}</span
      >
    </div>
    <div class="h-10 w-full grid grid-rows-2 my-1">
      <span class="text-xs font-semibold text-indigo-600"> 大小 </span>
      <span class="text-sm font-medium">{{ fileSize }}</span>
    </div>
    <div class="h-10 w-full grid grid-rows-2 my-1">
      <span class="text-xs font-semibold text-indigo-600"> 创建时间 </span>
      <span class="text-sm font-medium">1 天前</span>
    </div>
    <div class="h-10 w-full grid grid-rows-2 my-1">
      <span class="text-xs font-semibold text-indigo-600"> 修改时间 </span>
      <span class="text-sm font-medium">1 天前</span>
    </div>
    <div class="h-10 w-full grid grid-rows-2 my-1">
      <span class="text-xs font-semibold text-indigo-600"> 尺寸 </span>
      <span class="text-sm font-medium">1024*1024</span>
    </div>
    <div class="h-10 w-full grid grid-rows-2 my-1">
      <span class="text-xs font-semibold text-indigo-600"> 色彩通道 </span>
      <span class="text-sm font-medium">sRGB</span>
    </div>
  </div>
</template>

<script setup>
import { PhotoIcon } from "vue-tabler-icons";
const { data } = defineProps(["data"]);

let fileSize = computed(() => {
  if (data.size < 1000) return `${data.size} KB`;
  else if (data.size < 1000 * 1000)
    return `${Math.round((data.size / 1000) * 100) / 100} MB`;
  else return `${Math.round((data.size / 1000 / 1000) * 100) / 100} GB`;
});
</script>

<style scoped></style>
