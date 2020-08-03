<template>
  <div id="app">
    <HelloWorld :msg="msg" :count="count" />
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive } from "vue";
import HelloWorld from "./components/HelloWorld.vue";

interface propsReactive {
  msg: String;
  count: Number;
}
export default defineComponent({
  setup() {
    const data: propsReactive = reactive<propsReactive>({
      msg: "HELLO WORLD!",
      count: 0,
    });
    return {
      ...data,
    };
  },
  components: {
    HelloWorld,
  },
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
