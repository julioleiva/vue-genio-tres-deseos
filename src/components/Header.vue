<template>
    <div class="row center">
        <div class="col-sm-6 ">
            <h3>Deseos Concedidos</h3>
            <div class="progress">
                <div class="progress">
                    <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"
                        :style="{width: (deseoCount / maxDeseos) * 100 + '%'}">
                        {{ deseoCount }} / {{ maxDeseos}}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        props: ['deseoCount', 'maxDeseos']
    }
</script>
