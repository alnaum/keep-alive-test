<script lang="ts" setup>
const counter = ref<number>(0);

onMounted(() => {
  console.log("Index page", "onMounted");
});

onActivated(() => {
  counter.value++;
  console.log("Index page", "onActivated", counter.value);
});

definePageMeta({
  keepalive: {},
});
</script>

<template>
  <div>
    <h1>Index page</h1>
    <NuxtLink to="/secondPage">SecondPage</NuxtLink>
    <span>&nbsp;|&nbsp;</span>
    <NuxtLink to="/thirdPage">ThirdPage</NuxtLink>
  </div>
</template>
