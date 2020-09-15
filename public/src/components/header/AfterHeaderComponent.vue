<template>
    <div class="after-header">
        <a href="#">
            <picture v-lazy-container="{ selector: 'img' }">
                <source media="(max-width: 768px)" srcset="@/assets/img/html.png">
                <source srcset="@/assets/img/html.png">
                <img data-src="@/assets/img/html.png" alt="html">
            </picture>
            <span v-on:click="returnLink(html.ico)">
     {{html}}
    </span>
        </a>
        <a href="#">
            <picture v-lazy-container="{ selector: 'img' }">
                <source media="(max-width: 768px)" srcset="@/assets/img/css.png">
                <source srcset="@/assets/img/css.png">
                <img data-src="@/assets/img/css.png" alt="css">
            </picture>
            <span>
      {{css}}
    </span>
        </a>
        <a href="#">
            <picture v-lazy-container="{ selector: 'img' }">
                <source media="(max-width: 768px)" srcset="@/assets/img/js.png">
                <source srcset="@/assets/img/js.png">
                <img data-src="@/assets/img/js.png" alt="js">
            </picture>
            <span>
      {{js}}
    </span>
        </a>
    </div>
</template>
<script>
    export default {
        name: "AfterHeaderComponent",
        data() {
            return {
                html: "Html",
                css: "Css",
                js: "JavaScript",
            };
        }
    };


</script>

<style lang="scss">
    @import "../../variables";
    .after-header {
        height: 35px;
        padding: 0 10px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: $color-black;
        @include mq($from: tablet) {
            height: 63px;
        }
        a {
            width: calc(100% / 3);
            display: flex;
            align-items: center;
            justify-content: center;
            color: $color-white;
        span {
            font-size: 12px;
            @include mq($from: desktop) {
                font-size:unset;
            }

        }
            &:hover {
                border: 1px solid $color-white;
                margin-left: -1px;
                margin-right: -1px;
            }
            picture {
                padding: 9px;
                margin-top: 3px;
                display: none;
            }
            picture img {
                width: 20px;
                height: 20px;
            }
            @include mq($from: tablet) {
                picture {
                    display: block;
                }
            }
        }
    }
</style>
