<template>
  <div id="app">
    <div class="row">
      <div class="col s12">
        <img :src="url_imagen" alt="">
      </div>  
    </div>
    <div class="row">
      <div class="col s4"></div>
      <div class="col s4">
        <div class="card">
            
            <div class="card-content">
              <div class="row">
              <div class="col s6">
                <button class="waves-effect waves-light btn-large grey lighten-5 grey-text" @click="cambiar_ninja">NINJA</button>
              </div>
              <div class="col s6">
                <button class="waves-effect waves-light btn-large grey lighten-5 grey-text" @click="cambiar_gato">GATO</button>
              </div>
            </div>
          </div>
        </div>      
      </div>
    </div>
  </div>
</template>

<script>
const ninja_img = './assets/ninja.png';
const gato_img = './assets/gato.png'

export default {
  name: 'App',
  data: function(){
    return {
      url_imagen: ninja_img
    }
  },
  methods: {
    cambiar_ninja(){
      this.url_imagen = ninja_img
      //alert('cambiar a ninja')
    },
    cambiar_gato(){
      this.url_imagen = gato_img
      alert('cambiar a gato')
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
