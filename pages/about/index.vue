<template>
    <section class="container">
        <div>
            <div class="banner">
                <div class="img-bg">
                    <img src="/images/about/banner.jpg" alt="">
                </div>
                <div class="content">
                    <div class="txt">
                        <h2>您的信任<br/>我的责任</h2>
                        <p>我们只提供最优质的服务</p>
                    </div>
                </div>
            </div>
            <div class="container-box">
                <div class="banner-bottom">
                    <div class="banner-swiper">
                        <div v-swiper:bannerSwiper="swiperOption">
                            <div class="swiper-wrapper">
                                <div class="li-1 swiper-slide">
                                    <i></i>
                                    <b>我们的愿景</b>
                                    <span>做中国最优秀的呼叫中心</span>
                                </div>
                                <div class="li-2 swiper-slide">
                                    <i></i>
                                    <b>我们的使命</b>
                                    <span>为沟通创造价值，提高客户满度</span>
                                </div>
                                <div class="li-3 swiper-slide">
                                    <i></i>
                                    <b>我们的价值理念</b>
                                    <span>追求卓越，让客户的客户更满意</span>
                                </div>
                                <div class="li-4 swiper-slide">
                                    <i></i>
                                    <b>我们的服务理念</b>
                                    <span>专业专注、用心服务</span>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-pagination"></div>
                        <div class="swiper-button-prev"></div>
                        <div class="swiper-button-next"></div>
                    </div>
                </div>
                <div class="box b1">
                    <div class="content">
                        <h4>公司简介</h4>
                        <div class="b1-box">
                            <div class="b1-content">
                                <p>广州互动商业服务有限公司拥有十年呼叫中心外包经验，目前拥有位于深圳、东莞、武汉、成都、宿迁五个呼叫运营中心。能为客户提供多语种服务，如普通话、粤语、 英语、日语以及韩语，与多家大型企业缔结了长期合作伙伴关系。  互动商务致力于为企业提供客户关系管理，提升企业与客户的沟通效率，为企业带来极致的用户体验和提高客户满意度，为沟通创造价值是互动商务的企业愿景。一直以来互动商务以服务 用户为导向，遵循创新、卓越、极致的服务理念，为用户提供便捷、可靠、稳定的客服管理服务，让用户享受高效沟通带来的美好体验。</p>
                                <p>过去，广域成深刻理解客户需求，帮助数百家企业解决了客户满意度困境，是企业盈利和成长的最佳合作伙伴。未来，广域成将继续依托优质的专业服务为客户带来最佳价值增值。</p>
                                <p>广域成呼叫外包服务是基于现代通信技术，主要为企业提供客服外包、业务流程外包、咨询培训和系统集成等四大类产品的专家级服务</p>
                                <p>广域成呼叫外包服务拥有电信级呼叫中心平台和电信网络资源，可为企业提供本地或远端的座席租赁服务。</p>
                                <p>广域成呼叫外包服务拥有专业的呼叫中心运营管理团队，为企业提供业务流程外包服务，帮助企业建立完善的客户服务标准和流程体系。</p>
                                <p>广域成呼叫外包服务将多年积累的呼叫中心运营经验和管理模式，通过咨询和培训服务的方式分享成功管理经验，为企业提供灵活丰富的呼叫中心顾问服务。</p>
                            </div>
                            <div class="show-btn"><p><span>查看更多</span><i></i></p></div>
                        </div>
                    </div>
                </div>
                <div class="box b2">
                    <h4>合作案例</h4>
                    <div class="b2-swiper">
                        <div v-swiper:b2Swiper="swiperOption2">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide" v-for="(b2Item, key) in b2Items" :key="key">
                                    <div class="li-box">
                                        <span class="span-img"><img :src="'/images/about/b2_img' + (key+1) + '.png'" alt=""><i></i></span>
                                        <div class="txt">
                                            <b>{{b2Item.title}}</b>
                                            <p v-html="b2Item.content"></p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="swiper-button-prev swiper-button-prev-b2"></div>
                            <div class="swiper-button-next swiper-button-next-b2"></div>
                        </div>
                    </div>
                </div>
                <div class="b3 box">
                    <h4>我们的荣誉</h4>
                    <div class="b3-swiper content">
                        <div v-swiper:b3Swiper="swiperOption3">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide" v-for="(b3Item, key) in b3Items" :key="key">
                                    <div class="slider" :class="'slider-' + (key+1)">
                                        <i class="i1"></i>
                                        <div class="txt">
                                            <p>{{b3Item.t1}}</p>
                                            <p>{{b3Item.t2}}</p>
                                            <p>{{b3Item.t3}}</p>
                                            <span class="span-line"></span>
                                            <b>{{b3Item.year}}</b>
                                        </div>
                                        <i class="i2"></i>
                                    </div>
                                </div>
                            </div>
                            <div class="swiper-pagination-b3"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            swiperOption: {
                pagination: '.swiper-pagination',
                centeredSlides: true,
                loop: true,
                nextButton: '.swiper-button-next',
                prevButton: '.swiper-button-prev',
            },
            swiperOption2: {
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
                nextButton: '.swiper-button-next-b2',
                prevButton: '.swiper-button-prev-b2',
            },
            b2Items: [
                {
                    title: '酷狗',
                    content: '互动商务为星河地产齐下物业业主提供物业咨询、报修、投诉等全程跟踪并记录，认真及时替业主排优解难，全面提高业主满意度！'
                },{
                    title: '深粮集团',
                    content: '互动商务为星河地产齐下物业业主提供物业咨询、报修、投诉等全程跟踪并记录，认真及时替业主排优解难，全面提高业主满意度！'
                },{
                    title: '星河物业',
                    content: '互动商务为星河地产齐下物业业主提供物业咨询、报修、投诉等全程跟踪并记录，认真及时替业主排优解难，全面提高业主满意度！'
                },{
                    title: '詹姆士手机',
                    content: '互动商务为星河地产齐下物业业主提供物业咨询、报修、投诉等全程跟踪并记录，认真及时替业主排优解难，全面提高业主满意度！'
                }
            ],
            swiperOption3: {
                slidesPerView: "auto",
                spaceBetween: 26,
                centeredSlides: true,
                loop: true,
                pagination: '.swiper-pagination-b3',
            },
            b3Items: [
                {
                    t1: '中国优秀外包客服联络中心',
                    t2: '金耳唛中国呼叫中心年度新锐',
                    t3: '',
                    year: '2012'
                },{
                    t1: '金耳唛中国最佳呼叫中心',
                    t2: '中国最佳外包呼叫中心',
                    t3: '',
                    year: '2013'
                },{
                    t1: '中国优秀外包客服联络中心',
                    t2: '中国最佳外包呼叫中心',
                    t3: '中国最佳联络中心客户服务代表',
                    year: '2014'
                },{
                    t1: '荣获移动运营商“优秀合作伙伴”',
                    t2: '客户服务代表奖突出贡献奖',
                    t3: '中国最佳外包联络中心奖（呼入服务）',
                    year: '2015'
                },{
                    t1: '中国优秀外包客服联络中心',
                    t2: '中国最佳外包呼叫中心',
                    t3: '中国最佳外包联络中心奖（呼入服务）',
                    year: '2016'
                },{
                    t1: '中国最佳联络中心管理人奖',
                    t2: '中国最佳外包联络中心奖（呼入服务）',
                    t3: '',
                    year: '2017'
                }
            ],
        }
    },
    mounted() {
        $(".b1 .show-btn span").click(function () {
            $(".b1-box").toggleClass("show");
            if ($(".b1 .show-btn span").text() == '查看更多') {
                $(".b1 .show-btn span").text('收起');
            } else {
                $(".b1 .show-btn span").text('查看更多');
            }
            // console.log( $(".b1 .show-btn span").text())
        })
    }
}
</script>

<style lang="scss" scoped>
.container-box {
    background-color: #f3f3f3;
}

.banner {
    width: 100%;
    height: 600px;
    position: relative;
    padding-top: 166px;
    .img-bg {
        width: 100%;
        height: 600px;
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
        margin-left: 28px;
        h2 {
            font-size: 52px;
            color: #fff;
            line-height: 72px;
            margin-bottom: 50px;
        }
        p {
            color: #fff;
            font-size: 30px;
        }
    }
}

.banner-bottom {
    padding: 106px 0 100px;
    background-color: #fff;
    position: relative;
    .banner-swiper {
        padding-bottom: 50px;
        .swiper-slide {
            text-align: center;
            i {
                display: block;
                width: 133px;
                height: 147px;
                margin: 0 auto;
                background: url(/images/about/about_icon.png) 0 0 no-repeat;
                background-size: 812px 647px;
            }
            b {
                font-size: 36px;
                color: #333;
                display: block;
                margin: 30px auto 24px;
            }
            span {
                font-size: 26px;
                color: #666;
            }
        }
        .li-2 {
            i {
                width: 123px;
                background-position-x: -226px;
            }
        }
        .li-3 {
            i {
                width: 135px;
                background-position-x: -442px;
            }
        }
        .li-4 {
            i {
                width: 163px;
                background-position-x: -649px;
            }
        }
        .swiper-button-prev,
        .swiper-button-next {
            width: 51px;
            height: 154px;
            background: url(/images/about/about_icon.png) -215px -493px no-repeat;
            background-size: 812px 647px;
            left: 0;
            margin-top: -60px;
        }
        .swiper-button-next {
            background-position-x: -355px;
            right: 0;
            left: auto;
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
    margin-top: 26px;
    padding: 70px 0 60px;
    background-color: #fff;
    position: relative;
    .b1-box {
        margin-top: 38px;
        p {
            line-height: 50px;
            font-size: 26px;
            color: #666;
            text-align: justify;
            display: none;
        }
        p:first-child {
            display: block;
        }
        .show-btn {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 360px;
            display: block;
            background: transparent; /* 一些不支持背景渐变的浏览器 */  
            background: -moz-linear-gradient(top, transparent 0%, #fff 100%);
            background: -webkit-gradient(linear, left top, left bottom, color-stop(0%,transparent), color-stop(100%,#fff));
            background: -webkit-linear-gradient(top, transparent 0%,#fff 100%);
            background: -o-linear-gradient(top, transparent 0%,#fff 100%);
            background: -ms-linear-gradient(top, transparent 0%,#fff 100%);
            background: linear-gradient(to bottom, transparent 0%,#fff 100%);
            p {
                position: absolute;
                bottom: 60px;
                left: 0;
                text-align: center;
                width: 100%;
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
    }
    .b1-box.show {
        p {
            display: block;
        }
        .show-btn {
            background: transparent;
            p {
                bottom: 20px;
                i {
                    background-position-y: -617px;
                }
            }
        }
    }
}

.b2 {
    .b2-swiper {
        position: relative;
        margin-top: 30px;
        .swiper-container {
            padding: 30px 20px;
            box-sizing: border-box;
        }
        .swiper-slide {
            width: 431px;
            height: 426px;
            opacity: 0;
            border-radius: 10px;
            overflow: hidden;
            background-color: #fff;
             -webkit-box-shadow: 1px 1px 30px rgba(0, 0, 0, .15); 
            -moz-box-shadow: 1px 1px 30px rgba(0, 0, 0, .15); 
            box-shadow: 1px 1px 30px rgba(0, 0, 0, .15);
            .li-box {
                .span-img {
                    height: 186px;
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
                        margin-bottom: 34px;
                    }
                    p {
                        font-size: 26px;
                        color: #999;
                        line-height: 36px;
                        margin-top: 32px;
                        text-align: justify;
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

.b3 {
    background-color: #fff;
    padding: 80px 0 110px;
    .b3-swiper {
        margin-top: 50px;
        position: relative;
        .swiper-container {
            // padding-bottom: 50px;
            .swiper-slide {
                width: 520px;
            }
        }
        .slider {
            position: relative;
            text-align: center;
            height: 166px;
            i {
                width: 72px;
                height: 166px;
                display: inline-block;
                background: url(/images/about/about_icon.png) 0 -299px;
                background-size: 812px 647px;
                position: absolute;
                top: 0;
            }
            .i1 {
                left: 0;
            }
            .i2 {
                right: 0;
                background-position-x: -603px;
            }
            .txt {
                width: 100%;
                position: absolute;
                bottom: 0;
                left: 0;
                b {
                    font-size: 36px;
                    color: #333;
                    display: block;
                    // margin-bottom: 17px;
                }
                p {
                    font-size: 26px;
                    color: #666;
                    line-height: 36px;
                    text-align: center;
                }
                span {
                    display: inline-block;
                    width: 70%;
                    height: 2px;
                    background-color: #979797;
                    margin: 10px 0;
                }
            }
            
        }
        .swiper-slide:nth-child(2n+1) .slider{
            i {
                background-position-x: -185px;
            }
            .i2 {
                background-position-x: -419px;
            }
        }
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
.banner-bottom {
    .swiper-pagination-bullets {
        width: 100%;
        margin-top: 50px;
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

.b3 {
    .swiper-pagination-bullets {
        margin-top: 65px;
        z-index: 20;
        .swiper-pagination-bullet {
            width: 20px;
            height: 20px;
            background-color: #e3e3e3;
            margin: 0 10px;
            opacity: 1;
        }
        .swiper-pagination-bullet-active {
            background-color: #adadad;
        }
    }
}
</style>

