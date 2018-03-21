<template lang="html">
  <div>
    <Vheader/>
    <Slider/>
    <navbar/>
    <Novice/>
    <Borrow/>
    <Money/>
    <Product/>
    <Life/>
    <VFooter/>
    <Navbar/>
  </div>
</template>

<script>
import Vheader from "../public/header.vue";
import Slider from "./hslider.vue";
import Navbar from "../public/navbar.vue";
import Novice from "./novice.vue";
import Borrow from "./borrow.vue";
import Money from "./money.vue";
import Product from "./product.vue";
import Life from "./life.vue";
import VFooter from "../public/footer.vue";

export default {
  components: {
     Vheader,
     Slider,
     Novice,
     Borrow,
     Money,
     Product,
     Life,
     VFooter,
     Navbar
  }
}
</script>

<style lang="scss" module>

</style>
