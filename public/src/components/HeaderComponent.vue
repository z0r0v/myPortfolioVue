<template>
<header>
    <LogoComponent></LogoComponent>
    <SearcheComponent></SearcheComponent>
    <ContactsComponent></ContactsComponent>
</header>

</template>

<script>

import LogoComponent from '@/components/LogoComponent.vue'
import SearcheComponent from '@/components/SearcheComponent.vue'
import ContactsComponent from '@/components/ContactsComponent.vue'


export default {
  name: 'Home',
  components: {
    LogoComponent,
    SearcheComponent,
    ContactsComponent,
  }
}
</script>
<style lang="scss">
header {
  display: flex;
  justify-content: space-between;
}
</style>