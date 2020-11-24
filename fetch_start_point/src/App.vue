<template>
  <div id="app">
    <h1>RANDOGMISER</h1>
    <img id="dog-img" v-if="dogImgURL" :src="dogImgURL">
    <button v-on:click="fetchDog">Gimme those dogs!</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      dogImgURL: null
    }
  },
  mounted(){
    this.fetchDog(); //mounted helps load default
  },


  methods: {
    fetchDog: function(){
      fetch("https://dog.ceo/api/breeds/image/random")      //fetch is the promise
      .then(response => response.json())
      .then(data => this.dogImgURL = data.message)
    }                                              //lifecycle hooks - loads up all info in DOM
  }
}
</script>

<style>
#app {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 40%;
}

#dog-img {
  width: 500px;
}

</style>
