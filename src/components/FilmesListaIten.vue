<template>
    <li class="list-group-item">
        <span>{{ tituloConcatenado }} | {{ ano }}</span>
        <button class="btn btn-success float-right">Selecionar</button>
    </li>
</template>

<script>
export default {
    props: {
        titulo: {
            type: String,
            required: true
            // default () {
            //     return 'Vingadores'
            // },
            // validator (titulo) {
            //     return titulo.includes('Marvel');
            // }
        },
        ano: {
            type: Number,
            required: true
        }
    },
    computed: {
        tituloConcatenado () {
            return `Titulo: ${this.titulo}`
        }
    },
    created () {
        console.log(typeof this.titulo);
    }
}
</script>
