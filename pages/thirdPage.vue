<script lang="ts" setup>
onMounted(() => {
  console.log("Third page", "onMounted");
});

onActivated(() => {
  console.log("Third page", "onActivated");
});

definePageMeta({
  keepalive: {},
});
</script>

<template>
  <div>
    <h1>Third page</h1>
    <NuxtLink to="/">IndexPage</NuxtLink>
    <span>&nbsp|&nbsp</span>
    <NuxtLink to="/secondPage">SecondPage</NuxtLink>
  </div>
</template>
