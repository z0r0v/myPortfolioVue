<template>
    <div class="content">
        <HeaderComponent></HeaderComponent>
        <AfterHeaderComponent></AfterHeaderComponent>
        <section>
            <SitesInfoComponent></SitesInfoComponent>
            <BigStaticImgComponent></BigStaticImgComponent>
            <CertificateComponent></CertificateComponent>
        </section>
        <footer>
    <FooterComponent></FooterComponent>
            </footer>
    </div>
</template>
<script>
    // @ is an alias to /src
    import HeaderComponent from '@/components/header/HeaderComponent';
    import BigStaticImgComponent from '@/components/section/BigStaticImgComponent';
    import AfterHeaderComponent from "@/components/header/AfterHeaderComponent";
    import SitesInfoComponent from "@/components/section/SitesInfoComponent";
    import FooterComponent from "@/components/footer/FooterComponent";
    import CertificateComponent from "@/components/section/CertificateComponent";

    export default {
        name: 'Home',
        components: {
            HeaderComponent,
            BigStaticImgComponent,
            AfterHeaderComponent,
            SitesInfoComponent,
            FooterComponent,
            CertificateComponent,
        }
    }
</script>
<style lang="scss">
    @import "../variables";
    header {
        margin: 5px 10px;
        padding: 5px 10px;
        @include mq($from: tablet){
            margin: 20px 50px;
            padding: 10px 20px;
        }
    }
    section {
        padding: 0;
        @include mq($from: tablet) {
            padding: 0 20px;
        }
    }
    footer {
        margin: 20px 10px;
        padding: 30px 0;
        border-top: 1px solid $color-grey-border;
    }
</style>

