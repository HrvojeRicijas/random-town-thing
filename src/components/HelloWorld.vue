
<template>
  <div class="hello">
    <h1>Welcome to the fruit factory {{message}}</h1>
    <input v-on:keyup.enter="addFruit" v-model="message">
    <div>
      <p v-for="fruit in fruits" :key="fruit"> {{ fruit }} </p>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',

  props: {
    msg: String
  },

  data: function(){
    return {
      fruits: [
        "banana",
        "mrkva",
      ],
      message: "",

    }
  },

  methods: {
      addFruit(){
        this.fruits.push(this.message)
        this.message = ""
      }
  },

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
