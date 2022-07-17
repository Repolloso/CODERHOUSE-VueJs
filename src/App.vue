<!-- Where you construct your page adding the components -->
<template>
  <div id="app">

    <TableComponent 
      :msg="msg"
      :estilo_verde="estilo_verde"
      :estilo_amarillo="estilo_amarillo"
      :estilo_rojo="estilo_rojo"
      :blanco="blanco"
      :Json="Json"
    />

  </div>
</template>

<script>
// Import the components that will be used in the app
import TableComponent from './components/TableComponent.vue'

export default {
  name: 'App',
  components: {
    TableComponent,
  },
  data () {
    return {
      msg: 'Tabla con Vue CLI',
      estilo_verde: 'background-color: green; color: white;',
      estilo_amarillo: 'background-color: yellow;',
      estilo_rojo: 'background-color: red;',
      blanco: 'color: white;',
      Json: [
              {
                  cantidad: 12,
                  producto: 'Leche',
                  precio: 200
              },
              {
                  cantidad: 21,
                  producto: 'Carne',
                  precio: 351
              },
              {
                  cantidad: 43,
                  producto: 'Arroz',
                  precio: 512
              },
              {
                  cantidad: 54,
                  producto: 'Chocolate',
                  precio: 631
              },
              {
                  cantidad: 52,
                  producto: 'Cafe',
                  precio: 52
              },
              {
                  cantidad: 6,
                  producto: 'Salchichas',
                  precio: 63
              },
        ],
    }
  },
}
</script>

<style>
#app {
    background-image: linear-gradient(to right, #1768e1, #5a62ed, #8a57f3, #b743f2, #e112eb);
    justify-content: center;
    text-align: center;
    flex-direction: column;
    display: flex;
    height: 100vh;
    margin: 0;
    padding: 0;
}
</style>
