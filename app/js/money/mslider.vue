<template lang="html">
    <article :class="$style.content">
        <Slider :items="items" :cname="$style.slider"/>
        <router-link :to="{name:'money'}">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t5842/235/8356236245/38364/2112fd7e/597a95d4Ne01da140.png?width=750&height=270" alt="">
        </router-link>
    </article>
</template>d
<script>
import Slider from "../core/slider.vue";
export default {
    components: {
        Slider
    },
    data() {
        return {
            items:[{
                href:"money",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t11149/181/856008463/68797/dc303e9/59f97baeN3cdae084.jpg?width=750&height=400"
            },{
                href:"money",
                src:"//img12.360buyimg.com/jrpmobile/jfs/t9994/205/2575467053/189117/125e7b05/59f97c36N7599be57.png?width=750&height=400"
            }]
        }
    }
}
</script>
<style lang="scss" module>
@import "../../css/element.scss";

.content{
    .slider{
        margin-top: 100px;
        img{
            width:100%;
        }
    }
    img{
        width: 100%;
        margin-top: 20px;
        background: #fff;
    }
}

</style>
