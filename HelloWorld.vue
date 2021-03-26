<template>
  <div>
    {{ update }}
  </div>
  <slot></slot>
  <button @click="passData">CLICK</button>
</template>

<script>
import { computed } from "vue";
export default {
  props: {
    message: {
      type: String,
      require: true,
    },
  },
  //context {emit,attrs,slots}
  setup(props, { emit, attrs, slots }) {
    //setup 안에서는 this가 안됨
    console.log(attrs.class);
    console.log(slots.default());
    const update = computed(() => props.message + "!");
    const passData = () => emit("click", "hi!");
    return {
      update,
      passData,
    };
  },
};
</script>

<style lang="scss" scoped>
</style>