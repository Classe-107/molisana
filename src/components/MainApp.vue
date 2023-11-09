<template>
    <main>
    <section class="container">
        <h1>Content goes heare</h1>
    </section>
        
  </main>
</template>

<script>
    export default {
        name: 'MainApp',
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

 main{
    background-image: url('/images/fondo-pag-speciali.jpg');
    text-align: center;
    padding: 20px;

    h1{
        color:black;
    }
 }
</style>