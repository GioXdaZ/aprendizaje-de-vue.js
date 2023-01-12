<script>
import Home from "./components/Home.vue";
import Counters from "./components/Counters.vue";
import ReSizeText from "./components/ReSizeText.vue";

export default {
  components: {
    Home,
    Counters,
    ReSizeText,
  },
  data() {
    return {
      currentTab: "Home",
      tabs: ["Home", "Counters", "Re-Size-Text"],
    };
  },
};
</script>

<template>
  <div
    class="flex flex-col items-center py-5 px-8 border border-black overflow-auto h-screen"
  >
    <div class="flex gap-2">
      <button
        v-for="tab in tabs"
        :key="tab"
        :class="[
          'py-[6px] px-[10px] border border-gray-600 rounded-lg cursor-pointer bg-gray-300',
          { active: currentTab === tab },
        ]"
        @click="currentTab = tab"
      >
        {{ tab }}
      </button>
    </div>
    <component :is="currentTab" class="py-16"></component>
  </div>
</template>

<style>
h1 {
  font-size: xx-large;
}
</style>
