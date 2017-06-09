<template>
    <div class="row">
        <form>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <label>Deseo</label>
                <textarea class="form-control" rows="3" v-model="deseo"></textarea>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
               <button class="btn btn-primary" @click.prevent="createNew">Pedir Deseo</button>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
                deseo: ''
            };
        },
        methods: {
            createNew() {
                this.$emit('deseoAdded', this.deseo);
                this.deseo = '';
            }
        }
    }
</script>

<style>

</style>
