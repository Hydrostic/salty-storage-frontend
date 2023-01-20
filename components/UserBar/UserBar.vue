<template>
  <div class="grid grid-rows-2 grid-flow-col h-12 w-full">
    <img src="http://localhost:1145/IMG_0532.png" class="rounded-lg w-10 h-10 row-span-2"/>
    <span class="text-xs text-gray-400 row-span-1 col-span-1">欢迎回来,</span>
    <span class="text-sm font-medium col-span-2 -mt-1">不可溶的碳酸氢盐</span>
    <div class="w-6 h-full row-span-2">
      <Dropdown>
        <template #activator="{on}">
          <div class="w-6 h-6 flex my-1 hover:bg-gray-200 rounded-lg" v-on="on">
            <ChevronDownIcon class="m-auto" size="18"/>
          </div>
        </template>
        <DropdownItem>
          <BellIcon class="text-slate-800 mr-2 ml-4" size="18"/>
          <span class="text-sm font-medium text-slate-900">通知</span>
        </DropdownItem>
        <DropdownItem>
          <SettingsIcon class="text-slate-800 mr-2 ml-4" size="18"/>
          <span class="text-sm font-medium text-slate-900">设置</span>
        </DropdownItem>
        <DropdownItem>
          <AdjustmentsHorizontalIcon class="text-slate-800 mr-2 ml-4" size="18"/>
          <span class="text-sm font-medium text-slate-900">控制面板</span>
        </DropdownItem>
      </Dropdown>
    </div>
  </div>
  <div class="grid grid-rows-2 grid-col-flow items-center rounded-lg h-12 w-full">
<!--    <div class="w-8 h-8 flex hover:bg-gray-200 rounded-lg">-->
<!--      <DotsIcon class="text-slate-900 m-auto" size="18"/>-->
<!--    </div>-->
  </div>
</template>

<script>
import {DotsIcon,ChevronDownIcon,AdjustmentsHorizontalIcon,SettingsIcon,BellIcon} from "vue-tabler-icons";
import Dropdown from "~/components/Dropdown/Dropdown.vue";
import DropdownItem from "~/components/Dropdown/DropdownItem.vue";
export default {
  components:{
    DotsIcon,
    ChevronDownIcon,
    Dropdown,
    DropdownItem,
    AdjustmentsHorizontalIcon,
    SettingsIcon,
    BellIcon
  }
}
</script>