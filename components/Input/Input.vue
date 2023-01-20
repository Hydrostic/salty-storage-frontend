<template>
  <label>
    <span class="text-slate-900 text-sm font-medium">{{ label }}</span>
    <input type="text" placeholder="jane@example.com" class="transition ease-in-out font-sans block text-sm leading-5 w-full py-2 px-3 shadow-lg border-2 text-slate-500 rounded-lg shadow-sm focus:outline-none focus:ring focus:ring-blue-200 focus:border-blue-500">
  </label>
</template>
<script>
export default {
  props:{
    label:{
      type: String,
    }
  }
}
</script>