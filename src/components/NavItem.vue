<template>

<div v-if="active == 'true'">
  
  <a href="#" class="flex flex-row items-center mt-6 cursor-pointer transition duration-400 text-theme-gray justify-start" alt="{{ name }}">
    <img :src="require(`@/assets/icon/${icon}`)" alt="{{ name }}" class="w-6">
    <span class="ubuntu font-bold text-md ml-4">{{ name }}</span>
  </a>

</div>
<div v-else>
  
  <a href="#" class="flex flex-row items-center mt-6 cursor-pointer opacity-50 hover:opacity-100 hover:font-bold transition duration-400 text-theme-primary hover-text-theme-gray justify-start" alt="{{ name }}">
    <img :src="require(`@/assets/icon/${icon}`)" alt="{{ name }}" class="w-6">
    <span class="ubuntu font-medium text-md ml-4">{{ name }}</span>
  </a>

</div>

</template>

<script>
export default {
  name: 'NavItem',
  props: ['name', 'icon', 'active']
}
</script>