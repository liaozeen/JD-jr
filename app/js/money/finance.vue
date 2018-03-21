<template>
    <Panel title="理财精选" :class="$style.panel">
        <section :class="$style.list">
           <div :class="$style.item" v-for="item in enters" :key="item.img">
               <router-link :to="{name:item.href}">
                   <img :src="item.img" :alt="item.title">
                   <div :class="$style.info">
                        <h5>{{item.title}}</h5>
                        <p>{{item.rate}}</p>
                   </div>
                   <span>去赚钱</span>
               </router-link>
           </div>
       </section>
    </Panel>
</template>
<script>
import Panel from "../core/panel.vue";
export default {
  components: {
    Panel
  },
  data() {
    return {
        enters: [{
            href: "money",
            img: "//img12.360buyimg.com/jrpmobile/jfs/t3670/58/543125556/2606/a65096b9/580d80afN63b1085a.png?width=76&height=76",
            title: "月度理财",
            rate:"预期年化收益4.50%"
        }, {
            href: "money",
            img: "//img12.360buyimg.com/jrpmobile/jfs/t3679/44/511862277/2728/c1c6b2bf/580d8189N6b6f8052.png?width=76&height=76",
            title: "季度理财",
            rate:"预期年化收益5.50%"
        }, {
            href: "money",
            img: "//img12.360buyimg.com/jrpmobile/jfs/t3331/69/580199498/3074/d5bb21c5/580d7f6cN7f35e596.png?width=76&height=76",
            title: "一年理财",
            rate:"预期年化收益5.80%"
        }]  
    }
  }
}
</script>
<style lang="scss" module>
@import "../../css/element.scss";
.panel{
    @include panel;
    &>h4{
        box-sizing: border-box;
        border-bottom: 1px solid #ddd;
    }
    .list{
        .item{
            @include list(row);
            align-items:center;
            width: 100%;
            height: 140px;
            position: relative;
            &:first-child{
                &:before {
                    display: none;
                }
            }
            &:before {
                content: " ";
                width: 100%;
                height: 0;
                border-bottom: 0.025rem solid #ddd;
                margin-left: 152px;
            }
            a{
                text-decoration: none;
            }
            img{
                width: 88px;
                height: 88px;
                margin: 0 32px;
            }
            .info{
                display: inline-block;
                max-width: 60%;
                h5{
                    font-size: 32px;
                    color: #333;
                    line-height: 1.8;
                }
                p{
                    font-size: 24px;
                    color: #ff3232;
                    white-space: nowrap;
                    text-overflow: ellipsis;
                    overflow: hidden;
                    padding-bottom: 8px;
                }
            }
            span{
                font-size: 28px;
                color: #FF801A;
                position: absolute;
                right: 30px;
                top: 50%;
                &:after{
                    content: " >";
                    color: #ddd;
                }
            }
        }
    }
}
</style>
