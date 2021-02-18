<template>
	<div class="w-full bg-theme-secondary rounded-2xl p-4 flex flex-col items-center relative">
		<img :src="require('@/assets/images/Documents-amico.png')" alt="document" class="transform top-8 -translate-y-1/2 absolute w-48">
		<div class="font-medium text-md ubuntu mt-20">Todays Report</div>
		<div class="text-center text-xs text-theme-gray mt-2">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin iaculis tortor et volutpat finibus.</div>
		<div class="bg-theme-primary w-full text-xs rounded-lg flex flex-row items-center justify-center text-white py-2 mt-2"><img :src="require('@/assets/icon/arrow-down.png')" alt="download" class="w-6"><span class="ml-2 ubuntu font-bold text-theme-secondary">Download Report</span></div>
	</div>
</template>

<script>
export default {
  name: 'Reports',
}
</script>