<template>
  <div class="hellos">
    <h1>{{ msg }}</h1>
   <li><a href="http://localhost:8080/#/"> 退回上一页</a></li>
    <h2>Ecosystem</h2>
   
  </div>
</template>

<script>
export default {
  name: 'hellos',
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
