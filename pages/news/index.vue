<template>
    <section>
        <news-header></news-header>
        <div class="container News">
            <ul class="content">
                <li v-for="(newsLi, key) in newsList" :key="key" :class="'li-' + (key+1)">
                    <nuxt-link to="" class="clearfix">
                        <div class="img-box fl">
                            <img :src="newsLi.newsImg" alt="">
                        </div>
                        <div class="txt fr">
                            <b>{{newsLi.newsTitle}}</b>
                            <span><i></i>{{newsLi.newsDate}}</span>
                        </div>
                    </nuxt-link>
                </li>
            </ul>
            <span class="tip-span"><i></i>努力加载中...</span>
        </div>
    </section>
</template>

<script>
import NewsHeader from '~/components/NewsHeader.vue';
export default {
    data() {
        return {
            newsList: [
                {
                    newsImg: '/images/news/news_img1.jpg',
                    newsId: '1',
                    newsTitle: '10年客服老司机教你这样处理棘手的客户投诉',
                    newsDate: '2018/06/20'
                },{
                    newsImg: '/images/news/news_img2.jpg',
                    newsId: '2',
                    newsTitle: '10年客服老司机教你这样处理棘手的客户投诉',
                    newsDate: '2018/06/20'
                },{
                    newsImg: '/images/news/news_img3.jpg',
                    newsId: '3',
                    newsTitle: '10年客服老司机教你这样处理棘手的客户投诉',
                    newsDate: '2018/06/20'
                },{
                    newsImg: '/images/news/news_img4.jpg',
                    newsId: '4',
                    newsTitle: '10年客服老司机教你这样处理棘手的客户投诉',
                    newsDate: '2018/06/20'
                },{
                    newsImg: '/images/news/news_img5.jpg',
                    newsId: '5',
                    newsTitle: '10年客服老司机教你这样处理棘手的客户投诉',
                    newsDate: '2018/06/20'
                },{
                    newsImg: '/images/news/news_img6.jpg',
                    newsId: '6',
                    newsTitle: '10年客服老司机教你这样处理棘手的客户投诉',
                    newsDate: '2018/06/20'
                }
            ],
        }
    },
    components: {
        NewsHeader
    }
}
</script>

<style lang="scss" scoped>
.News {
    ul {
        padding-top: 30px;
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
                        width: 20px;
                        height: 20px;
                        display: inline-block;
                        background: url(/images/news/news_icon.png) 0 0 no-repeat;
                        background-size: 264px 90px;
                        margin-right: 10px;
                    }
                }
            }
        }
    }
    .tip-span {
        height: 104px;
        line-height: 104px;
        font-size: 24px;
        color: #666;
        display: block;
        text-align: center;
        i {
            width: 35px;
            height: 35px;
            display: inline-block;
            margin-right: 25px;
            vertical-align: middle;
            background: url(/images/news/news_icon.png) -229px 0 no-repeat;
            background-size: 264px 90px;
        }
    }
}

</style>
