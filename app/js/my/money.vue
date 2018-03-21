<template lang="html">
    <Panel title="个人资产" :class="$style.panel">
        <div :class="$style.content">
            <section :class="$style.total">
                <p :class="$style.title">总资产(元)</p>
                <p :class="$style.count">{{count}}</p>
                <p :class="$style.profit">今日收益{{profit}}元</p>
            </section>
            <section :class="$style.list">
                <div :class="$style.item" v-for="item in items">
                    <p :class="$style.name">{{item.name}}</p>
                    <p :class="$style.num">{{item.num}}</p>
                    <img src="//m.jr.jd.com/spe/qyy/main/images/icon_arrow1.png">
                </div>
            </section>
        </div>
    </Panel>
</template>
<script>
import Panel from "../core/panel.vue";

export default {
    components: {
        Panel,
    },
    data(){
        return {
            count:666,
            profit:2.34,
            items:[{
                name:"活期定期",
                num: "32.00元",
            },{
                name:"基金",
                num:"186.00元",
            },{
                name:"京东小金库",
                num:"0.26元",
            },{
                name:"小白理财",
                num: "期限丰富 安全稳定",
            }]
        }
    }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";

.panel{
    @include panel;
    margin-top: 120px !important;
    >h4{
        display: none;
    }
   .content{
        @include list(row);
        .total{
            width: 100%;
            height: 240px;
            padding: 0 32px;
            .title{
                font-size: 28px;
                height: 40px;
                line-height: 40px;
                color: #999;
                margin-top: 40px;
            }
            .count{
                font-size: 66px;
                height: 80px;
                line-height: 80px;
                color: #424954;
            }
            .profit{
                font-size: 28px;
                height: 40px;
                line-height: 40px;
                color: #FF801A;
            }
        }
        .list{
            width: 100%;
            @include list(row);
            .item{
                position: relative;
                width: 50%;
                height: 110px;
                padding: 32px 32px 0 32px;
                box-sizing: border-box;
                &:before{
                    content: "";
                    position: absolute;
                    top: 1px;
                    left: 0;
                    width: 100%;
                    height: 2px;
                    display: block;
                    background: #eee;
                    
                }
                &:after{
                    content: '';
                    position: absolute;
                    top: 0;
                    right: -1px;
                    width: 1px;
                    height: 100%;
                    display: block;
                    background: #eee;
                }
                .name{
                    font-size: 32px;
                    color: #333;
                    height: 40px;
                    line-height: 40px;
                }
                .num{
                    font-size: 28px;
                    color: #999;
                    height: 40px;
                    line-height: 40px;
                }
                >img{
                    position: absolute;
                    top:50%;
                    right: 32px;
                    width: 14px;
                    height: 24px;
                }
            }
        }
      
   }
}
</style>