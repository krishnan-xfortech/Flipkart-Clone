<template>
    <div class="modal fade" style="margin-top: 80px; margin-left:-100px" id="LoginModal" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <button type="button" class="btn border-0" style="margin-left:675px; font-size: 30px; color:#fff; margin-top: -12px;"
                    @click="hideModal()">✕</button>
                <div class="row rowstyle">
                    <div class="col-4 column-1">
                        <span class="login">Login</span><br>
                        <div class="p-2"></div>
                        <p class="text-2">Get access to your<br>Orders, Wishlist and Recommendations</p>
                        <div class="">
                            <img class="image"
                                src="https://static-assets-web.flixcart.com/fk-p-linchpin-web/fk-cp-zion/img/login_img_c4a81e.png">
                        </div>
                    </div>
                    <div class="col-8 column-2">
                        <form>
                            <div class="input-field">
                                <input type="text" id="name" ref="input_ref" v-model="email"
                                    class="border-0 form-control shadow-none border-bottom bg-transparent"
                                    style="width:21rem; margin-left:-25px; margin-top: -40px; padding-left:1px;" />
                                <label for="name">Enter Email/Mobile number</label>
                            </div>
                            <div class="mt-4" style="font-size: 12px; color:#878787; margin-left: -20px; width:410px;">By
                                continuing, you agree to Flipkart's <a class="" target="_blank" href="/pages/terms">Terms of
                                    Use</a> and <a class="" target="_blank" href="/pages/privacypolicy">Privacy<br>
                                    Policy</a>.
                            </div>
                            <div class="mt-3">
                                <button class="request-otp">Request OTP</button>
                            </div>
                            <div class="" style="margin-top:250px;">
                                <a class="_14Me7y" href="/account/login?signup=true">New to Flipkart? Create an account</a>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { Modal } from 'bootstrap';

export default {
    data() {
        return {
            modal: null,
            email: ''
        }
    },
    mounted() {
        this.modal = new Modal(document.getElementById('LoginModal'));
    },
    methods: {
        showModal() {
            this.modal.show()
            this.email = '';
            setTimeout(() => {
                this.$refs.input_ref.focus()
            }, 100);
        },
        hideModal() {
            this.modal.hide()
        }
    }
}
</script>

<style>
.modal-content {
    border: 0px;
    border-radius: 2px;
    height: 527px;
    width: 675px;
}

.column-1 {
    background-color: #2874f0;
    height: 528px;
    margin-left: 12px;
    margin-top: -46px;
    width: 265px;
    padding-top: 36px;
    padding-left: 33px;
}

.column-2 {
    height: 528px;
    width: 410px;
}

.login {
    font-size: 28px;
    font-weight: 500;
    color: #fff;
}

.text-2 {
    font-size: 18px;
    line-height: 150%;
    color: #dbdbdb;
}

.image {
    padding-top: 138px;
    padding-right:20px;
}

form {
    margin: 50px;
}

.input-field {
    position: relative;
    width: 250px;
    height: 44px;
    line-height: 90px;
}

label {
    position: absolute;
    top: -30px;
    left: -23px;
    font-size: 16px;
    font-weight: 400;
    color: #878787;
    transition: 0.2s all;
    cursor: text;
}

input {
    border: 0;
    outline: 0;
    border-bottom: 2px solid #d3d3d3;
    box-shadow: none;
    color: #111;
}

input:focus~.input-field {
    border-bottom: 1px solid #2874f0;
}

input:focus~label {
    font-size: 13px;
    top: -45px;
    left: -25px;

}

.request-otp {
    background-color: #fb641b;
    border: none;
    color: #fff;
    width: 330px;
    height: 48px;
    font-size: 15px;
    margin-left: -20px;
    border-radius: 2px;
    padding: 10px 20px;
    font-weight: 500;
    transition: box-shadow .2s ease;
    box-shadow: 0 1px 2px 0 rgb(0 0 0 / 20%);
}

._14Me7y {
    color: #2874f0;
    font-weight: 500;
    font-size: 14px;
    margin-left: 30px;
    font-family: sans-serif;
}
</style>