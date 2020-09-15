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


 h1 ,h2, span, p, ul, li, a {
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
