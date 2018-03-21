<template lang="html">
  <div>
    <Vheader/>
    <Islider/>
    <Donation/>
    <Server/>
    <VFooter/>
    <Navbar/>
  </div>
</template>

<script>
import Vheader from "../public/header.vue";
import Islider from "./islider.vue";
import Donation from "./donation.vue";
import Server from "./server.vue"
import VFooter from "../public/footer.vue";
import Navbar from "../public/navbar.vue";

export default {
  components: {
     Vheader,
     Islider,
     Donation,
     Server,
     VFooter,
     Navbar,
  }
}
</script>

<style lang="scss">

</style>
