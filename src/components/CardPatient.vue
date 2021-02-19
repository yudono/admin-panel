<template>
  <div class="w-8/12 p-3">
    <div class="w-full h-full bg-white p-5 rounded-2xl">
      <div class="flex flex-row items-center justify-between">
        <div class="ubuntu font-medium">Patient Statistic</div>
        <div class="text-indigo-300 text-xs">VIEW ALL</div>
      </div>
      <div class="flex flex-row items-center justify-between mt-2">
        <div>
          <div class="ubuntu text-xs text-gray-400">In Today</div>
          <div class="ubuntu text-2xl">248</div>
          <div class="ubuntu text-red-500 text-xs">
            <i class="fa fa-arrow-up"></i>15.45%
          </div>
        </div>
        <img
          :src="require('@/assets/images/chart-1.png')"
          alt="chart"
          class="w-3/5"
        />
      </div>
      <div class="flex flex-row items-center justify-between mt-2">
        <div>
          <div class="ubuntu text-xs text-gray-400">Out Today</div>
          <div class="ubuntu text-2xl">139</div>
          <div class="ubuntu text-green-500 text-xs">
            <i class="fa fa-arrow-up"></i>43%
          </div>
        </div>
        <img
          :src="require('@/assets/images/chart-2.png')"
          alt="chart"
          class="w-3/5"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardPatient',
}
</script>