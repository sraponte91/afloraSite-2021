<template>
    <div class="overflow-hidden">
        <section id="autodiagnostico" class="position-relative overflow-hidden feature-section ptb-60" v-bind:class="{ 'bg-brand-04' : isGray }">
            <div class="container">
                <div class="row align-items-center justify-content-between">
                    <div class="col-md-12 col-lg-6 text-center text-lg-left">
                        <div class="feature-contents section-heading">
                            <h2 class="auto-title">Realice el autodiagnóstico de su organización</h2>
                            <p class="auto-paragraph">
                                Para identificar sus fortalezas y aspectos por mejorar, a través de la evaluación de cada una de las áreas que la conforman. <br>
                                Recuerde que debe diligenciar el autodiagnóstico en su totalidad, de lo contrario la información no quedará guardada.
                            </p>
                            <div class="action-btns mt-4">
                                <a href="https://formamostalento.fundacionbd.org/blocks/autodiagnostico/formulario.php?instanceid=771" 
                                class="btn btn-brand-02 mr-3 auto-button"
                                @click="autodiagnostico"
                                target="_blank"
                                >Realice su autodiagnóstico</a>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6 col-lg-6">
                       <div>
                            <img src="../../assets/img/banner-2.svg" class="img-fluid" alt="about">
                        </div>
                    </div>
                </div>
                <div class="row justify-content-md-center justify-content-sm-center">
                    <div class="col-md-6 col-lg-3 text-center">
                        <img src="../../assets/img/elemento-5.svg" alt="" width="50%" height="auto">
                    </div>
                    <div class="col-md-6 col-lg-3 text-center">
                        <img src="../../assets/img/elemento-7.svg" alt="" width="50%" height="auto">
                    </div>
                    <div class="col-md-6 col-lg-3 text-center">
                        <img src="../../assets/img/elemento-6.svg" alt="" width="50%" height="auto">
                    </div>
                    <div class="col-md-6 col-lg-3 text-center">
                        <img src="../../assets/img/elemento-8.svg" alt="" width="50%" height="auto">
                    </div>
                </div>
                <div class="row align-items-center justify-content-md-center justify-content-sm-center" style="color: #333 !important;">
                    <div class="col-md-6 col-lg-3">
                        <div class="card border-0 single-promo-card p-2 mt-4 shadow">
                            <div class="card-body" style="height: 355px !important">
                                <div class="pb-2">
                                    <span class="fas fa-medal icon-size-md text-red-01"></span>
                                </div>
                                <div class="pt-2 pb-3">
                                    <h5>Tip</h5>
                                    <p class="mb-0"> Es muy importante que las respuestas al autodiagnóstico sean cercanas a su realidad, así nuestra herramienta reflejará la ruta de acompañamiento más acorde a sus necesidades.</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6 col-lg-3">
                        <div class="card border-0 single-promo-card p-2 mt-4 shadow">
                            <div class="card-body" style="height: 355px !important">
                                <div class="pb-2">
                                    <span class="fas fa-medal icon-size-md text-red-01"></span>
                                </div>
                                <div class="pt-2 pb-3">
                                    <h5>Tip</h5>
                                    <p class="mb-0">Cada uno de estos niveles ofrece diferentes beneficios a los que su organización podrá acceder a medida que avance en la Ruta de Formación.</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <YTModal url="https://www.youtube.com/watch?v=1APwq1df6Mw" v-if="showModal" @close="showModal = false">
                This is my first modal
            </YTModal>
        </section>
    </div>
</template>

<script>
    import YTModal from '../../components/YTModal';
    export default {
        name: 'Offerings',
        components: { YTModal },
        props: {
            isGray: {
                type: Boolean,
                default: false
            }
        },
        data: function(){
            return {
                showModal: false
            }
        },
        methods: {
            showYouTubeModal: function(e) {
                e.preventDefault();
                this.showModal = true;
            },
            autodiagnostico(){
                this.$gtag.event('autodiagnostico', {
                'event_category': 'interaccion',
                'event_label': 'autodiagnostico',
                'value': '2',
                })
            }
        }
    }

    
</script>