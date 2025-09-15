<script setup>
import { ref, onMounted } from "vue";
import { RouterLink, RouterView } from "vue-router";

import ChevronUp from "vue-material-design-icons/ChevronUp.vue";
import ChevronDown from "vue-material-design-icons/ChevronDown.vue";
import ChevronRight from "vue-material-design-icons/ChevronRight.vue";
import ChevronLeft from "vue-material-design-icons/ChevronLeft.vue";

let openMenu = ref(false);
</script>

<template>
  <div
    class="w-[calc(100%-240px)] h-[60px] fixed right-0 z-20 bg-[#101010] opacity-80 flex items-center justify-between"
  >
    <div class="flex items-center ml-6">
      <button
        type="button"
        class="rounded-full bg-black p-[1px] cursor-pointer"
      >
        <ChevronLeft fill-color="#FFFFFF" :size="30" />
      </button>
      <button
        type="button"
        class="rounded-full bg-black p-[1px] ml-4 cursor-pointer"
      >
        <ChevronRight fill-color="#FFFFFF" :size="30" />
      </button>
    </div>
    <button
      class="bg-black hover:bg-[#282828] rounded-full p-0.5 mr-8 mt-0.5 cursor-pointer"
    >
      <div class="flex items-center">
        <img
          class="rounded-full"
          width="27"
          src="https://images.steamusercontent.com/ugc/851600242208157774/7FBB64059B18F161EFADFF3C0B41F906F3D4AE2B/?imw=5000&imh=5000&ima=fit&impolicy=Letterbox&imcolor=%23000000&letterbox=false"
        />
        <div class="text-white text-[14px] ml-1.5 mr-1.5 font-semibold">
          Jorge-Guedes
        </div>
        <ChevronDown
          v-if="!openMenu"
          @click="openMenu = true"
          fill-color="#FFFFFF"
          :size="25"
        />
        <ChevronUp
          v-else
          @click="openMenu = false"
          fill-color="#FFFFFF"
          :size="25"
        />
      </div>
    </button>
  </div>
</template>
