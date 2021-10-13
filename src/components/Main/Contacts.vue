<template>
  <section>
    <div class="text">
      <h5>LOCATIONS</h5>
      <h3>Visit our Bakeries</h3>
    </div>
    <div class="container_contacts">
        <div class="contact">
            <div class="contact_img">
                <img src="../../assets/image/new-york-bk-600x397.jpg" alt="bakery">
            </div>
            <div class="adress_1">
                ciao
            </div>
        </div>
          <div class="contact">
            <div class="contact_img">
                <img src="../../assets/image/london-bk-600x397.jpg" alt="bakery">
            </div>
            <div class="adress_2">
                ciao
            </div>
        </div>
        
    </div>
  </section>
</template>

<script>
export default {
  name: "Contacts",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common";
@import "../../assets/style/variables";
section {
  @include margin_top_bottom_70px;
  @include container_80;
  @include section_header;
  .text {
    text-align: center;
  }
  .container_contacts{
    display: flex;
    .adress_1{
      height: 1.875rem;
      background-color: $sky;
    }
    .adress_2{
      height: 1.875rem;
      background-color: $light_pink;
    }

    }
  
}
</style>