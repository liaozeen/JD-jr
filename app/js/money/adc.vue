<template>
    <Panel title="理财专享" :class="$style.panel">
        <router-link :to="{name:'money'}">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t7162/219/4755741/18941/4e51a5aa/597b066dNf6c7a972.jpg?width=750&height=120">
        </router-link>
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
.panel{
    @include panel;
    &>h4{
        display: none;
    }
    img{
        width: 100%;
    }
}
</style>
