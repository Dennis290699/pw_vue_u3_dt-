<template>
    <h1>Hola Mundo</h1>
    <h1>Consultando datos del estudiante con ID: {{ idEstudiante }}</h1>

    <div>
        <button @click="mostrarDatos">Mostrar datos</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            idEstudiante: null,
        }
    },
    created() {
        console.log(this.$route.params.id);
        console.log(this.$route);
        console.log(this.$route.query.id);
    },
    methods: {
        mostrarDatos() {
            this.idEstudiante = this.$route.params.id;
        }
    }
}
</script>

<style scoped>
</style>
