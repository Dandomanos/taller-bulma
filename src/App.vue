<template>
  <div id="app" :class="{'show-grid':show}">
    <show-grid :show="show" @update="showGrid"></show-grid>
    <router-view></router-view>
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
html, body, * {
    box-sizing:border-box;
    margin:0;
    padding:0;  
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
