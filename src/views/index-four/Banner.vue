<template>
  <!--hero section start-->
  <section class="position-relative overflow-hidden hero-section-3 ptb-100" id="activese">
    <!--animated circle shape start-->
    <div class="animated-shape-wrap">
      <div class="animated-shape-item"></div>
      <div class="animated-shape-item"></div>
      <div class="animated-shape-item"></div>
      <div class="animated-shape-item"></div>
      <div class="animated-shape-item"></div>
    </div>
    <!--animated circle shape end-->
    <img src="../../assets/img/combined-shape.svg" alt="s" class="shape-img-2">
    <img src="../../assets/img/shape-2.svg" alt="group shape" width="60" class="img-fluid group-shape-2">
    <div class="container">
      <div class="row align-items-center justify-content-between">
        <div class="col-md-6 col-lg-6">
          <div class="hero-content-left pt-5">
            <h1 class="font-weight-bold">¡Organizaciones Sociales!</h1>
            <p class="lead">En Aflora nuestro propósito es acompañarlos en el proceso de formación para que multipliquen su capacidad de servir.</p>
            <div class="action-btns mt-4 text-center text-md-left">
              <a
                href="https://forms.gle/aYjN8NcGM7d1cUrz8"
                class="btn btn-brand-03 btn-rounded mr-3 aflora-secondary-btn"
                target="_blank"
                @click="activacion"
                >
                ¡Active su organización!
              </a>
              <a href="https://www.youtube.com/watch?v=pFNUdaoBIJI" class="popup-youtube btn btn-white btn-circle btn-icon" target="_blank"><i class="fas fa-play"></i> </a> <span class="pl-2">Conozca más</span>
            </div>
          </div>
        </div>
        <div class="col-md-6 col-lg-6">
          <div class="img-wrap">
            <img src="../../assets/img/banner.svg" alt="hero" class="img-fluid">
          </div>
        </div>
      </div>
    </div>

    <!--shape image start-->
    <img src="../../assets/img/hero-bg-shape-4.svg" class="shape-image" alt="shape image">
    <!--shape image end-->
  </section>
</template>

<script>
export default {
  name: "Banner",
    methods : {
      activacion(){
        this.$gtag.event('activacion', {
        'event_category': 'interaccion',
        'event_label': 'activacion',
        'value': '1',
      })
    }
  }
}
</script>

<!--<style lang="scss">-->
  <!--.hero-bottom-shape-bg {-->
    <!--background: url('../../assets/img/hero-bottom-shape-2.svg')no-repeat bottom center-->
  <!--}-->
<!--</style>-->