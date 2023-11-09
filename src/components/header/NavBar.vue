<template>
    <nav>
        <ul class="nav justify-content-center">
      <li class="nav-item" v-for="(link, index) in menu" :key="index">
      <a class="nav-link" :href="link.url" :class="{'active': link.current}">  {{ link.text }}</a>
    </li>
     </ul>
    </nav>
</template>

<script>
    export default {
        name: 'NavBar',
        data(){
            return {
                menu: [
                    {
                        text: "Home",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Prodotti",
                        url: "#",
                        current: true,
                    },
                    {
                        text: "Chi Siamo",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Contatti",
                        url: "#",
                        current: false,
                    },
                ]
            }
        }
    }
</script>

<style lang="scss">
 .active{
    background-color: blue;
 }
</style>