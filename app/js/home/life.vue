<template lang="html">
    <Panel title="生活服务"  :class="$style.panel">
        <ul :class="$style.list">
            <li :class="$style.item" v-for="item in items">
                <img :src="item.img">
                <p>{{item.title}}</p>
                <p v-if="item.text">{{item.text}}</p>
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
    data() {
        return {
            items:[{
                img:"//img12.360buyimg.com/jrpmobile/jfs/t4375/104/1184122472/3976/89741da4/58be8a6eNf10193d0.png?width=135&height=135",
                title:"惠加油"
            },{
                img:"//img12.360buyimg.com/jrpmobile/jfs/t4747/185/1901740991/5892/1383fb93/58f57851N17ee6993.jpg?width=132&height=132",
                title:"小白信用",
                text:"全新升级"
            },{
                img:"//img12.360buyimg.com/jrpmobile/jfs/t3241/234/8044685271/3713/7b29f77f/58be89c8Nb9d41295.png?width=135&height=135",
                title:"信用卡还款"
            },{
                img:"//img12.360buyimg.com/jrpmobile/jfs/t3172/259/7993557249/4351/fd082707/58be8a81Nd7716a06.png?width=135&height=135",
                title:"卡转让"
            },{
                img:"//img12.360buyimg.com/jrpmobile/jfs/t3085/320/8107659086/4344/cdbba2dd/58be8acfNdadcaf00.png?width=135&height=135",
                title:"定期还款"
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
        @include flex(row);
        padding-bottom: 40px;
        box-sizing: border-box;
        .item{
            width: 20%;
            text-align: center;
            img{
                display: inline-block;
                width: 90px;
                height: 90px;
            }
            p{
                font-size: 26px;
                color: #666;
                margin-top: 12px;
                text-overflow: ellipsis;
                white-space: nowrap;
                overflow: hidden;
                &:nth-child(3){
                    color: #FF801A;
                }
            }
        }
    }
}
</style>
