<template>
  <div class="w-full lg:w-4/12 p-3">
    <div class="w-full h-full bg-white p-5 rounded-2xl text-center">
      <div class="ubuntu font-medium">Hospital Capacity</div>
      <center>
        <img
        :src="require('@/assets/images/chart-3.png')"
        alt="chart"
        class="w-full mt-2"
        style="max-width:240px"
      />
      </center>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardHospital",
};
</script>