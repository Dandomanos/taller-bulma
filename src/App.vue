<template>
  <div id="app" :class="{'show-grid':show}">
    <div class="hero is-fullheight">
        <header class="hero-head">
            <nav class="level">
                <div class="level-left">
                    <div class="level-item">
                        <a href="">
                            <img src="./assets/bulma-logo.png" alt="" width="150">
                        </a>
                    </div>
                    <div class="level-item">
                        <a href="">
                            Link
                        </a>
                    </div>
                    <div class="level-item">
                        <a href="">
                            Link
                        </a>
                    </div>
                </div>
                <div class="level-right">
                    <div class="level-item">
                        <input type="email" class="input" placeholder="Email">
                    </div>
                    <div class="level-item">
                        <input type="password" class="input" placeholder="Contraseña">
                    </div>
                    <div class="level-item">
                        <button class="button">
                            Entrar
                        </button>
                    </div>
                </div>
            </nav>
        </header>
        <div class="hero-body">
            <router-view class="container"></router-view>
        </div>
        <footer class="footer hero-foot">
        </footer>
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
.container {
    max-width:100%;
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
