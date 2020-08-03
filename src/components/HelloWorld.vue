<template>
  <div class="msg-pael">{{ msg }}</div>
  <div class="msg-pael">{{ count }}</div>
  <div class="msg-pael">{{ compotedComponent }}</div>
</template>

<script lang="ts">
import { defineComponent, computed,  } from 'vue'
interface compotedComponent {}
interface ComputedRef {}
export default defineComponent({
  props: {
    msg: String,
    count: Number
  },
  setup(props: any) {
    console.log(props, 'props')
    const compotedComponent: ComputedRef<number> = computed<number>((count: any) => {
      count + 1
    })
    return {
      ...compotedComponent
    }
  },
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
