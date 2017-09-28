<template>
  <div class="hello">
    <a target="_blank" href="http://bulma.io/">
      <img src="./../assets/bulma-logo.png">
    </a>
    <section>
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
    </section>
    <section>
        <h2>Starting</h2>
        <p class="code">
            git clone https://github.com/Dandomanos/taller-bulma<br />
            cd taller-bulma <br />
            git checkout starting<br />
            npm i <br />
            npm run dev <br />
        </p>
    </section>
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
* {
    box-sizing:border-box;
}
h1, h2 {
  font-weight: normal;
}
section {
    margin:4rem auto;
    padding:1rem;
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
.code {
    font-family:monospace;
    font-size: 1.5rem;
    text-align:left;
    border:1px dashed #ccc;
    padding:1rem;
    max-width:40rem;
    margin:0 auto;
    width:auto;
}
</style>
