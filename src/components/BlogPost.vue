<script>
export default {
  props: ["fontSize"],
  emits: ["enlarge-text", "reduce-text", "font-percent"],
};
</script>

<template>
  <div>
    <h4>
      <slot />
    </h4>
    <div class="container flex justify-around items-center py-8">
      <button class="btn btn-circle btn-success" @click="$emit('enlarge-text')">
        +
      </button>
      <div>{{ fontSize }}%</div>
      <button class="btn btn-circle btn-error" @click="$emit('reduce-text')">
        -
      </button>
    </div>
  </div>
</template>
