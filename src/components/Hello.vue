<template>
  <div class="hello">
    <a target="_blank" href="http://bulma.io/">
      <img src="./../assets/bulma-logo.png">
      </a>
    <p>
      A modern CSS framework based on Flexbox by <b>Jeremy Thomas</b> (Frontend Designer from Bordeaux, France)<br />
      <ul>
        <li>
            <a target="_blank" href="http://jgthms.com/">
                <img src="./../assets/jeremy.jpg">
            </a>
            </li>
        <li>
            <a target="_blank" href="https://github.com/jgthms">
                <img src="./../assets/github.svg">
            </a>
        </li>
        <li>
            <a target="_blank" href="https://twitter.com/jgthms?lang=es">
                <img src="./../assets/twitter.svg">
            </a>
        </li>
        <li>
            <a target="_blank" href="http://caniuse.com/#feat=flexbox">
                <img src="./../assets/caniuse.png">
            </a>
        </li>
      </ul>
    </p>
  </div>
</template>

<script>
export default {
    data () {
        return {
            msg: 'Welcome to Your Vue.js App'
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
h1, h2 {
  font-weight: normal;
}

ul {
    list-style-type: none;
    padding: 0;
    li {
    display: inline-block;
    margin: 0 10px;
        img {
            max-width:40px;
            height:auto;
        }
    }

}


a {
  color: #42b983;
}
</style>
