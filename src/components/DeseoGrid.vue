<template>
    <div class="row">
        <app-deseo v-for="(deseo, index) in deseos" @click.native="deleteDeseo(index)"> Tue deseo :{{ deseo }} ¡ Ha sido concedido!</app-deseo>
    </div>
</template>

<script>
    import Deseo from './Deseo.vue';

    export default {
        props: ['deseos'],
        components: {
            appDeseo: Deseo
        },
        methods: {
            deleteDeseo(index) {
                this.$emit('deseoDeleted', index);
            }
        }
    }
</script>

<style>

</style>
