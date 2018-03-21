<template lang="html">
    <Panel title="更多服务" :class="$style.panel">
        <ul :class="$style.list">    
            <li :class="$style.item" v-for="item in items" :key="item.img">
                <router-link :to="{name:item.href}">
                    <img :src="item.img">
                    <h4>{{item.title}}</h4>
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
               title:"小白理财",
               href:"ious",
               img:"//img12.360buyimg.com/jrpmobile/jfs/t4330/133/678123946/5169/caa95df0/58b7dc5bN18e35d4c.png?width=120&height=119"
           },{
               title:"钢镚",
               href:"ious",
               img:"//img12.360buyimg.com/jrpmobile/jfs/t3649/359/1635382237/5435/20453a2e/582c3666Ne77dec97.png?width=120&height=120"
           },{
               title:"小白信用",
               href:"ious",
               img:"//img12.360buyimg.com/jrpmobile/jfs/t3571/19/1630706642/1939/c4a48e76/582c359cN20a00758.png?width=135&height=135"
           },{
               title:"存工资",
               href:"ious",
               img:"//img12.360buyimg.com/jrpmobile/jfs/t3400/21/1585015214/1646/8f5ad15f/582c35b9N8cd168a5.png?width=135&height=135"
           },{
               title:"保障险",
               href:"ious",
               img:"//img12.360buyimg.com/jrpmobile/jfs/t3385/44/1019888807/5770/d74683d1/58198963N4211803c.png?width=132&height=132"
           },{
               title:"白条提额",
               href:"ious",
               img:"//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135"
           },{
               title:"借钱",
               href:"ious",
               img:"//img12.360buyimg.com/jrpmobile/jfs/t8311/300/1385281399/9501/130a0046/59b8da06N14f62cf3.png?width=120&height=120"
           },{
               title:"小白卡",
               href:"ious",
               img:"//img12.360buyimg.com/jrpmobile/jfs/t4609/245/3975151339/11019/766e751d/590aca78Nf15a7947.png?width=135&height=135"
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
        @include list(row);
        .item{
            width: 25%;
            height: 140px;
            text-align: center;
            box-sizing: border-box;
            margin-bottom: 40px;
            img{
                display: block;
                width: 90px;
                height: 90px;
                margin: 0 auto;
            }
            h4{
                font-size: 26px;
                color: #666;
                margin-top: 12px;
                white-space: nowrap;
                text-overflow: ellipsis;
                overflow: hidden;
            }
            a{
                text-decoration: none;
            }
        }
    }
}
</style>
