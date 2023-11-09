<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-4">
                    <a href="#" class="logo">
                        <img src="../assets/images/la-molisana-logo.png" alt="La Molisana">
                    </a>
                </div>

                <div class="col-4" v-for="item, index in menu" :key="index">
                    <h4>{{ item.title }}</h4>
                    <nav>
                        <ul>
                            <li v-for="(link, index) in item.links" :key="index"><a :href="link.url">{{ link.text }}</a>
                            </li>

                        </ul>
                    </nav>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterApp',
    data() {
        return {
            menu: [
                {
                    title: 'Pastificio',
                    links: [
                        {
                            text: "Il Pastificio",
                            url: "#",
                        },
                        {
                            text: "Grano",
                            url: "#",
                        },
                        {
                            text: "Filiera",
                            url: "#",
                        },
                        {
                            text: "100 anni di pasta",
                            url: "#",
                        },
                        {
                            text: "Sartoria della pasta",
                            url: "#",
                        }

                    ]
                },
                {
                    title: 'Prodotti',
                    links: [
                        {
                            text: "Le classiche",
                            url: "#",
                        },
                        {
                            text: "Le Integrali",
                            url: "#",
                        },
                        {
                            text: "Le Speciali",
                            url: "#",
                        },
                        {
                            text: "Le Biologiche",
                            url: "#",
                        },
                        {
                            text: "SLe Gluten-free",
                            url: "#",
                        }
                    ]
                },

            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;


footer {
    padding-top: 3rem;
    background-image: url('/images/footer-montagne-bottom.jpg');
    background-repeat: no-repeat;
    background-position: bottom;
    padding-bottom: 1rem;

    ul {
        list-style-type: none;
        margin: 0;
        padding: 0;

        li a {
            color: $blacktext;
            text-decoration: none;

            &:hover {
                color: $bluetext;
            }
        }
    }
}
</style>