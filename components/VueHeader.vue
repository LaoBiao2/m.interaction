<template>
    <section>
        <div class="VueHeader">
            <div class="content clearfix">
                <div class="logo">
                    <nuxt-link to="/"><img src="/images/common/logo.png" alt=""></nuxt-link>
                </div>
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
                        <nuxt-link to="/">产品服务</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/">能力优势</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/">新闻中心</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link to="/">关于我们</nuxt-link>
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
                $(".VueHeader").toggleClass("up");
            });
            $(".sub-menu-bg").click(function () {
                $(".VueHeader").removeClass("up");
            });
            $(".sub-menu-bg").on('touchmove', function () {
                $(".VueHeader").removeClass("up");
            });
		},
        methods: {
        }
	};

</script>

<style lang="scss">
.VueHeader {
	width: 100%;
	height: 130px;
	display: block;
	position: fixed;
	top: 0;
	left: 0;
	z-index: 99;
	background-color: #0a0f2b;
    line-height: 130px;
    .logo {
        a {
            width: 100%;
            height: 100%;
            display: block;
            width: 232px;
            height: 70px;
            margin: 30px 0 30px 14px;
            float: left;
            img {
                width: 100%;
                height: 100%;
            }
        }
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
.VueHeader.up {
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

