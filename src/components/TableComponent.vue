<template lang="html">
  <section class="table-component">
    
    <h1 class="pb-3">{{msg}}</h1>

    <div class="container">
      <table class="table table-fluid">
          <thead>
              <tr>
                  <th scope="col">Cantidad</th>
                  <th scope="col">Producto</th>
                  <th scope="col">Precio</th>
              </tr>
          </thead>
          <tbody>
              <tr v-for="(product) in Json" :key="product.id">
                  <td>{{product.cantidad}}</td>
                  <td>{{product.producto}}</td>
                  <td v-if="product.precio < 100" :style="estilo_verde">{{product.precio}}</td>
                  <td v-else-if="product.precio >=100 && product.precio <=351" :style="estilo_amarillo" class="text-dark">{{product.precio}}</td>
                  <td v-else :style="estilo_rojo">{{product.precio}}</td>
              </tr>
          </tbody>
      </table>
    </div>

  </section>
</template>

<script>
  export default  {
    name: 'table-component',
    props: {
      msg: String,
      estilo_rojo: String,
      estilo_amarillo: String,
      estilo_verde: String,
      blanco: String,
      Json: Array
    },
    
    mounted () {

    },
    data () {
      return {

      }
    },
    methods: {
        
    },
    computed: {

    }
}
</script>

<style scoped>
  h1 {
    color: #fff !important;
    font-size: 2em;
    font-weight: bold;
    text-shadow: 0 0 10px black;
  }
  th {
    background-color: #42b983;
    color: #fff;
    text-shadow: 0 0 30px black;
  }
  td {
    color: #fff;
  }
</style>
