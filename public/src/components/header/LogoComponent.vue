<template>
  <div class="logo-box">
    <picture v-lazy-container="{ selector: 'img' }">
      <source media="(max-width: 768px)" srcset="@/assets/ico/ubuntu.svg">
      <source srcset="@/assets/ico/ubuntu.svg">
      <img data-src="@/assets/ico/ubuntu.svg" alt="Ubuntu-logo">
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
  @import '../../variables';
.logo-box {
    display: flex;
    align-items: center;
    picture img {
      width: 30px;
      margin-right: 7px;
      @include mq($from: tablet){
        width: 50px;
         margin-right: 15px;
      }
    }
    &__text {
      h1,h2 {
        font-size: 14px;
        font-weight: bold;
      }
        h2 {
            display: none;
            @include mq($from: tablet) {
                display: block;
            }
        }

    }
}
</style>
