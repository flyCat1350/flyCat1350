<template>
  <img alt="Vue logo" src="./assets/logo.png" @click="triggerEmit(1)"/>
  <HelloWorld msg="Hello Vue 3.0 + Vite" />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  mounted() {
    this.$on('trigger-emit', data => {
      alert(data)
    })
  },
  methods: {
    triggerEmit(val) {
      this.$emit('trigger-emit', val)
    }
  }
}
</script>
