<template lang="html">
    <Panel title="神券满" :class="$style.panel">
        <section :class="$style.content">
            <router-link :to="{name:'home'}">
                <img src="http://img12.360buyimg.com/jrpmobile/jfs/t7162/219/4755741/18941/4e51a5aa/597b066dNf6c7a972.jpg?width=750&height=120" alt="">
            </router-link>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
    },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel{
   @include panel;
   margin-bottom: 0;
   > h4{
     display: none;
   }
   .content{
     img{
       display: block;
       width: 100%;
     }
   }
}
</style>
