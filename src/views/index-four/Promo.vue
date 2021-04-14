<template>
    <section class="promo-section" v-bind:class="{ 'gray-light-bg' : isGray }">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-md-10 col-lg-8">
                    <div class="section-heading text-center">
                        <h2>Si usted lidera una causa social, nuestro propósito es acompañarlo</h2>
                        <p>Continuamos trabajando por nuestras organizaciones sociales para capacitar a los equipos comprometidos con su misión y fortalecer junto a ellos las habilidades necesarias para sacar adelante sus iniciativas sociales.</p>
                    </div>
                </div>
            </div>
            <div class="row justify-content-md-center justify-content-sm-center">
                    <div class="col-md-6 col-lg-3">
                        <img src="../../assets/img/causa-social-1.png" alt="" width="100%" height="auto">
                    </div>
                    <div class="col-md-6 col-lg-3">
                        <img src="../../assets/img/causa-social-2.png" alt="" width="100%" height="auto">
                    </div>
                    <div class="col-md-6 col-lg-3">
                        <img src="../../assets/img/causa-social-3.png" alt="" width="100%" height="auto">
                    </div>
                    <div class="col-md-6 col-lg-3">
                        <img src="../../assets/img/causa-social-4.png" alt="" width="100%" height="auto">
                    </div>
                </div>
        </div>
    </section>
</template>


<script>
    export default {
        name: 'Promo',
        props: {
            isGray: {
                type: Boolean,
                default: false
            }
        }
    }
</script>