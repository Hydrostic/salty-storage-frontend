<template>
  <slot name="activator" :on="listener"></slot>
  <div
    class="rounded-lg shadow w-32 absolute bg-white px-2 grid grid-cols-1 grid-flow-row place-content-around divide-y-1 gap-1 auto-rows-max overflow-hidden animation"
    :style="{ height: height }"
    @mouseover="handleDropdown(true)"
    @mouseleave="handleDropdown(false)"
  >
    <div
      class="py-2 animation"
      ref="content"
      :class="height !== '0px' ? 'opacity-100' : 'opacity-0'"
    >
      <slot></slot>
    </div>
  </div>
</template>

<script setup>
// let top = ref(0);
// let left = ref(0);
// let isActive = ref(false);
// let onDropdown = ref(false);
// let onActivator = ref(false);
// let showAnimation = ref(false);
// let timeOut = null;
// let listener = {
//         mouseover: withModifiers((e)=>{
//           e.preventDefault()
//           onActivator.value=true
//           let rect =e.target.getBoundingClientRect()
//           top.value=rect.top+rect.height;left.value=rect.left;
//           isActive.value=true
//         }, ['self']),
//         mouseleave: withModifiers((e)=>{
//           e.preventDefault()
//           onActivator.value=false
//           if (timeOut) clearTimeout(timeOut)
//           timeOut = setTimeout(()=>{
//             if(!onDropdown.value && !onActivator.value){
//               showAnimation.value=true
//               setTimeout(()=>{
//                 isActive.value=false
//                 showAnimation.value=false
//               },200)
//
//             }
//           },100)
//         }, ['self'])
//     }
let top = ref(0);
let left = ref(0);
let height = ref("0px");
let content = ref();
let onDropdown = false;
let onActivator = false;
let timeOut = null;
let onLeave = () => {
  if (timeOut) clearTimeout(timeOut);
  timeOut = setTimeout(() => {
    if (!onDropdown && !onActivator) {
      height.value = "0px";
    }
  }, 100);
};
let listener = {
  mouseover: withModifiers(
    (e) => {
      e.preventDefault();
      onActivator = true;
      let rect = e.target.getBoundingClientRect();
      top.value = rect.top + rect.height;
      left.value = rect.left;
      console.log(content.value.offsetHeight);
      height.value = `${content.value.offsetHeight}px`;
    },
    ["self"]
  ),
  mouseleave: withModifiers(
    (e) => {
      e.preventDefault();
      onActivator = false;
      onLeave();
    },
    ["self"]
  ),
};
// let onOutsideClick = ()=>{
//   console.log("a")
//   if(isActive.value){
//     isActive.value = false
//   }
// }
let handleDropdown = (on) => {
  onDropdown = on;
  onLeave();
};
</script>

<style scoped>
.animation {
  transition: height 300ms, opacity 50ms ease-in-out;
}
</style>
