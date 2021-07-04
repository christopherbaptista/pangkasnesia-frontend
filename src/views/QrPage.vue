<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
import VueQrcode from '@chenfengyuan/vue-qrcode';

@Component({
  components: {
    HelloWorld,
    VueQrcode
  },
})
export default class Home extends Vue {

    public isShowingCamera:boolean = false;
    public isScanned:boolean = false;

    public openCamera():void{
        this.isShowingCamera = !this.isShowingCamera;
    }

    public onDecode(decodeString:string) {
        alert(decodeString);
        console.log(decodeString);
        if(decodeString === "Pembayaran berhasil. Nomor transaksi anda #TRF353571") {
            this.isScanned = true;
        }
    }

    public async onInit (promise:any):Promise<any> {
        try {
            await promise;
            console.log("init", promise);
        } catch (error) {
            console.log(error);
            if (error.name === 'NotAllowedError') {
                // 
            } else if (error.name === 'NotFoundError') {
                // 
            } else if (error.name === 'NotSupportedError') {
                // 
            } else if (error.name === 'NotReadableError') {
                // 
            } else if (error.name === 'OverconstrainedError') {
                // 
            } else if (error.name === 'StreamApiNotSupportedError') {
                // 
            }
        } finally {
            // 
        }
    }
}
</script>

<template>
  <div class="home">
    <p>Welcome to the QR Page</p>
    <button @click="openCamera">{{ !isShowingCamera ? 'Scan a QrCode' : 'Exit QR Scanning'}}</button>
    <h3>Some random QR codes</h3>

    <div class="qr-code-wrapper">
        <vue-qrcode 
            :value="'Pembayaran berhasil. Nomor transaksi anda #TRF353571'">
        </vue-qrcode>
        <h2 v-if="isScanned">
            SUCCESS
        </h2>
    </div>
    <qrcode-stream v-if="isShowingCamera" @init="onInit" @decode="onDecode"></qrcode-stream>
  </div>
</template>

<style lang="scss" scoped>
    h2{
        position: absolute;
        color: yellowgreen;
        background: red;
        margin-top: -120px;
        margin-left: 10px;
        transform: rotate(45deg);
        font-weight: bold;
        font-size: 38px;
    }
    p{
        color:#333;
    }
    .qr-code-wrapper{
        padding: 50px;
        width: 300px;
        height: 250px;
        background: #F7F7F7;
        display: block;
        margin: 0 auto;
        border-radius: 7px;
    }
</style>