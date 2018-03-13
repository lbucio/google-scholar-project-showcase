<template>
  <div id="app">
    <app-header></app-header>
    <main>
      <router-view></router-view>
    </main>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader';

export default {
  name: 'app',

  components: {
    AppHeader,
  },

};
</script>

<style>
html, body {
  height: 100%;
  width: 100%;
}

html {
  font-family: -apple-system, BlinkMacSystemFont,
    "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Cantarell",
    "Fira Sans", "Droid Sans", "Helvetica Neue",
    sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  -webkit-tap-highlight-color: rgba(0,0,0,0);
}

body {
  margin: 0;
  background: #f2f5f9;
  overflow-y: scroll;
}

*, *::before, *::after {
  box-sizing: border-box;
}

#app {
  height: 100%;
  color: #2c3e50;
}

#app > div {
  height: 100%;
  width: 100%;
  position: relative;
  padding: 0;
  margin: 0;
  min-width: 0;
  min-height: 0;

  display: flex;
  flex-direction: column;
  flex-basis: auto;
  flex-shrink: 0;
  align-items: stretch;
}

main {
  text-align: center;
  /* margin-top: 20px; */
  overflow-y: scroll; /* has to be scroll, not auto */
  -webkit-overflow-scrolling: touch;
  width: 100%;
  position: relative;
  padding: 0;
  margin: 0;
  min-width: 0;
  min-height: 0;

  display: flex;
  flex-direction: column;
  flex-basis: auto;
  flex-shrink: 0;
  align-items: stretch;
  flex-grow: 1!important;
}


h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #35495E;
}
</style>
