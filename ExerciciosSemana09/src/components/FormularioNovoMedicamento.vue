<template>
    <form>
        <label>Nome do Medicamento</label>
        <input type="text" id="MedName" v-model="MedName">

        <label>Nome do Laboratório</label>
        <input type="text" id="LabName" v-model="LabName">

        <label>Preço do Medicamento</label>
        <input type="number" id="Price" v-model="price">

        <button type="submit" @click="$emit('cadastrar', MedName, LabName, Price)">Cadastrar</button>       
    </form>
</template>

<script>

export default {
    data() {
        return {
            MedName: '',
            LabName: '',
            Price: 0
        }
    },
}
</script>

<style scoped>
form {
    display: flex;
    flex-direction: column;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;

}

label{
    margin-top: 10px;
}

input{
    margin-bottom: 10px;
}

button {
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    height: 40px
}
</style>
