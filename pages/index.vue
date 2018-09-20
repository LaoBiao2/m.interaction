<template>
    <section class="container">
        <div>
            <div class="banner">
                <div v-swiper:bannerSwiper="swiperOption">
                    <div class="swiper-wrapper">
                        <div class="swiper-slide" v-for="(banner, key) in bannerList" :key="key">
                            <div class="img-bg">
                                <!-- <img src="/images/index/banner.jpg" alt=""> -->
                                <img :src="dataList.config.con_prefix + banner.ban_img" alt="">
                            </div>
                            <div class="content">
                                <div class="txt">
                                    <h2><span>{{banner.ban_short_title}}</span>{{banner.ban_long_title}}</h2>
                                    <p>{{banner.ban_text}}</p>
                                    <a href="javascript:;">{{banner.ban_button}}</a>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="swiper-pagination"></div>
                </div>
            </div>
            <div class="banner-bottom">
                <ul class="clearfix">
                    <li class="li-1">
                        <i></i>
                        <span>专注客户服务商</span>
                    </li>
                    <li class="li-2">
                        <i></i>
                        <span>专业的服务团队</span>
                    </li>
                    <li class="li-3">
                        <i></i>
                        <span>专业的服务体系</span>
                    </li>
                    <li class="li-4">
                        <i></i>
                        <span>全天候客户服务</span>
                    </li>
                </ul>
            </div>
            <div class="box b1">
                <h4>1000余名专业客服持证上岗</h4>
                <h5>「在线客服」与「电话客服」均能完美服务</h5>
                <div class="b1-swiper">
                    <div v-swiper:b1Swiper="swiperOption1">
                        <div class="swiper-wrapper">
                            <div class="li-1 swiper-slide">
                                <div class="li-box">
                                    <span class="span-img">
                                        <img src="/images/index/b1_img1.png" alt="">
                                        <i></i>
                                        </span>
                                    <div class="txt">
                                        <b>网店客服</b>
                                        <span>淘宝、天猫、京东售前 售后客服贴心服务</span>
                                        <p>售前：在线解答客户咨询问题 引导客户下单，积极促成好评
                                        <br/><br/>售后：退换货，物流问题，客 户的反映和投诉，差评等处理</p>
                                    </div>
                                </div>
                            </div>
                            <div class="li-2 swiper-slide">
                                <div class="li-box">
                                    <span class="span-img">
                                        <img src="/images/index/b1_img2.png" alt="">
                                        <i></i>
                                    </span>
                                    <div class="txt">
                                        <b>电话客服</b>
                                        <span>呼出、呼入、电话客服的 完美服务</span>
                                        <p>呼出：电话销售、电话邀约电 话回访、电话调研
                                        <br/><br/>呼入：业务咨询、业务办理投 诉处理等服务</p>
                                    </div>
                                </div>
                            </div>
                            <div class="li-3 swiper-slide">
                                <div class="li-box">
                                    <span class="span-img">
                                        <img src="/images/index/b1_img3.png" alt="">
                                        <i></i>
                                    </span>
                                    <div class="txt">
                                        <b>在线客服</b>
                                        <span>QQ、微信、web/app 在线客服轻松搞定</span>
                                        <p>回复在线客户咨询引导客户下单，处理订单记录汇总咨询
                                        <br/><br/>记录汇总咨询事件及时分析并 反馈给相应部门</p>
                                    </div>
                                </div>
                            </div>
                            <div class="li-4 swiper-slide">
                                <div class="li-box">
                                    <span class="span-img">
                                        <img src="/images/index/b1_img4.png" alt="">
                                        <i></i>
                                    </span>
                                    <div class="txt">
                                        <b>呼叫中心</b>
                                        <span>提供专业的呼叫中心外 包服务解决方案</span>
                                        <p>10000余持证上岗的专业客服 快速开启客户服务
                                        <br/><br/>提供专业的呼叫中心外 包服务解决方案</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="swiper-button-prev"></div>
                    <div class="swiper-button-next"></div>
                </div>
            </div>
            <div class="box b2">
                <h4>客服外包，我们能为您做的</h4>
                <div class="b2-swiper">
                    <div v-swiper:b2Swiper="swiperOption2">
                        <div class="swiper-wrapper">
                            <div class="swiper-slide" v-for="(b2Item, key) in b2Items" :key="key">
                                <div :class="'slider-' + (key+1)">
                                    <span class="span-i"><i></i></span>
                                    <div class="txt">
                                        <b>{{b2Item.title}}</b>
                                        <span>{{b2Item.content}}</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-pagination-b2"></div>
                    </div>
                </div>
            </div>
            <div class="box b3">
                <div class="content">
                    <h4>看过很多攻略，却依然做不好客服</h4>
                    <div class="b3-box">
                        <b>如果您有这些困扰，一切都让互动商务为您解决</b>
                        <ul>
                            <li><i></i>严重内耗</li>
                            <li><i></i>用人成本上升</li>
                            <li><i></i>业绩较差</li>
                            <li><i></i>招聘难流动性大</li>
                            <li><i></i>人员难管理</li>
                            <li><i></i>过度劳累筋疲力尽</li>
                            <li><i></i>大促忙不过来</li>
                            <li><i></i>夜间咨询忙不过来</li>
                        </ul>
                    </div>
                    <i class="i-img"></i>
                </div>
            </div>
            <div class="box b4">
                <div class="content">
                    <h4>我们的优势</h4>
                    <h5>沟通零距离，服务无止境<br/>用心倾听、传递微笑、提供帮助、用心沟通、解决问题</h5>
                    <div class="b4-swiper">
                        <div v-swiper:b4Swiper="swiperOption4">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide" v-for="(b4Item, key, index) in b4Items" v-bind:key="index" v-bind:class="'li-'+ (key+1)">
                                    <span class="top-span"><i></i>{{b4Item.title}}</span>
                                    <p v-html="b4Item.content"></p>
                                </div>
                            </div>
                            <div class="swiper-pagination-b4"></div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="box b5">
                <div class="content">
                    <h4>新闻资讯</h4>
                    <div class="b5-box clearfix">
                        <div class="b5-top">
                            <div class="img-box"><img src="/images/index/b5_img.jpg" alt=""></div>
                            <div class="txt">
                                <nuxt-link :to="'/news/' + b5Items[1].id"><span class="title-span"><i></i>{{b5Items[1].new_title}}</span></nuxt-link>
                                <p>
                                    {{b5Items[1].new_descriptions}}
                                </p>
                                <span class="time-span"><i></i>{{b5Items[1].new_time}}</span>
                            </div>
                        </div>
                        <ul>
                            <li v-for="(b5Item, index) in b5Items" :key="index" v-if="0 < index && index < 4">
                                <nuxt-link :to="'/news/' + b5Item.id">
                                    <span class="title-span">{{b5Item.new_title}}</span>
                                    <p>{{b5Item.new_descriptions}}</p>
                                    <span class="time-span"><i></i>{{b5Item.new_time}}</span>
                                </nuxt-link>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    async asyncData({ app }) {
        let  data  = await app.$axios.$get('/api');
        
        // console.log(data)
        return { 
            dataList: data, 
            bannerList: data.banner_wap,
            b5Items: data.information
        }
    },
    data() {
        return {
            swiperOption: {
                effect : 'fade',
                pagination: '.swiper-pagination',
                paginationClickable :true,
                loop: true
            },
            swiperOption1: {
                effect : 'coverflow',
                slidesPerView: "auto",
                centeredSlides: true,
                coverflow: {
                    rotate: 20,
                    stretch: 28,
                    depth: 60,
                    modifier: 3,
                    slideShadows : false
                },
                loop: true,
                nextButton: '.swiper-button-next',
                prevButton: '.swiper-button-prev',
            },
            swiperOption2: {
                slidesPerView: "auto",
                pagination: '.swiper-pagination-b2',
                spaceBetween: 18,
                centeredSlides: true,
                loop: true,
            },
            b2Items: [
                {
                    title: '管理规范 服务周全',
                    content: '托管人员的各种客服、劳动事务均由人力资源公司处理，并提供有关社会保障、劳动客服政策等方面的政策法规咨询。'
                },{
                    title: '解放人力 创造价值',
                    content: '免去办理各种琐碎的员工录用（退工）、社会保险申报、住房公积金办理等各种客服。'
                },{
                    title: '人员稳定 收入稳定',
                    content: '铁打的营盘，流水的兵解除了长期人员流失，人员缺少、没人值班的基本因素从而达到稳定的销售！'
                },{
                    title: '简化手续 降低成本',
                    content: '由于大量事务性工作被外包了出去，人力资源管理者足不出户圆满完成客服工作；减少人员和设备，避免重复操作，节省大量资金时间。'
                },{
                    title: '提高满意度 增强归属感',
                    content: '完善客服服务体系，解决员工的后顾之忧，提高员工满意度。同时由于劳动合同的主体仍是企业，员工对企业归属感更强，忠诚度更高。 '
                }
            ],
            swiperOption4: {
                pagination: '.swiper-pagination-b4',
                centeredSlides: true,
                spaceBetween: 18,
                loop: true,
            },
            b4Items: [
                {
                    title: '专业化',
                    content: '优秀的呼叫中心服务提供商，有多次业务重组整合的经验，新业务上马快、起点高；可确保服务质量的高水准；省去企业管理方面的烦恼，有利于简化 管理体系，优化管理水平。'
                },{
                    title: '灵活性',
                    content: '客户可以得到弹性的呼叫中心，其规模根据企业的要求随时扩大或缩小；还可以随着运营商的技术更新，始终得到一个相对先进的呼叫中心系统，企业通过外包得到的呼叫中心，其可改善性、可维护性、可开发性和可控制性都非常强。'
                },{
                    title: '节约成本',
                    content: '极大地节省在人力、系统和管理等方面的投资，降低风险；呼叫中心通常在价格上进行竞争，规模大的呼叫中心可以降低每个客户的平均服务成本。 '
                },{
                    title: '战略性合作',
                    content: '随着商业的发展，呼叫中心外包业务的范围和焦点也随之改变了，不再只局限于简单定义成与另一个公司签定长期提供服务的合同范畴，而意味着合作者之间的战略伙伴关系，风险与目标共担。企业可以集中精力从事其核心业务，而将剩下的工作委托给外包服务商。'
                },{
                    title: '团队优势',
                    content: '最专业的呼叫中心管理团队：可提供管理咨询、调查研究、数据分析、员工规划指导，以专家的视角为企业提供咨询服务。及时的人员补充：保证10天到岗。长期外包各保险公司客服及客户满意度调查和保单后期处理工作，我们的团队熟悉其工作流程，有丰富的管理经验。'
                },{
                    title: '服务承诺',
                    content: '* 7*24小时全天候网络安全和客户数据安全的保证。<br/>'
                            + '* 5*12小时热线咨询及在线客服。<br/>'
                            + '* 根据客户意愿签订保密协议，从法律效力上保证客户资料安全。<br/>'
                            + '* 快速响应，保证系统稳定性。<br/>'
                            + '* 专设服务回访和投诉小组，保证服务质量。<br/>'
                            + '* 专业客服一对一服务。'
                }
            ],
            bannerList: [],
            dataList: [],
            b5Items: []
        }
    },
    head() {
        return this.$seo(this.dataList.header.title, this.dataList.header.descriptions, this.dataList.header.keywords)
    },
    mounted() {
        console.log(this.dataList)
    }
}
</script>

<style lang="scss" scoped>
.banner {
    width: 100%;
    height: 700px;
    .swiper-container {
        height: 100%;
        .swiper-slide {
            position: relative;
        }
    }
    .img-bg {
        width: 100%;
        height: 700px;
        position: absolute;
        top: 0;
        left: 0;
        z-index: -1;
        img {
            width: 100%;
            height: 100%;
        }
    }
    .txt {
        margin-top: 162px;
        h2 {
            font-size: 52px;
            color: #fff;
            line-height: 72px;
            margin-bottom: 50px;
            span {
                color: #e91222;
                display: block;
            }
        }
        p {
            color: #fff;
            font-size: 30px;
            margin-bottom: 89px;
        }
        a {
            width: 200px;
            height: 60px;
            line-height: 60px;
            font-size: 26px;
            color: #fff;
            text-align: center;
            display: block;
            border-radius: 30px;
            background-color: #e91222;
            transition: all .3s;
        }
    }
}

.banner-bottom {
    text-align: center;
    ul {
        li {
            width: 50%;
            height: 210px;
            float: left;
            i {
                display: block;
                width: 90px;
                height: 82px;
                background: url(/images/index/index_icon.png) 0 0 no-repeat;
                background-size: 833px 608px;
                margin: 41px auto 32px;
            }
            span {
                display: block;
                color: #511616;
                font-size: 30px;
            }
        }
        li:nth-child(2),
        li:nth-child(3) {
            background-color: #f4f4f4;
        }
        .li-2 {
            i {
                width: 85px;
                background-position-x: -155px;
            }
        }
        .li-3 {
            i {
                width: 90px;
                background-position-x: -305px;
            }
        }
        .li-4 {
            i {
                width: 80px;
                background-position-x: -463px;
            }
        }

    }
}

.box {
    text-align: center;
    padding: 90px 0 80px;
    h4 {
        font-size: 36px;
        color: #333;
        font-weight: bold;
    }
    h5 {
        font-size: 24px;
        margin: 25px 0 0;
        font-size: 16px;
        color: #666;
    }
    ul {
        font-size: 0;
        li {
            display: inline-block;
        }
    }
}

.b1 {
    .b1-swiper {
        position: relative;
        .swiper-container {
            padding: 30px 20px;
            box-sizing: border-box;
        }
        .swiper-slide {
            width: 431px;
            height: 500px;
            opacity: 0;
            border-radius: 10px;
            overflow: hidden;
             -webkit-box-shadow: 1px 1px 30px rgba(0, 0, 0, .15); 
            -moz-box-shadow: 1px 1px 30px rgba(0, 0, 0, .15); 
            box-shadow: 1px 1px 30px rgba(0, 0, 0, .15);
            .li-box {
                background-color: #fff;
                .span-img {
                    height: 163px;
                    margin-bottom: 20px;
                    display: block;
                    img {
                        width: 100%;
                        height: 100%;
                    }
                }
                .txt {
                    width: 400px;
                    margin: 0 auto;
                    b {
                        font-size: 30px;
                        color: #333;
                        display: block;
                        margin-bottom: 27px;
                    }
                    span {
                        font-size: 26px;
                        color: #666;
                        line-height: 30px;
                        text-align: left;
                        font-weight: 300;
                        display: inline-block;
                    }
                    p {
                        font-size: 26px;
                        color: #999;
                        line-height: 30px;
                        margin-top: 32px;
                        text-align: left;
                    }
                }
            }
        }
        .swiper-slide-next,
        .swiper-slide-prev {
            opacity: .7;
        }
        .swiper-slide-active {
            opacity: 1;
        }
        .swiper-button-prev,
        .swiper-button-next {
            width: 58px;
            height: 58px;
            display: inline-block;
            background: url(/images/index/index_icon.png) -175px -549px no-repeat;
            background-size: 833px 608px;
        }
        .swiper-button-next {
            background-position-x: -286px;
        }
    }
}

.b2 {
    background-color: #0a0f2b;
    padding: 70px 0 80px;
    h4 {
        color: #fff;
    }
    .b2-swiper {
        margin-top: 70px;
        height: 315px;
        position: relative;
        .swiper-container {
            // height: 100%;
            .swiper-slide {
                width: 620px;
                height: 230px;
                border-radius: 10px;
                background-color: #fff;
                padding: 29px 26px 19px 22px;
                box-sizing: border-box;
            }
        }
        .span-i {
            width: 132px;
            height: 182px;
            display: table;
            float: left;
            i {
                width: 132px;
                height: 117px;
                display: block;
                margin: 33px auto;
                background: url(/images/index/index_icon.png) 0 -165px;
                background-size: 833px 608px;
            }
        }
        .txt {
            float: right;
            width: 420px;
            b {
                font-size: 30px;
                color: #333;
                display: block;
                margin-bottom: 17px;
                text-align: left;
            }
            span {
                font-size: 26px;
                color: #666;
                line-height: 36px;
                text-align: justify;
                display: block;
            }
        }
        .slider-2 {
            i {
                width: 116px;
                background-position-x: -188px;
            }
        }
        .slider-3 {
            i {
                width: 114px;
                background-position-x: -369px;
            }
        }
        .slider-4 {
            i {
                width: 91px;
                background-position-x: -560px;
            }
        }
        .slider-5 {
            i {
                width: 95px;
                background-position-x: -738px;
            }
        }
    }
}

.b3 {
    height: 741px;
    background: url(/images/index/b3_bg.jpg) no-repeat center;
    background-size: cover;
    .content {
        position: relative;
    }
    .b3-box {
        width: 710px;
        height: 444px;
        border-radius: 10px;
        background-color: #fcfcfc;
        border: 2px solid #b1b1b1;
        margin-top: 90px;
        text-align: left;
        b {
            width: 600px;
            height: 64px;
            line-height: 64px;
            border-radius: 10px;
            font-size: 26px;
            margin: -29px auto 0;
            color: #fff;
            text-align: center;
            display: block;
            background-color: #e91222;
            -webkit-box-shadow: 1px 4px 18px rgba(233, 18, 34, .5); 
            -moz-box-shadow: 1px 4px 18px rgba(233, 18, 34, .5); 
            box-shadow: 1px 4px 18px rgba(233, 18, 34, .5);
        }
        ul {
            width: 490px;
            font-size: 0;
            margin: 45px 0 0 22px;
            li {
                width: 242px;
                display: inline-block;
                line-height: 84px;
                text-align: left;
                font-size: 26px;
                color: #333;
                i {
                    width: 10px;
                    height: 10px;
                    border-radius: 50%;
                    display: inline-block;
                    background-color: #e91222;
                    margin-right: 19px;
                    vertical-align: middle;
                }
            }
        }
    }
    i.i-img {
        width: 217px;
        height: 377px;
        display: inline-block;
        background: url(/images/index/b3_img.png) no-repeat center;
        background-size: contain;
        position: absolute;
        bottom: 0;
        right: 0;
    }
}

.b4 {
    background-color: #0a0f2b;
    padding: 67px 0 64px;
    h4 {
        color: #fff;
    }
    h5 {
        margin: 20px 0 70px;
        line-height: 30px;
        color: #fff;
    }
    .b4-swiper {
        position: relative;
        // height: 532px;
        .swiper-slide {
            width: 702px;
            height: 360px;
            border-radius: 10px;
            background-color: #fff;
            padding: 36px 35px 0;
            box-sizing: border-box;
            .top-span {
                font-size: 30px;
                color: #333;
                font-weight: bold;
                i {
                    width: 59px;
                    height: 53px;
                    display: inline-block;
                    background: url(/images/index/index_icon.png) 0 -398px no-repeat;
                    background-size: 833px 603px;
                    vertical-align: middle;
                    margin-right: 19px;
                }
            }
            p {
                font-size: 26px;
                line-height: 36px;
                color: #666;
                text-align: left;
                margin: 20px 0 0;
            }
        }
        .li-2 {
            .top-span i {
                width: 48px;
                background-position-x: -133px;
            }
        }
        .li-3 {
            .top-span i {
                width: 50px;
                background-position-x: -259px;
            }
        }
        .li-4 {
            .top-span i {
                width: 48px;
                background-position-x: -388px;
            }
        }
        .li-5 {
            .top-span i {
                width: 60px;
                background-position-x: -509px;
            }
        }
        .li-6 {
            .top-span i {
                background-position-x: -637px;
            }
        }
    }
}

.b5 {
    padding: 70px 0;
    background-color: #fff;
    .b5-box {
        margin-top: 60px;
        text-align: left;
        .b5-top {
            border-radius: 10px;
            overflow: hidden;
            background-color: #fff;
            .img-box {
                height: 265px;
                margin-bottom: 24px;
                img {
                    width: 100%;
                    height: 100%;
                }
            }
            .txt {
                width: 680px;
                margin: 0 auto;
                p {
                    font-size: 24px;
                    color: #666;
                    line-height: 36px;
                    margin-top: 22px;
                }
            }
        }
        span {
            display: block;
            i {
                vertical-align: middle;
                display: inline-block;
                background: url(/images/index/index_icon.png) 0 -566px no-repeat;
                background-size: 833px 603px;
            }
        }
        .title-span {
            font-size: 30px;
            line-height: 36px;
            color: #333;
            i {
                width: 37px;
                height: 37px;
                margin-right: 17px;
            }
        }
        .time-span {
            text-align: right;
            color: #666;
            font-size: 24px;
            margin: 25px 0 30px;
            i {
                width: 23px;
                height: 23px;
                background-position: -65px -573px;
                margin-right: 10px;
            }
        }
        ul {
            border-top: 1px solid #e3e3e3;
            li {
                display: block;
                padding: 30px 14px;
                box-sizing: border-box;
                border-bottom: 1px solid #e3e3e3;
                a {
                    width: 100%;
                    height: 100%;
                    display: block;
                }
                .title-span {
                    font-weight: bold;
                    line-height: 1.1;
                    overflow: hidden;
                    text-overflow:ellipsis;
                    white-space: nowrap;
                }
                p {
                    font-size: 24px;
                    color: #666;
                    line-height: 36px;
                    overflow : hidden;
                    text-overflow: ellipsis;
                    display: -webkit-box;
                    -webkit-line-clamp: 3;
                    -webkit-box-orient: vertical;
                }
            }
        }
        
    }
}
</style>

<style lang="scss">
.banner {
    .swiper-pagination-bullets {
        bottom: 50px;
        z-index: 20;
        .swiper-pagination-bullet {
            width: 46px;
            height: 6px;
            border-radius: 23px;
            background-color: #fff;
            margin: 0 7px;
        }
    }
}

.b2 {
    .swiper-pagination-bullets {
        margin-top: 65px;
        z-index: 20;
        .swiper-pagination-bullet {
            width: 20px;
            height: 20px;
            background-color: #dadada;
            margin: 0 10px;
            opacity: 1;
        }
        .swiper-pagination-bullet-active {
            background-color: #e91222;
        }
    }
}

.b4 {
    .swiper-pagination-bullets {
        position: absolute;
        bottom: 40px;
        z-index: 20;
        .swiper-pagination-bullet {
            width: 16px;
            height: 16px;
            background-color: #dadada;
            margin: 0 9px;
            opacity: 1;
        }
        .swiper-pagination-bullet-active {
            background-color: #e91222;
            width: 43px;
            border-radius: 8px;
        }
    }
}
</style>

