<template>
    <div class="big-static-img-component">
        <figure>
            <picture v-lazy-container="{ selector: 'img' }">
                <source media="(max-width: 768px)" srcset="@/assets/img/bg1.jpg">
                <source srcset="@/assets/img/bg1.jpg">
                <img data-src="@/assets/img/bg1.jpg" alt="html">
            </picture>
        </figure>
    </div>
</template>

<script>
    export default {
        name: "BigStaticImgComponent",
    }
</script>

<style lang="scss">
    @import "../../variables";
    .big-static-img-component {
        figure {
            height: 100%;
            width: 100%;
            max-height: 500px;
            overflow: hidden;
            picture {
                display: flex;
                justify-content: center;
                align-items: center;
                align-content: center;
            }
            picture img {
                position: relative;
                height: 100%;
                top: -141px;
                box-shadow: 1000px 0 0 0 black, -1000px 0 0 0 black,;
            }
        }
    }
</style>