<script>
    import calculadora from './components/calculadora.vue';
    
    export default {
        components: {
        calculadora
        }
    };
</script>

<template>
    <div id="app">
        <h1>Calculadora Vue</h1>
        <calculadora />
    </div>
</template>

<style>
    #app {
        text-align: center;
    }
</style>
  