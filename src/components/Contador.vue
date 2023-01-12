<script>
export default {
  data() {
    return {
      count: 0,
      count2: 0,
      count3: 0,
    };
  },
};
</script>

<template>
  <div>
    <div class="container flex justify-center items-center gap-8">
      <div class="flex flex-col justify-center items-center gap-2">
        <p>x1</p>
        <button
          class="btn btn-circle btn-primary hover:btn-accent"
          @click="count++"
        >
          {{ count }}
        </button>
      </div>
      <div class="flex flex-col justify-center items-center gap-2">
        <p>x2</p>
        <button
          class="btn btn-circle btn-secondary hover:btn-info"
          @click="count2++"
        >
          {{ count2 * 2 }}
        </button>
      </div>
      <div class="flex flex-col justify-center items-center gap-2">
        <p>x3</p>
        <button
          class="btn btn-circle btn-active hover:btn-warning"
          @click="count3++"
        >
          {{ count3 * 3 }}
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
p {
  font-size: x-large;
}
</style>
