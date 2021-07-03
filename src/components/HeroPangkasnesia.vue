<template>
   <!-- Hero Section Begin -->
    <section class="hero-section">
      <carousel class="hero-items" :items="1" :dots="true" :loop="true" :autoplay="true" :nav="false">
        <div class="single-hero-items set-bg" style="background-image: url('img/pangkas-1.jpg')">
          <div class="container">
            <div class="row">
              <div class="col-lg-5">
                <span>pangkasnesia</span>
                <h1>Pangkas pria</h1>
                <p>
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed
                  do eiusmod tempor incididunt ut labore et dolore
                </p>
                <a href="#" class="primary-btn">Order Now</a>
              </div>
            </div>
          </div>
        </div>
        <div class="single-hero-items set-bg" style="background-image: url('img/pangkas-3.jpg')">
          <div class="container">
            <div class="row">
              <div class="col-lg-5">
                <span>pangkasnesia</span>
                <h1>Pangkas anak-anak</h1>
                <p>
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed
                  do eiusmod tempor incididunt ut labore et dolore
                </p>
                <a href="#" class="primary-btn">Order Now</a>
              </div>
            </div>
          </div>
        </div>
        <div class="single-hero-items set-bg" style="background-image: url('img/pangkas-2.jpg')">
          <div class="container">
            <div class="row">
              <div class="col-lg-5">
                <span>pangkasnesia</span>
                <h1>Pangkas wanita</h1>
                <p>
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed
                  do eiusmod tempor incididunt ut labore et dolore
                </p>
                <a href="#" class="primary-btn">Order Now</a>
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