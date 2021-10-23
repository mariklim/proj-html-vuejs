<template>
  <ScrollTopComponent>
    <a class="btn btn-light">
      <i class="fas fa-caret-up"></i>
    </a>
  </ScrollTopComponent>
</template>

<script>
import ScrollTopComponent from "./ScrollTopComponent";
export default {
  components: {
    ScrollTopComponent,
  },
};
</script>

<style lang="scss">
@import "./assets/style/common";
a {
  display: inline-block;
}
.btn {
  width: 3.125rem;
  height: 3.125rem;
  line-height: 3.125rem;
  font-size: 1.875rem;
  border-radius: 50%;
  background-color: rgba(84, 23, 102, 0.452);
  color: rgb(0, 0, 0);
  text-align: center;
  color: white;
  transition: all 0.7s;
  &:hover {
    background-color: rgba(84, 23, 102, 0.685);
  }
}
</style>