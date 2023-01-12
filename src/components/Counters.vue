<script>
import Contador from "./Contador.vue";

export default {
  components: {
    Contador,
  },
};
</script>
<template>
  <div class="container flex flex-col justify-center items-center py-16 gap-4">
    <h1>Counters Buttons</h1>
    <Contador />
  </div>
</template>
