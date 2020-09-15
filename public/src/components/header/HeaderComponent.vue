<template>
    <header>
        <div class="header-box">
            <LogoComponent></LogoComponent>
            <SearcheComponent></SearcheComponent>
            <ContactsComponent></ContactsComponent>
        </div>
    </header>
</template>

<script>
    import LogoComponent from "@/components/header/LogoComponent";
    import SearcheComponent from "@/components/header/SearcheComponent";
    import ContactsComponent from "@/components/header/ContactsComponent";


    export default {
        name: "Header",
        components: {
            LogoComponent,
            SearcheComponent,
            ContactsComponent,
        },
    };
</script>
<style lang="scss">
    @import "../../variables";
    .header-box {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
</style>
