
<script setup>
const { $useLoading } = useNuxtApp();

const loadingHandler = $useLoading({
  loader: "spinner",
  backgroundColor: "#5f99ff",
  width: 200,
  height: 200,
  color: '#000000',
});

function openLoading() {
  const loader = loadingHandler.show();
  setTimeout(() => {
    loader.hide();
  }, 1000);
}
</script>

<template>
  <button type="button" @click="openLoading">開啟 Loading 效果</button>
</template>

<style scoped></style>
