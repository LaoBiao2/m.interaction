<template>
    <section>
        <div class="NewsHeader">
            <div class="content clearfix">
                <div class="last-btn">
                    <nuxt-link to="/"><i></i></nuxt-link>
                </div>
                <b>新闻中心</b>
                <div class="menu-btn">
                    <i></i>
                </div>
            </div>
            <div class="sub-menu">
                <ul>
                    <li>
                        <nuxt-link to="/">首页</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/service">产品服务</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/advantage">能力优势</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/news">新闻中心</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/about">关于我们</nuxt-link>
                    </li>
                </ul>
            </div>
            <div class="sub-menu-bg"></div>
        </div>
    </section>
</template>

<script>
	export default {
        data(){
            return {
            }
        },
		mounted() {
            $(".menu-btn i").click(function () {
                $(".NewsHeader").toggleClass("up");
            });
            $(".sub-menu-bg").click(function () {
                $(".NewsHeader").removeClass("up");
            });
            $(".sub-menu-bg").on('touchmove', function () {
                $(".NewsHeader").removeClass("up");
            });
		},
        methods: {
        }
	};

</script>

<style lang="scss">
.NewsHeader {
	width: 100%;
	height: 130px;
	display: block;
	position: fixed;
	top: 0;
	left: 0;
	z-index: 99;
	background-color: #0a0f2b;
    line-height: 130px;
    .last-btn {
        display: inline-block;
        a {
            display: inline-block;
            i {
                width: 21px;
                height: 40px;
                display: inline-block;
                margin: 46px 0 44px 12px;
                background: url(/images/news/menu_btn.png) 0 0 no-repeat;
                background-size: 192px 40px;
            }
        }
    }
    b {
        position: absolute;
        top: 0;
        left: 50%;
        transform: translateX(-50%);
        font-size: 40px;
        line-height: 130px;
        color: #fff;
    }
	.menu-btn {
        float: right;
        position: relative;
        i {
            width: 50px;
            height: 42px;
            display: inline-block;
            background: url(/images/common/menu_btn.png) 0 0 no-repeat;
            background-size: 141px 40px;
            margin: 45px 20px 45px 0;
        }
    }
    .sub-menu {
        width: 375px;
        height: 100%;
        position: fixed;
        top: 130px;
        right: 0;
        z-index: 99;
        transform: translateX(100%);
        transition: all .3s;
        ul {
            width: 375px;
            height: 100%;
            overflow: scroll;
            position: absolute;
            right: 0;
            top: 0;
            z-index: 100;
            padding: 34px 0 130px;
            background-color: #0a0f2b;
            li {
                width: 340px;
                height: 128px;
                display: block;
                margin: 0 auto;
                border-bottom: 1px solid #484e70;
                a {
                    font-size: 30px;
                    color: #fff;
                    display: block;
                    line-height: 128px;
                    padding-left: 20px;
                }
            }
        }
    }
    .sub-menu-bg {
        width: 750px;
        height: 100%;
        position: fixed;
        top: 130px;
        right: 0;
        z-index: 98;
        background-color: rgba($color: #000, $alpha: .3);
        display: none;
    }
}
.NewsHeader.up {
    border-bottom: 1px solid #484e70;
    .menu-btn {
        i {
            width: 37px;
            background-position-x: -104px;
            margin-right: 40px;
        }
    }
    .sub-menu {
        transform: translateX(0);
    }
    .sub-menu-bg {
        display: block;
    }
}

</style>

