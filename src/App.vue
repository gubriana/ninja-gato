<template>
  <div id="app">
    <div class="row">
      <div class="col s4"></div>
      <div class="col s4">
        <div class="row">
          <div class="card">
            <div class="card-image">
              <img v-bind:src="url_imagen" alt="">
            </div>
            <div class="card-content">
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
const ninja_img = require('@/assets/ninja.png');
const gato_img = require('@/assets/gato.png')

export default {
  name: 'App',
  data(){
    return {
      url_imagen: ninja_img
    }
  },
  methods: {
    cambiar_ninja(){
      this.url_imagen = ninja_img;
      //alert('cambiar a ninja')
    },
    cambiar_gato(){
      this.url_imagen = gato_img;
      //alert('cambiar a gato')
    }
  },
  beforeUpdate(){
    alert(`Tu imagen está apunto de cambiar! Ya no será un ${this.url_img == ninja_img ? 'ninja y será un gato' : 'gato y será un ninja'}`)
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
