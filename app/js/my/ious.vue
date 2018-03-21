<template lang="html">
    <Panel title="白条额度" :class="$style.panel">
        <div :class="$style.content">
           <section :class="$style.total">
               <p :class="$style.title">白条可用额度(元)</p>
               <p :class="$style.count">{{count}}</p>
               <p :class="$style.profit">{{profit}}</p>
               <img src="//m.jr.jd.com/spe/qyy/main/images/icon_arrow1.png">
           </section>
           <div :class="$style.item" v-for="item in items">
               <p :class="$style.name">{{item.name}}</p>
               <p :class="$style.num" >{{item.num}}<i v-if="item.info">{{item.info}}</i></p>
               <img src="//m.jr.jd.com/spe/qyy/main/images/icon_arrow1.png" v-if="item.name">
           </div>
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
            count:"3308.00",
            profit: "近7日无待还",
            items:[{
                name:"小白信用",
                num: "89.4",
                info:"信用优秀"
            },{
                name:"",
                num: "",
                info:""
            }]
        }
    }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";

.panel{
    @include panel;
    >h4{
        display: none;
    }
   .content{
       @include list(row);
       .total{
            position: relative;
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
            img{
                position: absolute;
                top:50%;
                right: 32px;
                width: 14px;
                height: 24px;
            }
       }
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
                i{
                    font-size: 18px;
                    font-style: normal;
                    padding: 0 12px;
                    height: 28px;
                    line-height: 28px;
                    border-radius: 16px;
                    margin: -4px 0 0 4px;
                    border-radius: 16px;
                    text-align: center;
                    color: #fff;
                    background: #508CEE;

                }
            }
            img{
                position: absolute;
                top:50%;
                right: 32px;
                width: 14px;
                height: 24px;
            }
       }
   }
}
</style>