<script lang="ts" setup>
const counter = ref<number>(0);

onMounted(() => {
  console.log("Second page", "onMounted");
});

onActivated(() => {
  counter.value++;
  console.log("Second page", "onActivated", counter.value);
});

definePageMeta({
  keepalive: {},
});
</script>

<template>
  <div>
    <h1>Second page</h1>
    <h3>Counter: {{ counter }}</h3>
    <NuxtLink to="/">IndexPage</NuxtLink>
    <span>&nbsp;|&nbsp;</span>
    <NuxtLink to="/thirdPage">ThirdPage</NuxtLink>
  </div>
</template>
