<template>
  <div class="w-full p-3">
    <div class="w-full h-full bg-white p-5 rounded-2xl">
      <div class="flex flex-row justify-between">
        <div class="ubuntu font-bold">Room Waiting List</div>
        <div class="text-xs text-indigo-300">VIEW COMPLETE LIST</div>
      </div>
      <table class="table-auto w-full mt-4 text-sm">
        <thead
          class="font-medium text-left text-gray-300 border-b border-gray-200 ubuntu"
        >
          <tr>
            <th class="py-4">Name</th>
            <th class="py-4">Status</th>
            <th class="py-4">Date</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="p-2 text-gray-800">
              <img
                :src="require('@/assets/images/avatar-2.png')"
                alt="avatar"
                class="w-10 h-10 rounded-full object-cover inline-block mr-4"
              />Jessica Islander
            </td>
            <td class="p-4">
              <span
                class="bg-indigo-200 py-2 px-3 text-indigo-700 rounded-full font-bold text-xs"
                >VIP</span
              >
            </td>
            <td class="p-4 text-gray-300">January 30, 2021</td>
          </tr>
          <tr>
            <td class="p-2 text-gray-800">
              <img
                :src="require('@/assets/images/avatar-3.png')"
                alt="avatar"
                class="w-10 h-10 rounded-full object-cover inline-block mr-4"
              />
              Iyem
            </td>
            <td class="p-4">
              <span
                class="bg-yellow-200 py-2 px-3 text-yellow-700 rounded-full font-bold text-xs"
                >STD</span
              >
            </td>
            <td class="p-4 text-gray-300">February 05,2021</td>
          </tr>
          <tr>
            <td class="p-2 text-gray-800">
              <img
                :src="require('@/assets/images/avatar-4.png')"
                alt="avatar"
                class="w-10 h-10 rounded-full object-cover inline-block mr-4"
              />
              Sujiwan Parmin
            </td>
            <td class="p-4">
              <span
                class="bg-indigo-200 py-2 px-3 text-indigo-700 rounded-full font-bold text-xs"
                >VIP</span
              >
            </td>
            <td class="p-4 text-gray-300">February 10,2021</td>
          </tr>
          <tr>
            <td class="p-2 text-gray-800">
              <img
                :src="require('@/assets/images/avatar-5.png')"
                alt="avatar"
                class="w-10 h-10 rounded-full object-cover inline-block mr-4"
              />
              Parno Marpin
            </td>
            <td class="p-4">
              <span
                class="bg-yellow-200 py-2 px-3 text-yellow-700 rounded-full font-bold text-xs"
                >STD</span
              >
            </td>
            <td class="p-4 text-gray-300">February 15,2021</td>
          </tr>
          <tr>
            <td class="p-2 text-gray-800">
              <img
                :src="require('@/assets/images/avatar-6.png')"
                alt="avatar"
                class="w-10 h-10 rounded-full object-cover inline-block mr-4"
              />
              Paimer suka amer
            </td>
            <td class="p-4">
              <span
                class="bg-yellow-200 py-2 px-3 text-yellow-700 rounded-full font-bold text-xs"
                >STD</span
              >
            </td>
            <td class="p-4 text-gray-300">February 20,2021</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardRoom",
};
</script>