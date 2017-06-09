<template>
    <div class="container">
        <app-header :deseoCount="deseos.length" :maxDeseos="maxDeseos"></app-header>
        <app-new-deseo @deseoAdded="newDeseo" :v-if="visibilidad"></app-new-deseo>
        <app-deseo-grid :deseos="deseos" @deseoDeleted="deleteDeseo"></app-deseo-grid>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">{{ info }}</div>
            </div>
        </div>
    </div>
</template>

<script>
    import DeseoGrid from './components/DeseoGrid.vue';
    import NewDeseo from './components/NewDeseo.vue';
    import Header from './components/Header.vue';

    export default {
        data: function () {
            return {
                deseos: [
                    // 'Just a Deseo to see something'
                ],
                maxDeseos: 3,
                info:'Info: Pulsa en un deseo para eliminarlo!',
                visibilidad:true
              }
        },
        props:['visible'],
        methods: {
            newDeseo(deseo) {
                if (this.deseos.length >= this.maxDeseos) {
                    return this.info = 'Eres un avaricioso, lo has perdido todo';
                    return this.visibilidad= false;

                }
                this.deseos.push(deseo);
            },
            deleteDeseo(index) {
                this.deseos.splice(index, 1);
            }
        },
        components: {
            appDeseoGrid: DeseoGrid,
            appNewDeseo: NewDeseo,
            appHeader: Header
        }
    }
</script>

<style>
</style>
