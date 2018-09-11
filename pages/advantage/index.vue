<template>
    <section class="container">
        <div>
            <div class="banner">
                <div class="img-bg">
                    <img src="/images/advantage/banner.jpg" alt="">
                </div>
                <div class="content">
                    <div class="txt">
                        <h2>因为选择<br/>所以信任</h2>
                        <p>互动商务助力企业完善客户<br/>关系管理</p>
                    </div>
                </div>
            </div>
            <div class="container-box">
                <div class="box b1">
                    <h4>能力与优势</h4>
                    <div class="b1-swiper">
                        <div v-swiper:b1Swiper="swiperOption1">
                            <div class="swiper-wrapper">
                                <div class="li-1 swiper-slide">
                                    <i></i>
                                    <b>规模</b>
                                    <span>四大客服基地千人<br>团队遍及全国</span>
                                </div>
                                <div class="li-2 swiper-slide">
                                    <i></i>
                                    <b>经验</b>
                                    <span>服务千万商家聚焦<br>众多知名品牌</span>
                                </div>
                                <div class="li-3 swiper-slide">
                                    <i></i>
                                    <b>全面</b>
                                    <span>业务涵盖客服、管理<br>培训等多个维度</span>
                                </div>
                                <div class="li-4 swiper-slide">
                                    <i></i>
                                    <b>专业</b>
                                    <span>ISO质量管理体系认证<br>多年获得阿里官方荣誉</span>
                                </div>
                                <div class="li-5 swiper-slide">
                                    <i></i>
                                    <b>管理</b>
                                    <span>全面实现线上绩效考核<br>真正做到数据化管理</span>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-pagination"></div>
                        <div class="swiper-button-prev"></div>
                        <div class="swiper-button-next"></div>
                    </div>
                </div>
                <div class="box b2">
                    <h4><span>选择互动商务 </span> 客服外包的理由</h4>
                    <div class="b2-swiper">
                        <div v-swiper:b2Swiper="swiperOption2">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide" v-for="(b2Item, key) in b2Items" :key="key">
                                    <div class="li-box">
                                        <span class="span-img"><img :src="'/images/advantage/b2_img' + (key+1) + '.png'" alt=""><i></i></span>
                                        <div class="txt">
                                            <p>{{b2Item}}</p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="swiper-pagination-b2"></div>
                        </div>
                    </div>
                </div>
                <div class="b3 box">
                    <h4>服务时间和管理模式</h4>
                    <ul>
                        <li class="li-1"><i></i>白班</li>
                        <li class="li-2"><i></i>晚班</li>
                        <li class="li-3"><i></i>24小时</li>
                        <li class="li-4"><i></i>临时</li>
                        <li class="li-5"><i></i>定制</li>
                    </ul>
                    <div class="b3-swiper">
                        <div v-swiper:b3Swiper="swiperOption3">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide" v-for="(b3Item, key) in b3Items" :key="key">
                                    <div class="slider">
                                        <b>{{b3Item.title}}</b>
                                        <span>{{b3Item.content}}</span>
                                    </div>
                                </div>
                            </div>
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
            swiperOption1: {
                pagination: '.swiper-pagination',
                centeredSlides: true,
                loop: true,
                nextButton: '.swiper-button-next',
                prevButton: '.swiper-button-prev',
            },
            swiperOption2: {
                pagination: '.swiper-pagination-b2',
                effect : 'coverflow',
                slidesPerView: "auto",
                centeredSlides: true,
                coverflow: {
                    rotate: 0,
                    stretch: 40,
                    depth: 60,
                    modifier: 3,
                    slideShadows : false
                },
                loop: true,
            },
            b2Items: [
                '费用大大低于自己雇 佣客服无需为空闲 客服支付工资超高 性价比',
                '全天24小时在线，全年无休让企业省时省力更省心',
                '专业客服团队，管理经验丰富不定期展开客服技能培训，完善的KPI考核',
                '客服骨干都拥有五年客服经验，带领团队更好的提升产品转化率'
            ],
            swiperOption3: {
                slidesPerView: "auto",
                spaceBetween: 25,
                centeredSlides: true,
                loop: true,
            },
            b3Items: [
                {
                    title: '标准化管理',
                    content: '内部质量管理部门和组长主管每周抽调客服服务人员的聊天记录，并被照标准进行评估',
                },{
                    title: '项目激励',
                    content: '每个项目自定义KPI，充分激励成员的积极性，同时每月对每个项目进行考核',
                },{
                    title: '软件监控',
                    content: '使用相对应的软件对客服人员，进行数据化监控和管理',
                },{
                    title: '定期研讨培训',
                    content: '定期展开话术讨论，添加问题库，定期培训销售技巧，强化客服销售能力',
                }
            ],
        }
    },
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
    padding: 106px 0 100px;
    background-color: #fff;
    position: relative;
    .b1-swiper {
        padding-bottom: 50px;
        margin-top: 50px;
        .swiper-slide {
            text-align: center;
            i {
                display: block;
                width: 129px;
                height: 129px;
                margin: 0 auto;
                background: url(/images/advantage/advantage_icon.png) 0 0 no-repeat;
                background-size: 1012px 336px;
            }
            b {
                font-size: 30px;
                color: #333;
                display: block;
                margin: 36px auto 15px;
            }
            span {
                font-size: 26px;
                line-height: 30px;
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
            background: url(/images/advantage/advantage_icon.png) -313px -181px no-repeat;
            background-size: 1012px 336px;
            left: 0;
            margin-top: -60px;
        }
        .swiper-button-next {
            background-position-x: -488px;
            right: 0;
            left: auto;
        }
    }
}

.b2 {
    background-color: #242841;
    h4 {
        color: #fff;
        span {
            font-weight: normal;
        }
    }
    .b2-swiper {
        position: relative;
        margin-top: 30px;
        .swiper-container {
            padding: 30px 20px;
            box-sizing: border-box;
        }
        .swiper-slide {
            width: 444px;
            height: 412px;
            opacity: 0;
            border-radius: 10px;
            overflow: hidden;
            background-color: #fff;
             -webkit-box-shadow: 1px 1px 30px rgba(0, 0, 0, .15); 
            -moz-box-shadow: 1px 1px 30px rgba(0, 0, 0, .15); 
            box-shadow: 1px 1px 30px rgba(0, 0, 0, .15);
            .li-box {
                .span-img {
                    height: 164px;
                    margin-bottom: 20px;
                    display: block;
                    img {
                        width: 100%;
                        height: 100%;
                    }
                }
                .txt {
                    width: 366px;
                    margin: 0 auto;
                    p {
                        font-size: 26px;
                        color: #8d8c8c;
                        line-height: 60px;
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
    padding: 80px 0 120px;
    ul {
        margin-top: 57px;
        height: 80px;
        border: 2px solid #ebebeb;
        border-radius: 40px;
        li {
            width: 20%;
            line-height: 80px;
            text-align: center;
            i {
                width: 29px;
                height: 28px;
                margin-right: 15px;
                display: inline-block;
                vertical-align: middle;
                background: url(/images/advantage/advantage_icon.png) 0 -308px;
                background-size: 1012px 336px;
            }
        }
        .li-2 {
            i {
                width: 22px;
                background-position-x: -60px;
            }
        }
        .li-3 {
            i {
                width: 23px;
                background-position-x: -117px;
            }
        }
        .li-4 {
            i {
                width: 24px;
                background-position-x: -173px;
            }
        }
        .li-5 {
            i {
                width: 27px;
                background-position-x: -228px;
            }
        }
    }
    .b3-swiper {
        margin-top: 70px;
        position: relative;
        .swiper-container {
            // padding-bottom: 50px;
            .swiper-slide {
                width: 550px;
            }
        }
        .slider {
            position: relative;
            text-align: center;
            height: 225px;
            padding: 30px 40px 32px;
            box-sizing: border-box;
            border-radius: 10px;
            border: 2px solid #ced2df;
                b {
                    font-size: 30px;
                    color: #333;
                    display: block;
                    margin-bottom: 34px;
                }
                span {
                    font-size: 26px;
                    line-height: 36px;
                    display: inline-block;
                    color: #999;
                    text-align: justify;
                }
        }
    }
}
</style>

<style lang="scss">
.b1 {
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

.b2 {
    .swiper-pagination-bullets {
        margin-top: 70px;
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

