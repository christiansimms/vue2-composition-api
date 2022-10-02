<template>
  <div id="app">
    <button @click="refPlus">child plus</button>
    <HelloComposition ref="comp" />
  </div>
</template>

<script setup>
import HelloComposition from './components/HelloComposition.vue'

</script>
<script>
export default {
  name: 'App',
  comments: { HelloComposition },
  mounted() {
    console.log(this.$refs.comp)
  },
  methods: {
    refPlus() {
      this.$refs.comp.plusCount();
    }
  }

};
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
