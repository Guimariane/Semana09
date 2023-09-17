<template>
    <div>
        <button @click="$emit('favoritar', id)">Favoritar</button>
        <span v-if="favorito">Favorito</span>
        <img src='../assets/comprimidos.jpg'>
        <span>{{nome}}</span>
        <span>{{laboratorio}}</span>
        <span>{{preco}}</span>
    </div>
</template>

<script>

export default {
    props: ['nome', 'laboratorio', 'preco', 'favorito', 'id']
}
</script>
