<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div class="panel-body deseo">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
</script>

<style>
    .panel-body {
        font-family: 'Arizonia', cursive;
        font-size: 24px;
        color: #6e6e6e;
    }

    .deseo {
        cursor: pointer;
    }

    .deseo:hover {
        background-color: #ffe2e2;
    }
</style>
