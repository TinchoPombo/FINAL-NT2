<template>

  <section class="src-components-inicio">
    <div class="jumbotron">
      <h1>FINAL</h1>
      <hr>
      <hr>

      Color: <input type="text" v-model="color">
      Fondo: <input type="text" v-model="fondo">
      Tamaño: <input type="text" v-model="tamanio">
      <hr>
      Texto: <input type="text" v-model="texto" :style="getStyle">

      <Palabras v-show="texto" :texto="texto"/>

      <br>
      <br>
      <hr>
      <table class="table table-dark">
        <tr>
          <th>Pregunta</th>
          <th>Respuesta</th>
        </tr>
        <tr v-for="(pregunta,index) in preguntas" :key="index">
          <td>{{ pregunta.pregunta }}</td>
          <td>{{ pregunta.respuesta }}</td>
        </tr>
      </table>
    </div>
  </section>

</template>

<script>

  import Palabras from './Palabras.vue'
  export default  {
    name: 'src-components-inicio',
    components: {
      Palabras
    },
    props: [],
    mounted () {

    },
    data () {
      return {
        texto: '',
        color: '',
        fondo: '',
        tamanio: '',



        preguntas: [
          {
            pregunta:'1',
            respuesta:'B'
          },

          {
            pregunta:'2',
            respuesta:'C'
          },
          
          {
            pregunta:'3',
            respuesta:'B'
          },

          {
            pregunta:'4',
            respuesta:'D'
          },

          {
            pregunta:'5',
            respuesta:'D'
          }
        ]
      }
    },
    methods: {

    },
    computed: {
      getStyle(){
      return { 
        'color': this.color,
        'background-color': this.fondo,
        'font-size': this.tamanio
      }
    }
    }
}


</script>

<style scoped lang="css">
  .src-components-inicio {

  }
</style>
