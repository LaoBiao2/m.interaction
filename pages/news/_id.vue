<template>
	<section>
		<div class="container">
			<div class="news">
                <div class="content">
                    <div class="title-box">
                        <div class="title-content">
                            <b>{{detailList.new_title}}</b>
                            <span><i></i>{{detailList.new_time}}</span>
                        </div>
                    </div>
                    <div class="news-box clearfix">
                        <div class="news-content" v-html="detailContent">
                        </div>
                        <div class="show-btn"><p @click="more(detailList.id)"><span>展开剩余80%</span><i></i></p></div>
                    </div>
                    <div class="news-nav">
                        <span class="nav-span"><span>上一篇:</span><nuxt-link :to="'/news/' + newsNavPrev.id ">{{newsNavPrev.new_title}}</nuxt-link></span>
                        <span class="nav-span"><span>下一篇:</span><nuxt-link :to="'/news/' + newsNavNext.id ">{{newsNavNext.new_title}}</nuxt-link></span>
                    </div>
                    <div class="hot-news">
                        <h6><b>热门推荐</b></h6>
                        <ul>
                            <li v-for="(hotLi, key) in hotList" :key="key" :class="'li-' + (key+1)" v-if="key < 3">
                                <nuxt-link :to="'/news/' + hotLi.id" class="clearfix">
                                    <div class="img-box fl">
                                        <img :src="dataList.config.con_prefix + hotLi.new_img" alt="">
                                    </div>
                                    <div class="txt fr">
                                        <b>{{hotLi.new_title}}</b>
                                        <span><i></i>{{hotLi.new_time}}</span>
                                    </div>
                                </nuxt-link>
                            </li>
                        </ul>
                    </div>
                    <span id="top-span"></span>
                </div>
            </div>
		</div>
	</section>
</template>

<script>
	export default {
        async asyncData({ app, params }) {
            let  data  = await app.$axios.$get('/api/news/' + params.id);
            return { 
                dataList: data,
                detailList: data.detail,
                hotList: data.hot,
                newsNavPrev: data.prev,
                newsNavNext: data.next,
                detailContent: data.detail.new_descriptions
            }
        },
        data() {
            return {
                newsList: [
                    // {
                    //     newsImg: '/images/news/news_img1.jpg',
                    //     newsId: '1',
                    //     newsTitle: '10年客服老司机教你这样处理棘手的客户投诉',
                    //     newsDate: '2018/06/20'
                    // },{
                    //     newsImg: '/images/news/news_img2.jpg',
                    //     newsId: '2',
                    //     newsTitle: '10年客服老司机教你这样处理棘手的客户投诉',
                    //     newsDate: '2018/06/20'
                    // },{
                    //     newsImg: '/images/news/news_img3.jpg',
                    //     newsId: '3',
                    //     newsTitle: '10年客服老司机教你这样处理棘手的客户投诉',
                    //     newsDate: '2018/06/20'
                    // }
                ],
                newsNavPrev: {
                    // id: '1',
                    // title: '服务外包业促粤港澳大湾区城市建设'
                },
                newsNavNext: {
                    // id: '2',
                    // title: '呼叫中心如何正确衡量通话质量'
                },
                newsId: '',
                dataList: [],
                detailList: '',
                detailContent: ''
            }
        },
		mounted() {
            $(".news-box .news-content p").find("span").attr("style", "");
            this.detailContent = this.detailList.new_descriptions;
            $("#top-span").click(function () {
                $('html, body').animate({scrollTop: '0px'}, 500);
            })            
            console.log(this.detailList)
		},
        head() {
            return this.$seo(this.dataList.header.title, this.dataList.header.descriptions, this.dataList.header.keywords)
        },
        methods: {
            more(i) {
                $(".news-box .show-btn").toggleClass("up");
                this.$axios.get("/api/news/" + i)
                .then((response) => {
                    if ($(".news-box .show-btn p span").text() == '收起' ) {
                        $(".news-box .show-btn p span").text('展开剩余80%');
                        this.detailContent = response.data.detail.new_descriptions;
                    } else {
                        $(".news-box .show-btn p span").text('收起');
                        this.detailContent = response.data.detail.new_content;
                    }
                })
                .catch(function (error) {
                    console.log(error);
                });
            }
        }
	};

</script>

<style lang="scss" scoped>
.news {
    padding: 50px 0;
    background-color: #fff;
    .title-box {
        border-bottom: 2px solid #e0e0e0;
        .title-content {
            padding-bottom: 22px;
            b {
                font-size: 36px;
                color: #333;
                display: inline-block;
                padding-bottom: 18px;
                line-height: 44px;
            }
            span {
                font-size: 26px;
                color: #333;
                display: block;
                i {
                    width: 20px;
                        height: 20px;
                        display: inline-block;
                        background: url(/images/news/news_icon.png) 0 0 no-repeat;
                        background-size: 264px 90px;
                        margin-right: 12px;
                }
            }
        }
        
    }
    .news-box {
        padding: 50px 0 160px;
        border-bottom: 2px solid #e0e0e0;
        position: relative;
        .news-content {
            font-size: 14px;
            p,span {
                font-size: 26px;
                color: #666;
                line-height: 36px;
                margin-bottom: 43px;
                img {
                    display: block;
                    margin: 43px auto;
                }
            }
        }
        .show-btn {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 360px;
            display: block;
            background: url(/images/about/b1_img.png) no-repeat top;
            background-size: contain;
            p {
                position: absolute;
                bottom: 60px;
                left: 0;
                text-align: center;
                width: 100%;
                background-color: #fff;
                span {
                    font-size: 26px;
                    color: #e91222;
                }
                i {
                    width: 22px;
                    height: 12px;
                    display: inline-block;
                    vertical-align: middle;
                    margin-left: 5px;
                    background: url(/images/about/about_icon.png) -478px -635px no-repeat;
                    background-size: 812px 647px;
                }
            }
        }
        .show-btn.up {
            background: none;
            p {
                // bottom: 20px;
                i {
                    background-position-y: -617px;
                }
            }
        }
    }

    /* nav */
    .news-nav {
        padding-top: 43px;
        .nav-span {
            display: block;
            font-size: 26px;
            margin-bottom: 40px;
            span {
                color: #333;
                width: 104px;
                float: left;
            }
            a {
                color: #666;
                width: 600px;
                overflow: hidden;
                text-overflow:ellipsis;
                white-space: nowrap;
                display: inline-block;
            }
            a.active {
                color: #e91222;
            }
        }
    }
    
    .hot-news {
        h6 {
            margin-top: 28px;
            border-bottom: 2px solid #e0e0e0;
            position: relative;
            height: 62px;
            b {
                font-size: 30px;
                color: #333;
                display: inline-block;
                padding-bottom: 16px;
                border-bottom: 2px solid #e91222;
                position: absolute;
                left: 0;
                bottom: -2px;
            }
        }
        ul {
            li {
                border-bottom: 1px solid #e3e3e3;
                padding: 30px 0;
                box-sizing: border-box;
                height: 210px;
                .img-box {
                    width: 220px;
                    height: 150px;
                    border-radius: 10px;
                    overflow: hidden;
                    img {
                        width: 100%;
                        height: 100%;
                    }
                }
                .txt {
                    width: 456px;
                    margin-right: 10px;
                    b {
                        font-size: 30px;
                        line-height: 36px;
                        color: #333;
                        overflow : hidden;
                        text-overflow: ellipsis;
                        display: -webkit-box;
                        -webkit-line-clamp: 2;
                        -webkit-box-orient: vertical;
                        margin: 10px 0 40px;
                        height: 72px;
                    }
                    span {
                        font-size: 26px;
                        color: #666;
                        display: block;
                        i {
                            width: 22px;
                            height: 22px;
                            display: inline-block;
                            background: url(/images/news/news_icon.png) 0 0 no-repeat;
                            background-size: 264px 90px;
                            margin-right: 10px;
                        }
                    }
                }
            }
            li:last-child {
                border-bottom: none;
            }
        }
    }

    #top-span {
        width: 92px;
        height: 90px;
        display: inline-block;
        background: url(/images/news/news_icon.png) -83px 0 no-repeat;
        background-size: 264px 90px;
        position: fixed;
        bottom: 304px;
        right: 20px;
    }
}
</style>

<style lang="scss">
.news-box {
    .news-content {
        font-size: 26px !important;
        color: #666 !important;
        line-height: 36px !important;
        p,span {
            font-size: 26px !important;
            color: #666 !important;
            line-height: 36px !important;
            // margin-bottom: 43px !important;
            img {
                display: block !important;
                margin: 43px auto !important;
            }
        }
    }
}
</style>
