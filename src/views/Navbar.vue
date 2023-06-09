<template>
    <ul class="nav nav-tabs justify-content-center text-white" id="myTab" role="tablist"
        style="background-color: #2874f0; width:94.9rem;">
        <li class="nav-item ms-5 mx-2 p-2">
            <img width="75"
                src="https://static-assets-web.flixcart.com/fk-p-linchpin-web/fk-cp-zion/img/flipkart-plus_8d85f4.png">
            <div class="d-flex align-items-center">
                <a class="fst-italic text-white" style="font-size: 11px; margin-top: -1px;">Explore&nbsp;<span
                        class="text-warning">Plus&nbsp;</span>
                    <img width="10"
                        src="https://static-assets-web.flixcart.com/fk-p-linchpin-web/fk-cp-zion/img/plus_aef861.png">
                </a>
            </div>
        </li>
        <li class="nav-item d-flex align-items-center">
            <div class="input-group col-12-12">
                <input type="text" class="form-control shadow-none search" style="width: 33rem;"
                    placeholder="Search for products, brands and more" @focusin="show = true" @focusout="show = false">
                <a class="input-group-text bg-white" style="color:#2874f0; border-radius: 2px;">
                    <i class="fa fa-search" aria-hidden="true"></i></a>
            </div>
        </li>
        <li class="nav-item d-flex align-items-center ms-5 me-4">
            <div class="dropdown">
                <a type="button" class="btn btn-light shadow-none fw-semibold login-button"
                    @click="$refs.login_ref.showModal()"
                    style="width: 7.5rem; height: 55%; color:#2874f0; padding-top: 1px; border-radius: 2px; border: 1px solid #dbdbdb; font-size: 16px;">Login</a>
                <div class="dropdown-content">
                    <a href="#">New Customer Signup</a>
                    <a href="#">My profile</a>
                    <a href="#">Flipkart Plus zone</a>
                </div>
            </div>
        </li>
        <li class="nav-item d-flex align-items-center me-2">
            <a type="button" class="btn text-white border-0 fw-semibold">Become a Seller</a>
        </li>
        <li class="nav-item d-flex align-items-center">
            <a type="button" class="btn text-white border-0 fw-semibold dropdown-toggle">More</a>
        </li>
        <li class="nav-item d-flex align-items-center">
            <a type="button" class="btn text-white border-0 fw-semibold">
                <img src="/assets/cart-icon.png" class="pb-1" style="width: 27%; height: 27%;">
                <span class="ps-2">Cart</span></a>
        </li>

    </ul>
    <Teleport to="#modals">
        <Login ref="login_ref" />
    </Teleport>
</template>

<script>
import Login from './Login.vue';

export default {
    data() {
        return {
            show: false
        }
    },
    components: {
        Login
    }
}
</script>

<style>
.nav-link {
    color: black;
}

.nav-link:hover {
    color: rgb(22, 182, 250)
}

.show {
    color: aquamarine;
}

a,
img {
    text-decoration: none;
    color: inherit;
    border: none;
    outline: none;
}

.search {
    padding: 0 16px;
    border-radius: 2px 0 0 2px;
    border: 0px;
    font-size: 14px;
    height: 36px;
}

/* .search-dropdown {
    width: 33rem;
    height: 10rem;
    z-index: 99;
} */

/* ._1MRYA1 {
    border-radius: 0 0 2px 2px;
    border-top: 1px solid #e0e0e0;
    position: absolute;
    background-color: #fff;
    color: #000;
    z-index: 9;
    top: 35px;
    display: none;
    box-shadow: 2px 3px 5px -1px rgb(0 0 0 / 50%);
    overflow: hidden;
    white-space: nowrap;
} */

.dropdown {
    position: relative;
    display: inline-block;
}

/* Dropdown Content (Hidden by Default) */
.dropdown-content {
    display: none;
    position: absolute;
    background-color: #f1f1f1;
    min-width: 235px;
    padding: 2px;
    margin-left: -60px;
    box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
    z-index: 1;
}

/* Links inside the dropdown */
.dropdown-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
}

/* Change color of dropdown links on hover */
.dropdown-content a:hover {
    background-color: #ddd;
}

/* Show the dropdown menu on hover */
.dropdown:hover .dropdown-content {
    display: block;
}</style>