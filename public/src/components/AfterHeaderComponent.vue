<template>
  <div class="after-header">
   <a href="">1</a>
   <a href="">2</a>
   <a href="">3</a>
  </div>
</template>
<script>
export default {
  name: "AfterHeaderComponent",
  data() {
    return {

    };
  },
};
</script>

<style lang="scss">
@import "../_variables.scss";
.after-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 63px;
  margin-top: 20px;
  background-color: black;
  box-shadow: none;
  @include mq($from: tablet){
       box-shadow: 50px 0 0 0 black, -50px 0 0 0 black;
  }

  a {
    color: white;
  }
}
</style>
