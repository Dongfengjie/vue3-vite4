<script setup lang="ts">

import { ref, onMounted } from "vue";

defineProps<{ msg: string }>();

const count = ref(0);

const object = ref({
  name: "张三",
  age: "26",
});

onMounted(() => {
  console.log("start learn Vue3");
});

const handleClick = () => {
  count.value++;
  console.log(object.value.name);
};
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="handleClick">count is {{ count }}</button>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
