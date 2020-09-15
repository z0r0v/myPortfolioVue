<template>
    <div class="CertificateComponent">
        <figure>
            <picture v-lazy-container="{ selector: 'img' }">
                <source media="(max-width: 768px)" srcset="@/assets/img/vue.png">
                <source srcset="@/assets/img/vue.png">
                <img data-src="@/assets/img/vue.png" alt="html">
            </picture>
        </figure>
        <h2>{{h2}}</h2>
        <p>{{text}}</p>
    </div>
</template>

<script>
    export default {
        name: "CertificateComponent",
        data(){
            return {
                text:"Educational Center of Hi-Tech Park, Web application development with JavaScript. I am very proud\n" +
                    "            of myself having received this certificate. It was very difficult, but I did it.",
                h2: "Educational Center of Hi-Tech Park",
            }
        }
    }
</script>

<style scoped>

</style>