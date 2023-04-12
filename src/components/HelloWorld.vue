<script setup>
import { ref, computed } from 'vue'

const props = defineProps(["msg"]);
const count = ref(0);
const doubleCount = computed(() => count.value * 2);
const testArr = ref(["Uno", "Due", "Tre",]);


function incrementCount() {
  count.value++;
}

</script>

<template>
  <h1>{{ props.msg }}</h1>
  <button @click="incrementCount">
    {{ count }},
    {{ doubleCount }}
  </button>
  <div class="flexami">
    <div v-for="item in testArr">{{ item }}</div>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}

.flexami {
  display: flex;
  flex-flow: column;
  justify-content: start;
  align-items: start;
}
</style>
