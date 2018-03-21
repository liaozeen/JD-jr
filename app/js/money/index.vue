<template lang="html">
  <div>
    <Vheader/>
    <Mslider/>
    <Money/>
    <adb/>
    <finance/>
    <adc/>
    <VFooter cname="mfooter"/>
    <Navbar/>
  </div>
</template>

<script>
import Vheader from "../public/header.vue";
import Mslider from "./mslider.vue";
import VFooter from "../public/footer.vue";
import Navbar from "../public/navbar.vue";
import Money from "./money.vue";
import adb from "./adb.vue";
import finance from "./finance.vue";
import adc from "./adc.vue"

export default {
  components: {
     Vheader,
     VFooter,
     Navbar,
     Mslider,
     Money,
     adb,
     finance,
     adc
  }
}
</script>

<style lang="scss">
.mfooter{
  ul{
    li:first-child{
      display: none;
    }
  }
}
</style>
