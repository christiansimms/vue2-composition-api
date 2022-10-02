<template>
  <div>composition: {{count}} {{num}}<button @click="plusCount">plus</button> </div>
</template>
<script>
import { ref, defineComponent,computed } from "@vue/composition-api"
export default defineComponent({
  name: 'HelloComposition',
  setup() {
    const count = ref(1);
    const num = computed(() => count.value * 2)

    function plusCount() {
      count.value++
    }

    return {
      num,
      count,
      plusCount
    }
  }
})
</script>
