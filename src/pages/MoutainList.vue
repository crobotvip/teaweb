<template>
    <div>
        <van-sticky>
            <van-nav-bar title="大别山脉">
            </van-nav-bar>
        </van-sticky>
        <div>
            <van-cell
                    v-for="item in list"
                    :key="item"


            >
                <van-image :src="item.url" style="height: 200px;width: 100%" fit="cover" />
                <p style="text-align: center">{{item.title}}</p>

            </van-cell>

        </div>

    </div>
</template>

<script>

    export default {
        name: 'goods',
        components: {},
        data() {
            return {
                list: [{"url":"https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=900135045,1976899860&fm=26&gp=0.jpg",title:"鸡公山"},
                    {"url":"https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=2944906482,1620656057&fm=26&gp=0.jpg",title:"车云山"},
                    {"url":"https://gss3.bdstatic.com/7Po3dSag_xI4khGkpoWK1HF6hhy/baike/c0%3Dbaike92%2C5%2C5%2C92%2C30/sign=7bf99062f21f3a294ec5dd9cf84cd754/0b55b319ebc4b745b40486aacdfc1e178b8215fd.jpg",title:"震雷山"},
                    {"url":"https://gss2.bdstatic.com/9fo3dSag_xI4khGkpoWK1HF6hhy/baike/c0%3Dbaike92%2C5%2C5%2C92%2C30/sign=caad5d1d963df8dcb23087c3ac7819ee/f3d3572c11dfa9ec307105fd6bd0f703908fc1f9.jpg",title:"黑龙潭"},
                    {"url":"https://gss0.bdstatic.com/94o3dSag_xI4khGkpoWK1HF6hhy/baike/c0%3Dbaike180%2C5%2C5%2C180%2C60/sign=181620a3be3eb13550cabfe9c777c3b6/8694a4c27d1ed21b96e822aeaf6eddc451da3f53.jpg",title:"灵山"},
                    {"url":"https://www.93goodtea.com/img/tea/tea25.jpg",title:"皇城山"}],
                loading: false,
                finished: true
            };
        },
        methods: {
            onLoad() {
                // 异步更新数据
//                setTimeout(() => {
//                    for (let i = 0; i < 10; i++) {
//                        this.list.push(this.list.length + 1);
//                    }
//                    // 加载状态结束
//                    this.loading = false;
//
//                    // 数据全部加载完成
//                    if (this.list.length >= 40) {
//                        this.finished = true;
//                    }
//                }, 500);
            },
            gotoGoodsDetail(){
                this.$router.push('goodsDetail')
            }
        }
    };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less">

</style>
