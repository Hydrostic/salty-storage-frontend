<template>
  <div
    class="w-80 absolute bottom-10 right-10 rounded-lg shadow-lg select-none bg-white z-50 flex flex-col overflow-hidden"
    :class="showDetail ? 'large' : 'small'"
  >
    <!--    <div-->
    <!--      class="flex items-center w-full rounded-lg border-indigo-600 border-2 h-12"-->
    <!--    >-->
    <!--      <BoltIcon class="text-indigo-600 m-3 animate-bounce mt-4" />-->
    <!--      <span class="text-sm font-medium"-->
    <!--        ><strong>3</strong> 个文件上传中...</span-->
    <!--      >-->
    <!--      <div class="grow"></div>-->
    <!--      <div-->
    <!--        class="w-8 h-8 flex mx-1 hover:bg-gray-200 rounded-lg"-->
    <!--        @click="showDetail = !showDetail"-->
    <!--      >-->
    <!--        <ChevronDownIcon-->
    <!--          class="text-slate-800 m-auto"-->
    <!--          :class="showDetail ? 'icon-up' : 'icon-down'"-->
    <!--          size="18"-->
    <!--        />-->
    <!--      </div>-->
    <!--    </div>-->
    <div class="flex items-center w-full rounded-lg h-12">
      <CircleCheckIcon class="text-green-600 m-3" />
      <span class="text-sm font-medium"><strong>3</strong> 个文件上传完毕</span>
      <div class="grow"></div>
      <div
        class="w-8 h-8 flex mx-1 hover:bg-gray-200 rounded-lg"
        @click="showDetail = !showDetail"
      >
        <ChevronDownIcon
          class="text-slate-800 m-auto"
          :class="showDetail ? 'icon-up' : 'icon-down'"
          size="18"
        />
      </div>
    </div>
    <div
      class="grid grid-cols-1 auto-rows-max w-full transition-opacity overflow-y-scroll"
      :class="showDetail ? 'opacity-100' : 'opacity-0'"
    >
      <div
        class="h-12 flex items-center px-3 my-1 hover:bg-slate-100 rounded-lg mx-1"
      >
        <div class="flex w-full justify-start items-center">
          <MovieIcon size="22" class="text-indigo-600 row-span-2 mr-4" />
          <div class="flex flex-col justify-start w-full">
            <span class="text-sm font-medium text-slate-800 col-span-1"
              >冬之花.mp4</span
            >
            <div class="flex items-center col-span-1">
              <span class="text-xs text-gray-400"
                >114.5 MB 已上传至 <a class="text-blue-500">/homo</a></span
              >
            </div>
          </div>
        </div>
      </div>
      <div
        class="h-12 flex items-center px-3 my-1 hover:bg-slate-100 rounded-lg mx-1"
        v-for="i in 10"
        :key="i"
      >
        <div class="flex w-full justify-start items-center">
          <MovieIcon size="22" class="text-indigo-600 row-span-2 mr-4" />
          <div class="flex flex-col justify-start w-full">
            <span class="text-sm font-medium text-slate-800 col-span-1"
              >冬之花.mp4</span
            >
            <div class="flex items-center col-span-1">
              <div class="h-1 bg-slate-200 rounded-full grow mr-2">
                <div
                  class="bg-indigo-600 h-full rounded-full"
                  style="width: 10%"
                ></div>
              </div>
              <span class="text-xs text-gray-400">11.45 KB/s</span>
            </div>
          </div>
        </div>
      </div>
      <div
        class="h-12 flex items-center justify-center px-3 my-1 hover:bg-slate-100 rounded-lg mx-1 border-dashed border-2"
      >
        <PlusIcon class="text-slate-300" />
      </div>
    </div>
  </div>
</template>

<script>
import {
  BoltIcon,
  ChevronDownIcon,
  ChevronUpIcon,
  MovieIcon,
  CircleCheckIcon,
  PlusIcon,
} from "vue-tabler-icons";
import IconButton from "~/components/Button/IconButton.vue";
export default {
  components: {
    IconButton,
    BoltIcon,
    ChevronDownIcon,
    ChevronUpIcon,
    MovieIcon,
    CircleCheckIcon,
    PlusIcon,
  },
  data() {
    return {
      showDetail: false,
    };
  },
};
</script>

<style scoped>
.small {
  height: 3rem;
  transition: height 600ms cubic-bezier(0.6, 0, 0.01, 1);
}
.large {
  height: 25rem;
  transition: height 500ms cubic-bezier(0.5, 0, 0.01, 1);
}
.icon-down {
  transform: rotate(0deg);
  transition: transform 200ms ease-in-out;
}
.icon-up {
  transform: rotate(180deg);
  transition: transform 200ms ease-in-out;
}
</style>
