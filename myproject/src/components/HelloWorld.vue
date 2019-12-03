<template>
  <div class="hello">
    <shittylist/>
  </div>
</template>

<script>
  import Shittylist from "./Shittylist"
export default {
  name: 'HelloWorld',
  components: {Shittylist},

  mounted(){

  },
  //events and shit ...

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
