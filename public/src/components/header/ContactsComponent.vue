<template>
  <div class="contacts" >
    <a href="https://www.linkedin.com/in/alexzhorov/" target="_blank">
     <picture v-lazy-container="{ selector: 'img' }">
        <source media="(max-width: 768px)" srcset="@/assets/ico/icons8-linkedin.svg">
        <source srcset="@/assets/ico/icons8-linkedin.svg">
        <img data-src="@/assets/ico/icons8-linkedin.svg" alt="linked" />
    </picture>
    </a>
    <span class="contacts__text">My contact</span>
  </div>
</template>
<script>
export default {
  name: "ContactsComponent",
  data() {
    return {};
  },
};
</script>

<style lang="scss">
@import "../../variables";
.contacts {
display: none;
    @include mq($from: tablet) {
        display: flex;
    }

  a {
    display: flex;
  }
  img {
    width: 30px;
    height: 30px;
    margin-right: 7px;
    @include mq($from: tablet) {
      width: 48px;
      height: 48px;
    }
  }
  &__text {
    margin: auto 0;
    font-size: 14px;
    font-weight: bold;
    @include mq-add-breakpoint(mobileLar, 420px);
    @include mq($from: mobileLar) {
      display: none;
    }
  }
}
</style>
