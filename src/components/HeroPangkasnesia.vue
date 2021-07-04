<template>
   <!-- Hero Section Begin -->
    <section class="hero-section">
      <carousel class="hero-items" :items="1" :dots="true" :loop="true" :autoplay="true" :nav="false">
        <div class="single-hero-items set-bg" style="background-image: url('img/pangkas-1.jpg')">
          <div class="container">
            <div class="row">
              <div class="col-lg-5">
                <span>pangkasnesia</span>
                <h1 style="color:white">Pangkas pria</h1>
                <p>
                  Perawatan rambut mulai dari pangkas, keramas, hingga merawat kesehatan rambut khusus
                  pria, harga minimalis namun hasil diatas rata rata  
                </p>
                <a href="http://127.0.0.1:8000/login" class="primary-btn">Order Now</a>
              </div>
            </div>
          </div>
        </div>
        <div class="single-hero-items set-bg" style="background-image: url('img/pangkas-3.jpg')">
          <div class="container">
            <div class="row">
              <div class="col-lg-5">
                <span>pangkasnesia</span>
                <h1 style="color:white">Pangkas anak-anak</h1>
                <p>
                  Perawatan rambut mulai dari pangkas, keramas, hingga merawat kesehatan rambut khusus
                  anak anak dengan pelayanan yang ramah terhadap anak anak, harga nyaman di dompet 
                  namun hasil diatas rata - rata, dijamin anak - anak betah
                </p>
                <a href="http://127.0.0.1:8000/login" class="primary-btn">Order Now</a>
              </div>
            </div>
          </div>
        </div>
        <div class="single-hero-items set-bg" style="background-image: url('img/pangkas-2.jpg')">
          <div class="container">
            <div class="row">
              <div class="col-lg-5">
                <span>pangkasnesia</span>
                <h1 style="color:white">Pangkas wanita</h1>
                <p>
                  Perawatan rambut mulai dari keramas, cukur, creambath, hingga perawatan rambut
                  lainnya khusus wanita yang tentunya dicukur oleh wanita itu sendiri sehingga keamanan
                  dijamin 100%
                </p>
                <a href="http://127.0.0.1:8000/login" class="primary-btn">Order Now</a>
              </div>
            </div>
          </div>
        </div>
      </carousel>
    </section>
    <!-- Hero Section End -->
</template>

<script>
import carousel from 'vue-owl-carousel';

export default {
    name: 'HeroPangkasnesia',
    components: {
        carousel
    }
}
</script>