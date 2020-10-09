<template>
    <div class="card">
    <img src="https://www.flaticon.com/svg/static/icons/svg/1377/1377194.svg" class="card-img-top" alt="Image Failed to Load">
        <div class="card-body">
            <h5 class="card-title" :product="product" id="product-name">{{product}}</h5>
            <p class="card-text" :manufacturer="manufacturer" id="brand">{{manufacturer}}</p>
            <p class="card-text" :rating="rating" id="rating">Rating: {{rating}}</p>
            <p class="card-text" :price="price" id="price">{{price}}</p>
            <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
        </div>
    </div>
</template>

<script>

export default {
    props: {
        key: String,
        product: String,
        manufacturer: String,
        rating: Number,
        price: Number,
    }

}
</script>

<style>
.card {
    width: 18rem;
    padding: 0.5rem;
    margin: 1rem 0rem;
}


</style>