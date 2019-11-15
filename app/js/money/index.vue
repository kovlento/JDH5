<template lang="html">
    <div>
        <Heador/>
        <Mslider/>
        <Adfirst/>
        <Money/>
        <Adsecond/>
        <Finance/>
        <Adthird/>
        <Footor cname="mfooter"/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Footor from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Money from "../home/money.vue"
import Mslider from "./mslider.vue"
import Adfirst from "./adfirst.vue"
import Adsecond from "./adsecond.vue"
import Finance from "./finance.vue"
import Adthird from "./adthird.vue"
export default {
    components: {
        Heador,
        Footor,
        Mslider,
        Money,
        Navbar,
        Adfirst,
        Adsecond,
        Finance,
        Adthird,
    },
}
</script>
<style lang="scss">
    .mfooter{
        margin-top: 0;
        ul{
            li:first-child{
                display: none;
            }
        }
    }
</style>
