<template>
  <section id="ruta-formativa"
      class="screenshots-section"
      v-bind:class="{ 'gray-light-bg': isGray, 'pb-100': paddingBottom, 'pt-100': paddingTop }">
      <div class="container">
          <div class="row align-items-center justify-content-between text-center text-lg-left pt-40">
                    <div class="col-md-12 col-lg-6">
                        <div class="feature-contents section-heading">
                            <h2 class="form-title">Con los resultados del autodiagnóstico, puede emprender la Ruta de Formación virtual.</h2>
                            <p>
                                El proceso de formación fue diseñado por Aflora para que tanto el líder como el equipo de su organización mejoren en las áreas evaluadas y así tracen metas definidas, orientadas a cumplir objetivos de corto, mediano y largo plazo.
                            </p>
                            <div class="action-btns mt-4">
                                <a href="https://formamostalento.fundacionbd.org/blocks/autodiagnostico/ruta.php?instanceid=771"
                                class="btn btn-brand-02 mr-3 form-btn"
                                @click="rutaFormacion"
                                target="_blank"
                                >Inicie la ruta de formación</a>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6 col-lg-6">
                       <div>
                            <img src="../../assets/img/banner-3.svg" class="img-fluid" alt="about">
                        </div>
                    </div>
                </div>
          <div class="screenshot-wrap">
              <!--<div class="screenshot-frame"></div>-->

              <carousel
                  :autoplay="true"
                  :dots="true"
                  :loop="true"
                  :responsive="{0:{items: 1},768:{items: 3},991:{items: 4},1200:{items:4},1920:{items: 4}}"
                  :margin="0"
                  :center="true"
                  :nav="false"
                  class="screen-carousel owl-theme dot-indicator">
                  <img
                      src="../../assets/img/01.jpg"
                      class="img-fluid"
                      alt="screenshots"
                  />
                  <img
                      src="../../assets/img/02.jpg"
                      class="img-fluid"
                      alt="screenshots"
                  />
                  <img
                      src="../../assets/img/03.jpg"
                      class="img-fluid"
                      alt="screenshots"
                  />
                  <img
                      src="../../assets/img/04.jpg"
                      class="img-fluid"
                      alt="screenshots"
                  />
                  <img
                      src="../../assets/img/05.jpg"
                      class="img-fluid"
                      alt="screenshots"
                  />
                  <img
                      src="../../assets/img/06.jpg"
                      class="img-fluid"
                      alt="screenshots"
                  />
                  <img
                      src="../../assets/img/07.jpg"
                      class="img-fluid"
                      alt="screenshots"
                  />
                  <img
                      src="../../assets/img/08.jpg"
                      class="img-fluid"
                      alt="screenshots"
                  />
                  <img
                      src="../../assets/img/09.jpg"
                      class="img-fluid"
                      alt="screenshots"
                  />
              </carousel>

          </div>
      </div>
  </section>
</template>

<script>
    import carousel from "vue-owl-carousel";
    export default {
        name: "Screenshots",
        props: {
            isGray: {
                type: Boolean,
                default: false
            },
            paddingTop: {
                type: Boolean,
                default: true
            },
            paddingBottom: {
                type: Boolean,
                default: true
            }
        },
        components: { carousel },
        methods : {
            rutaFormacion(){
            this.$gtag.event('rutaFormacion', {
            'event_category': 'interaccion',
            'event_label': 'rutaFormacion',
            'value': '3',
            })
            }
        }
    };
</script>

<style>

</style>
