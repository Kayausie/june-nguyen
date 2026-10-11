<script setup>
import '../sass/styles.scss'
    defineProps({
        greet:String,
        desc:String,
    })
</script>
<template>
    <div class="container text-start">
        <div class="row align-items-center">
            <div class="col-8 ">
                <h1 >{{ greet }}</h1>
                <p>{{ desc }}</p>
            </div>
            <div class="col-4">
                <img src="../assets/unnamed.jpg">
            </div>
        </div>
    </div>
</template>
<style scoped>
    img{
        width: 100%;
        height: auto;
    }
</style>