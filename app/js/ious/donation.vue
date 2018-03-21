<template lang="html">
    <Panel title="白条福利" :class="$style.panel">
        <ul :class="$style.list">    
            <li :class="$style.item" v-for="item in items" :key="item.img">
                <img :src="item.img" :alt="item.title">
                <div :class="$style.info">
                    <h4>{{item.title}}</h4>
                    <p>{{item.text}}</p>
                </div>
                <router-link :to="{name:item.href}">
                    <em>{{item.enterText}}</em>
                </router-link>
            </li>
        </ul>
    </Panel>
</template>
<script>
import Panel from "../core/panel.vue"
export default {
   components: {
       Panel
   },
   data(){
       return {
           items:[{
               title:"开通白条",
               text:"送188元礼包",
               enterText:"立即开通",
               href:"ious",
               img:"//img12.360buyimg.com/jrpmobile/jfs/t4378/62/155957680/9017/16463551/58affd58Nb5c9198e.jpg?width=120&height=120"
           },{
               title:"白条闪付",
               text:"新手享158元礼包",
               enterText:"随机立减",
               href:"ious",
               img:"//img12.360buyimg.com/jrpmobile/jfs/t4150/330/141981421/9147/604e3e04/58affc3bNbfa8f9d7.jpg?width=120&height=120"
           },{
               title:"白条提额",
               text:"金融app专享提额礼包",
               enterText:"去提额",
               href:"ious",
               img:"//img12.360buyimg.com/jrpmobile/jfs/t4270/96/1102370053/8651/58b7fa5a/58bd2e10N453e9464.jpg?width=120&height=120"
           }]
       }
   }
}
</script>
<style lang="scss" module>
@import "../../css/element.scss";
.panel{
    @include panel;
    .list{
        .item{
            @include list(row);
            align-items:center;
            width: 100%;
            height: 140px;
            img{
                width: 88px;
                height: 88px;
                margin: 0 32px;
            }
            .info{
                display: inline-block;
                flex: 2;
                overflow: hidden;
                h4{
                    font-size: 32px;
                    color: #333;
                    line-height: 1.8;
                    white-space: nowrap;
                    text-overflow: ellipsis;
                    overflow: hidden;
                }
                p{
                    font-size: 24px;
                    color: #999;
                    white-space: nowrap;
                    text-overflow: ellipsis;
                    overflow: hidden;
                }
            }
            em{
                max-width: 39%;
                font-size: 28px;
                color: #FF801A;
                margin-right: 16px;
                white-space: nowrap;
                text-overflow: ellipsis;
                overflow: hidden;
                &::after{
                    content: " > ";
                    color: #999;

                }
            }
            a{
                text-decoration: none;
            }
        }
    }
}
</style>
