<template>
  <div>
    <HelloWorld message="gg" @click="consoleLog" class="kk">
      <div>slots</div>
    </HelloWorld>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  components: {
    HelloWorld,
  },
  setup() {
    const consoleLog = (value) => console.log("click!" + value);
    return { consoleLog };
  },
};
</script>

<style lang="scss" scoped>
</style>