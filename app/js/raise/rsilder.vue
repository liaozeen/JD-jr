<template lang="html">
    <Panel title="金融头条" :class="$style.panel">
        <section :class="$style.content">
            <swiper :options="options">
                <swiper-slide v-for="item in items">
                    {{item.title}}
                    <em>></em>
                </swiper-slide>
            </swiper>
        </section>
    </Panel>
</template>
<script>
import Panel from "../core/panel.vue";
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
    components: {
        Panel,
        swiper,
        swiperSlide
    },
    data() {
        return {
            options:{
                direction: "vertical",
                loop: true,
                autoplay:true
            },
            items:[{
                title:"签到领流量，1元500M！",
                href:"raise"
            },{
                title:"百万白条券免费送，速来领取！！ ",
                href:"raise"
            }]
        }
    }
}
</script>

<style lang="scss">
.swiper-container-vertical{
    height: 72px;
    .swiper-slide{
        position: relative;
        font-family: PingFangSC-Medium;
        font-size: 28px;
        padding-right: 40px;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
        color: #333;
        em{
            position: absolute;
            color: #ddd;
            right: 20px;
        }
    
    }
}
</style>

<style lang="scss" module>
@import "../../css/element.scss";

.panel{
    @include panel;
    >h4{
        display: none;
    }
    margin-top: 120px !important;
    .content{
        height: 72px;
        line-height: 72px;
        padding-left:166px;
        overflow: hidden;
        background:url('//m.jr.jd.com/spe/qyy/main/images/scroll_title_img.png') left top no-repeat;
        background-size:146px 72px;
    }
}
</style>
