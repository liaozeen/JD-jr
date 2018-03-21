<template>
   <Panel title="下载APP" :class="$style.panel">
      <section :class="$style.content">
        <div :class="$style.logo"></div>
        <p>立即下载</p>
      </section>
   </Panel>
</template>

<script>
import Panel from "../core/panel.vue";
export default {
    components: {
        Panel
    }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
html,body{
    background: #fff;
}
.panel{
    @include panel;
    margin:0!important;
    >h4{
        display: none;
    }
    .content{
        @include flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 1136px;
        .logo{
            background:url(//img12.360buyimg.com/jrpmobile/jfs/t10054/120/2165982932/56512/574e4766/59f031f3N1a75e42d.png?width=1125&height=890) center center no-repeat;
            width: 400px;
            height: 500px;
            background-size: 100% auto;
            margin-top: -200px;
        }
        >p{
            @include btn($size:32px,$color:#fff,$bgcolor:#f1443e,$padding:5px,$radius:5px);
            height: 100px;
            line-height: 100px;
            width: 471px;
            background-image: linear-gradient(270deg,#f55c33 0,#ee2d1b 75%);
            box-shadow: 0 12px 16px 0 rgba(255, 159, 135, .6);
            position: fixed;
            bottom: 130px;
        }
    } 
}
</style>
