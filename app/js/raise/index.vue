<template lang="html">
  <div>
    <Vheader/>
    <Rsilder/>
    <Daily/>
    <In/>
    <More/>
    <VFooter cname="mfooter"/>
    <Navbar/>
  </div>
</template>

<script>
import Vheader from "../public/header.vue";
import Rsilder from "./rsilder.vue";
import Daily from "./daily.vue";
import In from "./in.vue";
import More from "./more.vue";
import VFooter from "../public/footer.vue";
import Navbar from "../public/navbar.vue";

export default {
  components: {
     Vheader,
     VFooter,
     Navbar,
     Rsilder,
     Daily,
     In,
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
