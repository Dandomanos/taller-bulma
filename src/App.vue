<template>
  <div id="app" :class="{'show-grid':show}">
    <div class="hero is-fullheight">
        <header class="hero-head">Header</header>
        <div class="hero-body">
            <router-view class="is-overlay"></router-view>
        </div>
        <footer class="footer hero-foot">Footer</footer>
    </div>
    <show-grid :show="show" @update="showGrid"></show-grid>
  </div>
</template>

<script>
import ShowGrid from './components/ShowGrid'
export default {
    name: 'app',
    data() {
        return {
            show:false,
        }
    },
    methods: {
        showGrid(show) {
            this.show = show
        }
    },
    components: {
        ShowGrid
    }
}
</script>

<style lang="scss">
@import './scss/grid.scss';
@import '~bulma';
html, body {
    margin:0;
    padding:0;  
}
* {
    box-sizing:border-box;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin:0;
  padding:0;
  > img {
    margin-bottom:2rem;
    max-width:100%;
  }
}

</style>
