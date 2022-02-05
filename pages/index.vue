<script lang="ts" setup>
onMounted(() => {
  console.log("Index page", "onMounted");
});


onActivated(() => {
  console.log("Index page", "onActivated");
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
