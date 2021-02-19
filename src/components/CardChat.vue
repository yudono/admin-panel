<template>
  <div class="w-full px-3 py-4">
    <div class="w-full h-full bg-white p-5 rounded-2xl">
      <div class="flex flex-row justify-between mb-4">
        <div>
          <div class="ubuntu font-bold">Nurse Chat Room</div>
          <div class="relative w-full h-8 transform scale-80">
            <img
              :src="require('@/assets/images/avatar-6.png')"
              alt="avatar"
              class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-0"
            />
            <img
              :src="require('@/assets/images/avatar-7.png')"
              alt="avatar"
              class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-6"
            />
            <img
              :src="require('@/assets/images/avatar-8.png')"
              alt="avatar"
              class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-12"
            />
            <img
              :src="require('@/assets/images/avatar-9.png')"
              alt="avatar"
              class="w-8 h-8 object-cover border-white border-2 rounded-full absolute left-24 transform -translate-x-3/4"
            />
          </div>
        </div>
        <div
          class="text-xs bg-indigo-200 text-indigo-800 px-4 py-2 rounded-lg table"
        >
          Start new chat
        </div>
      </div>
      <div class="border-t border-gray-200 pt-4">
        <div class="flex flex-row">
          <img
            :src="require('@/assets/images/avatar-2.png')"
            alt="avatar"
            class="w-8 h-8 object-cover rounded-full"
          />
          <div class="ml-4 text-xs p-2 bg-chat rounded-full ubuntu">
            Botak, can you come to room no. 312 ?
          </div>
        </div>
        <div class="flex flex-row justify-end mt-2">
          <div class="ml-4 text-xs p-2 bg-chat-2 rounded-full ubuntu">
            I’m lazy, why ?
          </div>
          <img
            :src="require('@/assets/images/avatar.png')"
            alt="avatar"
            class="w-8 h-8 object-cover rounded-full"
          />
        </div>
        <div class="flex flex-row mt-2">
          <img
            :src="require('@/assets/images/avatar-2.png')"
            alt="avatar"
            class="w-8 h-8 object-cover rounded-full"
          />
          <div class="ml-4 text-xs p-2 bg-chat rounded-full ubuntu">
            Patient was dying, you better come here
          </div>
        </div>
        <div class="flex flex-row justify-end mt-2">
          <div class="ml-4 text-xs p-2 bg-chat-2 rounded-full ubuntu">
            Let him die then
          </div>
          <img
            :src="require('@/assets/images/avatar.png')"
            alt="avatar"
            class="w-8 h-8 object-cover rounded-full"
          />
        </div>
        <div class="flex flex-row mt-2">
          <img
            :src="require('@/assets/images/avatar-3.png')"
            alt="avatar"
            class="w-8 h-8 object-cover rounded-full"
          />
          <div class="ml-4 text-xs p-2 bg-chat rounded-full ubuntu">
            You’re fired. Get your ass outa here.
          </div>
        </div>
        <div class="mt-6 relative">
          <input
            type="text"
            placeholder="Type a message..."
            class="w-full p-3 rounded-lg border text-sm pr-12"
          />
          <i
            class="fa fa-paper-plane absolute top-0 right-0 p-4 text-indigo-600"
          ></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardChat",
};
</script>