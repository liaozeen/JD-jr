<template>
  <Panel title="理财推荐" :class="$style.panel">
    <div :class="$style.list">
        <div :class="$style.item" v-for="item in items" :key="item.href">
            <router-link :to="{name:item.href}">
                <h4>{{item.title}}<span :class="$style.red">{{item.sub}}</span></h4>
                <h5>{{item.rate}}</h5>
                <p>{{item.text}}</p>
            </router-link>
        </div>
    </div>
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
        items:[{
            title:"定期理财",
            sub:"理财首选",
            rate:"5.60%",
            text:"历史年化回报率"
        },{
            title:"小白理财",
            sub:"理财首选",
            rate:"4.22%",
            text:"7日年化回报率"
        },{
            title:"月月盈",
            sub:"养老保障",
            rate:"5%",
            text:"7日年化回报率"
        },{
            title:"小白基金",
            sub:"天天赚钱",
            rate:"4.27%",
            text:"7日年化回报率"
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
        justify-content: space-around;
        box-sizing: border-box;
        &:after{
            content: "";
            display: block;
            width: 100%;
            height: 0px;
            box-sizing: border-box;
            border-bottom: 1px solid #ddd;
            position: relative;
            top: -208px;
        }
        a{
            text-decoration: none;
        }
        .item{
            position: relative;
            box-sizing: border-box;
            width: 50%;
            padding: 34px 16px;
            &:after{
                content: "";
                width: 1px;
                height: 136px;
                display: block;
                position:absolute;
                top: 50%;
                margin-top: -68px;
                right: 0;
                border-right: 1px solid #eee;
            }
            &:nth-child(2n){
                &:after{
                    display: none;
                }
            }
            h4{
                font-size: 30px;
                line-height: 42px;
                color: #333;
                .red{
                    font-size: 22px;
                    color: #FF5155;
                    text-align: center;
                    border: 1px solid #FF5155;
                    padding: 0 8px;
                    margin-left: 4px;
                }
            }
            h5{
                font-weight: 700;
                font-size: 44px;
                height: 58px;
                line-height: 58px;
                color: #FF5155;  
            }
            p{
                font-size: 24px;
                height: 34px;
                line-height: 34px;
                color: #999;
                white-space: nowrap;
                text-overflow: ellipsis;
                overflow: hidden;
            }
        }
    }
}
</style>
