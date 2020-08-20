<template>
  <header>
    <div class="header-box">
      <LogoComponent></LogoComponent>
      <SearcheComponent></SearcheComponent>
      <ContactsComponent></ContactsComponent>
    </div>
   <AfterHeaderComponent></AfterHeaderComponent>
  </header>
 
</template>

<script>
import LogoComponent from "@/components/LogoComponent.vue";
import SearcheComponent from "@/components/SearcheComponent.vue";
import ContactsComponent from "@/components/ContactsComponent.vue";
import AfterHeaderComponent from "@/components/AfterHeaderComponent.vue";

export default {
  name: "Home",
  components: {
    LogoComponent,
    SearcheComponent,
    ContactsComponent,
    AfterHeaderComponent,
  },
};
</script>
<style lang="scss">
@import "../_variables.scss";
.header-box {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
</style>
