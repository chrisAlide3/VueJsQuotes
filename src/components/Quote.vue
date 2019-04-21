<template>
    <div class="row">
        <div class="col-xs-4 col-md-8 col-lg-12">
            <div  class="card w-100">
                <div class="card-body">
                    <slot class="card-text"></slot>
                    <!-- <p class="card-text" readonly>{{ quote }}</p> -->
                </div>
            </div>
        </div>
    </div>        
</template>

<script>
export default {
    
}
</script>

<style scoped>
    .card {
        box-shadow: 1px 1px 2px grey;
        cursor: pointer;
    }
    .card:hover {
        background-color: azure;
    }
</style>
