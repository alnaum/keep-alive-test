<script lang="ts" setup>
const counter = ref<number>(0);

onMounted(() => {
  console.log("Third page", "onMounted");
});

onActivated(() => {
  counter.value++;
  console.log("Third page", "onActivated", counter.value);
});

definePageMeta({
  keepalive: {},
});
</script>

<template>
  <div>
    <h1>Third page</h1>
    <h3>Counter: {{ counter }}</h3>
    <NuxtLink to="/">IndexPage</NuxtLink>
    <span>&nbsp;|&nbsp;</span>
    <NuxtLink to="/secondPage">SecondPage</NuxtLink>
  </div>
</template>
