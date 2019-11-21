<template>
    <div>
        <van-sticky>
            <van-nav-bar title="九山" >
                <van-icon name="search" slot="right" />
            </van-nav-bar>
        </van-sticky>
        <van-swipe style="height: 200px;" :autoplay="3000">
            <van-swipe-item v-for="(image, index) in images" :key="index">
                <img :src="image" style="height: 200px;width: 100%"/>
            </van-swipe-item>
        </van-swipe>

        <van-grid :colum-num="4">
            <van-grid-item icon="photo-o" :text="bean.title" v-for="(bean,index) in spuList" :key="index">
                <van-image style="height: 80px"  slot="icon" :src="bean.url" fit="cover" round />
            </van-grid-item>

        </van-grid>
        <!--<p>极品豪车</p>-->
        <div class="teaweb_title">热销榜</div>
        <van-grid :column-num="3">
            <van-grid-item
                    v-for="(item,index) in hotList"
                    :key="index"
                    icon="photo-o"
                    :text="item.title">
                <van-image style="height: 80px;width: 80px"  slot="icon" :src="item.url" fit="scale-down"  />
                <div slot="text" style="font-size: 10px;flex-direction: column;justify-content: center;display: flex">

                    <span>{{item.title}}</span>
                    <span>{{item.price}}</span>
                </div>
            </van-grid-item>

        </van-grid>

        <!--<p>精品茶具</p>-->
        <div class="teaweb_title">精品推荐</div>
        <van-grid :border="false" :column-num="3">
            <van-grid-item v-for="(image,index) in images" :key="index" text="尽请期待">
                <van-image :src="image" style="height: 80px" fit="cover" slot="icon" />
            </van-grid-item>
        </van-grid>

        <div class="teaweb_title">礼品必备</div>
        <van-grid :border="false" :column-num="3">
            <van-grid-item v-for="(image,index) in images" :key="index" text="尽请期待">
                <van-image :src="image" style="height: 80px" fit="cover" slot="icon"/>
            </van-grid-item>
        </van-grid>

    </div>
</template>

<script>
    export default {
        name: 'home',
        data() {
            return {
                images: [
                    'https://www.93goodtea.com/img/tea/tea25.jpg',
                    'https://www.93goodtea.com/img/pic/775x362-2.jpg',
                    'https://www.93goodtea.com/img/pic/775x362.jpg',

                ],
                spuList:[
                    {title:"云雾毛尖",url:"https://www.93goodtea.com/img/pic/504x567%E5%89%AF%E6%9C%AC.jpg"},
                    {title:"手工茶",url:"https://www.93goodtea.com/img/pic/421x273%E5%89%AF%E6%9C%AC.jpg"},
                    {title:"明前茶",url:"https://www.93goodtea.com/img/pic/354x271%E5%89%AF%E6%9C%AC.jpg"},
                    {title:"谷雨茶",url:"https://www.93goodtea.com/img/pic/271x271.jpg"},
                ],
                hotList:[
                    {title:"精品贴合",url:"https://www.93goodtea.com/img/tea/tea63.jpg",price:"10元/只"},
                    {title:"精品礼盒",url:"https://www.93goodtea.com/img/tea/tea22.jpg",price:"40元/只"},
                    {title:"明前二级次芽",url:"https://www.93goodtea.com/img/tea/tea53.jpg",price:"560元/500克"},
                    {title:"明前一级包芽",url:"https://www.93goodtea.com/img/tea/tea53.jpg",price:"880元/500克"},
                    {title:"明前特级珍芽",url:"https://www.93goodtea.com/img/tea/tea20.jpg",price:"1260元/500克"},
                    {title:"明前特级顶芽",url:"https://www.93goodtea.com/img/pic/421x273%E5%89%AF%E6%9C%AC.jpg",price:"1688元/500克"},
                ]
            };
        },
        methods:{
            goDetail(index){
                this.$router.push('goodsDetail')
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


</style>
