<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
  @import "_variables.scss";
  @import 'defalut-css.scss';
 body {
   margin: 5px 10px;
   padding: 5px 10px;
   @include mq($from: tablet){
        margin: 20px 50px;
        padding: 10px 20px;
   }
   
 }
 h1 ,h2, span, p {
    font: normal small-caps 18px/18px Prompt, sans-serif;
 }
#app {
  

}

#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
