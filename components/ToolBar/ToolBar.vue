<template>
<div class="absolute top-0 h-16 pl-56 p-4 w-full flex flex-wrap items-center justify-around">
  <div class="flex h-8 items-center ml-5">
    <span class="text-base text-slate-300 mx-1">文件</span>
    <ChevronRightIcon size="20"/>
    <span class="text-base font-bold text-gray-700 mx-1">文件夹 1</span>
  </div>
  <div class="grow h-8"></div>
  <div class="flex h-8">
    <div class="w-8 h-8 flex mx-1 hover:bg-gray-200 rounded-lg">
      <UploadIcon class="text-slate-800 m-auto" size="18"/>
    </div>
    <div class="w-8 h-8 flex mx-1 hover:bg-gray-200 rounded-lg">
      <LinkIcon class="text-slate-800 m-auto" size="18"/>
    </div>
    <div class="w-8 h-8 flex mx-1 hover:bg-gray-200 rounded-lg">
      <CornerDownRightIcon class="text-slate-800 m-auto" size="18"/>
    </div>
    <div class="w-8 h-8 flex mx-1 hover:bg-gray-200 rounded-lg">
      <TrashIcon class="text-slate-800 m-auto" size="18"/>
    </div>
    <div class="w-3"></div>
    <div class="w-8 h-8 flex mx-1 hover:bg-gray-200 rounded-lg">
      <ListDetailsIcon class="text-slate-800 m-auto" size="18"/>
    </div>
    <div class="w-8 h-8 flex mx-1 bg-indigo-100 rounded-lg">
      <InfoCircleIcon class="m-auto text-indigo-600 " size="18"/>
    </div>
  </div>
</div>
</template>

<script>
import { UploadIcon,LinkIcon,CornerDownRightIcon,TrashIcon,ListDetailsIcon,InfoCircleIcon,ChevronRightIcon  } from "vue-tabler-icons";

export default {
  components:{
    UploadIcon,
    LinkIcon,
    CornerDownRightIcon,
    TrashIcon,
    ListDetailsIcon,
    InfoCircleIcon,
    ChevronRightIcon
  }
}
</script>

<style scoped>

</style>