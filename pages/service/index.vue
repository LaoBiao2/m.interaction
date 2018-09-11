<template>
    <section class="container">
        <div>
            <div class="banner">
                <div class="img-bg">
                    <img src="/images/service/banner.jpg" alt="">
                </div>
                <div class="content">
                    <div class="txt">
                        <h2><span>互动商务</span><br/>专业客服外包</h2>
                        <p>现在选择互动商务，让您的<br/>每一位客户更满意</p>
                    </div>
                </div>
            </div>
            <div class="container-box">
                <div class="box b1">
                    <h4>我们能为你做什么</h4>
                    <div class="b1-swiper">
                        <div v-swiper:b1Swiper="swiperOption1">
                            <div class="swiper-wrapper">
                                <div class="li-1 swiper-slide">
                                    <i></i>
                                    <b>呼出服务</b>
                                    <span>呼出服务主要包括市场推广、电话回访、信息核实、市场调查、商业活动邀请、客户关怀、数据调研、运营商增值业务等。可根据客户的项目要求和项目特点，按照项目的完成时间设定服务周期。</span>
                                </div>
                                <div class="li-2 swiper-slide">
                                    <i></i>
                                    <b>客服外派</b>
                                    <span>互动商务人力派遣，专注为企业提供客服人力派遣、客服外包、驻场客服、短期客服招聘、快速组建客服团队。按人天、人月等灵活方式。涵盖各行业、各领域，为企业提供专业的客户服务。</span>
                                </div>
                                <div class="li-3 swiper-slide">
                                    <i></i>
                                    <b>数据录入</b>
                                    <span>为企业提供各种表单数据文字录入、档案录入、各种格式数据录入、各行业数据录入。可分为资料整理、扫描录入、图像处理、拼写检查等烦杂耗费人力的服务</span>
                                </div>
                                <div class="li-4 swiper-slide">
                                    <i></i>
                                    <b>增值业务</b>
                                    <span>通过电话对移动、联通、电信等运营平台的话费套餐、流量包等SP增值业务外呼年的移动运营商外呼经验，可有效减少客户投诉</span>
                                </div>
                                <div class="li-5 swiper-slide">
                                    <i></i>
                                    <b>客服外包</b>
                                    <span>互动商务高品质的呼入服务，互动商务信息的呼叫中心系统，它是一种基于ＣＴＩ技术、完整的综合信息服务系统，它能为用户提供多种服务。该系统包含了全面的呼叫中心的功能，并在各个部分进行系统性的创新。</span>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-button-prev"></div>
                        <div class="swiper-button-next"></div>
                    </div>
                </div>
                <div class="box b2">
                    <h4>合作案例</h4>
                    <div class="b2-box">
                        <ul class="clearfix">
                            <li class="li-1">
                                <i></i>
                                <span>① 前期沟通</span>
                            </li>
                            <li class="li-2">
                                <i></i>
                                <span>② 确认合作</span>
                            </li>
                            <li class="li-3">
                                <i></i>
                                <span>③ 岗前培训</span>
                            </li>
                            <li class="li-4">
                                <i></i>
                                <span>④ 上线服务</span>
                            </li>
                            <li class="li-5">
                                <i></i>
                                <span>⑤ 定期质检</span>
                            </li>
                            <li class="li-6">
                                <i></i>
                                <span>⑥ 数据反馈</span>
                            </li>
                        </ul>
                        <i class="flow-i i1"></i>
                        <i class="flow-i i2"></i>
                        <i class="flow-i i3"></i>
                        <i class="flow-i i4"></i>
                        <i class="flow-i i5"></i>
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
            swiperOption1: {
                effect : 'coverflow',
                slidesPerView: "auto",
                centeredSlides: true,
                loop: true,
                coverflow: {
                    rotate: 0,
                    stretch: 28,
                    depth: 60,
                    modifier: 3,
                    slideShadows : false
                },
                nextButton: '.swiper-button-next',
                prevButton: '.swiper-button-prev',
            },
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
            span {
                color: #e91222;
            }
        }
        p {
            color: #fff;
            font-size: 30px;
            line-height: 48px;
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
    padding: 106px 0 20px;
    background-color: #fff;
    position: relative;
    .b1-swiper {
        // padding-top: 60px;
        .swiper-container {
            padding: 60px 0;
        }
        .swiper-slide {
            width: 612px;
            // height: 427px;
            border-radius: 10px;
            overflow: hidden;
            background-color: #fff;
             -webkit-box-shadow: 1px 1px 50px rgba(0, 0, 0, .15); 
            -moz-box-shadow: 1px 1px 50px rgba(0, 0, 0, .15); 
            box-shadow: 1px 1px 50px rgba(0, 0, 0, .15);
            text-align: center;
            padding: 32px 60px;
            box-sizing: border-box;
            opacity: 0;
            i {
                display: block;
                width: 100px;
                height: 93px;
                margin: 0 auto;
                background: url(/images/service/service_icon.png) 0 0 no-repeat;
                background-size: 953px 525px;
            }
            b {
                font-size: 30px;
                color: #666;
                display: block;
                margin: 18px auto 44px;
            }
            span {
                font-size: 26px;
                color: #999;
                line-height: 36px;
                text-align: justify;
                display: block;
            }
        }
        .li-2 {
            i {
                width: 94px;
                background-position-x: -174px;
            }
        }
        .li-3 {
            i {
                width: 93px;
                background-position-x: -346px;
            }
        }
        .li-4 {
            i {
                width: 101px;
                background-position-x: -513px;
            }
        }
        .li-5 {
            i {
                width: 110px;
                background-position-x: -679px;
            }
        }
        .swiper-slide-next,
        .swiper-slide-prev {
            opacity: .5;
        }
        .swiper-slide-active {
            opacity: 1;
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

.b2 {
    margin-top: 26px;
    background-color: #fff;
    padding: 66px 0 0;
    .b2-box {
        position: relative;
        margin-top: 56px;
        ul {
            li {
                float: left;
                width: 50%;
                height: 160px;
                margin-bottom: 125px;
                i {
                    width: 84px;
                    height: 96px;
                    display: block;
                    margin: 0 auto 29px;
                    background: url(/images/service/service_icon.png) 0 -193px no-repeat;
                    background-size: 953px 525px;
                }
                span {
                    font-size: 30px;
                    color: #666;
                }
            }
            .li-2 {
                i {
                    width: 84px;
                    background-position-x: -171px;
                }
            }
            .li-3 {
                i {
                    width: 100px;
                    background-position-x: -334px;
                }
            }
            .li-4 {
                i {
                    width: 95px;
                    background-position-x: -508px;
                }
            }
            .li-5 {
                i {
                    width: 124px;
                    background-position-x: -665px;
                }
            }
            .li-6 {
                i {
                    width: 110px;
                    background-position-x: -843px;
                }
            }
        }
        .flow-i {
            width: 166px;
            height: 10px;
            display: inline-block;
            background: url(/images/service/service_icon.png) 0 -437px no-repeat;
            background-size: 953px 525px;
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
        }
        .i2,.i4 {
            width: 10px;
            height: 166px;
            background-position: -548px -359px;
        }
        .i1 {
            top: 65px;
        }
        .i2 {
            top: 92px;
            margin-left: 190px;
        }
        .i3 {
            top: 342px;
            background-position-x: -235px;
        }
        .i4 {
            top: 373px;
            margin-left: -190px;
        }
        .i5 {
            top: 617px;
        }
    }
}

</style>
