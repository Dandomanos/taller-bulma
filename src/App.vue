<template>
  <div id="app" :class="{'show-grid':show}">
    <div class="hero is-fullheight">
        <header class="hero-head">
            <nav class="navbar is-primary">
                <div class="hero">
                    <div class="hero-body">
                        <div class="container has-text-centered">
                            <div class="level">
                                <div class="level-item">
                                    <router-link to="home" class="button is-link is-primary ">
                                        Home
                                    </router-link>
                                </div>
                                <div class="level-item">
                                    <router-link to="news" class="button is-link is-primary">
                                        News
                                    </router-link>
                                </div>
                                <div class="level-item">
                                    <router-link to="blog" class="button is-link is-primary">
                                        Blog
                                    </router-link>
                                </div>
                            </div>
                            
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
@import './scss/_var/_bulma.scss';
@import '~bulma';
html, body {
    margin:0;
    padding:0;  
}
* {
    box-sizing:border-box;
}

//fix container width on hero fullheight
@media screen and (max-width: 1023px) {
    .container {
        max-width:100%;
    }
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
