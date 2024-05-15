<template>
  <div id="app">
    <h1 :style="{
      color: colorPrincipal,
      fontSize: peso,
    }">Titulo principal</h1>
    <div>
      <label for="rangeImg"> Rango imagen</label>
      <input type="range" name="vol" id="rangeImg" min="20" max="100" step="1" v-model="anchoImagen"><span></span>

      <label for="sombra"> Sombra</label>
      <input type="range" name="vol" id="rangeImg" min="20" max="100" step="1" v-model="sombra"><span></span>

      <label for="Borde"> Borde Redondeado</label>
      <input type="range" name="vol" id="rangeImg" min="0" max="50" step="1" v-model="borde"><span>{{ borde + "%"
        }}</span>


      <div>
        <img :style="{ width: anchoImagen + '%', boxShadow: sombra, borderRadius: borde + '%', }"
          src="https://picsum.photos/id/1025/1200/800" alt="" />
      </div>
    </div>
    <div style="padding: 25px 20px;">
          <p :class="{realizado: p1}">Texto de ejemplo 1 <input type="checkbox" v-model="p1"></p>
          <p :class="{realizado: p2}">Texto de ejemplo 2 <input type="checkbox" v-model="p2"></p>
          <p :class="{realizado: p3}">Texto de ejemplo 3 <input type="checkbox" v-model="p3"></p>
          <p :class="{realizado: p4}">Texto de ejemplo 4 <input type="checkbox"
            v-model="p4"></p>
        </div>


  </div>
</template>

<script>

export default {
  name: 'App',
  components: {

  },
  data() {
    return {
      colorPrincipal: "red",
      peso: "10px",
      anchoImagen: undefined,
      sombra: "5px 5px 10px 5px rgba(0,0,0,0.75)",
      borde: "50%",

    }
  },
}
</script>
<style>
  .realizado {
    color: red;
    font-weight: 800;
  }
</style>
