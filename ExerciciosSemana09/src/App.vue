<template>
<Header/>
<Formulario/>
</template>

<script>
import Header from '../src/components/Header.vue';
import Formulario from '../src/components/FormularioNovoMedicamento.vue'

export default {
  data() {
    listaMedicamentos: []
  },

  method:{
    AdicionarMedicamento(nome, laboratorio, preco){
      if (nome == '' || laboratorio == '' || preco == 0){
        alert("Dados obrigatórios")
        return
      }
      const novoMedicamento = {
        id: 1,
        nome: MedName,
        laboratorio: LabName,
        preco: Price,
        favorito: false
      }
      this.listaMedicamentos.push(novoMedicamento)
    }
  },
  components: {
    Header,
    Formulario
  }
}
</script>

<style scoped>

</style>

