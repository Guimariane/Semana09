<template>
<Header/>
<Formulario @cadastrar="AdicionarMedicamento"/>

<div>
  <CardMedicamento 
  v-for="MedName in listaMedicamentos"
  :key="MedName.id"
  @favoritar="FavoritarMedicamento"
  :nome="MedName.nome"
  :laboratorio="MedName.laboratorio"
  :preco="MedName.preco"
  :id="MedName.id"/>
</div>
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
    },

    FavoritarMedicamento (id){
      this.listaMedicamentos = this.listaMedicamentos.map(item => {
        if(item.id === id) {
          item.favorito =! item.favorito
        }
      })
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

