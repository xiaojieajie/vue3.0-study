<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Hello Vue 3.0 + Vite" />
    <div @click="increment">{{count}}</div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import { ref, watchEffect, watch, reactive } from 'vue'
export default {
  name: 'App',
  components: {
    HelloWorld
  },
  setup (props, context) {
    const userInfo = reactive({ name: '杰杰', age: 18 })
    return { userInfo }
  },
  // 等同于
  data () {
    return {
      userInfo: { name: '杰杰', age: 18 }
    }
  }
}
</script>
