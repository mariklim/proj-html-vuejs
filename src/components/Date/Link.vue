<template>
  <a :href="link.url" :class="link.isActive == true ? 'currentPage' : null">{{
    link.nameLink
  }}</a>
</template>

<script>
export default {
  name: "Link",
  props: ["link"],
};
</script>

<style lang="scss">
@import "../../assets/style/common";
.currentPage {
  border-bottom: 2px solid $main_color;
}
</style>