<script setup>
import produto from '@/assets/js/product.json'
import 'bootstrap';
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-12">
                <p class="product-title fs-4">
                    {{ produto.product.name }}
                    <br />
                    <span>
                        {{ produto.product.score }} ({{ produto.product.reviews }} avaliações)
                    </span>
                </p>
            </div>
            <div class="col-7">
                <div id="carouselProduto" class="carousel slide">
                    <div class="carousel-inner">
                        <div class="carousel-item" :class="{ 'active': index === 0 }" v-for="(image, index) in produto.product.pictures" :key="index">
                            <img :src="image" :alt="'Imagem ' + (index + 1)" class="img-fluid">
                        </div>
                    </div>
                    <button class="carousel-control-prev" type="button" data-bs-target="#carouselProduto"
                        data-bs-slide="prev">
                        <span class="carousel-control-prev-icon" aria-hidden="true">
                            <svg width="32" height="32" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path d="M14.9991 19L9.83911 14C9.56672 13.7429 9.34974 13.433 9.20142 13.0891C9.0531 12.7452 8.97656 12.3745 8.97656 12C8.97656 11.6255 9.0531 11.2548 9.20142 10.9109C9.34974 10.567 9.56672 10.2571 9.83911 10L14.9991 5" stroke="#000000" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path> </g></svg>
                        </span>
                        <span class="visually-hidden">Previous</span>
                    </button>
                    <button class="carousel-control-next" type="button" data-bs-target="#carouselProduto"
                        data-bs-slide="next">
                        <span class="carousel-control-next-icon" aria-hidden="true">
                            <svg width="32" height="32" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path d="M9 5L14.15 10C14.4237 10.2563 14.6419 10.5659 14.791 10.9099C14.9402 11.2539 15.0171 11.625 15.0171 12C15.0171 12.375 14.9402 12.7458 14.791 13.0898C14.6419 13.4339 14.4237 13.7437 14.15 14L9 19" stroke="#000000" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path> </g></svg>
                        </span>
                        <span class="visually-hidden">Next</span>
                    </button>
                </div>
            </div>
            <div class="col-5">
                <p class="produto-price fs-3">
                    R$
                    {{ produto.product.price }}
                </p>
            </div>
        </div>
    </div>
</template>

<style></style>