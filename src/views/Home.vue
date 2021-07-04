<template>
  <div class="home">
    <!-- Page Preloder -->
    <!-- <div id="preloder">
        <div class="loader"></div>
    </div> -->

    <HeaderPangkasnesia />
    <HeroPangkasnesia />
    <ProductBanner />
    <InstaPangkasnesia />
    <PartnerPangkasnesia />
    <FooterPangkasnesia />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderPangkasnesia from "@/components/HeaderPangkasnesia.vue";
import HeroPangkasnesia from "@/components/HeroPangkasnesia.vue";
import ProductBanner from "@/components/ProductBanner.vue";
import InstaPangkasnesia from "@/components/InstaPangkasnesia.vue";
import PartnerPangkasnesia from "@/components/PartnerPangkasnesia.vue";
import FooterPangkasnesia from "@/components/FooterPangkasnesia.vue";
export default {
  name: "Home",
  components: {
    // HelloWorld
    HeaderPangkasnesia,
    HeroPangkasnesia,
    ProductBanner,
    InstaPangkasnesia,
    PartnerPangkasnesia,
    FooterPangkasnesia
  },
};
</script>