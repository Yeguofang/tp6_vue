<template>
    <div>
        <!-- 顶部tab -->
        <header_></header_>
        <!-- 搜索栏 -->
        <search></search>
        <!-- 首页导航栏 -->
        <div class="top-nav bg3">
            <div class="nav-box inner">
                <div class="all-cat">
                    <div class="title"><i class="iconfont icon-menu"></i> 全部分类</div>

                    <div class="cat-list__box">
                        <div class="cat-box" v-for="(v,k) in categoryInfo">
                            <div class="title">
                                <i class="iconfont icon-skirt ce"></i>
                                <span v-text="v.name" @click="category(v.category_id)"></span>
                            </div>
                            <ul class="cat-list clearfix">
                                <li @click="category(v1.category_id)" v-for="(v1,k1) in v.list" v-text="v1.name"></li>
                            </ul>
                            <div class="cat-list__deploy">
                                <div class="deploy-box">
                                    <div class="genre-box clearfix" v-for="(v1,k1) in v.list">
                                        <span class="title"><span v-text="v1.name"></span>：</span>
                                        <div class="genre-list">
                                            <a @click="category(v2.category_id)" v-for="(v2,k2) in v1.list"
                                               v-text="v2.name"></a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <ul class="nva-list">
                    <a href="/">
                        <li class="active">首页</li>
                    </a>
                </ul>
            </div>
        </div>
        <!-- 顶部轮播 -->
        <div class="swiper-container banner-box">
            <div class="swiper-wrapper">
                <div class="swiper-slide">
                    <router-link to="/detail">
                        <img src="https://img12.360buyimg.com/da/jfs/t1/93922/4/3509/47504/5de0e99aEd9c531e9/a03cd528ff983c5f.jpg"
                             class="cover">
                    </router-link>
                </div>
                <div class="swiper-slide">
                    <router-link to="/detail"><img
                            src="https://img30.360buyimg.com/da/jfs/t1/63018/26/15387/89966/5dccc00cE2e1c5cfb/e502efb14dc3e8c8.jpg"
                            class="cover"></router-link>
                </div>
                <div class="swiper-slide">
                    <router-link to="/detail"><img
                            src="https://img14.360buyimg.com/da/jfs/t1/59402/20/5415/153057/5d37b3f4E565eee1d/b3818446414de902.jpg"
                            class="cover"></router-link>
                </div>
                <div class="swiper-slide">
                    <router-link to="/detail"><img
                            src="https://img11.360buyimg.com/da/jfs/t1/39081/22/12393/126937/5d37b4b8E52d6ce7c/dcbe17e4d5047824.jpg"
                            class="cover"></router-link>
                </div>
                <div class="swiper-slide">
                    <router-link to="/detail"><img
                            src="https://img20.360buyimg.com/da/jfs/t1/73731/27/16369/74974/5ddf9a11E16271c71/35a86509b23c0336.jpg"
                            class="cover"></router-link>
                </div>
            </div>
            <div class="swiper-pagination"></div>
        </div>
        <div class="content inner" style="margin-bottom: 40px;">
            <section class="scroll-floor floor-2">
                <div class="floor-title">
                    <i class="iconfont icon-skirt fz16"></i> 女装
                    <div class="case-list fz0 pull-right">
                        <a href="item_category.html">高端女装</a>
                        <a href="item_category.html">时尚女装</a>
                        <a href="item_category.html">上装</a>
                        <a href="item_category.html">下装</a>
                        <a href="item_category.html">裙装</a>
                        <a href="item_category.html">内衣</a>
                    </div>
                </div>
                <div class="con-box">
                    <a class="left-img hot-img" href="">
                        <img src="https://img14.360buyimg.com/cms/jfs/t1/56617/17/1177/72633/5cee2b3fE593f7a14/7faa2b84748e11e5.jpg"
                             alt="" class="cover">
                    </a>
                    <div class="right-box">
                        <router-link to="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="@/assets/images/temp/S-001.jpg" alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </router-link>
                        <router-link to="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="https://img11.360buyimg.com/n8/jfs/t1/33712/34/14343/139215/5d0ddb64Ed3694d55/6cec565de4b8732a.jpg"
                                     alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </router-link>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="https://img11.360buyimg.com/n1/s150x150_jfs/t1/102521/18/4034/218859/5de46abeE5f6df8fb/2bd3ec95d5e71b00.jpg"
                                     alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="https://img14.360buyimg.com/n1/s150x150_jfs/t1/89332/6/4034/210605/5de46accEfb594a1b/2bb95e34120978b9.jpg"
                                     alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="@/assets/images/temp/S-005.jpg" alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="https://img14.360buyimg.com/n2/jfs/t1/102659/25/271/265505/5daacb1fEaa0985e7/23b5bc89c4bd3c11.jpg"
                                     alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="@/assets/images/temp/S-007.jpg" alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="https://img10.360buyimg.com/n2/jfs/t1/75251/11/13363/334605/5daac7baEe6f10939/e5c2f4dc7e32fda3.jpg"
                                     alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                    </div>
                </div>
            </section>
            <section class="scroll-floor floor-3">
                <div class="floor-title">
                    <i class="iconfont icon-fushi fz16"></i> 男装
                    <div class="case-list fz0 pull-right">
                        <a href="item_category.html">高端女装</a>
                        <a href="item_category.html">时尚女装</a>
                        <a href="item_category.html">上装</a>
                        <a href="item_category.html">下装</a>
                        <a href="item_category.html">裙装</a>
                        <a href="item_category.html">内衣</a>
                    </div>
                </div>
                <div class="con-box">
                    <a class="left-img hot-img" href="">
                        <img src="https://img11.360buyimg.com/cms/jfs/t1/49578/23/1175/20557/5cedeee6Ea319f1d6/a7cf5906ada4141d.jpg"
                             alt="" class="cover">
                    </a>
                    <div class="right-box">
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="https://img10.360buyimg.com/n2/jfs/t1/83976/17/13522/269558/5dad16d6E44f16555/c46f52288570118a.jpg"
                                     alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="https://img11.360buyimg.com/n2/jfs/t1/64354/38/10354/407895/5d7f0967E4e4ccd74/4265f64d6f52603a.jpg"
                                     alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="@/assets/images/temp/M-003.jpg" alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="https://img10.360buyimg.com/n2/jfs/t1/83976/17/13522/269558/5dad16d6E44f16555/c46f52288570118a.jpg"
                                     alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="https://img11.360buyimg.com/n8/jfs/t1/33712/34/14343/139215/5d0ddb64Ed3694d55/6cec565de4b8732a.jpg"
                                     alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="https://img11.360buyimg.com/n2/jfs/t1/64354/38/10354/407895/5d7f0967E4e4ccd74/4265f64d6f52603a.jpg"
                                     alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="@/assets/images/temp/M-007.jpg" alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                        <a href="/detail" class="floor-item">
                            <div class="item-img hot-img">
                                <img src="https://img11.360buyimg.com/n8/jfs/t1/33712/34/14343/139215/5d0ddb64Ed3694d55/6cec565de4b8732a.jpg"
                                     alt="纯色圆领短袖T恤活a动衫弹" class="cover">
                            </div>
                            <div class="price clearfix">
                                <span class="pull-left cr fz16">￥18.0</span>
                                <span class="pull-right c6">进货价</span>
                            </div>
                            <div class="name ep" title="纯色圆领短袖T恤活a动衫弹力柔软">纯色圆领短袖T恤活a动衫弹力柔软</div>
                        </a>
                    </div>
                </div>
            </section>
        </div>
        <footer_></footer_>
    </div>
</template>

<script>
    import header_ from '../components/header_'
    import search from '../components/search'
    import footer_ from '../components/footer_'
    import {category} from "../lib/interface";

    export default {
        components: {header_, search, footer_},
        name: "index",
        data() {
            return {
                categoryInfo: [],
            }
        },
        mounted() {
            // 顶部banner轮播
            var banner_swiper = new Swiper('.banner-box', {
                autoplayDisableOnInteraction: false,
                pagination: '.banner-box .swiper-pagination',
                paginationClickable: true,
                autoplay: 5000,
            });
            // 新闻列表滚动
            var notice_swiper = new Swiper('.notice-box .swiper-container', {
                paginationClickable: true,
                mousewheelControl: true,
                direction: 'vertical',
                slidesPerView: 10,
                autoplay: 2e3,
            });
            $('.to-top').toTop({position: false});
            this.getCategoryInfo();
        },
        methods: {
            category(id) {
                this.$router.replace("/category?cid=" + id);
            },
            async getCategoryInfo() {
                let result = await category();
                this.categoryInfo = result.result;
                console.log(this.categoryInfo);
            }

        }
    }
</script>

<style scoped>

</style>
