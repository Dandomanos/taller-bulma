<template>
  <div id="app" :class="{'show-grid':show}">
    <div class="hero is-fullheight">
        <header class="hero-head">
            <nav class="navbar is-primary" role="navigation">
                <div class="navbar-brand">
                    <router-link to="hello" class="navbar-item">
                        <img src="./assets/bulma-logo.png" alt="" width="150">
                    </router-link>
                    <button class="button navbar-burger" @click="toggleActive" :class="{'is-active':menuActive}">
                        <span></span>
                        <span></span>
                        <span></span>
                    </button>
                </div>
                <div class="navbar-menu" id="navMenu" :class="{'is-active':menuActive}">
                    <div class="navbar-start">
                        <router-link class="navbar-item" to="news">News</router-link>
                        <router-link class="navbar-item" to="blog">Blog</router-link>
                        <div class="navbar-item has-dropdown is-hoverable">
                            <div class="navbar-link">External Links</div>
                            <div class="navbar-dropdown">
                                <a href="http://www.google.com" target="_blank" class="navbar-item">
                                    Google
                                </a>
                                <hr class="navbar-divider">
                                <a href="http://www.bulma.iom" target="_blank" class="navbar-item">
                                    Bulma
                                </a>
                            </div>
                        </div>
                    </div>
                    <div class="navbar-end">
                        <div class="navbar-item">
                            <input type="email" class="input" placeholder="Email">
                        </div>
                        <div class="navbar-item">
                            <input type="password" class="input" placeholder="Contraseña">
                        </div>
                        <div class="navbar-item">
                            <button class="button is-info">Entrar</button>
                        </div>
                    </div>
                </div>
            </nav>
        </header>
        <div class="hero-body">
            <router-view class="container"></router-view>
        </div>
        <footer class="footer hero-foot">
            <nav class="level">
                <div class="level-item has-text-centered">
                    <div>Oficial<br><a href="">Link</a></div>
                </div>
                <div class="level-item has-text-centered">
                    <div><a href="">Link2</a><br><small><a href="">Ver +</a></small></div>
                </div>
                <div class="level-item has-text-centered">
                    <div><a href="">Link3</a></div>
                </div>
            </nav>
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
            menuActive:false
        }
    },
    methods: {
        showGrid(show) {
            this.show = show
        },
        toggleActive() {
            this.menuActive = !this.menuActive
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
