<template>
    <div>
        <div :class="cont.title" :id="cont.title">
            <ul :class="cont.title + cl.ul + cl.bi">
                <li :class="cont.title + cl.ul + cl.bi + cl.it">
                    <div>
                        <h3>{{cont.title}}:</h3>
                        <ul>
                            <li><a :class="cont.phone.text" :href="cont.phone.href">{{cont.phone.text}}</a></li>
                            <li><a :class="cont.email.text" :href="cont.email.href">{{cont.email.text}}</a></li>
                        </ul>
                    </div>
                </li>
                <li :class="cont.title + cl.ul + cl.bi + cl.it">
                    <div>
                        <h3>{{mes.title}}:</h3>
                        <ul>
                            <li><a :class="mes.teleg.text" :href="mes.teleg.href">{{mes.teleg.text}}</a></li>
                            <li :class="dvf"><a :class="mes.vib.text" :href="mes.vib.href">{{mes.vib.text}}</a></li>
                            <li :class="dvf"><a :class="mes.sky.text" :href="mes.sky.href">{{mes.sky.text}}</a></li>
                        </ul>
                    </div>
                </li>

<!--         /////////////////////////////////////////       -->


                <li :class="cont.title + cl.ul + cl.bi + cl.it">
                    <div>
                        <h3 class="">Socials:</h3>
                        <ul>
                            <li><a :class="link.text" :href="link.href" target="_blank">{{link.text}}</a></li>
                            <li :class="dvf"><a class="facebook" href="https://www.facebook.com/alex.zhorov.77" target="_blank">Facebook</a></li>
                            <li :class="dvf"><a class="vk" href="https://vk.com/zhorovalex" target="_blank">VK</a></li>
                        </ul>
                    </div>
                </li>

<!--          //////////////////////////////////////////////      -->

                <li :class="cont.title + cl.ul + cl.bi + cl.it">
                    <div>
                        <h3 class="">Experience:</h3>
                        <ul>
                            <li><a class="git-lub" href="https://gitlab.com/z0r0v" target="_blank">GitLub</a></li>
                            <li><a class="git-hub" href="https://github.com/z0r0v" target="_blank">GitHub</a></li>
                            <li><a class="stackblitz" href="https://stackblitz.com/github/z0r0v/DZ" target="_blank">Stackblitz</a></li>
                            <li><a class="codepen" href="https://codepen.io/z0r0v/pens/public" target="_blank">Codepen</a></li>
                        </ul>
                    </div>

                </li>
            </ul>
        </div>
        <div class="copywriting"><p>zhorovalex © 2020</p></div>
    </div>
</template>

<script>
    export default {
        name: "FooterComponent",
        data(){
            return {
                cl: {
                    ul:"__ul",
                    bi:"--box-items",
                    it:"__item",
                    la:"__label",
                    label:"",
                    li:"",
                    dvf:"desktop-visible-flex",
                },
                cont: {
                    title: "contacts",
                    phone: {
                        text: "phone",
                        href:"tel:+375293767082",
                    },
                    email: {
                        text:"email",
                        href:"mailto:3767082@mail.ru"
                    },
                },
                mes:{
                    title:"mesengers",
                    teleg: {
                        text:"telegram",
                        href:"tg://resolve?domain=+375293767082",
                    },
                    vib: {
                        text:"viber",
                        href:"viber://chat?number=+375293767082",
                    },
                    sky: {
                        text:"skype",
                        href:"skype:zhorovalex?call",
                    }
                },
                ///////////////////////////////////

            }
        },
    }
</script>
<style lang="scss">
    @import "../../variables";
    .contacts {
        display: flex;
        justify-content: center;
        &__ul--box-items {
            width: 100%;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;

        &__item {
            width: calc(100% / 2);
            box-sizing: border-box;
            padding: 25px;
            display: flex;
            flex-direction: column;
            align-items: center;
            @include mq($from: tablet) {
                width: calc(100% / 4);
            }

            h3 {
                margin-bottom: 15px;
                font-size: 25px;
                color: $color-black;
                font-weight: 700;
                text-transform: capitalize;

            }
            a {
                all:unset;
                position: relative;
                padding-left: 30px;
                padding-bottom: 10px;
                display: block;
                cursor: pointer;
                text-transform: capitalize;
                &::before {
                    width: 20px;
                    height: 20px;
                    content: ".";
                    position: absolute;
                    left: 0px;
                    top: -19%;
                    transform: translate(50%);
                }
            }
            a:visited {
                color: $color-link-visited;
            }
            a:hover {
                color: $color-hover-link;
            }


        }
        }
    }
    .copywriting {
        border-top: 1px solid $color-grey-border;
        p {
            margin-top: 31px;
            text-align: center;
            font-weight: 700;
        }
    }

</style>