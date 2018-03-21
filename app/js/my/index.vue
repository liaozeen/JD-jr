<template lang="html">
  <div>
    <Vheader/>
    <Money/>
    <Ious/>
    <More/>
    <VFooter cname="mfooter"/>
    <Navbar/>
  </div>
</template>

<script>
import Vheader from "../public/header.vue";
import VFooter from "../public/footer.vue";
import Navbar from "../public/navbar.vue";
import Money from "./money.vue";
import Ious from "./ious.vue";
import More from "./more.vue"

export default {
  components: {
     Vheader,
     VFooter,
     Navbar,
     Money,
     Ious,
     More
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
