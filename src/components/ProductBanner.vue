<template>
    <!-- Product Banner Section Begin -->
    <section class="product-banner spad">
        <div class="container-fluid">
            <div class="row">
                <div class="col-lg-12 mt-5">
                    <carousel class="product-slider" :items="3" :dots="false" :autoplay="true" :nav="false">
                        <div class="product-item">
                            <div class="pi-pic">
                                <img src="img/products/sisir-3.jpg" alt="" />
                                <ul>
                                    <li class="w-icon active">
                                        <a href="#"><i class="icon_bag_alt"></i></a>
                                    </li>
                                    <li class="quick-view">
                                        <router-link to="/product">
                                            + Quick View
                                        </router-link>
                                    </li>
                                </ul>
                            </div>
                            <div class="pi-text">
                                <div class="catagory-name">Sisir Portable</div>
                                <a href="#">
                                    <h5>Sisir Mini Stainless Steel</h5>
                                </a>
                                <div class="product-price">
                                    $25.00
                                    <span>$35.00</span>
                                </div>
                            </div>
                        </div>                      
                        <div class="product-item">
                            <div class="pi-pic">
                                <img src="img/products/pomade-6.jpg" alt="" />
                                <ul>
                                    <li class="w-icon active">
                                        <a href="#"><i class="icon_bag_alt"></i></a>
                                    </li>
                                    <li class="quick-view"><a href="#">+ Quick View</a></li>
                                </ul>
                            </div>
                            <div class="pi-text">
                                <div class="catagory-name">Hair Styling</div>
                                <a href="#">
                                    <h5>Death Pomade Pop</h5>
                                </a>
                                <div class="product-price">
                                    $36.00
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="pi-pic">
                                <img src="img/products/pomade-1.jpg" alt="" />
                                <ul>
                                    <li class="w-icon active">
                                        <a href="#"><i class="icon_bag_alt"></i></a>
                                    </li>
                                    <li class="quick-view"><a href="#">+ Quick View</a></li>
                                </ul>
                            </div>
                            <div class="pi-text">
                                <div class="catagory-name">Hair Styling</div>
                                <a href="#">
                                    <h5>American Crew Pomade</h5>
                                </a>
                                <div class="product-price">
                                    $45.00
                                </div>
                            </div>
                        </div>
                        <div class="product-item">
                            <div class="pi-pic">
                                <img src="img/products/pomade-4.png" alt="" />
                                <ul>
                                    <li class="w-icon active">
                                        <a href="#"><i class="icon_bag_alt"></i></a>
                                    </li>
                                    <li class="quick-view"><a href="#">+ Quick View</a></li>
                                    <li class="w-icon">
                                        <a href="#"><i class="fa fa-random"></i></a>
                                    </li>
                                </ul>
                            </div>
                            <div class="pi-text">
                                <div class="catagory-name">Hair Styling</div>
                                <a href="#">
                                    <h5>Folti Baffi Italy Pomade</h5>
                                </a>
                                <div class="product-price">
                                    $34.00
                                </div>
                            </div>
                        </div>
                    </carousel>
                </div>
            </div>
        </div>
    </section>
    <!-- Product Banner Section End -->
</template>

<script>
import carousel from 'vue-owl-carousel';

export default {
    name: 'ProductBanner',
    components: {
        carousel
    }
}
</script>

<style scoped>
.product-item {
    margin-right: 25px;
}
</style>