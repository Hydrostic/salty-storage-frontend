<template>
  <div
    class="flex flex-col gap-1 items-center justify-start pt-10 w-56 absolute inset-y-0 left-0 bg-slate-100 px-3"
  >
    <slot></slot>
    <div class="w-full mx-2 flex items-center rounded-lg py-2.5 bg-indigo-100">
      <FileIcon class="m-0 mr-4 ml-5 text-indigo-600" size="22" />
      <span class="text-sm font-bold text-indigo-600">文件</span>
    </div>
    <div
      class="w-full mx-2 flex items-center hover:bg-gray-200 rounded-lg py-2.5"
    >
      <PhotoIcon class="text-slate-800 m-0 mr-4 ml-5" size="22" />
      <span class="text-sm font-bold text-slate-900">相册</span>
    </div>
    <div
      class="w-full mx-2 flex items-center hover:bg-gray-200 rounded-lg py-2.5"
    >
      <StarIcon class="text-slate-800 m-0 mr-4 ml-5" size="22" />
      <span class="text-sm font-bold text-slate-900">收藏</span>
    </div>
    <div
      class="w-full mx-2 flex items-center hover:bg-gray-200 rounded-lg py-2.5"
    >
      <ShareIcon class="text-slate-800 m-0 mr-4 ml-5" size="22" />
      <span class="text-sm font-bold text-slate-900">分享</span>
    </div>
    <div
      class="w-full mx-2 flex items-center hover:bg-gray-200 rounded-lg py-2.5 mt-3"
    >
      <TrashIcon class="text-slate-800 m-0 mr-4 ml-5" size="22" />
      <span class="text-sm font-bold text-slate-900">回收站</span>
    </div>
    <!--    <div class="mt-5">-->
    <!--      <img src="http://localhost:1145/IMG_0532.png" class="rounded-lg w-10 h-10"/>-->
    <!--    </div>-->
    <!--    <div class="w-10 h-10 mb-5 hover:bg-gray-200 rounded-lg grid">-->
    <!--      <BellIcon class="text-slate-900 place-self-center" stroke-width="1"/>-->
    <!--    </div>-->
    <!--    <div class="w-8 h-8">-->
    <!--      <ServerIcon class="text-slate-800 m-auto" stroke-width="1.5"/>-->
    <!--    </div>-->
    <!--    <div class="w-8 h-8">-->
    <!--      <SettingsIcon class="text-slate-800 m-auto" stroke-width="1.5"/>-->
    <!--    </div>-->
    <!--    <div class="w-8 h-8">-->
    <!--      <AdjustmentsHorizontalIcon class="text-slate-800 m-auto" stroke-width="1.5"/>-->
    <!--    </div>-->
    <div class="w-full h-16 px-5 absolute bottom-10">
      <div
        class="w-full flex items-center hover:bg-gray-200 rounded-lg py-1 my-3"
      >
        <ServerIcon class="text-slate-800 mr-4 ml-1" size="18" />
        <span class="text-sm font-bold text-slate-900">Webdav 设置</span>
      </div>
      <div class="w-full h-1 bg-slate-200 rounded-full">
        <div class="bg-indigo-600 h-full rounded-full" style="width: 10%"></div>
      </div>
      <span class="text-xs font-medium text-slate-800"
        >已用 <b>100GB/1T</b></span
      >
    </div>
  </div>
</template>

<script>
import {
  StarIcon,
  FileIcon,
  PhotoIcon,
  ShareIcon,
  TrashIcon,
  ServerIcon,
} from "vue-tabler-icons";
export default {
  components: {
    StarIcon,
    FileIcon,
    PhotoIcon,
    ShareIcon,
    TrashIcon,
    ServerIcon,
  },
};
</script>
