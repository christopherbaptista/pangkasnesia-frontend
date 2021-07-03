<template>
  <div class="home">
    <!-- Page Preloder -->
    <!-- <div id="preloder">
        <div class="loader"></div>
    </div> -->

    <HeaderLoginPangkasnesia />
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
import HeaderLoginPangkasnesia from "@/components/HeaderLoginPangkasnesia.vue";
import HeroPangkasnesia from "@/components/HeroPangkasnesia.vue";
import ProductBanner from "@/components/ProductBanner.vue";
import InstaPangkasnesia from "@/components/InstaPangkasnesia.vue";
import PartnerPangkasnesia from "@/components/PartnerPangkasnesia.vue";
import FooterPangkasnesia from "@/components/FooterPangkasnesia.vue";

export default {
  name: "HomeLogin",
  components: {
    // HelloWorld
    HeaderLoginPangkasnesia,
    HeroPangkasnesia,
    ProductBanner,
    InstaPangkasnesia,
    PartnerPangkasnesia,
    FooterPangkasnesia
  },
};
</script>
