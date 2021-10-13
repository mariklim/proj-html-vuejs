<template>
  <section>
    <div class="card">
      <h3>{{ infoImage.name }}</h3>
      <img :src="infoImage.src" :alt="infoImage.name" />
    </div>
  </section>
</template>

<script>
export default {
  name: "Card",
  props: ['infoImage'],
};
</script>

<style>
</style>