<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the111
      <a href="#" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <ul>
      <li><a href="#" target="_blank" rel="noopener">router1</a></li>
      <li><a href="#" target="_blank" rel="noopener">router</a></li>
      <li><a href="#" target="_blank" rel="noopener">vuex</a></li>
    </ul>
    <h3>Essential Links1111111</h3>
    <ul>
      <li><a href="#" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="#" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="#" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="#" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="#" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="#" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="#" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="#" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="#" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="#" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
