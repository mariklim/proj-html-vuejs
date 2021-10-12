<template>
  <div class="corporate">
    <h5>CORPORATE & WEDDINGS</h5>
    <h3>Baking Special Moments</h3>
    <div class="corporate_cards">
      <div class="card corporate">
        <div class="card corporate active">
          <span>
            <h5>INTERNATIONAL BAKERY</h5>
            <h3>Corporate Events</h3>
            <button class="btn_lilac">Explore more</button>
          </span>
        </div>
      </div>
      <div class="card wedding">
        <div class="card wedding active">
          <span>
            <h5>PRIVATE DINING HALL</h5>
            <h3>Weddings & Parties</h3>
            <button class="btn_lilac">Explore more</button>
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Corporate",
};
</script>

<style lang="scss">
@import "../../assets/style/common";
@import "../../assets/style/variables";

.corporate {
  @include section_header;
  @include container_80;
  //   @include margin_top_bottom_70px;
  text-align: center;
  .corporate_cards {
    @include margin_top_bottom_70px;
    display: flex;
    justify-content: space-between;
    .card {
      width: 37.5rem;
      height: 40.625rem;
      background-color: coral;
      &.corporate {
        background-image: url("../../assets/image/corporate-bg.jpg");
        background-size: cover;
        &.active {
          background-image: url("../../assets/image/corporate-hover-bg.jpg");
        }
      }
      &.wedding {
        background-image: url("../../assets/image/wedding-bg.jpg");
        background-size: cover;
        &.active {
          background-image: url("../../assets/image/wedding-hover-bg.jpg");
        }
      }
      .active {
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        text-align: center;
        opacity: 0;
        transition: opacity 1s;
      }
    }

    //Hover
    .card.corporate:hover .card.corporate.active{
        opacity: 1;
    }
     .card.wedding:hover .card.wedding.active{
        opacity: 1;
    }
  }
}
</style>