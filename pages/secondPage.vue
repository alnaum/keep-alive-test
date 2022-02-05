<script lang="ts" setup>
onMounted(() => {
  console.log("Second page", "onMounted");
});

onActivated(() => {
  console.log("Second page", "onActivated");
});

definePageMeta({
  keepalive: {},
});
</script>

<template>
  <div>
    <h1>Second page</h1>
    <NuxtLink to="/">indexPage</NuxtLink>
    <span>&nbsp|&nbsp</span>
    <NuxtLink to="/thirdPage">ThirdPage</NuxtLink>
  </div>
</template>
