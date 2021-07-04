<template>
    <!-- Header Section Begin -->
    <header class="header-section">
        <div class="header-top">
            <div class="container">
                <div class="nav-left">
                    <div class="mt-3 mb-3">
                        <i class=" fa fa-envelope"></i> hello.pangkasnesia@gmail.com
                        <span class="ml-3"></span> <i class=" fa fa-phone"></i> +628 22081996
                    </div>
                </div>
            </div>
            <!-- Top Right -->
            <div class="container">
                <div class="nav-right">
                    <div class="mt-3 ">
                        <i class="fa fa-power-off"></i><a href="http://127.0.0.1:8000/login" style="color: #111111;"> Login</a> <a href="http://127.0.0.1:8000/register" style="color: #111111; margin-left: 20px;">Register</a>
                    </div>
                </div>
            </div>
            <!-- End Top Right -->
        </div>
        <div class="container">
            <div class="inner-header">
                <div class="row">
                    <div class="col-lg-2 col-md-2">
                        <div class="logo">
                            <a href="./index.html">
                                <img src="img/logo-pangkasnesia.png" alt="" />
                            </a>
                        </div>
                    </div>
                    <div class="col-lg-7 col-md-7"></div>
                    <div class="col-lg-3 text-right col-md-3">
                        <ul class="nav-right">
                            <li class="cart-icon">
                                Cart &nbsp;
                                <a href="#">
                                    <i class="icon_bag_alt"></i>
                                    <span>{{ keranjangUser.length }}</span>
                                </a>
                                <div class="cart-hover">
                                    <div class="select-items">
                                        <table>
                                            <tbody v-if="keranjangUser.length > 0">

                                                <tr v-for="keranjang in keranjangUser" :key="keranjang.id">
                                                    <td class="si-pic">
                                                        <img class="photo-item" :src="keranjang.photo" alt />
                                                    </td>
                                                    <td class="si-text">
                                                        <div class="product-selected">
                                                        <p>Rp{{ keranjang.price }} x 1</p>
                                                        <h6>{{ keranjang.name }}</h6>
                                                        </div>
                                                    </td>
                                                    <td @click="removeItem(keranjang.id)" class="si-close">
                                                        <i class="ti-close"></i>
                                                    </td>
                                                </tr>
                                                
                                            </tbody>
                                            <tbody v-else>
                                                <tr>
                                                <td>Keranjang kosong</td>
                                                </tr>
                                            </tbody>
                                        </table>
                                    </div>
                                    <div class="select-total">
                                        <span>total:</span>
                                        <h5>Rp{{ totalHarga }}.00</h5>
                                    </div>
                                    <div class="select-button">
                                        <a href="#" class="primary-btn checkout-btn">
                                            <router-link to="/cart" style="color: #FFF;">CHECK OUT</router-link>
                                        </a>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </header>
    <!-- Header End -->
</template>

<script>
export default {
    name: 'HeaderPangkasnesia',
    data() {
        return {
            keranjangUser: []
        }
    },
    methods: {
        removeItem(idx) {

            // Cari id dari item yang akan dihapus
            let keranjangUserStorage = JSON.parse(localStorage.getItem("keranjangUser"));
            let itemKeranjangUserStorage = keranjangUserStorage.map(itemKeranjangUserStorage => itemKeranjangUserStorage.id);
            
            // Cocokan id item dengan id pada storage
            let index = itemKeranjangUserStorage.findIndex(id => id == idx);
            this.keranjangUser.splice(index, 1);

            const parsed = JSON.stringify(this.keranjangUser);
            localStorage.setItem("keranjangUser", parsed);
            window.location.reload();
        }
    },
    mounted() {
        if (localStorage.getItem('keranjangUser')) {
            try {
                this.keranjangUser = JSON.parse(localStorage.getItem('keranjangUser'));
            } catch(e) {
                localStorage.removeItem('keranjangUser');
            }
        }
    },
    computed: {
        totalHarga() {
            return this.keranjangUser.reduce(function(items, data){
                return items + data.price;
            }, 0);
        }
    }
}
</script>

<style scoped>
.photo-item {
  width: 80px;
  height: 80px;
}
</style>