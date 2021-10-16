<template>
<div>

<top-menu></top-menu>

    <div v-bind:id="idCarousel" class="carousel slide" data-ride="carousel">
    <ol class="carousel-indicators">
        <li v-bind:data-target="'#' + idCarousel" data-slide-to="0" class="active"></li>
        <li v-bind:data-target="'#' + idCarousel" data-slide-to="1" class=""></li>
        <li v-bind:data-target="'#' + idCarousel" data-slide-to="2" class=""></li>
    </ol>
    <div class="carousel-inner">
        <div class="carousel-item active">
<img src="https://holatelcel.com/wp-content/uploads/2017/08/Smart-Parking-1280x720.jpg" alt="banner image" height="400" width = "1600">
            <div class="carousel-caption d-none d-md-block">
                <h5>Parking Management
Solutions</h5>
                <p>Zonas de parqueo seguras</p>
            </div>
        </div>
        <div class="carousel-item">
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS-siLqZ4rH7rdxoouKm0UukavMDDvfH-pYrA&usqp=CAU" alt="banner image" height="400" width = "1600">
            <div class="carousel-caption d-none d-md-block">
                <h5>Parking Management
Solutions</h5>
                <p>Seguridad las 24 horas</p>
            </div>
        </div>
        <div class="carousel-item">
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTyXkrJupwmMDxHIXZC_wAqLiErrom26az-gw&usqp=CAU" alt="banner image" height="400" width = "1600" >
            <div class="carousel-caption d-none d-md-block">
                <h5>Parking Management
Solutions</h5>
                <p>Su confianza es nuestra responsabilidad.</p>
            </div>
        </div>
    </div>
    <a class="carousel-control-prev" :href="'#' + idCarousel" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next" :href="'#' + idCarousel" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
    </a>
</div>

</div>
</template>

<script>
import TopMenu from './TopMenu';

export default {
  name: "TopBanner",
  components:{
      TopMenu
  },
  props: ['idCarousel']
};
</script>

<style scoped>
</style>