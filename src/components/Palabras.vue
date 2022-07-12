<template>

  <section class="src-components-palabras">
    Cantidad de Palabras: {{obtenerCantPalabras}}
  </section>

</template>

<script>

  export default  {
    name: 'src-components-palabras',
    props: ['texto'],
    mounted () {

    },
    data () {
      return {

      }
    },
    methods: {

    },
    computed: {
      obtenerCantPalabras(){
        return this.texto.trim().split(' ').length
      }
    }
}


</script>

<style scoped lang="css">
  .src-components-palabras {

  }
</style>
