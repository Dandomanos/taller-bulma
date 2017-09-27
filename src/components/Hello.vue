<template>
  <div class="hello">
    <img src="http://bulma.io/images/bulma-logo.png" alt="Bulma">
    <p>
      A modern CSS framework based on Flexbox by <b>Jeremy Thomas</b><br />
      <ul>
        <li><a target="_blank" href="http://bulma.io/">Oficial</a></li>
        <li><a target="_blank" href="https://github.com/jgthms">Github</a></li>
        <li><a target="_blank" href="https://twitter.com/jgthms?lang=es">Twitter</a></li>
      </ul>
    </p>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
  color: #42b983;
}
</style>
