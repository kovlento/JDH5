<template lang="html">
    <article class="">
        <Slider :items="items" :cname="$style.slider"/>
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in enters" :key="item.img">
                <router-link :to="{name:item.href}">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{ item.title }}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>

<script>
import Slider from "../core/slider.vue"
export default {
    components: {
        Slider,
    },
    data() {
        return {
            items: [{
                href: "home",
                src: "//m.360buyimg.com/mobilecms/s700x280_jfs/t1/24046/10/6380/94217/5c511b9dEcc9ba39c/7913173ae5ed0617.jpg!cr_1125x445_0_171!q70.jpg.dpg",
            }, {
                href: "home",
                src: "//m.360buyimg.com/mobilecms/s700x280_jfs/t1/61433/5/14484/83564/5dbd0c15Eabaf413e/d2382b828cfd450a.jpg!cr_1125x445_0_171!q70.jpg.dpg",
            }, {
                href: "home",
                src: "//m.360buyimg.com/mobilecms/s700x280_jfs/t1/79939/21/13282/200865/5dbb08cdE932aa652/435ce52431f0d107.jpg!cr_1125x445_0_171!q70.jpg.dpg",
            }, {
                href: "home",
                src: "//m.360buyimg.com/mobilecms/s700x280_jfs/t1/62008/34/14059/127095/5dba796bE85fc285b/360f8c9e33c2729f.jpg!cr_1125x445_0_171!q70.jpg.dpg",
            }],
            enters: [{
                href: "download",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
                title: "优惠券",
            },
            {
                href: "download",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
                title: "领福利",
            },
            {
                href: "download",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
                title: "抢钢镚",
            },
            {
                href: "download",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
                title: "白条提额",
            },
            {
                href: "download",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t1/36242/13/119/12214/5cb06492E0c73a66f/a284f91242e27af1.png?width=90&height=90",
                title: "领京豆",
            }],
        }
    },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.slider{
 margin-top: 120px;
 img{
     width: 100%;
 }
}
.list{
  @include list(row);
  background: #fff;
  padding-top: 40px;
  padding-bottom: 20px;
  justify-content: space-around;
  a{
    text-decoration: none;
  }
  .item{
    text-align: center;
    img{
      display: inline-block;
      width: 90px;
      height: 90px;
    }
    h4{
      font-size: 26px;
      margin-top: 12px;
      color:#666;
    }
  }
}
</style>
