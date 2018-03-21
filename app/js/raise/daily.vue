<template lang="html">
    <Panel title="每日签到" :class="$style.panel">
        <section :class="$style.content">
           <img src="//img12.360buyimg.com/jrpmobile/jfs/t3184/283/6032981290/37056/fa30c674/589bd5a2Nabdbbbd9.jpg?width=376&height=160">
           <img src="//img12.360buyimg.com/jrpmobile/jfs/t3298/196/6130416421/33755/a0536d3e/589bd5d4Nf32e7adc.jpg?width=374&height=160">
        </section>
        <span :class="$style.text">不抢白不抢</span>
    </Panel>
</template>
<script>
import Panel from "../core/panel.vue";

export default {
    components: {
        Panel,
    }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";

.panel{
    @include panel;
    position: relative;
    .content{
        @include list(row);
        img{
            flex: 1;
            width: 320px;
            height: 126px;
        }
    }
    .text{
        position: absolute;
        top: 0;
        right: 20px;
        width: 140px;
        height: 112px;
        font-size: 28px;
        color: #999;
        line-height: 112px;
    }
}
</style>