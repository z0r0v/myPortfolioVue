<template>
  <div class="logo-box">
    <picture>
      <source media="(max-width: 768px)" srcset="@/assets/ico/ubuntu.svg">
      <source srcset="@/assets/ico/ubuntu.svg">
      <img src="@/assets/ico/ubuntu.svg" alt="Ubuntu-logo">
    </picture>
    <div class="logo-box__text">
      <h1>{{alexName}}</h1>
      <h2>{{qualification}}</h2>
    </div>
  </div>
</template>
<script>
export default {
  name: 'LogoComponent',
  data() {
    return {
      alexName: 'Alex Zhorov',
      qualification: 'Front-End Developer',
    }
  }
}
</script>
<style lang="scss">
.logo-box {
    display: flex;
    picture img {
      width: 50px;
    }
}
</style>
