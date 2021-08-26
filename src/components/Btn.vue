<template>
    <button
        @click="accionHijo"
    >
        {{textoBoton}}
    </button>
</template>

<script>
export default {
    props: ['textoBoton'],
    setup(props, context) {
        const accionHijo = () => {
            context.emit('accionBtn')
        }

        return {accionHijo}
    }
}
</script>

<style>

</style>