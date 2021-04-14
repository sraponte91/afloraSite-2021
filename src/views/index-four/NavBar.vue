<template>
    <header class="header">
        <nav class="navbar navbar-expand-lg fixed-top" v-bind:class="{ affix: hasAffix, 'custom-nav': coloredLogo, 'bg-transparent': !coloredLogo }">
            <div class="container">
                <a class="navbar-brand" href="/">
                    <img
                        :src="coloredLogo ? '../../assets/img/logo-color.png' : '../../assets/img/logo-white.png'"
                        alt="logo"
                        class="img-fluid"
                    />
                </a>
                <button class="navbar-toggler" type="button" @click="mobileNavClicked" v-bind:class="{ 'collapsed': collapsed }">
                    <span class="ti-menu"></span>
                </button>
                <div class="collapse navbar-collapse h-auto" v-bind:class="{ 'show': !collapsed }" id="navbarSupportedContent">
                    <ul class="navbar-nav ml-auto menu">
                        <li>  
                        <router-link to="#activese" v-scroll-to="'#activese'">Activación</router-link>
                        </li>
                        <li>
                            <router-link to="#autodiagnostico" v-scroll-to="'#autodiagnostico'">Autodiagnóstico</router-link>
                        </li>
                        <li>
                            <router-link to="#ruta-formativa" v-scroll-to="'#ruta-formativa'">Ruta Formativa</router-link>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </header>
</template>

<script>
    export default {
        props: {
            coloredLogo: {
                type: Boolean,
                default: false
            }
        },
        data: function() {
            return {
                windowTop: 0,
                collapsed: true
            }
        },
        mounted() {
            window.addEventListener("scroll", this.onScroll)
        },
        beforeDestroy() {
            window.removeEventListener("scroll", this.onScroll)
        },
        methods: {
            onScroll: function() {
                this.windowTop = window.top.scrollY
            },
            mobileNavClicked: function() {
                this.collapsed = !this.collapsed;
            }
        },
        computed: {
            hasAffix: function () {
                return this.windowTop > 0;
            }
        }
    }
</script>

